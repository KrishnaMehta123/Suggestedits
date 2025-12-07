---
title: Debugger
excerpt: 'CleverTap Debugger: Enhancing Integration Troubleshooting'
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
> 📘 Private Beta
> 
> Currently, this feature is a Private Beta Release. If you want access to this feature, contact your Account Manager.

# Overview

The CleverTap Debugger feature is a robust tool that simplifies integration and debugging with CleverTap. The primary objective is to improve the go-live process by assisting users in auditing integration and swiftly resolving errors directly on the CleverTap dashboard. 

# Key Objectives

The Debugger feature aims for the following:

- Ensures data is correctly sent to CleverTap by visually confirming its ingestion.
- Provides a single place from where you can view events and user properties of debug-enabled profiles.
- Check the Reachability status
- Enables you to check the data and data types sent from the App to CleverTap on a single view along with timestamps. 

# Prerequisites

Before using the CleverTap Debugger feature, ensure you have the following:

- Access to CleverTap Test or Production account.
- Successfully integrated CleverTap SDK's debugger-supported version into your application or website. The following table lists the Debugger-supported SDK versions for different platforms:

| Platform     | Debugger-Supported Version |
| :----------- | :------------------------- |
| iOS          | v5.2.1 or higher           |
| Android      | v.5.2.1 or higher          |
| Cordova      | v2.7.2. or higher          |
| Flutter      | v1.9.1 or higher           |
| React Native | v1.1.2 or higher           |
| Unity        | v.3.0.0 or higher          |
| Web          | v.1.6.7 or higher          |

- Enabled the Debug Mode. The steps to enable this mode vary depending on your platform. Refer to the respective debugger documentation as listed below:

  - [iOS](https://developer.clevertap.com/docs/advanced-options-ios#debugging)
  - [Android](https://developer.clevertap.com/docs/android-advanced-features#debugging) 
  - [Cordova](https://developer.clevertap.com/docs/cordova-advance-features#debugging)
  - [Flutter](https://developer.clevertap.com/docs/flutter-advanced-features#debugging) 
  - [React Native](https://developer.clevertap.com/docs/react-native-advanced-features#debugging) 
  - [Unity](https://developer.clevertap.com/docs/unity-advanced-features#debugging) 
  - [Web](https://developer.clevertap.com/docs/web-quickstart-guide#debugging) 

# Access the Debugger Feature

Click the <img src= "https://files.readme.io/28f71a8-Debugger_Icon_.png" height="30px" width="30px" >  _Debugger_ icon on the left pane of the CleverTap dashboard. 

  The _Debugger_ page opens, displaying all the user profiles with their details. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/76336f8d4f51354ea0971f562d66e66c1c8e6c79d1cc68a8dd02e7a44e150680-Debugger.png",
        null,
        "Accessing the Debugger Feature "
      ],
      "align": "center",
      "border": true,
      "caption": "Accessing the Debugger Feature "
    }
  ]
}
[/block]


> 📘 Data Storage
> 
> - Debug data remains accessible for a duration of _seven_ days from the time the data is fetched.
> - Each account is equipped with the capacity to execute up to 1000 storage requests.
> - The system can handle up to 100 incoming storage requests per minute.

You can view the following details for the debugged user profile:

| Field          | Description                                                                                                                                                                                                |
| :------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| _Time_         | This field displays the exact date and time when the user interaction occurred.                                                                                                                            |
| _Data_         | This field displays the raw data associated with a specific user interaction. It includes information about the actions taken, events triggered, and any relevant data points tied to the user's activity. |
| _Category_     | This indicates if the data in the user profile is Events or User Property.                                                                                                                                 |
| _Identity_     | This field displays a unique user ID.                                                                                                                                                                      |
| _Device model_ | This field displays the device model that the user uses. This can be instrumental in identifying hardware-specific issues or compatibility problems.                                                       |
| _Source_       | This field displays the SDK associated with the user profile.                                                                                                                                              |

# Search

From the _Debugger_ page, you can search for a user profile in the search bar. You can also search for event name, _Identity_, _Device model_, or _Source_. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/50f62efd5a16bf5a5d4a981f9395122981adf95a97725004525388700b4248ba-Debugger_Search_.gif",
        "",
        "Search Functionality"
      ],
      "align": "center",
      "border": true,
      "caption": "Search Functionality"
    }
  ]
}
[/block]


