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
    Refer to the pages listed below to learn more about the following WhatsApp
    sections:
  pages:
    - type: link
      title: Personalize Message
      url: https://docs.clevertap.com/docs/personalize-message-whatsapp_c20
    - type: link
      title: WhatsApp Campaign Stats
      url: https://docs.clevertap.com/docs/whatsapp-stats_c20
---
## Create a New Campaign

Create a campaign to deliver your WhatsApp message. Follow the steps below to create a new WhatsApp campaign:

1. From the CleverTap dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **WhatsApp**. 

<Image title="Whatsapp Campaign.png" alt={2844} className="border" border={true} src="https://files.readme.io/3ffe7bd-Whatsapp_Campaign.png" />

The campaign page displays.

<Image title="whatsapp sections.png" alt={2352} className="border" border={true} src="https://files.readme.io/19ccbc0-whatsapp_sections.png" />

Define all the sections and publish the campaign.

## Start Campaign Setup

The *Start here* section displays the setup information. 

This section has the following parts:

* **Start here**: Check that the required platforms are integrated and ready for campaigns. 
* **Qualification criteria**: Deliver the notification based on *Past behavior*, [Custom list](doc:custom-list-segments), or *Live behavior* For more information about segmenting users, refer to [Segments](https://docs.clevertap.com/docs/segments).
* **WhatsApp Service Provider**: Select the available WhatsApp service provider from the list.
* **Set a goal**:  You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve with the campaign. This selection is optional.

Define the conversion period by selecting the *Conversion Time*. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, see [Events](https://docs.clevertap.com/docs/events).

<Image title="Push_notification_set_goal_track_conversion.png" alt={919} className="border" border={true} src="https://files.readme.io/b582a37-Push_notification_set_goal_track_conversion.png" />

## Define the Audience

You must indicate the target audience for your WhatsApp campaign. You can target your WhatsApp campaign to a new user segment by clicking on the **Target Segment** section. Here, you can create a new segment or use a previously saved user segment from the *segment* list. 

<Image title="WA Who.png" alt={2726} className="border" border={true} src="https://files.readme.io/cb455cd-WA_Who.png" />

You can create the target based on past user behavior and user properties or live (ongoing) user behavior. The latter is helpful to send out real-time, triggered campaigns.

For instance, you can create a live *Inaction within time* campaign that targets users as soon as they add a product to their cart but do not finish transacting within 10 minutes; the golden window within which most users transact on online platforms.

### Deliver Action Based WhatsApp Notifications

You can trigger a WhatsApp message to users when they perform a specific action. This makes notifications more contextual and increases conversion. For example, sending a cab booking link to customers who have just booked a hotel or flight.

### Deliver WhatsApp Notifications based on Past Behavior (PBS)

You can also target users basis their past behavior. For example, you might want to target customers who have purchased a specific product in the past. 

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to reach users who meet specific criteria. 

For example, you can send a WhatsApp notification to all the customers from **Mumbai** who are currently subscribed to *Platinum* membership. 

<Image title="User properties whatsapp.png" alt={2376} className="border" border={true} src="https://files.readme.io/d56a113-User_properties_whatsapp.png" />

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

### Constant event property

You can also hold a property constant across the selected events.  For more information, see [Constant Event Property](doc:constant-property).

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information, refer to [Control Groups](doc:control-groups).

<Image title="Control_Group_Editor.png" alt={933} className="border" border={true} src="https://files.readme.io/b79e920-Control_Group_Editor.png" />

### Targeting Cap

In certain cases, you may need to send a message to only a subset of the qualifying audience (*Target Reach*) for a campaign or avoid sending it if the number of qualified users exceeds the specified number.

A relevant use case is a limited offer where you want to send a fixed number of coupon codes you want to distribute. If the total reach for your campaign exceeds the number of coupon codes you can distribute, you can limit the number of users who will receive the message to exactly the number of coupons you want to distribute.

<Image title="subset_image.png" alt={406} className="border" border={true} src="https://files.readme.io/3aa9241-subset_image.png" />

## Define the Message Content

Now, you need to set up the *What* section where you have to define the content for the WhatsApp campaign  Click *Go To Editor* to create your message. 

<Image title="Whatsapp What.png" alt={1092} className="border" border={true} src="https://files.readme.io/3af6c8f-Whatsapp_What.png" />

## WhatsApp Editor

Select from the approved templates.

<Image title="whatsapp editor.png" alt={2772} className="border" border={true} src="https://files.readme.io/b4f4fbf-whatsapp_editor.png" />

Fill in the details and click **Done**.

<Image title="Whatsapp_editor_create_message.png" alt={1238} className="border" border={true} src="https://files.readme.io/98aa909-Whatsapp_editor_create_message.png" />

### Preview & Test

Once you are all done setting up the content of your campaign in the *What* section, you have the option to send a test notification to any CleverTap user profile you have marked as a *Test profile*.\
Click the **Preview & Test** button from the message editor to test a message.

### Message Types

You can create the following types of messages:

* [Single Message](https://docs.clevertap.com/docs/push-campaign#section-single-message)
* [By User Property](https://docs.clevertap.com/docs/push-campaign#section-by-user-property)

### Single Message

In this campaign, we send the same message to all users who qualify as your target audience. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between properties such as language, geography, or any other user properties.

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. For example,  sending a localized update to people based on their preferred language.

You can use the **+** button while defining the target segment to add multiple variants based on a user property value.

## Define the Campaign Schedule

The WhatsApp message campaign needs to be scheduled to run actively for a specific timeline. To define the schedule for your Whatsapp campaign, you need to specify the *Start date and time* and *End date and time* under the *When* section. You also have the option to start a campaign immediately by selecting *Now*.  Besides, you can also define a delay (by seconds, minutes, hours, or days) once a user qualifies for the target segment. Once you define the schedule and click on *Done*, the campaign will be triggered and terminated as per the defined timings.

<Image title="WhatsApp When.png" alt={2566} className="border" border={true} src="https://files.readme.io/748dd43-WhatsApp_When.png" />

### Delivery preferences

In certain scenarios, you might not want a campaign to run actively on a particular day and time. In such cases, you can set the frequency for that particular campaign.

You can select the *Do Not Disturb* (DND) hours during which messages from this Whatsapp campaign are prevented from going out, either by discarding them or delaying delivery after DND hours complete, such as 9 PM to 9 AM.  

If you want your campaign to adapt delivery times according to the user’s timezone, check the *Timezone* checkbox. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

Additionally, you can check the *Cut-Off* checkbox to avoid sending messages to users after a set cut-off time. This is important for time-sensitive campaigns, for example, live events. 

<Image title="Whatsapp DP.png" alt={1466} className="border" border={true} src="https://files.readme.io/a6cb503-Whatsapp_DP.png" />

## Publish Campaign

After previewing the appearance of your overall campaign, finalize your campaign by clicking **Publish Campaign.**

<Image title="campaign_Publish.png" alt={1193} className="border" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png" />
