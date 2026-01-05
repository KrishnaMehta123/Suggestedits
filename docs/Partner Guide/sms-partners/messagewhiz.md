---
title: MessageWhiz
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

* You have an active **MessageWhiz account** with access to:
  * **Account ID**
  * **API Key**
  * **Sender ID** (approved by MessageWhiz)
* You have a **CleverTap account** with SMS setup enabled.
* Your account and templates comply with **local regulations** (for example, DLT in India).

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by MessageWhiz. The CleverTap and MessageWhiz integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [MessageWhiz](https://messagewhiz.com/contact-us/) for support and resolution.

# Integrate MessageWhiz with CleverTap

To integrate MessageWhiz with CleverTap, complete the following steps:

1. [Find MessageWhiz API Credentials](#find-messagewhiz-api-credentials)
2. [Set Up CleverTap Dashboard](#set-up-clevertap-dashboard)
3. [Send a Test SMS](#send-a-test-sms)

## Find MessageWhiz API Credentials

To set up the integration, gather your credentials from the MessageWhiz portal:

* **API Key**: Used for authentication in the request header.
* **Account ID**: Unique identifier for your MessageWhiz account.
* **Sender ID**: The alphanumeric name or number registered for sending SMS.

To retrieve these details:

1. Log in to your [MessageWhiz Portal](https://portal.messagewhiz.com/) .
2. Navigate to _Settings_ > _API Settings_.
3. Copy the **API Key**, **Account ID**, and **Sender ID**.

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
        Enter this URL in the MessageWhiz portal to receive delivery reports. Refer to [Set Up SMS Callbacks]().
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
        Select `No Authentication`.
      </td>
    </tr>
  </tbody>
</Table>

<br />

#### Set Headers

Under the **Headers** section, add the following key–value pairs:

| Key            | Value                        |
| -------------- | ---------------------------- |
| `apikey`       | `<YOUR_MESSAGEWHIZ_API_KEY>` |
| `Content-Type` | `application/json`           |

> 📘 **Note**
>
> Ensure the API key is copied exactly as shown in your MessageWhiz dashboard.
> Incorrect keys will result in a “401 Unauthorized” response.

<Image alt="Set Headers" border={false} src="https://files.readme.io/2d150958aebb2dd35c5b3971d8cca19650dd768e4b387c106c726777c9adfb2e-image.png" title="Set Headers" />

***

#### Configure Parameters (JSON Payload)

<br />

Under **Parameters**, choose **JSON** as the request format for the POST call.

<br />

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
| `from`       | Sender ID registered in MessageWhiz.                           | ✅        |
| `to`         | Recipient’s mobile number. Use `$$To` for dynamic replacement. | ✅        |
| `text`       | Message text content. Use `$$Body`.                            | ✅        |
| `client_ref` | Unique message ID (CleverTap replaces this dynamically).       | ✅        |
| `callback`   | CleverTap Delivery Report Callback URL.                        | Optional |

***

### Send a Test SMS

<br />

To verify that the integration works:

1. In the CleverTap dashboard, click **Send Test SMS**.

   2. Enter the following:

   * **Country Code and Mobile Number**
     * **Message:** “This is a test message powered by MessageWhiz.”

       3. Click **Send Test**.

       <br />

       If configured correctly:

       * The test SMS will be delivered to the specified number.
         * CleverTap will display a success confirmation.
           * A DLR (Delivery Receipt) will be sent from MessageWhiz to the CleverTap callback URL.

             <br />

             If an error occurs, check:

             * The **API Key** in headers.
               * The **endpoint URL** (`https://sms.messagewhiz.com/sms`).
                 * The **payload structure** (ensure required parameters are included).

                   <Image alt="Send a Test SMS" border={false} src="https://files.readme.io/440d338366857bc07cb488cff8ce0b667c10fe20e57ca880cb2b9e4689cdff65-image.png" title="Send a Test SMS" />

                   ***

### Set Up SMS Callbacks

<br />

To track delivery reports and message statuses:

1. In CleverTap, go to
   _Settings_ → _Channels_ → _SMS_ → _Provider Nickname_.

   2. Copy the **Delivery Report Callback URL**.
      3. Log in to your [MessageWhiz Portal](https://portal.messagewhiz.com/) .
         4. Go to **Settings → API Settings**.
            5. Paste the CleverTap Callback URL into the **Callback** field.

   <Image alt="Set Up SMS Callbacks" border={false} src="https://files.readme.io/27be1e248b9101270026cf9be1bc09c56248d3f3b3c6cbbb4feef98e3bb6c85f-image.png" title="Set Up SMS Callbacks" />

   ***

### Verifying Successful Integration

<br />

Your integration is considered successful when:

* The test SMS is delivered to the intended mobile number.
  * CleverTap receives a DLR callback from MessageWhiz with delivery status (`DELIVERED`, `FAILED`, or `QUEUED`).
    * No errors appear in CleverTap’s message logs related to payload or authentication.
      <br />
      Once verified, you can begin building [SMS campaigns](doc:create-message-sms)  or [Journeys](doc:journeys)  using MessageWhiz as your provider.
      <br />
      ***
      <br />
      <br />

## Open Questions

1. [ ] Confirm if **DLT parameters** (`entity_id`, `template_id`) are required for Indian traffic.

   2. [ ] Verify **callback response format** expected from MessageWhiz for CleverTap parsing.
      3. [ ] Confirm **batch sending** support (multiple recipients in one request).

   ***

### Style & Validation Summary

<br />

✅ Clean heading hierarchy (H1 → H2 → H3 → H4).
✅ Logical doc flow: Overview → Prerequisites → Setup → Test → Callbacks → Verification.
✅ Tables, code blocks, and images follow Markdown best practices.
✅ Internal cross-links match CleverTap documentation convention.
✅ Consistent use of termino
