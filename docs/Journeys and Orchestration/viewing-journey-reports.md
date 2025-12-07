---
title: Viewing Journey Reports
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
## Overview

You can view comprehensive reports for all Journeys. You can export these reports to analyze Journey performance with your metrics, compare performance across Journeys and understand engagement trends.

# Export Journey Reports

You can export a Journey report in a CSV file. When you choose to export a Journey report, it will be emailed to you on your registered email address. 

You can select the time period and the required Journeys from the Journeys list page. The Email report button is available on top right-hand side of the list page. 

> 📘 Note
> 
> You can email reports for up to 100 Journeys at a time from the dashboard.

<br />

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d70a4245bd5284616b17a3025c1eb83bc3a8ea30d6934848d5b44a4a90fa0ebd-Email_Journey_Report.png",
        null,
        "Email Journey Report"
      ],
      "align": "center",
      "border": true,
      "caption": "Email Journey Report"
    }
  ]
}
[/block]


<br />

| Steps | Description                                                                                   |
| :---- | :-------------------------------------------------------------------------------------------- |
| **1** | Select the date range for which you wish to view the Journeys.                                |
| **2** | Select the required Journeys from the Journeys list page.                                     |
| **3** | Click the **Email Report** icon. It emails you the Journey report to the registered email ID. |

## Schedule Journey Exports

You can choose to get daily or weekly reports for any Journeys with the _running_ status. You can choose the period and frequency from the reports section in Settings.  Go to _Settings_ > _Setup_ > _Reports_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/463b609-Journey-reports.jpg",
        "Schedule Journey reports",
        1000
      ],
      "align": "center",
      "border": true,
      "caption": "Schedule Journey Reports"
    }
  ]
}
[/block]


# Types of Journey Reports

There are two types of Journey Reports available:

1. Journey Summary Report
2. Journey Nodewise Report

## Journey Summary Report

This is a Journey level report. Each row in the report represents a Journey and contains information for the Journey and all the users in it.  

Journey Summary report column headers: 

### Journey Data

[block:parameters]
{
  "data": {
    "h-0": "Journey Data",
    "h-1": "Description",
    "0-0": "Journey Start Time",
    "0-1": "Time when the journey initiates. This is typically recorded in a standard time format (e.g., @Soumen: Need date time format).",
    "1-0": "Journey End time",
    "1-1": "Time when the journey ends. Similar to the start time, this is recorded in a standard time format. The format is (@Soumen: Need date time format.)",
    "2-0": "Journey Name",
    "2-1": "Name of the journey.",
    "3-0": "Journey ID",
    "3-1": "Unique identifier of the journey.",
    "4-0": "Journey Entry type",
    "4-1": "Method how users can enter the journey. The following are the journey entry types:  \n  \n<li>Past Behaviour</li><li>Live</li>  \n  \n<br />",
    "5-0": "Re-entry Allowed",
    "5-1": "Indicates whether user's re-entry into the journey is permitted after initial entry. The possible values are TRUE or FALSE.",
    "6-0": "Journey Status",
    "6-1": "Current status of the journey. The possible statuses include Stopped, Completed, Pause, Running, etc.",
    "7-0": "Journey Created by",
    "7-1": "Email ID of the user who created the journey.",
    "8-0": "Journey Labels\\*\\*",
    "8-1": "<li>Displays active labels only.</li><li>Displays multiple labels.</li>",
    "9-0": "Journey Number of nodes",
    "9-1": "Total number of nodes in a journey. <li>It includes entry nodes, segment nodes, engagement nodes, and IntelliNODE.</li> <li>It does not include phantom nodes, user profile updates, and force exits.</li>",
    "10-0": "Journey URL",
    "10-1": "URL of the CleverTap dashboard where the journey can be accessed."
  },
  "cols": 2,
  "rows": 11,
  "align": [
    "left",
    "left"
  ]
}
[/block]


### User Data

| User Data                          | Description                                                                                                                                                                 |
| :--------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Qualified                          | Total number of users who qualified for the journey.                                                                                                                        |
| Entered                            | Total number of users who entered the journey.                                                                                                                              |
| Goal Met                           | Total number of user who met the journey goal.                                                                                                                              |
| Goal 1 Name                        | Title of the first goal in the journey.                                                                                                                                     |
| Goal 1 Conversions                 | Number of users converted by achieving goal 1.                                                                                                                              |
| Goal 1 Control Group Conversions   | Number of control group users who achieved goal 1.                                                                                                                          |
| Goal 2 Name                        | Title of the second goal in the journey.                                                                                                                                    |
| Goal 2 Conversions                 | Number of users converted by achieving goal 2.                                                                                                                              |
| Goal 2 Control Group Conversions   | Number of control group users who achieved goal 2.                                                                                                                          |
| Goal 3 Name                        | Title of the third goal in the journey.                                                                                                                                     |
| Goal 3 Conversions                 | Number of users converted by achieving goal 3.                                                                                                                              |
| Goal 3 Control Group Conversions   | Number of control group users who achieved goal 3.                                                                                                                          |
| Journey Timeout                    | If a Journey timeout is set in the Journey builder (entry criteria), these are all the users who timed out.                                                                 |
| Force Exits                        | Number of users who force exited the journey via the Force Exit node.                                                                                                       |
| Completed                          | <li>Total number of users who have completed the journey by reaching the last node.  </li><li>If a user achieves the goal in the last node, it is marked as completed.</li> |
| Control Group (Total)              |                                                                                                                                                                             |
| System Control Group Conversions   |                                                                                                                                                                             |
| Campaign Control Group Conversions |                                                                                                                                                                             |
| Custom Control Group Conversions   |                                                                                                                                                                             |
| Custom Control Group Name          | Name of the custom control group.                                                                                                                                           |

