---
title: Direct Call
excerpt: Understand how to make direct calls from your app.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
# Overview
CleverTap's Direct Call is a new age calling feature that works on Voice Over Internet Protocol (VoIP) technology. The Direct Call SDK enables sending and receiving voice over the internet. As long as a device has an internet connection and the Direct Call SDK, you can make calls happen. Direct Call SDK makes the calls from within the apps without sharing the actual phone number of the call initiator. Direct calls require minimal customization and prove to be cost-effective.

# Getting Started
Navigate to the CleverTap dashboard and click *Direct Call* under *Message*
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9de955c-Direct_Call_Navigation.png",
        "Direct Call Navigation.png",
        2846,
        1344,
        "#c4d8c1"
      ],
      "border": true
    }
  ]
}
[/block]
## Account Settings
To setup Direct Call on Android, click *Settings* > *Direct Call* > *Integration*
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/69fbe64-Direct_Call_SDK_Integration.png",
        "Direct Call SDK Integration.png",
        2842,
        1196,
        "#f6f7f8"
      ],
      "border": true
    }
  ]
}
[/block]
After creating your account, you can view the **API Key** and **Account ID** on the CleverTap dashboard.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5a92de7-Account_settings.png",
        "Account_settings.png",
        2370,
        566,
        "#fafafb"
      ],
      "border": true
    }
  ]
}
[/block]
# Integration
CleverTap Direct Call feature work for all the platforms. This section explains the integration of Direct Call SDK for all the supported platforms.

## Integrate Web
Refer to [Web SDK Integration Guide](https://developer.clevertap.com/docs/web-sdk) to understand the integration of the Direct Call Web SDK.

## Integrate Android
Refer to [Android SDK Integration guide](https://developer.clevertap.com/docs/direct-call-android-sdk-integration-document-421) to understand the integration of the Direct Call Android SDK.

## Integrate iOS
Refer to [iOS SDK Integration Guide](https://developer.clevertap.com/docs/ios-sdk) to understand the integration of the Direct Call iOS SDK.

### Upload iOS Identifiers
iOS identifiers are the pre-requisites of integrating Direct Call iOS SDK. Upload the following iOS identifiers on your infra to enable the VoIP push:
* Team ID
* Bundle ID
* Authkey .p8 file
* .p12 VoIP certificate
* .pem VoIP certificate
* Key ID
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7f7deaf-iOS_Identifiers.png",
        "iOS Identifiers.png",
        693,
        499,
        "#fafbfc"
      ],
      "border": true
    }
  ]
}
[/block]
# Direct Call Settings
This section covers how to set up Call Branding, Content, and Styles of the call screen.

## Branding
You can customize the brand logo, theme, and color via the **Direct Call Branding** feature. An incoming call with the business's branding on the user's screen indicates authenticity. It is done via the CleverTap dashboard under Direct Call settings.

To set up Call Branding, navigate to *Direct Call* > *Branding*
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a59c91a-Branding_Navigation.png",
        "Branding Navigation.png",
        2840,
        1194,
        "#f6f7f8"
      ],
      "border": true
    }
  ]
}
[/block]
## Create Content
To create content for the call screen enter the following:
* The URL of the image of your Brand Logo.
* The Message or Context of your call (Maximum 20 characters).
* Click *Done*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2334828-Create_Content.png",
        "Create_Content.png",
        2376,
        1154,
        "#f2f1f2"
      ],
      "border": true
    }
  ]
}
[/block]
## Create Style
To create the content style, select the following:
* Background color of the call screen.
* Color of the text on the call screen.
* Button theme (Default/White).
* Click *Done*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/261b958-Create_Style.png",
        "Create_Style.png",
        2374,
        1354,
        "#f3f2f3"
      ],
      "border": true
    }
  ]
}
[/block]
## Direct Call Stats
Click the *Stats* tab to view direct call stats. Select the duration for the call stats.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/37cff67-Direct_Call_Stats.png",
        "Direct_Call_Stats.png",
        2728,
        1420,
        "#fbf9fb"
      ],
      "border": true
    }
  ]
}
[/block]
### Call Status
Call Status is the status of all the Direct Calls initiated via the CleverTap Direct Call SDK.
* **Declined** - shows the calls disconnected by the receiver.
* **Missed** - shows the calls missed by the receiver.
* **Cancelled** - shows the calls canceled by the initiator.
* **Over** - shows the calls completed.

