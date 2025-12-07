---
title: Amplitude Export_PE_2
excerpt: Analytics Partner
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

[Amplitude](https://amplitude.com/), analytics and business intelligence platform, helps make informed decisions for targeting users. Integration CleverTap with Amplitude allows you to export your CleverTap event data to your Amplitude dashboard. You can use this event data for further analysis.

# Integrate Amplitude with CleverTap

This process involves the following two steps:

1. [Find Amplitude Project Details](doc:amplitude-export#find-amplitude-project-details)
2. [Configure CleverTap Dashboard](doc:amplitude-export#configure-clevertap-dashboard)

## Find Amplitude Project Details

1. Log in to your Amplitude account.
2. Navigate to the _Settings_ page. 
3. Navigate to _Org Settings_ > _Projects_. 
4. Click on a project to find the _API Key_ under the _General_ tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/75bc618-Finding_API_key.png",
        "Finding API key.png",
        3552
      ],
      "border": true
    }
  ]
}
[/block]

## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Navigate to _Settings_ > _Partners_ from the CleverTap dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f4c2b91-Navigating_to_Partners_page.png",
        "Navigating to Partners page.png",
        2700
      ],
      "border": true
    }
  ]
}
[/block]

2. Hover on the _Amplitude_ icon and click **Integrate**. The _Integrate analytics partner - Amplitude_ popup opens on the right side of the screen.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0128cc7-Click_Integrate.png",
        "Click Integrate.png",
        2214
      ],
      "border": true
    }
  ]
}
[/block]

3. Enter the following details and click **Integrate**:

| <p>Field</p>            | <p>Description</p>                                                                                                                                                                                                  |
| :---------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <p>Partner Nickname</p> | <p>Enter the <em>Nickname</em> for your integration.</p>                                                                                                                                                            |
| <p>API key</p>          | <p>The unique code for Amplitude to verify your credentials. For more information about obtaining the key, refer to <a href="doc:amplitude-export#find-amplitude-project-details">Find Amplitude Details</a>.</p>   |
| <p>Data Residency</p>   | <p>The Data Residency is the physical/geographical storage location of data for each project. </p><ul><li>Select from the following available options:<ul><li>Europe (default)</li><li>Standard</li></ul></li></ul> |
| Device ID Mapping       | This field is mapped to Amplitude's `device_id` field for identification when sending data from CleverTap to Amplitude.                                                                                             |
| User ID Mapping         | This field is mapped to Amplitude's `user_id` field for identification when sending data from CleverTap to Amplitude.                                                                                               |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6a45898-Enter_details.png",
        "Enter details.png",
        2224
      ],
      "border": true
    }
  ]
}
[/block]

After successful integration, the _Integrated_ tag displays against _Amplitude_ on the _Partner List_ page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2db790d-Integrated_tag.png",
        "Integrated tag.png",
        2224
      ],
      "border": true
    }
  ]
}
[/block]

# Create New Export

This section lists steps to create a new export from the CleverTap dashboard. To do so:

1. Navigate to _Settings_ > _Partners_ > _Exports_ from the CleverTap dashboard.
2. Click **+ Export** and select _Amplitude_ from the _Partners_ dropdown.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/414614a-Create_Export.png",
        "Create Export.png",
        2222
      ],
      "sizing": "smart",
      "border": true
    }
  ]
}
[/block]

The _Export to Amplitude_ window displays on the right side of the screen.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ef30939-Export_to_amplitude.png",
        "Export to amplitude.png",
        2228
      ],
      "border": true
    }
  ]
}
[/block]

3. Configure the following settings:
   - **Type**: Select the events to export from the available options. For more information, refer to [Export Details](doc:amplitude-export#export-details).
   - **Frequency**: Select from one of the following options:
     - _Once only_: A single export for the selected export type. You can export data up to the last 60 days. You create an export for a specific day, date range, previous month, current month, and more.  
     - _Recurring_: Set up a recurring export that exports all the new events/user profiles captured in the last window. You can export as frequently as every 4 hours and up to once every 24 hours. 
4. Click **Export**. The _Export to Amplitude_ window closes, and the following message displays at the top of _Exports_ page:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/de71059-Export_initiated.png",
        "Export initiated.png",
        2150
      ],
      "border": true
    }
  ]
}
[/block]

   CleverTap processes the export, and you can now see the newly created export for Amplitude.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ce2d7dd-Exports_page.png",
        "Exports page.png",
        2216
      ],
      "border": true
    }
  ]
}
[/block]

The status for each export is displayed as _Pending_ as soon as the export is created. The status changes to _Running_ after the processing starts. In the case of _Once only_ export, the status changes to _Done_ when the export is complete.

# Stop Export

