---
title: Optimize Delivery
excerpt: ''
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
      title: Collapse Key
      url: https://docs.clevertap.com/docs/collapse-key
    - type: link
      title: Test Push Notifications
      url: https://docs.clevertap.com/docs/test-push-notifications
    - type: link
      title: Post Action Webhooks
      url: https://docs.clevertap.com/docs/post-action-webhooks-c20
    - type: link
      title: Push Campaign Stats
      url: https://docs.clevertap.com/docs/push-campaign-stats
    - type: link
      title: Push Troubleshooting & FAQs
      url: https://docs.clevertap.com/docs/troubleshooting-faqs-push-notifications
---
## Overview

You can optimize push delivery with push amplification and sending to the app inbox. Push amplification can be achieved via retrying the *Push* message as is (where messages are suppressed by the device) and *App Inbox* where the user has chosen to DND the push messages.

## Optimize via Push Amplification

Push notifications are a great way to engage customers despite the issue of low deliverability on certain device manufacturers. 

With push amplification at your disposal, you can counter this challenge by enhancing the delivery of push notifications to devices that missed receiving them.

To enable this feature, navigate to *Settings* > *Engage* > *Setup* > *Push Amplification*. Turn on the push amplification toggle as displayed below:

<Image title="Screenshot 2019-01-09 at 6.58.11 AM.png" alt={945} className="border" border={true} src="https://files.readme.io/188e8ce-Screenshot_2019-01-09_at_6.58.11_AM.png" />

> 🚧 Toggling Push Notification Amplification
>
> All the push campaigns that are created *after* turning on the push amplification toggle are amplified. Similarly, no new campaigns are amplified after the push amplification is turned off.

Once push amplification is turned on, your campaigns reach more users through your push notifications. You can check these boost numbers on your push campaign stats page.

<Image title="push_amplification_optimize_delivery.png" alt={2672} className="border" border={true} src="https://files.readme.io/1c984d8-push_amplification_optimize_delivery.png" />

> 📘 Support for Push Amplification via Inbox
>
> We support *Push Amplification via Inbox* and retrying push notifications due to delivery issues with certain OEMs. 
>
> If the app is online when *Push* is delivered, the Inbox delivery is done on the next *App Launch* and not immediately after the *Push* is delivered.

## Optimize via App Inbox

Apart from push amplification, you can further increase the delivery of push notifications by sending a copy of the same message to *App Inbox*. 

To send a copy of the push message to **App Inbox**, click the checkbox that appears at the bottom of the message builder of push notification in the *What* section.

![746](https://files.readme.io/d3fa57a-campaign_push_app_inbox.png "campaign_push_app_inbox.png")

> 📘 App Inbox as its Own Channel
>
> *App Inbox* also exists as a stand-alone channel. For more information, refer to [App Inbox](https://docs.clevertap.com/docs/app-inbox-overview).

  From this screen, you can do the following:

* You can customize the same push message for *App Inbox*. 
  * You can change the title color, message color, background color and add filter tags that classify your message into tabs. For more information, refer to [Message Tags](https://docs.clevertap.com/docs/app-inbox#section-message-tags). 
  * You can set a time to live (TTL) for the *App Inbox* message in the setup section. For more information on setting up TTL, refer to [Time to Live](https://docs.clevertap.com/docs/app-inbox#section-time-to-live).

## Push Amplification and App Inbox Stats

You can view the stats for push messages copied to *App Inbox* on the *Push stats* page. The percentage boost represents the percentage of messages boosted by *App Inbox* compared to the total of messages sent via *App Inbox* and *Push Amplification*.

To view the stats for the copied messages, you can use the tab *App Inbox stats*.

<Image title="push_amplification_stats.png" alt={5344} className="border" border={true} src="https://files.readme.io/2a58958-push_amplification_stats.png" />

# Push Campaign Throttling

You can throttle the rate at which CleverTap delivers push notifications under *Settings* > *Setup* > *Campaign Limits*. If your user base is large and all users receive and click on a push notification at roughly the same time to open the app, you could experience a significant, unwanted load on your systems.

By using push campaign throttling, you can meter how quickly CleverTap delivers your notifications.

> 👍 Push Campaign Throttling Example
>
> If your reachable audience for a campaign is 500,000 users and your back-end systems can only support up to 20% of them, you can set a throttle limit to 100,000 notifications per 15-minute interval. The entire campaign will then deliver in 1 hour 15 minutes.
