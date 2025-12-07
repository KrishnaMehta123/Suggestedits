---
title: Create Message
excerpt: Learn how to create a Push campaign using the CleverTap dashboard.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Create a New Push Campaign

Create a campaign to deliver your push message. 
To create a new campaign:

1. From the dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select the messaging channel.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ec0c217-Select_all_channel.png",
        "Select_all_channel.png",
        1360,
        658,
        "#f7f7fa"
      ],
      "border": true,
      "sizing": "80",
      "caption": "Select Messaging Channel"
    }
  ]
}
[/block]

The campaign page displays.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a805f56-Campaign_Creation_Page.jpg",
        "Campaign_Creation_Page.jpg",
        1404,
        619,
        "#fbfafb"
      ],
      "border": true,
      "sizing": "80",
      "caption": "Create Campaign"
    }
  ]
}
[/block]

4. Define all the sections and publish the campaign. 


## Start Campaign Setup

The *Start here* section displays the setup information. 

This section has the following parts:
* **Start here**:  Displays the information for platforms such as FCM, Xiaomi, or iOS. Check that the required platforms are integrated and ready for campaigns. 
* **Qualification criteria**: Deliver the notification by Past Behavior, Custom List, or Live behavior. For more information about segmenting users, refer to [Segments](https://docs.clevertap.com/docs/segments).
* **Set a Goal**: You can track your campaign conversion by setting up a goal. This is optional. You can define your conversion goal further by selecting the Event and Conversion time. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. 

The campaign goal can be as generic or as specific as you want. It can answer questions from *How many users were influenced for purchasing an X amount?* to *How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount?* ". 


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4fbbeb2-Push_notification_set_goal_track_conversion.png",
        "Push_notification_set_goal_track_conversion.png",
        919,
        361,
        "#fafafc"
      ],
      "border": true,
      "caption": "Set a Goal"
    }
  ]
}
[/block]

## Define the Audience

You must indicate the target audience for your campaign from the *Who* section. You can specify your target audience from the *Target segment* section. Here, you can create a new segment or use a previously saved user segment from the *segment* list. 

For Past Behavior segments, you also calculate the estimated reach. 


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/030202d-Push_notification_editor_Who.png",
        "Push_notification_editor_Who.png",
        1168,
        771,
        "#f8f8fc"
      ],
      "border": true,
      "sizing": "80",
      "caption": "Define - Who"
    }
  ]
}
[/block]

### Segment
If you want to create an ad-hoc segment, you can select a type of segment on which to base your campaign. You can create the target based on past user behavior and user properties or live (ongoing) user behavior. The latter is helpful to send out real-time, triggered campaigns.

For instance, you can create a live *Inaction within time* campaign that targets users as soon as they add a product to their cart but do not finish transacting within 10 minutes; that is the golden window within which most users transact on iOS and Android app platforms.

On this basis, you would then set up the *Who* by sending this campaign to all users who qualify or limit the users who qualify under *Estimated reach*. 

### Deliver Action Based Messages
You can trigger a message based on an action. Users receive messages when they perform an action in the app instead of waiting for the next app launch. It makes the messages more contextual and increases conversion. Campaigns with delays and app inbox coupled with a push message do not trigger instant messages.

### Deliver Messages based on Past Behavior (PBS)

You can also target users their past user behavior. For past behavior campaigns, you also have an option to calculate estimated reach. The estimated reach shows the number of users that qualify for the campaign criteria and the number of reachable users via mobile push.


### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to reach users who meet specific criteria. 

For example, you can send a push notification to English-speaking female users who live in the United States. 


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cbc719c-user_properties_all.png",
        "user_properties_all.png",
        486,
        216,
        "#f6f8fc"
      ],
      "border": true,
      "caption": "Filter by User Properties"
    }
  ]
}
[/block]

The following table explains the various property types:


[block:parameters]
{
  "data": {
    "h-2": "Example",
    "h-0": "Property Type",
    "h-1": "Description",
    "0-0": "User Properties",
    "1-0": "Demographics",
    "2-0": "Geography",
    "3-0": "Geography Radius",
    "4-0": "Reachability",
    "5-0": "App Fields",
    "5-1": "App fields filters include *App Version*, *Device Make*, *Device Model*, *OS Version*, and CleverTap *SDK Version*. This information is sent by CleverTap's SDK for each device that has your app which means a single user can have multiple devices associated with their user profile.",
    "4-1": "Reachability filters include *Has email address*, *Has phone number*, *Unsubscribed email*, and *Unsubscribed SMS*.",
    "3-1": "User's exact location. You can select a city, and then define the target radius. You can also select multiple cities. You can send this information using CleverTap's SDK. For more information, refer to the [iOS](https://developer.clevertap.com/docs/ios#section-send-location-information-to-clevertap) and [Android](https://developer.clevertap.com/docs/android#section-manually-updating-user-location) developer guides.",
    "2-1": "User's coarse location. Filters include *Country*, *Region*, and *City*. CleverTap's SDK can automatically detect this from the user's IP address.",
    "1-1": "Demographics filters include *Age* and *Gender*.",
    "0-1": "Custom [user profile properties](https://docs.clevertap.com/docs/user-profiles#section-user-profile-data-model) that you define and send to CleverTap.",
    "1-2": "Age = 25 to 40 years\nGender = Female",
    "2-2": "Country = United States\nState = California\nCity = San Francisco",
    "0-2": "Customer Type = Platinum",
    "3-2": "Locations = San Francisco, USA; Paris, France",
    "5-2": "OS Version = 10",
    "4-2": "Unsubscribed email = No"
  },
  "cols": 3,
  "rows": 6
}
[/block]

To know more about what segments can be used, see [Segments](doc:segments).

### Constant event property

This is an advanced feature that allows you to hold a property constant across the selected events. For more information, refer to [Constant Event Property](doc:constant-property).

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information on control groups, see [Control Groups](doc:control-groups).


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0eacc15-Control_Group_Editor.png",
        "Control_Group_Editor.png",
        933,
        549,
        "#fbfbfc"
      ],
      "caption": "Control Group"
    }
  ]
}
[/block]

### Targeting Cap

You can limit the number of users receiving the message. 

A relevant use case is a limited offer where you want to distribute a fixed number of coupon codes. If the total reach for your campaign exceeds the number of coupon codes you can distribute, then you can limit the number of users who will receive the message to precisely the number of coupons you want to distribute.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/20d412f-Target_Cap.jpg",
        "Target_Cap.jpg",
        835,
        288,
        "#fafbfc"
      ],
      "caption": "Target Cap",
      "border": true
    }
  ]
}
[/block]

## Define Message Content

You can have up to four variations to message content in the *What* section:

  * Single Message
  * AB Test
  * Split Delivery
  * By User Property

Click *Go To Editor* to create your message. 
## Push Editor
The Push Editor allows you to create and edit beautiful and timely messages for your push campaign. From the *What* section, click *Go To Editor* to create your message. This section displays the editor to create your push message. You can see various options that will help you create a contextual and timely message. 

Enter the details. You can use the *@* personalization or *{{}}* to add [personalization](https://docs.clevertap.com/docs/personalize-message-all) for your message. Enter the required details to create the message.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/46013be-push_main.png",
        "push_main.png",
        971,
        621,
        "#d4cbd9"
      ],
      "border": true
    }
  ]
}
[/block]


You can add a fixed (or with dynamic replacements) URL for Android (Image only) and iOS (Image and video) for rich push notifications.



[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/eeec895-Push_notification_image_URL_Android.png",
        "Push_notification_image_URL_Android.png",
        1274,
        666,
        "#e1dbe6"
      ],
      "border": true
    }
  ]
}
[/block]

You can add an image carousel with each image having its own caption, sub caption, and call to action URL (fixed or with dynamic replacements) to your iOS push notifications.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b0bb0ab-Push_notification_ios_advanced_editor.png",
        "Push_notification_ios_advanced_editor.png",
        1294,
        2241,
        "#f4f2f6"
      ],
      "border": true,
      "sizing": "80"
    }
  ]
}
[/block]

You can add default or custom (fixed or with dynamic replacements) sound files to your Android and iOS push notifications.

You can add a deep link (fixed or with dynamic replacement) to the Android or iOS push notification and lead the users to specific screens when they click it.



[block:image]
{
  "images": [
    {
      "image": []
    }
  ]
}
[/block]


### Push notification delivery
You can further increase the delivery of push notifications by sending a copy of the same message to App Inbox. For more information, see [Optimize Delivery](doc:push-optimize-delivery).

### Advanced iOS Settings
#### Rich Media 

Upload or add images or carousel for your push notifications.

#### Other Media 

#### Sound File 
You have to specify the name of the sound file which is included in your app bundle. Apple supports .aiff, .caf and .wav extensions. 

#### Badge Count 
This updates the badge count for your app to the one specified while creating the campaign. Please note that this does not increment the badge count or set the value to 0 (zero) to hide the badge number. This should be handled manually at the application level.

#### Category 
You can input the name of the category while creating the campaign. Each category has to be registered with the app. Each such category is associated with actions that the user can perform when a notification of rich media type is delivered. Each category can have up to four actions associated with it, although the number of actions actually displayed depends on the type of notification delivered. This provides users the ability to take multiple actions for the notification. 