You can also stop the export that you have created. To do so, click the ![Stop export](https://files.readme.io/437ad4c-Stop_export_icon.png) icon for the export request you want to stop and then click **Stop** to confirm your action.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/48b5bdc-Stop_Export.png",
        "Stop Export.png",
        2216
      ],
      "border": true
    }
  ]
}
[/block]

You now return to the _Exports_ page, and the _Amplitude data export stopped_ message displays at the top. The status of the export is displayed as _Stopped_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/18b6435-Export_Stopped.png",
        "Export Stopped.png",
        2216
      ],
      "border": true
    }
  ]
}
[/block]

# Export Details

Select from one of the following options to export events from CleverTap to the Amplitude dashboard:

- [All events](doc:amplitude-export-pe-2#all-events)
- [Selected events](doc:amplitude-export-pe-2#selected-events)
- [Engagement events](doc:amplitude-export-pe-2#engagement-events)

## All events

Export data for all defined events, including System and Custom events.

## Selected events

Select the specific events you want to export from CleverTap to the Amplitude dashboard.

## Engagement Events

Select this option to export the following engagement events:

| <p>CleverTap Event Name</p> | <p>Event Description</p>                                                                                                                                                                                                                                                                                                                                          |
| :-------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Notification Sent</p>    | <p>The event is tracked when the notification is successfully sent from CleverTap to the communication channel you select for your campaign.</p>                                                                                                                                                                                                                  |
| <p>Notification Viewed</p>  | <p>This event is tracked when a user views an email, in-app notification, or a web notification sent from CleverTap.</p>                                                                                                                                                                                                                                          |
| <p>Notification Clicked</p> | <p>This event is tracked only when a user clicks on a notification sent via CleverTap. It is recorded when a user clicks on a mobile push, in-app, email, web popup, or web push message sent via the CleverTap dashboard or through the campaign API.</p>                                                                                                        |
| <p>Push Impressions</p>     | <p>This event is tracked when a Push notification sent from CleverTap is delivered on a user’s device.</p>                                                                                                                                                                                                                                                        |
| <p>Notification Replied</p> | <p>This event is tracked when a user replies to a WhatsApp message.</p>                                                                                                                                                                                                                                                                                           |
| <p>Push Unregistered</p>    | <p>The event is raised when the user unregisters to receive Push Notifications.</p>                                                                                                                                                                                                                                                                               |
| <p>Control Group</p>        | <p>The event is raised when a campaign is activated with a Control group.</p>                                                                                                                                                                                                                                                                                     |
| <p>Channel Unsubscribed</p> | <p>The event is raised when a user unsubscribes to receive further communication through a channel.</p>                                                                                                                                                                                                                                                           |
| <p>Reachable By</p>         | <ul><li>The debug event raised when the user becomes reachable by a communication channel such as SMS, email, mobile push, or when there are changes to the existing communication channel.</li><li>Tracked for a profile when:<ul><li>Push token is added/changed.</li><li>Email ID is added/changed.</li><li>Phone number is added/changed.</li></ul></li></ul> |
| Push Impressions            | This event is tracked when a push notification sent from CleverTap is delivered on a user’s device. The funnels on the Push campaign statistics page reflect the count for this event.                                                                                                                                                                            |
| Notification Delivered      | This event is recorded when communication is delivered to the user's device                                                                                                                                                                                                                                                                                       |
| AB Experiment Rendered      | This event is recorded when communication is delivered to the user who is part of an A/B experiment campaign                                                                                                                                                                                                                                                      |
| AB Experiment Stopped       | This event is recorded when AB experiment is stopped.                                                                                                                                                                                                                                                                                                             |
| AB Experiment Rolled Out    | This event is recorded when AB experiment is started                                                                                                                                                                                                                                                                                                              |
| Geocluster Entered          | This event is recorded to mark when a device enters a geofence.                                                                                                                                                                                                                                                                                                   |
| Geocluster Exited           | This event is recorded to mark when a device exits a geofence.                                                                                                                                                                                                                                                                                                    |
| Reply Sent                  | This event is recorded when an agent (CleverTap user) replies to a message from the end-user.                                                                                                                                                                                                                                                                     |
| App Uninstalled             | This event is recorded when a user uninstalls your application.                                                                                                                                                                                                                                                                                                   |
| Webhook Delivered           | This event is recorded when a Webhook campaign is delivered successfully                                                                                                                                                                                                                                                                                          |
| State Transitioned          | This event is recorded for Lifecycle Optimizer when a user transitions from one stage to another.                                                                                                                                                                                                                                                                 |
| UTM Visited                 | This event is tracked when a user clicks on a link from a marketing campaign that has a UTM parameter defined on it.                                                                                                                                                                                                                                              |

> 📘 Availability of Feature
> 
> This feature is available for the _CleverTap for Enterprise_ plan. Contact your sales account manager to activate it.