## Journey Nodewise Report

This is a node level report. Each row in the report represents a node in a Journey. This report has multiple rows that represent multiple nodes in a Journey. 

> 📘 Note
> 
> If a Journey has multiple Campaign OS' and Variants, they will be represented in separate rows.

This data is available for Segment and Engage nodes. The report display Journey Overview data, Node Overview data, Node user data, and campaign data. A Journey Node report has the following column headers: 

### Journey Overview Data

[block:parameters]
{
  "data": {
    "h-0": "Journey Overview Data",
    "h-1": "Description",
    "0-0": "Journey Start Time",
    "0-1": "Time when the journey initiates. This is typically recorded in a standard time format (e.g., @Soumen: Need date time format). ",
    "1-0": "Journey End time",
    "1-1": "Time when the journey ends. Similar to the start time, this is recorded in a standard time format. The format is (@Soumen: Need date time format.)",
    "2-0": "Journey Name",
    "2-1": "Name of the journey. ",
    "3-0": "Journey ID",
    "3-1": "Unique identifier of the journey. For example, 5. ",
    "4-0": "Journey Entry type",
    "4-1": "The  method for users to enter the journey. This describes how users can enter the journey. The following are the journey entry types:  \n  \n<li>Past Behaviour</li><li>Live</li>  \n  \n<br />",
    "5-0": "Re-entry Allowed",
    "5-1": "Indicates whether user's re-entry into the journey is permitted after initial entry. The possible values are TRUE or FALSE. ",
    "6-0": "Journey Status",
    "6-1": "Current status of the journey. The possible statuses include Stopped, Completed, Pause, Running, etc.",
    "7-0": "Journey Created by",
    "7-1": "Email ID of the user who created the journey.",
    "8-0": "Journey Labels",
    "8-1": "Labels associated with the journey. These are used for categorization or filtering and can be multiple tags separated by commas or spaces.",
    "9-0": "Journey Number of Nodes",
    "9-1": "Total number of nodes in a journey: <li>It includes entry nodes, segment nodes, engagement nodes, and IntelliNODE.</li> <li>It does not include phantom nodes, user profile updates, and force exits.</li>",
    "10-0": "Journey URL",
    "10-1": "URL of the CleverTap dashboard where the journey can be accessed."
  },
  "cols": 2,
  "rows": 11,
  "align": [
    "left",
    "left"
  ]
}
[/block]


<br />

### Node Overview Data

[block:parameters]
{
  "data": {
    "h-0": "Node Overview Data",
    "h-1": "Description",
    "0-0": "Node Type",
    "0-1": "Type of journey node. The possible values are:  \n  \n<li>segment</li><li>message</li>  \n  \n<br />",
    "1-0": "Node ID",
    "1-1": "Unique identifier of the node. For example, 2. ",
    "2-0": "Previous Node\\*\\*",
    "2-1": "Indicates the presence of multiple preceding nodes. For example, 6. ",
    "3-0": "Delay before Node\\*\\*",
    "3-1": "Displays delay time before node:  \n  \n<li>For PBS: 0 mins 16:32. For Action: 5 mins</li> <li>\nBest time is shown like PBS: 0 mins 10:00</li> <li>\nMultiple cases are separated by \"|\". E.g., 10 mins | 10 mins | 10 mins</li>  \n  \n<br />",
    "4-0": "Connector from Previous\\*\\*",
    "4-1": "Connector path taken from the previous node. The possible values are: Yes, No, Sent, Updated, Failed, etc.",
    "5-0": "Qualifying window",
    "5-1": "The qualifying window in journeys refers to the time period during which users must meet certain criteria in order to move forward in the journey. It is set on the segment node by clicking on the hexagon. The qualifying window must be set in combination with the node timeout connector, as users will not move if the node timeout is not connected to another node. The qualifying window can be set based on specific time or event triggers.",
    "6-0": "Campaign Name / Segment Name",
    "6-1": "Name of the campaign or segment. ",
    "7-0": "Campaign ID / Segment ID\\*\\*",
    "7-1": "Displays both previous node single IDs and multi-target IDs.",
    "8-0": "Channel / Segment Type",
    "8-1": "Type of channel or segment. For example, Push, PBS, SMS, etc. ",
    "9-0": "Campaign URL",
    "9-1": "URL of the CleverTap dashboard where the campaign can be accessed.",
    "10-0": "Template Name",
    "10-1": "Name of the campaign template.",
    "11-0": "Provider Name",
    "11-1": "Name of the Email or SMS service provider. For example, SendGrid.",
    "12-0": "WABA number",
    "12-1": "A WABA number refers to a WhatsApp Business Account number. It is a dedicated WhatsApp number that is used for business purposes. Each CleverTap project must have a distinct WABA number. The WABA number is registered and connected with CleverTap BSP (Business Solution Provider) to enable integration with WhatsApp. The WABA number is used to send and receive messages with customers on WhatsApp."
  },
  "cols": 2,
  "rows": 13,
  "align": [
    "left",
    "left"
  ]
}
[/block]


