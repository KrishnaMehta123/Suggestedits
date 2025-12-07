---
title: mParticle Export_PE_2
excerpt: Customer Data Platform
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
[mParticle](https://www.mparticle.com/) is a customer data platform that manages data quality and drives better customer interactions. Integrating CleverTap with mParticle allows you to export your CleverTap event data to your mParticle dashboard. You can use this event data for further analysis.

# Integrate mParticle with CleverTap
This process involves the following two steps:
1. [Find mParticle Project Details](doc:mparticle-export#find-mparticle-project-details).
2. [Configure CleverTap Dashboard](doc:mparticle-export#configure-clevertap-dashboard).

## Find mParticle Project Details
To find your project details:
1. Log in to your mParticle account.
2. Navigate to *Setup* > *Inputs* > *Feeds*.
3. Click **Add Feed Input** and select *CleverTap* from the dropdown list. The *Input: Feed Configuration* popup opens.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d09bae1-Add_Feed_Input.png",
        "Add Feed Input.png",
        2862,
        1360,
        "#dddede"
      ]
    }
  ]
}
[/block]
4. Enter the *Configuration Name* and turn **ON** the *Feed Status* toggle. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1a0fc12-Feed_Config_popup.png",
        "Feed Config popup.png",
        2818,
        1352,
        "#7e818e"
      ],
      "border": true
    }
  ]
}
[/block]

5. Click **Save**. The *Server to Server Key* and *Server to Server Secret* are displayed.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/af1581a-Key_and_Secret_Details.png",
        "Key and Secret Details.png",
        2806,
        1350,
        "#888d98"
      ],
      "border": true
    }
  ]
}
[/block]
5. Copy the project details. You will need them when configuring the CleverTap dashboard.

## Configure CleverTap Dashboard
To configure the CleverTap dashboard:
1. Log in to your CleverTap account and navigate to the *Settings* > *Partners* page. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a5fc4fa-Navigating_to_Partners_page.png",
        "Navigating to Partners page.png",
        2700,
        1745,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]
2. Hover on the *mParticle* icon and click **Integrate**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c4a1f62-Click_Integrate.png",
        "Click Integrate.png",
        2376,
        1138,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]
   On clicking, *Integrate raw data partner - mParticle* popup opens on the right side of the screen.
3. Enter the following details and click **Integrate**. 
[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "0-0": "Partner Nickname",
    "1-0": "API key and API secret",
    "0-1": "Enter the *Nickname* for your integration.",
    "1-1": "These are the unique codes passed to mParticle to verify your credentials. For more information about obtaining the key, refer to [Find mParticle Project Details](doc:mparticle-export#find-mparticle-project-details).",
    "2-0": "Customer ID Mapping",
    "2-1": "This is used as an identifier when sending event data to mParticle."
  },
  "cols": 2,
  "rows": 3
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fad6773-Integrate_raw_data_partner.png",
        "Integrate raw data partner.png",
        2362,
        1284,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]
   After successful integration, the *Integrated* tag displays against *mParticle* on the *Partner List* page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f38ed77-Integrated_tag.png",
        "Integrated tag.png",
        2390,
        1138,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]
# Create New Export
To create a new export:
1. Navigate to *Settings* > *Partners* > *Exports* from the CleverTap dashboard.
2. Click **+ Export** and select *mParticle* from the *Partners* list.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f03c9d4-Create_Export.png",
        "Create Export.png",
        2376,
        1192,
        "#000000"
      ],
      "border": true,
      "sizing": "smart"
    }
  ]
}
[/block]
On clicking, the *Export to mParticle* pop-up displays on the right side of the screen.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2e61e9a-Export_to_mParticle.png",
        "Export to mParticle.png",
        2376,
        1288,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]
3. Configure the following settings:
    * **Type**: Select the type of data that you want to export from the available options. For more information, refer to [Export Details](doc:mparticle-export#export-details).
    * **Frequency**: Select from one of the following options:
        * *Once only*: A single export for the selected export type. You can export data up to the last 60 days. You create an export for a specific day, date range, previous month, current month, and more.  
       * *Recurring*: Set up a recurring frequency to export all the new events/user properties captured in the last window. You can export event data as frequently as every 4 hours and up to once every 24 hours. You can export user properties only once every 24 hours. 
4. Click **Export**. The popup closes, and the following message displays at the top of the *Exports* page:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1acfbc0-Export_initiated.png",
        "Export initiated.png",
        2284,
        1158,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]
CleverTap processes the export, and you can now see the newly-created export for mParticle.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1b9a88e-Exports_page.png",
        "Exports page.png",
        2372,
        1178,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]
The status for each export is displayed as *Pending* as soon as the export is created. The status changes to *Running* after the processing starts. And, it changes to *Done* when the export is complete.

