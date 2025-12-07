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

![2862](https://files.readme.io/d09bae1-Add_Feed_Input.png "Add Feed Input.png")

4. Enter the *Configuration Name* and turn **ON** the *Feed Status* toggle. 

<Image title="Feed Config popup.png" alt={2818} className="border" border={true} src="https://files.readme.io/1a0fc12-Feed_Config_popup.png" />

5. Click **Save**. The *Server to Server Key* and *Server to Server Secret* are displayed.

<Image title="Key and Secret Details.png" alt={2806} className="border" border={true} src="https://files.readme.io/af1581a-Key_and_Secret_Details.png" />

5. Copy the project details. You will need them when configuring the CleverTap dashboard.

## Configure CleverTap Dashboard

To configure the CleverTap dashboard:

1. Log in to your CleverTap account and navigate to the *Settings* > *Partners* page. 

<Image title="Navigating to Partners page.png" alt={2700} className="border" border={true} src="https://files.readme.io/a5fc4fa-Navigating_to_Partners_page.png" />

2. Hover on the *mParticle* icon and click **Integrate**.

<Image title="Click Integrate.png" alt={2376} className="border" border={true} src="https://files.readme.io/c4a1f62-Click_Integrate.png" />

   On clicking, *Integrate raw data partner - mParticle* popup opens on the right side of the screen.\
3\. Enter the following details and click **Integrate**. 

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
        Partner Nickname
      </td>

      <td>
        Enter the *Nickname* for your integration.
      </td>
    </tr>

    <tr>
      <td>
        API key and API secret
      </td>

      <td>
        These are the unique codes passed to mParticle to verify your credentials. For more information about obtaining the key, refer to [Find mParticle Project Details](doc:mparticle-export#find-mparticle-project-details).
      </td>
    </tr>

    <tr>
      <td>
        Customer ID Mapping
      </td>

      <td>
        This is used as an identifier when sending event data to mParticle.
      </td>
    </tr>
  </tbody>
</Table>

<Image title="Integrate raw data partner.png" alt={2362} className="border" border={true} src="https://files.readme.io/fad6773-Integrate_raw_data_partner.png" />

   After successful integration, the *Integrated* tag displays against *mParticle* on the *Partner List* page.

<Image title="Integrated tag.png" alt={2390} className="border" border={true} src="https://files.readme.io/f38ed77-Integrated_tag.png" />

# Create New Export

To create a new export:

1. Navigate to *Settings* > *Partners* > *Exports* from the CleverTap dashboard.
2. Click **+ Export** and select *mParticle* from the *Partners* list.

<Image title="Create Export.png" alt={2376} className="border" width="smart" border={true} src="https://files.readme.io/f03c9d4-Create_Export.png" />

On clicking, the *Export to mParticle* pop-up displays on the right side of the screen.

<Image title="Export to mParticle.png" alt={2376} className="border" border={true} src="https://files.readme.io/2e61e9a-Export_to_mParticle.png" />

3. Configure the following settings:
   * **Type**: Select the type of data that you want to export from the available options. For more information, refer to [Export Details](doc:mparticle-export#export-details).
   * **Frequency**: Select from one of the following options:
     * *Once only*: A single export for the selected export type. You can export data up to the last 60 days. You create an export for a specific day, date range, previous month, current month, and more.  
     * *Recurring*: Set up a recurring frequency to export all the new events/user properties captured in the last window. You can export event data as frequently as every 4 hours and up to once every 24 hours. You can export user properties only once every 24 hours. 
4. Click **Export**. The popup closes, and the following message displays at the top of the *Exports* page:

<Image title="Export initiated.png" alt={2284} className="border" border={true} src="https://files.readme.io/1acfbc0-Export_initiated.png" />

CleverTap processes the export, and you can now see the newly-created export for mParticle.

<Image title="Exports page.png" alt={2372} className="border" border={true} src="https://files.readme.io/1b9a88e-Exports_page.png" />

The status for each export is displayed as *Pending* as soon as the export is created. The status changes to *Running* after the processing starts. And, it changes to *Done* when the export is complete.

# Stop Export

You can also stop the export that you have created. To do so, click the ![Stop export](https://files.readme.io/437ad4c-Stop_export_icon.png) icon for the export request you want to stop and then click **Stop** to confirm your action.

<Image title="Stop Export.png" alt={2372} className="border" border={true} src="https://files.readme.io/7c7af00-Stop_Export.png" />

You are navigated back to the *Exports* page, and the *mParticle data export stopped* message displays at the top. The status for the data export now displays as *Stopped*.

<Image title="Export Stopped.png" alt={2340} className="border" border={true} src="https://files.readme.io/8d483ed-Export_Stopped.png" />

# Export Details

Select from one of the following options to export events from CleverTap to the mParticle dashboard:

* [All events](doc:mparticle-export-pe-2#all-events)
* [Selected events](doc:mparticle-export-pe-2#selected-events)
* [Engagement events](doc:mparticle-export-pe-2#engagement-events)
* [User properties](doc:mparticle-export-pe-2#user-properties)

## All Events

When you select this option, the following defined system events are exported:

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
        Push Impressions
      </td>

      <td>
        This event is tracked when a push notification sent from CleverTap is delivered on a user’s device. The funnels on the Push campaign statistics page reflect the count for this event.
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
        AB Experiment Disqualified
      </td>

      <td>
        This event is raised when the device is disqualified.
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
        App Version Changed
      </td>

      <td>
        This event is raised when a user’s current app version is different from the user’s previous app version.
      </td>
    </tr>

    <tr>
      <td>
        App Launched
      </td>

      <td>
        This event is recorded every time a user launches your application.
      </td>
    </tr>

    <tr>
      <td>
        App Installed
      </td>

      <td>
        The event is raised when the user launches the app for the first time.
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
        UTM Visited
      </td>

      <td>
        This event is tracked when a user clicks on a link from a marketing campaign that has a UTM parameter defined on it.
      </td>
    </tr>
  </tbody>
</Table>

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
        Name
      </td>

      <td>
        Indicates the name of the user.
      </td>
    </tr>

    <tr>
      <td>
        Gender
      </td>

      <td>
        Indicates the gender of the user.
      </td>
    </tr>

    <tr>
      <td>
        DOB
      </td>

      <td>
        Indicates the date of the birth of the user.
      </td>
    </tr>

    <tr>
      <td>
        All communication preference
      </td>

      <td>
        Flags that determine the communication preference of the user.
      </td>
    </tr>
  </tbody>
</Table>

> 📘 Availability of Feature
>
> If you are a CleverTap for Enterprises user, contact your sales account manager to activate this feature at your end. In the case of CleverTap for Startups, it is available as a paid add-on.