<br />

### Node User Data

| Node User Data                 | Description                                                                                                                                                                 |
| :----------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Moved Forward                  | Total number of users who moved forward via node connectors, such as Yes, No, or Node Timeout.                                                                              |
| Moved Forward via Yes          | Number of users who moved forward via Yes path.                                                                                                                             |
| Moved Forward via No           | Number of users who moved forward via the No path.                                                                                                                          |
| Moved Forward via Node Timeout | Number of users who moved forward via the Node Timeout path.                                                                                                                |
| Journey Timeout                | If a Journey timeout is set in the Journey builder (entry criteria), these are all the users who timed out.                                                                 |
| Completed                      | <li>Total number of users who have completed the journey by reaching the last node.  </li><li>If a user achieves the goal in the last node, it is marked as completed.</li> |
| Goal Met                       | Total number of user who met the journey goal.                                                                                                                              |
| Goal 1 Name                    | Title of the first goal in the journey.                                                                                                                                     |
| Goal 1 Conversions             | Number of users who have been converted by achieving goal 1.                                                                                                                |
| Goal 2 Name                    | Title of the second goal in the journey.                                                                                                                                    |
| Goal 2 Conversions             | Number of users who have been converted by achieving goal 2.                                                                                                                |
| Goal 3 Name                    | Title of the third goal in the journey.                                                                                                                                     |
| Goal 3 Conversions             | Number of users who have been converted by achieving goal 3.                                                                                                                |

### Campaign Data

| Campaign Data                           | Description                                                                   |
| :-------------------------------------- | :---------------------------------------------------------------------------- |
| Campaign Type                           | Type of campaign. For example, Single message.                                |
| Campaign Variant                        |                                                                               |
| Campaign OS                             | Target Operating Systems (OS) for the campaign. For example, Android and iOS. |
| Global Campaign Limits Applied          |                                                                               |
| Campaign Title                          | Name of the campaign.                                                         |
| Total Sent                              |                                                                               |
| Total Viewed                            |                                                                               |
| Total Clicked                           |                                                                               |
| Errors                                  | Dispalys total number of errors including Unreachable error.                  |
| Conversion Event                        |                                                                               |
| Conversion Time (in minutes)            |                                                                               |
| Unique Sent within Conversion Time      |                                                                               |
| Unique Viewed within Conversion Time    |                                                                               |
| Unique Clicked within Conversion Time   |                                                                               |
| Unique Converted within Conversion Time |                                                                               |
| Influenced Conversions                  |                                                                               |
| Influenced Revenue                      |                                                                               |
| Amplified By Push                       |                                                                               |
| Deep link URL                           |                                                                               |

> 📘 Column Headers
> 
> Column headers with `**` can have multiple values separated by `|`

### Conversion Stats for WhatsApp Nodes

CleverTap BSP allows tracking clicks on the WhatsApp message. The stats for these clicks are available under the Campaigns > Stats page. If Click Tracking is enabled, the Journey Report will display the node stats for the _sent > delivered > viewed > clicked > converted_ funnel. However, if Click Tracking is not enabled, only the viewed data is reported for your campaign. Therefore, the funnel in this case is, _sent> delivered > viewed > converted_ . 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b139aea-sent_delivered_funnel.jpg",
        "",
        "Click Tracking Funnel"
      ],
      "align": "center",
      "border": true,
      "caption": "Click Tracking Funnel"
    }
  ]
}
[/block]


| Campaign/Journey Data                   | Click Tracking Enabled                          | Click Tracking Disabled               |
| :-------------------------------------- | :---------------------------------------------- | :------------------------------------ |
| Unique Sent within Conversion Time      | sent > delivered > viewed > clicked > converted | sent > delivered > viewed >converted  |
| Unique Viewed within Conversion Time    | sent > delivered > viewed > clicked > converted | sent > delivered > viewed > converted |
| Unique Clicked within Conversion Time   | sent > delivered > viewed >clicked > converted  | sent > delivered > viewed > converted |
| Unique Converted within Conversion Time | sent > delivered > viewed >clicked > converted  | 0.                                    |