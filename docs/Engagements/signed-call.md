---
title: Signed Call™
excerpt: Learn how to enable Signed Call™ from the CleverTap dashboard.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

Signed Call™ is a new-age voice communication system that uses Voice over Internet Protocol (VoIP) technology. The Signed Call SDKs enable sending and receiving voice over the internet. All you need to make calls is a device with an internet connection and the Signed Call SDK. Signed Call has many advantages because it is software-driven. Signed Call SDKs manage the in-app calling without sharing the user's phone number, and the signed calls are more cost-effective and secure than the usual PSTN calls. Developers have the ultimate control over call flows, call screens, and so on.

Signed Call can help multiple businesses. For more information about business use cases, refer to [Signed Call Use Cases](https://docs.clevertap.com/docs/signed-call-use-cases).

> 📘 Feature in Beta
> 
> This feature is released in private Beta. To enable this feature, contact your CleverTap Customer Success Team or [raise a support ticket](https://help.clevertap.com/hc/en-us/requests/new).

# Signed Call Account Setting

Signed Call is an add-on feature to the existing messaging channels of CleverTap, requiring an additional account setup. After setting up your account, you will get an API Key and an Account ID that you can use to integrate the Signed Call SDKs.

To set up your account, navigate to _Messages_ > _Signed Call_, and click **Sign Up** on the CleverTap dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2c7a1bb-Sign_Up.png",
        "Sign Up",
        "A First Responder Screen showing the Sign-Up button to avail of the Signed Call feature"
      ],
      "align": "center",
      "border": true,
      "caption": "Sign Up for Signed Call"
    }
  ]
}
[/block]


# Set Up Signed Call Integration

The Signed Call feature supports Android, iOS, and Web platforms. This section explains the Signed Call SDK integration for all the supported platforms.  
To set up Signed Call integration:

1. Navigate to _Settings_ > _Signed Call_ > _Integration_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/94e0c79-Signed_Call_Integration.png",
        "Signed Call Integration",
        "A dashboard screen showing Signed Call SDK Integration steps for Android, iOS, and Web platforms. Refer to the Quick Start Guide for documentation"
      ],
      "align": "center",
      "border": true,
      "caption": "Integrate Signed Call SDKs"
    }
  ]
}
[/block]


2. Choose the integration platform and refer to the _Quickstart Guide_ to integrate:

- [Signed Call Android SDK](https://developer.clevertap.com/docs/signed-call-android-sdk)
- [Signed Call iOS SDK](https://developer.clevertap.com/docs/signed-call-ios-sdk)
- [Signed Call Web SDK](https://developer.clevertap.com/docs/signed-call-web-sdk)
- [Signed Call React Native SDK](https://developer.clevertap.com/docs/signed-call-react-native-sdk)
- [Signed Call Flutter SDK](https://developer.clevertap.com/docs/signed-call-flutter-sdk)

> 📘 Signed Call Recordings
> 
> CleverTap exports the Signed Call voice recorded files directly to your Amazon S3 bucket instead of storing them in the database.

# Set Up Signed Call Branding

You can customize the brand logo, theme, and color with the Signed Call Branding feature. An incoming call with business branding helps personalize the user experience. This section explains how to set up _Content_, and _Style_ for the incoming and outgoing call screens. 

To set up Signed Call Branding:

1. Navigate to _Settings_ > _Signed Call_.
2. Click **Branding**.
3. Enter the _Image URL_ of your _Brand Logo_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/80ee6cf-Create_Content.png",
        "Create Content",
        "A dashboard image showing how to set up Branding for your Calling screen from the Create Content tab"
      ],
      "align": "center",
      "border": true,
      "caption": "Create Content for Calling Screen"
    }
  ]
}
[/block]


4. Click **Done**.
5. Click the **Style** tab.
6. Select the _Background Color_.
7. Select the color of the text.
8. Select _Button Theme_ (Default or White).
9. Click **Done**.  
   You can preview how the call screen will look on different devices by switching between the Android and iOS toggle.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/02ab373-Create_Style.png",
        "Create Style",
        "A dashboard image showing how to Create Style i.e. color, text and button theme for your calling screen"
      ],
      "align": "center",
      "border": true,
      "caption": "Create Styles for Calling Screen"
    }
  ]
}
[/block]


> 📘 Override Dashboard's Branding
> 
> You can also show the initiator's and receiver's images on the call screen instead of the brand logo. To do so, use the Override Dashboard's Branding feature for [Android](https://developer.clevertap.com/docs/signed-call-android-sdk#override-the-dashboards-call-screen-branding) and [iOS](https://developer.clevertap.com/docs/signed-call-ios-sdk#override-the-dashboards-call-screen-branding) platforms.

# Signed Call Stats

Signed Call Stats show the analytics of the call initiated using the Signed Call SDKs. These analytics are real-time. You can view, download, and print the analytics chart in different formats.  
To view the stats:

1. Navigate to _Messages_ and click **Signed Call**.
2. Select the duration for the call stats.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ba3a2f6-Signed_Call_Stats.png",
        "Signed Call Stats",
        "A pie chart that represents the call stats for a desired date range from the"
      ],
      "align": "center",
      "border": true,
      "caption": "View Stats"
    }
  ]
}
[/block]


