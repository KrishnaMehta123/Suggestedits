---
title: SMS Provider Operations_EM-1033
excerpt: Understand how to edit, archive, and delete providers.
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

This section describes actions for the available SMS service providers.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/936ca90-SMS_setup_provider_archive_edit.png",
        "SMS_setup_provider_archive_edit.png",
        1183
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


# Operations

The operations for SMS providers are as follows:

## Edit Settings

Edit the SMS settings to change _Provider credentials_.

Follow the steps to edit provider settings:

1. From the CleverTap dashboard, navigate to _Settings_ > _Channels_ > _SMS_ > Providers\_ tab. 
2. Click the ellipsis next to the provider. 
3. Select _Edit settings_ from the list. The _Provider credentials_ window displays.
4. Change the required information. 
5. Click **Send Test SMS** to check that the provider is working correctly. 
6. Click **Save**.

## Mark as Default

Set a service provider as default so that the same provider appears pre-selected from the dropdown by default in the campaign creation workflow for delivering your SMS

To set up a default SMS service provider:

1. From the CleverTap dashboard, navigate to _Settings_ > _Channels_ > _SMS_ > _Providers_ tab. 
2. Click the ![](https://files.readme.io/9c12d50-Ellipses_icon.png) icon next to the provider. 
3. Select _Mark as Default_ from the list.

## Archive Service Providers

You can archive any current SMS service providers from the SMS settings. Archiving the SMS service provider stops any active _Campaigns_ or _Journeys_ for this provider. The archived provider will not be available for use in the future. However, it will still retain the provider stats. 

To archive an SMS service provider:

1. From the CleverTap dashboard, navigate to _Settings > Channels > SMS > Providers_ tab. 
2. Click the ellipsis next to the provider. 
3. Select _Archive_ from the list.

> 📘 Restoring an Archived Provider
> 
> After you archive a service provider, you can not restore it. However, the stats are available for the user to view.

## Delete Service Providers

You can delete any current SMS service providers from the SMS settings. Deleting the SMS service provider will remove all existing data from our system and stop any active _Campaigns_ or _Journeys_. The deleted provider will not be available for use in the future.

Follow the steps to delete an SMS service provider:

1. From the CleverTap dashboard, navigate to _Settings > Channels > SMS > Providers_ tab. 
2. Click the ellipsis next to the provider. 
3. Select _Delete_ from the list.

## View Provider Stats

You can view the detailed actionable stats such as SMS delivered, clicked, and replied from the CleverTap dashboard. To view the provider stats:

1. Navigate to _Settings_ > _Channels_ > _SMS_ from the dashboard.
2. Click the SMS provider name from the _Providers_ tab.
3. Navigate to the _Stats_ tab. The following _Stats_ page opens where you can view the overall stats with different metrics:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/36910b3-SMS_Provider_Stats.png",
        null,
        "SMS Provider Stats"
      ],
      "align": "center",
      "border": true,
      "caption": "SMS Provider Stats"
    }
  ]
}
[/block]


- **Total Sent**: Displays the total number of SMS sent from CleverTap.
- **Total Delivered**: Displays the total number of messages delivered to the end user. This count is available only if the [delivery callbacks](doc:generic-sms_em-1033-structure#configure-sms-callback) are set up so that CleverTap can track delivered SMS.
- **Total Clicks**: Represents the count of clicks by the users.
- **Total Errors**: Displays the total number of system errors encountered when delivering an SMS campaign.
- **Delivery Rate**: Available if delivery callbacks are set up else it is displayed as zero. It is calculated as [(Delivered/Sent)* 100].

The _Provider Stats_ also provides:

- **Delivery Stats** such as:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d3f50ea-small-Delivery_Stats.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


- _Daily Avg Sent_: Calculated as the total sent SMS divided by the number of days. 

- _Daily Avg Delivery_: Calculated as \[(Total delivered SMS/Number of days) \* 100).

- _Clicked_: Displays the number of clicks registered on SMSes. Available only when using CleverTap's [Click Tracking](https://docs.clevertap.com/docs/create-message-sms-click-tracking#click-tracking) or [SMS Callback](https://staging.docs.user.clevertap.net/docs/generic-sms_em-1033-structure#sms-callbacks) feature. 

- _Errors_: Displays the number of errors for the selected duration.

- **SMS Delivery Stats**: Displays the line graph for the following: _Total Sent_, _Total Errors_, and _Total Clicks_. You can toggle each of these stats to view only the specific stats or view all these stats at once.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3446542-small-Sends_and_Errors.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


- **Performance**: Displays the campaign performance based on Click Through Rate (CTR) for a specific period. When the callbacks are configured, it is calculated as [(Clicked/Delivered) * 100]. When the callbacks are not configured, it is calculated as [(Clicked/Sent) * 100].

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/377439e-small-Performance_Stats.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


- **Delivery Rate**:  Available if delivery callbacks are set up else it is displayed as zero. It is calculated as [(Delivered/Sent)* 100]. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2928613-small-Delivery_Rate_Stats.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


> 📘 SMS Clicks
> 
> Total SMS Clicks count is available in SMS only if the URL specified in the message body is shortened using [CleverTap Link Shortening](https://docs.clevertap.com/docs/create-message-sms#link-shortening) feature or the click data is sent to CleverTap via the SMS provider through callbacks.