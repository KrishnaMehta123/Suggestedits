---
title: Create Message
excerpt: Create a message for your webhook.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
  pages:
    - type: link
      title: Personalize Webhooks
      url: https://docs.clevertap.com/docs/personalize-message-webhooks_c20
    - type: link
      title: Webhook Stats
      url: https://docs.clevertap.com/docs/webhooks-stats_c20
---
[block:api-header]
{
  "title": "Create a New Campaign"
}
[/block]
Create a campaign to deliver your Webhook. To create a new campaign

1. From the CleverTap dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **Webhooks**. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cac8ebf-Webhook.png",
        "Webhook.png",
        2826,
        1426,
        "#ecedf2"
      ],
      "border": true,
      "caption": "The campaign page displays."
    }
  ]
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cfb9567-Webhook_campaign.png",
        "Webhook campaign.png",
        2760,
        2010,
        "#fbfafa"
      ],
      "border": true
    }
  ]
}
[/block]
Define all the sections to publish the campaign. 


## Start Campaign Setup

The *Start here* section displays the setup information. 

This section has the following parts:

* **Qualification criteria**: Deliver the notification based on Past Behavior/Custom List or Live Behavior. 
* **Webhook**: Select from the available Webhooks. Alternatively, you may create a new webhook.
* **Set a goal**: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve with the campaign. This selection is optional. Define the conversion period by selecting the *Conversion Time*. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, refer to [Events](https://docs.clevertap.com/docs/events). 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7d83483-Push_notification_set_goal_track_conversion.png",
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

You need to indicate the target audience for your Webhook campaign. You can target your Webhook campaign to a new user segment by clicking on the **Target segment** section. Here, you can create a new ad-hoc segment or use a previously saved user segment from the *segment* list. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7884aa0-webhooks_who.png",
        "webhooks who.png",
        2672,
        1312,
        "#f9f9fd"
      ],
      "border": true
    }
  ]
}
[/block]
You can create the target on the basis of past user behavior and/or user properties, or live (ongoing) user behavior (the latter is useful to send out real-time, triggered Webhook campaigns).

For instance, you can create a live *Inaction within time* campaign that targets users as soon as they add a product to their cart but do not finish transacting within 10 minutes, the golden window within which most users transact on online platforms

### Deliver Action Based Webhook Notifications
You can trigger a Webhook notification based on an action. Users receive Webhook notifications when they perform an action in the app instead of waiting for the next app launch. This makes notifications more contextual and increases conversion. The instant Webhook message is not triggered for campaigns with delays or when the app inbox is coupled with a Webhook message.


### Filter Webhook Notifications based on Past Behavior

You can also target users basis their past behavior. For past behavior campaigns, you also have an option to calculate estimated reach to view:

* Number of users that qualify for the campaign criteria.
* Number of users that are reachable via Webhook.


### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can send webhook notifications only for female users who live in the United States. The image below represents a sample target segment that is filtered using specific user properties to target the required audience.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9289ee7-Screenshot_2021-10-26_at_2.53.00_PM.png",
        "Screenshot 2021-10-26 at 2.53.00 PM.png",
        2202,
        822,
        "#decfad"
      ],
      "border": true
    }
  ]
}
[/block]
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
## Define the Webhook Content

Now, you can set up the *What* which is the Webhook campaign content. Click *Go To Editor* to create your message. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6dfb26c-Webhook_what_without_options.png",
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
### Sample Payload
Following is a sample webhook payload containing all possible fields for profile variables. The targetId corresponds to the webhook campaign ID for which you are receiving the payload. 

