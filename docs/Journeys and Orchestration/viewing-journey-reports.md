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

<Image alt="Email Journey Report" align="center" border={true} src="https://files.readme.io/d70a4245bd5284616b17a3025c1eb83bc3a8ea30d6934848d5b44a4a90fa0ebd-Email_Journey_Report.png">
  Email Journey Report
</Image>

<br />

| Steps | Description                                                                                   |
| :---- | :-------------------------------------------------------------------------------------------- |
| **1** | Select the date range for which you wish to view the Journeys.                                |
| **2** | Select the required Journeys from the Journeys list page.                                     |
| **3** | Click the **Email Report** icon. It emails you the Journey report to the registered email ID. |

## Schedule Journey Exports

You can choose to get daily or weekly reports for any Journeys with the *running* status. You can choose the period and frequency from the reports section in Settings.  Go to *Settings* > *Setup* > *Reports*.

<Image title="Schedule Journey reports" alt={1000} align="center" border={true} src="https://files.readme.io/463b609-Journey-reports.jpg">
  Schedule Journey Reports
</Image>

# Types of Journey Reports

There are two types of Journey Reports available:

1. Journey Summary Report
2. Journey Nodewise Report

## Journey Summary Report

This is a Journey level report. Each row in the report represents a Journey and contains information for the Journey and all the users in it.  

Journey Summary report column headers: 

### Journey Data

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Journey Data
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Journey Start Time
      </td>

      <td>
        Time when the journey initiates. This is typically recorded in a standard time format (e.g., @Soumen: Need date time format).
      </td>
    </tr>

    <tr>
      <td>
        Journey End time
      </td>

      <td>
        Time when the journey ends. Similar to the start time, this is recorded in a standard time format. The format is (@Soumen: Need date time format.)
      </td>
    </tr>

    <tr>
      <td>
        Journey Name
      </td>

      <td>
        Name of the journey.
      </td>
    </tr>

    <tr>
      <td>
        Journey ID
      </td>

      <td>
        Unique identifier of the journey.
      </td>
    </tr>

    <tr>
      <td>
        Journey Entry type
      </td>

      <td>
        Method how users can enter the journey. The following are the journey entry types:  

        <li>Past Behaviour</li><li>Live</li>  
          
        <br />
      </td>
    </tr>

    <tr>
      <td>
        Re-entry Allowed
      </td>

      <td>
        Indicates whether user's re-entry into the journey is permitted after initial entry. The possible values are TRUE or FALSE.
      </td>
    </tr>

    <tr>
      <td>
        Journey Status
      </td>

      <td>
        Current status of the journey. The possible statuses include Stopped, Completed, Pause, Running, etc.
      </td>
    </tr>

    <tr>
      <td>
        Journey Created by
      </td>

      <td>
        Email ID of the user who created the journey.
      </td>
    </tr>

    <tr>
      <td>
        Journey Labels\*\*
      </td>

      <td>
        <li>Displays active labels only.</li><li>Displays multiple labels.</li>
      </td>
    </tr>

    <tr>
      <td>
        Journey Number of nodes
      </td>

      <td>
        Total number of nodes in a journey. <li>It includes entry nodes, segment nodes, engagement nodes, and IntelliNODE.</li> <li>It does not include phantom nodes, user profile updates, and force exits.</li>
      </td>
    </tr>

    <tr>
      <td>
        Journey URL
      </td>

      <td>
        URL of the CleverTap dashboard where the journey can be accessed.
      </td>
    </tr>
  </tbody>
</Table>

### User Data

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        User Data
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Qualified
      </td>

      <td>
        Total number of users who qualified for the journey.
      </td>
    </tr>

    <tr>
      <td>
        Entered
      </td>

      <td>
        Total number of users who entered the journey.
      </td>
    </tr>

    <tr>
      <td>
        Goal Met
      </td>

      <td>
        Total number of user who met the journey goal.
      </td>
    </tr>

    <tr>
      <td>
        Goal 1 Name
      </td>

      <td>
        Title of the first goal in the journey.
      </td>
    </tr>

    <tr>
      <td>
        Goal 1 Conversions
      </td>

      <td>
        Number of users converted by achieving goal 1.
      </td>
    </tr>

    <tr>
      <td>
        Goal 1 Control Group Conversions
      </td>

      <td>
        Number of control group users who achieved goal 1.
      </td>
    </tr>

    <tr>
      <td>
        Goal 2 Name
      </td>

      <td>
        Title of the second goal in the journey.
      </td>
    </tr>

    <tr>
      <td>
        Goal 2 Conversions
      </td>

      <td>
        Number of users converted by achieving goal 2.
      </td>
    </tr>

    <tr>
      <td>
        Goal 2 Control Group Conversions
      </td>

      <td>
        Number of control group users who achieved goal 2.
      </td>
    </tr>

    <tr>
      <td>
        Goal 3 Name
      </td>

      <td>
        Title of the third goal in the journey.
      </td>
    </tr>

    <tr>
      <td>
        Goal 3 Conversions
      </td>

      <td>
        Number of users converted by achieving goal 3.
      </td>
    </tr>

    <tr>
      <td>
        Goal 3 Control Group Conversions
      </td>

      <td>
        Number of control group users who achieved goal 3.
      </td>
    </tr>

    <tr>
      <td>
        Journey Timeout
      </td>

      <td>
        If a Journey timeout is set in the Journey builder (entry criteria), these are all the users who timed out.
      </td>
    </tr>

    <tr>
      <td>
        Force Exits
      </td>

      <td>
        Number of users who force exited the journey via the Force Exit node.
      </td>
    </tr>

    <tr>
      <td>
        Completed
      </td>

      <td>
        <li>Total number of users who have completed the journey by reaching the last node.  </li><li>If a user achieves the goal in the last node, it is marked as completed.</li>
      </td>
    </tr>

    <tr>
      <td>
        Control Group (Total)
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        System Control Group Conversions
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Campaign Control Group Conversions
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Custom Control Group Conversions
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Custom Control Group Name
      </td>

      <td>
        Name of the custom control group.
      </td>
    </tr>
  </tbody>
