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
  robots: noindex
next:
  description: ''
---
> 📘 Feature in Beta
>
> This is a pre-release feature. If you are an Enterprise user and have any queries about the feature, contact CleverTap Customer Success Team. If you are a CleverTap for Startups user and have any queries about the feature, raise a ticket.

# Overview

Mixpanel data export enables exporting your CleverTap event data to the Mixpanel dashboard.

> 📘 Export Limit Per Event
>
> Mixpanel supports the export of only 255 event properties per event. If the limit exceeds, CleverTap exports the first 255 event properties.

# Setup

The setup involves adding Mixpanel project details to the CleverTap dashboard. To add the project details:

1. Log in to your CleverTap account.
2. Navigate to *Settings* > *Partners* > *Exports*. 

<Image title="Unconnected partners.png" alt={1924} className="border" border={true} src="https://files.readme.io/e39d8db-Unconnected_partners.png" />

3. Click the **Mixpanel** icon under the *Unconnected partners* section. The Mixpanel page displays.
4. Enter the Mixpanel project details.

<Image title="Mixpanel project details.png" alt={1926} className="border" border={true} src="https://files.readme.io/dbec96d-Mixpanel_project_details.png" />

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
        Mixpanel Project ID
      </td>

      <td>
        The Project token is used to send event data to Mixpanel. For more information, refer to [Project ID](https://help.mixpanel.com/hc/en-us/articles/115004490503-Project-Settings#project-id).
      </td>
    </tr>

    <tr>
      <td>
        Service Account Username
      </td>

      <td>
        A descriptive name for the service account in Mixpanel. For more information, refer to [Service Account Username] ([https://developer.mixpanel.com/reference/service-accounts#authenticating-with-a-service-account](https://developer.mixpanel.com/reference/service-accounts#authenticating-with-a-service-account)).
      </td>
    </tr>

    <tr>
      <td>
        Service Account Secret
      </td>

      <td>
        The secret API is the key that corresponds to your project. For more information, refer to [Service Account Secret] ([https://developer.mixpanel.com/reference/service-accounts#authenticating-with-a-service-account](https://developer.mixpanel.com/reference/service-accounts#authenticating-with-a-service-account)).
      </td>
    </tr>

    <tr>
      <td>
        Data Residency
      </td>

      <td>
        The physical/geographical storage location of a project's data (EU or Standard) at a project level (per project).\
        For more information, refer to [Data Residency](https://help.mixpanel.com/hc/en-us/articles/115004490503-Project-Settings#data-residency).
      </td>
    </tr>

    <tr>
      <td>
        Mixpanel Distinct ID Mapping
      </td>

      <td>
        This user property is used as an identifier when sending events data to Mixpanel. For more information, refer to [Distinct ID](https://help.mixpanel.com/hc/en-us/articles/115004509406-Distinct-IDs-).
      </td>
    </tr>
  </tbody>
</Table>

5. Click **Save credentials**. On clicking, the following popup displays:

<Image title="Credentials saved.png" alt={1546} className="border" border={true} src="https://files.readme.io/c3d85c6-Credentials_saved.png" />

Mixpanel is now displayed under *Connected partners* when you navigate to  *Settings* > *Partners* > *Exports*.

<Image title="MIxpanel Connected partner .png" alt={1924} className="border" border={true} src="https://files.readme.io/cd56b87-MIxpanel_Connected_partner_.png" />

# Create New Export

To create a new export:

1. Navigate to *Settings* > *Partners* > *Exports*.
2. Navigate to the *Activity log* tab and then click **+ Create Export**.

<Image title="2020-11-12_09-13-32_Data Export.png" alt={1316} className="border" width="smart" border={true} src="https://files.readme.io/82460f3-2020-11-12_09-13-32_Data_Export.png" />

On clicking, the *Create new board* popup displays.

<Image title="Create New Board popup.png" alt={892} className="border" width="80%" border={true} src="https://files.readme.io/b7f5915-Create_New_Board_popup.png" />

3. Configure the settings as required. 
   * **Choose an export partner**: Select *Mixpanel* from the *Choose an export partner* list.
   * **Export details**: Select the events to export from the available options. For more information, refer to [Export Details](https://docs.clevertap.com/docs/mixpanel-export#export-details).
   * **Choose export frequency**: Select from one of the following options:
     * *One time*: Single export for the export type selected. You can export data up to the last 60 days. 
     * *Recurring*: Set up a recurring export that exports all the new events captured in the last window. You can export data as frequently as every 4 hours and up to once every 24 hours. 

> 📘 Rate Limits
>
> If you are a Mixpanel enterprise customer and require a higher limit for a one-time backfill, contact [apis@mixpanel.com](mailto:apis@mixpanel.com) with your project\_id and use-case.

4. Click **Create export**.

<Image title="Create export.png" alt={838} className="border" width="smart" border={true} src="https://files.readme.io/cbba146-Create_export.png" />

On successful creation of export, the following message is displayed:

<Image title="Successful export.png" alt={1554} className="border" border={true} src="https://files.readme.io/db73cf0-Successful_export.png" />

5. Click **Ok** to return to the *Exports* page.

<Image title="Export created.png" alt={1916} className="border" border={true} src="https://files.readme.io/c704d50-Export_created.png" />

# Stop Export

You can also stop the export that you have created. To stop the current export:

1. Click the ![ellipses](https://files.readme.io/0210143-ellipses_icon.png) icon for the export request you want to stop and then click ![stop](https://files.readme.io/930e98c-Stop_icon.png). 

<Image title="Click Stop.png" alt={2300} className="border" border={true} src="https://files.readme.io/8ad4dae-Click_Stop.png" />

You are prompted to confirm your action.

<Image title="Stop export.png" alt={1868} className="border" border={true} src="https://files.readme.io/7117fac-Stop_export.png" />

2. Click **Yes, stop export** to stop the export request. On clicking, the following message displays:

<Image title="Export stopped successfully.png" alt={1874} className="border" border={true} src="https://files.readme.io/1c7d3f3-Export_stopped_successfully.png" />

3. Click **Ok** to return to the *Exports* page.

# Export Details

Select from one of the following options to export events from CleverTap to the Mixpanel dashboard:

## All events

Export data for all defined events including *System* and *Custom* events.

## Selected events

Select the specific events to export. 

## Engagement Events

Export the following engagement events:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        CleverTap Event Name
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Notification Sent
      </td>

      <td>
        * The event is tracked when the notification is successfully sent from CleverTap to the communication channel you select for your campaign. 
        * This event is always recorded, even if the user does not open or click on the message. 
        * This event is recorded for email, mobile push, SMS  and web push campaigns. 
        * The event is available on the Event dashboard but it is not displayed on the User Profile.
      </td>
    </tr>

    <tr>
      <td>
        Notification Viewed
      </td>

      <td>
        * The event is tracked when a user views an email, in-app notification, or a web notification sent from CleverTap.
        * The event is available for email, web push, in-app, web popup, and app inbox.
      </td>
    </tr>

    <tr>
      <td>
        Notification Clicked
      </td>

      <td>
        The event is tracked when a user clicks on a mobile push, in-app, email, web-popup, or web push message sent via the CleverTap dashboard or through the campaign API.
      </td>
    </tr>

    <tr>
      <td>
        Push Impressions
      </td>

      <td>
        * After the toggle for Push Impressions is turned on/setup from settings, the CleverTap SDK starts recording an event whenever a push notification sent via CleverTap is delivered to the user’s device.
        * The funnels on the Push campaign statistics page reflects the count for this event.
      </td>
    </tr>

    <tr>
      <td>
        Notification Replied
      </td>

      <td>
        This event is tracked when the brand receives a reply from the user for WhatsApp.
      </td>
    </tr>

    <tr>
      <td>
        Push Unregistered
      </td>

      <td>
        * This debug event is tracked when an existing mobile push token is removed for a profile.

        * The event is tracked for a profile when:

          * A user logs out of the device and another user logs in. Applicable only if the onUserLogin() method is implemented.
          * When a push token is removed using the pushFcmRegisterationId("token",false) method. Applicable only for Android.
      </td>
    </tr>

    <tr>
      <td>
        Control Group
      </td>

      <td>
        The event is tracked when a campaign is activated with a Control group.
      </td>
    </tr>

    <tr>
      <td>
        Channel Unsubscribed
      </td>

      <td>
        * The event is raised when an email is not acknowledged.

        * The following are the event properties:
          * Campaign ID: This is the ID of\
            the campaign from which user are updating subscriptions.\
            Campaign Type: Currently only email.
          * Group: Group name from which the user unsubscribed/resubscribed.
          * Identity: The user identity/email address.
          * Variant Type: Valid values are bounced, dropped, and spam. Email IDs which bounce, drop or marked as spam are opted out from future emails
          * Subscription Type: Account level and profile level. Profile level signifies that the user who qualified for the communication is opted out. Account level signifies that all users with the email address are opted out from future communications.
          * Reason: Reason which was given by the email provider for the type of the error. For example: "smtp;550 5.1.1 The email account that you tried to reach does not exist. Please try double-checking the recipient's email address for typos or unnecessary spaces."
      </td>
    </tr>

    <tr>
      <td>
        Reachable By
      </td>

      <td>
        The event is tracked for a profile when:

        * Push token is added/changed.
        * Email ID is added/changed.
        * Phone number is added/changed.
      </td>
    </tr>

    <tr>
      <td>
        Notification Delivered
      </td>

      <td>
        The event is tracked when the WhatsApp provider confirms that the notification has reached the end user (double-tick of WhatsApp).
      </td>
    </tr>

    <tr>
      <td>
        AB Experiment Rendered
      </td>

      <td>
        The event is tracked when you are using the Product A/B Tests feature and the variant reaches the device.
      </td>
    </tr>

    <tr>
      <td>
        AB Experiment Stopped
      </td>

      <td>
        The event is tracked when you are using the Product A/B Tests feature and the AB experiment is stopped.
      </td>
    </tr>

    <tr>
      <td>
        AB Experiment Rolled Out
      </td>

      <td>
        The event is tracked when you are using the Product A/B Tests feature and the winner variant is sent to all the devices.
      </td>
    </tr>

    <tr>
      <td>
        Geocluster Entered
      </td>

      <td>
        The event is tracked when you enable the geofence feature and your device enters a geofence.
      </td>
    </tr>

    <tr>
      <td>
        Geocluster Exited
      </td>

      <td>
        The event is tracked when you enable the geofence feature and your device exits a geofence.
      </td>
    </tr>

    <tr>
      <td>
        Reply Sent
      </td>

      <td>
        The event is tracked against the user profile of the end user when an agent (CleverTap user) replies to a WhatsApp message from the end user.
      </td>
    </tr>

    <tr>
      <td>
        App Uninstalled
      </td>

      <td>
        * The event is tracked when the user uninstalls the application.

        * There are three cases when this event is tracked multiple times for a single user:
          * The first case is when a user installs your app, uninstalls it, and then reinstalls it. 
          * The second case is when a user clears the app's memory. 
          * The third case is when a user installs your app on multiple devices.
      </td>
    </tr>

    <tr>
      <td>
        Webhook Delivered
      </td>

      <td>
        The event is tracked when a webhook campaign is delivered successfully.
      </td>
    </tr>

    <tr>
      <td>
        State Transitioned
      </td>

      <td>
        * The event is tracked whenever a user transitions from one state to another or from unmapped to one of the states in the lifecycle optimization framework.
      </td>
    </tr>

    <tr>
      <td>
        UTM Visited
      </td>

      <td>
        * The event is tracked when a user clicks on a link from a marketing campaign that has a UTM parameter defined on it.
        * The event is also tracked when a CleverTap-integrated attribution platform, such as Branch or Apsalar, sends this information to CleverTap.
      </td>
    </tr>
  </tbody>
</Table>

> 📘 Availability of Feature
>
> This feature is available only for the Enterprise plan. Contact your sales account manager to activate it.