[block:code]
{
  "codes": [
    {
      "code": "{\n    \"targetId\": 1472124953,\n    \"key_values\": {\n        \"PromoCode\": \"MT50\",\n        \"PowerUser\": \"true\"\n    },\n    \"profiles\": [\n        {\n            \"Email\": \"jack@gmail.com\",\n            \"Identity\": \"foo\",\n            \"ObjectId\": \"-g55b74fb1030740e4a4931910a8abb862\",\n            \"ProfileData\": {\n                \"Last Score\": 308,\n                \"High Score\": 308,\n                \"Replayed\": true\n            },\n            \"Event_properties\": {\n                \"Score\": 1200,\n                \"Game Mode\": \"Practice\",\n                \"Rating\": 1\n            },\n            \"Push_token\": \"19403aa5d3bb376769a8101c9cbf22159cb1836117659cc684a71243589982ea\"\n        },\n        {\n            \"Email\": \"jill@gmail.com\",\n            \"Identity\": \"bar\",\n            \"ObjectId\": \"__g09c9bf3b0d374a259c86f5b855ec9b19\",\n            \"ProfileData\": {\n                \"Last Score\": 309,\n                \"High Score\": 309,\n                \"Replayed\": true\n            },\n            \"Event_properties\": {\n                \"Score\": 500,\n                \"Game Mode\": \"Tournament\",\n                \"Rating\": 2\n            },\n            \"Push_token\": \"fiCjRO_opjw:APA91bH0yzS_eBj1Xx8TcakMzz4yTc3id29A79GOjnaaMtIQLrjztNfzzRz7slqWmNzndECx_hHh7qiL0LZJOkGwzr9Zp_g1mC9B6BVuEbsjrMFoxXX830zMRuvxtU_AhFTC0JPHejZh\"\n        }\n    ]\n}",
      "language": "json"
    }
  ]
}
[/block]
## Webhook Editor 

From the Webhook Editor:

1. Add query parameters in the URL key-value pairs section. 
2. Select the content type (JSON or plain text).
3. Add the webhook content to send or receive the data. 


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6a7e4ff-Webhook_editor_what.png",
        "Webhook_editor_what.png",
        1152,
        941,
        "#dcd9e2"
      ],
      "border": true
    }
  ]
}
[/block]
You can either use *Profile Variables & custom key value pairs* or *Custom Body*. You have the option to send/receive an email, identity, objectId (CleverTap ID), profileData (custom profile variables), event properties (applicable only for Live behavior), and push_token for each user.  


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f64e3dc-Webhookf1.png",
        "Webhookf1.png",
        1650,
        1524,
        "#f6f4fa"
      ],
      "border": true
    }
  ]
}
[/block]
You can also choose a custom payload. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dead0f2-webhooks_custom_json.png",
        "webhooks custom json.png",
        1672,
        1508,
        "#f4f3f9"
      ],
      "border": true
    }
  ]
}
[/block]
The preview for your payload is displayed on the right side of the pane.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ae38cd3-webhooks_preview.png",
        "webhooks preview.png",
        2832,
        1330,
        "#dbd7e2"
      ],
      "border": true
    }
  ]
}
[/block]
## Define the Campaign Schedule

Each webhook campaign needs to be scheduled for a specific timeline. To define the schedule for your webhook campaign, you need to specify the *Start date and time* and *End date and time*. You also have the option to start a campaign immediately by selecting *Now*.  

Besides, you can also define a delay (by seconds, minutes, hours, or days) once a user qualifies for the target segment. Once you define the schedule and click *Done*; the campaign will be triggered and terminated as per the defined timings.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b635c3a-webhook_when.png",
        "webhook when.png",
        1886,
        864,
        "#fbfaf9"
      ],
      "border": true
    }
  ]
}
[/block]
###Delivery preferences
 
Checkmark the *Do Not Disturb* (DND) checkbox to delay or avoid sending messages to users for a specified period of time. 

For fine-tuning the campaign, you can also choose to deliver the campaign to users each time they qualify or choose to deliver multiple campaigns at specified intervals (in minutes, hours, or days).

To control the maximum number of messages users receive for a given channel of communication, tick mark the *Global campaign limits* checkbox
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/40c126c-Webhooks_DP.png",
        "Webhooks DP.png",
        1696,
        798,
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