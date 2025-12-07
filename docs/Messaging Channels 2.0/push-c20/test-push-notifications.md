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
## Overview

This section covers how to send test notifications in operations in two ways and test push notifications with multiple logins.

# Send Test Notifications in Operations

The test notification can be sent during the campaign creation. 

Once you are all done setting up the content of your campaign in the *What* section, you have the option to send a test push notification to any CleverTap user profile you have marked as a *Test profile*.\
Click the **Preview & Test** button from the message editor to test a message.

<Image title="push_test_notification.png" alt={836} className="border" border={true} src="https://files.readme.io/a9f309e-push_test_notification.png" />

In the second approach, you can initiate *Send Push* for the required device to send test push notifications to the user on a specific user profile page. 

<Image title="2.png" alt={1999} className="border" border={true} src="https://files.readme.io/4bd5d33-2.png" />

# Send Test Notifications with Multiple Logins

If there are multiple logins during a test push notification, the push token moves to the latest profile. 

If a user has multiple devices associated with a profile, then the push notification from the campaign that the user has qualified into will be received by the latest device. The event is being captured in real-time as the campaign sends notifications to the latest active device.
