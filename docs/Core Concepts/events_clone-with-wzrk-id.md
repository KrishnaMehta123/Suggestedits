---
title: Events_clone with WZRK ID_WIP
excerpt: ''
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

Events track what individual actions users perform in your app or website. Some examples of events include a user launching an app, viewing a product, listening to a song, sharing a photo, making a purchase, or favoriting an item.

By tracking events in your app, you can better understand what users are doing. In CleverTap, you can analyze these events in many different ways, such as getting aggregating metrics of a specific event or measuring how a specific event type trends over time. You can also engage with your users based on these events by creating campaigns in CleverTap that are triggered by them. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/40b874a-events1.png",
        "events1.png",
        898,
        704,
        "#fcfcfc"
      ],
      "border": true
    }
  ]
}
[/block]
**Event Categories**

There are two categories of events in CleverTap: System Events and Custom Events. 

System Events are events recorded automatically after you integrate our SDK. Custom Events are events you define and track with our SDK or API.

**Event Properties**

Events have details that describe the action taking place called properties. 

For example, while recording the “Product viewed” event, you could also store event properties like product name, category, and price. Recording event properties will help you answer questions like which category of products are more popular and help you segment users based on which categories or price points they’ve viewed.

# System Events 

System Events are events recorded automatically after you integrate our SDK. 
[block:parameters]
{
  "data": {
    "h-0": "Event Type",
    "h-1": "Description",
    "h-2": "How Event is Tracked",
    "0-0": "App Installed",
    "1-0": "App Launched",
    "2-0": "App Uninstalled",
    "4-0": "Notification Sent",
    "5-0": "Notification Viewed",
    "5-1": "This event is tracked when a user views an email, in-app notification, or a web notification sent from CleverTap.",
    "5-2": "The CleverTap SDK recognizes when a notification sent via CleverTap is viewed by a user.\n\nNotification Viewed is available for Email, Web Push, InApp, Web Popup and App Inbox.",
    "4-1": "This event is tracked when a campaign message is sent to a user. This event is always recorded, even if the user does not open or click on the message. This event is recorded for email, mobile push, SMS, web push, and Facebook Audience campaigns. The Notification Sent event is available on the Event dashboard but it is not displayed on the User Profile.",
    "4-2": "The event is tracked when the notification is successfully sent from CleverTap to the communication channel you select for your campaign.",
    "2-1": "This event is recorded when a user uninstalls your application.",
    "2-2": "This event is tracked by sending silent push notifications, which are type of notification that is not rendered on a user’s device. We send silent push notifications to your entire install base once every 24 hours to track uninstalls. For more information, please see [App Uninstall](https://clevertap.com/blog/track-app-uninstalls-effectively/).",
    "1-1": "This event is recorded every time a user launches your application.",
    "1-2": "There are two cases when this event will recorded. The first case is a fresh app launch, which is when an app is launched from a killed state. The second case is when a app is brought to the foreground after 20 minutes of inactivity in the background.",
    "0-1": "This event is recorded when a user installs your application.",
    "0-2": "The event is raised when the user launches the app for the first time. \n\nThere are three cases when this event will be recorded multiple times for a single user. The first case is when a user installs your app, uninstalls it, and then reinstalls it. The second case is when clear your app's memory. The third case is when a user installs your app on multiple devices.",
    "6-0": "Notification Clicked",
    "6-1": "This event is tracked only when a user clicks on a campaign sent via CleverTap. You can track or create a Notification Clicked event for every UTM Visited event that is tracked by CleverTap and not any other provider. There is no separate event storage required for the Notification Clicked event because it is derived from the UTM Visited event.",
    "6-2": "Recorded when a user clicks on a mobile push, in-app, email, web-popup or web push message sent via the CleverTap dashboard, or through the campaign API. \n\nThe Android Push notifications containing deep links to third-party apps are not tracked.",
    "3-0": "UTM Visited",
    "3-1": "This event is tracked when user clicks on a link from a marketing campaign that has a UTM parameter defined on it. This event is also tracked when a CleverTap-integrated attribution platform, such as Branch or Apsalar, sends this information to CleverTap.",
    "3-2": "The UTM Visited event is recorded for your marketing campaigns from external sources, such as Google Adwords or AdRoll.",
    "7-0": "Push Impressions",
    "7-1": "This event is tracked when a Push notification sent from CleverTap is delivered on a user’s device. The funnels on the Push campaign statistics page reflects the count for this event.",
    "7-2": "After the toggle for Push Impressions is turned on/setup from settings, the CleverTap SDK starts recording an event whenever a Push notification sent via CleverTap is delivered to the user’s device.",
    "8-0": "App Version Changed",
    "8-1": "This event is raised when a user’s current app version is different from the user’s previous app version.",
    "8-2": "This event is tracked when the \"CT App version\" system property differs from one \"App Launched\" event to another.",
    "9-0": "Notification Replied",
    "9-1": "This event is recorded when a user replies to a WhatsApp message.",
    "9-2": "This event is raised when the brand receives a reply from the user.",
    "10-0": "Reply Sent",
    "10-1": "This event is recorded when an agent (CleverTap user) replies to a message from the end user.",
    "10-2": "This event is raised against the user profile of the end user.",
    "11-0": "State Transitioned",
    "11-1": "This event is recorded for lifecycle optimizer when a user transitions from one stage to another.",
    "11-2": "This event is raised whenever a user transitions from one state to another or from unmapped to one of the states in the lifecycle optimization framework. It is meant for internal usage at CleverTap and therefore unavailable for querying.",
    "12-0": "Session Concluded",
    "12-1": "This event is recorded to mark the end of a session. Session Tracking must be enabled for the event to be tracked.",
    "12-2": "This event is raised when there is 20 minutes of inactivity after an event is raised for a user."
  },
  "cols": 3,
  "rows": 13
}
[/block]
# Debug Events
Debug Events are events recorded automatically after you integrate our SDK. These events are raised at certain lifecycle stages in your integration and helps you track and manage your integration
These events are available on any profile page and Find People page by adding a parameter to the url '*?showDebugEvents=true*'
[block:parameters]
{
  "data": {
    "0-0": "Identity Set",
    "0-1": "This DEBUG event is raised when a new user is identified on a customer’s app or an identified user pushes another identity.",
    "0-2": "This event monitors the status and data points that are important for the identification and engagement of users. This event is for monitoring and debugging only.",
    "h-0": "Event Name",
    "h-1": "Description",
    "h-2": "When is it raised",
    "1-0": "Identity Reset",
    "1-1": "This DEBUG event is raised when a profile is de-merged (after de-merge a new profile for every device is created and identities are dropped) either from dashboard (“reset identities” click on profile page) or through the Demerge Profile API.",
    "1-2": "It monitors the reset of identities and handles unnecessary merges. This event is used for monitoring and debugging only.",
    "2-0": "Identity Error",
    "2-1": "This DEBUG event is raised when an existing identity is associated incorrectly with another identity. The former identity is now declared as invalid for the latter's profile.",
    "2-2": "This event is for monitoring and debugging when identity merges are invalid",
    "3-0": "Reachable By",
    "3-1": "This DEBUG event is raised when a user becomes reachable by a communication channel, such as SMS, Email, Mobile Push, or there are changes to the existing communication channel.",
    "3-2": "Tracked for a profile when\n- Push token is added/changed.\n- Email ID is added/changed\n- Phone number is added/changed."
  },
  "cols": 3,
  "rows": 4
}
[/block]
# Custom Events

