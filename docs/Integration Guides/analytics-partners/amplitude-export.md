---
title: Amplitude Export
excerpt: Understand how you can export event data from CleverTap dashboard to Amplitude
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
[block:callout]
{
  "type": "info",
  "title": "Feature in Beta",
  "body": "Currently, this is a private beta feature. If you have any queries about the feature, contact CleverTap Customer Success Team."
}
[/block]

# Overview

The data export feature provides the capability to export your CleverTap event data to your Amplitude dashboard. You can use this event data for further analysis.

# Setup
This process involves adding Amplitude details to the CleverTap dashboard. To add the project details to the CleverTap dashboard:
a. Log in to your CleverTap account.
b. Navigate to *Settings* > *Partners* > *Exports*. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e941d6c-Amplitude_unconnected.png",
        "Amplitude unconnected.png",
        1708,
        964,
        "#f6f7f9"
      ],
      "border": true
    }
  ]
}
[/block]
c. Click the **Amplitude** icon under the *Unconnected partners* section. The *Amplitude* page is displayed.
d. Enter the Amplitude details.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b37e1b5-Enter_Amplitude_details.png",
        "Enter Amplitude details.png",
        1390,
        888,
        "#fafbfd"
      ],
      "border": true
    }
  ]
}
[/block]
The project details can be obtained by navigating to *Settings* > *Projects* on the Amplitude dashboard and selecting the project for which you want to view the details.
[block:parameters]
{
  "data": {
    "h-0": "Field",
    "0-0": "Amplitude API Key",
    "1-1": "The Data Residency is the physical/geographical storage location of a project's data and is at a project level (per project). Select from the following available options:\n* Europe\n* Standard",
    "1-0": "Data Residency",
    "2-0": "Amplitude User ID Mapping",
    "2-1": "This identifier will be mapped to Amplitude's `user_id` field while sending data from CleverTap to Amplitude.",
    "3-0": "Amplitude Device ID Mapping",
    "3-1": "This identifier will be mapped to Amplitude's `device_id` field while sending data from CleverTap to Amplitude.",
    "h-1": "Description",
    "0-1": "It is the unique code passed to Amplitude to verify your credentials. You can find the API key under *Settings* > *Projects*."
  },
  "cols": 2,
  "rows": 4
}
[/block]
e. Click **Save credentials**. On clicking, the following popup is displayed:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/befc108-Credentials_saved.png",
        "Credentials saved.png",
        1388,
        880,
        "#7e7f81"
      ],
      "border": true
    }
  ]
}
[/block]
Amplitude is now displayed under Connected partners when you navigate to  *Settings* > *Partners* > *Exports*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d0dee3b-Amplitude_connected.png",
        "Amplitude connected.png",
        1390,
        830,
        "#f9f8fa"
      ],
      "border": true
    }
  ]
}
[/block]
# Create New Export
To create a new export:
1. Navigate to *Settings* > *Partners* > *Exports*.
2. Navigate to the *Activity log* tab and then click **+ Create Export**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/577eb72-Create_export.png",
        "Create export.png",
        1388,
        978,
        "#f6f7f8"
      ],
      "border": true,
      "sizing": "smart"
    }
  ]
}
[/block]
On clicking, the *Create an export* popup is displayed.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8658e96-Create_an_export_popup.png",
        "Create an export popup.png",
        1384,
        938,
        "#a1a2a3"
      ],
      "border": true
    }
  ]
}
[/block]
3. Configure the following settings:
    * **Choose an export partner**: Select *Amplitude* from the *Choose an export partner* dropdown list.
    * Export details: Select the events to export from the available options. For more information, refer to [Export Details](https://docs.clevertap.com/docs/amplitude-export#export-details).
    * Choose export frequency: Select from one of the following options
       * One time: Single export for the export type selected. You can export data up to the last 60 days. 
       * Recurring: Set up a recurring export that exports all the new events/user profiles captured in the last window. You can export as frequently as every 4 hours and up to once every 24 hours. 
4. Click **Create export**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f9d455e-Click_create_export.png",
        "Click create export.png",
        1390,
        1022,
        "#a6a6a7"
      ],
      "border": true,
      "sizing": "smart"
    }
  ]
}
[/block]
On successful creation of export, the following message is displayed:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b36d7bc-Export_created_successfully.png",
        "Export created successfully.png",
        1390,
        972,
        "#7a7b7d"
      ],
      "border": true
    }
  ]
}
[/block]
5. Click **Ok** to return to the *Exports* page. CleverTap processes the export, and you can now see the newly created export for Amplitude.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/13572f5-Export_page.png",
        "Export page.png",
        1384,
        968,
        "#f6f6f7"
      ],
      "border": true
    }
  ]
}
[/block]
The status for each export is displayed as *Pending* as soon as the export is created. The status changes to *Running* after the processing starts. And, it changes to *Done* when the export is complete.

