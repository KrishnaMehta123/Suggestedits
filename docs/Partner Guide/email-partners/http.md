---
title: HTTP
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

CleverTap supports integrating any Email Service Provider (ESP) using the HTTP protocol to send Email campaigns.

It also tracks delivery failures through callbacks, allowing you to monitor issues under Errors in campaign stats and include them in exports and reports.

# Integrate Generic HTTP Provider

To integrate the ESP with CleverTap, follow these steps:

1. Go to *Settings* > *Email* from the dashboard and click **+ Provider**.
2. Select *Generic HTTP* from the *Provider* dropdown.
3. Enter the following details:

| Field                    | Description                                                                                                                                                                                                                                                         |
| :----------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Nickname                 | A unique name to identify your HTTP configuration within the CleverTap dashboard.                                                                                                                                                                                   |
| Callback URL             | The URL where callbacks for tracking events like delivered and delivery related failure will be sent. It is non-editable, and the option to copy the callback URL is available.                                                                                     |
| Request Type             | Dropdown to choose the type of HTTP request (GET and POST).                                                                                                                                                                                                         |
| HTTP endpoint            | The URL endpoint of your HTTP endpoint.                                                                                                                                                                                                                             |
| Authentication           | Type dropdown: Option to choose between *No Authentication* or *Basic Authentication*. In case of *Basic Authentication*, enter the Username and Password values that must be your HTTP credentials needed to connect to the service.                               |
| Default From Name        | The sender’s name will appear in the recipient's inbox, helping them identify the sender of the email.                                                                                                                                                              |
| Default From Address     | Enter the sender’s email address.                                                                                                                                                                                                                                   |
| Default Reply to Address | The email address where replies from recipients are sent to.                                                                                                                                                                                                        |
| Email Preference Center  | A landing page where users can [manage their email preferences](doc:manage-email-preferences), including opting out or subscribing to specific types of emails. You can select from the following options: *None*, *CleverTap Preference Center*, and *Custom URL*. |

