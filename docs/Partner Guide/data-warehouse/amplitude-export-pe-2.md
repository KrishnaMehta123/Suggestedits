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
2. Navigate to the *Settings* page. 
3. Navigate to *Org Settings* > *Projects*. 
4. Click on a project to find the *API Key* under the *General* tab.

<Image title="Finding API key.png" alt={3552} className="border" border={true} src="https://files.readme.io/75bc618-Finding_API_key.png" />

## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Navigate to *Settings* > *Partners* from the CleverTap dashboard.

<Image title="Navigating to Partners page.png" alt={2700} className="border" border={true} src="https://files.readme.io/f4c2b91-Navigating_to_Partners_page.png" />

2. Hover on the *Amplitude* icon and click **Integrate**. The *Integrate analytics partner - Amplitude* popup opens on the right side of the screen.

<Image title="Click Integrate.png" alt={2214} className="border" border={true} src="https://files.readme.io/0128cc7-Click_Integrate.png" />

3. Enter the following details and click **Integrate**:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        <p>Field</p>
      </th>

      <th>
        <p>Description</p>
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>Partner Nickname</p>
      </td>

      <td>
        <p>Enter the <em>Nickname</em> for your integration.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>API key</p>
      </td>

      <td>
        <p>The unique code for Amplitude to verify your credentials. For more information about obtaining the key, refer to <a href="doc:amplitude-export#find-amplitude-project-details">Find Amplitude Details</a>.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Data Residency</p>
      </td>

      <td>
        <p>The Data Residency is the physical/geographical storage location of data for each project. </p><ul><li>Select from the following available options:<ul><li>Europe (default)</li><li>Standard</li></ul></li></ul>
      </td>
    </tr>

    <tr>
      <td>
        Device ID Mapping
      </td>

      <td>
        This field is mapped to Amplitude's 

        `device_id`

         field for identification when sending data from CleverTap to Amplitude.
      </td>
    </tr>

    <tr>
      <td>
        User ID Mapping
      </td>

      <td>
        This field is mapped to Amplitude's 

        `user_id`

         field for identification when sending data from CleverTap to Amplitude.
      </td>
    </tr>
  </tbody>
</Table>

<Image title="Enter details.png" alt={2224} className="border" border={true} src="https://files.readme.io/6a45898-Enter_details.png" />

After successful integration, the *Integrated* tag displays against *Amplitude* on the *Partner List* page.

<Image title="Integrated tag.png" alt={2224} className="border" border={true} src="https://files.readme.io/2db790d-Integrated_tag.png" />

# Create New Export

This section lists steps to create a new export from the CleverTap dashboard. To do so:

1. Navigate to *Settings* > *Partners* > *Exports* from the CleverTap dashboard.
2. Click **+ Export** and select *Amplitude* from the *Partners* dropdown.

<Image title="Create Export.png" alt={2222} className="border" width="smart" border={true} src="https://files.readme.io/414614a-Create_Export.png" />

The *Export to Amplitude* window displays on the right side of the screen.

<Image title="Export to amplitude.png" alt={2228} className="border" border={true} src="https://files.readme.io/ef30939-Export_to_amplitude.png" />

