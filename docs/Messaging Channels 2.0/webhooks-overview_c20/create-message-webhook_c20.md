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
## Create a New Campaign

Create a campaign to deliver your Webhook. To create a new campaign

1. From the CleverTap dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **Webhooks**. 

<Image title="Webhook.png" alt={2826} border={true} src="https://files.readme.io/cac8ebf-Webhook.png">
  The campaign page displays.
</Image>

<Image title="Webhook campaign.png" alt={2760} className="border" border={true} src="https://files.readme.io/cfb9567-Webhook_campaign.png" />

Define all the sections to publish the campaign. 

## Start Campaign Setup

The *Start here* section displays the setup information. 

This section has the following parts:

* **Qualification criteria**: Deliver the notification based on Past Behavior/Custom List or Live Behavior. 
* **Webhook**: Select from the available Webhooks. Alternatively, you may create a new webhook.
* **Set a goal**: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve with the campaign. This selection is optional. Define the conversion period by selecting the *Conversion Time*. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, refer to [Events](https://docs.clevertap.com/docs/events). 

<Image title="Push_notification_set_goal_track_conversion.png" alt={919} className="border" border={true} src="https://files.readme.io/7d83483-Push_notification_set_goal_track_conversion.png" />

## Define the Audience

You need to indicate the target audience for your Webhook campaign. You can target your Webhook campaign to a new user segment by clicking on the **Target segment** section. Here, you can create a new ad-hoc segment or use a previously saved user segment from the *segment* list. 

<Image title="webhooks who.png" alt={2672} className="border" border={true} src="https://files.readme.io/7884aa0-webhooks_who.png" />

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

<Image title="Screenshot 2021-10-26 at 2.53.00 PM.png" alt={2202} className="border" border={true} src="https://files.readme.io/9289ee7-Screenshot_2021-10-26_at_2.53.00_PM.png" />

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information on control groups, see [Control Groups](doc:control-groups).

<Image title="campaign_control_group_targeting_cap.png" alt={1107} className="border" border={true} src="https://files.readme.io/a739a68-campaign_control_group_targeting_cap.png" />

### Targeting Cap

Sometimes, you want to send a message to only a subset of the qualifying audience (*Target Reach*) for a campaign or avoid sending it if the number of qualified users exceeds the specified number.

A relevant use case is a limited offer where you want to send a fixed number of coupon codes you want to distribute. If the total reach for your campaign exceeds the number of coupon codes you can distribute, you can limit the number of users who will receive the message to exactly the number of coupons you want to distribute.

<Image title="subset_image.png" alt={406} className="border" border={true} src="https://files.readme.io/3aa9241-subset_image.png" />

## Define the Webhook Content

Now, you can set up the *What* which is the Webhook campaign content. Click *Go To Editor* to create your message. 

<Image title="Webhook_what_without_options.png" alt={1048} className="border" border={true} src="https://files.readme.io/6dfb26c-Webhook_what_without_options.png" />

### Sample Payload

Following is a sample webhook payload containing all possible fields for profile variables. The targetId corresponds to the webhook campaign ID for which you are receiving the payload. 

```json
{
    "targetId": 1472124953,
    "key_values": {
        "PromoCode": "MT50",
        "PowerUser": "true"
    },
    "profiles": [
        {
            "Email": "jack@gmail.com",
            "Identity": "foo",
            "ObjectId": "-g55b74fb1030740e4a4931910a8abb862",
            "ProfileData": {
                "Last Score": 308,
                "High Score": 308,
                "Replayed": true
            },
            "Event_properties": {
                "Score": 1200,
                "Game Mode": "Practice",
                "Rating": 1
            },
            "Push_token": "19403aa5d3bb376769a8101c9cbf22159cb1836117659cc684a71243589982ea"
        },
        {
            "Email": "jill@gmail.com",
            "Identity": "bar",
            "ObjectId": "__g09c9bf3b0d374a259c86f5b855ec9b19",
            "ProfileData": {
                "Last Score": 309,
                "High Score": 309,
                "Replayed": true
            },
            "Event_properties": {
                "Score": 500,
                "Game Mode": "Tournament",
                "Rating": 2
            },
            "Push_token": "fiCjRO_opjw:APA91bH0yzS_eBj1Xx8TcakMzz4yTc3id29A79GOjnaaMtIQLrjztNfzzRz7slqWmNzndECx_hHh7qiL0LZJOkGwzr9Zp_g1mC9B6BVuEbsjrMFoxXX830zMRuvxtU_AhFTC0JPHejZh"
        }
    ]
}
```

## Webhook Editor

From the Webhook Editor:

1. Add query parameters in the URL key-value pairs section. 
2. Select the content type (JSON or plain text).
3. Add the webhook content to send or receive the data. 

<Image title="Webhook_editor_what.png" alt={1152} className="border" border={true} src="https://files.readme.io/6a7e4ff-Webhook_editor_what.png" />

You can either use *Profile Variables & custom key value pairs* or *Custom Body*. You have the option to send/receive an email, identity, objectId (CleverTap ID), profileData (custom profile variables), event properties (applicable only for Live behavior), and push\_token for each user.  

<Image title="Webhookf1.png" alt={1650} className="border" border={true} src="https://files.readme.io/f64e3dc-Webhookf1.png" />

You can also choose a custom payload. 

<Image title="webhooks custom json.png" alt={1672} className="border" border={true} src="https://files.readme.io/dead0f2-webhooks_custom_json.png" />

The preview for your payload is displayed on the right side of the pane.

<Image title="webhooks preview.png" alt={2832} className="border" border={true} src="https://files.readme.io/ae38cd3-webhooks_preview.png" />

## Define the Campaign Schedule

Each webhook campaign needs to be scheduled for a specific timeline. To define the schedule for your webhook campaign, you need to specify the *Start date and time* and *End date and time*. You also have the option to start a campaign immediately by selecting *Now*.  

Besides, you can also define a delay (by seconds, minutes, hours, or days) once a user qualifies for the target segment. Once you define the schedule and click *Done*; the campaign will be triggered and terminated as per the defined timings.

<Image title="webhook when.png" alt={1886} className="border" border={true} src="https://files.readme.io/b635c3a-webhook_when.png" />

### Delivery preferences

Checkmark the *Do Not Disturb* (DND) checkbox to delay or avoid sending messages to users for a specified period of time. 

For fine-tuning the campaign, you can also choose to deliver the campaign to users each time they qualify or choose to deliver multiple campaigns at specified intervals (in minutes, hours, or days).

To control the maximum number of messages users receive for a given channel of communication, tick mark the *Global campaign limits* checkbox

<Image title="Webhooks DP.png" alt={1696} className="border" border={true} src="https://files.readme.io/40c126c-Webhooks_DP.png" />

## Publish Campaign

After previewing the appearance of your overall campaign, finalize your campaign by clicking **Publish Campaign.**

<Image title="campaign_Publish.png" alt={1193} className="border" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png" />