4. Click **Save** to save your settings.
5. Click **Send a test email**. You will receive an email in your inbox after the setup is complete. If you do not receive the email, refer to [Troubleshooting](doc:generic-smtp-new#troubleshooting).

## Integration Setup

This section provides detailed guidance on setting up the **Generic HTTP Integration**, covering Authentication, Headers, and Parameters, including mandatory payload fields and batch processing for efficient API calls.

### 1. Authentication

Authentication is required to verify the identity of the sender before making HTTP requests to the provider.

* **No Authentication**: This option does not require any authentication credentials.

* **Basic Authentication**: Basic Authentication requires a **Username** and **Password** to authenticate the HTTP request.
  * **Username**: A field to enter the username for authentication.
  * **Password**: A field to enter the password for authentication.

### 2. Headers

Headers are essential for customizing HTTP requests by adding extra metadata to the request. They help manage authentication, content type, and other key information that the provider needs to process the request.

* **Custom Key-Value Pairs**: You can add custom headers as key-value pairs. This might include authentication tokens (e.g., **API keys**) or other essential data for the provider. Common headers include `Authorization` for API tokens, or `Content-Type` for specifying the body format (like JSON or XML). These headers are sent as part of the payload in the HTTP request.
  * **Enter parameter name**: Define the key (e.g., `Authorization`).
  * **Enter parameter value**: Define the value (e.g., `Bearer <your-api-key>`).

* **Dynamic Headers**: Dynamic headers are customizable placeholders that can be replaced with specific values during campaign setup. For example, **$$hid** is a custom placeholder that cannot be personalized at the user level, but its value can be set uniquely for each campaign.

   In this configuration, a single message record will be set up under the key `msgs`, and all the message body key-value pairs are used with user-level personalization. However, **$$hid** serves as a static placeholder that is replaced with a campaign-specific value during setup, ensuring consistency across all users in that campaign.

   For example, **$$hid** could be replaced with a promotion code or tracking ID that applies to the entire campaign, but each user will receive the same value for this placeholder.

### Parameters

Parameters define the body of the request (payload) and hold the data you need to send to the provider. Parameters are used in **POST** requests to send data, typically as a JSON payload. This payload will include the email content or other data that the provider will process.

The following dynamic placeholders can be used in both headers and parameters:

| Field             | Description                                                                    | Required  |
| ----------------- | ------------------------------------------------------------------------------ | --------- |
| **$$To**          | The recipient’s email address                                                  | Mandatory |
| **$$HTML**        | The HTML content of the email (replacement parameter during campaign creation) | Mandatory |
| **$$Subject**     | The subject of the email                                                       | Mandatory |
| **$$FromName**    | The sender's name                                                              | Mandatory |
| **$$FromAddress** | The sender's email address                                                     | Mandatory |

In addition to these, CleverTap supports other dynamic values such as:

| Placeholder | Description                                                |
| ----------- | ---------------------------------------------------------- |
| `$$hid`     | Static campaign-level value (e.g., tracking or promo code) |

### Using Dynamic Body Parameters in Campaign Setup

Dynamic parameters serve as placeholders configured during provider setup and are assigned actual values during campaign creation. This enables campaign-specific customization while keeping the payload template consistent.

**Example payload structure with dynamic parameters:**

```json
{
  "to": "$$To",
  "subject": "$$Subject",
  "fromName": "$$FromName",
  "fromAddress": "$$FromAddress",
  "htmlContent": "$$HTML",
  "trackingId": "$$hid",
  "userName": "{{profile.name}}"
}
```

#### Assigning Values During Campaign Creation

1. Go to **Engage > Campaigns** and click **+ Campaign**.
2. Select **Email** and choose your configured **Generic HTTP** provider.
3. In the **What** step, you’ll be prompted to provide values for campaign-level placeholders (e.g., subject, from name, `$$hid`).
4. CleverTap will automatically resolve profile-level dynamic values (e.g., `{{profile.name}}`) at send time for each recipient.

This setup provides a flexible yet scalable way to personalize email content across campaigns using a single provider configuration.

> For details, refer to [Email Campaigns](https://docs.clevertap.com/docs/email-campaigns) and [Personalization](https://docs.clevertap.com/docs/personalization).

### Batching Option

The **Batch Parameter** checkbox allows you to send multiple instances of the same parameter in a single API call. This is useful for bulk operations (e.g., sending the same email to multiple recipients). The minimum number of records that can be batched is **2**, and the maximum number of records that can be batched in a single API call is **1000**.

* **Enter parameter name**: Define the key (e.g., `"to"`).
* **Enter number of instances**: Define how many instances of this parameter you want to include (e.g., send to multiple recipients).

#### **Example of Batching**:

```json
{
    "to": ["recipient1@example.com", "recipient2@example.com", "recipient3@example.com"],
    "subject": "Test Email",
    "body": "This is a test email."
}
```

This allows you to send the same email to multiple recipients in one API call.

# Generic HTTP Callbacks

Generic HTTP Callbacks provide insights into email delivery success, failures, and user interactions such as unsubscribes and spam reports. These callbacks are essential for optimizing email campaigns and improving user engagement. The following events are captured through HTTP callbacks:

* **Notification Failed Event**: This event captures delivery issues like hard and soft bounces, as well as spam reports and unsubscribes. The `type` parameter specifies the cause of the failure.
* **Profile Unsubscribes**: If a user unsubscribes, marks an email as spam, or experiences a hard bounce (but not a soft bounce), their profile is automatically unsubscribed from future communications. This triggers the **Channel Unsubscribed** event in CleverTap.

### Sending Callback Events

To send callback events to CleverTap, customers must send a **POST** request to CleverTap's Callback URL. You can find this URL under the **Provider Setup** tab in the Email Provider Settings section of your CleverTap dashboard.

### Payload Structure

```json
{
  "version": "v2",
  "events": {
    "failed": [
      {
        "type": "unsubscribed",
        "email": "user1@example.com",
        "meta": "user1@example.com|1568798080|1730714617|20241104|0|wzrk_default|-17005907|",
        "description": "Hard bounce detected"
      }
    ],
    "clicked": [
      {
        "type": "clicked",
        "email": "user6@example.com",
        "meta": "user6@example.com|1568798080|1730714617|20241104|0|wzrk_default|-17005906|",
        "description": "User clicked on the promotional link"
      }
    ]
  }
}
```

### Callback Payload Keys

| Key         | Description                                                                                 | Required |
| ----------- | ------------------------------------------------------------------------------------------- | -------- |
| version     | Payload version. Must be set to `v2` to track delivery and user events.                     | Yes      |
| event       | Event group. Supported values: `failed`, `clicked`.                                         | Yes      |
| type        | Event type (e.g., `hard_bounce`, `soft_bounce`, `spam`, `unsubscribed`, `clicked`).         | Yes      |
| email       | Email address of the recipient.                                                             | Yes      |
| meta        | Value to link the event back to the campaign and profile. Must match the sent HTTP payload. | Yes      |
| description | Additional context about the event.                                                         | No       |

### Event Mappings

* **Notification Failed**: Triggered when `type` is `hard_bounce` or `soft_bounce`. Appears under campaign error stats.
* **Channel Unsubscribed**: Triggered when `type` is `unsubscribed`, `spam`, or `hard_bounce`.
* **Clicked**: Tracked when `type` is `clicked` and reflected in campaign and provider stats.

### Response Codes

| Status Code | Description                        | Explanation                                                      |
| ----------- | ---------------------------------- | ---------------------------------------------------------------- |
| 200         | Success                            | The request was processed successfully.                          |
| 400         | Bad Request                        | One or more required parameters were missing or invalid.         |
|             | More than allowed events received. | The payload exceeded the maximum limit of 1000 events.           |
| 5xx         | Server Error                       | Internal CleverTap server issue. Contact support if it persists. |

**Sample Response:**

```json
{
    "TOTAL_EVENTS": 4,
    "PROCESSED_EVENTS": 4,
    "UNPROCESSED_EVENTS": []
}
```

### Handling Bounces and Unsubscribes

* **Soft Bounces**: Indicate temporary issues. Do not trigger unsubscription.
* **Hard Bounces**: Indicate permanent failure. Trigger automatic unsubscription.
* **Unsubscribes/Spam**: Automatically unsubscribe the user from future communication.

# Troubleshooting

* Ensure SPF and DKIM records are correctly configured.
* Some email providers (e.g., Gmail, Yahoo) may block test emails sent via your own SMTP gateway.
* Verify that your IP/domain is not blacklisted by spam services (e.g., Spamhaus).

> 📘 Note
>
> The Unsubscribe link does not function in test emails sent during campaign setup.