### Call volumes
Call volumes can help you identify the period during which the app handles maximum calls.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/85b3603-Call_Volumes.png",
        "Call_Volumes.png",
        2606,
        984,
        "#fcfcfd"
      ],
      "border": true
    }
  ]
}
[/block]
# Calling Screen
This section shows incoming and outgoing call screens on Android, iOS, and Web platforms.

## Android Call Screen
Following is an example of a call screen on android devices:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7862382-Android_Call_Screen.png",
        "Android_Call_Screen.png",
        1566,
        1034,
        "#9e9c9c"
      ],
      "border": true
    }
  ]
}
[/block]
## iOS Call Screen
Following is an example of a call screen on iOS devices:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/19f9ed4-Ios_Call_Screen.png",
        "Ios_Call_Screen.png",
        1568,
        1018,
        "#a3a0a0"
      ],
      "sizing": "smart",
      "border": true
    }
  ]
}
[/block]
## Web Call Screen
Following is an example of a call screen on web browsers:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4581b61-web_call.png",
        "web call.png",
        2040,
        1380,
        "#f8f8fa"
      ],
      "border": true
    }
  ]
}
[/block]
# Use cases
Refer to [Sample Events by Business Vertical](https://docs.clevertap.com/docs/direct-call-use-cases) for sample use cases by vertical that you can solve with CleverTap Direct Call.  

# FAQs
Q. What is a Direct Call?
A. Direct Call means sending and receiving voice over the internet. As long as a device has an internet connection and the Direct Call SDK, you can make calls on any device or browser.

Q. Why do you need Direct Call?
A. Direct Call has many advantages because it is software-driven. Developers have the ultimate control over call flows, call screens, etc. Since telecom operators do not control this medium, it is very cost-effective.

Q. Does the Direct Call work if a user has switched off his internet?
A. No, you can not make Direct Calls without the internet.

Q. Do Direct Calls work on 3G/4G/WiFi?
A. Yes, they work on all networks.

Q. Are there any special permissions required?
A. Yes, the end-user/consumer must allow permission to use the device microphone.

Q. Does a phone ring if the app is running in the background?
A. Yes, the phone rings. The user sees an incoming call screen with options to answer or decline the call.

Q. Does a phone ring if the app is killed?
A. An end-user may not receive the Direct Call if the app is killed.

Q. What kind of businesses should use the Direct Calls feature?
A. Ideally, all the digital businesses with a few exceptions. Such as where a user doesn't interact with the app frequently or if the frequency of opening the app is more than three days.

Q. How does a business ensure that its logo and brand color are set on the incoming, ongoing, and outgoing call screens?
A. They can do this via the CleverTap dashboard under Direct Call settings.

Q. What is the size of the SDK?
A. The Direct Call Android SDK is <500KB, for iOS, it is 7.5MB and the Web SDK is 356KB.

Q. How frequently the business needs to update the SDK?
A. The SDK may require an update once a year. However, you may have to roll out an update if there is a compliance requirement due to Android or iOS updates.

Q. How is a business charged for the calls?
A. A business is charged based on the minutes consumed. The business can choose from different packs based on its consumption patterns. 

Q. Does Direct Call work on mobile web?
A. Yes, the system can initiate calls from the mobile web. However, there are limitations on receiving calls (the browser window/tab must be active).

Q. How is CleverTap better than what businesses have today?
A. CleverTap works on data channels, so cost savings are apparent. However, the real value-add is the trustworthiness of the incoming call due to the **Context** (the reason why a user is getting the call), **Branding** with logo and brand colors (the call is authentic and is coming from a legitimate business)

Q. Are there any examples today for us to understand the use case?
A. Yes, in India, **Uber** introduced Direct Calls under the "Free Call" feature. It is used when a taxi is booked and the user is waiting for the taxi. The user and the driver can call each other without revealing the number of either party.