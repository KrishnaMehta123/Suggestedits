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
[block:callout]
{
  "type": "info",
  "title": "Feature in Beta",
  "body": "This is a pre-release feature. If you are an Enterprise user and have any queries about the feature, contact CleverTap Customer Success Team. If you are a CleverTap for Startups user and have any queries about the feature, raise a ticket."
}
[/block]
# Overview

Mixpanel data export enables exporting your CleverTap event data to the Mixpanel dashboard.

[block:callout]
{
  "type": "info",
  "body": "Mixpanel supports the export of only 255 event properties per event. If the limit exceeds, CleverTap exports the first 255 event properties.",
  "title": "Export Limit Per Event"
}
[/block]
# Setup
The setup involves adding Mixpanel project details to the CleverTap dashboard. To add the project details:
1. Log in to your CleverTap account.
2. Navigate to *Settings* > *Partners* > *Exports*. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e39d8db-Unconnected_partners.png",
        "Unconnected partners.png",
        1924,
        1126,
        "#f6f7f9"
      ],
      "border": true
    }
  ]
}
[/block]
3. Click the **Mixpanel** icon under the *Unconnected partners* section. The Mixpanel page displays.
4. Enter the Mixpanel project details.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dbec96d-Mixpanel_project_details.png",
        "Mixpanel project details.png",
        1926,
        1084,
        "#f7f8fb"
      ],
      "border": true
    }
  ]
}
[/block]

[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "1-0": "Service Account Username",
    "1-1": "A descriptive name for the service account in Mixpanel. For more information, refer to [Service Account Username] (https://developer.mixpanel.com/reference/service-accounts#authenticating-with-a-service-account).",
    "2-0": "Service Account Secret",
    "2-1": "The secret API is the key that corresponds to your project. For more information, refer to [Service Account Secret] (https://developer.mixpanel.com/reference/service-accounts#authenticating-with-a-service-account).",
    "0-0": "Mixpanel Project ID",
    "0-1": "The Project token is used to send event data to Mixpanel. For more information, refer to [Project ID](https://help.mixpanel.com/hc/en-us/articles/115004490503-Project-Settings#project-id).",
    "3-0": "Data Residency",
    "3-1": "The physical/geographical storage location of a project's data (EU or Standard) at a project level (per project).\nFor more information, refer to [Data Residency](https://help.mixpanel.com/hc/en-us/articles/115004490503-Project-Settings#data-residency).",
    "4-0": "Mixpanel Distinct ID Mapping",
    "4-1": "This user property is used as an identifier when sending events data to Mixpanel. For more information, refer to [Distinct ID](https://help.mixpanel.com/hc/en-us/articles/115004509406-Distinct-IDs-)."
  },
  "cols": 2,
  "rows": 5
}
[/block]
5. Click **Save credentials**. On clicking, the following popup displays:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c3d85c6-Credentials_saved.png",
        "Credentials saved.png",
        1546,
        834,
        "#858687"
      ],
      "border": true
    }
  ]
}
[/block]
Mixpanel is now displayed under *Connected partners* when you navigate to  *Settings* > *Partners* > *Exports*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cd56b87-MIxpanel_Connected_partner_.png",
        "MIxpanel Connected partner .png",
        1924,
        1002,
        "#f5f6f8"
      ],
      "border": true
    }
  ]
}
[/block]
# Create New Export
To create a new export:
1. Navigate to *Settings* > *Partners* > *Exports*.
2. Navigate to the *Activity log* tab and then click **+ Create Export**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/82460f3-2020-11-12_09-13-32_Data_Export.png",
        "2020-11-12_09-13-32_Data Export.png",
        1316,
        344,
        "#f9faf9"
      ],
      "border": true,
      "sizing": "smart"
    }
  ]
}
[/block]
On clicking, the *Create new board* popup displays.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b7f5915-Create_New_Board_popup.png",
        "Create New Board popup.png",
        892,
        714,
        "#f7f9fb"
      ],
      "border": true,
      "sizing": "80"
    }
  ]
}
[/block]
3. Configure the settings as required. 
    * **Choose an export partner**: Select *Mixpanel* from the *Choose an export partner* list.
    * **Export details**: Select the events to export from the available options. For more information, refer to [Export Details](https://docs.clevertap.com/docs/mixpanel-export#export-details).
    * **Choose export frequency**: Select from one of the following options:
       * *One time*: Single export for the export type selected. You can export data up to the last 60 days. 
       * *Recurring*: Set up a recurring export that exports all the new events captured in the last window. You can export data as frequently as every 4 hours and up to once every 24 hours. 
[block:callout]
{
  "type": "info",
  "body": "If you are a Mixpanel enterprise customer and require a higher limit for a one-time backfill, contact [apis@mixpanel.com](mailto:apis@mixpanel.com) with your project_id and use-case.",
  "title": "Rate Limits"
}
[/block]
   
4. Click **Create export**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cbba146-Create_export.png",
        "Create export.png",
        838,
        670,
        "#f7f8fb"
      ],
      "border": true,
      "sizing": "smart"
    }
  ]
}
[/block]
On successful creation of export, the following message is displayed:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/db73cf0-Successful_export.png",
        "Successful export.png",
        1554,
        786,
        "#858687"
      ],
      "border": true
    }
  ]
}
[/block]
5. Click **Ok** to return to the *Exports* page.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c704d50-Export_created.png",
        "Export created.png",
        1916,
        1102,
        "#f3f4f6"
      ],
      "border": true
    }
  ]
}
[/block]
# Stop Export
You can also stop the export that you have created. To stop the current export:

