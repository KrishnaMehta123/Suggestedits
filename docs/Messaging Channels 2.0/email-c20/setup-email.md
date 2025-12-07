---
title: Setup
excerpt: Set up your email.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
  pages:
    - type: link
      title: Email Create Message
      url: https://docs.clevertap.com/docs/create-message-email
    - type: link
      title: Email Editor
      url: https://docs.clevertap.com/docs/email-editor-templates
    - type: link
      title: Email Personalize
      url: https://docs.clevertap.com/docs/personalize-message-email
    - type: link
      title: Handling Unsubscribes
      url: https://docs.clevertap.com/docs/handling-unsubscribes-c20
    - type: link
      title: Group Unsubscribe
      url: https://docs.clevertap.com/docs/group-unsubscribe-new
    - type: link
      title: Override Link Tracking
      url: https://docs.clevertap.com/docs/override-link-tracking-c20
    - type: link
      title: Email Campaign Stats
      url: https://docs.clevertap.com/docs/email-stats
    - type: link
      title: Email Troubleshooting
      url: https://docs.clevertap.com/docs/troubleshooting-email
---
# Overview

This section covers various email tasks, including the integrations, and inbox previews. No matter the type of customer emails, all businesses have the same goal to get to the correct recipient's inbox. By setting up your email correctly, you ensure successful email deliverability.

# Email Integrations

Before you can create email campaigns, you must integrate an email service provider with CleverTap. 

CleverTap supports integrations with popular email service providers. Select your email service provider from the following list:

* [Mandrill](doc:mandrill) 
* [Amazon Simple Email Service](doc:amazon-simple-email-service) 
* [Postmark](doc:postmark) 
* [SendGrid](doc:sendgrid) 
* [Gmail/Google Apps](doc:gmail-google-apps) 

For all other service providers, use [Generic SMTP](doc:generic-smtp).

# Setup Provider

Once you have integrated an email service provider with CleverTap, you can set up your email service provider.

To add a provider, perform the following steps:

1. From the dashboard, navigate to *Settings* > *Engage* > *Channels* > *Email*.
2. Click **+ Provider** to add a provider. 

<Image title="Plus provider.png" alt={1162} border={true} src="https://files.readme.io/9206de0-Plus_provider.png">
  Add Provider
</Image>

3. Add the email provider's information.
4. Click **Save**.
5. Click *Send Test Email* to check if the provider has been set up correctly and can send emails.

## Provider Operations

This section describes actions for the available email service providers.

<Image title="Email_Operations.png" alt={736} border={true} src="https://files.readme.io/36c908a-Email_Operations.png">
  Provider Operations
</Image>

### Archive Service Providers

You can archive any of the current email service providers from the email settings. Archiving the email service provider stops any active *Campaigns* or *Journeys* for this provider. The archived provider will not be available for use in the future. However, it will still retain the provider stats. 

Follow the steps to archive an email service provider:

1. From the CleverTap dashboard, navigate to *Settings > Channels > Email > Providers* tab. 
2. Click the ellipsis next to the provider. 
3. Select *Archive* from the list. 

### Delete Service Providers

You can delete any of the current email service providers from the email settings. Deleting the email service provider will remove all existing data from our system and stop any active *Campaigns* or *Journeys*.  The deleted provider will not be available for use in the future.

Follow the steps to archive an email service provider:

1. From the CleverTap dashboard, navigate to *Settings > Channels > Email > Providers* tab. 
2. Click the ellipsis next to the provider. 
3. Select *Delete* from the list.

### Edit Settings

Edit the email settings to change *Provider credentials*.

Follow the steps to edit provider settings:

1. From the CleverTap dashboard, navigate to *Settings > Channels > Email > Providers* tab. 
2. Click the ellipsis next to the provider. 
3. Select *Edit settings* from the list. The *Provider credentials* window displays.
4. Change the required information. 
5. Click **Send Test Email** to check that the provider is working correctly. 
6. Click **Save**.

### Mark as Default

Set a service provider as default so that the same provider is used for delivering your emails. 

1. Follow the steps to set a default email service provider:
2. From the CleverTap dashboard, navigate to *Settings > Channels > Email > Providers* tab. 
3. Click the ellipsis next to the provider. 
4. Select *Mark as Default* from the list.

# Inbox Previews

Before you can use inbox previews, you must enable them. Inbox previews with code analysis let you view an analysis of your HTML code. It also provides the capability to view previews across devices and inboxes before you send out a campaign. 

> 🚧 Account Specifications
>
> Email previews are available only if you have opted for the email add-on from CleverTap.

## Enable or Disable Inbox Previews

To enable or disable the inbox preview, perform the following steps:

1. From the dashboard, navigate to *Settings* > *Engage* > *Channels* > *Email*.
2. Select the *Previews* tab.
3. Select a client from the list.
4. Click on the ellipsis and click **Enable** or **Disable**.

> 📘 Multi-select
>
> You can also select multiple clients, then enable or disable previews by clicking **Enable in inbox previews** or **Disable in inbox previews**.

<Image title="Enable an inbox preview.png" alt={1172} className="border" border={true} src="https://files.readme.io/49e8f2d-Enable_an_inbox_preview.png" />

The *Previews* tab lists the available email inboxes. For example, a mobile device that runs Gmail on Android 8 or a computer that runs Apple Mail 10 on an OS X 10.10 operating system. 

> 🚧 Account Specifications
>
> Email previews are available only if you have opted for the email add-on from CleverTap.\
> This feature is not available for trial accounts.