</Table>

## Journey Nodewise Report

This is a node level report. Each row in the report represents a node in a Journey. This report has multiple rows that represent multiple nodes in a Journey. 

> 📘 Note
>
> If a Journey has multiple Campaign OS' and Variants, they will be represented in separate rows.

This data is available for Segment and Engage nodes. The report display Journey Overview data, Node Overview data, Node user data, and campaign data. A Journey Node report has the following column headers: 

### Journey Overview Data

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Journey Overview Data
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Journey Start Time
      </td>

      <td>
        Time when the journey initiates. This is typically recorded in a standard time format (e.g., @Soumen: Need date time format). 
      </td>
    </tr>

    <tr>
      <td>
        Journey End time
      </td>

      <td>
        Time when the journey ends. Similar to the start time, this is recorded in a standard time format. The format is (@Soumen: Need date time format.)
      </td>
    </tr>

    <tr>
      <td>
        Journey Name
      </td>

      <td>
        Name of the journey. 
      </td>
    </tr>

    <tr>
      <td>
        Journey ID
      </td>

      <td>
        Unique identifier of the journey. For example, 5. 
      </td>
    </tr>

    <tr>
      <td>
        Journey Entry type
      </td>

      <td>
        The  method for users to enter the journey. This describes how users can enter the journey. The following are the journey entry types:  

        <li>Past Behaviour</li><li>Live</li>  
          
        <br />
      </td>
    </tr>

    <tr>
      <td>
        Re-entry Allowed
      </td>

      <td>
        Indicates whether user's re-entry into the journey is permitted after initial entry. The possible values are TRUE or FALSE. 
      </td>
    </tr>

    <tr>
      <td>
        Journey Status
      </td>

      <td>
        Current status of the journey. The possible statuses include Stopped, Completed, Pause, Running, etc.
      </td>
    </tr>

    <tr>
      <td>
        Journey Created by
      </td>

      <td>
        Email ID of the user who created the journey.
      </td>
    </tr>

    <tr>
      <td>
        Journey Labels
      </td>

      <td>
        Labels associated with the journey. These are used for categorization or filtering and can be multiple tags separated by commas or spaces.
      </td>
    </tr>

    <tr>
      <td>
        Journey Number of Nodes
      </td>

      <td>
        Total number of nodes in a journey: <li>It includes entry nodes, segment nodes, engagement nodes, and IntelliNODE.</li> <li>It does not include phantom nodes, user profile updates, and force exits.</li>
      </td>
    </tr>

    <tr>
      <td>
        Journey URL
      </td>

      <td>
        URL of the CleverTap dashboard where the journey can be accessed.
      </td>
    </tr>
  </tbody>
</Table>

<br />

