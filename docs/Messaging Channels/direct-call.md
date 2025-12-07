---
title: Direct Call
excerpt: Learn how to enable Direct Call from the CleverTap dashboard.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

Direct Call is a new-age voice communication system that uses Voice Over Internet Protocol (VoIP) technology. The Direct Call SDKs enable sending and receiving voice over the internet. All you need to make calls is a device with an internet connection and the Direct Call SDK. Direct Call has many advantages because it is software-driven. Direct Call SDKs manage the in-app calling without sharing the user's phone number, and the direct calls are more cost-effective and secure than the usual PSTN calls. Developers have the ultimate control over call flows, call screens, and so on.

Direct Call can help multiple businesses. For more examples of business use, refer to [Direct Call Use Cases](https://docs.clevertap.com/docs/direct-call-use-cases).

> 📘 Feature in Beta
>
> This feature is released in private Beta. To enable this feature, contact your CleverTap Customer Success Team or [raise a support ticket](https://help.clevertap.com/hc/en-us/requests/new).

# Direct Call Account Setting

Direct Call is an add-on feature to the existing messaging channels of CleverTap, requiring an additional account setup. After setting up your account, you will get an API Key and an Account ID that you can use to integrate the Direct Call SDKs.

To set up your account, navigate to *Messages* > *Direct Call*, and click **Sign Up** on the CleverTap dashboard.

<Image title="Sign Up.png" alt={2840} className="border" border={true} src="https://files.readme.io/c1f3438-Sign_Up.png" />

# Set Up Direct Call Integration

The Direct Call feature supports Android, iOS, and Web platforms. This section explains the Direct Call SDK integration for all the supported platforms.\
To set up Direct Call integration:

1. Navigate to *Settings* > *Direct Call* > *Integration*.

<Image title="Signed Call Integration.png" alt={1423} className="border" border={true} src="https://files.readme.io/94e0c79-Signed_Call_Integration.png" />

2. Choose the integration platform and refer to the *Quickstart Guide* to integrate:

* [Direct Call Android SDK](https://developer.clevertap.com/docs/direct-call-android-sdk)
* [Direct Call iOS SDK](https://developer.clevertap.com/docs/direct-call-ios-sdk)
* [Direct Call Web SDK](https://developer.clevertap.com/docs/direct-call-web-sdk)

> 📘 Direct Call Recordings
>
> CleverTap exports the Direct Call voice recorded files directly to your Amazon S3 bucket instead of storing them in the database.

# Set Up Direct Call Branding

You can customize the brand logo, theme, and color with the Direct Call Branding feature. An incoming call with business branding helps personalize the user experience. This section explains how to set up *Content*, and *Style* for the incoming and outgoing call screens. 

To set up Direct Call Branding:

1. Navigate to *Settings* > *Direct Call*.
2. Click **Branding**.
3. Enter the *Image URL* of your *Brand Logo*.

<Image title="Create Content.png" alt={1180} className="border" border={true} src="https://files.readme.io/80ee6cf-Create_Content.png" />

4. Click **Done**.
5. Click the **Style** tab.
6. Select the *Background Color*.
7. Select the color of the text.
8. Select *Button Theme* (Default or White).
9. Click **Done**.\
   You can preview how the call screen will look on different devices by switching between the Android and iOS toggle.

<Image title="Create Style.png" alt={1171} className="border" border={true} src="https://files.readme.io/02ab373-Create_Style.png" />

> 📘 Override Dashboard's Branding
>
> You can also show the initiator's and receiver's images on the call screen instead of the brand logo. To do so, use the Override Dashboard's Branding feature for [Android](https://developer.clevertap.com/docs/direct-call-android-sdk#override-the-dashboards-call-screen-branding) and [iOS](https://developer.clevertap.com/docs/direct-call-ios-sdk#override-the-dashboards-call-screen-branding) platforms.

# Direct Call Stats

Direct Call Stats shows the analytics of the call initiated using the Direct Call SDKs. These analytics are real-time. You can view, download, and print the analytics chart in different formats.\
To view the stats:

1. Navigate to *Messages* and click **Direct Call**.
2. Select the duration for the call stats.

<Image title="Signed Call Stats.png" alt={1358} className="border" border={true} src="https://files.readme.io/ba3a2f6-Signed_Call_Stats.png" />

## Call Status

*Call status* shows the status of all the initiated calls. Following are the status you can view on the dashboard:

* **Over** - shows the completed calls.
* **Declined** - shows the calls disconnected by the receiver.
* **Missed** - shows the calls missed by the receiver.
* **Canceled** - shows the calls canceled by the initiator.

## Call Volumes

The *Call volumes across the day* board shows the number of calls initiated during a specific period (daily, weekly or monthly).

<Image title="Call_Volumes.png" alt={2606} className="border" border={true} src="https://files.readme.io/85b3603-Call_Volumes.png" />

> 📘 Call Volumes
>
> You can view a maximum of 30 days of calls on this board.

# Call Screens

CleverTap Direct Call provides inbuilt call screens (Outgoing, Ongoing, and Incoming) with Volume, Bluetooth, and Speaker control for all platforms with zero development efforts. The Direct Call system also comes with inbuilt support for network switching, missed call notifications, and call handling if the user is busy on another call.

Following is an example of a Direct Call screen on Android devices:

<Image title="Android Call Screen.png" alt={772} className="border" border={true} src="https://files.readme.io/699a452-Android_Call_Screen.png" />

Following is an example of a Direct Call screen on iOS devices:

<Image title="iOS Call Screen.png" alt={769} className="border" width="smart" border={true} src="https://files.readme.io/d20f21e-iOS_Call_Screen.png" />

Following is an example of a Direct Call screen on Web browsers:

<Image title="web call.png" alt={2040} className="border" border={true} src="https://files.readme.io/4581b61-web_call.png" />

# FAQs

Q. Does Direct Call work if users switch off their internet?\
A. No, you can not make calls without the internet.

Q. Does Direct Call work on 3G/4G/WiFi?\
A. Yes, Direct Call works on all networks.

Q. What are the special permissions required for Direct Call?\
A. For Android and Web, the initiator and receivers must allow microphone permission of their device. However, in iOS devices, the Direct Call SDK also requires camera permission.

Q. Does a phone ring if the app is running in the background?\
A. Yes.

Q. Does a phone ring if the app is killed?\
A. If the app is killed, the call still connects on iOS. However, in the case of Android, especially in Chinese OEM devices, we do not guarantee to connect a call if the app is killed because of Battery optimization features on these devices. However, for other Android devices, we can connect a call even if the app is killed.

Q. What are the sizes of the Direct Call SDKs?\
A. The Direct Call SDKs sizes are 515KB, 10MB, and 327KB for Android, iOS, and Web, respectively.

Q. How frequently the business needs to update the SDK?\
A. The SDK may require an update once a year. However, you may have to roll out an update if there is a compliance requirement due to Android or iOS updates.

Q. How is a business charged for the calls?\
A. A business is charged based on the minutes consumed. The business can choose from different packs based on its consumption patterns. 

Q. Does Direct Call work on mobile web?\
A. Yes, the device can make or receive calls from the mobile web, but the browser window or tab must be active.

Q. How is Direct Call better than others?\
A. Direct Call works on data channels, so cost savings are apparent. However, the real value-add is the incoming call's trustworthiness and effectiveness due to the **Branding** (the call is authentic and comes from a legitimate business) and **Context** (the reason why a user is getting the call) options.

Q. Are there any examples today to understand the Direct Call use case?\
A. Yes, in India, a ride-hailing company introduced direct calls and named it the "Free Call" feature. The feature is used when a user books a cab. The user and the driver can call each other without revealing the number of either party.
