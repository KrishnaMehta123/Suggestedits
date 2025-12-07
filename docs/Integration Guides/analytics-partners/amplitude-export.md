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
> 📘 Feature in Beta
>
> Currently, this is a private beta feature. If you have any queries about the feature, contact CleverTap Customer Success Team.

# Overview

The data export feature provides the capability to export your CleverTap event data to your Amplitude dashboard. You can use this event data for further analysis.

# Setup

This process involves adding Amplitude details to the CleverTap dashboard. To add the project details to the CleverTap dashboard:\
a. Log in to your CleverTap account.\
b. Navigate to *Settings* > *Partners* > *Exports*. 

<Image title="Amplitude unconnected.png" alt={1708} className="border" border={true} src="https://files.readme.io/e941d6c-Amplitude_unconnected.png" />

c. Click the **Amplitude** icon under the *Unconnected partners* section. The *Amplitude* page is displayed.\
d. Enter the Amplitude details.

<Image title="Enter Amplitude details.png" alt={1390} className="border" border={true} src="https://files.readme.io/b37e1b5-Enter_Amplitude_details.png" />

The project details can be obtained by navigating to *Settings* > *Projects* on the Amplitude dashboard and selecting the project for which you want to view the details.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Amplitude API Key
      </td>

      <td>
        It is the unique code passed to Amplitude to verify your credentials. You can find the API key under *Settings* > *Projects*.
      </td>
    </tr>

    <tr>
      <td>
        Data Residency
      </td>

      <td>
        The Data Residency is the physical/geographical storage location of a project's data and is at a project level (per project). Select from the following available options:

        * Europe
        * Standard
      </td>
    </tr>

    <tr>
      <td>
        Amplitude User ID Mapping
      </td>

      <td>
        This identifier will be mapped to Amplitude's `user_id` field while sending data from CleverTap to Amplitude.
      </td>
    </tr>

    <tr>
      <td>
        Amplitude Device ID Mapping
      </td>

      <td>
        This identifier will be mapped to Amplitude's `device_id` field while sending data from CleverTap to Amplitude.
      </td>
    </tr>
  </tbody>
</Table>

e. Click **Save credentials**. On clicking, the following popup is displayed:

<Image title="Credentials saved.png" alt={1388} className="border" border={true} src="https://files.readme.io/befc108-Credentials_saved.png" />

Amplitude is now displayed under Connected partners when you navigate to  *Settings* > *Partners* > *Exports*.

<Image title="Amplitude connected.png" alt={1390} className="border" border={true} src="https://files.readme.io/d0dee3b-Amplitude_connected.png" />

# Create New Export

To create a new export:

1. Navigate to *Settings* > *Partners* > *Exports*.
2. Navigate to the *Activity log* tab and then click **+ Create Export**.

<Image title="Create export.png" alt={1388} className="border" width="smart" border={true} src="https://files.readme.io/577eb72-Create_export.png" />

On clicking, the *Create an export* popup is displayed.

<Image title="Create an export popup.png" alt={1384} className="border" border={true} src="https://files.readme.io/8658e96-Create_an_export_popup.png" />

3. Configure the following settings:
   * **Choose an export partner**: Select *Amplitude* from the *Choose an export partner* dropdown list.
   * Export details: Select the events to export from the available options. For more information, refer to [Export Details](https://docs.clevertap.com/docs/amplitude-export#export-details).
   * Choose export frequency: Select from one of the following options
     * One time: Single export for the export type selected. You can export data up to the last 60 days. 
     * Recurring: Set up a recurring export that exports all the new events/user profiles captured in the last window. You can export as frequently as every 4 hours and up to once every 24 hours. 
4. Click **Create export**.

<Image title="Click create export.png" alt={1390} className="border" width="smart" border={true} src="https://files.readme.io/f9d455e-Click_create_export.png" />

On successful creation of export, the following message is displayed:

<Image title="Export created successfully.png" alt={1390} className="border" border={true} src="https://files.readme.io/b36d7bc-Export_created_successfully.png" />

5. Click **Ok** to return to the *Exports* page. CleverTap processes the export, and you can now see the newly created export for Amplitude.

<Image title="Export page.png" alt={1384} className="border" border={true} src="https://files.readme.io/13572f5-Export_page.png" />

The status for each export is displayed as *Pending* as soon as the export is created. The status changes to *Running* after the processing starts. And, it changes to *Done* when the export is complete.

# Stop Export

You can also stop the export that you have created. To do so:

1. Click the ![ellipses](https://files.readme.io/0210143-ellipses_icon.png) icon for the export request you want to stop and then click ![stop](https://files.readme.io/930e98c-Stop_icon.png). 

<Image title="Click Stop.png" alt={1382} className="border" border={true} src="https://files.readme.io/6340035-Click_Stop.png" />

You are prompted to confirm your action.

<Image title="Confirm stop export.png" alt={1386} className="border" border={true} src="https://files.readme.io/a5797fa-Confirm_stop_export.png" />

2. Click **Yes, stop export** to stop the export request. On clicking, the following message is displayed:

<Image title="Export stopped successfully.png" alt={1398} className="border" border={true} src="https://files.readme.io/1a50eb7-Export_stopped_successfully.png" />

3. Click **Ok** to return to the *Exports* page.

# Export Details

Select from one of the following options to export events from CleverTap to the Amplitude dashboard:

## All events

Export data for all defined events including System and Custom events.

## Selected events

Select the specific events that you want to export from CleverTap to the Amplitude dashboard.

## Engagement Events

Export the following engagement events:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        CleverTap Event Name
      </th>

      <th>
        Event Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Notification Sent
      </td>

      <td>
        The event is tracked when the notification is successfully sent from CleverTap to the communication channel you select for your campaign.
      </td>
    </tr>

    <tr>
      <td>
        Notification Viewed
      </td>

      <td>
        This event is tracked when a user views an email, in-app notification, or a web notification sent from CleverTap.
      </td>
    </tr>

    <tr>
      <td>
        Notification Clicked
      </td>

      <td>
        This event is tracked only when a user clicks on a notification sent via CleverTap.Recorded when a user clicks on a mobile push, in-app, email, web-popup, or web push message sent via the CleverTap dashboard or through the campaign API.
      </td>
    </tr>

    <tr>
      <td>
        Push Impressions
      </td>

      <td>
        This event is tracked when a Push notification sent from CleverTap is delivered on a user’s device.
      </td>
    </tr>

    <tr>
      <td>
        Notification Replied
      </td>

      <td>
        This event is recorded when a user replies to a WhatsApp message.
      </td>
    </tr>

    <tr>
      <td>
        Push Unregistered
      </td>

      <td>
        The event raised when the user unregisters to receive Push Notifications.
      </td>
    </tr>

    <tr>
      <td>
        Control Group
      </td>

      <td>
        The event raised when a campaign is activated with a Control group.
      </td>
    </tr>

    <tr>
      <td>
        Channel Unsubscribed
      </td>

      <td>
        The event raised when a user Unsubscribes to receive further communication through a channel
      </td>
    </tr>

    <tr>
      <td>
        Reachable By
      </td>

      <td>
        * The debug event raised when the user becomes reachable by a communication channel such as SMS, email, mobile push, or when there are changes to the existing communication channel.
        * Tracked for a profile when:
          * Push token is added/changed.
          * Email ID is added/changed.
          * Phone number is added/changed.
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
        This event is recorded for lifecycle optimizer when a user transitions from one stage to another.
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
> This feature is available for CleverTap for Enterprise plan. Contact your sales account manager to activate it.