# Stop Export
You can also stop the export that you have created. To do so, click the ![Stop export](https://files.readme.io/437ad4c-Stop_export_icon.png) icon for the export request you want to stop and then click **Stop** to confirm your action.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7c7af00-Stop_Export.png",
        "Stop Export.png",
        2372,
        1178,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]
You are navigated back to the *Exports* page, and the *mParticle data export stopped* message displays at the top. The status for the data export now displays as *Stopped*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8d483ed-Export_Stopped.png",
        "Export Stopped.png",
        2340,
        1160,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]

# Export Details
Select from one of the following options to export events from CleverTap to the mParticle dashboard:
* [All events](doc:mparticle-export-pe-2#all-events)
* [Selected events](doc:mparticle-export-pe-2#selected-events)
* [Engagement events](doc:mparticle-export-pe-2#engagement-events)
* [User properties](doc:mparticle-export-pe-2#user-properties)

## All Events
When you select this option, the following defined system events are exported:
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
    "5-0": "Control Group",
    "6-0": "Channel Unsubscribed",
    "7-0": "Push Impressions",
    "8-0": "AB Experiment Stopped",
    "9-0": "AB Experiment Rolled Out",
    "11-0": "Geocluster Entered",
    "12-0": "Geocluster Exited",
    "13-0": "Reply Sent",
    "15-0": "App Launched",
    "18-0": "UTM Visited",
    "0-1": "The event is tracked when the notification is successfully sent from CleverTap to the communication channel you select for your campaign.",
    "1-1": "This event is tracked when a user views an email, in-app notification, or a web notification sent from CleverTap.",
    "2-1": "This event is tracked only when a user clicks on a notification sent via CleverTap.Recorded when a user clicks on a mobile push, in-app, email, web-popup, or web push message sent via the CleverTap dashboard or through the campaign API.",
    "3-1": "This event is tracked when a Push notification sent from CleverTap is delivered on a user’s device.",
    "4-1": "This event is recorded when a user replies to a WhatsApp message.",
    "5-1": "The event raised when a campaign is activated with a Control group.",
    "6-1": "The event raised when a user Unsubscribes to receive further communication through a channel",
    "7-1": "This event is tracked when a push notification sent from CleverTap is delivered on a user’s device. The funnels on the Push campaign statistics page reflect the count for this event.",
    "8-1": "This event is recorded when AB experiment is stopped.",
    "9-1": "This event is recorded when AB experiment is started",
    "11-1": "This event is recorded to mark when a device enters a geofence.",
    "12-1": "This event is recorded to mark when a device exits a geofence.",
    "13-1": "This event is recorded when an agent (CleverTap user) replies to a message from the end-user.",
    "15-1": "This event is recorded every time a user launches your application.",
    "18-1": "This event is tracked when a user clicks on a link from a marketing campaign that has a UTM parameter defined on it.",
    "17-0": "App Uninstalled",
    "17-1": "This event is recorded when a user uninstalls your application.",
    "16-0": "App Installed",
    "10-0": "AB Experiment Disqualified",
    "14-0": "App Version Changed",
    "16-1": "The event is raised when the user launches the app for the first time.",
    "14-1": "This event is raised when a user’s current app version is different from the user’s previous app version.",
    "10-1": "This event is raised when the device is disqualified."
  },
  "cols": 2,
  "rows": 19
}
[/block]
For more information about these events, refer to [Events](doc:events).

## Selected Events
With this option, you can select the specific system events (from those listed in the above table) that you want to export from CleverTap to the mParticle dashboard.

## Engagement Events
When you select this option, the following engagement events are exported:
  * Notification Sent
  * Notification Viewed
  * Notification Clicked
  * Push Impressions
  * Notification Replied
  * Control Group
  * Channel Unsubscribed
  * Push Impressions
  * Notification Delivered
  * AB Experiment Rendered
  * AB Experiment Stopped
  * AB Experiment Rolled Out
  * Geocluster Entered
  * Geocluster Exited
  * Reply Sent
  * App Uninstalled
  * Webhook Delivered
  * State Transitioned
  * UTM Visited

For more information about these events, refer to [Events](doc:events).

## User Properties
When you select this option, the following user profile attributes are exported:
[block:parameters]
{
  "data": {
    "0-0": "Name",
    "1-0": "Gender",
    "2-0": "DOB",
    "3-0": "All communication preference",
    "h-0": "Field",
    "h-1": "Description",
    "0-1": "Indicates the name of the user.",
    "1-1": "Indicates the gender of the user.",
    "2-1": "Indicates the date of the birth of the user.",
    "3-1": "Flags that determine the communication preference of the user."
  },
  "cols": 2,
  "rows": 4
}
[/block]

[block:callout]
{
  "type": "info",
  "body": "If you are a CleverTap for Enterprises user, contact your sales account manager to activate this feature at your end. In the case of CleverTap for Startups, it is available as a paid add-on.",
  "title": "Availability of Feature"
}
[/block]