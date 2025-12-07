---
title: Email Provider Operations
excerpt: ''
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

This section describes actions for the available email service providers.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/36c908a-Email_Operations.png",
        "Email service providers",
        736
      ],
      "align": "center",
      "border": true,
      "caption": "Email Service Providers"
    }
  ]
}
[/block]


# Operations

You can perform the following operations on any email service provider:

## Edit Settings

Edit the email settings to change _Provider credentials_.

To edit the provider settings:

1. From the CleverTap dashboard, navigate to _Settings_ > _Channels_ > _Email_ > _Providers_ tab. 
2. Click the ![](https://files.readme.io/ecfbe56-Ellipses_icon.png) icon next to the provider. 
3. Select _Edit settings_ from the list. The _Provider credentials_ window displays.
4. Change the required information. 
5. Click **Send Test Email** to check that the provider is working correctly. 
6. Click **Save**.

## Mark as Default

Set a service provider as default so that the same provider is used for delivering your emails. 

To set up a default email service provider:

1. From the CleverTap dashboard, navigate to _Settings_ > _Channels_ > _Email_ > _Providers_ tab. 
2. Click the ![](https://files.readme.io/9c12d50-Ellipses_icon.png) icon next to the provider.
3. Select _Mark as Default_ from the list.

## Archive Service Providers

You can archive any of the current email service providers from the email settings. Archiving the email service provider stops any active _Campaigns_ or _Journeys_ for this provider. The archived provider will not be available for use in the future. However, it will still retain the provider stats. 

To archive an email service provider:

1. From the CleverTap dashboard, navigate to _Settings_ > _Channels_ > _Email_ > _Providers_ tab. 
2. Click the ![](https://files.readme.io/690a04c-Ellipses_icon.png) icon next to the provider. 
3. Select _Archive_ from the list. 

## Delete Service Providers

You can delete any of the current email service providers from the email settings. Deleting a provider will remove all existing data from our system and stop any active _Campaigns_ or _Journeys_. The deleted provider will not be available for use in the future.

To delete an email service provider

1. From the CleverTap dashboard, navigate to _Settings_ > _Channels_ > _Email_ > _Providers_ tab. 
2. Click the ![](https://files.readme.io/0f986d4-Ellipses_icon.png) icon next to the provider. 
3. Select _Delete_ from the list. 

# View Provider Stats

You can view the detailed actionable stats such as Email Sent, Open, and Open Rate from the CleverTap dashboard. To view the provider stats:

1. Navigate to _Settings_ > _Channels_ > _Email_ from the dashboard.
2. Click the Email provider name from the _Providers_ tab.
3. Navigate to the _Stats_ tab. The following _Stats_ page opens where you can view the overall stats with different metrics:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/13aef66-image.png",
        null,
        null
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


<br />

- **Total Sent**: Displays the total number of emails sent from CleverTap. This count excludes the count for CC Sent and BCC Sent.
- **Total Opens**: Displays the total number of emails opened.
- **Open Rate**: Displays the open percentage for your message. It is calculated as [(Viewed /Sent)* 100].

The _Provider Stats_ also displays the following: 

- **Delivery stats**:
  - _Daily Avg Sent_: Calculated as the total sent emails divided by the number of days. 
  - _Daily Avg Opens_: Calculated as [(Total Opens/Number of days)* 100].
  - _Clicked_: Displays the number of clicks registered on the email campaign.
  - Unsubscribed: Displays the number of unsubscribes on the email campaign.
  - Spam Reports: Displays the number of emails marked as spam by recipients

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e6615ec-image.png",
        null,
        null
      ],
      "align": "center",
      "border": true,
      "caption": "Email Delivery Stats"
    }
  ]
}
[/block]


- **Performance Stats**: Displays the campaign performance based on Click Through Rate (CTR) and Open Rate for a specific period. Avg CTR is calculated as: (CTR/Number of days). Avg Open Rate is calculated as: (Open Rate/Number of days).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a1b1c17-image.png",
        null,
        null
      ],
      "align": "center",
      "border": true,
      "caption": "Performance Stats"
    }
  ]
}
[/block]


- **Deliverability Stats**:             

Displays the campaign deliverability based on Opened and Spam Reports stats for a specific period.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2be6eda-image.png",
        null,
        null
      ],
      "align": "center",
      "border": true,
      "caption": "Deliverability Stats"
    }
  ]
}
[/block]