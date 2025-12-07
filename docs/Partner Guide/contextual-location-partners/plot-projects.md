---
title: Plot Projects
excerpt: Contextual Location Partner
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

[Plot Projects](https://www.plotprojects.com/), a leading geofencing and location data platform, helps boost your brand sales and engage your users effectively. CleverTap and Plot Projects integration allows you to segment users and engages with them based on the places they visit. For example, you can segment all frequent users to a cafe and send them an anniversary bash campaign.

For any queries about Plot Projects, refer to the [Plot Projects FAQs](https://www.plotprojects.com/faqs/).

# Prerequisite for Integration

The following are the prerequisites for this integration:

* You must have an account with Plot Projects.
* You must have an account with CleverTap.

# Integrate CleverTap with Plot Projects

This process involves the following two major steps:

1. [Set up a Listening Campaign in Plot Projects Dashboard](doc:plot-projects#set-up-a-listening-campaign-in-plot-projects-dashboard).
2. [Integrate with your App](plot-projects#integrate-with-your-app).

## Set up a Listening Campaign in Plot Projects Dashboard

Plot Projects provides the *Geo* SDK that connects with the CleverTap SDK. After connecting, you need to set up a listening campaign in the Plot Projects dashboard to track the travel history of users. To do so, proceed as follows:

1. Create the locations you want to track. It can be either a single location or a large set of locations you may want to track.

<Image title="Creating a single location to track from the Plot Projects Dashboard" alt={1232} align="center" width="80%" border={true} src="https://files.readme.io/2c49e86-Track_Single_Location.png">
  Creating a Single Location to Track
</Image>

<Image title="Creating a large set of locations to track from the Plot Projects Dashboard" alt={1232} align="center" width="80%" border={true} src="https://files.readme.io/8dcb98a-Track_a_Large_Set_of_Locations.png">
  Creating a Large Set of Locations to Track
</Image>

2. Create a **Plot Projects Listening Campaign**. It defines the segment to which the users will be added after visiting the target locations. You have many options for Plot Project Listening campaigns, including:
   * Trigger on geofences, polygons, and/or beacons
   * Trigger on entering, exiting, or dwell
   * Define opening hours per location
   * Define the start and end dates of the campaign

<Image title="Creating a listening campaign from the Plot Projects dashboard" alt={1386} align="center" border={true} src="https://files.readme.io/769e163-Create_Listening_Campaign.png">
  Creating a Plot Projects Listening Campaign
</Image>

3. Set the field *Listening Campaign Data* with the tag key value in JSON format.

```json
{"key": "visited_train_station"}
```

Users are now automatically added to the corresponding segments in your CleverTap dashboard.

## Integrate with your App

After setting up the Listening Campaign, your app will know the user's location. To send this data to the CleverTap dashboard, integrate the CleverTap SDK and the Plot Projects SDK into your application. Plot Projects triggers a CleverTap event that is available on the *Events* page. You can create a segment of users based on this event, filter users with specific attributes, and engage with them.

### iOS Integration

Perform [CleverTap iOS integration](doc:ios-quickstart-guide) and [Plot Projects iOS SDK integration](https://files.plotprojects.com/documentation/ios/3.5.0/how-to-guides/iOS-integration-guide/). You can then track geotrigger events from Plot Projects in CleverTap.

To receive *geotrigger* events from Plot Projects, add the `plotHandleGeotriggers` method shown below to your `AppDelegate.m file`. In that method, you also call the CleverTap API to send the event. 

```objectivec
- (void)plotHandleGeotriggers:(PlotHandleGeotriggers*) geotriggerHandler {
    for (PlotGeotrigger* geotrigger in geotriggerHandler.geotriggers) {
        NSString* data = [geotrigger.userInfo objectForKey:PlotGeotriggerDataKey];
        NSString *now = [NSString stringWithFormat:@"%.f",[[NSDate date] timeIntervalSince1970]];
        NSDictionary *props = [NSDictionary dictionaryWithObject:now forKey:@"Date"];
        [[CleverTap sharedInstance] recordEvent:data withProps:props];
        NSLog(@"Sending event with properties:(%@,%@)",data,props);
    }
    [geotriggerHandler markGeotriggersHandled:geotriggerHandler.geotriggers];
}
```

The `plotHandleGeotriggers` method, presented above, sends an event to CleverTap using the data field set in the dashboard as key and the current timestamp as value.

### Android Integration

Perform [CleverTap Android integration](doc:android-quickstart-guide) and [Plot Projects Android SDK integration](https://files.plotprojects.com/documentation/android/3.13.0/how-to-guides/Android-integration-guide/). After doing so, you can track geotrigger events from Plot Projects in CleverTap.

To receive geotrigger events from Plot Projects, create a class that extends `GeotriggerHandlerBroadcastReceiver` class. Call the CleverTap API to send the event.

```java
public class MyGeotriggerHandlerBroadcastReceiver extends GeotriggerHandlerBroadcastReceiver {
   private static final String LOG_TAG = "MyGeotriggerHandler";
   @Override
   public List<Geotrigger> handleGeotriggers(List<Geotrigger> list) {
       for (Geotrigger geotrigger: list)
           try {
               JSONObject jsonObject = new JSONObject(geotrigger.getData());
               String key = jsonObject.getString("key");
               CleverTapAPI cleverTap = CleverTapAPI.getInstance(getContext());
               cleverTap.pushevent(key);
               Log.d(LOG_TAG, "sent CleverTap event: " + key);
           } catch (CleverTapException e) {
               // handle CleverTap exception
           } catch (JSONException e) {
               // handle JSON exception
           }
       return list;
   }
}
```

The `MyGeotriggerHandlerBroadcastReceiver` class, presented above, records an event for CleverTap using the data field set in the dashboard as a key.

For the Android app to identify the receiver, add the following to the `AndroidManifest.xml` file:

```xml
<receiver
    android:name=".MyGeotriggerHandlerBroadcastReceiver"
    android:permission="false">
    <intent-filter>
        <action android:name="${applicationId}.plot.HandleGeotriggers" />
    </intent-filter>
</receiver>
```
