---
title: Mixpanel Export_PE_2
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

This section provides information about exporting event data from CleverTap to the Mixpanel dashboard. CleverTap also offers to import Mixpanel cohorts. To learn more about this feature, refer to [Mixpanel Import](https://docs.clevertap.com/docs/mixpanel-integration).

> 📘 Export Limit Per Event
> 
> Mixpanel supports exporting only 255 event properties per event. If the number of event properties exceeds the Mixpanel limit, the CleverTap exports the first 255 event properties.

# Setup

The setup involves adding Mixpanel project details to the CleverTap dashboard. To add the project details:

1. Log in to your CleverTap account.
2. Navigate to _Settings_ > _Partners_. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d5f2cd9-Navigating_to_Partners_page.png",
        "Navigating to Partners page.png",
        2850
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


3. Hover on the _Mixpanel_ icon and click **Integrate**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d68e130-Hover_on_Mixpanel_.png",
        "Hover on Mixpanel .png",
        2372
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


On clicking, _Integrate analytics partner - Mixpanel_ popup opens on the right side of the screen.

4. Enter the following details and click **Integrate**:

| <p>Field</p>                    | <p>Description</p>                                                                                                                                                                                                                                                                          |
| :------------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <p>Mixpanel Project ID</p>      | <p>The Project token is used to send event data to Mixpanel. For more information, refer to <a href="https://help.mixpanel.com/hc/en-us/articles/115004490503-Project-Settings#project-id">Project ID</a>.</p>                                                                              |
| <p>Service Account Username</p> | <p>A descriptive name for the service account in Mixpanel. For more information, refer to <a href="https://developer.mixpanel.com/reference/service-accounts#authenticating-with-a-service-account">Service Account Username</a>.</p>                                                       |
| <p>Service Account Secret</p>   | <p>The secret API is the key that corresponds to your project. For more information, refer to <a href="https://developer.mixpanel.com/reference/service-accounts#authenticating-with-a-service-account">Service Account Secret</a>.</p>                                                     |
| <p>Data Residency</p>           | <ul><li>The Data Residency is the physical/geographical storage location of data (EU or Standard) for each project.</li><li>For more information, refer to <a href="https://help.mixpanel.com/hc/en-us/articles/115004490503-Project-Settings#data-residency">Data Residency</a>.</li></ul> |
| Mixpanel Distinct ID Mapping    | This user property is used as an identifier when sending events data to Mixpanel. For more information, refer to [Distinct ID](https://help.mixpanel.com/hc/en-us/articles/115004509406-Distinct-IDs-).                                                                                     |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/da87724-Integrate_with_Mixpanel.png",
        "Integrate with Mixpanel.png",
        2372
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


After successful integration, the _Integrated_ tag displays against Mixpanel on the _Partner List_ page.

![](https://files.readme.io/1e2074d-Integrated_tag.png "Integrated tag.png")

# Create New Export

To create a new export:

1. Navigate to _Settings_ > _Partners_ > _Exports_.
2. Click **Create Export** and select _Mixpanel_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/632039a-CreateMixpanelExport.jpg",
        "Select Mixpanel from Partner List.png",
        2376
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


The _Export to Mixpanel_ popup displays on the right side of the screen.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cc81d4e-ExportToMixpanel.jpg",
        "Export to Mixpanel .png",
        2346
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


3. Configure the settings as required. 
   - **Type**: Select the events to export from the available options. For more information, refer to [Export Details](https://docs.clevertap.com/docs/mixpanel-export#export-details).
   - **Frequency**: Select from one of the following options:
     - _One time_: A single export for the selected export type. You can export data up to the last **60 days**. You create an export for a specific day, date range, previous month, current month, and more.  
     - _Recurring_: Set up a recurring export that exports all the new events captured in the last window. You can export data as frequently as every 4 hours and up to once every 24 hours. 

> 📘 Rate Limits
> 
> If you are a Mixpanel enterprise customer and require a higher limit for a one-time backfill, contact [apis@mixpanel.com](mailto:apis@mixpanel.com) with your project_id and use-case.

4. Click **Export**. On clicking, the popup closes, and the following message displays at the top of the _Exports_ page:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c0c8219-MixpanelExportInitiated.jpg",
        "MIxpanel export initiated.png",
        2442
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


CleverTap processes the export, and you can now see the newly created export for Mixpanel.

The status for each export is displayed as _Pending_ as soon as the export is created. The status changes to _Running_ after the processing starts. It changes to _Done_ when the export is complete.

# Stop Export

You can also stop the running export. To do so, click the  ![Stop export](https://files.readme.io/203208a-StopExport.jpg) **Stop Export** icon and click **Stop** to confirm your action.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/029bab7-StopMixpanel.jpg",
        "Click Stop icon.png",
        2376
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


On clicking, you are navigated back to the _Exports_ page and the _Mixpanel data export stopped_ message displays at the top. The status of export is now displayed as _Stopped_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e2fe660-MixpanelExportStopped.jpg",
        "Mixpanel data export stopped.png",
        2368
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


# Export Details

Select from one of the following options to export events from CleverTap to the Mixpanel dashboard:

- [All events](doc:mixpanel-export_pe_2#all-events)
- [Selected events](doc:mixpanel-export_pe_2#selected-events)
- [Engagement events](doc:mixpanel-export_pe_2#engagement-events)

## All Events

Export data for all defined events, including _System_ and _Custom_ events.

## Selected Events

Select the specific events to export. 

## Engagement Events

Export the following engagement events:

| <p>CleverTap Event Name</p>     | <p>Description</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| :------------------------------ | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Notification Sent</p>        | <ul><li>The event is tracked when the notification is successfully sent from CleverTap to the communication channel you select for your campaign. </li><li>This event is always recorded, even if the user does not open or click the message. </li><li>This event is recorded for Email, Mobile Push, SMS, and Web Push campaigns. </li><li>This event is available on the Event dashboard but not on the User Profile.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <p>Notification Viewed</p>      | <ul><li>The event is tracked when a user views an email, in-app, or web notification sent from CleverTap.</li><li>The event is available for Email, Web Push, In-App, Web Popup, and App Inbox.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <p>Notification Clicked</p>     | <p>The event is tracked when a user clicks on a Mobile Push, In-App, Email, Web Popup, or Web Push message sent via the CleverTap dashboard or through the campaign API.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <p>Push Impressions</p>         | <ul><li>After the Push Impression is implemented in the SDK, the toggle must be turned on from the CleverTap dashboard.</li><li>This event is recorded whenever a push notification sent via CleverTap is delivered to the user’s device.</li><li>The funnels on the Push campaign statistics page reflect the count for this event.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <p>Notification Replied</p>     | <p>This event is tracked when the brand receives a reply from the user for WhatsApp.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <p>Push Unregistered</p>        | <ul><li>This debug event is tracked when an existing mobile push token is removed for a profile.</li><li>The event is tracked for a profile when:<ul><li>A user logs out of the device, and another user logs in. Applicable only if the onUserLogin() method is implemented.</li><li>When a push token is removed using the pushFcmRegisterationId("token",false) method. Applicable only for Android.</li></ul></li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <p>Control Group</p>            | <p>The event is tracked when a campaign is activated with a Control group.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <p>Channel Unsubscribed</p>     | <ul><li><p>The event is raised when an email is not acknowledged.</p></li><li><p>The following are the event properties:</p><ul><li>Campaign ID: This is the ID of<br>the campaign from which users are updating subscriptions.<br>Campaign Type: Currently only email.</li><li>Group: Group name from which the user unsubscribed/resubscribed.</li><li>Identity: The user identity/email address.</li><li>Variant Type: Valid values are bounced, dropped, and spam. Email IDs that bounce, drop or marked as spam are opted out from future emails</li><li>Subscription Type: Account level and profile level. Profile level signifies that the user who qualified for the communication is opted out. Account level signifies that all users with the email address are opted out from future communications.</li><li>Reason: Reason which was given by the email provider for the type of the error. For example: "smtp;550 5.1.1 The email account that you tried to reach does not exist. Please try double-checking the recipient's email address for typos or unnecessary spaces."</li></ul></li></ul> |
| <p>Reachable By</p>             | <p>The event is tracked for a profile when:</p><ul><li>Push token is added/changed.</li><li>Email ID is added/changed.</li><li>Phone number is added/changed.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <p>Notification Delivered</p>   | <p>The event is tracked when the WhatsApp provider confirms that the notification has reached the end user (double-tick of WhatsApp).</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <p>AB Experiment Rendered</p>   | <p>The event is tracked when you are using the Product A/B Tests feature and the variant reaches the device.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <p>AB Experiment Stopped</p>    | <p>The event is tracked when you are using the Product A/B Tests feature and the AB experiment is stopped.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <p>AB Experiment Rolled Out</p> | <p>The event is tracked when you are using the Product A/B Tests feature and the winner variant is sent to all the devices.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <p>Geocluster Entered</p>       | <p>The event is tracked when you enable the geofence feature and your device enters a geofence.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <p>Geocluster Exited</p>        | <p>The event is tracked when you enable the geofence feature and your device exits a geofence.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <p>Reply Sent</p>               | <p>The event is tracked against the user profile of the end user when an agent (CleverTap user) replies to a WhatsApp message from the end user.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <p>App Uninstalled</p>          | <ul><li><p>The event is tracked when the user uninstalls the application.</p></li><li><p>There are three cases when this event is tracked multiple times for a single user:</p><ul><li>The first case is when a user installs your app, uninstalls it, and then reinstalls it. </li><li>The second case is when a user clears the app's memory. </li><li>The third case is when a user installs your app on multiple devices.</li></ul></li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <p>Webhook Delivered</p>        | <p>The event is tracked when a webhook campaign is delivered successfully.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <p>State Transitioned</p>       | <ul><li>The event is tracked whenever a user transitions from one state to another or from an unmapped state to one of the states in the lifecycle optimization framework.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <p>UTM Visited</p>              | <ul><li>The event is tracked when a user clicks on a link from a marketing campaign that has a UTM parameter defined on it.</li><li>The event is also tracked when a CleverTap-integrated attribution platform, such as Branch or Apsalar, sends this information to CleverTap.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |

> 📘 Availability of Feature
> 
> If you are a _CleverTap for Enterprises_ user, contact your sales account manager to activate this feature at your end. It is available as a paid add-on for _CleverTap for Startups_ users.