---
title: Generic SMTP
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
## Overview

While we highly recommend using a reputable email service provider (ESP) such as Amazon SES, Postmark, or SendGrid, you can also integrate any other SMTP gateway to send emails.

# Set Up SMS Provider

This process involves the following three major steps:

1. [Set Up CleverTap dashboard](https://docs.clevertap.com/docs/generic-smtp#set-up-clevertap-dashboard).
2. [Handle Bounces](https://docs.clevertap.com/docs/generic-smtp#handle-bounces).
3. [Handle Unsubscriptions](https://docs.clevertap.com/docs/generic-smtp#handle-unsubscriptions).

## Set Up CleverTap Dashboard

To set up the CleverTap dashboard:

1. Navigate to *Settings* > *Email* from the dashboard and click **+ Provider**.
2. Select *SMTP* from the *Provider* dropdown.
3. Enter the following details:

| Field                 | Description                                                                                                              |
| :-------------------- | :----------------------------------------------------------------------------------------------------------------------- |
| Host                  | In the *Host* text box, fill your publicly accessible IP address or hostname of your SMTP server                         |
| Port                  | In the *Port* text box, fill in your SMTP port.                                                                          |
| Username and Password | *Username* and *Password* values must be your SMTP credentials needed to connect to the service.                         |
| From Address          | *From Address* value is the sender’s email address. Most people will not open an email unless they recognize the sender. |

4. Click **Save** to save your settings.
5. Click **Send a test email**. You will receive an email in your inbox after the setup is complete. If you do not receive the email, refer to [Troubleshooting](https://docs.clevertap.com/docs/generic-smtp#troubleshooting).

<details> 

<summary>New Version</summary>

The new version introduces more detailed events with richer metadata and tracking. It includes additional events for notification failures (e.g., hard bounce, spam) and profile unsubscriptions (e.g., hard bounces, spam complaints). These events are now automatically raised to ensure accurate tracking of delivery failures and user status changes.

* **Notification Failure Event**: For all event types except unsubscribed, a notification failed or bounce event will be raised to track delivery issues.
* **Profile Unsubscribe**: For all event types except soft\_bounce, the user profile will be automatically unsubscribed, and a channel unsubscribed event will be triggered to reflect this change.

These enhancements enable better tracking of failed delivery events and more automated profile management, ensuring a smoother user experience when dealing with invalid email addresses, bounces, or spam complaints.

## Capabilities of the New Version:

* **Automatic Notification Failure Events**: For all event types except unsubscribed, a notification failed event (e.g., bounce or failed notification)will be raised to track delivery issues such as hard bounces, soft bounces, and spam reports.
* **Profile Unsubscribes**: For all event types except soft bounce, the user profile will be automatically unsubscribed from future communications, and a channel unsubscribed event will be triggered.
* **Clear Event Categorization**: Events are grouped under Notification Failed event with specific event types like hard bounce, soft bounce, spam, and unsubscribed.
* **Real-Time Tracking**: Provides real-time insights into email delivery issues, user behavior (e.g., spam reports), and user profile status changes.

## Event Types in the New Version

The new version follows the structure for the email event reporting system, which includes different types of events related to email delivery and user interaction. Below is a detailed explanation of each event type represented in the payload.

### Unsubscribed Event (`type: unsubscribed`)

 This event is triggered when a user unsubscribes from receiving emails. This could happen via a direct unsubscribe link in the email or through the user’s account settings. It indicates that the recipient has opted out of future communications.

```json
{
  "type": "unsubscribed",
  "email": "user+callbackunsub1@example.com",
  "meta": "user+callbackunsub1@example.com|1568798080|1730714617|20241104|0|wzrk_default|-17005907|",
  "description": "user unsubscribed user+callbackunsub1@example.com"
}
```

* **`email`**: The email address that unsubscribed (`user+callbackunsub1@example.com`).
* **`meta`**: Metadata containing contextual information, such as timestamps and user/session details.
* **`description`**: A human-readable explanation of the event, which in this case states that the user unsubscribed from `user+smtp1@example.com`.

### Hard Bounce Event (`type: hard_bounce`)

This event is triggered when an email fails to be delivered due to a permanent issue, such as an invalid or non-existent email address. Hard bounces usually indicate that the email address is incorrect, and no further delivery attempts will be made for that email address.

```json
{
  "type": "hard_bounce",
  "email": "user+bounce3@example.com",
  "meta": "user+bounce3@example.com|1568798080|1730799638|20241105|0|wzrk_default|-17005910|",
  "description": "hard bounced user+bounce3@example.com"
}
```

* **`email`**: The email address that experienced the hard bounce (`user+bounce3@example.com`).
* **`meta`**: Metadata, such as timestamps and session information.
* **`description`**: A description of the event indicating that the email to `user+smtp2@example.com` resulted in a **hard bounce**.

### Soft Bounce Event (`type: soft bounce`)

This event is triggered when an email fails to be delivered due to a temporary issue, such as a full inbox, a temporary server error, or a network issue. Soft bounces generally result in a retry attempt to deliver the email.

```json
{
  "type": "soft_bounce",
  "email": "user+callbacksoft1@example.com",
  "meta": "user+callbacksoft1@example.com|1568798080|1730714617|20241104|0|wzrk_default|-17005905|",
  "description": "soft bounced user+callbacksoft1@example.com"
}
```

* **`email`**: The email address that experienced the soft bounce (`user+callbacksoft1@example.com`).
* **`meta`**: Metadata, which includes timestamps and other contextual information about the event.
* **`description`**: Describes the temporary nature of the bounce, noting that the email to `user+smtp3@example.com` resulted in a **soft bounce**.

### Spam Event (`type: spam`)

This event is triggered when an email is marked as spam by the recipient. This usually happens when the recipient actively reports the email as spam or junk in their email client. As a result, the email is flagged, and future communications may be blocked or filtered.

```json
{
  "type": "spam",
  "email": "user+callbackspam1@example.com",
  "meta": "user+callbackspam1@example.com|1568798080|1730714617|20241104|0|wzrk_default|-17005904|",
  "description": "spam user+callbackspam1@example.com"
}
```

* **`email`**: The email address that was marked as spam (`user+callbackspam1@example.com`).
* **`meta`**: Metadata containing timestamps and additional session details.
* **`description`**: The description that identifies this as a **spam** event for `user+smtp4@example.com`.

### Example Payload

```Text JSON
{
  "version": "v2",
  "events": {
    "failed": [
      {
        "type": "unsubscribed",
        "email": "user+callbackunsub1@example.com",
        "meta": "user+callbackunsub1@example.com|1568798080|1730714617|20241104|0|wzrk_default|-17005907|",
        "description": "hard bounced user+smtp1"
      },
      {
        "type": "hard_bounce",
        "email": "user+bounce3@example.com",
        "meta": "user+bounce3@example.com|1568798080|1730799638|20241105|0|wzrk_default|-17005910|",
        "description": "soft bounced user+smtp2"
      },
      {
        "type": "soft_bounce",
        "email": "user+callbacksoft1@example.com",
        "meta": "user+callbacksoft1@example.com|1568798080|1730714617|20241104|0|wzrk_default|-17005905|",
        "description": "unsubscribed user+smtp3"
      },
      {
        "type": "spam",
        "email": "user+callbackspam1@example.com",
        "meta": "user+callbackspam1@example.com|1568798080|1730714617|20241104|0|wzrk_default|-17005904|",
        "description": "spam user+smtp4"
      }
    ]
  }
}
```

<br />

### Summary of Event Types

The event types in the new version allow for better tracking and management of email delivery, as well as user interactions with emails. Here’s a recap of each event type:

| **Event Type**   | **Description**                                                                          | **Example Action**                  |
| ---------------- | ---------------------------------------------------------------------------------------- | ----------------------------------- |
| **unsubscribed** | Triggered when a user unsubscribes from emails.                                          | User opts out of future emails.     |
| **hard\_bounce** | Triggered when an email fails due to a permanent delivery issue (e.g., invalid address). | Delivery permanently failed.        |
| **soft\_bounce** | Triggered for temporary delivery failures (e.g., full inbox, server errors).             | Temporary failure, retry attempt.   |
| **spam**         | Triggered when a user marks an email as spam.                                            | Email flagged as spam by recipient. |

By monitoring these events, email senders can take the necessary actions to improve email deliverability, ensure compliance, and manage user engagement effectively.

</details> 

<details> 

<summary>Old Version</summary>

This old version provides the structure for handling email bounce and unsubscribe events via HTTP POST requests. The payload reports soft and hard bounces and user unsubscriptions.

### Handle Bounces

When a recipient’s email server rejects an email, it is called a bounce. There are two types of bounces: 

* Soft Bounces: Soft bounces typically indicate a temporary delivery issue to an address. Some reasons for a soft bounce could be that the recipient’s mailbox is full or the Mail Server is down. Soft bounces are included in the campaign reports; the users are not marked unsubscribed.
* Hard Bounces: A hard bounce indicates a permanent reason an email cannot be delivered. Hard bounces are included in the campaign reports; the users are marked as unsubscribed. 

To handle bounced email messages, you need to make an HTTP request to the callback URL specified under *Dashboard* > *Settings* > *Integration* > *Email* > *Setup provider tab* > *Nickname*.

Ensure that the request is be of type HTTP POST with the payload in the following format:

```json
// if you're not sure of the time of the bounce, just set it to the current epoch

[
    {
        "event": "softbounce",
        "data": [
            {
                "e": "email1@emailprovider.com",  // email id that soft bounced
                "ts": 1435322805                  // time of the bounce
            },
            {
                "e": "email2@emailprovider2.com", // email id that soft bounced
                "ts": 1435322805                  // time of the bounce
            }
        ]
    },
    {
        "event": "hardbounce",
        "data": [
            {
                "e": "email3@emailprovider.com",   // email id that hard bounced
                "ts": 1435322805
            }
        ]
    }
]
```

### Handle Unsubscriptions

To share unsubscription data from custom pages directly, you need to make an HTTP request to the callback URL that is specified in *Dashboard* > *Settings* >  *Channels* > *Email* > *Setup* tab. Ensure that the request is of type HTTP POST with the payload in the following format.

```json
// if you're not sure of the time of the unsubscribe, just set it to the current epoch

[
    {
        "event": "unsubscribe",
        "data": [
            {
                "e": "email1@emailprovider.com",  // email id of the user
                "ts": 1504632929                  // time of the unsubscribe
            },
            {
                "e": "email2@emailprovider2.com", // email id of the user
                "ts": 1500630929                  // time of the unsubscribe
            }
        ]
    }
]
```

For more information about handling unsubscription requests from users, refer to [Handling Unsubscribes](doc:handling-unsubscribes).

</details>

# Troubleshooting

* As you are using your SMTP gateway, some email providers, such as Gmail and Yahoo, might not deliver the email to your inbox.
* Check if you have set up DKIM and SPF correctly.
* Check if Spamhaus has blacklisted your IP/domain.

> 🚧 Unsubscription Link
>
> The unsubscription link does not work for test emails sent from the notification creation page.

# Errors

The following table lists the errors that you may encounter after sending a campaign:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Error
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        *SMTP invalid email ID*
      </td>

      <td>
        * \*Cause &#x31;**: The*SMTP invalid email ID* error occurs when the provided email address is not formatted correctly or does not exist. Typos or errors in the email address commonly cause this error. **&#x52;esolutio&#x6E;**: Double-check the email address and ensure the email ID is valid to fix this error.**&#x43;ause &#x32;**: This error can also occur if you are using a test email address.**&#x52;esolution\*\*: We recommend using an actual email address. Contact your ESP's customer support for further assistance if the issue persists.
      </td>
    </tr>

    <tr>
      <td>
        *SMTP dispatching failed*
      </td>

      <td>
        * \*Caus&#x65;**: The*SMTP dispatching failed* error occurs when the email message cannot be delivered to the recipient's email address.Some of the other common causes could be:<ul> <li>The email address that you are trying to send to is incorrect.</li> <li>The email address's domain is invalid.</li> <li>The recipient's ESP blocks your IP address.</li> <li>The ESP is experiencing a temporary outage.</li> </ul>**&#x52;esolution\*\*: To fix this error, you can check the recipient's email address and ensure that the email address is valid and that the email infrastructure is working correctly. If the issue persists, contact your provider's customer support.
      </td>
    </tr>

    <tr>
      <td>
        *SMTP connection error*
      </td>

      <td>
        * * Caus&#x65;**: The*SMTP connection error* occurs when CleverTap is unable to establish a connection with your ESP's SMTP server.Some of the other common causes could be:<ul> <li>Incorrect server details such as the server's hostname, port, or credentials. You can check the server details you have entered to confirm they are correct. </li> <li>Network issue that prevents the application from connecting to the SMTP server. It could be a temporary issue on your ESP's end.</li> </ul>**&#x52;esolution\*\*: Contact your provider's customer support for further assistance if the issue persists.
      </td>
    </tr>

    <tr>
      <td>
        *SMTP timeout*
      </td>

      <td>
        * \*Caus&#x65;**: The*SMTP timeout* error occurs when CleverTap cannot connect with your ESP's SMTP server, or the connection takes longer than expected. Some of the other common causes could be:<ul> <li>The email-sending process has taken longer than the allocated time frame for connection establishment or completion.</li> <li>The SMTP server of your ESP is experiencing high traffic. </li> <li>Your sending IP has been flagged as a source of spam.</li> <li>There is an issue with your ESP's infrastructure.</li> </ul>**&#x52;esolution\*\*: Contact your provider's customer support for further assistance if the issue persists.
      </td>
    </tr>
  </tbody>
</Table>

<HTMLBlock>{`
<style>
  .rm-Guides .content-body, .rm-Guides #content-head .col-xs-9 {
      max-width: 100%;
      width: 1000px;
  }
  .markdown-body summary {
  font-size: 20px;
  font-weight: bold;
  text-transform: camelcase;
}
</style>
`}</HTMLBlock>
