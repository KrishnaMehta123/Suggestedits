---
title: Netcore Cloud API
excerpt: Email Partner
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Introduction

Netcore offers artificial intelligence-powered marketing automation and customer engagement platform to help marketers listen, analyze, and build conversations with consumers. CleverTap users can now leverage the email capabilities of Netcore Cloud API to communicate with their customers.

# Prerequisites for Integration

The following are the prerequisites:

- You must have an account with Email permissions from Netcore Cloud.
- You must have a CleverTap account. 

# Integrate Netcore Cloud API with CleverTap

To integrate with CleverTap:

1. Navigate to _Settings_ > _Engage_ > _Channels_ > _Email_ from the CleverTap dashboard.
2. Click **+ Provider**. The _Provider credentials _page displays. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/170b8b2-Click_Pepipost.png",
        "Click Pepipost.png",
        2728
      ],
      "border": true
    }
  ]
}
[/block]

3. Select _Netcorecloud Email_ from the _Provider_ dropdown list.
4. Enter the following details:

| <p>Field</p>            | <p>Description</p>                                                                                                                                                                                                                                                     |
| :---------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Nickname</p>         | <p>Enter the nickname for your integration.</p>                                                                                                                                                                                                                        |
| <p>Callback URL</p>     | <p>Enter the callback URL where Netcore Cloud API can POST the event data.</p>                                                                                                                                                                                         |
| <p>API Key</p>          | <ul><li>Enter the Netcore Cloud API key. </li><li>For more information about getting the key, refer to <a href="https://emaildev.netcorecloud.com/docs/pepipost-api/ZG9jOjQyMTU3NjQ0-authentication#how-to-get-your-api-key">Authentication</a> section.</li></ul>     |
| <p>From Address</p>     | <p>Enter the sender's email address. Most people will not open an email unless they recognize the sender.</p>                                                                                                                                                          |
| <p>Unsubscribe Page</p> | <ul><li>If you wish to handle unsubscription by creating your personalized page, enter the unsubscription page URL.</li><li>To handle unsubscribed requests from users, refer to the steps in <a href="doc:handling-unsubscribes">Handling Unsubscribes</a>.</li></ul> |

5. Click **Send Test Email** and fill in your details to test the configuration details you entered.  
   You receive an email in the inbox.

> 📘 Default Email Service Provider
> 
> Click ![ellipses](https://files.readme.io/0e520ca-ellipses_icon.png) icon and then select _Mark as Default_ to mark the email service provider as default.

# Handle Bounces, Rejections, Unsubscriptions, and Spam

When an email is classified as bounced, rejected, or spam, or when a user unsubscribes, CleverTap needs to be notified so that no further deliveries to that mailbox are attempted. This is considered a good practice and helps improve your sender's reputation. Good sender reputation virtually guarantees better delivery rates.

To handles such scenarios:

1. Navigate to _Settings_ >_ Webhooks_ and enable **Event Notification**.
2. Set up a _Global_ webhook for each email event by entering a valid callback URL where Netcore Cloud API can POST the event data.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2b02439-Global_API.png",
        "Global API.png",
        2398
      ],
      "border": true
    }
  ]
}
[/block]

5. Click **Verify** to verify your webhook before adding it. For more information about verifying your webhook, refer to [How to test and debug Webhooks?](https://emaildocs.netcorecloud.com/docs/how-to-test-and-debug-webhooks).

> 📘 Inactive Users
> 
> - When an email bounces, drops, or unsubscribes, CleverTap marks the user's email address as **Inactive**.
> - The count of email bounces is shown on the _Stats_ page.

# Edit Email Service Provider Settings

To edit the settings on the CleverTap dashboard:

1. From the Email Providers page, click ![ellipses](https://files.readme.io/0e520ca-ellipses_icon.png) icon and then select _Edit settings_. On selecting, the _Provider credentials_ popup opens. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/50d94bb-Provider_credentials.png",
        "Provider credentials.png",
        1458
      ],
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]

2. Edit the required credentials and then click **Save**. You are navigated back to the _Email Service Provider_ list page, and the _Email settings updated successfully_ message displays at the top. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1e48b7d-Email_settings_saved_successfully.png",
        "Email settings saved successfully.png",
        2372
      ],
      "border": true
    }
  ]
}
[/block]

> ❗️ Delete Email Service Provider
> 
> If you delete a service provider, then the following warning displays  
> (see figure below) and you are prompted to confirm if you still want to delete the service provider

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/da86162-Delete_service_provider.png",
        "Delete service provider.png",
        2240
      ],
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]

# Event Data

Currently, CleverTap has enabled notifications for the following events:

- Dropped
- Bounced
- Unsubscribed
- Invalid
- Abuse

For more information about these events, refer to [Supported events](https://emaildev.netcorecloud.com/docs/pepipost-api/ZG9jOjQyMTU3NjUz-outline).

# Troubleshooting

## Failed to send out test notifications

**Issue**  
The following error displays when saving Netcore Cloud API credentials on the CleverTap dashboard:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c26ee17-Screenshot_2022-05-27_at_3.29.09_PM.png",
        "Screenshot 2022-05-27 at 3.29.09 PM.png",
        1426
      ],
      "border": true
    }
  ]
}
[/block]

**Resolution**  
The following are the steps to resolve the issue:

1. Find your Netcore Cloud API Email Credentials. Ensure that the keys are added correctly as they are case-sensitive.
2. Raise the [CleverTap Support Request](https://help.clevertap.com/hc/en-us/requests/new?ticket_form_id=4416487002257) to get the error code if the issue persists.
3. Connect with the Netcore Cloud API support team to get this resolved after you receive the error code from the CleverTap support team.