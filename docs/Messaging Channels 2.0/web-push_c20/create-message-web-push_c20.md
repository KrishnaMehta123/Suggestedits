---
title: Create Message
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: >-
    Refer to the pages listed below to learn more about the following Web Push
    sections:
  pages:
    - type: link
      title: Personalize Message
      url: https://docs.clevertap.com/docs/personalize-message-web-push_c20
    - type: link
      title: Web Push Campaign Stats
      url: https://docs.clevertap.com/docs/web-push-stats_c20
---
## Create a New Campaign

Create a campaign to deliver your Web Push message. To create a new campaign:

1. From the dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **Web Push**. 

<Image title="Web PUSH.png" alt={2854} className="border" border={true} src="https://files.readme.io/06785e3-Web_PUSH.png" />

The campaign page displays.

<Image title="Web_push_Editor_main.png" alt={1109} className="border" width="80%" border={true} src="https://files.readme.io/16ca3e5-Web_push_Editor_main.png" />

Define all the sections and publish the campaign.

## Start Campaign Setup

The *Start here* section displays the setup information. 

This section has the following parts:

* **Start here**:  Displays the list of integrated and available browsers.
* **Qualification criteria**: Here you need to define the criteria for your target audience. You can deliver the web push notification based on *Past behavior/Custom list* or *Live behavior*.
* **Set a goal**: You can track your campaign conversion by setting up a specific goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. This selection is optional.

Define the conversion period by selecting the *Conversion Time*. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, see [Events](doc:events).

<Image title="Push_notification_set_goal_track_conversion.png" alt={919} className="border" border={true} src="https://files.readme.io/4fbbeb2-Push_notification_set_goal_track_conversion.png" />

## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the *Target segment* section. Here, you can create a new segment or use a previously saved user segment from the segment list. 

<Image title="Web_push_Who.png" alt={1140} className="border" border={true} src="https://files.readme.io/ffefe62-Web_push_Who.png" />

You can also create the target audience based on past user behavior and user properties or live (ongoing) user behavior. The latter is helpful to send out real-time, triggered campaigns.

For instance, you can create a live *Inaction within time* campaign that targets users as soon as they add a product to their cart but do not finish transacting within 10 minutes; the golden window within which most users transact on online platforms.

### Deliver Action Based Web Push Notifications

You can trigger a web push message based on an action. For example, a web push message with a promo code can be shown to a set of customers who have just completed a purchase. This will help in incentivizing an existing user. Moreover, such push messages make notifications more contextual and result in increased conversion.

### Filter Users based on Past Behavior

You can also target users basis their past behavior. For example, you might want to target customers who have purchased a specific product in the past. 

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can send a Web Push notification to all the customers from **Mumbai** who are currently subscribed to *Platinum* membership. 

<Image title="User properties whatsapp.png" alt={2376} className="border" border={true} src="https://files.readme.io/5fb2969-User_properties_whatsapp.png" />

