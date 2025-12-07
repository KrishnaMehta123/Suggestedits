---
title: Mailmodo
excerpt: Email
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

[Mailmodo](https://www.mailmodo.com/) is a no-code email marketing platform that allows you to create and send **interactive emails** with app-like experiences inside inboxes. It offers features such as interactive widgets (forms, calendars, surveys), automation, and AI-powered content tools designed to improve engagement and conversions.

Integrating Mailmodo with CleverTap, you can:

- Trigger Mailmodo campaigns directly from CleverTap using Webhooks.
- Sync campaign activity data back into CleverTap as custom events.
- Build segments, flows, or dashboards in CleverTap using Mailmodo engagement data.
- Personalize and automate follow-up campaigns across multiple channels.

For example, you can trigger a Mailmodo survey campaign from CleverTap and then use responses or non-engagement signals (such as unopened emails) to launch push notifications, SMS, or other follow-up campaigns in CleverTap.

# Prerequisites for Integration

Ensure you have the following before setting up the integration:

- An active Mailmodo account.
- A CleverTap account with a valid **Project ID** and **Passcode**.
- Access to Webhook configuration in CleverTap.

# Integrate Mailmodo with CleverTap

The integration involves the following three major steps:

1. [Configure Mailmodo with CleverTap](doc:mailmodo#configure-mailmodo-with-clevertap)
2. [Set Up Trigger Campaigns in Mailmodo](doc:mailmodo#set-up-trigger-campaigns-in-mailmodo)
3. [Set Up CleverTap Webhooks](doc:mailmodo#set-up-webhooks-in-clevertap)

# Data Is Synced Between CleverTap and Mailmodo

Once the integration is enabled, for every campaign triggered from CleverTap, Mailmodo pushes the following activity data back into CleverTap as **custom events**:

| Event Name                            | Description                                                           |
| ------------------------------------- | --------------------------------------------------------------------- |
| **MM Email Opened**                   | Sent when a recipient opens an email triggered from Mailmodo.         |
| **MM Email Link Clicked**             | Sent when a recipient clicks a link inside a Mailmodo email.          |
| **MM Email Form Submitted**           | Sent when a recipient submits an AMP form or widget inside the email. |
| **MM `Template Name` Form Submitted** | Sent with detailed form responses when a form or widget is submitted. |
| **MM Email Bounced**                  | Sent when a triggered email bounces for a recipient.                  |
| **MM Email Unsubscribed**             | Sent when a recipient unsubscribes from a Mailmodo email.             |
| **MM Email Marked as Spam**           | Sent when a Mailmodo email is marked as spam by the recipient.        |

Each event also includes **additional properties** (campaign name, subject line, campaign type, email type, and so on.) to help filter and analyze campaign performance inside CleverTap.

> 🚧 Important
> 
> Mailmodo requires the `CleverTap user_id` of the recipients to push data back correctly. Ensure that the `clevertap_id` property is set in the JSON body when setting up the trigger campaign in CleverTap.

## Configure Mailmodo with CleverTap

Link your Mailmodo account with CleverTap. To do so, perform the following steps:

1. In your Mailmodo dashboard, go to _Integrations_.

2. Under _Available for Connection_, find _CleverTap_ and click **Click to authenticate**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1786728896fe38673f1871736f13cbe8bb1cefec79c354c304fbc195fa77b1e5-image.png",
        null,
        "Authenticating CleverTap Integration"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Authenticating CleverTap Integration"
    }
  ]
}
[/block]


3. Select your [REST API Host](https://developer.clevertap.com/docs/idc) from the dropdown.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9bf957512f2380fa1f19447326abf3114bc6732a741caa04f5a50850aa988a07-image.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true
    }
  ]
}
[/block]


4. Enter your **Project ID** and **Passcode** (available in your CleverTap Settings page).
5. Click **Test and Save**. A _Setup successful_ message confirms the integration.

For testing, Mailmodo sends a sample event (`MM Email Opened`) with `user_id = hello@mailmodo.com` to CleverTap. You can verify this event in your CleverTap dashboard.

## Set Up Trigger Campaigns in Mailmodo

Once your accounts are connected, you can design and activate campaigns in Mailmodo that CleverTap will trigger:

1. In Mailmodo, create or select a _Template_ for your campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0e48de5a70867b26b6522078cb42a4a1f40ea61572174d566f8daa00b95d9f3c-Screen_Recording_2025-07-03_at_3.29.59_PM_1.gif",
        "",
        "Create or Select Template"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Create or Select Template"
    }
  ]
}
[/block]


2. Go to _Campaigns_ > _Triggers_  > **+ Create Trigger Campaign**.
3. Select your template, configure campaign details, and proceed to the next step.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8a9029cba808801ca0c93cec99de9029f237aede752228ba6ab23bde9cfba94b-Screen_Recording_2025-07-03_at_3.32.21_PM_1.gif",
        "",
        "Create Trigger Campaign"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Create Trigger Campaign"
    }
  ]
}
[/block]


