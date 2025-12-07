---
title: Create Message_Message On User Property
excerpt: Learn how to create an SMS campaign using the CleverTap dashboard.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Create a New Campaign

Follow the steps below to create a new SMS campaign:

1. From the CleverTap dashboard, select _Campaigns_.
2. Click **+ Campaign**.
3. From the _Messaging Channels_ list, select **SMS**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d0a3e77-SMS_Create.png",
        "SMS Create.png",
        2796
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



The _Campaign_ page displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3afb28a-SMS_Editor_main.png",
        "SMS_Editor_main.png",
        1107
      ],
      "align": "center",
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]



Define all the sections and publish the campaign. 

## Start Campaign Setup

The _Start here_ section displays the setup information.  
This section has the following parts:

- **Qualification criteria**: Here, you need to define the criteria for your target audience. You can deliver the SMS based on _Past behavior/Custom list_ or _Live behavior_.
- **SMS Service Provider**:  Here, you need to select your SMS service provider or a provider group.
- **Goal**: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign performance. This selection is optional. Define the conversion period by selecting the _Conversion Time_. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, see [Events](doc:events).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6001c3f-Push_notification_set_goal_track_conversion.png",
        "Push_notification_set_goal_track_conversion.png",
        919
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



## Define the Audience

You must indicate the target audience for your push campaign. You can target your SMS campaign to a new user segment by clicking on the **Target segment** section. Here, you can create a new ad-hoc segment or use a previously saved user segment from the _segment_ list. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/074ff4c-SMS_Who.png",
        "SMS_Who.png",
        961
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



You can also create the target based on past user behavior and user properties or live (ongoing) user behavior. the latter is useful to send out real-time, triggered SMS campaigns.

> 🚧 Delay > 24 Hours
> 
> We recommend creating a Past Behavior campaign for all campaigns where the delay is greater than 24 hours for a live inaction campaign.

For instance, you can create a live _Inaction within time_ campaign that targets users when they add a product to their cart but do not finish transacting within 10 minutes.

### Deliver Action Based SMS

You can trigger an SMS based on an action. For example, you can send an SMS with a promo code for the next purchase can be sent to a set of customers who have just completed a purchase. This makes notifications more contextual and increases conversion.

### Deliver SMS based on Past Behavior (PBS)

You can also target users basis their past behavior. For example, you might want to target customers who have purchased a specific product in the past by sending them attractive discount vouchers or offers. 

### Filter by User Properties

Using the _With user properties_ filter in the _Who_ section, you can segment your campaign to only reach users who meet specific criteria. For example, you can send an SMS to all the customers from **Mumbai** who are currently subscribed to _Platinum_ membership. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d8f91b7-User_properties_whatsapp.png",
        "User properties whatsapp.png",
        2376
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



To know more about what segments can be used, see [Segments](doc:segments).

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information on control groups, see [Control Groups](doc:control-groups).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a739a68-campaign_control_group_targeting_cap.png",
        "campaign_control_group_targeting_cap.png",
        1107
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



### Targeting Cap

Sometimes, you want to send a message to only a subset of the qualifying audience (_Target Reach_) for a campaign or avoid sending it if the number of qualified users exceeds the specified number.

A relevant use case is a limited offer where you want to send a fixed number of coupon codes you want to distribute. If the total reach for your campaign exceeds the number of coupon codes you can distribute, you can limit the number of users who will receive the message to precisely the number of coupons that you want to distribute.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3aa9241-subset_image.png",
        "subset_image.png",
        406
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



## Define the SMS Content

Now, you can set up the _What_ section in the campaign content, with two different options:

- Single Message
- By User Property

Click _Go To Editor_ to create your message. 

## Message Editor

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a0060bb-SMS_What_User_Property.png",
        "SMS_What_User_Property.png",
        737
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



The _Create SMS Notification_ window displays. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/29c4894-SMS_Editor_What.png",
        "SMS_Editor_What.png",
        851
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



For users targeted in India, you might be required to set up template IDs. For more information, refer to [SMS Regulations ](https://docs.clevertap.com/docs/regulation-impact#future-campaigns).

> ❗️ Template IDs
> 
> A template ID is required for the SMS campaigns targeted to Indian mobile numbers and having MSG-91 as the service provider. A template ID may or may not be required for other service providers. We recommend checking with your service provider.

This section of the campaign creation flow depends on the SMS provider selected for the campaign.

### Out-of-the-box Providers

All SMS service providers are listed on the _Personalization Setup_ page (including Msg91, Nexmo, Twilio, Exotel, and Netcore). The connection with these providers is configured by default, and the mandatory input required for these providers is the message. This is only applicable for SMS campaigns in India for template id.

### Preview & Test

Once you are all done setting up the content of your campaign in _What_ section, you have the option to send a test SMS.

Click the **Preview & Test** button from the message editor to test a message.

## Message Types

You can create the following types of messages:

- Single Message
- By User Property

#### Single Message

We send the same message to all users who qualify as your target audience in this campaign. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between properties such as language, geography, or any other user properties.

### By User Property

Suppose you would like to send different message variants to your target audience based on the user properties. In that case, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fa28d4b-SMS_What_User_Property.png",
        "SMS_What_User_Property.png",
        737
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



You can use the + **+Variant** button to add multiple variants based on a user property value. In this example, we have used the _Customer Type_ user property so users with different customer type property values will receive corresponding copies of the campaign based on their different levels (Silver, Gold, or Platinum). 

![](https://files.readme.io/087cf49-SMS_What_User_Property_variant.png "SMS_What_User_Property_variant.png")

## Define the Campaign Schedule

You can schedule the campaign's start and end duration using the options below:

Past behavior campaigns can be scheduled to run:

- On a specific date and time.
- On multiple specified dates and times.
- Recurring at a periodicity you set.

Live campaigns can be set up for a specific event:

- In response to a user event.
- User event/inaction combination (e.g., abandoned cart scenario).
- Based on a date event property value of an event (for example,  a reminder for upcoming travel booking).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8ca1af6-Push_notification_editor_when.png",
        "Push_notification_editor_when.png",
        978
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



> 📘 Recurring Day
> 
> If you specify a recurring day for a campaign such as the 7th of each month, then the campaign will start for the specified day and ignore the creation date. This is a precaution to avoid sending a campaign unintentionally on a prior date.

### Delivery preferences

To cap the number of messages delivered every 5 minutes in a campaign, check the _Global throttle limits_ checkbox.

You can set the _Do Not Disturb_ (DND) hours during which SMS from this campaign are prevented from going out, either by discarding them or delaying delivery to after DND hours complete, such as 9 PM to 9 AM.

If you want your campaign to adapt delivery times according to the user’s timezone, check the _Timezone_ checkbox. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

Since past behavior campaigns can have scheduled times, you have the option to stop a campaign delivery after a certain cut-off time, or even deliver at the specified time in the user’s timezone. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/be4fee7-SMS_delivery_preferences.png",
        "SMS_delivery_preferences.png",
        838
      ],
      "align": "center",
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
        1193
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]