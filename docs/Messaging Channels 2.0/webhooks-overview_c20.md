---
title: Webhooks
excerpt: Monitor specific events.
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
      title: Setup Webhooks
      url: https://docs.clevertap.com/docs/webhooks-overview_c20
    - type: link
      title: Create Webhooks
      url: https://docs.clevertap.com/docs/create-message-webhook_c20
    - type: link
      title: Personalize Webhooks
      url: https://docs.clevertap.com/docs/personalize-message-webhooks_c20
    - type: link
      title: Webhook Stats
      url: https://docs.clevertap.com/docs/webhooks-stats_c20
---
# Overview

CleverTap webhooks enable you to pass user information basis on specific business workflows to any third-party endpoint. 

For example, when a high-value transaction is abandoned on your e-commerce website, you can send details about the abandoned products and user details via a webhook campaign to your operations center.

There are six categories of webhooks that you can create. The table below describes each of those categories.
[block:parameters]
{
  "data": {
    "h-0": "Type",
    "h-1": "Description",
    "h-2": "Example",
    "0-0": "Single action",
    "1-0": "Actions",
    "2-0": "Inaction within time",
    "3-0": "Inaction",
    "4-0": "Date time property",
    "5-0": "Actions with user properties",
    "5-1": "Performed an action or not, filtered by their demographic properties.",
    "4-1": "Period of time after a date time property on a user event.",
    "3-1": "Users performed an action, but did not perform another action.",
    "2-1": "User performed an action, but does not perform another action within a certain time.",
    "1-1": "User performed multiple actions.",
    "0-1": "User performed an action.",
    "0-2": "User launched the app.",
    "1-2": "User launched the app and viewed a notification.",
    "2-2": "User has not launched the app in three days.",
    "3-2": "User launched the app, but did not view a notification.",
    "4-2": "User purchased an item and three days have passed.",
    "5-2": "User purchased an item and lives in Canada."
  },
  "cols": 3,
  "rows": 6
}
[/block]