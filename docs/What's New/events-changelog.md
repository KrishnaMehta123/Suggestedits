---
title: Events Changelog
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
Welcome to the Events changelog document for CleverTap. This changelog provides insights about the system event updates in CleverTap, ensuring you use CleverTap effectively and monitor your metrics with greater accuracy.

We are dedicated to empowering businesses with advanced mobile marketing and analytics capabilities and delivering continuous improvements to meet our users' evolving needs. Stay tuned as we update this changelog regularly, informing our customers about any changes to existing system events or the introduction of new ones.

<br />

# October

<br />

[block:parameters]
{
  "data": {
    "h-0": "Change Release Date",
    "h-1": "Event Name",
    "h-2": "Property Name",
    "h-3": "Update Type",
    "h-4": "Description",
    "0-0": "October 11th, 2024",
    "0-1": "Notification Failed",
    "0-2": "",
    "0-3": "Others",
    "0-4": "Now, this event also captures the errors that occur in email campaigns.  \n  \n**Note**: This event is currently in Private Beta. Contact your account manager to enable this event."
  },
  "cols": 5,
  "rows": 1,
  "align": [
    "left",
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]


# June

[block:parameters]
{
  "data": {
    "h-0": "Change Release Date",
    "h-1": "Event Name",
    "h-2": "Property Name",
    "h-3": "Update Type",
    "h-4": "Description",
    "0-0": "June 19th, 2024",
    "0-1": "Notification Failed",
    "0-2": "",
    "0-3": "Event Added",
    "0-4": "This event captures the errors that occurred in the campaign.  \n  \nThis event is currently in private beta and can be enabled upon request. Contact your account manager if you need access to this event.",
    "1-0": "",
    "1-1": "",
    "1-2": "Campaign ID",
    "1-3": "",
    "1-4": "The property helps identify the specific campaign associated with the error.",
    "2-0": "",
    "2-1": "",
    "2-2": "Campaign Type",
    "2-3": "",
    "2-4": "The property indicates the type of campaign (e.g., WhatsApp, SMS, Email).",
    "3-0": "",
    "3-1": "",
    "3-2": "Error",
    "3-3": "",
    "3-4": "The property describes the title of the error observed in the campaign.",
    "4-0": "",
    "4-1": "",
    "4-2": "Label",
    "4-3": "",
    "4-4": "The property denotes the specific label associated with the error.",
    "5-0": "",
    "5-1": "",
    "5-2": "Variant",
    "5-3": "",
    "5-4": "The property helps identify the errors for a specific campaign variant in the case of A/B, split delivery, or multi-variant campaigns."
  },
  "cols": 5,
  "rows": 6,
  "align": [
    "left",
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]


# May

[block:parameters]
{
  "data": {
    "h-0": "Change Release Date",
    "h-1": "Event Name",
    "h-2": "Property Name",
    "h-3": "Update Type",
    "h-4": "Description",
    "0-0": "May 15, 2024",
    "0-1": "Push Unregistered",
    "0-2": "",
    "0-3": "Properties Added",
    "0-4": "",
    "1-0": "",
    "1-1": "",
    "1-2": "Source",
    "1-3": "",
    "1-4": "The property can have any one of the following values:  \n  \n<ul><li> **CT_Push**: Indicating that the event is raised via silent Push. In this case, FCM returns a [404 Unregistered error](https://firebase.google.com/docs/reference/fcm/rest/v1/ErrorCode) for stale tokens from devices that have not connected to FCM for 270 days or for users who have uninstalled the app. </li> <li> **CT_SDK**: Indicating that the event is raised via OnUserLogin() method.</li> <li> **CT_Target**: Indicating that the event is raised via campaigns or journeys. </li></ul>",
    "2-0": "",
    "2-1": "",
    "2-2": "Token Value",
    "2-3": "",
    "2-4": "The property contains the actual value of the token.",
    "3-0": "",
    "3-1": "",
    "3-2": "Token Type",
    "3-3": "",
    "3-4": "The property indicates the type of token and can have any one of the following values:  \n  \n<ul><li> FCM </li> <li> Baidu </li> <li> Huawei </li></ul>",
    "4-0": "",
    "4-1": "",
    "4-2": "targetId",
    "4-3": "",
    "4-4": "The property denotes the ID of the campaign or journey."
  },
  "cols": 5,
  "rows": 5,
  "align": [
    "left",
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]


# April

[block:parameters]
{
  "data": {
    "h-0": "Change Release Date",
    "h-1": "Event Name",
    "h-2": "Property Name",
    "h-3": "Update Type",
    "h-4": "Description",
    "0-0": "April 2, 2024",
    "0-1": "Notification Clicked",
    "0-2": "",
    "0-3": "Property Added",
    "0-4": "",
    "1-0": "",
    "1-1": "",
    "1-2": "button_id",
    "1-3": "",
    "1-4": "The property is visible for the event if the _Notification Clicked_ event is tracked for button clicks associated with the new Image Interstitial template. Therefore, the customers adopting this template will see this new property.  \n  \nFor more information, refer to [In-App Image Interstitial Template](doc:in-app-editor#image-interstitial)."
  },
  "cols": 5,
  "rows": 2,
  "align": [
    "left",
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]