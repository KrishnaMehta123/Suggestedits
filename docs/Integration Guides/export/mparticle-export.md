---
title: mParticle Export
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

The data export feature provides the capability to export your CleverTap event data to your mParticle dashboard. You can use this event data for further analysis.

# Setup
This process involves adding mParticle project details to the CleverTap dashboard. To add the project details to the CleverTap dashboard:
a. Log in to your CleverTap account.
b. Navigate to *Settings* > *Partners* > *Exports*. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5db8db6-mparticle_unconnected.png",
        "mparticle unconnected.png",
        1672,
        1028,
        "#e9eaf0"
      ],
      "border": true
    }
  ]
}
[/block]
c. Click the **mParticle** icon under the *Unconnected partners* section. The *mPaticle* page is displayed.
d. Enter the mParticle details.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/53c2195-Enter_details.png",
        "Enter details.png",
        1392,
        744,
        "#fbfcfd"
      ],
      "border": true
    }
  ]
}
[/block]
The project details can be obtained by selecting **** under ** of the mParticle dashboard.
[block:parameters]
{
  "data": {
    "h-0": "Field Description",
    "0-0": "mParticle API Key",
    "1-0": "mParticle API Secret",
    "2-1": "The Data Center is the physical/geographical storage location of a project's data and is at a project level (per project). Select from the following available options:\n* Default (@harsh: what would be the default center? I think we should mention it here)\n* Australia\n* Europe\n* USA",
    "2-0": "Data Center",
    "3-0": "Customer ID Mapping",
    "3-1": "This user property is used as an identifier when sending events data to mParticle."
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
        "https://files.readme.io/563f769-Save_credentials_successfully.png",
        "Save credentials successfully.png",
        1390,
        742,
        "#848587"
      ],
      "border": true
    }
  ]
}
[/block]
mParticle is now displayed under Connected partners when you navigate to  *Settings* > *Partners* > *Exports*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1204680-mParticle_connected.png",
        "mParticle connected.png",
        1394,
        782,
        "#f8f8f9"
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
        "https://files.readme.io/82460f3-2020-11-12_09-13-32_Data_Export.png",
        "2020-11-12_09-13-32_Data Export.png",
        1316,
        344,
        "#f9faf9"
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
        "https://files.readme.io/8fc1f80-Create_an_export.png",
        "Create an export.png",
        1384,
        1064,
        "#a7a8a9"
      ],
      "border": true
    }
  ]
}
[/block]
3. Configure the following settings:
    * Choose an export partner: Select *mParticle* from the *Choose an export partner* dropdown list.
    * Export details: Select from one of the following options:
       * All events: This exports data for all events that have been defined which include *System* and *Custom* events.
      * Selected events: This exports specific events you want to export. 
      * User properties: This exports all your user profile data.
    * Choose export frequency: Select from one of the following options
       * One time: Single export for the export type selected. You can export data up to the last 60 days. 
       * Recurring: Set up a recurring export that exports all the new events/user profiles captured in the last window. You can export as frequently as every 4 hours and up to once every 24 hours. 
4. Click **Create export**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ae5a876-Click_Create_Export.png",
        "Click Create Export.png",
        1382,
        1158,
        "#aaabac"
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
        "https://files.readme.io/fc81fda-Successful_export.png",
        "Successful export.png",
        1388,
        904,
        "#7d7e7f"
      ],
      "border": true
    }
  ]
}
[/block]
5. Click **Ok** to return to the *Exports* page. CleverTap processes the export, and you can now see the newly created export for mParticle.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ecad062-Export_created.png",
        "Export created.png",
        1388,
        966,
        "#f6f6f7"
      ],
      "border": true
    }
  ]
}
[/block]
For recurring exports, *Pending* status is displayed.

# Stop Export
You can also stop the export that you have created. To do so:

1. Click the ![ellipses](https://files.readme.io/0210143-ellipses_icon.png) icon for the export request you want to stop and then click ![stop](https://files.readme.io/930e98c-Stop_icon.png). 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/faf4270-Click_Stop.png",
        "Click Stop.png",
        1390,
        964,
        "#f6f6f8"
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
        "https://files.readme.io/941bc34-Confirm_Stop.png",
        "Confirm Stop.png",
        1382,
        956,
        "#7d7c7d"
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
        "https://files.readme.io/1060180-Stopped_successfully.png",
        "Stopped successfully.png",
        1392,
        956,
        "#7b7c7d"
      ],
      "border": true
    }
  ]
}
[/block]
3. Click **Ok** to return to the *Exports *page.

# Events Exported to mParticle

The following table provides information about the events exported to the mParticle dashboard:

[block:parameters]
{
  "data": {
    "h-0": "CleverTap Event Name",
    "h-1": "Event Description",
    "0-0": "App Installed",
    "1-0": "App Launched",
    "2-0": "App Uninstalled",
    "3-0": "UTM Visited",
    "4-0": "Notification Sent",
    "5-0": "Notification Viewed",
    "6-0": "Notification Clicked",
    "7-0": "Push Impressions",
    "11-0": "AB Experiment Rolled Out",
    "14-0": "Geocluster Entered",
    "15-0": "Geocluster Exited",
    "0-1": "This event is recorded when a user installs the application.",
    "1-1": "This event is recorded every time a user launches the application.",
    "2-1": "This event is recorded when a user uninstalls the application.",
    "3-1": "This event is tracked when the user clicks on a link from a marketing campaign that has a UTM parameter defined for it.",
    "4-1": "This event is tracked when a campaign message is sent to a user.",
    "5-1": "This event is tracked when a user views an email, in-app notification, or a web notification sent from CleverTap.",
    "6-1": "This event is tracked only when a user clicks on a marketing campaign sent via CleverTap.",
    "7-1": "This event is tracked when a Push notification sent from CleverTap is delivered on a user’s device.",
    "11-1": "This event is recorded when the AB experiment is sent to the user.",
    "14-1": "This event is recorded to mark when a device enters a geofence.",
    "15-1": "This event is recorded to mark when a device exits a geofence.",
    "8-0": "App Version Changed",
    "8-1": "This event is raised when a user upgrades to a new version of application.",
    "9-1": "This event is raised when a user replies to a campaign message. It is raised only for WhatsApp.",
    "9-0": "Notification Replied",
    "10-0": "AB Experiment Stopped",
    "10-1": "This event is raised when AB Experiment is stopped.",
    "12-0": "AB Experiment Disqualified",
    "12-1": "This event is raised when the user is disqualified from the experiment.",
    "13-0": "AB Experiment Rendered",
    "13-1": "This event is raised when the experiment is rendered at the user's end."
  },
  "cols": 2,
  "rows": 16
}
[/block]

[block:callout]
{
  "type": "info",
  "body": "This feature is available for both CleverTap for Enterprises and CleverTap for Startups plans.\nContact your sales account manager to have it activated for you.",
  "title": "Availability of Feature"
}
[/block]