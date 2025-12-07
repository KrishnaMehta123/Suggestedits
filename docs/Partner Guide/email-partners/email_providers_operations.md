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

<Image title="Email service providers" alt={736} align="center" border={true} src="https://files.readme.io/36c908a-Email_Operations.png">
  Email Service Providers
</Image>

# Operations

You can perform the following operations on any email service provider:

## Edit Settings

Edit the email settings to change *Provider credentials*.

To edit the provider settings:

1. From the CleverTap dashboard, navigate to *Settings* > *Channels* > *Email* > *Providers* tab. 
2. Click the ![](https://files.readme.io/ecfbe56-Ellipses_icon.png) icon next to the provider. 
3. Select *Edit settings* from the list. The *Provider credentials* window displays.
4. Change the required information. 
5. Click **Send Test Email** to check that the provider is working correctly. 
6. Click **Save**.

## Mark as Default

Set a service provider as default so that the same provider is used for delivering your emails. 

To set up a default email service provider:

1. From the CleverTap dashboard, navigate to *Settings* > *Channels* > *Email* > *Providers* tab. 
2. Click the ![](https://files.readme.io/9c12d50-Ellipses_icon.png) icon next to the provider.
3. Select *Mark as Default* from the list.

## Archive Service Providers

You can archive any of the current email service providers from the email settings. Archiving the email service provider stops any active *Campaigns* or *Journeys* for this provider. The archived provider will not be available for use in the future. However, it will still retain the provider stats. 

To archive an email service provider:

1. From the CleverTap dashboard, navigate to *Settings* > *Channels* > *Email* > *Providers* tab. 
2. Click the ![](https://files.readme.io/690a04c-Ellipses_icon.png) icon next to the provider. 
3. Select *Archive* from the list. 

## Delete Service Providers

You can delete any of the current email service providers from the email settings. Deleting a provider will remove all existing data from our system and stop any active *Campaigns* or *Journeys*. The deleted provider will not be available for use in the future.

To delete an email service provider

1. From the CleverTap dashboard, navigate to *Settings* > *Channels* > *Email* > *Providers* tab. 
2. Click the ![](https://files.readme.io/0f986d4-Ellipses_icon.png) icon next to the provider. 
3. Select *Delete* from the list. 

# View Provider Stats

You can view the detailed actionable stats such as Email Sent, Open, and Open Rate from the CleverTap dashboard. To view the provider stats:

1. Navigate to *Settings* > *Channels* > *Email* from the dashboard.
2. Click the Email provider name from the *Providers* tab.
3. Navigate to the *Stats* tab. The following *Stats* page opens where you can view the overall stats with different metrics:

<Image align="center" className="border" border={true} src="https://files.readme.io/13aef66-image.png" />

<br />

* **Total Sent**: Displays the total number of emails sent from CleverTap. This count excludes the count for CC Sent and BCC Sent.
* **Total Opens**: Displays the total number of emails opened.
* **Open Rate**: Displays the open percentage for your message. It is calculated as [(Viewed /Sent)* 100].

The *Provider Stats* also displays the following: 

* **Delivery stats**:
  * *Daily Avg Sent*: Calculated as the total sent emails divided by the number of days. 
  * *Daily Avg Opens*: Calculated as [(Total Opens/Number of days)* 100].
  * *Clicked*: Displays the number of clicks registered on the email campaign.
  * Unsubscribed: Displays the number of unsubscribes on the email campaign.
  * Spam Reports: Displays the number of emails marked as spam by recipients

<Image alt="Email Delivery Stats" align="center" border={true} src="https://files.readme.io/e6615ec-image.png">
  Email Delivery Stats
</Image>

* **Performance Stats**: Displays the campaign performance based on Click Through Rate (CTR) and Open Rate for a specific period. Avg CTR is calculated as: (CTR/Number of days). Avg Open Rate is calculated as: (Open Rate/Number of days).

<Image alt="Performance Stats" align="center" border={true} src="https://files.readme.io/a1b1c17-image.png">
  Performance Stats
</Image>

* **Deliverability Stats**:             

Displays the campaign deliverability based on Opened and Spam Reports stats for a specific period.

<Image alt="Deliverability Stats" align="center" border={true} src="https://files.readme.io/2be6eda-image.png">
  Deliverability Stats
</Image>