# Stop Export
You can also stop the export that you have created. To do so:

1. Click the ![ellipses](https://files.readme.io/0210143-ellipses_icon.png) icon for the export request you want to stop and then click ![stop](https://files.readme.io/930e98c-Stop_icon.png). 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6340035-Click_Stop.png",
        "Click Stop.png",
        1382,
        966,
        "#f5f6f8"
      ],
      "border": true
    }
  ]
}
[/block]
You are prompted to confirm your action.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a5797fa-Confirm_stop_export.png",
        "Confirm stop export.png",
        1386,
        698,
        "#868586"
      ],
      "border": true
    }
  ]
}
[/block]
2. Click **Yes, stop export** to stop the export request. On clicking, the following message is displayed:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1a50eb7-Export_stopped_successfully.png",
        "Export stopped successfully.png",
        1398,
        958,
        "#7b7c7d"
      ],
      "border": true
    }
  ]
}
[/block]
3. Click **Ok** to return to the *Exports *page.

# Export Details
Select from one of the following options to export events from CleverTap to the Amplitude dashboard:

## All events
Export data for all defined events including System and Custom events.

## Selected events
Select the specific events that you want to export from CleverTap to the Amplitude dashboard.

## Engagement Events
Export the following engagement events:
[block:parameters]
{
  "data": {
    "h-0": "CleverTap Event Name",
    "h-1": "Event Description",
    "0-0": "Notification Sent",
    "1-0": "Notification Viewed",
    "2-0": "Notification Clicked",
    "3-0": "Push Impressions",
    "4-0": "Notification Replied",
    "5-0": "Push Unregistered",
    "6-0": "Control Group",
    "7-0": "Channel Unsubscribed",
    "8-0": "Reachable By",
    "9-0": "Push Impressions",
    "10-0": "Notification Delivered",
    "11-0": "AB Experiment Rendered",
    "12-0": "AB Experiment Stopped",
    "13-0": "AB Experiment Rolled Out",
    "14-0": "Geocluster Entered",
    "15-0": "Geocluster Exited",
    "16-0": "Reply Sent",
    "17-0": "App Uninstalled",
    "18-0": "Webhook Delivered",
    "19-0": "State Transitioned",
    "20-0": "UTM Visited",
    "0-1": "The event is tracked when the notification is successfully sent from CleverTap to the communication channel you select for your campaign.",
    "1-1": "This event is tracked when a user views an email, in-app notification, or a web notification sent from CleverTap.",
    "2-1": "This event is tracked only when a user clicks on a notification sent via CleverTap.Recorded when a user clicks on a mobile push, in-app, email, web-popup, or web push message sent via the CleverTap dashboard or through the campaign API.",
    "3-1": "This event is tracked when a Push notification sent from CleverTap is delivered on a user’s device.",
    "4-1": "This event is recorded when a user replies to a WhatsApp message.",
    "5-1": "The event raised when the user unregisters to receive Push Notifications.",
    "6-1": "The event raised when a campaign is activated with a Control group.",
    "7-1": "The event raised when a user Unsubscribes to receive further communication through a channel",
    "8-1": "* The debug event raised when the user becomes reachable by a communication channel such as SMS, email, mobile push, or when there are changes to the existing communication channel.\n* Tracked for a profile when:\n   * Push token is added/changed.\n   * Email ID is added/changed.\n   * Phone number is added/changed.",
    "9-1": "This event is tracked when a push notification sent from CleverTap is delivered on a user’s device. The funnels on the Push campaign statistics page reflect the count for this event.",
    "10-1": "This event is recorded when communication is delivered to the user's device",
    "11-1": "This event is recorded when communication is delivered to the user who is part of an A/B experiment campaign",
    "12-1": "This event is recorded when AB experiment is stopped.",
    "13-1": "This event is recorded when AB experiment is started",
    "14-1": "This event is recorded to mark when a device enters a geofence.",
    "15-1": "This event is recorded to mark when a device exits a geofence.",
    "16-1": "This event is recorded when an agent (CleverTap user) replies to a message from the end-user.",
    "17-1": "This event is recorded when a user uninstalls your application.",
    "18-1": "This event is recorded when a Webhook campaign is delivered successfully",
    "19-1": "This event is recorded for lifecycle optimizer when a user transitions from one stage to another.",
    "20-1": "This event is tracked when a user clicks on a link from a marketing campaign that has a UTM parameter defined on it."
  },
  "cols": 2,
  "rows": 21
}
[/block]

[block:callout]
{
  "type": "info",
  "body": "This feature is available for CleverTap for Enterprise plan. Contact your sales account manager to activate it.",
  "title": "Availability of Feature"
}
[/block]