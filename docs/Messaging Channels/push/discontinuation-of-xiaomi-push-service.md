---
title: Discontinuation of Xiaomi Push Service
excerpt: (Pls ignore this page - it has been moved to dev docs.)
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Xiaomi Corporation made a significant announcement recently, notifying users about discontinuing the Mi Push service beyond Mainland China due to operational concerns. You might have already received communication regarding this matter (see the following image).

<Image alt="Mi Push Service Discontinuation Notification" align="center" border={true} src="https://files.readme.io/216611a-Discontinuation_Message.png">
  Mi Push Service Discontinuation Notification
</Image>

# Who Does this Shutdown Affect?

The change solely affects App Push Notifications sent to Xiaomi Devices via XPS.

# Impact of Shutdown

With the Mi Push service's closure, CleverTap will cease offering Mi Push support for Xiaomi devices. However, the overall functionality for receiving notifications on Xiaomi devices will still be maintained, but through Firebase Cloud Messaging (FCM) after the shutdown. 

You can still use the CleverTap Push and Rendermax<sup>TM</sup> to send push notifications to Xiaomi devices along with all other OEM devices.

**Other changes that CleverTap would be making regarding Mi Push deprecation**

Starting from Android SDK version v6.1.0, CleverTap will discontinue the support for Mi Push. Consequently, CleverTap will remove the provision to set up the Xiaomi credentials from the CleverTap dashboard and will remove all the existing credentials.

<Image alt="Mi Push Settings" align="center" border={true} src="https://files.readme.io/403a8ce-image.png">
  Mi Push Settings
</Image>

# When Does CleverTap Plan to Implement the Changes?

To ensure a smooth transition and help our customers adapt to forthcoming adjustments, we will continue the Mi Push service for Xiaomi devices until March 30th, 2024. Starting March 31st, 2024, Xiaomi devices will be directed through the FCM service instead.

# Action Required

Upgrade your app to CleverTap Android SDK v6.1.0 and above, expected to be released on February 20, 2024, and promptly remove the XPS SDK usage. This must be done immediately to prevent any potential errors or crashes. The steps to do so will be listed under the [Changelog](https://github.com/CleverTap/clevertap-android-sdk/blob/master/CHANGELOG.md) after the CleverTap Android v6.1.0 is released.