> 📘 Call Detail Records
> 
> Signed Call provides Call Detail Records (CDRs). Customers can choose to export CDRs directly in their S3 Bucket after configuring it on the CleverTap dashboard.

## Call Status

_Call status_ shows the status of all the initiated calls. Following are the status you can view on the dashboard:

- **Over** - shows the completed calls.
- **Declined** - shows the calls disconnected by the receiver.
- **Missed** - shows the calls missed by the receiver.
- **Canceled** - shows the calls canceled by the initiator.

## Call Volumes

The _Call volumes across the day_ board shows the number of calls initiated during a specific period (daily, weekly or monthly).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5d84f6b-Call_Volumes.png",
        "Call Volumes",
        "A line graph that represents the call volumes across the day, week, or a month from the dashboard"
      ],
      "align": "center",
      "border": true,
      "caption": "View Call Volumes"
    }
  ]
}
[/block]


> 📘 Call Volumes
> 
> You can view a maximum of 30 days of calls on this board.

# Call Screens

CleverTap Signed Call provides inbuilt call screens (Outgoing, Ongoing, and Incoming) with Volume, Bluetooth, and Speaker control for all platforms with zero development efforts. The Signed Call system also comes with inbuilt support for network switching, missed call notifications, and call handling if the user is busy on another call.

Following is an example of a Signed Call screen on Android devices:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/699a452-Android_Call_Screen.png",
        "Android Call Screen",
        "An example image from the dashboard showing how the calling screen looks on an Android device"
      ],
      "align": "center",
      "border": true,
      "caption": "Call Screen in an Android Device"
    }
  ]
}
[/block]


Following is an example of a Signed Call screen on iOS devices:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d20f21e-iOS_Call_Screen.png",
        "iOS Call Screen",
        "An example image from the dashboard showing how the calling screen looks on an iOS device"
      ],
      "align": "center",
      "sizing": "smart",
      "border": true,
      "caption": "Call Screen in an iOS Device"
    }
  ]
}
[/block]


Following is an example of a Signed Call screen on Web browsers:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4581b61-web_call.png",
        "web call",
        "An example image from the dashboard showing how the calling screen looks on a web browser"
      ],
      "align": "center",
      "border": true,
      "caption": "Call Screen in a Web Browser"
    }
  ]
}
[/block]


# FAQs

### Q. Does a Signed Call work if users switch off their internet?

A. No, you can not make calls without the internet.

### Q. Does Signed Call work on 3G/4G/WiFi?

A. Yes, Signed Call works on all networks.

### Q. What are the special permissions required for a Signed Call?

A. For Android and Web, the initiator and receivers must allow microphone permission for their device. However, in iOS devices, the Signed Call SDK requires camera permission.

### Q. Does a phone ring if the app runs in the background?

A. Yes.

### Q. Does a phone ring if the app is killed?

A. If the app is killed, the call still connects on iOS. However, in the case of Android, especially in Chinese OEM devices, we do not guarantee to connect a call if the app is killed because of Battery optimization features on these devices. However, we can connect a call for other Android devices even if the app is killed.

### Q. What are the sizes of the Signed Call SDKs?

A. The Signed Call SDKs sizes are ~480KB, ~9MB, and 326KB for Android, iOS, and Web, respectively.

### Q. How frequently the business needs to update the SDK?

A. The SDK may require an update once a year. However, you may have to roll out an update if there is a compliance requirement due to Android or iOS updates.

### Q. How is a business charged for the calls?

A. A business is charged based on the minutes consumed. The business can choose from different packs based on its consumption patterns. 

### Q. Does Signed Call work on mobile web?

A. Yes, the device can make or receive calls from the mobile web, but the browser window or tab must be active.

### Q. Are there any examples today to understand the Signed Call use case?

A. Yes, in India, a ride-hailing company introduced signed calls and named it the "Free Call" feature. The feature is used when a user books a cab. The user and the driver can call each other without revealing the number of either party.

### Q. What are the best practices for initializing Signed Call SDKs?

A. We recommend you initialize the Signed Call SDKs when there is a possibility of initiating and receiving the calls. For example, if you are a Food-Tech company, you would only want to initialize the SDK for the consumer once they place an order. After the order is complete, the Signed Call SDK session can be logged out.

### Q. How is Signed Call better than others?

A. The following are the main USPs of Signed Call:

- Signed Call has the world's lightest SDKs.
- Signed Call uses its signaling stack for the slightest lag in signaling. Also, Signed Call uses Firebase Cloud Messaging (FCM) and Apple Push Notification service (APNs) as a fallback mechanism for ideal performance. This is the only solution that requires zero development effort and can be integrated in no time.
- Signed Call works on data channels, so cost savings are apparent.
- Signed Call provides the ability to determine incoming calls' trustworthiness and effectiveness along with the **Branding** (the call is authentic and comes from a legitimate business) and **Context** (the reason why a user is getting the call) options.