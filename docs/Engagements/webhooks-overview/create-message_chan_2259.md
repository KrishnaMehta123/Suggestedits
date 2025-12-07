---
title: Create Message_CHAN_2259
excerpt: Create a message for your webhook.
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

Create a campaign to deliver your Webhook. To create a new campaign

1. From the CleverTap dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **Webhooks**. 

<Image title="Webhook.png" alt={2826} align="center" border={true} src="https://files.readme.io/cac8ebf-Webhook.png">
  The campaign page displays.
</Image>

<Image title="Webhook campaign.png" alt={2760} align="center" className="border" border={true} src="https://files.readme.io/cfb9567-Webhook_campaign.png" />

Define all the sections to publish the campaign. 

## Start Campaign Setup

The *Start here* section displays the setup information. 

This section has the following parts:

* **Qualification criteria**: Deliver the notification based on Past Behavior/Custom List or Live Behavior. 
* **Webhook**: Select from the available Webhooks. Alternatively, you may create a new webhook.
* **Set a goal**: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve with the campaign. This selection is optional. Define the conversion period by selecting the *Conversion Time*. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, refer to [Events](https://docs.clevertap.com/docs/events). 

<Image title="Push_notification_set_goal_track_conversion.png" alt={919} align="center" className="border" border={true} src="https://files.readme.io/7d83483-Push_notification_set_goal_track_conversion.png" />

## Define the Audience

You need to indicate the target audience for your Webhook campaign. You can target your Webhook campaign to a new user segment by clicking on the **Target segment** section. Here, you can create a new ad-hoc segment or use a previously saved user segment from the *segment* list. 

<Image title="webhooks who.png" alt={2672} align="center" className="border" border={true} src="https://files.readme.io/7884aa0-webhooks_who.png" />

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

<Image title="Screenshot 2021-10-26 at 2.53.00 PM.png" alt={2202} align="center" className="border" border={true} src="https://files.readme.io/9289ee7-Screenshot_2021-10-26_at_2.53.00_PM.png" />

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information on control groups, see [Control Groups](doc:control-groups).

<Image title="Control_Group.png" alt={677} align="center" className="border" border={true} src="https://files.readme.io/5adb13c-Control_Group.png" />

### Targeting Cap

Sometimes, you want to send a message to only a subset of the qualifying audience (*Target Reach*) for a campaign or avoid sending it if the number of qualified users exceeds the specified number.

A relevant use case is a limited offer where you want to send a fixed number of coupon codes you want to distribute. If the total reach for your campaign exceeds the number of coupon codes you can distribute, you can limit the number of users who will receive the message to exactly the number of coupons you want to distribute.

> 📘 Note
>
> The maximum reach for the target segment may be less than the limit specified in Targeting Cap.

<Image title="subset_image.png" alt={406} align="center" className="border" border={true} src="https://files.readme.io/3aa9241-subset_image.png" />

## Define the Webhook Content

Now, you can set up the *What* which is the Webhook campaign content. Click *Go To Editor* to create your message. 

<Image title="Webhook_what_without_options.png" alt={1048} align="center" className="border" border={true} src="https://files.readme.io/6dfb26c-Webhook_what_without_options.png" />

### Sample Payload

Following is a sample webhook payload containing all possible fields for profile variables. The `targetId` corresponds to the webhook campaign ID for which you receive the payload.

```json
{
  "targetId": 1659684581,
  "key_values": {
    "SomeKey1": "SomeValue1"
  },
  "profiles": [
    {
      "key_values": {
        "SomeKey1": "SomeValue1"
      },
      "email": "webhook227@gmail.com",
      "identity": "webhook227@gmail.com",
      "all_identities": [
        "webhook227@gmail.com"
      ],
      "objectId": "__Webhook227",
      "phone": "+917872483227",
      "systemProfileData": {
        "webPushSubscription": "Unsubscribed",
        "mobilePushSubscription": "Unsubscribed",
        "emailSubscription": "Subscribed",
        "smsSubscription": "Subscribed",
        "whatsappSubscription": "Subscribed",
        "timezone": "Eastern Standard Time",
        "country": "Unknown",
        "region": "Unknown",
        "city": "Unknown",
        "latitude": 19.16670036315918,
        "longitude": 72.84851837158203,
        "age": "2 years 1 months"
      },
      "profileData": {
        "customer type": "gold",
        "customer id": 11384938,
        "language": “english”,
        "last score": 308,
        "high score": 308,
        "replayed": true,
                "multi": [
          "foo",
          "bar"
        ],
        "ts": 1586937505801
      },
      "name": "Nick",
      "event_properties": {
        "zip-code": "0500",
        "Product Id": 1,
        "test prop 2": 100,
        "prop1": 19.16670036315918,
        "prop2": 72.84851837158203,
        "Make": "random make",
        "Model": "s",
        "SDK Version": 30200,
        "OS Version": "9.1.11111",
        "Version": 6.55,
        "date": "$D_1664890781",
        "ct_sdk_version": 30700,
        "ct_latitude": 19.16670036315918,
        "ct_longitude": 72.84851837158203,
        "ct_os_version": "9.1.11111",
        "ct_app_version": 6.55,
        "CT Source": "Mobile"
      },
      "session_props": {}
    }
  ]
}
```

## Webhook Editor

From the Webhook Editor:

1. Add query parameters in the URL key-value pairs section. 
2. Select the content type (JSON or plain text).
3. Add the webhook content to send or receive the data.

<Image title="Webhook Editor What.png" alt={1425} align="center" className="border" border={true} src="https://files.readme.io/a1faeb5-Webhook_Editor_What.png" />

You can either use *Profile Variables & custom key value pairs* or *Custom Body*. You have the option to send/receive an email, identity, objectId (CleverTap ID), profileData (custom profile variables), event properties (applicable only for Live behavior), and push\_token for each user.  

<Image title="Create Webhook Content.png" alt={839} align="center" className="border" border={true} src="https://files.readme.io/5589ea5-Create_Webhook_Content.png" />

You can also choose a custom payload. 

<Image title="webhooks custom json.png" alt={1672} align="center" className="border" border={true} src="https://files.readme.io/dead0f2-webhooks_custom_json.png" />

The preview for your payload is displayed on the right side of the pane.

<Image title="webhooks preview.png" alt={2832} align="center" className="border" border={true} src="https://files.readme.io/ae38cd3-webhooks_preview.png" />

## Define the Campaign Schedule

Each webhook campaign needs to be scheduled for a specific timeline. To define the schedule for your webhook campaign, you need to specify the *Start date and time* and *End date and time*. You also have the option to start a campaign immediately by selecting *Now*.  

Besides, you can also define a delay (by seconds, minutes, hours, or days) once a user qualifies for the target segment. Once you define the schedule and click *Done*; the campaign will be triggered and terminated as per the defined timings.

<Image title="webhook when.png" alt={1886} align="center" className="border" border={true} src="https://files.readme.io/b635c3a-webhook_when.png" />

### Delivery preferences

Global frequency caps operate on a per-channel basis and let you specify the message cadence, dwell time between messages, and throttle limits (delivery rates). To control the maximum number of messages users receive for a given channel of communication, select *Global campaign limits*. And, to control the delivery rates for your campaigns, select *Global throttle limits*. For more information about *Global campaign limits* and *Global throttle limits*, refer to [Messaging Frequency Caps](doc:messaging-frequency-caps).

You can also define the cut-off time for your campaign by selecting *Cut-off*.

<Image align="center" className="border" border={true} src="https://files.readme.io/56b834b-image.png" />

## Publish Campaign

After previewing the appearance of your overall campaign, finalize your campaign by clicking **Publish Campaign.**

<Image title="campaign_Publish.png" alt={1193} align="center" className="border" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png" />
