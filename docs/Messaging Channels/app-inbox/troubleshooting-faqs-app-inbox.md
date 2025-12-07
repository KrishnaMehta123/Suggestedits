---
title: 'App Inbox: Troubleshooting and FAQs'
excerpt: ''
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

This section covers FAQs related to the App inbox. 

# FAQs

## Q. Does the app inbox stay after the user has uninstalled the application?

The app inbox would not stay in the application after the user has uninstalled, as the messages are stored locally. Clearing the cache or uninstalling the app deletes the app inbox from the device.  CleverTap does not maintain a user's app inbox state in the backend.

## Q. If a user opens the app after a very long time, will the SDK fetch all the pending app inbox messages for the user?

The SDK will fetch the newest ten messages only. Even though you have launched the application after a long time and have qualified for more than ten app inbox messages, you'll still see only ten messages. The messages should also be under the [Time to Live](https://docs.clevertap.com/docs/create-message-app-inbox#time-to-live-ttl).

## Q. Are special characters supported in the filter tags for app inbox campaigns? For example, an underscore, a hyphen, Chinese characters, Vietnamese/ pinyin characters, and so on.

Yes, special Unicode-encoded characters are supported.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/47b359e-Special_characters.png",
        "Special characters.png",
        634
      ],
      "align": "center",
      "sizing": "smart",
      "border": true
    }
  ]
}
[/block]


## Q. How can I view the notification count for a custom App Inbox?

The inbox message count for a custom App Inbox is available from the `cleverTapDefaultInstance.getInboxMessageCount()` API. For more information, refer to [Create your App-Inbox](https://developer.clevertap.com/docs/android-app-inbox#create-your-app-inbox).