---
title: Collapse Key
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
[block:api-header]
{
  "title": "Overview"
}
[/block]
A collapse notification key or collapse key is used to update push notifications on Android and iOS devices.
[block:callout]
{
  "type": "info",
  "body": "The collapse key feature is only specific to Android devices.",
  "title": "Android Only"
}
[/block]
This feature is used to update a notification that is rendered and available in the notification tray. While setting up the campaigns, check that the same key is used in similar campaigns. For example, a Score Update notification if the key used is *score-update*. All following campaigns that would be used to update earlier notifications must have the same key.
[block:callout]
{
  "type": "info",
  "body": "A new notification will be rendered if the earlier notification was dismissed and not present on the device notification tray.",
  "title": "New Notification"
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/73ae9f0-Collapse_Key.png",
        "Collapse Key.png",
        989,
        159,
        "#ececee"
      ],
      "border": true
    }
  ]
}
[/block]
#Use Case
Following is the order in which a notification can be replaced:

Push notification 1 (general notification) > Notification 2 (promo code or coupon) > Notification 2 with a higher validity. 

Coupon code to avail free snacks with orders above $20 at 5:00 PM > Promotional code valid for one hour can be sent at 7:00 PM > Replace it with a thank you notification for ordering and status tracking notification.