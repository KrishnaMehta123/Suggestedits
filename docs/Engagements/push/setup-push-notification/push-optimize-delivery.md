---
title: Optimize Delivery
excerpt: >-
  Understand how to optimize push messages with Pull Notifications and App
  Inbox.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Overview

You can optimize push delivery using the following two features: 

* Pull Notification 
* Sending the push message to App Inbox 

You can optimize the delivery rate by retrying the *Push* message as is (where messages are suppressed by the device) or by sending it to *App Inbox* when the user enables DND for push messages.

## Optimize Delivery via Pull Notification

Push notifications are a great way to engage customers despite the issue of low deliverability on certain device manufacturers. 

With Pull Notification at your disposal, you can counter this challenge by optimizing the delivery of push notifications to devices that missed receiving them.

To enable this feature, navigate to *Settings* > *Engage* > *Setup* > *Pull Notification*. Toggle ON the Pull Notification as shown in the following figure:

<Image title="Increase Deliverability of Push Notifications" alt={2514} align="center" border={true} src="https://files.readme.io/ba8fa22-pull_notification.png">
  Toggle Pull Notification
</Image>

> 🚧 Toggle Pull Notification
>
> All the push campaigns that are created *after* turning on the Pull Notification toggle are enhanced. Similarly, no new campaigns are enhanced after the Pull Notification toggle is turned off.

After Pull Notification is turned ON, your campaigns reach more users through your notifications. You can check these boost numbers on your campaign *Stats* page.

<Image title="Push Uplift" alt={2672} align="center" border={true} src="https://files.readme.io/2e7757d-enhanced_push_deliver.png">
  Enhanced Delivery Stats
</Image>

> 📘 Support for Optimize Delivery via Inbox
>
> We support *Optimize Delivery via Inbox* and retry notifications due to delivery issues with certain OEMs. 
>
> If the app is online when *Push* is delivered, the Inbox delivery is done on the next *App Launch* and not immediately after the *Push* is delivered.

## Optimize Delivery via App Inbox

You can further increase the delivery of push notifications by sending a copy of the same message to *App Inbox*. 

To send a copy of the push message to **App Inbox**, select *Send a copy of this message to the App Inbox* that appears at the bottom of the message builder of push notification in the *What* section.

<Image title="Copy of Push Message in App Inbox" alt={746} align="center" src="https://files.readme.io/d3fa57a-campaign_push_app_inbox.png">
  Delivery via App Inbox
</Image>

> 📘 App Inbox as its Own Channel
>
> *App Inbox* also exists as a stand-alone channel. For more information, refer to [App Inbox](doc:app-inbox-overview).

  From this screen, you can do the following:

* You can customize the same push message for *App Inbox*. 
* You can change the title color, message color, and background color and add filter tags that classify your message into tabs. For more information, refer to [Message Tags](doc:create-message-app-inbox#define-the-message-content). 
* You can set a Time To Live (TTL) for the *App Inbox* message in the *Setup* section. For more information on setting up TTL, refer to [Time to Live](doc:create-message-app-inbox#define-the-message-content).

## Pull Notification and App Inbox Stats

You can view the stats for messages copied to *App Inbox* on the *Push Stats* page. The percentage boost represents the percentage of messages boosted by *App Inbox* compared to the total of messages sent via *App Inbox* and *Pull Notification*.

To view the stats for the copied messages, navigate to *App Inbox stats* tab.

<Image title="Push Uplift with App Inbox" alt={5344} align="center" border={true} src="https://files.readme.io/a2437a9-enhanced_push_deliver_2.png">
  Pull Notification and App Inbox Stats
</Image>

## Optimize Push Impressions

CleverTap SDK raises the *Push Impression* event when the end user's device displays a push notification. This is important because a push successfully sent might not be delivered or displayed on the user's device due to various reasons such as:

* The device's battery optimization killed the app's background activity and suppressed the push notification. Hence, it could not be displayed. This is observed in most Android devices.
* The user is offline, and the push was delivered after the TTL duration. Hence, the push notification was not displayed. The user unsubscribes the notification channel ID used for the push notification in the Android app settings, and hence the push was dismissed by the Operating System (OS).
* If the user is in an unstable network, Push Impression might not be sent but counted as sent. Also, users may have unsubscribed push notifications from the app on the device level, which causes low CTR too.
* When a push is sent from CleverTap, it is delivered to the end user through Firebase. Chinese OEMs usually suppress push notifications for battery optimization, thereby reducing deliveries.

**To increase reachability, CleverTap provides the following options:**

* *Pull Notification*: For more information about optimizing delivery using pull notifications, refer to [Optimize Delivery via Pull Notification](https://docs.clevertap.com/docs/push-optimize-delivery#optimize-delivery-via-pull-notification).
* *Push + App Inbox Campaigns*: The message from push would be sent to the App Inbox when a user launches the app. Integrating with other push notification providers to increase reach and deliverability. For more information, refer to the following documentation: 
  * [Xiaomi Push Integration](https://developer.clevertap.com/docs/xiaomi-push-notifications)
  * [Huawei Push Integration](https://developer.clevertap.com/docs/clevertap-huawei-push-integration)
  * [Baidu Push Integration](https://developer.clevertap.com/docs/baidu-push-notifications)
* Also, if your application is custom-handling the push notification in Android, you must raise the Push Impression event in your Push Handling code. For more information, refer to the [Android SDK](https://developer.clevertap.com/docs/android) documentation. 
* For both (Android and iOS), you must upgrade your respective application with CleverTap SDK version 3.5.1 or above to track the Push Impression. Ensuring the Push Impression is implemented correctly might help increase the Push Impression numbers marked on CleverTap.
* If your application displays the push notification using your custom code and not through CleverTap SDK, then you must raise the *Notification Clicked* event through your code by calling the following code:
  ```
  1CleverTapAPI.getDefaultInstance(application).pushNotificationClickedEvent(activity.getIntent().getExtras());
  ```

# Push Campaign Throttling

You can throttle the rate at which CleverTap delivers push notifications under *Settings* > *Setup* > *Campaign Limits*. If your user base is large and all users receive and click on a push notification at roughly the same time to open the app, you could experience a significant, unwanted load on your systems.

By using push campaign throttling, you can meter how quickly CleverTap delivers your notifications.

> 👍 Push Campaign Throttling Example
>
> If your reachable audience for a campaign is 500,000 users and your back-end systems can only support up to 20% of them, you can set a throttle limit to 100,000 notifications per 15-minute interval. The entire campaign will then deliver in 1 hour 15 minutes.

\<Push throttling section is repeated here?>