1. Click the ![ellipses](https://files.readme.io/0210143-ellipses_icon.png) icon for the export request you want to stop and then click ![stop](https://files.readme.io/930e98c-Stop_icon.png). 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8ad4dae-Click_Stop.png",
        "Click Stop.png",
        2300,
        1130,
        "#f2f4f6"
      ],
      "border": true
    }
  ]
}
[/block]
You are prompted to confirm your action.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7117fac-Stop_export.png",
        "Stop export.png",
        1868,
        1008,
        "#848383"
      ],
      "border": true
    }
  ]
}
[/block]
2. Click **Yes, stop export** to stop the export request. On clicking, the following message displays:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1c7d3f3-Export_stopped_successfully.png",
        "Export stopped successfully.png",
        1874,
        1034,
        "#828384"
      ],
      "border": true
    }
  ]
}
[/block]
3. Click **Ok** to return to the *Exports *page.

# Export Details
Select from one of the following options to export events from CleverTap to the Mixpanel dashboard:
  
## All events 
Export data for all defined events including *System* and *Custom* events.
      
## Selected events
Select the specific events to export. 

## Engagement Events
Export the following engagement events:
[block:parameters]
{
  "data": {
    "h-0": "CleverTap Event Name",
    "h-1": "Description",
    "0-0": "Notification Sent",
    "1-0": "Notification Viewed",
    "2-0": "Notification Clicked",
    "3-0": "Push Impressions",
    "4-0": "Notification Replied",
    "5-0": "Push Unregistered",
    "6-0": "Control Group",
    "7-0": "Channel Unsubscribed",
    "8-0": "Reachable By",
    "9-0": "Notification Delivered",
    "10-0": "AB Experiment Rendered",
    "11-0": "AB Experiment Stopped",
    "12-0": "AB Experiment Rolled Out",
    "13-0": "Geocluster Entered",
    "14-0": "Geocluster Exited",
    "15-0": "Reply Sent",
    "16-0": "App Uninstalled",
    "17-0": "Webhook Delivered",
    "18-0": "State Transitioned",
    "19-0": "UTM Visited",
    "0-1": "* The event is tracked when the notification is successfully sent from CleverTap to the communication channel you select for your campaign. \n* This event is always recorded, even if the user does not open or click on the message. \n* This event is recorded for email, mobile push, SMS  and web push campaigns. \n* The event is available on the Event dashboard but it is not displayed on the User Profile.",
    "1-1": "* The event is tracked when a user views an email, in-app notification, or a web notification sent from CleverTap.\n* The event is available for email, web push, in-app, web popup, and app inbox.",
    "2-1": "The event is tracked when a user clicks on a mobile push, in-app, email, web-popup, or web push message sent via the CleverTap dashboard or through the campaign API.",
    "3-1": "* After the toggle for Push Impressions is turned on/setup from settings, the CleverTap SDK starts recording an event whenever a push notification sent via CleverTap is delivered to the user’s device.\n* The funnels on the Push campaign statistics page reflects the count for this event.",
    "4-1": "This event is tracked when the brand receives a reply from the user for WhatsApp.",
    "5-1": "* This debug event is tracked when an existing mobile push token is removed for a profile.\n\n* The event is tracked for a profile when:\n\n  * A user logs out of the device and another user logs in. Applicable only if the onUserLogin() method is implemented.\n  * When a push token is removed using the pushFcmRegisterationId(\"token\",false) method. Applicable only for Android.",
    "6-1": "The event is tracked when a campaign is activated with a Control group.",
    "7-1": "* The event is raised when an email is not acknowledged.\n\n* The following are the event properties:\n  * Campaign ID: This is the ID of\nthe campaign from which user are updating subscriptions.\nCampaign Type: Currently only email.\n  * Group: Group name from which the user unsubscribed/resubscribed.\n  * Identity: The user identity/email address.\n  * Variant Type: Valid values are bounced, dropped, and spam. Email IDs which bounce, drop or marked as spam are opted out from future emails\n  * Subscription Type: Account level and profile level. Profile level signifies that the user who qualified for the communication is opted out. Account level signifies that all users with the email address are opted out from future communications.\n  * Reason: Reason which was given by the email provider for the type of the error. For example: \"smtp;550 5.1.1 The email account that you tried to reach does not exist. Please try double-checking the recipient's email address for typos or unnecessary spaces.\"",
    "8-1": "The event is tracked for a profile when:\n   * Push token is added/changed.\n   * Email ID is added/changed.\n   * Phone number is added/changed.",
    "9-1": "The event is tracked when the WhatsApp provider confirms that the notification has reached the end user (double-tick of WhatsApp).",
    "10-1": "The event is tracked when you are using the Product A/B Tests feature and the variant reaches the device.",
    "11-1": "The event is tracked when you are using the Product A/B Tests feature and the AB experiment is stopped.",
    "12-1": "The event is tracked when you are using the Product A/B Tests feature and the winner variant is sent to all the devices.",
    "13-1": "The event is tracked when you enable the geofence feature and your device enters a geofence.",
    "14-1": "The event is tracked when you enable the geofence feature and your device exits a geofence.",
    "15-1": "The event is tracked against the user profile of the end user when an agent (CleverTap user) replies to a WhatsApp message from the end user.",
    "16-1": "* The event is tracked when the user uninstalls the application.\n\n* There are three cases when this event is tracked multiple times for a single user:\n  * The first case is when a user installs your app, uninstalls it, and then reinstalls it. \n  * The second case is when a user clears the app's memory. \n  * The third case is when a user installs your app on multiple devices.",
    "17-1": "The event is tracked when a webhook campaign is delivered successfully.",
    "18-1": "* The event is tracked whenever a user transitions from one state to another or from unmapped to one of the states in the lifecycle optimization framework.",
    "19-1": "* The event is tracked when a user clicks on a link from a marketing campaign that has a UTM parameter defined on it.\n* The event is also tracked when a CleverTap-integrated attribution platform, such as Branch or Apsalar, sends this information to CleverTap.",
    "h-2": "",
    "0-2": "",
    "1-2": "",
    "2-2": "",
    "3-2": "",
    "4-2": "",
    "5-2": "",
    "7-2": "",
    "8-2": "",
    "9-2": "",
    "10-2": "",
    "11-2": "",
    "12-2": "",
    "13-2": "",
    "14-2": "",
    "15-2": "",
    "16-2": "",
    "18-2": "",
    "19-2": "",
    "6-2": "",
    "17-2": ""
  },
  "cols": 2,
  "rows": 20
}
[/block]

[block:callout]
{
  "type": "info",
  "body": "This feature is available only for the Enterprise plan. Contact your sales account manager to activate it.",
  "title": "Availability of Feature"
}
[/block]