3. Configure the following settings:
   * **Type**: Select the events to export from the available options. For more information, refer to [Export Details](doc:amplitude-export#export-details).
   * **Frequency**: Select from one of the following options:
     * *Once only*: A single export for the selected export type. You can export data up to the last 60 days. You create an export for a specific day, date range, previous month, current month, and more.  
     * *Recurring*: Set up a recurring export that exports all the new events/user profiles captured in the last window. You can export as frequently as every 4 hours and up to once every 24 hours. 
4. Click **Export**. The *Export to Amplitude* window closes, and the following message displays at the top of *Exports* page:

<Image title="Export initiated.png" alt={2150} className="border" border={true} src="https://files.readme.io/de71059-Export_initiated.png" />

   CleverTap processes the export, and you can now see the newly created export for Amplitude.

<Image title="Exports page.png" alt={2216} className="border" border={true} src="https://files.readme.io/ce2d7dd-Exports_page.png" />

The status for each export is displayed as *Pending* as soon as the export is created. The status changes to *Running* after the processing starts. In the case of *Once only* export, the status changes to *Done* when the export is complete.

# Stop Export

You can also stop the export that you have created. To do so, click the ![Stop export](https://files.readme.io/437ad4c-Stop_export_icon.png) icon for the export request you want to stop and then click **Stop** to confirm your action.

<Image title="Stop Export.png" alt={2216} className="border" border={true} src="https://files.readme.io/48b5bdc-Stop_Export.png" />

You now return to the *Exports* page, and the *Amplitude data export stopped* message displays at the top. The status of the export is displayed as *Stopped*.

<Image title="Export Stopped.png" alt={2216} className="border" border={true} src="https://files.readme.io/18b6435-Export_Stopped.png" />

# Export Details

Select from one of the following options to export events from CleverTap to the Amplitude dashboard:

* [All events](doc:amplitude-export-pe-2#all-events)
* [Selected events](doc:amplitude-export-pe-2#selected-events)
* [Engagement events](doc:amplitude-export-pe-2#engagement-events)

## All events

Export data for all defined events, including System and Custom events.

## Selected events

Select the specific events you want to export from CleverTap to the Amplitude dashboard.

## Engagement Events

Select this option to export the following engagement events:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        <p>CleverTap Event Name</p>
      </th>

      <th>
        <p>Event Description</p>
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>Notification Sent</p>
      </td>

      <td>
        <p>The event is tracked when the notification is successfully sent from CleverTap to the communication channel you select for your campaign.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Notification Viewed</p>
      </td>

      <td>
        <p>This event is tracked when a user views an email, in-app notification, or a web notification sent from CleverTap.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Notification Clicked</p>
      </td>

      <td>
        <p>This event is tracked only when a user clicks on a notification sent via CleverTap. It is recorded when a user clicks on a mobile push, in-app, email, web popup, or web push message sent via the CleverTap dashboard or through the campaign API.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Push Impressions</p>
      </td>

      <td>
        <p>This event is tracked when a Push notification sent from CleverTap is delivered on a user’s device.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Notification Replied</p>
      </td>

      <td>
        <p>This event is tracked when a user replies to a WhatsApp message.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Push Unregistered</p>
      </td>

      <td>
        <p>The event is raised when the user unregisters to receive Push Notifications.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Control Group</p>
      </td>

      <td>
        <p>The event is raised when a campaign is activated with a Control group.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Channel Unsubscribed</p>
      </td>

      <td>
        <p>The event is raised when a user unsubscribes to receive further communication through a channel.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Reachable By</p>
      </td>

      <td>
        <ul><li>The debug event raised when the user becomes reachable by a communication channel such as SMS, email, mobile push, or when there are changes to the existing communication channel.</li><li>Tracked for a profile when:<ul><li>Push token is added/changed.</li><li>Email ID is added/changed.</li><li>Phone number is added/changed.</li></ul></li></ul>
      </td>
    </tr>

    <tr>
      <td>
        Push Impressions
      </td>

      <td>
        This event is tracked when a push notification sent from CleverTap is delivered on a user’s device. The funnels on the Push campaign statistics page reflect the count for this event.
      </td>
    </tr>

    <tr>
      <td>
        Notification Delivered
      </td>

      <td>
        This event is recorded when communication is delivered to the user's device
      </td>
    </tr>

    <tr>
      <td>
        AB Experiment Rendered
      </td>

      <td>
        This event is recorded when communication is delivered to the user who is part of an A/B experiment campaign
      </td>
    </tr>

    <tr>
      <td>
        AB Experiment Stopped
      </td>

      <td>
        This event is recorded when AB experiment is stopped.
      </td>
    </tr>

    <tr>
      <td>
        AB Experiment Rolled Out
      </td>

      <td>
        This event is recorded when AB experiment is started
      </td>
    </tr>

    <tr>
      <td>
        Geocluster Entered
      </td>

      <td>
        This event is recorded to mark when a device enters a geofence.
      </td>
    </tr>

    <tr>
      <td>
        Geocluster Exited
      </td>

      <td>
        This event is recorded to mark when a device exits a geofence.
      </td>
    </tr>

    <tr>
      <td>
        Reply Sent
      </td>

      <td>
        This event is recorded when an agent (CleverTap user) replies to a message from the end-user.
      </td>
    </tr>

    <tr>
      <td>
        App Uninstalled
      </td>

      <td>
        This event is recorded when a user uninstalls your application.
      </td>
    </tr>

    <tr>
      <td>
        Webhook Delivered
      </td>

      <td>
        This event is recorded when a Webhook campaign is delivered successfully
      </td>
    </tr>

    <tr>
      <td>
        State Transitioned
      </td>

      <td>
        This event is recorded for Lifecycle Optimizer when a user transitions from one stage to another.
      </td>
    </tr>

    <tr>
      <td>
        UTM Visited
      </td>

      <td>
        This event is tracked when a user clicks on a link from a marketing campaign that has a UTM parameter defined on it.
      </td>
    </tr>
  </tbody>
</Table>

> 📘 Availability of Feature
>
> This feature is available for the *CleverTap for Enterprise* plan. Contact your sales account manager to activate it.
