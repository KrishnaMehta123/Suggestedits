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

# June 2025

| Change Release Date | Event Name                  | Property Name | Update Type | Description                                                                                                                                                                                                                    |
| :------------------ | :-------------------------- | :------------ | :---------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| July 1, 2025        | Notification Failed         |               | Event Added | This event captures the errors that occurred in the WhatsApp campaign.                                                                                                                                                         |
| June 30, 2025       | CT Coupon Rewarded          |               | Event Added | This event is raised when the coupon is issued to a user through a Promo campaign. For more information about the properties of this event, refer to CT Coupon Rewarded under [System Events](doc:events#system-events).       |
| June 30, 2025       | CT Coupon Redeemed          |               | Event Added | This event is raised when the user redeems the coupon through the coupon redemption API. For more information about the properties of this event, refer to CT Coupon Redeemed under [System Events](doc:events#system-events). |
| June 30, 2025       | CT Coupon Reverted          |               | Event Added | This event is raised when a redeemed coupon is reversed. For more information about the properties of this event, refer to CT Coupon Reverted under [System Events](doc:events#system-events).                                 |
| June 30, 2025       | CT Points Credited          |               | Event Added | This event is raised when points are credited to the loyalty wallet. For more information about the properties of this event, refer to CT Points Credited under [System Events](doc:events#system-events).                     |
| June 30, 2025       | CT Points Debited           |               | Event Added | This event is raised when points are debited from the loyalty wallet. For more information about the properties of this event, refer to CT Points Debited under [System Events](doc:events#system-events).                     |
| June 30, 2025       | CT Partner Voucher Rewarded |               | Event Added | This event is raised when a user receives a third-party partner voucher. For more information about the properties of this event, refer to CT Partner Voucher Rewarded under [System Events](doc:events#system-events).        |

# February 2025

[block:parameters]
{
  "data": {
    "h-0": "Change Release Date",
    "h-1": "Event Name",
    "h-2": "Property Name",
    "h-3": "Update Type",
    "h-4": "Description",
    "0-0": "February 5, 2025",
    "0-1": "Notification Delivered",
    "0-2": "-",
    "0-3": "Others",
    "0-4": "Now, this event is raised for Email campaigns, indicating the successful delivery to the end user. For more information, refer to [Email Campaign Stats](doc:email-campaign-stats-delivered).  \n  \n**Note**: Delivered is currently released in Private Beta. Contact your Customer Success Manager to enable this for email campaigns."
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


# October 2024

[block:parameters]
{
  "data": {
    "h-0": "Change Release Date",
    "h-1": "Event Name",
    "h-2": "Property Name",
    "h-3": "Update Type",
    "h-4": "Description",
    "0-0": "October 11, 2024",
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


# June 2024

[block:parameters]
{
  "data": {
    "h-0": "Change Release Date",
    "h-1": "Event Name",
    "h-2": "Property Name",
    "h-3": "Update Type",
    "h-4": "Description",
    "0-0": "June 19, 2024",
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


# May 2024

| Change Release Date | Event Name        | Property Name | Update Type      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| :------------------ | :---------------- | :------------ | :--------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| May 15, 2024        | Push Unregistered |               | Properties Added |                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|                     |                   | Source        |                  | <ul><li> **CT_Push**: Indicating that the event is raised via silent Push. In this case, FCM returns a [404 Unregistered error](<>) for stale tokens from devices that have not connected to FCM for 270 days or for users who have uninstalled the app. </li> <li> **CT_SDK**: Indicating that the event is raised via OnUserLogin() method.</li> <li> **CT_Target**: Indicating that the event is raised via campaigns or journeys. </li></ul> |
|                     |                   | Token Value   |                  | The property contains the actual value of the token.                                                                                                                                                                                                                                                                                                                                                                                             |
|                     |                   | Token Type    |                  | <ul><li> FCM </li> <li> Baidu </li> <li> Huawei </li></ul>                                                                                                                                                                                                                                                                                                                                                                                       |
|                     |                   | targetId      |                  | The property denotes the ID of the campaign or journey.                                                                                                                                                                                                                                                                                                                                                                                          |

# April 2024

[block:parameters]
{
  "data": {
    "h-0": "Change Release Date",
    "h-1": "Property Name",
    "h-2": "Event Name",
    "h-3": "Update Type",
    "h-4": "Description",
    "0-0": "April 2, 2024",
    "0-1": "",
    "0-2": "Notification Clicked",
    "0-3": "Property Added",
    "0-4": "",
    "1-0": "",
    "1-1": "button_id",
    "1-2": "",
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