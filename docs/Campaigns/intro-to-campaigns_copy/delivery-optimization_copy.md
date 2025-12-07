---
title: Delivery Optimization
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Overview

You can optimize push delivery with push implication and sending to app inbox. 

## Optimize with Push Amplification

Push notifications are a great way to engage customers despite the issue of low deliverability on certain device manufacturers. In addition, more and more users choose to opt out of push notifications.

With push amplification, you can counter this challenge by enhancing the delivery of push notifications to devices that missed receiving them. This feature is supported for Android and Flutter apps.

### Enable Push Amplification

To enable this feature:

1. Integrate code for custom push amplification handling into your Android app code. For detailed steps, refer to [Custom Push Amplification Handling](https://developer.clevertap.com/docs/custom-handling-push-amplification).
2. Navigate to *Settings* > *Engage* > *Setup* > *Push Amplification* in the CleverTap dashboard. 
3. Turn on the push amplification toggle. 

<Image title="Enable Push Amp.png" alt={2052} className="border" border={true} src="https://files.readme.io/228b60a-Enable_Push_Amp.png" />

The **Enable Push Amplification** popup opens. 

<Image title="save as popup.png" alt={456} className="border" width="smart" border={true} src="https://files.readme.io/2bc2954-save_as_popup.png" />

4. Click **Enable**. After enabling the Push Notification Amplification successfully, the message *Push Amplification is enabled* is displayed:

<Image title="Push Amp enabled.png" alt={1580} className="border" border={true} src="https://files.readme.io/5571e8f-Push_Amp_enabled.png" />

> 🚧 Turn On/Off Push Notification Amplification
>
> After you turn on push amplification, all the push campaigns created are amplified from that moment onward. This applies the same way when you turn it off.

After push amplification is turned on, the push notification campaigns reach more users. You can check the uplift on the push campaign stats page.

<Image title="Push amplification stats.png" alt={2678} className="border" border={true} src="https://files.readme.io/64a0eb1-Push_amplification_stats.png" />

> 📘 Support for Push Amplification via Inbox
>
> * We support *Push Amplification via Inbox* and retrying push notifications due to delivery issues with certain OEMs. 
>
> * If the app is online when *Push* is delivered, the inbox delivery is done on the next *App Launch* and not immediately after the *Push* is delivered.

## Optimize with App Inbox

Apart from push amplification, you can further increase delivery of push notification by sending a copy of the same message to *App Inbox*. 

To send a copy of the push message to **App Inbox**, click the checkbox that appears at the bottom of the message builder of push notification in the *What* section.

![1318](https://files.readme.io/777a4b6-New_1.png "New 1.png")

> 📘 App Inbox as its Own Channel
>
> *App Inbox* also exists as a stand-alone channel. For more information, refer to [App Inbox](https://docs.clevertap.com/docs/app-inbox).

  From this screen, you can do the following:

* You can customize the same push message for *App Inbox*. 
  * You can change the title color, message color, background color, and also add filter tags that classify your message into tabs. For more information, refer to [Message Tags](https://docs.clevertap.com/docs/app-inbox#section-message-tags). 
  * You can set a time to live (TTL) for *App Inbox* message in the setup section. For more information on setting up TTL, refer to [Time to Live](https://docs.clevertap.com/docs/app-inbox#section-time-to-live).

## Push Amplification and App Inbox Stats

You can view the stats for push messages copied to *App Inbox* on the *Push stats* page. The percentage boost represents the percentage of messages boosted by *App Inbox* as compared to the total of messages sent via *App Inbox* and *Push Amplification*.

To view the stats for the copied messages, you can use the tab *App Inbox stats*.

<Image title="Push amplification report for App Inbox.png" alt={1580} className="border" border={true} src="https://files.readme.io/1401bf8-Push_amplification_report_for_App_Inbox.png" />