### Node Overview Data

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Node Overview Data
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Node Type
      </td>

      <td>
        Type of journey node. The possible values are:  

        <li>segment</li><li>message</li>  
          
        <br />
      </td>
    </tr>

    <tr>
      <td>
        Node ID
      </td>

      <td>
        Unique identifier of the node. For example, 2. 
      </td>
    </tr>

    <tr>
      <td>
        Previous Node\*\*
      </td>

      <td>
        Indicates the presence of multiple preceding nodes. For example, 6. 
      </td>
    </tr>

    <tr>
      <td>
        Delay before Node\*\*
      </td>

      <td>
        Displays delay time before node:  

        <li>For PBS: 0 mins 16:32. For Action: 5 mins</li> <li>
        Best time is shown like PBS: 0 mins 10:00</li> <li>
        Multiple cases are separated by "|". E.g., 10 mins | 10 mins | 10 mins</li>  
          
        <br />
      </td>
    </tr>

    <tr>
      <td>
        Connector from Previous\*\*
      </td>

      <td>
        Connector path taken from the previous node. The possible values are: Yes, No, Sent, Updated, Failed, etc.
      </td>
    </tr>

    <tr>
      <td>
        Qualifying window
      </td>

      <td>
        The qualifying window in journeys refers to the time period during which users must meet certain criteria in order to move forward in the journey. It is set on the segment node by clicking on the hexagon. The qualifying window must be set in combination with the node timeout connector, as users will not move if the node timeout is not connected to another node. The qualifying window can be set based on specific time or event triggers.
      </td>
    </tr>

    <tr>
      <td>
        Campaign Name / Segment Name
      </td>

      <td>
        Name of the campaign or segment. 
      </td>
    </tr>

    <tr>
      <td>
        Campaign ID / Segment ID\*\*
      </td>

      <td>
        Displays both previous node single IDs and multi-target IDs.
      </td>
    </tr>

    <tr>
      <td>
        Channel / Segment Type
      </td>

      <td>
        Type of channel or segment. For example, Push, PBS, SMS, etc. 
      </td>
    </tr>

    <tr>
      <td>
        Campaign URL
      </td>

      <td>
        URL of the CleverTap dashboard where the campaign can be accessed.
      </td>
    </tr>

    <tr>
      <td>
        Template Name
      </td>

      <td>
        Name of the campaign template.
      </td>
    </tr>

    <tr>
      <td>
        Provider Name
      </td>

      <td>
        Name of the Email or SMS service provider. For example, SendGrid.
      </td>
    </tr>

    <tr>
      <td>
        WABA number
      </td>

      <td>
        A WABA number refers to a WhatsApp Business Account number. It is a dedicated WhatsApp number that is used for business purposes. Each CleverTap project must have a distinct WABA number. The WABA number is registered and connected with CleverTap BSP (Business Solution Provider) to enable integration with WhatsApp. The WABA number is used to send and receive messages with customers on WhatsApp.
      </td>
    </tr>
  </tbody>
</Table>

<br />

### Node User Data

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Node User Data
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Moved Forward
      </td>

      <td>
        Total number of users who moved forward via node connectors, such as Yes, No, or Node Timeout.
      </td>
    </tr>

    <tr>
      <td>
        Moved Forward via Yes
      </td>

      <td>
        Number of users who moved forward via Yes path.
      </td>
    </tr>

    <tr>
      <td>
        Moved Forward via No
      </td>

      <td>
        Number of users who moved forward via the No path.
      </td>
    </tr>

    <tr>
      <td>
        Moved Forward via Node Timeout
      </td>

      <td>
        Number of users who moved forward via the Node Timeout path.
      </td>
    </tr>

    <tr>
      <td>
        Journey Timeout
      </td>

      <td>
        If a Journey timeout is set in the Journey builder (entry criteria), these are all the users who timed out.
      </td>
    </tr>

    <tr>
      <td>
        Completed
      </td>

      <td>
        <li>Total number of users who have completed the journey by reaching the last node.  </li><li>If a user achieves the goal in the last node, it is marked as completed.</li>
      </td>
    </tr>

    <tr>
      <td>
        Goal Met
      </td>

      <td>
        Total number of user who met the journey goal.
      </td>
    </tr>

    <tr>
      <td>
        Goal 1 Name
      </td>

      <td>
        Title of the first goal in the journey.
      </td>
    </tr>

    <tr>
      <td>
        Goal 1 Conversions
      </td>

      <td>
        Number of users who have been converted by achieving goal 1.
      </td>
    </tr>

    <tr>
      <td>
        Goal 2 Name
      </td>

      <td>
        Title of the second goal in the journey.
      </td>
    </tr>

    <tr>
      <td>
        Goal 2 Conversions
      </td>

      <td>
        Number of users who have been converted by achieving goal 2.
      </td>
    </tr>

    <tr>
      <td>
        Goal 3 Name
      </td>

      <td>
        Title of the third goal in the journey.
      </td>
    </tr>

    <tr>
      <td>
        Goal 3 Conversions
      </td>

      <td>
        Number of users who have been converted by achieving goal 3.
      </td>
    </tr>
  </tbody>
</Table>

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

CleverTap BSP allows tracking clicks on the WhatsApp message. The stats for these clicks are available under the Campaigns > Stats page. If Click Tracking is enabled, the Journey Report will display the node stats for the *sent > delivered > viewed > clicked > converted* funnel. However, if Click Tracking is not enabled, only the viewed data is reported for your campaign. Therefore, the funnel in this case is, *sent> delivered > viewed > converted* . 

<Image alt="Click Tracking Funnel" align="center" border={true} src="https://files.readme.io/b139aea-sent_delivered_funnel.jpg">
  Click Tracking Funnel
</Image>

| Campaign/Journey Data                   | Click Tracking Enabled                          | Click Tracking Disabled               |
| :-------------------------------------- | :---------------------------------------------- | :------------------------------------ |
| Unique Sent within Conversion Time      | sent > delivered > viewed > clicked > converted | sent > delivered > viewed >converted  |
| Unique Viewed within Conversion Time    | sent > delivered > viewed > clicked > converted | sent > delivered > viewed > converted |
| Unique Clicked within Conversion Time   | sent > delivered > viewed >clicked > converted  | sent > delivered > viewed > converted |
| Unique Converted within Conversion Time | sent > delivered > viewed >clicked > converted  | 0.                                    |
