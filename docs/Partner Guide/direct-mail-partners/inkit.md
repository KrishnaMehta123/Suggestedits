---
title: Inkit
excerpt: Direct Mail Partner
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

[Inkit](https://www.inkit.com/), a leading Document Generation Platform (DGP), enables you to communicate with your customers by delivering automated and personalized direct mail campaigns, rendering paperless documents at scale, and validating customer mailing addresses.

With this integration, CleverTap seamlessly lets Inkit send direct mailers to your users using CleverTap Webhook.

# Prerequisites for Integration

The following are the prerequisites for this integration:

* You must have an Inkit [Account](https://app.inkit.io/), an [API token](https://docs.inkit.com/docs/authentication#how-to-find-the-api-key-or-token-in-the-app), and a [Template ID](https://docs.inkit.com/docs/inkit-postcards-api#api-token-and-template-id) to send requests from CleverTap using webhook.
* You must have an account with CleverTap.

# Integrate CleverTap with Inkit

This process involves the following three major steps:

1. [Create Inkit Template](doc:inkit#create-inkit-template).
2. [Set Up a Webhook on CleverTap Dashboard](doc:inkit#set-up-a-webhook).
3. [Create a Webhook Campaign](doc:inkit#create-a-webhook-campaign).

## Create Inkit Template

To create the Inkit template:

1. [Create a Postcard template](https://docs.inkit.com/docs/create-a-template) on the Inkit dashboard, which can be used on the CleverTap dashboard for sending campaigns.
2. Copy the Template ID and save it for future use. You will need this Template ID when sending out the campaign from CleverTap.

<Image title="d2a2948-create_a_template_with_key.gif" alt={2149} className="border" border={true} src="https://files.readme.io/e0c55e7-d2a2948-create_a_template_with_key.gif" />

## Set Up a Webhook

To set up a webhook:

1. Navigate to *Settings* > *Engage* > *Channels* > *Webhooks* to create a webhook on the CleverTap dashboard. 
2. Click **+ Add Webhook**.

<Image title="Add a webhook.png" alt={3200} className="border" border={true} src="https://files.readme.io/01372a9-Add_a_webhook.png" />

3. Configure the webhook template by adding the following details and click **Create**:

<Image title="create webhook template.png" alt={2014} className="border" width="80%" border={true} src="https://files.readme.io/8dcbae6-create_webhook_template.png" />

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        <p>Field</p>
      </th>

      <th>
        <p>Description</p>
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>Name</p>
      </td>

      <td>
        <p>Enter the nickname for your webhook to uniquely identify the webhook.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Destination URL</p>
      </td>

      <td>
        <p>Enter the following URL:<br /><a href="https://internal.inkit.io/integrations/webhook">https\://internal.inkit.io/integrations/webhook</a> </p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Method</p>
      </td>

      <td>
        <p>Select the POST method from the dropdown.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Basic Authorization</p>
      </td>

      <td>
        <ul><li>Enter the following:<br />Inkit \<API Token></li><li>To obtain the API token, refer to <a href="https://docs.inkit.com/docs/authentication#how-to-find-the-api-key-or-token-in-the-app">Find API Key or Token in the App</a>.</li></ul>
      </td>
    </tr>
  </tbody>
</Table>

## Create a Webhook Campaign

To create a webhook campaign:

1. Click **Go To Editor** to create your message.
2. Select Custom JSON Body and use the following example to help structure your payload and enter the desired fields:

```json
{
  	"api_token": "Inkit <INKIT API TOKEN>",
  	"template_id": "<TEMPLATE ID>",
  	"first_name": "@Profile - First Name | default: "CleverTap"",
  	"last_name": "@Profile - LastName | default: "Partner"",
  	"email": "@Profile - Email | default: "integrations@clevertap.com",
  	"company": "@Profile - Custom_Key | default: "CleverTap "",
  	"phone" : "@Profile - Phone | default: "+919999999999 "",
  	"address_line_1": "@Profile - address | default: "607 W Dana St."",
  	"address_line_2": "@Profile - address | default: "Mountain View"",
  	"address_city": "@Profile - City Name | default: "CA" ",
  	"address_state": "@Profile - Custom_Key | default: "CA" ",
  	"address_zip": "@Profile - Pin Code | default: "94041" ",
  	"address_country": "@Profile - Country | default: "United States""
}
```

<Image title="Define the campaign content.png" alt={3150} className="border" width="80%" border={true} src="https://files.readme.io/8be8c4d-Define_the_campaign_content.png" />

To learn more about creating a webhook, refer to [Create a Webhook Campaign](doc:create-message-webhook).

> 📘 Uploading Custom User Properties
>
> First Name, Last Name, Company, Address Line 1, Address Line 2, Address City, Address State, Address Zip, and Country are the custom user properties. You need to push it for every user using [API](https://developer.clevertap.com/docs/upload-user-profiles-api), [CSV upload](doc:csv-upload), [SDK](https://developer.clevertap.com/docs/clevertap-sdks#mobile-sdks), or [SFTP](https://developer.clevertap.com/docs/imports-via-sftp).
