---
title: Test Push Notifications
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
This section covers how to send test notifications in operations in two ways and test push notifications with multiple logins.

#Send Test Notifications in Operations
The test notification can be sent during the campaign creation. 

Once you are all done setting up the content of your campaign in the *What* section, you have the option to send a test push notification to any CleverTap user profile you have marked as a *Test profile*.
Click the **Preview & Test** button from the message editor to test a message.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a9f309e-push_test_notification.png",
        "push_test_notification.png",
        836,
        603,
        "#d4d4d9"
      ],
      "border": true
    }
  ]
}
[/block]
In the second approach, you can initiate *Send Push* for the required device to send test push notifications to the user on a specific user profile page. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4bd5d33-2.png",
        "2.png",
        1999,
        406,
        "#f6f6f7"
      ],
      "border": true
    }
  ]
}
[/block]
#Send Test Notifications with Multiple Logins
If there are multiple logins during a test push notification, the push token moves to the latest profile. 

If a user has multiple devices associated with a profile, then the push notification from the campaign that the user has qualified into will be received by the latest device. The event is being captured in real-time as the campaign sends notifications to the latest active device.