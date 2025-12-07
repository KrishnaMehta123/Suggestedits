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

Once the campaign has been published, you can view the detailed campaign stats under *All Campaigns* page.

# View Campaign Stats

To view the detailed campaign stats:

1. Click **Campaigns** from the dashboard. 
2. Select your campaign and open it.

The *Stats* tab displays the following campaign stats:

<Image alt="SMS Campaign Stats" align="center" border={true} src="https://files.readme.io/ef538b0-SMS_Campaign_Stats.png">
  SMS Campaign Stats
</Image>

* **Sent**: Represents the total number of messages sent from CleverTap.
* **Delivered**: Displays the total number of messages delivered to the end user. This count is available only if the [delivery callbacks](doc:generic-sms_em-1033-structure#configure-sms-callback) are set up so that CleverTap can track delivered SMS.
* **Clicked**: Represents the count of clicks by the users.
* **CTR**: Represents the Click Through Rate of the SMS campaign. When the callbacks are configured, it is calculated as [(Clicked/Delivered) * 100]. When the callbacks are not configured, it is calculated as [(Clicked/Sent) * 100].
* **Converted users**: Represents the percentage of total users that performed the conversion event.

## Message Trend

Click **Message Trend** to view the *Performance Trend* by *Sent*, *Delivered*, and *Clicked*. You can view these trends on a daily, weekly, or monthly basis.

<Image alt="SMS Performance Trend" align="center" border={true} src="https://files.readme.io/9f0fc27-SMS_Performance_Trend.png">
  SMS Performance Trend
</Image>

## Conversion performance

Click **Conversion Performance** to view *Conversion performance*, *Revenue performance*, and users' *Influenced Conversion Funnel*.

<Image alt="SMS Conversion Performace" align="center" width="60% " border={true} src="https://files.readme.io/535dc12-Conversion_Performance_Stats.png">
  SMS Conversion Performace
</Image>

## Split of Clicks

You can track the click distribution of each link in your SMS campaign. If you want to send an SMS promotion for an upcoming movie on your video streaming app with multiple links for *reviews*, *promotions*, *and movie merchandise*. We will record the clicks for each link in the SMS, and you can see them on the Campaign *Stats* page.

<Image alt="Split of Clicks" align="center" width="75% " border={true} src="https://files.readme.io/d3d819b-Split_of_Clicks.png">
  Split of Clicks
</Image>

## Errors

The **Errors** tab represents the errors that occurred while sending the SMS. his contains errors that occur while SMS is dispatched from CleverTap as well as delivery-related errors from the SMS provider's side. [Delivery-related errors](doc:generic-sms_em-1033-structure#error-codes) can be captured only if callbacks are set up.

<Image align="center" className="border" border={true} src="https://files.readme.io/a05466b-SMS_Campaign_Error_Stats.png" />
