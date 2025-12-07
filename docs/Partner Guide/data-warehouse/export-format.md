---
title: Export Format
excerpt: ''
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

This document provides information about the file format and the name format of the files exported to different Data-Warehouse partners.

# Event Export

# File Name Format

The example below shows the file name format for event export:

```text
<export request id>-<timestamp of the export run>-<event name>-<yyyymmdd>-<file index>-<database-id>.json
```

- _Export request ID_: Indicates the export request ID generated when you create a request in the CleverTap dashboard.
- _Timestamp of export run_: Indicates the time when the export was run in EPOCH format.
- _Event name_: Indicates the event type included in the file. For example, the _Charged_ event. 
- _File index_: Larger data exports are split into several files. We limit file records to 1,000 K event exports per file.
- _Database ID_: Indicates the database ID of the CleverTap from where the file was exported. 
- _File format_: Indicates the file format exported to the S3 bucket. For instance, CSV file format will be as .csv.gzip

## File Data Format

### Event Export Schema

[block:parameters]
{
  "data": {
    "h-0": "Key",
    "h-1": "Sub-Headers",
    "h-2": "Description",
    "0-0": "ts",
    "0-1": "",
    "0-2": "Indicates the time when the event occurred. [Need to add format] ",
    "1-0": "eventName",
    "1-1": "",
    "1-2": "Indicates the name of the exported event. ",
    "2-0": "profile",
    "2-1": "",
    "2-2": "Includes the profile properties of the user who performed the event.",
    "3-0": "",
    "3-1": "profile.identity",
    "3-2": "Denotes the identity of the user. We will add the details as per the identity priorities set while creating the export. For more information, refer to [Prioritize User Identity for Exports](https://docs.clevertap.com/docs/data-export-to-aws-s3#prioritize-user-identity-for-exports).",
    "4-0": "",
    "4-1": "profile.objectId ",
    "4-2": "Denotes the CleverTap ID of the user. This data is not exported by default. to export this information, contact your CSM or raise a support ticket.",
    "5-0": "",
    "5-1": "profile.all_identities ",
    "5-2": "Denotes all the unique identities of the user present on the CleverTap.",
    "6-0": "",
    "6-1": "profile.platform ",
    "6-2": "Denotes the platform from which they have raised the event.",
    "7-0": "",
    "7-1": "profile.phone",
    "7-2": "Denotes the phone number of the user, if present.",
    "8-0": "",
    "8-1": "profile.name ",
    "8-2": "Denotes the name of the user.",
    "9-0": "",
    "9-1": "profile.email ",
    "9-2": "Denotes the email address of the user.",
    "10-0": "",
    "10-1": "profile.push_token",
    "10-2": "<li> Indicates the device token.</li>  \n<li> It is present if the user raises an event through the device having a token associated with it.</li>",
    "11-0": "deviceInfo",
    "11-1": "",
    "11-2": "",
    "12-0": "",
    "12-1": "deviceInfo.make",
    "12-2": "Denotes the make of the user device through which the event is raised.",
    "13-0": "",
    "13-1": "deviceInfo.model ",
    "13-2": "Denotes the model of the user device through which the event is raised.",
    "14-0": "",
    "14-1": "deviceInfo.appVersion ",
    "14-2": "Denotes the application version of the user device through which the event is raised",
    "15-0": "",
    "15-1": "deviceInfo.sdkVersion ",
    "15-2": "Denotes the CleverTap SDK version installed on the user device through which the event is raised.",
    "16-0": "",
    "16-1": "deviceInfo.osVersion ",
    "16-2": "Denotes the OS version of the user device through which the event is raised.",
    "17-0": "",
    "17-1": "deviceInfo.browser ",
    "17-2": "Denotes the Browser (for example, Chrome, Firefox, etc.) on the user device through which the event is raised.",
    "18-0": "",
    "18-1": "deviceInfo.dpi ",
    "18-2": "Denotes the DPI of the user device through which the event is raised.",
    "19-0": "",
    "19-1": "deviceInfo.dimensions.width  ",
    "19-2": "Denotes the width of the user device through which the event is raised.",
    "20-0": "",
    "20-1": "deviceInfo.dimensions.height ",
    "20-2": "Denotes the height of the user device through which the event is raised.",
    "21-0": "",
    "21-1": "deviceInfo.dimensions.unit",
    "21-2": "Indicates the unit of measure for user device dimensions through which the event is raised. For example, px (pixels), etc. ",
    "22-0": "controlGroupName",
    "22-1": "",
    "22-2": "Only present for the **Custom control group **event export. The custom control group will have a name associated with it in the control group name column. If the column does not have any name in it, that entry is for the Campaign/Journey control group",
    "23-0": "eventProps",
    "23-1": "",
    "23-2": "Indicates the properties of the event raised by the user. For more information, refer to Event Properties.",
    "24-0": "sessionProps",
    "24-1": "",
    "24-2": "Includes the properties only for _UTM Visited_ events."
  },
  "cols": 3,
  "rows": 25,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


## Event Properties

### Notification Sent

This event is tracked when a message is sent to a user. This event is recorded for Mobile Push, Web Push, App Inbox, Email, SMS, WhatsApp, and Remarketing Channel campaigns. It is available under the _Event_ page on the dashboard but not displayed under the user profile.

[block:parameters]
{
  "data": {
    "h-0": "Keys",
    "h-1": "Description",
    "0-0": "eventProps.Campaign id",
    "0-1": "**For Recurring Campaign**:  \nThe value is always the CampaignID_eventtimestamp. This can help you to identify on which day users receive notifications from the campaign.  \nFormat = campaignID_YYYYMMDD  \n  \n**For Trigger Campaign**:  \nThe value is always the Campaign ID_timestamp. The timestamp is in EPOCH format, representing time in seconds. This can help you to identify when the users received these notifications from the campaign.  \nFormat = campaignID_EpochTS  \n  \n**For One Time Campaign**:  \nThe value is always Campaign ID and is unique since it was sent only once time -  \nFormat = campaignID",
    "1-0": "eventProps.Campaign type",
    "1-1": "Contains the type of campaign. For example, Push, Email, etc.",
    "2-0": "eventProps.Campaign name",
    "2-1": "Contains the name of the campaign. For example, Black Friday Sales, New Year Sales, and so on.",
    "3-0": "eventProps.Variant",
    "3-1": "Contains the campaign variants created for A/B Testing. For example, Variant A, Variant B, Variant C, etc.",
    "4-0": "eventProps.Campaign labels",
    "4-1": "Contains the labels added for the campaign. For example, Diwali Offer, New User Offer, and so on.",
    "5-0": "eventProps.Journey id",
    "5-1": "Helps uniquely identify the journey in which the campaign is present."
  },
  "cols": 2,
  "rows": 6,
  "align": [
    "left",
    "left"
  ]
}
[/block]


### Notification Viewed

This event is tracked when a user views an Email, SMS, In-App notification, App Inbox, Web notification or WhatsApp sent from the CleverTap dashboard.

[block:parameters]
{
  "data": {
    "h-0": "Keys",
    "h-1": "Description",
    "0-0": "eventProps.wzrk_id",
    "0-1": "Ignore this field. To get details, refer to **eventProps.Campaign id**",
    "1-0": "eventProps.wzrk_animated",
    "1-1": "",
    "2-0": "eventProps.wzrk_pivot",
    "2-1": "Indicates the campaign variants created for A/B Testing.",
    "3-0": "eventProps.wzrk_ttl",
    "3-1": "Indicates the time to live for the campaign.  \n(check for web channel, whatsapp - if available?)",
    "4-0": "eventProps.wzrk_acct_id",
    "4-1": "Indicates the CleverTap Account ID.",
    "5-0": "eventProps.wzrk_pid",
    "5-1": "Ignore this field. To get details, refer to **eventProps.Campaign id**",
    "6-0": "eventProps.wzrk_rnv",
    "6-1": "If present then the Notification Viewed event will be raised",
    "7-0": "eventProps.wzrk_pn",
    "7-1": "If present then it indicates that the notification is sent from the CleverTap dashboard ",
    "8-0": "eventProps.Campaign type",
    "8-1": "Indicates the CleverTap campaign type. For example, Push, Web Push, Webhook, etc.",
    "9-0": "eventProps.wzrk_cid",
    "9-1": "Indicates the channel ID.",
    "10-0": "eventProps.wzrk_bc",
    "10-1": "Indicates the badge count.",
    "11-0": "eventProps.wzrk_bi",
    "11-1": "Indicates the badge icon. ",
    "12-0": "eventProps.wzrk_dl",
    "12-1": "Indicates if the campaign includes a deep link URL.",
    "13-0": "eventProps.wzrk_acts",
    "13-1": "Indicates the action button payload.",
    "14-0": "eventProps.wzrk_bp",
    "14-1": "Indicates the Image URL included in the notification.",
    "15-0": "eventProps.CTSource",
    "15-1": "Indicates the mobile phone or desktop on which the user viewed the notification.",
    "16-0": "eventProps.CTLatitude",
    "16-1": "Indicates the last known latitude captured by CleverTap on launching the application.",
    "17-0": "eventProps.CTLongitude",
    "17-1": "Indicates the last known longitude captured by CleverTap on launching the application.",
    "18-0": "eventProps.wzrk_c2a",
    "18-1": "<li> Indicates the value of the button clicked by the user. </li>  \n<li> This button can be present for the following campaign types: In-App, App Inbox or Email </li>",
    "19-0": "eventProps.browser",
    "19-1": "Indicates the browser of the device. ",
    "20-0": "eventProps.CT Session Id",
    "20-1": "Indicates the CleverTap Session ID. ",
    "21-0": "eventProps.User Agent",
    "21-1": "Indicates the agents where the email was viewed. For example, Mozilla Firefox. More reference: <https://docs.clevertap.com/docs/track-email#track-client-names>",
    "22-0": "eventProps.Client Name",
    "22-1": "Indicates the client where the email was viewed. For example, Gmail. Reference: <https://docs.clevertap.com/docs/track-email#track-client-names>",
    "23-0": "eventProps.skipTCM",
    "23-1": "Available if the message was sent from autoresponders or agent chat. The following are the values for this key: True or False. ",
    "24-0": "eventProps.Campaign id",
    "24-1": "**For Recurring Campaign**:  \nThe value is always the CampaignID_eventtimestamp. This can help you to identify on which day users receive notifications from the campaign.  \nFormat = campaignID_YYYYMMDD  \n  \n**For Trigger Campaign**:  \nThe value is always the Campaign ID_timestamp. The timestamp is in EPOCH format, representing time in seconds.. This can help you to identify when the users received these notifications from the campaign.  \nFormat = campaignID_EpochTS  \n  \n**For One Time Campaign**:  \nThe value is always Campaign ID and is unique since it was sent only once time -  \nFormat = campaignID",
    "25-0": "eventProps.Variant",
    "25-1": "Contains the campaign variants created for A/B Testing. For example, Variant A, Variant B, Variant C, etc.",
    "26-0": "eventProps.ct_sdk_version",
    "26-1": "The app uses the CleverTap SDK version when an event is raised. For example, 30501.",
    "27-0": "eventProps.ct_os_version",
    "27-1": "The operating system of the device. For example, 1.0.0.",
    "28-0": "eventProps.ct_app_version",
    "28-1": "This is the current version of your application installed on the user's device.",
    "29-0": "eventProps.ct_connected_to_wifi",
    "29-1": "Status of Wi-Fi on the device when the event is raised. The possible values are True or False.",
    "30-0": "eventProps.ct_network_carrier",
    "30-1": "The network carrier of the device. For example, AT&T, Vodafone, etc.",
    "31-0": "eventProps.ct_network_type",
    "31-1": "The network type of the device. For example, 4G.",
    "32-0": "eventProps.ct_bluetooth_version",
    "32-1": "The Bluetooth version of the device.",
    "33-0": "eventProps.ct_bluetooth_enabled",
    "33-1": "Indicates if Bluetooth is enabled on the device.",
    "34-0": "eventProps.mimeType",
    "34-1": "This property helps you understand the performance of your AMP emails. For more information, refer to [Email Campaigns](doc:ampforemail#amp-for-email-campaign-stats).",
    "35-0": "eventProps.Campaign name",
    "35-1": "Indicates the name of the campaign.",
    "36-0": "eventProps.Campaign labels",
    "36-1": "Indicates the labels added for the campaign",
    "37-0": "eventProps.Journey id",
    "37-1": "Helps uniquely identify the journey in which the campaign is present. This is recorded only if the campaign is part of any journey."
  },
  "cols": 2,
  "rows": 38,
  "align": [
    "left",
    "left"
  ]
}
[/block]


### Notification Clicked

This event is tracked only when a user clicks on the message sent via CleverTap.

[block:parameters]
{
  "data": {
    "h-0": "Keys",
    "h-1": "Description",
    "0-0": "eventProps.Campaigntype",
    "0-1": "Indicates the CleverTap campaign type. For example, Push, Web Push, Webhook, etc.",
    "1-0": "eventProps.wzrk_pivot",
    "1-1": "Indicates the campaign variants created for A/B Testing.",
    "2-0": "eventProps.wzrk_bi",
    "2-1": "Indicates the badge icon.",
    "3-0": "eventProps.wzrk_ttl",
    "3-1": "Indicates the time to live for the campaign.",
    "4-0": "eventProps.wzrk_bc",
    "4-1": "Indicates the badge count.",
    "5-0": "eventProps.wzrk_dt",
    "5-1": "Indicates the service used to send the message. For example, Firebase, etc.",
    "6-0": "eventProps.wzrk_id",
    "6-1": "**For Recurring Campaign**:  \nThe value is always the CampaignID_eventtimestamp. This can help you to identify on which day users receive notifications from the campaign.  \nFormat = campaignID_YYYYMMDD  \n  \n**For Trigger Campaign**:  \nThe value is always the Campaign ID_timestamp. The timestamp is in EPOCH format, representing time in seconds.. This can help you to identify when the users received these notifications from the campaign.  \nFormat = campaignID_EpochTS  \n  \n**For One Time Campaign**:  \nThe value is always Campaign ID and is unique since it was sent only once time -  \nFormat = campaignID",
    "7-0": "eventProps.CTSource",
    "7-1": "Indicates the mobile phone or desktop on which the user viewed the notification. (@parth: pls check the explanation.)",
    "8-0": "eventProps.wzrk_cid",
    "8-1": "Indicates the Channel ID.",
    "9-0": "eventProps.wzrk_push_amp",
    "9-1": "<li> Accepts the following boolean value: true or false</li>  \n<li> If true, indicates that the notification is rendered through Push amplification. </li>",
    "10-0": "eventProps.wzrk_pn",
    "10-1": "Indicates that the notification is sent from the CleverTap dashboard when present.",
    "11-0": "eventProps.wzrk_pid",
    "11-1": "Ignore this field. To get details, refer to **eventProps.Campaign id**",
    "12-0": "eventProps.wzrk_bp",
    "12-1": "Indicates the Image URL included in the notification.",
    "13-0": "eventProps.wzrk_acct_id",
    "13-1": "Indicates the CleverTap Account ID.",
    "14-0": "eventProps.wzrk_rnv",
    "14-1": "<li> A flag that indicates if the Notification Clicked event is raised. </li>  \n<li> If present and not empty, it indicates that the Notification Viewed event was raised. </li>",
    "15-0": "eventProps.CTAppVersion",
    "15-1": "This is the current version of your application installed on the user's device.",
    "16-0": "eventProps.wzrk_ck",
    "16-1": "Indicates whether the collapse key is present or not",
    "17-0": "eventProps.wzrk_ttl_s",
    "17-1": "Indicates the time-to-live for the campaign in seconds.",
    "18-0": "eventProps.wzrk_dl",
    "18-1": "Contains Deep Link URL",
    "19-0": "eventProps.wzrk_mutable_content",
    "19-1": "<li> Captured for iOS push notification. </li>  \n<li> Value is 1 if enabled and 0 if disabled. </li>  \n(@Parth: what does this property indicate?) ",
    "20-0": "eventProps.wzrk_collapsible",
    "20-1": "Indicates the Collapse key (the actual key which you have provided).",
    "21-0": "eventProps.wzrk_st",
    "21-1": "Content of the subtitle added in the push notification",
    "22-0": "eventProps.wzrk_nms",
    "22-1": "Indicates the summary text when sending push notifications.",
    "23-0": "eventProps.wzrk_sound",
    "23-1": "A boolean flag that indicates if the custom sound is to be played when the push notification is rendered on the device",
    "24-0": "eventProps.wzrk_acts",
    "24-1": "Indicates the action button payload.",
    "25-0": "eventProps.wzrk_c2a",
    "25-1": "<li> Indicates the value of the button clicked by the user. </li>  \n<li> This button can be present for the following campaign types: In-App, Push, or Mobile In-Box. </li>",
    "26-0": "eventProps.wzrk_c2a_short_url",
    "26-1": "Indicates the short URL on which the customer clicked (available only for SMS and WhatsApp). It is available only if you use CleverTap's Click Tracking feature.",
    "27-0": "eventProps.mimeType",
    "27-1": "Helps understand the performance of the AMP emails. For more information, refer to [Email Campaigns](doc:ampforemail#amp-for-email-campaign-stats).",
    "28-0": "eventProps.Campaign name",
    "28-1": "Indicates the name of the campaign.",
    "29-0": "eventProps.Campaign labels",
    "29-1": "Indicates the labels added for the campaign.",
    "30-0": "eventProps.Journey id",
    "30-1": "Uniquely identifies the journey in which the campaign is present. This is recorded only if the campaign is part of any journey.",
    "31-0": "eventProps.Variant",
    "31-1": "Contains the campaign variant name created for A/B Testing. For example, Variant A, Variant B, Variant C, etc.",
    "32-0": "eventProps.wzrk_slideNo",
    "32-1": "",
    "33-0": "eventProps.wzrk_click_innerText",
    "33-1": "",
    "34-0": "eventProps.wzrk_click_c2a",
    "34-1": "",
    "35-0": "eventProps.wzrk_acct_id",
    "35-1": "Indicates the CleverTap Account ID.",
    "36-0": "eventProps.wzrk_bpds",
    "36-1": "",
    "37-0": "eventProps.wzrk_interruption_level",
    "37-1": "",
    "38-0": "eventProps.wzrk_relevance_score",
    "38-1": ""
  },
  "cols": 2,
  "rows": 39,
  "align": [
    "left",
    "left"
  ]
}
[/block]


### Push Impression

This event is raised when a push notification is rendered on the device.

[block:parameters]
{
  "data": {
    "h-0": "Key",
    "h-1": "Description",
    "0-0": "eventProps.wzrk_acct_id",
    "0-1": "Indicates the CleverTap Account ID.",
    "1-0": "eventProps.wzrk_pivot",
    "1-1": "Indicates the campaign variants created for A/B Testing.",
    "2-0": "eventProps.wzrk_cid",
    "2-1": "Indicates the Channel ID.",
    "3-0": "eventProps.wzrk_pid",
    "3-1": "@Parth: Please provide input.]",
    "4-0": "eventProps.wzrk_rnv",
    "4-1": "<li> A flag that indicates if the Notification Viewed event is raised. </li><li> If present and not empty, it indicates that the Notification Viewed event was raised. </li>",
    "5-0": "eventProps.wzrk_ttl",
    "5-1": "Indicates the time-to-live for the campaign",
    "6-0": "eventProps.wzrk_bc",
    "6-1": "Indicates the batch count.",
    "7-0": "feventProps.wzrk_bi",
    "7-1": "Indicates the badge icon. (@parth: Is it batch or badge?)",
    "8-0": "eventProps.wzrk_id",
    "8-1": "Indicates the Campaign ID.",
    "9-0": "eventProps.wzrk_pn",
    "9-1": "Indicates that the notification is sent from the CleverTap dashboard when present.",
    "10-0": "eventProps.Campaign type",
    "10-1": "Indicates the CleverTap campaign type. For example, Push, Web Push, Webhook, etc.",
    "11-0": "eventProps.wzrk_sound",
    "11-1": "A boolean flag that indicates if the custom sound is to be played when the (@Parth: When is this custom sound played?)",
    "12-0": "eventProps.wzrk_acts",
    "12-1": "Indicates the action button payload.",
    "13-0": "eventProps.wzrk_bp",
    "13-1": "Indicates the Image URL included in the notification.",
    "14-0": "eventProps.wzrk_dl",
    "14-1": "Indicates if the campaign includes a deep link (@Parth: Is the explanation correct?)",
    "15-0": "eventProps.wzrk_ck",
    "15-1": "Indicates the collapse key.",
    "16-0": "eventProps.CTAppVersion",
    "16-1": "Indicates the Application version",
    "17-0": "eventProps.CTSource",
    "17-1": "Indicates the source of the event i.e., Mobile, Desktop, etc.",
    "18-0": "eventProps.CTLatitude",
    "18-1": "Indicates the last known latitude captured by CleverTap on launching the application.",
    "19-0": "eventProps.CTLongitude",
    "19-1": "Indicates the last known longitude captured by CleverTap on launching the application.",
    "20-0": "eventProps.wzrk_push_amp",
    "20-1": "<li> Accepts the following boolean value: true or false</li>  \n<li> If true, indicates that the notification is rendered through Push Amplification. </li>  \n(@parth: Should we use the push amp term here - we are not using that term anymore.)",
    "21-0": "eventProps.wzrk_dt",
    "21-1": "Indicates the service used to send the message. For example, Firebase, etc.",
    "22-0": "eventProps.wzrk_ttl_s",
    "22-1": "Indicates the time to live for the campaign in seconds.",
    "23-0": "eventProps.wzrk_st",
    "23-1": "Indicates the subtitle ",
    "24-0": "eventProps.Campaign name",
    "24-1": "Indicates the name of the campaign.",
    "25-0": "eventProps.Campaign labels",
    "25-1": "Indicates the labels added for the campaign.",
    "26-0": "eventProps.Journey id",
    "26-1": "Uniquely identifies the journey in which the campaign is present. This is recorded only if the campaign is part of any journey.",
    "27-0": "eventProps.wzrk_interruption_level",
    "27-1": "",
    "28-0": "eventProps.wzrk_relevance_score",
    "28-1": "",
    "29-0": "eventProps.wzrk_cts",
    "29-1": "",
    "30-0": "eventProps.ct_os_version",
    "30-1": "The operating system of the device. For example, 1.0.0.",
    "31-0": "eventProps.ct_app_version",
    "31-1": "This is the current version of your application installed on the user's device.",
    "32-0": "eventProps.ct_sdk_version",
    "32-1": "The CleverTap SDK version used by the app when an event is raised. For example, 30501.",
    "33-0": "eventProps.ct_network_carrier",
    "33-1": "The network carrier of the device. For example, AT&T, Vodafone, etc.",
    "34-0": "eventProps.Campaign type",
    "34-1": "Indicates the CleverTap campaign type. For example, Push, Web Push, Webhook, etc.",
    "35-0": "eventProps.Variant",
    "35-1": "Contains the campaign variants created for A/B Testing. For example, Variant A, Variant B, Variant C, etc.",
    "36-0": "eventProps.wzrk_id",
    "36-1": "Indicates the Campaign ID."
  },
  "cols": 2,
  "rows": 37,
  "align": [
    "left",
    "left"
  ]
}
[/block]


### Notification Replied

This event is raised when a user replies to any WhatsApp campaign. (@Parth: this will be applicable for both WhatsApp and SMS - pls comfirm.)

[block:parameters]
{
  "data": {
    "h-0": "Key",
    "h-1": "Description",
    "0-0": "eventProps.CTSource",
    "0-1": "Indicates the WhatsApp provider that received the message",
    "1-0": "eventProps.wzrk_id",
    "1-1": "Indicates the campaign ID and batch ID  of the WhatsApp campaign sent to the user.  \n(@Parth: should we say \"campaign ID & Batch ID of the SMS & WhatsApp campaign?)",
    "2-0": "eventProps.Incoming message type",
    "2-1": "Indicates the type of message received from the user.",
    "3-0": "eventProps.Incoming text",
    "3-1": "Indicates the incoming text received from the user.",
    "4-0": "eventProps.Destination WABA number",
    "4-1": "Indicates the Business Phone number that received the incoming message.",
    "5-0": "eventProps.Source WABA number",
    "5-1": "Indicates the end user's number that sent the message.",
    "6-0": "eventProps.wzrk_pivot",
    "6-1": "Indicates the message variant of the last campaign delivered to the end user.",
    "7-0": "eventProps.Campaign type",
    "7-1": "Indicates the CleverTap campaign type. For example, Push, Web Push, Webhook, etc.",
    "8-0": "eventProps.Campaign name",
    "8-1": "Indicates the name of the campaign.",
    "9-0": "eventProps.Variant",
    "9-1": "Indicates the message variant of the last campaign delivered to the end user.",
    "10-0": "eventProps.Incoming media URL",
    "10-1": "Indicates the incoming media URL in case the customers have sent a media.",
    "11-0": "eventProps.Lat",
    "11-1": "Indicates the Latitude of the location if the customer has sent a location.",
    "12-0": "eventProps.Long",
    "12-1": "Indicates the Longitude of the location if the customer has sent a location.",
    "13-0": "eventProps.QR Paylolad",
    "13-1": "Indicates the custom payload of the quick reply button that the customer clicked.",
    "14-0": "eventProps.Campaign labels",
    "14-1": "Indicates the label of the last campaign sent to the user",
    "15-0": "eventProps.Message Id",
    "15-1": "Message ID to last campaign sent to the end user (applicable in case of the message via identity API)",
    "16-0": "eventProps.Journey id",
    "16-1": "Uniquely identifies the journey in which the campaign is present. This is recorded only if the campaign is part of any journey.",
    "17-0": "eventProps.Variant",
    "17-1": "Indicates the message variant of the last campaign delivered to the end user."
  },
  "cols": 2,
  "rows": 18,
  "align": [
    "left",
    "left"
  ]
}
[/block]


### Notification Delivered

This event is captured when messages get delivered to the user's WhatsApp. (Raised only for WhatsApp).  
(@Parth: Should we modify it to say - raised for both SMS and WhatsApp?)

[block:parameters]
{
  "data": {
    "h-0": "Key",
    "h-1": "Description",
    "0-0": "eventProps.Campaign type",
    "0-1": "Indicates the CleverTap campaign type. For example, Push, Web Push, Webhook, etc.",
    "1-0": "eventProps.CT Source",
    "1-1": "Indicates the WhatsApp provider that was used to send the campaign.",
    "2-0": "eventProps.wzrk_id",
    "2-1": "Indicates the WhatsApp campaign's ID and batch ID sent to the user.  \n(@Parth: should we say \"campaign ID & Batch ID of the SMS & WhatsApp campaign?)",
    "3-0": "eventProps.wzrk_pivot",
    "3-1": "Indicates the message variant of the campaign delivered to the end user.",
    "4-0": "events props.skipTCM",
    "4-1": "Available if the message was sent from autoresponders or agent chat. The following are the values for this key: True or False.",
    "5-0": "eventProps.pivot_index",
    "5-1": "Indicates the message variant of the campaign delivered to the end user.",
    "6-0": "eventProps.Message Id",
    "6-1": "Message ID of the campaign sent to the end user (applicable in case of the message via identity API)",
    "7-0": "eventProps.Campaign name",
    "7-1": "Indicates the name of the campaign sent to the user.",
    "8-0": "eventProps.Campaign labels",
    "8-1": "Indicates the labels added for the campaign sent to the user.",
    "9-0": "eventProps.Journey id",
    "9-1": "Uniquely identifies the journey in which the campaign is present.",
    "10-0": "eventProps.Campaign type",
    "10-1": "Indicates the CleverTap campaign type. For example, Push, Web Push, Webhook, etc.",
    "11-0": "eventProps.Variant",
    "11-1": "Indicates the message variant of the last campaign delivered to the end user.",
    "12-0": "eventProps.Campaign id",
    "12-1": "Indicates the ID of the last campaign sent to the user."
  },
  "cols": 2,
  "rows": 13,
  "align": [
    "left",
    "left"
  ]
}
[/block]


### Reply Sent

This event is recorded when an agent (CleverTap user) replies to a message from the end user.

| Key                      | Description                                                                                                                                                                                                                                                                                                                                                            |
| :----------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| eventProps.Campaign type | Indicates the communication channel where this reply was sent.                                                                                                                                                                                                                                                                                                         |
| eventProps.Campaign id   | Indicates the ID of the last WhatsApp campaign sent to the user.                                                                                                                                                                                                                                                                                                       |
| eventProps.CT Source     | <p>The source of the event.</p><p>For example, the event may originate from a Mobile SDK or an API.</p><p>All possible values:</p><ul><li>Mobile (Mobile SDK)</li><li>MobileWeb (Web SDK)</li><li>Web (Web SDK)</li><li>API</li><li>segment</li><li>appsflyer</li><li>apsalar</li><li>branch</li><li>tune</li><li>System (for events generated by CleverTap)</li></ul> |

### App Installed

This event is recorded when the user installs the application.

[block:parameters]
{
  "data": {
    "h-0": "Key",
    "h-1": "Description",
    "0-0": "eventProps.ct_app_version",
    "0-1": "This is the current version of your application installed on the user's device.  \n(@Parth: How is it different from eventProps.CTApp Version mentioned under Push Impression)",
    "1-0": "eventProps.CTSource",
    "1-1": "Indicates the source of the event, i.e. Mobile, Desktop, etc.",
    "2-0": "eventProps.ct_latitude",
    "2-1": "Indicates the last known latitude captured by CleverTap on launching the application. (@Parth: How is it different from eventProps.CTLatitude mentioned under Push Impression?)",
    "3-0": "eventProps.ct_longitude",
    "3-1": "Indicates the last known longitude captured by CleverTap on launching the application. (@Parth: How is it different from eventProps.CTLongitude mentioned under Push Impression)"
  },
  "cols": 2,
  "rows": 4,
  "align": [
    "left",
    "left"
  ]
}
[/block]


### App Launched

This event is recorded every time the user launches the application.

| Key                             | Description                                                                                                  |
| :------------------------------ | :----------------------------------------------------------------------------------------------------------- |
| eventProps.CTNetworkCarrier     | Indicates the network carrier for the user's device.                                                         |
| eventProps.CTSource             | Indicates the source of the event i.e. Mobile, Desktop, etc.                                                 |
| eventProps.CTBluetoothVersion   | Indicates the Bluetooth version of the user's device.                                                        |
| eventProps.CTSDKVersion         | Indicates CleverTap SDK version which is used (@parth: where is the SDK version used?)                       |
| eventProps.CT BluetoothEnabled  | Indicates if Bluetooth is enabled for the user's device.                                                     |
| eventProps.CTOSVersion          | Indicates the OS version of the user's device.                                                               |
| eventProps.CTNetworkType        | Indicates the type of network being used on the user's device. For example, Wifi, 4G, etc.                   |
| eventProps.Model                | Indicates the model of the user's device.                                                                    |
| eventProps.CT Longitude         | Indicates the last known longitude captured by CleverTap on launching the application.                       |
| eventProps.CT Latitude          | Indicates the last known latitude captured by CleverTap on launching the application.                        |
| eventProps.CTConnectedToWiFi    | Indicates if the user's device is connected to Wifi.                                                         |
| eventProps.CT Session Id        | Indicates the CleverTap session ID. (@parth: need more information here.)                                    |
| eventProps.CTAppVersion         | Indicates the version of the application installed on the user's device. (@parth: check if this is correct.) |
| eventProps.ct_sdk_version       | CT SDK version used by the app when an event is raised.                                                      |
| eventProps.ct_app_version       | This is the current version of your application installed on the user's device.                              |
| eventProps.ct_os_version        | The operating system of the device. For example, 1.0.0.                                                      |
| eventProps.ct_network_carrier   | The network carrier of the device. For example, AT&T, Vodafone, etc.                                         |
| eventProps.ct_first_time        |                                                                                                              |
| eventProps.ct_latitude          | Indicates the last known latitude captured by CleverTap.                                                     |
| eventProps.ct_longitude         | Indicates the last known longitude captured by CleverTap.                                                    |
| eventProps.ct_connected_to_wifi | Status of Wi-Fi on the device when the event is raised. The possible values are True or False.               |
| eventProps.ct_network_type      | The network type of the device. For example, 4G.                                                             |
| eventProps.ct_bluetooth_version | The Bluetooth version of the device.                                                                         |
| eventProps.ct_bluetooth_enabled | Indicates if Bluetooth is enabled on the device.                                                             |

### App Uninstalled

This event is recorded every time the user uninstalls the application.

| Key                    | Description                                                                                                                                                                                                                                                                                                                                                            |
| :--------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| eventProps.CT Source   | <p>The source of the event.</p><p>For example, the event may originate from a Mobile SDK or an API.</p><p>All possible values:</p><ul><li>Mobile (Mobile SDK)</li><li>MobileWeb (Web SDK)</li><li>Web (Web SDK)</li><li>API</li><li>segment</li><li>appsflyer</li><li>apsalar</li><li>branch</li><li>tune</li><li>System (for events generated by CleverTap)</li></ul> |
| eventProps.clevertapId | Indicates the unique device identifier. This is assigned to all the users when they launch the app for the first time. (@parth: Pls confirm if this is correct.)                                                                                                                                                                                                       |
| eventProps.token       | Indicates the Device token of the event                                                                                                                                                                                                                                                                                                                                |
| eventProps.source      | Indicates the source of the event, i.e., FCM or API                                                                                                                                                                                                                                                                                                                    |

### Webhook Delivered

This event is recorded when a Webhook campaign is delivered successfully.

| Key                                        | Description                                                                                                                                                                                                                                                                                                                                                            |
| :----------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| eventProps.ContentName                     |                                                                                                                                                                                                                                                                                                                                                                        |
| eventProps.CT Source                       | <p>The source of the event.</p><p>For example, the event may originate from a Mobile SDK or an API.</p><p>All possible values:</p><ul><li>Mobile (Mobile SDK)</li><li>MobileWeb (Web SDK)</li><li>Web (Web SDK)</li><li>API</li><li>segment</li><li>appsflyer</li><li>apsalar</li><li>branch</li><li>tune</li><li>System (for events generated by CleverTap)</li></ul> |
| eventProps.ct_app_version                  | This is the current version of your application installed on the user's device.                                                                                                                                                                                                                                                                                        |
| eventProps.ct_latitude                     | Indicates the latitude of the user.                                                                                                                                                                                                                                                                                                                                    |
| eventProps.all_identities                  | Indicates all Identity of the user                                                                                                                                                                                                                                                                                                                                     |
| eventProps.ct_longitude                    | Indicates the longitude of the user.                                                                                                                                                                                                                                                                                                                                   |
| eventProps.session_props \| session_source |                                                                                                                                                                                                                                                                                                                                                                        |
| eventProps.Campaign Id                     | Uniquely identifies the campaign.                                                                                                                                                                                                                                                                                                                                      |
| eventProps.mp_processing_time_ms           | Indicates the time in which we get a response from the customer API.                                                                                                                                                                                                                                                                                                   |
| eventProps.ts                              | Indicates the timestamp of the event.                                                                                                                                                                                                                                                                                                                                  |

### Channel Unsubscribed

This event is raised when a user unsubscribes from any group in an email.

[block:parameters]
{
  "data": {
    "h-0": "Key",
    "h-1": "Description",
    "0-0": "eventProps.Variant",
    "0-1": "Indicates the campaign variants created for A/B Testing.",
    "1-0": "eventProps.Resubscribed",
    "1-1": "Yes/No",
    "2-0": "eventProps.Group",
    "2-1": "Subscription Group",
    "3-0": "eventProps.Campaign id",
    "3-1": "Helps uniquely identify the campaign.",
    "4-0": "eventProps.Subscription Type",
    "4-1": "Indicates the type of Subscription",
    "5-0": "eventProps.Identity",
    "5-1": "Indicates the Unique Identity of the User",
    "6-0": "eventProps.Reason",
    "6-1": "Indicates the reason for Unsubscribing/Resubscribing",
    "7-0": "eventProps.Campaign type",
    "7-1": "@Parth, How is it different from eventProps.Type ?  \n(Amrita to take description from page history)",
    "8-0": "eventProps.CT Source",
    "8-1": "<p>The source of the event.</p><p>For example, the event may originate from a Mobile SDK or an API.</p><p>All possible values:</p><ul><li>Mobile (Mobile SDK)</li><li>MobileWeb (Web SDK)</li><li>Web (Web SDK)</li><li>API</li><li>segment</li><li>appsflyer</li><li>apsalar</li><li>branch</li><li>tune</li><li>System (for events generated by CleverTap)</li></ul>",
    "9-0": "eventProps.Clevertap ID",
    "9-1": "CleverTap account ID. [@Parth: Please confirm.]",
    "10-0": "eventProps.CT SDK Version",
    "10-1": "The CleverTap SDK version. For example, 30501.",
    "11-0": "eventProps.CT App Version",
    "11-1": "This is the current version of your application installed on the user's device.",
    "12-0": "eventProps.mimeType",
    "12-1": "",
    "13-0": "eventProps.Type",
    "13-1": ""
  },
  "cols": 2,
  "rows": 14,
  "align": [
    "left",
    "left"
  ]
}
[/block]


### Custom Control Group

This event is raised when a campaign is activated with a Control group.

| Key                        | Description                                                                                                                                                                                                                                                                                                                                                            |
| :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| eventProps.CT Source       | <p>The source of the event.</p><p>For example, the event may originate from a Mobile SDK or an API.</p><p>All possible values:</p><ul><li>Mobile (Mobile SDK)</li><li>MobileWeb (Web SDK)</li><li>Web (Web SDK)</li><li>API</li><li>segment</li><li>appsflyer</li><li>apsalar</li><li>branch</li><li>tune</li><li>System (for events generated by CleverTap)</li></ul> |
| eventProps.wzrk_id         | Indicates the Campaign ID.                                                                                                                                                                                                                                                                                                                                             |
| eventProps.wzrk_pivot      | Indicates the campaign variants created for A/B Testing.                                                                                                                                                                                                                                                                                                               |
| eventProps.Campaign name   | Indicates the name of the campaign.                                                                                                                                                                                                                                                                                                                                    |
| eventProps.Campaign type   | Indicates the CleverTap campaign type. For example, Push, Web Push, Webhook, etc.                                                                                                                                                                                                                                                                                      |
| eventProps.Campaign labels | Indicates the labels added for the campaign.                                                                                                                                                                                                                                                                                                                           |
| eventProps.Journey id      | Helps uniquely identify the journey in which the campaign is present.                                                                                                                                                                                                                                                                                                  |

### System Control Group

This event is raised when a campaign is activated with a Control group.

| Key                      | Description                                                                     |
| :----------------------- | :------------------------------------------------------------------------------ |
| eventProps.CT Source     | Indicates the source of the event, i.e., Mobile, Desktop, etc.                  |
| eventProps.wzrk_id       | Indicates the Campaign ID.                                                      |
| eventProps.wzrk_pivot    | Indicates the campaign variants created for A/B Testing.                        |
| eventProps.Campaign id   | Indicates the CleverTap campaign ID (@Parth: How is it different from wzrk_id?) |
| eventProps.Campaign name | Indicates the name of the campaign.                                             |
| eventProps.Campaign type | Indicates the type of campaign - Push, Email, etc.                              |
| eventProps.Journey id    | Helps uniquely identify the journey in which the campaign is present.           |

### Custom & Journey Control Group (Journeys)

This event is raised when a custom control group user or journey control group user qualifies for the journey.

| Key                     | Description                                                                                   |
| :---------------------- | :-------------------------------------------------------------------------------------------- |
| eventProps.Journey id   | Helps uniquely identify the journey in which the campaign is present.                         |
| eventProps.Journey name | Indicates Unique Journey identifier (@Parth, how is it different from eventProps.Journey id?) |

### System Control Group (Journeys)

This event is raised when a system control group user qualifies for the Journey.

| Key                     | Description                                                                                   |
| :---------------------- | :-------------------------------------------------------------------------------------------- |
| eventProps.Journey id   | Helps uniquely identify the journey in which the campaign is present.                         |
| eventProps.Journey name | Indicates Unique Journey identifier (@Parth, how is it different from eventProps.Journey id?) |

### Geocluster Entered

This event is raised when a user enters a Geo Cluster.

| Key                             | Description                                                                                                                                                                                                                                                                                                                                                            |
| :------------------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| eventProps.ct_connected_to_wifi | Status of Wifi on the device when the event is raised. The possible values are True or False.                                                                                                                                                                                                                                                                          |
| eventProps.ct_source            | Source is mobile or web                                                                                                                                                                                                                                                                                                                                                |
| eventProps.network_carrier      | Network Carrier for the device                                                                                                                                                                                                                                                                                                                                         |
| eventProps.longitude            | Longitude                                                                                                                                                                                                                                                                                                                                                              |
| eventProps.latitude             | Latitude                                                                                                                                                                                                                                                                                                                                                               |
| eventProps.os_version           | [@Parth: What's the difference between os_version and ct_os_version]                                                                                                                                                                                                                                                                                                   |
| eventProps.application_version  | Version of App                                                                                                                                                                                                                                                                                                                                                         |
| eventProps.ct_sdk_version       | CT SDK version used by the app when an event is raised                                                                                                                                                                                                                                                                                                                 |
| eventProps.geofence_id          | CT Geogence ID                                                                                                                                                                                                                                                                                                                                                         |
| eventProps.cluster_name         | CT Geofence Cluster Name                                                                                                                                                                                                                                                                                                                                               |
| eventProps.cluster_id           | CT Geofence Cluster ID                                                                                                                                                                                                                                                                                                                                                 |
| eventProps.ct_network_type      | The network type of the device. For example, 4G.                                                                                                                                                                                                                                                                                                                       |
| eventProps.ct_os_version        | The operating system of the device. For example, 1.0.0.                                                                                                                                                                                                                                                                                                                |
| eventProps.ct_app_version       | Indicates the version of the application.                                                                                                                                                                                                                                                                                                                              |
| eventProps.ct_latitude          | Indicates the last known latitude captured by CleverTap.                                                                                                                                                                                                                                                                                                               |
| eventProps.ct_longitude         | Indicates the last known longitude captured by CleverTap.                                                                                                                                                                                                                                                                                                              |
| eventProps.ct_network_carrier   | The network carrier of the device. For example, AT&T, Vodafone, etc.                                                                                                                                                                                                                                                                                                   |
| eventProps.CT Source            | <p>The source of the event.</p><p>For example, the event may originate from a Mobile SDK or an API.</p><p>All possible values:</p><ul><li>Mobile (Mobile SDK)</li><li>MobileWeb (Web SDK)</li><li>Web (Web SDK)</li><li>API</li><li>segment</li><li>appsflyer</li><li>apsalar</li><li>branch</li><li>tune</li><li>System (for events generated by CleverTap)</li></ul> |
| eventProps.Geofence id          |                                                                                                                                                                                                                                                                                                                                                                        |
| eventProps.Cluster name         |                                                                                                                                                                                                                                                                                                                                                                        |

### GeoCluster Exited

This event is raised when a user enters a Geo Cluster.

| Key                             | Description                                                                                   |
| :------------------------------ | :-------------------------------------------------------------------------------------------- |
| eventProps.ct_source            | Source is mobile or web                                                                       |
| eventProps.network_carrier      | Network Carrier for the device                                                                |
| eventProps.longitude            | Longitude                                                                                     |
| eventProps.latitude             | Latitude                                                                                      |
| eventProps.os_version           | OS Version of the device                                                                      |
| eventProps.application_version  | Version of App                                                                                |
| eventProps.ct_sdk_version       | CT SDK version used by the app when an event is raised.                                       |
| eventProps.geofence_id          | CT Geogence ID                                                                                |
| eventProps.cluster_name         | CT Geofence Cluster Name                                                                      |
| eventProps.cluster_id           | CT Geofence Cluster ID                                                                        |
| eventProps.ct_connected_to_wifi | Status of Wifi on the device when the event is raised. The possible values are True or False. |

### AB Experiment Stopped

This event is raised when the A/B experiment is stopped.

| Key                           | Description                   |
| :---------------------------- | :---------------------------- |
| eventProps.ct_source          | Source is mobile or web       |
| eventProps.stickiness         | Yes/No                        |
| eventProps.mutually_exclusive | Should show only 1 experiment |
| eventProps.variant            | Variant of Experiment         |
| eventProps.variant_id         | Unique Variant ID             |
| eventProps.version            | Version of Experiment         |
| eventProps.experiment_id      | Experiment ID                 |

### AB Experiment Rolled Out

This event is raised when the A/B experiment is sent to users.

| Key                           | Description                                                                                                                                                                                                                                                                                                                                                            |
| :---------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| eventProps.Variant            | Variant of Experiment                                                                                                                                                                                                                                                                                                                                                  |
| eventProps.Variant Id         | Unique Variant ID                                                                                                                                                                                                                                                                                                                                                      |
| eventProps.CT Source          | <p>The source of the event.</p><p>For example, the event may originate from a Mobile SDK or an API.</p><p>All possible values:</p><ul><li>Mobile (Mobile SDK)</li><li>MobileWeb (Web SDK)</li><li>Web (Web SDK)</li><li>API</li><li>segment</li><li>appsflyer</li><li>apsalar</li><li>branch</li><li>tune</li><li>System (for events generated by CleverTap)</li></ul> |
| eventProps.Version            | Version of Experiment                                                                                                                                                                                                                                                                                                                                                  |
| eventProps.Experiment Id      | Experiment ID                                                                                                                                                                                                                                                                                                                                                          |
| eventProps.Stickiness         | Yes/No                                                                                                                                                                                                                                                                                                                                                                 |
| eventProps.Mutually Exclusive | Should show only 1 experiment                                                                                                                                                                                                                                                                                                                                          |

### AB Experiment Disqualified

This event is raised when a user is disqualified from the A/B experiment.

### AB Experiment Rendered

This event is raised when the A/B experiment is rendered to a user.

| Key                           | Description                                                                                                                                                                                                                                                                                                                                                            |
| :---------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| eventProps.Variant            | Variant of Experiment                                                                                                                                                                                                                                                                                                                                                  |
| eventProps.Variant Id         | Unique Variant ID                                                                                                                                                                                                                                                                                                                                                      |
| eventProps.CT Source          | <p>The source of the event.</p><p>For example, the event may originate from a Mobile SDK or an API.</p><p>All possible values:</p><ul><li>Mobile (Mobile SDK)</li><li>MobileWeb (Web SDK)</li><li>Web (Web SDK)</li><li>API</li><li>segment</li><li>appsflyer</li><li>apsalar</li><li>branch</li><li>tune</li><li>System (for events generated by CleverTap)</li></ul> |
| eventProps.Version            | Version of Experiment                                                                                                                                                                                                                                                                                                                                                  |
| eventProps.Experiment Id      | Experiment ID                                                                                                                                                                                                                                                                                                                                                          |
| eventProps.Stickiness         | Yes/No [@Parth: Need inputs.]                                                                                                                                                                                                                                                                                                                                          |
| eventProps.Mutually Exclusive | Should show only 1 experiment                                                                                                                                                                                                                                                                                                                                          |

### State Transitioned

This event is recorded for lifecycle optimizer when a user transitions from one stage to another.

| Key                    | Description             |
| :--------------------- | :---------------------- |
| eventProps.Destination | Destination Value       |
| eventProps.Type        | Type Value of Lifecycle |
| eventProps.Model       | Model Value             |
| eventProps.Source      | Value of Source         |

### Session Concluded

This event is raised when a user session is completed.

| Key                       | Description                        |
| :------------------------ | :--------------------------------- |
| eventProps.Session Length | Time for which user was using apps |
| eventProps.Session Id     | Unique CT Session identifier       |

### UTM Visited

This event is tracked when a user clicks on a link from a marketing campaign that has a UTM parameter defined on it.

[block:parameters]
{
  "data": {
    "h-0": "Key",
    "h-1": "Description",
    "0-0": "eventProps.Campaign id",
    "0-1": "Unique campaign ID for campaigns",
    "1-0": "eventProps.ct_latitude",
    "1-1": "Indicates the last known latitude captured by CleverTap",
    "2-0": "eventProps.ct_longitude",
    "2-1": "Longitude",
    "3-0": "eventProps.ct_app_version",
    "3-1": "Indicates the version of the application.",
    "4-0": "eventProps.CT Source",
    "4-1": "<p>The source of the event.</p><p>For example, the event may originate from a Mobile SDK or an API.</p><p>All possible values:</p><ul><li>Mobile (Mobile SDK)</li><li>MobileWeb (Web SDK)</li><li>Web (Web SDK)</li><li>API</li><li>segment</li><li>appsflyer</li><li>apsalar</li><li>branch</li><li>tune</li><li>System (for events generated by CleverTap)</li></ul>",
    "5-0": "eventProps.Campaign type",
    "5-1": "Indicates the CleverTap campaign type. For example, Push, Web Push, Webhook, etc.",
    "6-0": "eventProps.Install",
    "6-1": "Y or N",
    "7-0": "eventProps.Variant",
    "7-1": "Indicates the message variant of the last campaign delivered to the end user.",
    "8-0": "eventProps.action",
    "8-1": "",
    "9-0": "eventProps.browser",
    "9-1": "",
    "10-0": "eventProps.wzrk_slideNo",
    "10-1": "",
    "11-0": "eventProps.wzrk_c2a",
    "11-1": "<li> Indicates the value of the button clicked by the user. </li>  \n<li> This button can be present for the following campaign types: In-App, Push, or Mobile In-Box. </li>",
    "12-0": "eventProps.wzrk_click_innerText",
    "12-1": "",
    "13-0": "eventProps.wzrk_click_c2a",
    "13-1": "",
    "14-0": "eventProps.wzrk_acct_id",
    "14-1": "Indicates the CleverTap Account ID.",
    "15-0": "eventProps.wzrk_cid",
    "15-1": "Indicates the Channel ID.",
    "16-0": "eventProps.wzrk_pid",
    "16-1": "",
    "17-0": "eventProps.wzrk_rnv",
    "17-1": "<li> A flag that indicates if the Notification Clicked event is raised. </li>  \n<li> If present and not empty, it indicates that the Notification Viewed event was raised. </li>",
    "18-0": "eventProps.wzrk_ttl",
    "18-1": "Indicates the time-to-live for the campaign",
    "19-0": "eventProps.wzrk_push_amp",
    "19-1": "",
    "20-0": "eventProps.wzrk_bc",
    "20-1": "Indicates the batch count.",
    "21-0": "eventProps.wzrk_bi",
    "21-1": "Indicates the badge icon. (@parth: Is it batch or badge?)",
    "22-0": "eventProps.wzrk_ck",
    "22-1": "Indicates the collapse key.",
    "23-0": "eventProps.wzrk_dt",
    "23-1": "Indicates the service used to send the message. For example, Firebase, etc.",
    "24-0": "eventProps.wzrk_pn",
    "24-1": "Indicates that the notification is sent from the CleverTap dashboard when present.",
    "25-0": "eventProps.ct_sdk_version",
    "25-1": "The CleverTap SDK version used by the app when an event is raised. For example, 30501.",
    "26-0": "eventProps.ct_os_version",
    "26-1": "The operating system of the device. For example, 1.0.0.",
    "27-0": "eventProps.ct_connected_to_wifi",
    "27-1": "Status of WiFi on the device when the event is raised. The possible values are True or False.",
    "28-0": "eventProps.ct_network_carrier",
    "28-1": "The network carrier of the device. For example, AT&T, Vodafone, etc.",
    "29-0": "eventProps.ct_bluetooth_version",
    "29-1": "The Bluetooth version of the device.",
    "30-0": "eventProps.ct_bluetooth_enabled",
    "30-1": "Indicates if Bluetooth is enabled on the device.",
    "31-0": "eventProps.ct_network_type",
    "31-1": "The network type of the device. For example, 4G.",
    "32-0": "eventProps.wzrk_cts",
    "32-1": "",
    "33-0": "eventProps.wzrk_bpds",
    "33-1": "",
    "34-0": "eventProps.wzrk_interruption_level",
    "34-1": "",
    "35-0": "eventProps.wzrk_relevance_score",
    "35-1": "",
    "36-0": "eventProps.wzrk_c2a_short_url",
    "36-1": "Indicates the short URL on which the customer clicked (available only for SMS and WhatsApp). It is available only if you use CleverTap's Click Tracking feature.",
    "37-0": "eventProps.wzrk_pn_h",
    "37-1": "",
    "38-0": "eventProps.CT App Version",
    "38-1": "This is the current version of your application installed on the user device.",
    "39-0": "eventProps.button_id",
    "39-1": "",
    "40-0": "eventProps.install_time",
    "40-1": "",
    "41-0": "eventProps.provider",
    "41-1": "",
    "42-0": "eventProps.wzrk_id",
    "42-1": "Unique campaign ID for campaigns.",
    "43-0": "sessionProps.utm_campaign",
    "43-1": "Campaign name",
    "44-0": "sessionProps.utm_medium",
    "44-1": "Medium such as email, banner, etc",
    "45-0": "sessionProps.utm_source",
    "45-1": "Origination source"
  },
  "cols": 2,
  "rows": 46,
  "align": [
    "left",
    "left"
  ]
}
[/block]


### Identity Set

| Key                        | Description |
| :------------------------- | :---------- |
| eventProps.ID              |             |
| eventProps.Type            |             |
| eventProps.Dropped History |             |
| eventProps.Source          |             |

### Identity Error

| Key               | Description |
| :---------------- | :---------- |
| eventProps.ID     |             |
| eventProps.Source |             |

### Identity Reset

| Key               | Description |
| :---------------- | :---------- |
| eventProps.ID     |             |
| eventProps.User   |             |
| eventProps.Source |             |

### App Version Changed

| Key                            | Description                                                                                                                                                                                                                                                                                                                                                            |
| :----------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| eventProps.CT App Version      | This is the current version of your application installed on the user's device.                                                                                                                                                                                                                                                                                        |
| eventProps.CT App Version Prev |                                                                                                                                                                                                                                                                                                                                                                        |
| eventProps.CT Source           | <p>The source of the event.</p><p>For example, the event may originate from a Mobile SDK or an API.</p><p>All possible values:</p><ul><li>Mobile (Mobile SDK)</li><li>MobileWeb (Web SDK)</li><li>Web (Web SDK)</li><li>API</li><li>segment</li><li>appsflyer</li><li>apsalar</li><li>branch</li><li>tune</li><li>System (for events generated by CleverTap)</li></ul> |
| eventProps.CT Latitude         | Indicates the last known latitude captured by CleverTap on launching the application.                                                                                                                                                                                                                                                                                  |
| eventProps.CT Longitude        | Indicates the last known longitude captured by CleverTap on launching the application.                                                                                                                                                                                                                                                                                 |

### Reachable By

| Key              | Description |
| :--------------- | :---------- |
| eventProps.value |             |
| eventProps.type  |             |
| eventProps.state |             |

### Push Unregistered

| Key                    | Description |
| :--------------------- | :---------- |
| eventProps.Token Type  |             |
| eventProps.Token Value |             |

### Partner Sync

| Key                             | Description                                                                                                                                                                                                                                                                                                                                                            |
| :------------------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| eventProps.CT Source            | <p>The source of the event.</p><p>For example, the event may originate from a Mobile SDK or an API.</p><p>All possible values:</p><ul><li>Mobile (Mobile SDK)</li><li>MobileWeb (Web SDK)</li><li>Web (Web SDK)</li><li>API</li><li>segment</li><li>appsflyer</li><li>apsalar</li><li>branch</li><li>tune</li><li>System (for events generated by CleverTap)</li></ul> |
| eventProps.Partner Name         |                                                                                                                                                                                                                                                                                                                                                                        |
| eventProps.Partner Segment Name |                                                                                                                                                                                                                                                                                                                                                                        |
| eventProps.Partner Segment ID   |                                                                                                                                                                                                                                                                                                                                                                        |
| eventProps.Action               |                                                                                                                                                                                                                                                                                                                                                                        |

### Channel Subscribed

| Key                       | Description                                                                                                                                                                                                                                                                                                                                                            |
| :------------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| eventProps.CT Source      | <p>The source of the event.</p><p>For example, the event may originate from a Mobile SDK or an API.</p><p>All possible values:</p><ul><li>Mobile (Mobile SDK)</li><li>MobileWeb (Web SDK)</li><li>Web (Web SDK)</li><li>API</li><li>segment</li><li>appsflyer</li><li>apsalar</li><li>branch</li><li>tune</li><li>System (for events generated by CleverTap)</li></ul> |
| eventProps.CT App Version | This is the current version of your application installed on the user's device.                                                                                                                                                                                                                                                                                        |
| eventProps.Campaign type  | Indicates the CleverTap campaign type. For example, Push, Web Push, Webhook, etc.                                                                                                                                                                                                                                                                                      |
| eventProps.CT SDK Version | The CleverTap SDK version. For example, 30501.                                                                                                                                                                                                                                                                                                                         |
| eventProps.Clevertap ID   | CleverTap account ID [@Parth: Could you confirm if this is correct?]                                                                                                                                                                                                                                                                                                   |

### Notification Sent

| Key                      | Description                                                                       |
| :----------------------- | :-------------------------------------------------------------------------------- |
| eventProps.Campaign id   | Unique campaign ID for the campaign.                                              |
| eventProps.Campaign type | Indicates the CleverTap campaign type. For example, Push, Web Push, Webhook, etc. |
| eventProps.Labels        |                                                                                   |
| eventPropsVariant        | Indicates the message variant of the last campaign delivered to the end user.     |

# User Profile Export

## File Name Format

```text
<export request id>-<timestamp of the export run>-<event name>-<yyyymmdd>-<file index>-<database-id>.json
```

- **File Name Format for User Profile Export**:  
   The example below shows the file name format for user profile export:
  - _Account ID_: Indicates the integer value for your CleverTap project ID. 
  - _Request ID_: Indicates the export request ID generated when you create a request in the CleverTap dashboard.
  - _Timestamp of export run_: Indicates when the export was run.
  - _Database ID_: Indicates the database ID of the CleverTap from where the file was exported. 
  - _File format_: Indicates the file format exported to the S3 bucket.

```text
<account id>-<request id>-<timestamp of the export run>-<database-id>-<file format>.gz
```

## File Data Format

Files are split by event names for event exports, and each file will have all event data for the given period for the event.

### JSON

The first line of the file contains the event name. After the first line, each line in JSON describes the timestamp, object ID, and event properties.

```json
{
	"profile": {
		"identity": "dqsndckfk234"
	},
	"ts": 20171109000015,
	"eventProps": {
		"ct_connected_to_wifi": "false",
		"ct_bluetooth_version": "ble",
		"ct_bluetooth_enabled": "false",
		"ct_sdk_version": 30107,
		"ct_latitude": -6.1975594,
		"ct_longitude": 106.52913,
		"ct_os_version": "5.1.1",
		"ct_app_version": "2.30.1",
		"ct_network_carrier": "3",
		"ct_network_type": "4G"
	}
}
```

### CSV

CSV files are comma-delimited and have each event in separate rows.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/aa71f9f-Screenshot_2020-02-28_at_12.53.22_PM.png",
        "Sample CSV File",
        2032
      ],
      "align": "center",
      "border": true,
      "caption": "Sample CSV File"
    }
  ]
}
[/block]


### XML

XML has the timeStamp, eventName, followed by eventProperties.

```typescript
<Event>
    <ts>20200220130735</ts>
    <eventName>Export Custom Event</eventName>
    <profile>
        <all_identities>exportProfile+81@clevertap.com</all_identities>
        <platform>Web</platform>
        <email>exportProfile+81@clevertap.com</email>
    </profile>
    <deviceInfo>
        <browser>Others</browser>
    </deviceInfo>
    <eventProps>
        <entry>
            <key>CT Source</key>
            <value>API</value>
        </entry>
        <entry>
            <key>Category</key>
            <value>Mens Watch</value>
        </entry>
        <entry>
            <key>Product name</key>
            <value>Casio Chronograph Watch</value>
        </entry>
        <entry>
            <key>Price</key>
            <value>59.99</value>
        </entry>
        <entry>
            <key>Currency</key>
            <value>USD</value>
        </entry>
    </eventProps>
</Event>
```

### Parquet

Parquet has a timestamp, eventName, and eventProperties for each event. 

> 📘 Parquet File Format
> 
> Parquet is an open-source file format for Hadoop. Parquet stores nested data structures in a flat columnar format.