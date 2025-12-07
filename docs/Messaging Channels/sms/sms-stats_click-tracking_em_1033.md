---
title: SMS Stats_Generic Callbacks_EM-1033
excerpt: Measure the performance of your SMS campaign.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

Once the campaign has been published, you can view the detailed campaign stats under _All Campaigns_ page.

# View Campaign Stats

To view the detailed campaign stats:

1. Click **Campaigns** from the dashboard. 
2. Select your campaign and open it.

The _Stats_ tab displays the following campaign stats:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ef538b0-SMS_Campaign_Stats.png",
        null,
        "SMS Campaign Stats"
      ],
      "align": "center",
      "border": true,
      "caption": "SMS Campaign Stats"
    }
  ]
}
[/block]

- **Sent**: Represents the total number of messages sent from CleverTap.
- **Delivered**: Displays the total number of messages delivered to the end user. This count is available only if the [delivery callbacks](doc:generic-sms_em-1033-structure#configure-sms-callback) are set up so that CleverTap can track delivered SMS.
- **Clicked**: Represents the count of clicks by the users.
- **CTR**: Represents the Click Through Rate of the SMS campaign. When the callbacks are configured, it is calculated as [(Clicked/Delivered) * 100]. When the callbacks are not configured, it is calculated as [(Clicked/Sent) * 100].
- **Converted users**: Represents the percentage of total users that performed the conversion event.

## Message Trend

Click **Message Trend** to view the _Performance Trend_ by _Sent_, _Delivered_, and _Clicked_. You can view these trends on a daily, weekly, or monthly basis.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9f0fc27-SMS_Performance_Trend.png",
        null,
        "SMS Performance Trend"
      ],
      "align": "center",
      "border": true,
      "caption": "SMS Performance Trend"
    }
  ]
}
[/block]

## Conversion performance

Click **Conversion Performance** to view _Conversion performance_, _Revenue performance_, and users' _Influenced Conversion Funnel_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/535dc12-Conversion_Performance_Stats.png",
        null,
        "SMS Conversion Performace"
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "SMS Conversion Performace"
    }
  ]
}
[/block]

## Split of Clicks

You can track the click distribution of each link in your SMS campaign. If you want to send an SMS promotion for an upcoming movie on your video streaming app with multiple links for _reviews_, _promotions_, _and movie merchandise_. We will record the clicks for each link in the SMS, and you can see them on the Campaign _Stats_ page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d3d819b-Split_of_Clicks.png",
        null,
        "Split of Clicks"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Split of Clicks"
    }
  ]
}
[/block]

## Errors

The **Errors** tab represents the errors that occurred while sending the SMS. his contains errors that occur while SMS is dispatched from CleverTap as well as delivery-related errors from the SMS provider's side. [Delivery-related errors](doc:generic-sms_em-1033-structure#error-codes) can be captured only if callbacks are set up.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a05466b-SMS_Campaign_Error_Stats.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]