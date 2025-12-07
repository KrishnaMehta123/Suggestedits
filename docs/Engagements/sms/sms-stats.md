---
title: SMS Stats
excerpt: Measure the performance of your SMS campaign.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

Once the campaign has been published, you can view the detailed campaign stats under *All Campaigns* page. The *Stats* tab displays the overall conversion performance and errors.

# View Campaign Stats

To view the detailed campaign stats:

1. Click **Campaigns** from the dashboard. 
2. Select your campaign and open it.

The *Stats* tab displays the following campaign stats:

<Image alt="SMS Campaign Stats" align="center" border={true} src="https://files.readme.io/ef538b0-SMS_Campaign_Stats.png">
  SMS Campaign Stats
</Image>

* **Sent**: Represents the total number of messages sent from CleverTap.
* **Delivered**: Displays the total number of messages delivered to the end user. This count is available only if the [delivery callbacks](doc:generic-sms#configure-sms-callback) are set up so that CleverTap can track delivered SMS.
* **Clicked**: Displays the total number of clicks registered on the shortened link sent via CleverTap in an SMS.
* **CTR**: Represents the Click Through Rate of the SMS campaign. When the callbacks are configured, it is calculated as [(Clicked/Delivered) * 100]. When the callbacks are not configured, it is calculated as [(Clicked/Sent) * 100].
* **Converted users**: Represents the percentage of total users that performed the conversion event.

> 📘 Note
>
> When a recipient of the message forwards the message to someone else who then clicks on a shortened link, the click is attributed to the original recipient who received the message.

## Variant Comparison

Click **Variant Comparison** to view the *Sent*, *Delivered*, and *Clicked* for each variant. You can view these trends daily, weekly, or monthly. 

> 📘 Note
>
> This applicable to the following message types: A/B test, split delivery, and message on user property.

<Image alt="SMS Performance Trend" align="center" border={true} src="https://files.readme.io/411a9bc-image.png">
  SMS Performance Trend
</Image>

## Conversion Performance

Click **Conversion Performance** to view *Conversion performance*, *Revenue performance*, and users' *Influenced Conversion Funnel*.

<Image alt="SMS Conversion Performance" align="center" border={true} src="https://files.readme.io/90c14af-image.png">
  SMS Conversion Performance
</Image>

For A/B Test, Split Delivery, and Message on User Property campaigns, you can view stats for each variant under both the Direct and Influenced Conversion Funnel.

> 📘 Key Points to Remember
>
> The Conversion Performance number for *All Variants* may be equal to or less than the combined Conversion Performance number for each individual variant. For example, if the Conversion Performance number for All Variants is 10500, with Variant A at 5575 and Variant B at 5053, the total for Variants A and B combined is 10628, exceeding the total for *All Variants*.
>
> This scenario can occur due to the following reasons:
>
> * For Live campaigns, different variants are delivered to various devices, identified by different GUIDs for the same user. Consequently, the Conversion Performance number for All Variants might not match the sum of the Conversion Performance numbers for each variant. For instance, a user may receive Variant A before uninstalling the app and then receive Variant B after reinstalling it until their identity is established.
> * For Recurring campaigns (user property campaigns), the user can qualify more than once when and receive different message copy each time. For example, the user upgrades to a new plan. In this case, the message copy received by the user before and after upgrading the *Membership type* can be different.
>
> In both the cases, the same user is counted twice, once for Variant A and once for Variant B. However, when calculating the Conversion Performance number for *All Variants*, each user is counted only once.

## Split of Clicks

You can track the click distribution of each link in your SMS campaign. If you want to send an SMS promotion for an upcoming movie on your video streaming app with multiple links for *reviews*, *promotions*, *and movie merchandise*. We will record the clicks for each link in the SMS, and you can see them on the Campaign *Stats* page.

<Image alt="Split of Clicks" align="center" border={true} src="https://files.readme.io/ea32568-image.png">
  Split of Clicks
</Image>

## Errors

The **Errors** tab represents the errors that occurred while sending the SMS. his contains errors that occur while SMS is dispatched from CleverTap and delivery-related errors from the SMS provider's side. [Delivery-related errors](doc:generic-sms#error-codes) can be captured only if callbacks are set up.

<Image alt="Error Tab View" align="center" border={true} src="https://files.readme.io/2941095022108d0cda0c9ab036ba544d6576345a9689f7592dbf6036602e958b-SMS_-_Errors.png">
  Error Tab View
</Image>
