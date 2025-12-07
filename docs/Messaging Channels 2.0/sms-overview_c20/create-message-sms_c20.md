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
    Refer to the pages listed below to learn more about the following SMS
    sections:
  pages:
    - type: link
      title: Personalize Message
      url: https://docs.clevertap.com/docs/personalize-message-sms_c20
    - type: link
      title: SMS Regulations
      url: https://docs.clevertap.com/docs/sms-regulations_c20
    - type: link
      title: Regulation Impact
      url: https://docs.clevertap.com/docs/regulation-impact_c20
    - type: link
      title: FAQs
      url: https://docs.clevertap.com/docs/sms-faqs_c20
---
[block:api-header]
{
  "title": "Create a New Campaign"
}
[/block]
Follow the steps below to create a new SMS campaign:

1. From the CleverTap dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **SMS**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d0a3e77-SMS_Create.png",
        "SMS Create.png",
        2796,
        1106,
        "#f8f8f9"
      ],
      "border": true,
      "caption": ""
    }
  ]
}
[/block]
The *Campaign* page displays.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3afb28a-SMS_Editor_main.png",
        "SMS_Editor_main.png",
        1107,
        1248,
        "#fbfafb"
      ],
      "border": true,
      "sizing": "80"
    }
  ]
}
[/block]
Define all the sections and publish the campaign. 

## Start Campaign Setup

The *Start here* section displays the setup information. 
This section has the following parts:

* **Qualification criteria**: Here, you need to define the criteria for your target audience. You can deliver the SMS based on *Past behavior/Custom list* or *Live behavior*.
* **SMS Service Provider**:  Here, you need to select your SMS service provider or a provider group.
* **Goal**: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign performance. This selection is optional. Define the conversion period by selecting the *Conversion Time*. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, see [Events](doc:events).
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6001c3f-Push_notification_set_goal_track_conversion.png",
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

You must indicate the target audience for your push campaign. You can target your SMS campaign to a new user segment by clicking on the **Target segment** section. Here, you can create a new ad-hoc segment or use a previously saved user segment from the *segment* list. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/074ff4c-SMS_Who.png",
        "SMS_Who.png",
        961,
        766,
        "#f8f8fc"
      ],
      "border": true
    }
  ]
}
[/block]
You can also create the target on the basis of past user behavior and user properties or live (ongoing) user behavior. the latter is useful to send out real-time, triggered SMS campaigns.

For instance, you can create a live *Inaction within time* campaign that targets users as soon as they add a product to their cart but do not finish transacting within 10 minutes.

### Deliver Action Based SMS

You can trigger an SMS based on an action. For example, an SMS with a promo code for the next purchase can be sent to a set of customers who have just completed a purchase. This makes notifications more contextual and increases conversion.

### Deliver SMS based on Past Behavior (PBS)

You can also target users basis their past behavior. For example, you might want to target customers who have purchased a specific product in the past by sending them attractive discount vouchers or offers. 

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to only reach users who meet specific criteria. For example, you can send an SMS to all the customers from **Mumbai** who are currently subscribed to *Platinum* membership. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d8f91b7-User_properties_whatsapp.png",
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
        1107,
        555,
        "#fbfbfd"
      ],
      "border": true
    }
  ]
}
[/block]
### Targeting Cap

Sometimes, you want to send a message to only a subset of the qualifying audience (*Target Reach*) for a campaign or avoid sending it if the number of qualified users exceeds the specified number.

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
## Define the SMS Content

Now, you can set up the *What* which is the SMS campaign content.

Click *Go To Editor* to create your message. 

##Message Editor
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e241760-Webhook_what_without_options.png",
        "Webhook_what_without_options.png",
        1048,
        188,
        "#f8f3f5"
      ],
      "border": true
    }
  ]
}
[/block]
The Create SMS Notification window displays. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/29c4894-SMS_Editor_What.png",
        "SMS_Editor_What.png",
        851,
        645,
        "#eee9f5"
      ],
      "border": true
    }
  ]
}
[/block]
For users targeted in India, you might be required to set up template IDs. Learn more about it [here](https://docs.clevertap.com/docs/regulation-impact_c20#future-campaigns).

This section of the campaign creation flow will be dependent upon the SMS provider selected for the campaign.

### Out-of-the-box Providers
All SMS service providers are listed on the **Personalization Setup** page (including Msg91, Nexmo, Twilio, Exotel, and Netcore). The connection with these providers is configured by default and the mandatory input required for these providers is the message. This is only applicable for SMS campaigns in India with respect to template id.

### Preview & Test

Once you are all done setting up the content of your campaign in *What* section, you have the option to send a test SMS.

Click the **Preview & Test** button from the message editor to test a message.

## Define the Campaign Schedule

You can schedule the campaign's start and end duration using the options below:

Past behavior campaigns can be scheduled to run:

  * On a specific date and time.
  * On multiple specified dates and times.
  * Recurring at a periodicity you set.

Live campaigns can be set up on a specific event:
  * In response to a user event.
  * User event/inaction combination (e.g., abandoned cart scenario).
  * Based on a date event property value of an event (for example,  a reminder for upcoming travel booking).
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8ca1af6-Push_notification_editor_when.png",
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
###Delivery preferences
 
To cap the number of messages delivered every 5 minutes in a campaign, check the *Global throttle limits* checkbox.

You can set the *Do Not Disturb* (DND) hours during which SMS from this campaign are prevented from going out, either by discarding them or delaying delivery to after DND hours complete, such as 9 PM to 9 AM.

If you want your campaign to adapt delivery times according to the user’s timezone, check the *Timezone* checkbox. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

Since past behavior campaigns can have scheduled times, you have the option to stop a campaign delivery after a certain cut-off time, or even deliver at the specified time in the user’s timezone. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/be4fee7-SMS_delivery_preferences.png",
        "SMS_delivery_preferences.png",
        838,
        626,
        "#fbfbfc"
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