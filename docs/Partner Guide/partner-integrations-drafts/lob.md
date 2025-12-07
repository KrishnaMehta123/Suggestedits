---
title: Lob
excerpt: Direct Mail
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

[Lob](https://www.lob.com/) is a platform that enables automated direct mail at scale. It allows businesses to send personalized physical mail, such as letters, postcards, and checks, through simple API requests. This capability enables easy connection between online user journeys and offline engagement touchpoints.

Integrating Lob with CleverTap, marketers and product teams can trigger direct mail campaigns directly from CleverTap using webhooks. For instance, when a user completes a purchase or becomes inactive, CleverTap can send a real-time API call to Lob to automatically send a mail, such as a postcard, thank-you note, or coupon.

With this integration, you can:

* Re-engagement: Automatically send postcards to users who have not interacted in a set period.
* Lifecycle Marketing: Send printed coupons or thank-you letters after a purchase.
* Transactional Communication: Deliver physical invoices, payment reminders, or receipts.

# Prerequisites for Integration

The following are the prerequisites:

* Access to your Lob Dashboard.
* A valid Lob API Key available under *Settings* > *API Keys* in Lob.
* Access to your CleverTap Dashboard with permission to create Webhook campaigns.

# Integrate Lob with CleverTap

This section explains how to connect CleverTap and Lob step by step. You’ll select the appropriate Lob API endpoint, configure a webhook in CleverTap, and create a campaign that triggers mail when user conditions are met.

1. [Select Lob API Endpoint](doc:lob#select-lob-api-endpoint)
2. [Set Up Webhook in CleverTap](doc:lob#set-up-webhook-in-clevertap)
3. [Create Webhook Campaign in CleverTap](doc:lob#create-webhook-campaign-in-clevertap)

## Select Lob API Endpoint

Before setting up the CleverTap connection, identify which Lob API endpoint you plan to use. Each mail type—postcards, letters, or checks—uses a specific endpoint.

For this guide, we’ll use the *Postcards API endpoint* as an example.

#### Example Endpoint:

```
https://api.lob.com/v1/postcards
```

Refer to the [Lob API Documentation](https://docs.lob.com/) for a complete list of endpoints and to confirm the one that applies to your use case (letters, checks, and so on).

## Set Up Webhook in CleverTap.

Set up the webhook connection that will transmit your campaign data from CleverTap to Lob. The webhook ensures that when certain conditions are met in CleverTap, Lob receives a properly formatted API request.

To configure the webhook:

1. Go to *Settings* > *Channels* > *Webhooks* from the CleverTap dashboard.
2. Click **+ Add Webhook** and provide a meaningful name for the webhook.
3. In the *Create webhook template*, enter the following details:

| Field               | Description                             | Example / Value                    |
| ------------------- | --------------------------------------- | ---------------------------------- |
| **Name**            | Enter a descriptive webhook name        | `Lob Postcard Webhook`             |
| **HTTP Method**     | The request type used to send data      | `POST`                             |
| **Destination URL** | The Lob API endpoint for your mail type | `https://api.lob.com/v1/postcards` |

4. Enable **Basic Authorization** and enter the username and password provided by Lob.
5. Click **Save**.

<Image alt="Create Webhook" align="center" width="75% " border={true} src="https://files.readme.io/0a659c358f4452b3b10c66a69de148572a45f20a3ae8c7cf7b74a9f6c56b8084-image.png">
  Create Webhook
</Image>

This webhook acts as a secure connection between CleverTap and Lob. It ensures that your campaign data is transmitted safely and formatted correctly for Lob’s API.

## Create Webhook Campaign in CleverTap

After setting up your webhook, the next step is to create a Webhook Campaign. This campaign determines when and how the webhook will be triggered. You can use this to send mail based on user behavior, profile attributes, or event triggers.

To configure the campaign:

1. Go to *Campaigns* on the CleverTap dashboard, click **+ Campaign** and select *Webhook* from the list of messaging channels.

<Image alt="Create Webhook Campaign" align="center" width="85% " border={true} src="https://files.readme.io/76f4ef966fa70f3987fa3aa1004b16beb31953f3ecbc68b99b874b7f046c2da9-image.png">
  Create Webhook Campaign
</Image>

2. Configure the following campaign settings: qualification criteria, target segment, and delivery preferences.
3. Under the *What* section, select the webhook created in [Set Up Webhook in CleverTap](doc:lob#set-up-webhook-in-clevertap).
4. Click **Go to Editor**, under the *Webhook Content* and enter the following details:
   * Content Format: `JSON`
   * Custom Body: Enter the request payload. Refer to the [sample request payload](doc:lob#example-request-payload).

<Image alt="Webhook Configuration" align="center" width="75% " border={true} src="https://files.readme.io/8141b202938f046e2db2004487ce0ea9ab9b8070e86ce2dfb8f25deb6988806b-image.png">
  Webhook Configuration
</Image>

### Example Request Payload

This payload structure defines what data will be sent to Lob when the webhook is triggered. It includes user-specific details, such as name, address, and profile information, from CleverTap.

```json
{
  "description": "CleverTap Postcard Test",
  "to": {
    "name": "{{ Profile.name | default: 'User' }}",
    "address_line1": "{{ Profile.address | default: '123 Main Street' }}",
    "address_city": "{{ Profile.city | default: 'San Francisco' }}",
    "address_state": "{{ Profile.state | default: 'CA' }}",
    "address_zip": "{{ Profile.zip | default: '94107' }}",
    "address_country": "{{ Profile.country | default: 'US' }}"
  },
  "from": {
    "name": "CleverTap Marketing Team",
    "address_line1": "210 King St",
    "address_city": "San Francisco",
    "address_state": "CA",
    "address_zip": "94107",
    "address_country": "US"
  },
  "front": "tmpl_fac4fdc69acd22c",
  "back": "tmpl_fac4fdc69acd22c",
  "mail_type": "usps_first_class",
  "merge_variables": {
    "name": "{{ Profile.name | default: 'User' }}"
  }
}
```

> ⚠️ Note
>
> * Make sure that your Creative Template ID in Lob (e.g., postcard, letter) is valid and corresponds to the `front` and `back` values above.
> * You can use Liquid tags (`{{ }}`) to dynamically personalize your postcard or letter content using CleverTap profile data.

5. Click **Preview & Test** in CleverTap to send a sample request to Lob.

<Image alt="Preview & Test" align="center" width="75% " border={true} src="https://files.readme.io/ff8ea7386a76173ac0826979fccc7284333f1ef7dab29338a152f871bbda2310-image.png">
  Preview & Test
</Image>

### Verify Integration in Lob

After configuring the webhook campaign, verify that CleverTap and Lob are communicating correctly. This step ensures that CleverTap’s trigger successfully reaches Lob and that the intended mail item (for example, a postcard or letter) is created as expected.

1. Log in to your Lob Dashboard and check *API Requests* > *API Logs* to confirm the request was received.
2. Go to *Print & Mail* > *Postcards* to verify that the postcard has been created.

<Image alt="Verify Integration in Lob" align="center" width="75% " border={true} src="https://files.readme.io/8937242092638442340e8fc32083a7a3a5663475a174d4166585ca130c7bd349-image.png">
  Verify Integration in Lob
</Image>

3. Once confirmed, go back to CleverTap and click **Publish** to make the campaign live.

<Image alt="Publish Campaign" align="center" width="76% " border={true} src="https://files.readme.io/2004e7a58d05b7e46acd09bb4c06d6a6d12278d3606ca6d694eafe4b9d22c8c7-image.png">
  Publish Campaign
</Image>

### Verification and Analysis

After publishing, verify the integration by checking both CleverTap and Lob logs. Analyze mail delivery success rates and timing to optimize future campaigns.

#### Recommended Checks:

* Confirm that Lob requests appear under **API Logs** with successful status codes.
* Review CleverTap campaign delivery metrics for trigger validation.
* Ensure personalization data (name, address, or variables) appear correctly in printed mail.

<Image alt="Lob API Logs page" align="center" width="75% " border={true} src="https://files.readme.io/361d7f3b79cf6d9fe3d297f27ba922c0ccf0fb1bcd63b7a6419a8c24238c69dd-2025-12-01_11-31-58_1.gif">
  Lob API Logs page
</Image>