# Play/Pause for User Profile

You can use the _Play_ or _Pause_ icon to start or pause processes during debugging, making it easier to examine and control the execution of debugging sessions. This feature is available only at the user level.

# Refresh

Click the <img src= "https://files.readme.io/02c530b-Refresh_Icon.png" height="30px" width="30px" >   _Refresh_ icon to update the _Debugger_ page. This action displays the most recent data when a filter is applied, or you are not on the initial.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/017dca2289d7bf836a944e2c0bbe28680f35a609aaec28105f1ab0e2d8ce2e15-Debugger_Refresh.gif",
        "",
        "Refresh Functionality"
      ],
      "align": "center",
      "border": true,
      "caption": "Refresh Functionality"
    }
  ]
}
[/block]


# Accessing User Profile

When troubleshooting user-specific issues or gaining deeper insights into user interactions, it iscrucial to be able to delve into individual user profiles. Click on the individual user profile on the _Debugger_ page to view the details on the left pane. 

The following details appear on the left pane of the _Debugger_ page.

## User Profile

This section provides a summary of the primary identifiers selected for the project. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d8eaad0820b319380b75d9b6583b9fecf40f123f751ae5fbbe4218cb58a5cb53-Debugger_User_Profile.png",
        null,
        "User Profile View"
      ],
      "align": "center",
      "border": true,
      "caption": "User Profile View"
    }
  ]
}
[/block]


This summary typically includes:

| Field           | Description                                      |
| :-------------- | :----------------------------------------------- |
| _CleverTap ID_  | A unique identifier within the CleverTap system. |
| _Phone Number_  | The user's registered phone number.              |
| _Email Address_ | The user's registered email address.             |

1. Click the _Copy_ icon beside the respective fields to copy _CleverTap ID_, _Phone Number_, or _Email Address_.
2. Click the _View Profile_ icon to check the individual user profile details. The _Find People_>  
   _Profile_ page appears. For more information on user details, view Profile[ Details](https://docs.clevertap.com/docs/find-people).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0c0231e5ae022d89f1079e741341ca12c99d0eab5f3c004ebeea056d53bd6768-Debugger_User_Profiles.gif",
        "",
        "Refresh Functionality"
      ],
      "align": "center",
      "border": true,
      "caption": "View Profile"
    }
  ]
}
[/block]


> 📘 User Profile states
> 
> - **Identity Present**- In this case, the user's identity is established, and the corresponding ID is displayed. If there is a profile push onto the profile, the data column displays Profile data, and the data type indicates whether it is a Profile property or identity. If both profile properties and identity are present, the profile property is shown. 
> - **Identity Absent**- If identity is not set, then the field is empty.

## JSON Payload

In the JSON payload section, you can view the JSON payload of data coming in from the SDK/JSON for an event or user property. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7a10033f616524ca7ea210f13624b6af31796bc74b767e7516ade72b83e5b8fa-Debugger_JSON_Payload_.png",
        null,
        "Profile Property View"
      ],
      "align": "center",
      "border": true,
      "caption": "JSON Payload View"
    }
  ]
}
[/block]


> 📘 Reload Time
> 
> If the JSON payload section does not load within 10 seconds, please refresh the page.

## Reachability

This allows you to verify if the user is reachable on the following channels:

- Mobile Push
- Email
- SMS
- Web Push

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a76459f852b57ca6c6ecd2f1c79d375e575d68c47083a821e1a5f9fee2401743-Debugger_Reachability.png",
        null,
        "Channels Reachability"
      ],
      "align": "center",
      "border": true,
      "caption": "Channels Reachability"
    }
  ]
}
[/block]


Under the _Status_ column for individual channels, you can view the following state for the channels:

| Status          | Description                                                                                                    |
| :-------------- | :------------------------------------------------------------------------------------------------------------- |
| _Reachable_     | Indicates that the user is reachable on the respective channel. This is indicated by the green status icon.    |
| _Not Reachable_ | Indicates that the user is not reachable on the respective channel. This is indicated by the grey status icon. |