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

Netcore is an email delivery platform that integrates with CleverTap to send campaigns and track delivery events.

# Prerequisites for Integration

The following are the prerequisites:

* You must have an account with Email permissions from Netcore Cloud.
* You must have a CleverTap account. 

# Integrate Netcore Cloud API with CleverTap

To integrate with CleverTap, perform the following steps:

1. Go to *Settings* > *Channels* > *Email* from the CleverTap dashboard.
2. Click **+ Provider**. The *Provider credentials* page displays. 

<Image title="Click Pepipost.png" alt={2728} align="center" width="85% " border={true} src="https://files.readme.io/170b8b2-Click_Pepipost.png">
  Add Provider Credentials
</Image>

3. Select *Netcore* from the *Provider* dropdown list.
4. Enter the following details:

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
        Nickname
      </td>

      <td>
        <p>Enter the nickname for your integration.</p>
      </td>
    </tr>

    <tr>
      <td>
        Callback URL
      </td>

      <td>
        The Callback URL is used to receive bounce, delivery, and subscription information from Netcore Cloud API to CleverTap. This is a read-only field that is auto-populated with CleverTap's callback URL. Ensure you add this URL to your ESP dashboard settings to send callback data to CleverTap. For more information, refer to 

        [Webhooks](https://cpaasdocs.netcorecloud.com/docs/email-api-v6/ocbf6v6gdlxjc-sent-webhook)

        .
      </td>
    </tr>

    <tr>
      <td>
        API Endpoint
      </td>

      <td>
        API endpoint of the Email Service Provider (ESP). Must start with 

        `http://`

         or 

        `https://`

        .
      </td>
    </tr>

    <tr>
      <td>
        API Key
      </td>

      <td>
        <ul><li>Enter the Netcore Cloud API key. </li><li>For more information about getting the key, refer to <a href="https://emaildev.netcorecloud.com/docs/pepipost-api/ZG9jOjQyMTU3NjQ0-authentication#how-to-get-your-api-key">Authentication</a> section.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        From Address
      </td>

      <td>
        Enter the default email address you want to use for sending your email campaigns.
      </td>
    </tr>

    <tr>
      <td>
        Reply Address
      </td>

      <td>
        Enter the default email address to which you want your users to reply to the campaign.
      </td>
    </tr>

    <tr>
      <td>
        Email Preference Center
      </td>

      <td>
        <p>Select System from the dropdown to use a pre-built preference center with a sample preview. </p><p>Select Custom URL to add your hosted unsubscription page URL.</p><p>Select None if you want to manage the email preferences directly on your own.</p>For more information, refer to [Manage Email Preferences](doc:manage-email-preferences#configure-email-preference-center).
      </td>
    </tr>
  </tbody>
</Table>

5. Click **Send Test Email** and fill in your details to test the configuration. You receive an email in your inbox.

You can also mark a particular ESP as default by clicking the  ![](https://files.readme.io/0e520ca-ellipses_icon.png) icon and selecting *Mark as Default*.

# Set Up Email Status Callbacks

When an email is classified as bounced, rejected, or spam or when a user unsubscribes, CleverTap needs to be notified so that no further deliveries to that mailbox are attempted. This is considered good practice and helps improve your sender's reputation, which virtually guarantees better delivery rates.

To handle such scenarios, perform the following steps:

1. Go to *Settings* > *Webhooks* and add the CleverTap callback URL under *Global API*  for Netcore Cloud API to POST the event data. 

   <Image alt="Callback URL Setup On Netcore Dashboard" align="center" border={true} src="https://files.readme.io/c6dc491356724626d57675114aafa539eb95849f9d378a8b6583841f503204e2-Callback_URL_Setup.png">
     Callback URL Setup On Netcore Dashboard
   </Image>
2. Click **Verify** to verify your webhook before adding it. For more information about verifying your webhook, refer to [How to test and debug Webhooks?](https://emaildocs.netcorecloud.com/docs/how-to-test-and-debug-webhooks).

> 📘 CleverTap Callback
>
> Currently, CleverTap supports tracking the following events: 
>
> * Delivered: Tracked as Notification Delivered on the CleverTap dashboard.
> * Dropped, Bounced, Unsubscribed, Invalid, and Spam: Tracked as Notification Failed event on the CleverTap dashboard.

# Edit Email Service Provider Settings

To edit the settings on the CleverTap dashboard:

1. From the Email Providers page, click the ![](https://files.readme.io/0e520ca-ellipses_icon.png) icon and then select *Edit settings*. The *Provider credentials* popup opens. 

<Image title="Provider credentials.png" alt={1458} align="center" width="50% " border={true} src="https://files.readme.io/918bd1697e40cc79cf1ff33a995c750056e70d9eeb80e17ad7d97aff8cbbe82d-Netcore_Provider_Setup.png">
  Edit Provider Settings
</Image>

2. Edit the required credentials and then click **Save**. You are navigated back to the *Email Service Provider* list page, and the *Email settings updated successfully* message displays at the top. 

# Troubleshooting

### Failed to send out test notifications

**Issue**\
The following error displays when saving Netcore Cloud API credentials on the CleverTap dashboard:

<Image title="Screenshot 2022-05-27 at 3.29.09 PM.png" alt={1426} align="center" width="75% " border={true} src="https://files.readme.io/c26ee17-Screenshot_2022-05-27_at_3.29.09_PM.png">
  Send Test Notification Error
</Image>

**Resolution**\
To resolve the issue, perform the following steps:

1. Find your Netcore Cloud API Email Credentials. Ensure that the keys are added correctly as they are case-sensitive.
2. Raise a [CleverTap Support Request](https://help.clevertap.com/hc/en-us/requests/new?ticket_form_id=4416487002257) to get the error code if the issue persists. After you receive the error code from the CleverTap support team, contact the Netcore Cloud API support team to resolve this.