[block:callout]
{
  "type": "success",
  "body": "A single media push notification can have two buttons such as, *Buy Now* and *Save for Later*.",
  "title": "Multiple Buttons Example"
}
[/block]


#### Content Available
If you include the content-available key with a value of 1 to send out a silent notification to your users. It will not alert the user in any way (update badge count/play a sound/show a notification), but it will wake your app up in the background so you can fetch new content and prepare it for the next time the user opens your app.

Key: content-available
Value: 1

#### Deep Link/Open URL
Deep links allow you to land the user to a particular part of your app. Your app’s OpenURL method is called with the deep link specified here. If you want to use external URLs, then you have to whitelist the IPs or provide http/https before the URL so they can be handled properly by the SDK.

#### Mutable Content
Check this box if you would like to send the mutable-content flag along with your payload. This invokes your app’s notification service extension. For more information, refer to [Modifying Content in Newly Delivered Notifications](https://developer.apple.com/documentation/usernotifications/modifying_content_in_newly_delivered_notifications) in the Apple documentation.

### Advanced Android Settings

#### Add Custom Actions to Android Notifications

A simple way to urge users to respond to your calls to action is by adding button-like actions right into your Android push notifications. 


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/630d0b1-Push_notification_android_action_button.png",
        "Push_notification_android_action_button.png",
        1307,
        627,
        "#e2dce7"
      ],
      "border": true,
      "sizing": "80"
    }
  ]
}
[/block]

Once set up, the various calls to action would display below the push as displayed below.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a91ddec-Push_notification_example.jpg",
        "Push_notification_example.jpg",
        1080,
        895,
        "#2e2d2a"
      ],
      "border": false
    }
  ]
}
[/block]

#### Notification Priority
You can set these priority levels from the CleverTap dashboard as you create your Android push campaigns. Notification tray priority


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bc0cf2e-campaign_Android_notification_tray_priority.png",
        "campaign_Android_notification_tray_priority.png",
        687,
        332,
        "#fafbfc"
      ],
      "border": true
    }
  ]
}
[/block]

Have your app running our latest SDK (versions v3.1.4 or higher) and follow the steps outlined above to send actionable push notifications and set notification priority on Android devices.

#### Notification Tray Priority
On Android, you can also set a priority level for each notification to influence how prominently it is displayed. The higher the priority, the more noticeable it will be.

##### Default Priority
Use most of your messages that are not time-sensitive, such as general notifications and promotional offers.

##### High Priority
Use for important communications that require extra attention, such as chat messages. These will also display as heads-up notifications and be given a higher priority in the user’s tray. Heads up notifications are notifications that pop up on your screen from the top even when you are using other apps. For example, receive a message on your chat app when you’re using the food delivery app. This feature is available for Android N (API 25) and below. For Android Oreo and above, define the priority in the *Notification Channel*.  

##### Maximum Priority
Use for urgent, time-sensitive notifications. These notifications will get higher placement inside the user’s tray and display as heads-up notifications.

####Collapse Key
To replace an existing notification with the same collapse key, you can use the collapse notification option. For example, if push X and push Y have a collapse key A. Push X notification is present on the mobile device when push Y notification is received. The push X notification will no longer be visible (it will be collapsed), and push Y will be displayed. The collapse key must be added under the collapse notification field. For more information, see [Collapse Key](doc:collapse-key).

####Custom key-value pair 

Send custom data with the notification payload. This payload allows the app to perform any business logic preconfigured within the app. For example, you can send a key *CouponCode* and its value as FREE200. This key tells the app the user assigned for the coupon code. 

### Preview & Test

Once you are all done setting up the content of your campaign in the *What* section, you have the option to send a test push notification to any CleverTap user profile you have marked as a *Test profile*.
Click the **Preview & Test** button from the message editor to test a message.


### Message Types
You can create the following types of messages:

* Single Message
* AB Test
*  Split Delivery
*  By User Property

### Single Message
This message type allows a single message copy to be set up for the entire audience. This message copy can be [personalized](https://docs.clevertap.com/docs/personalize-message-all) for each qualifying user. This message type is best suited for use cases where the message doesn’t vary much based on user properties such as language, geography, and so on.


### A/B Testing
A/B testing helps you understand what type of message copy works best to get clicks from users.

You can test up to three message variants on a test group, and the variant that gets the most clicks is declared the winning variant and is automatically sent to the rest of your target audience.

When creating multiple variants for a campaign, you can also auto-copy what is already present in a current variant.



[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4d99162-AB_Test_all.png",
        "AB_Test_all.png",
        881,
        633,
        "#dcdddd"
      ],
      "border": true
    }
  ]
}
[/block]