4. Under _Trigger App_, select **CleverTap**.
5. Review configuration, then click **Enable Campaign**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/528e9b53b10985578cc97b0afe9b02bd343b9a1c8d3c9d2eb6a769aaf7f3c090-Screen_Recording_2025-07-03_at_3.34.10_PM_1.gif",
        "",
        "Configuring Trigger Campaign with CleverTap"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Configuring Trigger Campaign with CleverTap"
    }
  ]
}
[/block]


6. Once enabled, click **Show Setup Steps** to view the _Webhook URL_ and _JSON Body_. Copy both, as you’ll need them in CleverTap.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ad8c41b1691dd5a95e3f9df1985aa4d246053b8fa4d56f63f3fd9bec156f6f51-Screen_Recording_2025-07-03_at_3.37.36_PM_1.gif",
        "",
        "Webhook URL and Body"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Webhook URL and Body"
    }
  ]
}
[/block]


## Set Up Webhooks in CleverTap

To ensure CleverTap can trigger Mailmodo campaigns, you need to configure a Webhook in CleverTap using the URL and Body obtained from Mailmodo.

### Configure the Webhook

Set up a Webhook in CleverTap using the URL provided by Mailmodo. This allows CleverTap to call Mailmodo whenever a campaign is triggered. To do so, perform the following steps:

1. In your CleverTap dashboard, go to _Settings_ > _Channels_  >  _Webhook_ > **+ Webhook**.
2. Provide a descriptive name for the Webhook (for example, _Mailmodo Trigger_).
3. Set the HTTP method to _POST_.
4. Paste the _Webhook URL_ copied from _step 6_ of [Set Up Trigger Campaigns in Mailmodo](doc:mailmodo#set-up-trigger-campaigns-in-mailmodo).
5. Click **Save**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/87223e8f928c6c641c71b4f4402364772a901b5825d7a472cd9c03a3c17b6727-image.png",
        null,
        "Webhook Setup in CleverTap"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Webhook Setup in CleverTap"
    }
  ]
}
[/block]


### Create a Webhook Campaign in CleverTap

Once the Webhook is configured, create a campaign that uses it. This ensures CleverTap can send campaign data (including `clevertap_id`) to Mailmodo in real time. To do so, perform the following steps:

1. In CleverTap, go to _Campaigns_ > _+ Campaign_ > _Webhook_.
2. Enter campaign details.
3. In the **What** section, select **Custom Body**.
4. Paste the JSON Body copied from _step 6_ of [Set Up Trigger Campaigns in Mailmodo](doc:mailmodo#set-up-trigger-campaigns-in-mailmodo).

Replace static values with dynamic [Liquid tags](doc:personalize-message-all#liquid-tags) to personalize the email. For example:

```json
{
  "email": "${user_email}",
  "data": {
    "first_name": "${first_name}",
    "subscription_plan": "${plan_type}"
  }
}
```

- `${user_email}` is replaced dynamically with each recipient’s email address.
- Additional properties (such as `first_name`, `plan_type`) can be added inside `data` for more personalization.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e16948b8581c4fa1a33c0a722723ec2ce08d7f699e56ecf167e79472b2597119-image.png",
        null,
        "Liquid Tags in Webhook Body"
      ],
      "align": "center",
      "border": true,
      "caption": "Liquid Tags in Webhook Body"
    }
  ]
}
[/block]


### Publish the Campaign

Publishing the campaign activates the connection. Once live, Mailmodo sends engagement data (opens, clicks, unsubscribes, form submissions) back to CleverTap as custom events tied to the user profile.

- CleverTap sends campaign data (email ID, `clevertap_id`) to Mailmodo.
- Mailmodo triggers the configured email to the recipient.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/660ad1e11fc14bc903172f2c274f314d1ad42936efb38c151871bc8034ffeb39-image.png",
        null,
        "Email Response"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Email Response"
    }
  ]
}
[/block]


- Mailmodo sends campaign engagement events (opens, clicks, unsubscribes, form submissions) back into CleverTap as **custom events** tied to the recipient’s profile.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/24ce9fc8094d179938e04abe12279966d42abc31423eb24e66541ba2166cbd9b-image.png",
        null,
        "CleverTap dashboard showing tracked custom events"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "CleverTap dashboard showing tracked custom events"
    }
  ]
}
[/block]


# FAQs

### How do CleverTap and Mailmodo work together?

This example shows the end-to-end flow of the integration:

- A CleverTap Webhook campaign triggers a Mailmodo interactive survey email.
- The recipient opens and submits the survey.
- Mailmodo sends **MM Email Opened** and **MM Email Form Submitted** events to CleverTap.
- CleverTap logs these events under the user’s profile, enabling segmentation and automated follow-ups (for example, sending an SMS to non-respondents).