The following table explains the various property types:

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Property Type
      </th>

      <th>
        Description
      </th>

      <th>
        Example
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        User Properties
      </td>

      <td>
        Custom [user profile properties](https://docs.clevertap.com/docs/user-profiles#section-user-profile-data-model) that you define and send to CleverTap.
      </td>

      <td>
        Customer Type = Platinum
      </td>
    </tr>

    <tr>
      <td>
        Demographics
      </td>

      <td>
        Demographics filters include *Age* and *Gender*.
      </td>

      <td>
        Age = 25 to 40 years\
        Gender = Female
      </td>
    </tr>

    <tr>
      <td>
        Geography
      </td>

      <td>
        User's coarse location. Filters include *Country*, *Region*, and *City*. CleverTap's SDK can automatically detect this from the user's IP address.
      </td>

      <td>
        Country = United States\
        State = California\
        City = San Francisco
      </td>
    </tr>

    <tr>
      <td>
        Geography Radius
      </td>

      <td>
        User's exact location. You can select a city, and then define the target radius. You can also select multiple cities. You can send this information using CleverTap's SDK. For more information, refer to the [iOS](https://developer.clevertap.com/docs/ios#section-send-location-information-to-clevertap) and [Android](https://developer.clevertap.com/docs/android#section-manually-updating-user-location) developer guides.
      </td>

      <td>
        Locations = San Francisco, USA; Paris, France
      </td>
    </tr>

    <tr>
      <td>
        Reachability
      </td>

      <td>
        Reachability filters include *Has email address*, *Has phone number*, *Unsubscribed email*, and *Unsubscribed SMS*.
      </td>

      <td>
        Unsubscribed email = No
      </td>
    </tr>

    <tr>
      <td>
        App Fields
      </td>

      <td>
        App fields filters include *App Version*, *Device Make*, *Device Model*, *OS Version*, and CleverTap *SDK Version*. This information is sent by CleverTap's SDK for each device that has your app which means a single user can have multiple devices associated with their user profile.
      </td>

      <td>
        OS Version = 10
      </td>
    </tr>
  </tbody>
</Table>

To know more about what segments can be used, see [Segments](doc:segments).

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information on control groups, see [Control Groups](doc:control-groups).

<Image title="control group web push.png" alt={1404} className="border" border={true} src="https://files.readme.io/333e4c4-control_group_web_push.png" />

### Targeting Cap

Sometimes, you want to send a message to only a subset of the qualifying audience (*Target Reach*) for a campaign or avoid sending it if the number of qualified users exceeds the specified number.

A relevant use case is a limited offer where you want to send a fixed number of coupon codes you want to distribute. If the total reach for your campaign exceeds the number of coupon codes you can distribute, you can limit the number of users who will receive the message to exactly the number of coupons you want to distribute.

<Image title="subset_image.png" alt={406} className="border" border={true} src="https://files.readme.io/3aa9241-subset_image.png" />

## Define the Web Push Message Content

Now, you can set up the *What* which is the Web Push campaign content.

 Click *Go To Editor* to create your message. 

<Image title="Webhook_what_without_options.png" alt={1048} className="border" border={true} src="https://files.readme.io/8a73e71-Webhook_what_without_options.png" />

The *Create Web Push Message* window displays.

## Web Push Editor

The web push notification text fields shown below can be personalized for every user based on specific user property or event property values. For more information, refer to [User Profiles](https://docs.clevertap.com/docs/user-profiles).

Enter all the required information. 

<Image title="Web Push What.png" alt={2876} className="border" border={true} src="https://files.readme.io/2a54fa4-Web_Push_What.png" />

* Deep Link: Specify a deep link, so that upon a web push click, the user is taken back to one of your specific webpages, such as the checkout page. With dynamic replacements, you can take the user right back to the webpage of the product they just added to their cart and present them with an incentive to encourage the transaction. 

* Image Link: Specify an image link for the image you wish to send along with the web push message. The supported image ratio for the image is 4:3 and the most commonly preferred image sizes are 512x256 and 1440x720 pixels. The supported file formats are JPG, JPEG, and PNG for desktop. Only JPEG is supported for mobile.

* Icon Link: Specify an icon link. This is primarily used for displaying brand logos. The recommended size of the icon is **192x192 pixels** 

* Time To Live: It defines how long the push message is preserved for delivery if the device is offline or due to OEM device restrictions.

* Custom key-value pairs: It lets you send custom data when a user clicks on the button. This data is not visible to the customers. 

> 🚧 Browser Considerations
>
> Some of the optional items only apply to a certain browser, such as Firefox, Chrome, or KaiOS.

### Preview & Test

Once you are all done setting up the content of your campaign in the *What* section, you have the option to send a test notification to any CleverTap user profile you have marked as a *Test profile*.\
Click the **Preview & Test** button from the message editor to test a message.

## Define the Campaign Schedule

You can set up the *When* to schedule the campaign's start and end.

Past behavior campaigns can be scheduled to run at a specific time:

* On a specific date and time.
* On multiple specified dates and times.
* Recurring at a periodicity you set.

Live campaigns can be set up on a specific event:

* In response to a user event.
* User event/inaction combination (e.g., abandoned cart scenario).
* Based on a date event property value of an event (for example,  a reminder for upcoming travel booking).

<Image title="Push_notification_editor_when.png" alt={978} className="border" border={true} src="https://files.readme.io/4974c50-Push_notification_editor_when.png" />

### Delivery preferences

You can also set the *Do Not Disturb* (DND) hours during which notifications from this Web Push campaign are prevented from going out, either by discarding them or delaying delivery to after DND hours complete, such as 9 PM to 9 AM.

If you want your campaign to adapt delivery times according to the user’s timezone, check the *Timezone* checkbox. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

Since past behavior campaigns can have scheduled times, you have the option to stop a campaign delivery after a certain cut-off time, or even deliver at the specified time in the user’s timezone. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

<Image title="Campaign_Adwords_delivery_preferences.png" alt={777} className="border" border={true} src="https://files.readme.io/8f97d75-Campaign_Adwords_delivery_preferences.png" />

> 📘 Recurring Day
>
> If you specify a recurring day for a campaign such as the 7th of each month, then the campaign will start for the specified day and ignore the creation date. This is a precaution to avoid sending a campaign unintentionally on a prior date.

## Publish Campaign

After previewing the appearance of your overall campaign, finalize your campaign by clicking **Publish Campaign.**

<Image title="campaign_Publish.png" alt={1193} className="border" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png" />