###Split Delivery
With split delivery, you can decide what percentage of your audience receives each message variant for the campaign duration.




[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/890fc40-Push_notification_split_delivery.png",
        "Push_notification_split_delivery.png",
        992,
        749,
        "#e7e7e7"
      ],
      "border": true
    }
  ]
}
[/block]




[block:image]
{
  "images": [
    {
      "image": []
    }
  ]
}
[/block]


#### Split Delivery to Past Behavior Segments
For campaigns sent to *Past Behavior Segments* (grouping of users based on what they have done in the past), you have two options: launch the A/B test to a percentage of your target audience or send out an absolute number of messages. In either case, we deliver the variants equally to the test audience.

For example:
  * If you are testing three messages (e.g., Variant A, Variant B, Variant C).
  * Your campaign reach is 2,000,000 users.
  * You choose a test population of 15% of campaign reach (300,000 users).

Then, we send:
  * Variant A to 100,000 users.
  * Variant B to 100,000 users.
  * Variant C to 100,000 users.

After delivering 300,000 messages, we calculate the winning message over this test group based on the number of click-throughs. In this example, we then automatically send the winning message to the remainder of your target audience, which is 1,700,000 users.

Note that for A/B testing, we ensure there is always an equal number of messages sent for each variant, so there is no bias introduced during the test phase and that the best-performing message is always declared the winner.

#### Split Delivery to Live User Segments 

With campaigns sent to live user segments (triggered campaigns), messages are delivered immediately when a user’s activity matches your selected criteria. For example, you can send a message when the user has completed a booking or purchase. Because it is impossible to determine the reach of triggered campaigns upfront, you need to decide how many total messages to send for A/B testing before a winner is declared.


[block:callout]
{
  "type": "success",
  "body": "If you select 500 users as your test audience, we will alternate delivery of Variant A and Variant B as users qualify for the campaign. After a total of messages are sent (Variant A – 250 and Variant B – 250), we then decide the winner based on the number of clicks and continue only with this winning message for the duration of the campaign.",
  "title": "Triggered Campaign Example"
}
[/block]

Deciding on a test audience for A/B testing triggered campaigns requires some estimation. We recommend you check the total messages sent for similar triggered campaigns in the past to get a sense of how many users may qualify. If you select a test audience that is too small such as 25 users, you will get a statistically insignificant sample. Suppose your test group size exceeds the total number of users who ultimately qualify for that campaign. In that case, no winner will be declared, and each message variant will be alternatively delivered for the campaign's duration.

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be sending a localized update to people based on their preferred language.

Similar to creating A/B test variants, you can use the + button to add multiple variants based on a user property value. In the example below, we have used the *Customer Type* user property so users with different customer type property values will receive corresponding copies of the campaign based on their different levels (Silver, Gold, or Platinum).


## Define Campaign Schedule

You can set up the *When* section to schedule the campaign start and end using the options below:

Past behavior campaigns can be scheduled to run:

  * On a specific date and time.
  * On multiple specified dates and times.
  * Recurring at a periodicity you set.

Live campaigns can be set up on a specific event:
  * In response to a user event.
  * User event/inaction combination (e.g., abandoned cart scenario).
  * Based on a date event property value of an event (for example,  a reminder for upcoming travel booking).

### Delivery preferences
 
You can apply global campaign limits to determine how many push notifications each app user receives per day. If you want to override these settings for an important campaign, you can click on the *Don’t apply global campaign limits to this campaign* checkbox.

You can also click the *Advanced* checkbox to specify *Do Not Disturb* (DND) hours during which notifications from this push campaign are prevented from going out, either by discarding them or delaying delivery after DND hours such as 9 PM to 9 AM.

Since past behavior campaigns can have scheduled times, you have the option to stop a campaign delivery after a certain cut-off time or even deliver at the specified time in the user’s timezone. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5e3de30-Push_notification_editor_when.png",
        "Push_notification_editor_when.png",
        978,
        485,
        "#fbfaf8"
      ],
      "border": true
    }
  ]
}
[/block]




[block:callout]
{
  "type": "info",
  "title": "Recurring Day",
  "body": "If you specify a recurring day for a campaign such as the 7th of each month, then the campaign will start for the specified day and ignore the creation date. This is a precaution to avoid sending a campaign unintentionally on a prior date."
}
[/block]


## Publish Campaign

After testing and once you are satisfied with the appearance of your campaign, finalize your campaign with the following steps:
1. Click **Continue** to view your campaign summary. The overview page displays.
2. View your campaign summary, then click **Publish Campaign**.




[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b521e92-campaign_Publish.png",
        "campaign_Publish.png",
        1193,
        356,
        "#f0f0fc"
      ],
      "border": true
    }
  ]
}
[/block]