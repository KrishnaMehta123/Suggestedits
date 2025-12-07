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

This process involves adding mParticle project details to the CleverTap dashboard. To add the project details to the CleverTap dashboard:\
a. Log in to your CleverTap account.\
b. Navigate to *Settings* > *Partners* > *Exports*. 

<Image title="mparticle unconnected.png" alt={1672} className="border" border={true} src="https://files.readme.io/5db8db6-mparticle_unconnected.png" />

c. Click the **mParticle** icon under the *Unconnected partners* section. The *mPaticle* page is displayed.\
d. Enter the mParticle details.

<Image title="Enter details.png" alt={1392} className="border" border={true} src="https://files.readme.io/53c2195-Enter_details.png" />

The project details can be obtained by selecting \* **\* under** of the mParticle dashboard.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field Description
      </th>

      <th>

      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        mParticle API Key
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        mParticle API Secret
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Data Center
      </td>

      <td>
        The Data Center is the physical/geographical storage location of a project's data and is at a project level (per project). Select from the following available options:

        * Default (@harsh: what would be the default center? I think we should mention it here)
        * Australia
        * Europe
        * USA
      </td>
    </tr>

    <tr>
      <td>
        Customer ID Mapping
      </td>

      <td>
        This user property is used as an identifier when sending events data to mParticle.
      </td>
    </tr>
  </tbody>
</Table>

e. Click **Save credentials**. On clicking, the following popup is displayed:

<Image title="Save credentials successfully.png" alt={1390} className="border" border={true} src="https://files.readme.io/563f769-Save_credentials_successfully.png" />

mParticle is now displayed under Connected partners when you navigate to  *Settings* > *Partners* > *Exports*.

<Image title="mParticle connected.png" alt={1394} className="border" border={true} src="https://files.readme.io/1204680-mParticle_connected.png" />

# Create New Export

To create a new export:

1. Navigate to *Settings* > *Partners* > *Exports*.
2. Navigate to the *Activity log* tab and then click **+ Create Export**.

<Image title="2020-11-12_09-13-32_Data Export.png" alt={1316} className="border" width="smart" border={true} src="https://files.readme.io/82460f3-2020-11-12_09-13-32_Data_Export.png" />

On clicking, the *Create an export* popup is displayed.

<Image title="Create an export.png" alt={1384} className="border" border={true} src="https://files.readme.io/8fc1f80-Create_an_export.png" />

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

<Image title="Click Create Export.png" alt={1382} className="border" width="smart" border={true} src="https://files.readme.io/ae5a876-Click_Create_Export.png" />

On successful creation of export, the following message is displayed:

<Image title="Successful export.png" alt={1388} className="border" border={true} src="https://files.readme.io/fc81fda-Successful_export.png" />

5. Click **Ok** to return to the *Exports* page. CleverTap processes the export, and you can now see the newly created export for mParticle.

<Image title="Export created.png" alt={1388} className="border" border={true} src="https://files.readme.io/ecad062-Export_created.png" />

For recurring exports, *Pending* status is displayed.

# Stop Export

You can also stop the export that you have created. To do so:

1. Click the ![ellipses](https://files.readme.io/0210143-ellipses_icon.png) icon for the export request you want to stop and then click ![stop](https://files.readme.io/930e98c-Stop_icon.png). 

<Image title="Click Stop.png" alt={1390} className="border" border={true} src="https://files.readme.io/faf4270-Click_Stop.png" />

You are prompted to confirm your action.

<Image title="Confirm Stop.png" alt={1382} className="border" border={true} src="https://files.readme.io/941bc34-Confirm_Stop.png" />

2. Click **Yes, stop export** to stop the export request. On clicking, the following message is displayed:

<Image title="Stopped successfully.png" alt={1392} className="border" border={true} src="https://files.readme.io/1060180-Stopped_successfully.png" />

3. Click **Ok** to return to the *Exports* page.

# Events Exported to mParticle

The following table provides information about the events exported to the mParticle dashboard:

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
        App Installed
      </td>

      <td>
        This event is recorded when a user installs the application.
      </td>
    </tr>

    <tr>
      <td>
        App Launched
      </td>

      <td>
        This event is recorded every time a user launches the application.
      </td>
    </tr>

    <tr>
      <td>
        App Uninstalled
      </td>

      <td>
        This event is recorded when a user uninstalls the application.
      </td>
    </tr>

    <tr>
      <td>
        UTM Visited
      </td>

      <td>
        This event is tracked when the user clicks on a link from a marketing campaign that has a UTM parameter defined for it.
      </td>
    </tr>

    <tr>
      <td>
        Notification Sent
      </td>

      <td>
        This event is tracked when a campaign message is sent to a user.
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
        This event is tracked only when a user clicks on a marketing campaign sent via CleverTap.
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
        App Version Changed
      </td>

      <td>
        This event is raised when a user upgrades to a new version of application.
      </td>
    </tr>

    <tr>
      <td>
        Notification Replied
      </td>

      <td>
        This event is raised when a user replies to a campaign message. It is raised only for WhatsApp.
      </td>
    </tr>

    <tr>
      <td>
        AB Experiment Stopped
      </td>

      <td>
        This event is raised when AB Experiment is stopped.
      </td>
    </tr>

    <tr>
      <td>
        AB Experiment Rolled Out
      </td>

      <td>
        This event is recorded when the AB experiment is sent to the user.
      </td>
    </tr>

    <tr>
      <td>
        AB Experiment Disqualified
      </td>

      <td>
        This event is raised when the user is disqualified from the experiment.
      </td>
    </tr>

    <tr>
      <td>
        AB Experiment Rendered
      </td>

      <td>
        This event is raised when the experiment is rendered at the user's end.
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
  </tbody>
</Table>

> 📘 Availability of Feature
>
> This feature is available for both CleverTap for Enterprises and CleverTap for Startups plans.\
> Contact your sales account manager to have it activated for you.