Custom Events are events you define and track with our SDK or API. For more information, please visit our [developer documentation](https://developer.clevertap.com/v1.0/docs/concepts-events).

# Event Metadata Recorded Automatically

For every event that’s recorded, CleverTap records the following standard metadata:
  * Information about the user who performed the event.
  * Date and time when the event was recorded.
  * The number of screens viewed by the user before performing the action.
  * The referring site and the source of the user visit if it was from an external source.

Additionally, CleverTap keeps the user profiles updated with the latest:
  * Geographic information like their city, region, country, and latitude/longitude (if available).
  * Browser or device make, model, etc. used to access the website or app.

# System Properties

CleverTap tracks the following system properties automatically from the mobile SDK. All the system properties are prefixed by ‘CT’, indicating that they are provided by CleverTap. 

The following properties are tracked automatically on all events:
[block:parameters]
{
  "data": {
    "1-0": "CT Latitude",
    "h-0": "System Property",
    "0-0": "CT App version",
    "h-1": "Description",
    "0-1": "This is the current version of your application installed on the user device.",
    "1-1": "The user location identified by the latitude.",
    "2-0": "CT Longitude",
    "2-1": "The user location identified by the longitude.",
    "3-0": "CT Source",
    "3-1": "The source of the event.\nFor example, the event may originate from a Mobile SDK or an API.\n\nAll possible values:\n  * Mobile (Mobile SDK)\n  * MobileWeb (Web SDK)\n  * Web (Web SDK)\n  * API\n  * segment\n  * appsflyer\n  * apsalar\n  * branch\n  * tune\n  * System (For events generated by CleverTap)"
  },
  "cols": 2,
  "rows": 4
}
[/block]
The following properties are available on the App Launched event:
[block:parameters]
{
  "data": {
    "h-0": "System Property",
    "h-1": "Description",
    "0-0": "CT App version",
    "0-1": "This is the current version of your application installed on the user device.",
    "1-0": "CT Latitude",
    "1-1": "The user location identified by the latitude.",
    "2-0": "CT Longitude",
    "2-1": "The user location identified by the longitude.",
    "3-0": "CT OS Version",
    "3-1": "The Operating system of the device. \nFor example,  1.0.0",
    "4-0": "CT SDK Version",
    "4-1": "The CleverTap SDK version. For example, 30501",
    "5-0": "CT Network Carrier",
    "5-1": "The network carrier of the device.\nFor example, AT&T, Vodafone.",
    "6-0": "CT Network Type",
    "6-1": "The network type of the device\nFor example, 4g",
    "7-0": "CT Connected To WiFi",
    "7-1": "Indicates if the device is connected to the Wi-FI.",
    "8-0": "CT Bluetooth Version",
    "8-1": "The Bluetooth version of the device",
    "9-0": "CT Bluetooth Enabled",
    "9-1": "Indicates if  Bluetooth is enabled on the device.",
    "10-0": "CT Source",
    "10-1": "The source of the event.\nFor example, the event may originate from a Mobile SDK or an API.\n\nAll possible values:\n  * Mobile (Mobile SDK)\n  * MobileWeb (Web SDK)\n  * Web (Web SDK)\n  * API\n  * segment\n  * appsflyer\n  * apsalar\n  * branch\n  * tune\n  * System (For events generated by CleverTap)"
  },
  "cols": 2,
  "rows": 11
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "Latitude and Longitude",
  "body": "The system properties 'latitude' and 'longitude' are captured and sent from the SDK only if the user gives consent on your app."
}
[/block]
##Notification Viewed event 
The following properties are available on the Notification Viewed event:

[block:parameters]
{
  "data": {
    "h-0": "System Property",
    "h-1": "Description",
    "0-0": "wzrk_id",
    "0-1": "Open rate tracking ID (can be empty or it might not be present).",
    "h-2": "Raise event if",
    "0-2": "This event is tracked when a user views an email, in-app notification, or a web notification sent from CleverTap.",
    "1-0": "wzrk_pivot",
    "1-1": "Variant of the A/B test",
    "2-0": "Campaign type",
    "2-1": "CT campaign type (push,Web,Webhook,)",
    "3-0": "Campaign id",
    "3-1": "CT campaign id",
    "4-0": "wzrk_acct_id",
    "4-1": "CT account id",
    "5-0": "wzrk_cid",
    "5-1": "Channel ID",
    "6-0": "wzrk_pid",
    "6-1": "Campaign ID",
    "7-0": "wzrk_rnv",
    "7-1": "If present and not empty, it will raise notification viewed event",
    "8-0": "wzrk_ttl",
    "8-1": "time to live",
    "9-0": "wzrk_bc",
    "9-1": "Batch count",
    "10-0": "wzrk_bp",
    "10-1": "Image URL",
    "11-0": "wzrk_ck",
    "11-1": "Collapse key (the actual key which you have provided)",
    "12-0": "wzrk_dl",
    "12-1": "deeplink",
    "13-0": "wzrk_pn",
    "13-1": "If present, this notification is sent from CleverTap.",
    "14-0": "wzrk_sound",
    "14-1": "Custom sound to play or not boolean value.",
    "15-0": "wzrk_collapsible",
    "15-1": "Collapse key (the actual key which you have provided) {@ankita same as wzrk_ck ? what is the difference?}",
    "16-0": "CT App Version",
    "16-1": "CT version",
    "17-0": "CT Source",
    "17-1": "Mobile Phone or Desktop",
    "18-0": "CT Latitude",
    "18-1": "last known latitude captured by CT (on APP launch)",
    "19-0": "CT Longitude",
    "19-1": "Last known longitude captured by CT (on APP launch)"
  },
  "cols": 3,
  "rows": 20
}
[/block]
##Notification sent

[block:parameters]
{
  "data": {
    "h-0": "System Property",
    "h-1": "Description",
    "h-2": "Raised event if",
    "0-0": "Campaign Id",
    "0-1": "campaign id",
    "0-2": "This event is tracked when a campaign message is sent to a user. This event is always recorded, even if the user does not open or click on the message. This event is recorded for email, mobile push, SMS, web push, and Facebook Audience campaigns. The Notification Sent event is available on the Event dashboard but it is not displayed on the User Profile.",
    "1-0": "Campaign type",
    "1-1": "type of campaign - push, email, etc",
    "2-0": "Labels",
    "2-1": "labels added to campaign"
  },
  "cols": 3,
  "rows": 3
}
[/block]
##Notification clicked

[block:parameters]
{
  "data": {
    "0-0": "wzrk_acct_id",
    "h-0": "System Property",
    "h-1": "Description",
    "h-2": "Raised event if",
    "0-1": "account id",
    "0-2": "This event is tracked only when a user clicks on a campaign sent via CleverTap.",
    "1-0": "wzrk_bc",
    "1-1": "badge count",
    "2-0": "wzrk_bi",
    "2-1": "badge icon",
    "3-0": "wzrk_c2a",
    "3-1": "call to action (c2a) buttons",
    "4-0": "wzrk_cid",
    "4-1": "channel id",
    "5-0": "wzrk_ck",
    "5-1": "Collapse key (the actual key which you have provided)",
    "6-0": "wzrk_clr",
    "6-1": "If present and not empty, it contains the Hex value of the colour to be applied on the small icon (and app name for Android versions below Pie)",
    "7-0": "wzrk_cts",
    "7-1": "Clicked Timestamp",
    "8-0": "wzrk_collapsible",
    "8-1": "if collapse key is added",
    "9-0": "wzrk_dl",
    "9-1": "deep link",
    "10-0": "wzrk_nms",
    "10-1": "notification message summary",
    "11-0": "wzrk_pid",
    "11-1": "Internal Push notification id",
    "12-0": "wzrk_pivot",
    "12-1": "Variant of the A/B test",
    "13-0": "wzrk_pn",
    "13-1": "If present, this notification is sent from CleverTap.",
    "14-0": "wzrk_rnv",
    "14-1": "Flag to raise notification viewed event",
    "15-0": "wzrk_sound",
    "15-1": "custom sound (true/flase)",
    "16-0": "wzrk_st",
    "16-1": "notification subtext",
    "17-0": "wzrk_ttl",
    "17-1": "time to live",
    "18-0": "Campaign id",
    "18-1": "campaign id",
    "19-0": "CT App Version",
    "19-1": "app version",
    "20-0": "CT Source",
    "20-1": "Mobile or Web"
  },
  "cols": 3,
  "rows": 21
}
[/block]
##Push Impression
This event is raised when a push notification is delivered/rendered on the device.

[block:parameters]
{
  "data": {
    "h-0": "System Property",
    "h-1": "Description",
    "h-2": "Raised event if",
    "0-0": "CT App Version",
    "0-1": "app version",
    "1-0": "CT Source",
    "1-1": "Mobile or Web",
    "2-0": "Campaign type",
    "2-1": "email/push",
    "3-0": "wzrk_acct_id",
    "3-1": "account id",
    "4-0": "wzrk_bc",
    "4-1": "badge count",
    "5-0": "wzrk_bi",
    "5-1": "badge icon",
    "6-0": "wzrk_cid",
    "6-1": "channel id",
    "7-0": "wzrk_dl",
    "7-1": "deep link",
    "8-0": "wzrk_id",
    "8-1": "campaign id",
    "9-0": "wzrk_pid",
    "9-1": "Internal Push notification id",
    "10-0": "wzrk_pivot",
    "10-1": "Variant of the A/B test",
    "11-0": "wzrk_pn",
    "11-1": "If present, this notification is sent from CleverTap.",
    "12-0": "wzrk_rnv",
    "12-1": "Flag to raise notification viewed event",
    "13-0": "wzrk_sound",
    "13-1": "custom sound (true/flase)",
    "14-0": "wzrk_ttl",
    "14-1": "time to live"
  },
  "cols": 2,
  "rows": 15
}
[/block]
##App Installed
This event is recorded when a user installs your application.
[block:parameters]
{
  "data": {
    "h-0": "System Property",
    "h-1": "Description",
    "0-0": "CT App Version",
    "0-1": "app version",
    "1-0": "CT Source",
    "1-1": "Mobile or Web"
  },
  "cols": 2,
  "rows": 2
}
[/block]
##App Uninstalled

{@ankita need info here}
[block:parameters]
{
  "data": {
    "h-0": "System Property",
    "h-1": "Description"
  },
  "cols": 2,
  "rows": 1
}
[/block]

##Identity Set

This DEBUG event is raised when a new user is identified on a customer’s app or an identified user pushes another identity.

[block:parameters]
{
  "data": {
    "h-0": "System Property",
    "h-1": "Description",
    "0-0": "ID",
    "0-1": "user identity",
    "1-0": "Type",
    "1-1": "new or existing user",
    "2-0": "Source",
    "2-1": "API/ SDK",
    "3-0": "Dropped History",
    "3-1": "if history is dropped"
  },
  "cols": 2,
  "rows": 4
}
[/block]
##Identity Reset

This DEBUG event is raised when a profile is de-merged (after de-merge a new profile for every device is created and identities are dropped) either from dashboard (“reset identities” click on profile page) or through the Demerge Profile API.

[block:parameters]
{
  "data": {
    "h-0": "System Property",
    "h-1": "Description",
    "0-0": "Dropped History",
    "0-1": "if history is dropped",
    "1-0": "Source",
    "1-1": "API/ SDK"
  },
  "cols": 2,
  "rows": 2
}
[/block]
##Identity Error

This DEBUG event is raised when an existing identity is associated incorrectly with another identity. The former identity is now declared as invalid for the latter's profile.
[block:parameters]
{
  "data": {
    "0-0": "ID",
    "0-1": "user identity",
    "1-0": "Source",
    "1-1": "API/ SDK",
    "h-0": "System Property",
    "h-1": "Description"
  },
  "cols": 2,
  "rows": 2
}
[/block]
##Reachable By
This DEBUG event is raised when a user becomes reachable by a communication channel, such as SMS, Email, Mobile Push, or there are changes to the existing communication channel.
[block:parameters]
{
  "data": {
    "0-0": "type",
    "0-1": "channel type where reachable - Email or push",
    "1-0": "value",
    "1-1": "email of the user if reachable via email and push token if reachable via Mobile Push",
    "h-0": "System Property",
    "h-1": "Description"
  },
  "cols": 2,
  "rows": 2
}
[/block]
##App Version Change

This event is raised when a user’s current app version is different from the user’s previous app version.
[block:parameters]
{
  "data": {
    "h-0": "System Property",
    "h-1": "Description",
    "0-0": "CT App Version",
    "1-0": "CT Previous App Version",
    "2-0": "CT Source",
    "0-1": "current app version",
    "1-1": "previous app version",
    "2-1": "mobile"
  },
  "cols": 2,
  "rows": 3
}
[/block]
##Webhook Delivered
This event is raised when a webhook is delivered.
[block:parameters]
{
  "data": {
    "0-0": "CT Source",
    "1-0": "Campaign id",
    "0-1": "system",
    "1-1": "campaign id",
    "h-0": "System Property",
    "h-1": "Description"
  },
  "cols": 2,
  "rows": 2
}
[/block]
##UTM Visited

This event is tracked when user clicks on a link from a marketing campaign that has a UTM parameter defined on it. This event is also tracked when a CleverTap-integrated attribution platform, such as Branch or Apsalar, sends this information to CleverTap.
[block:parameters]
{
  "data": {
    "h-0": "System Property",
    "h-1": "Description",
    "0-0": "install",
    "1-0": "provider",
    "0-1": "if this is an install",
    "1-1": "attribution provider integrated with"
  },
  "cols": 2,
  "rows": 2
}
[/block]