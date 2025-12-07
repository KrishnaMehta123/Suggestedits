---
title: Optimize Push Delivery_RenderMax_WIP
excerpt: >-
  Understand how to optimize push messages with Enhanced Push Delivery and App
  Inbox
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

You can optimize push delivery using the following two features: 

* Sending the push message to App Inbox 

You can optimize the delivery rate by sending the content for push message to *App Inbox* when the user enables DND for push messages or throttling campaigns. 

## Optimize Delivery via App Inbox

You can further optimize the delivery of push notifications by sending a copy of the same message to *App Inbox*. 

To send a copy of the push message to **App Inbox**, select *Send a copy of this message to the App Inbox* that appears at the bottom of the message builder of push notification in the *What* section.

![746](https://files.readme.io/d3fa57a-campaign_push_app_inbox.png "campaign_push_app_inbox.png")

> 📘 App Inbox as its Own Channel
>
> *App Inbox* also exists as a stand-alone channel. For more information, refer to [App Inbox](doc:app-inbox-overview).

  From this screen, you can do the following:

* You can customize the same push message for *App Inbox*. 
* You can change the title color, message color, and background color and add filter tags that classify your message into tabs. For more information, refer to [Message Tags](doc:create-message-app-inbox#define-the-message-content). 
* You can set a Time To Live (TTL) for the *App Inbox* message in the *Setup* section. For more information on setting up TTL, refer to [Time to Live](doc:create-message-app-inbox#define-the-message-content).

## Enhanced Push Delivery and App Inbox Stats

You can view the stats for push messages copied to *App Inbox* on the *Push Stats* page. The percentage boost represents the percentage of messages boosted by *App Inbox* compared to the total of messages sent via *App Inbox* and *Enhanced Push Delivery*.

To view the stats for the copied messages, navigate to *App Inbox stats* tab.

<Image title="enhanced push deliver 2.png" alt={5344} className="border" border={true} src="https://files.readme.io/a2437a9-enhanced_push_deliver_2.png" />

# Push Campaign Throttling

You can throttle the rate at which CleverTap delivers push notifications under *Settings* > *Setup* > *Campaign Limits*. If your user base is large and all users receive and click on a push notification at roughly the same time to open the app, you could experience a significant, unwanted load on your systems.

By using push campaign throttling, you can meter how quickly CleverTap delivers your notifications.

> 👍 Push Campaign Throttling Example
>
> If your reachable audience for a campaign is 500,000 users and your back-end systems can only support up to 20% of them, you can set a throttle limit to 100,000 notifications per 15-minute interval. The entire campaign will then deliver in 1 hour 15 minutes.
