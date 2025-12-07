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
[block:api-header]
{
  "title": "Create a New Campaign"
}
[/block]
Create a campaign to deliver your WhatsApp message. Follow the steps below to create a new WhatsApp campaign:

1. From the CleverTap dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **WhatsApp**. 



[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3ffe7bd-Whatsapp_Campaign.png",
        "Whatsapp Campaign.png",
        2844,
        1242,
        "#f7f6f8"
      ],
      "border": true
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
        "https://files.readme.io/19ccbc0-whatsapp_sections.png",
        "whatsapp sections.png",
        2352,
        1808,
        "#f3f2f6"
      ],
      "border": true
    }
  ]
}
[/block]
Define all the sections and publish the campaign.


## Start Campaign Setup

The *Start here* section displays the setup information. 

This section has the following parts:
* **Start here**: Check that the required platforms are integrated and ready for campaigns. 
* **Qualification criteria**: Deliver the notification based on *Past behavior*, [Custom list](doc:custom-list-segments), or *Live behavior* For more information about segmenting users, refer to [Segments](https://docs.clevertap.com/docs/segments).
* **WhatsApp Service Provider**: Select the available WhatsApp service provider from the list.
* **Set a goal**:  You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve with the campaign. This selection is optional.

 

Define the conversion period by selecting the *Conversion Time*. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, see [Events](https://docs.clevertap.com/docs/events).
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b582a37-Push_notification_set_goal_track_conversion.png",
        "Push_notification_set_goal_track_conversion.png",
        919,
        361,
        "#fafafc"
      ],
      "border": true
    }
  ]
}
[/block]
## Define the Audience

You must indicate the target audience for your WhatsApp campaign. You can target your WhatsApp campaign to a new user segment by clicking on the **Target Segment** section. Here, you can create a new segment or use a previously saved user segment from the *segment* list. 



[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cb455cd-WA_Who.png",
        "WA Who.png",
        2726,
        1046,
        "#faf9fd"
      ],
      "border": true
    }
  ]
}
[/block]
You can create the target based on past user behavior and user properties or live (ongoing) user behavior. The latter is helpful to send out real-time, triggered campaigns.

For instance, you can create a live *Inaction within time* campaign that targets users as soon as they add a product to their cart but do not finish transacting within 10 minutes; the golden window within which most users transact on online platforms.

### Deliver Action Based WhatsApp Notifications
You can trigger a WhatsApp message to users when they perform a specific action. This makes notifications more contextual and increases conversion. For example, sending a cab booking link to customers who have just booked a hotel or flight.

### Deliver WhatsApp Notifications based on Past Behavior (PBS)
You can also target users basis their past behavior. For example, you might want to target customers who have purchased a specific product in the past. 

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to reach users who meet specific criteria. 

For example, you can send a WhatsApp notification to all the customers from **Mumbai** who are currently subscribed to *Platinum* membership. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d56a113-User_properties_whatsapp.png",
        "User properties whatsapp.png",
        2376,
        714,
        "#e6decb"
      ],
      "border": true
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

###Constant event property

You can also hold a property constant across the selected events.  For more information, see [Constant Event Property](doc:constant-property).

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information, refer to [Control Groups](doc:control-groups).
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b79e920-Control_Group_Editor.png",
        "Control_Group_Editor.png",
        933,
        549,
        "#fbfbfc"
      ],
      "border": true
    }
  ]
}
[/block]
### Targeting Cap

In certain cases, you may need to send a message to only a subset of the qualifying audience (*Target Reach*) for a campaign or avoid sending it if the number of qualified users exceeds the specified number.

A relevant use case is a limited offer where you want to send a fixed number of coupon codes you want to distribute. If the total reach for your campaign exceeds the number of coupon codes you can distribute, you can limit the number of users who will receive the message to exactly the number of coupons you want to distribute.




[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3aa9241-subset_image.png",
        "subset_image.png",
        406,
        87,
        "#5faeb1"
      ],
      "border": true
    }
  ]
}
[/block]
## Define the Message Content

Now, you need to set up the *What* section where you have to define the content for the WhatsApp campaign  Click *Go To Editor* to create your message. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3af6c8f-Whatsapp_What.png",
        "Whatsapp What.png",
        1092,
        368,
        "#f7f3f6"
      ],
      "border": true
    }
  ]
}
[/block]
## WhatsApp Editor 

Select from the approved templates.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b4f4fbf-whatsapp_editor.png",
        "whatsapp editor.png",
        2772,
        1064,
        "#e1dde3"
      ],
      "border": true
    }
  ]
}
[/block]
Fill in the details and click **Done**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/98aa909-Whatsapp_editor_create_message.png",
        "Whatsapp_editor_create_message.png",
        1238,
        689,
        "#ebe2ee"
      ],
      "border": true
    }
  ]
}
[/block]
### Preview & Test

Once you are all done setting up the content of your campaign in the *What* section, you have the option to send a test notification to any CleverTap user profile you have marked as a *Test profile*.
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

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/748dd43-WhatsApp_When.png",
        "WhatsApp When.png",
        2566,
        910,
        "#fcfbfa"
      ],
      "border": true
    }
  ]
}
[/block]
###Delivery preferences
 
In certain scenarios, you might not want a campaign to run actively on a particular day and time. In such cases, you can set the frequency for that particular campaign.

You can select the *Do Not Disturb* (DND) hours during which messages from this Whatsapp campaign are prevented from going out, either by discarding them or delaying delivery after DND hours complete, such as 9 PM to 9 AM.  

If you want your campaign to adapt delivery times according to the user’s timezone, check the *Timezone* checkbox. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

Additionally, you can check the *Cut-Off* checkbox to avoid sending messages to users after a set cut-off time. This is important for time-sensitive campaigns, for example, live events. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a6cb503-Whatsapp_DP.png",
        "Whatsapp DP.png",
        1466,
        974,
        "#fbfcfd"
      ],
      "border": true
    }
  ]
}
[/block]
## Publish Campaign

After previewing the appearance of your overall campaign, finalize your campaign by clicking **Publish Campaign.**


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