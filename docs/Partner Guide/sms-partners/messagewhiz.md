---
title: MessageWhiz
excerpt: SMS Provider
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

[MessageWhiz](https://messagewhiz.com/)  is a global cloud communication platform that enables businesses to deliver SMS, WhatsApp, and voice messages worldwide. Integrating MessageWhiz with CleverTap allows you to send transactional and promotional SMS messages directly from CleverTap’s engagement dashboard.

This integration supports HTTP-based message delivery, delivery status tracking via DLR (Delivery Receipt), and event-based campaign triggering.

Here’s how businesses use MessageWhiz with CleverTap:

* _Send OTPs and Notifications_: Trigger instant messages for authentication or alerts.
* _Run Promotional Campaigns_: Deliver targeted offers to user segments based on behavioral triggers.
* _Re-engage Customers_: Automate reminders and follow-ups for inactive or dropped-off users.

Integrating MessageWhiz with CleverTap combines real-time messaging power with intelligent segmentation and journey orchestration.

# Prerequisites for Integration

Before integrating, ensure the following:

* You have an active **MessageWhiz account** with access to **Account ID**, **API Key** and **Sender ID** (approved by MessageWhiz).
* You have a **CleverTap account** with SMS setup enabled.
* Your account and templates comply with **local regulations** (for example, DLT in India).

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by MessageWhiz. The CleverTap and MessageWhiz integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [MessageWhiz](https://messagewhiz.com/contact-us/) for support and resolution.

# Integrate MessageWhiz with CleverTap

To integrate MessageWhiz with CleverTap, complete the following steps:

1. [Find MessageWhiz API Credentials](doc:messagewhiz#find-messagewhiz-api-credentials)
2. [Set Up CleverTap Dashboard](doc:messagewhiz#set-up-clevertap-dashboard)
3. [Send a Test SMS](doc:messagewhiz#send-a-test-sms)

## Find MessageWhiz API Credentials

To set up the integration, gather your credentials from the MessageWhiz portal:

* **API Key**: Used for authentication in the request header.
* **Account ID**: Unique identifier for your MessageWhiz account.
* **Sender ID**: The alphanumeric name or number registered for sending SMS.

To retrieve these details:

1. Log in to your [MessageWhiz Portal](https://portal.messagewhiz.com/) .
2. Go to _Settings_ > _API Settings_.
3. Copy the **API Key**, **Account ID**, and **Sender ID**.

For additional details, refer to the [MessageWhiz API Documentation](https://sms.messagewhiz.com/api-doc) where you can view authentication setup, request parameters, and usage examples.

## Set Up CleverTap Dashboard

Set up the CleverTap dashboard to connect and authenticate the MessageWhiz SMS provider. To configure the CleverTap dashboard:

1. Go to _Settings_ > _Engage_ > _Channels_ > _SMS_ in the CleverTap dashboard.
2. Click **+ Add Provider**. The Add SMS provider page opens.

<Image align="center" alt="Add Provider" border={true} caption="Add Provider" src="https://files.readme.io/8ca98feff96deb7a4d4b6c4a0576f0b108f3d696f98dfbaa9b61faca58641cf2-image.png" width="65% " />

3. Under **Provider**, select _Other (Generic)_ and enter the following details:

<Table>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Value
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Nickname
      </td>

      <td>
        Enter a unique name, such as `MessageWhiz_SMS`.
      </td>
    </tr>

    <tr>
      <td>
        Callback URL
      </td>

      <td>
        Enter this URL in the MessageWhiz portal to receive delivery reports. Refer to [Set Up SMS Callbacks](doc:messagewhiz#set-up-sms-callbacks).
      </td>
    </tr>

    <tr>
      <td>
        Request Type
      </td>

      <td>
        Select `POST`
      </td>
    </tr>

    <tr>
      <td>
        HTTP Endpoint
      </td>

      <td>
        Paste the MessageWhiz API endpoint: `https://sms.messagewhiz.com/sms`
        Ensure that the URL is in HTTPS format, that is, your URL must begin with `https://.`
      </td>
    </tr>

    <tr>
      <td>
        Authentication
      </td>

      <td>
        Select `No Authentication` (authentication will be handled via headers).
      </td>
    </tr>
  </tbody>
</Table>

4. Enter the following details under the _Headers_ section.

| Key           | Value                        |
| ------------- | ---------------------------- |
| Authorization | `<YOUR_MESSAGEWHIZ_API_KEY>` |
| Content-Type  | `application/json`           |

> 📘 Note
>
> Ensure the API key is copied exactly as shown in your MessageWhiz dashboard.
> Incorrect keys will result in a `401 Unauthorized` response.

<Image align="center" alt="Set Headers" border={true} caption="Set Headers" title="Set Headers" src="https://files.readme.io/2d150958aebb2dd35c5b3971d8cca19650dd768e4b387c106c726777c9adfb2e-image.png" width="65% " />

5. Under _Parameters_, select `JSON` as the request type for the `POST` request. Refer to the sample payload below for the expected structure.

##### Sample Payload Structure (JSON)

```json
{
  "from": "<Your Sender ID>",
  "to": "$$To",
  "text": "$$Body",
  "client_ref": "$$MessageID",
  "callback": "<CleverTap Callback URL>"
}
```

Explanation of variables:

| Parameter    | Description                                                    | Required |
| ------------ | -------------------------------------------------------------- | -------- |
| `from`       | Sender ID registered in MessageWhiz.                           | Yes      |
| `to`         | Recipient’s mobile number. Use `$$To` for dynamic replacement. | Yes      |
| `text`       | Message text content. Use `$$Body`.                            | Yes      |
| `client_ref` | Unique message ID (CleverTap replaces this dynamically).       | Yes      |
| `callback`   | CleverTap Delivery Report Callback URL.                        | Optional |

6. Select the Batch checkbox and fill in the details as required.

> 📘 Single Batch Limit
>
> A single batch can have a maximum of 1,000 records.

7. Click on **Save**. A pop-up box will appear, prompting you to [Send Test SMS](doc:messagewhiz#send-test-sms).

## Send Test SMS

Sending a test SMS helps confirm that your MessageWhiz integration is working before launching a live campaign. This ensures the API endpoint is correctly configured, authentication is valid, and messages can be delivered.

To verify that the integration works:

1. Click the **Send Test SMS** hyperlink before creating SMS campaigns and journeys.
2. Enter the following details:  
   * _Country Code and Mobile Number_: Enter the country code and mobile number to which you want to send the message.
   * _Message_: Enter sample text, such as `This is a test message powered by MessageWhiz.`

<Image align="center" alt="Send a Test SMS" border={true} caption="Send a Test SMS" src="https://files.readme.io/58adde1828bfba405e3cca9f4290259ed2176abeaaad5e0f7218ff2e142c23ef-4141da97af121d16805772fb980f0888272958269467d79efd1a0a9f5f7c7dab-image.png" width="65% " />

3. Click **Send Test**.

If the configuration is correct, the test message will be delivered, and MessageWhiz will return a DLR update. If there is an error (for example, incorrect credentials or endpoint), CleverTap will display a failure notification.

### Set Up SMS Callbacks

To track SMS requests, copy the Delivery report callback URL from CleverTap and add it in the JSON payload

1. You can find the Delivery report callback URL on the CleverTap dashboard under the Provider  
   Setup page _Settings_ > _Channels_ > _SMS_ > _Provider Nickname_.
2. Add it to the JSON payload.

<Image align="center" alt="Set Up SMS Callbacks" border={true} caption="Set Up SMS Callbacks" src="https://files.readme.io/27be1e248b9101270026cf9be1bc09c56248d3f3b3c6cbbb4feef98e3bb6c85f-image.png" width="65% " />

### Verifying Successful Integration

Your integration is considered successful when the following criteria are met:

* The test SMS is delivered to the intended mobile number.
* You receive a DLR (Delivery Report) callback from MessageWhiz at the configured CleverTap callback URL, indicating delivery, failure, or queue status.
* CleverTap logs show no errors related to authentication, payload structure, or message transmission.

Once these conditions are met, you can proceed to build and launch [SMS campaigns](doc:create-message-sms) or set up [Journeys](doc:journeys) using MessageWhiz as your SMS provider.
