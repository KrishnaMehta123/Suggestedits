---
title: Mixpanel Export
excerpt: >-
  Understand how you can export event data from CleverTap to the Mixpanel
  dashboard. To learn more about the import feature, refer to [Mixpanel
  Import](https://docs.clevertap.com/docs/mixpanel-integration).
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

This section provides information about exporting event data from CleverTap to the Mixpanel dashboard. CleverTap also offers to import Mixpanel cohorts. To learn more about this feature, refer to [Mixpanel Import](doc:mixpanel-integration).

> 📘 Export Limit Per Event
>
> Mixpanel supports exporting only 255 event properties per event. If the number of event properties exceeds the Mixpanel limit, the CleverTap exports the first 255 event properties.

# Setup

The setup involves adding Mixpanel project details to the CleverTap dashboard. To add the project details:

1. Log in to your CleverTap account.
2. Navigate to *Settings* > *Partners* > *Partner List*. 

<Image title="Navigating to Partners page from the CleverTap Dashboard" alt={2850} align="center" width="90% " border={true} src="https://files.readme.io/54ea074-PartnersList.jpg">
  Navigate to the Partners Page
</Image>

3. Hover on the *Mixpanel* icon and click **Integrate**.

<Image title="Hover on the Mixpanel icon and click Integrate" alt={2372} align="center" width="90% " border={true} src="https://files.readme.io/0102041-IntegrateMixpanel.jpg">
  Integrate Mixpanel
</Image>

On clicking, the *Integrate analytics partner - Mixpanel* popup opens on the right side of the screen.

4. Enter the following details and click **Integrate**:

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
        <p>Mixpanel Project ID</p>
      </td>

      <td>
        <p>The Project token is used to send event data to Mixpanel. For more information, refer to <a href="https://help.mixpanel.com/hc/en-us/articles/115004490503-Project-Settings#project-id">Project ID</a>.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Service Account Username</p>
      </td>

      <td>
        <p>A descriptive name for the service account in Mixpanel. For more information, refer to <a href="https://developer.mixpanel.com/reference/service-accounts#authenticating-with-a-service-account">Service Account Username</a>.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Service Account Secret</p>
      </td>

      <td>
        <p>The secret API is the key that corresponds to your project. For more information, refer to <a href="https://developer.mixpanel.com/reference/service-accounts#authenticating-with-a-service-account">Service Account Secret</a>.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Data Residency</p>
      </td>

      <td>
        <ul><li>The Data Residency is the physical/geographical storage location of data (EU or Standard) for each project.</li><li>For more information, refer to <a href="https://help.mixpanel.com/hc/en-us/articles/115004490503-Project-Settings#data-residency">Data Residency</a>.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        Mixpanel Distinct ID Mapping
      </td>

      <td>
        This user property is used as an identifier when sending event data to Mixpanel. For more information, refer to 

        [Distinct ID](https://help.mixpanel.com/hc/en-us/articles/115004509406-Distinct-IDs-)

        .
      </td>
    </tr>
  </tbody>
</Table>

<br />

<Image alt="Enter Mixpanel Project Details to Integrate" align="center" width="70% " border={true} src="https://files.readme.io/cae2046-image.png">
  Enter Mixpanel Project Details to Integrate
</Image>

After successful integration, the *Integrated* tag displays against Mixpanel on the *Partner List* page.

<Image alt="Successful Mixpanel Integration" align="center" border={true} src="https://files.readme.io/13059cb-image.png">
  Successful Mixpanel Integration
</Image>

# Create New Export

To create a new export:

1. Navigate to **Settings** > **Partners** > **Exports**.
2. Click **Create Export** and select **Mixpanel**.

<Image title="Click + Export and select Mixpanel from the Partner dropdown" alt={2376} align="center" width="90% " border={true} src="https://files.readme.io/2b7000c-CreateMixpanelExport.jpg">
  Create Mixpanel Export
</Image>

The **Export to Mixpanel** popup displays.

<Image title="Enter export details and click Export" alt={2346} align="center" width="90% " border={true} src="https://files.readme.io/ba2ad2e-ExportToMixpanel.jpg">
  Enter Mixpanel Export Details
</Image>

3. Configure the settings as required. 
   * **Partner Nickname**: Nickname for the partner. To edit the nickname, go to **Partner List**. 
   * **DATA TYPE & IDENTIFIER PRIORITY**: Select the events from the available options to export. For more information, refer to [Export Details](https://docs.clevertap.com/docs/mixpanel-export#export-details).
   * **FREQUENCY**: Select from one of the following options:
     * **One time**: A single export for the selected export type. You can export data up to the last **60 days**. You create an export for a specific day, date range, previous month, current month, and more.  
     * **Recurring**: Set up a recurring export that exports all the new events captured in the last window. You can export data as frequently as every 4 hours and up to once every 24 hours. 
     * **Live Datastreaming**: Exports data continuously in real-time.
     * **Date to export data**: The export starts at 12:00 a.m. on the specified date by default.

> 📘 Rate Limits
>
> If you are a Mixpanel enterprise customer and require a higher limit for a one-time backfill, contact [apis@mixpanel.com](mailto:apis@mixpanel.com) with your project\_id and use-case.

4. Click **Export**. On clicking, the popup closes, and the following message displays at the top of the *Exports* page:

<Image title="Mixpanel export has initiated message displays at the top" alt={2442} align="center" width="90% " border={true} src="https://files.readme.io/724549a-MixpanelExportInitiated.jpg">
  Mixpanel Export Initiated
</Image>

CleverTap processes the export, and you can now see the newly created export for Mixpanel.

The status for each export is displayed as **PENDING** as soon as the export is created. The status changes to **RUNNING** after the processing starts. It changes to **DONE** when the export is complete.

# Stop Export

You can also stop the running export. Hover over the export. Click the **Stop**  ![Stop export](https://files.readme.io/203208a-StopExport.jpg) button.

<Image title="Click the Stop icon to stop the ongoing Mixpanel export" alt={2376} align="center" width="90% " border={true} src="https://files.readme.io/623b663-StopMixpanel.jpg">
  Stop Mixpanel Export
</Image>

The **Stop export?** window appears. Click **Stop** to confirm your action.

<Image align="center" className="border" width="60% " border={true} src="https://files.readme.io/8f7a2ee-StopMixpanelWindow.jpg" />

You are navigated back to the **Exports** page. The *Mixpanel data export stopped* message displays at the top. The status of export is now displayed as **STOPPED**.

<Image title="Mixpanel export has initiated message displays at the top" alt={2368} align="center" width="90% " border={true} src="https://files.readme.io/ecfcc6b-MixpanelExportStopped.jpg">
  Mixpanel Export Stopped
</Image>

# Edit an Export

You might need to modify an export to meet specific business requirements or while waiting for the next run. This section describes editing a Live Data Streaming and Recurring export in the **RUNNING** and **PENDING**(awaiting next run) state. 

> 📘 Points to Remember
>
> * In case of running exports, the new changes will apply to the next run.
> * You cannot edit a One-time export, regardless its status (RUNNING, PENDING, DONE, or STOPPED).
> * You cannot change the export from User Profile to Event and vice-versa.
> * You cannot modify exports marked as **DONE** or **STOPPED**.
> * Export changes for Live DataStreaming take 10-15 minutes to take effect.

To edit an export: 

1. On the CleverTap dashboard, go to **Partners** > **Exports**.
2. Hover over the required export. The **View**, **Edit**, and the **Stop** buttons appear.

<Image alt="Click the Edit Export Icon" align="center" width="90% " border={true} src="https://files.readme.io/4ef3467-EditMixpanel.jpg">
  Click the Edit Export Icon
</Image>

3. Click the **Edit** button. The **Export to Mixpanel** section appears.

<Image alt="Edit the Export" align="center" width="90% " border={true} src="https://files.readme.io/5cb8482-UpdateMixpanelExport.jpg">
  Edit the Export
</Image>

4. Edit the export details and click **Update export**.

# Filter Exports

This section describes the different ways you can filter exports.

## Filter by Export Details

To filter by export details: 

1. Click the **Filter** button at the top right corner. 
2. You can filter exports by **Partner**, **Type**, **Format**, **Status**, or **Frequency**. 
3. To clear the filter, click **Reset all**.

<Image alt="Filter Exports" align="center" width="90% " border={true} src="https://files.readme.io/6499e90-FilterButton.jpg">
  Filter Exports
</Image>

## Filter Exports by Date Range

You can also filter the exports based on the export date. 

To filter exports by export date range:

1. Click the **Filter** button at the top right corner. 
2. Click the **Exported on** button.\
   The **Calendar** widget appears. 

<Image alt="Calendar Widget" align="center" width="90% " border={true} src="https://files.readme.io/74ce34b-Amplitude_Exports_-_Calendar_Widget.png">
  Calendar Widget
</Image>

1. Choose the custom date range and click **Apply**.\
   The exports are filtered accordingly.

## Filter Exports by Pagination

To choose how many export items you view per page:

1. Use the **Items per page** drop-down at the bottom of the **Exports** page.
2. Options include 10, 20, 30, or 40. By default, the **Exports** page shows 20 exports.

# Export Details

Select from one of the following options to export events from CleverTap to the Mixpanel dashboard:

* [All events](doc:mixpanel-export#all-events)
* [Selected events](doc:mixpanel-export#selected-events)
* [Engagement events](doc:mixpanel-export#engagement-events)

## All Events

Export data for all defined events, including *System* and *Custom* events.

## Selected Events

Select the specific events to export. 

## Engagement Events

Export the following engagement events:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        <p>CleverTap Event Name</p>
      </th>

      <th>
        <p>Description</p>
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>Notification Sent</p>
      </td>

      <td>
        <ul><li>The event is tracked when the notification is successfully sent from CleverTap to the communication channel you select for your campaign. </li><li>This event is always recorded, even if the user does not open or click the message. </li><li>This event is recorded for Email, Mobile Push, SMS, and Web Push campaigns. </li><li>This event is available on the Event dashboard but not on the User Profile.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Notification Viewed</p>
      </td>

      <td>
        <ul><li>The event is tracked when a user views an email, in-app, or web notification sent from CleverTap.</li><li>The event is available for Email, Web Push, In-App, Web Popup, and App Inbox.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Notification Clicked</p>
      </td>

      <td>
        <p>The event is tracked when a user clicks on a Mobile Push, In-App, Email, Web Popup, or Web Push message sent via the CleverTap dashboard or through the campaign API.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Push Impressions</p>
      </td>

      <td>
        <ul><li>After the Push Impression is implemented in the SDK, the toggle must be turned on from the CleverTap dashboard.</li><li>This event is recorded whenever a push notification sent via CleverTap is delivered to the user’s device.</li><li>The funnels on the Push campaign statistics page reflect the count for this event.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Notification Replied</p>
      </td>

      <td>
        <p>This event is tracked when the brand receives a reply from the user for WhatsApp.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Push Unregistered</p>
      </td>

      <td>
        <ul><li>This debug event is tracked when an existing mobile push token is removed for a profile.</li><li>The event is tracked for a profile when:<ul><li>A user logs out of the device, and another user logs in. Applicable only if the onUserLogin() method is implemented.</li><li>When a push token is removed using the pushFcmRegisterationId("token",false) method. Applicable only for Android.</li></ul></li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Control Group</p>
      </td>

      <td>
        <p>The event is tracked when a campaign is activated with a Control group.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Channel Unsubscribed</p>
      </td>

      <td>
        <ul><li><p>The event is raised when an email is not acknowledged.</p></li><li><p>The following are the event properties:</p><ul><li>Campaign ID: This is the ID of<br />the campaign from which users are updating subscriptions.<br />Campaign Type: Currently only email.</li><li>Group: Group name from which the user unsubscribed/resubscribed.</li><li>Identity: The user identity/email address.</li><li>Variant Type: Valid values are bounced, dropped, and spam. Email IDs that bounce, drop or marked as spam are opted out from future emails</li><li>Subscription Type: Account level and profile level. Profile level signifies that the user who qualified for the communication is opted out. Account level signifies that all users with the email address are opted out from future communications.</li><li>Reason: Reason which was given by the email provider for the type of the error. For example: "smtp;550 5.1.1 The email account that you tried to reach does not exist. Please try double-checking the recipient's email address for typos or unnecessary spaces."</li></ul></li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Reachable By</p>
      </td>

      <td>
        <p>The event is tracked for a profile when:</p><ul><li>Push token is added/changed.</li><li>Email ID is added/changed.</li><li>Phone number is added/changed.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Notification Delivered</p>
      </td>

      <td>
        <p>The event is tracked when the WhatsApp provider confirms that the notification has reached the end user (double-tick of WhatsApp).</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>AB Experiment Rendered</p>
      </td>

      <td>
        <p>The event is tracked when you are using the Product A/B Tests feature and the variant reaches the device.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>AB Experiment Stopped</p>
      </td>

      <td>
        <p>The event is tracked when you are using the Product A/B Tests feature and the AB experiment is stopped.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>AB Experiment Rolled Out</p>
      </td>

      <td>
        <p>The event is tracked when you are using the Product A/B Tests feature and the winner variant is sent to all the devices.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Geocluster Entered</p>
      </td>

      <td>
        <p>The event is tracked when you enable the geofence feature and your device enters a geofence.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Geocluster Exited</p>
      </td>

      <td>
        <p>The event is tracked when you enable the geofence feature and your device exits a geofence.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Reply Sent</p>
      </td>

      <td>
        <p>The event is tracked against the user profile of the end-user when an agent (CleverTap user) replies to a WhatsApp message from the end user.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>App Uninstalled</p>
      </td>

      <td>
        <ul><li><p>The event is tracked when the user uninstalls the application.</p></li><li><p>There are three cases when this event is tracked multiple times for a single user:</p><ul><li>The first case is when a user installs your app, uninstalls it, and then reinstalls it. </li><li>The second case is when a user clears the app's memory. </li><li>The third case is when a user installs your app on multiple devices.</li></ul></li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Webhook Delivered</p>
      </td>

      <td>
        <p>The event is tracked when a webhook campaign is delivered successfully.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>State Transitioned</p>
      </td>

      <td>
        <ul><li>The event is tracked whenever a user transitions from one state to another or from an unmapped state to one of the states in the lifecycle optimization framework.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>UTM Visited</p>
      </td>

      <td>
        <ul><li>The event is tracked when a user clicks on a link from a marketing campaign that has a UTM parameter defined on it.</li><li>The event is also tracked when a CleverTap-integrated attribution platform, such as Branch or Apsalar, sends this information to CleverTap.</li></ul>
      </td>
    </tr>
  </tbody>
</Table>

# FAQs

### Q. Do CleverTap data exports allow special characters?

A. Yes, CleverTap data exports allow the following special characters:

* CleverTap's export system supports Unicode (UTF-8)  character encoding. It facilitates the accurate representation of text in various languages and scripts. For example, Indian regional languages, Arabic, Korean, Russian, Japanese, Chinese, Spanish, Greek, Indonesian, etc.
* It replaces the following characters with a hyphen to avoid issues in output file generation:
  * Whitespace
  * Tab
  * Slash
  * null (\\0)
* Control characters are replaced with ?. For more information, refer to [Control Character](https://en.wikipedia.org/wiki/Control_character). 
* Supports emoji characters; however, some emojis (UTF-16) may not render properly.
