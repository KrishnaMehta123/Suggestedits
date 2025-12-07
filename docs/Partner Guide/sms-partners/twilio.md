---
title: Twilio
excerpt: SMS Provider
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Introduction

Twilio is a leading communication platform that empowers businesses to connect with their users through various channels, including SMS. This document highlights the integration of CleverTap and Twilio, empowering businesses to elevate their SMS communication using Twilio's infrastructure. 

# Prerequisites for Integration

Before you begin with integration, ensure you have:

- A Twilio account with SMS permissions
- A CleverTap account with SMS setup enabled

# Twilio Setup

This process involves the following three significant steps:

1. [Find Twilio Details](doc:twilio#find-twilio-details)
2. [Add Twilio Details on CleverTap Dashboard](doc:twilio#add-twilio-details-on-clevertap-dashboard)
3. [Send a Test SMS](doc:twilio#send-a-test-sms)

## Find Twilio Details

CleverTap recommends keeping the Twilio account handy before configuring it on the CleverTap dashboard. To locate these details, navigate to the _Console_ page from the Twilio dashboard:

- Account SID
- Auth Token
- My Twilio phone number

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b4ef390-Twilio_Account_Details.png",
        "",
        "Twilio Account Details"
      ],
      "align": "center",
      "border": true,
      "caption": "Twilio Account Details"
    }
  ]
}
[/block]


## Add Twilio Details on CleverTap Dashboard

To add Twilio details on the CleverTap dashboard:

1. From the CleverTap Dashboard, navigate to  _Settings_ > _Channels_ > _SMS_.
2. Click **+Add Provider**. The _Add SMS provider_ page opens.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dd87beb-SMS_Add_Provider.png",
        "",
        "Add SMS Provider"
      ],
      "align": "center",
      "border": true,
      "caption": "Add SMS Provider"
    }
  ]
}
[/block]


3. Under _Setup_, enter the following details:

[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "0-0": "_Nickname_",
    "0-1": "Uniquely identifies the provider.",
    "1-0": "_Account SID_",
    "1-1": "Enter your account identifier from the Twilio dashboard. This is a unique key to distinguish a specific Twilio parent account or subaccount.  For more information, refer to [Twilio Account SID](https://support.twilio.com/hc/en-us/articles/14726256820123-What-is-a-Twilio-Account-SID-and-where-can-I-find-it-).",
    "2-0": "_Auth token_",
    "2-1": "Enter the Auth Token (Password) obtained from the Twilio dashboard. For more information, refer to [Auth Token](https://support.twilio.com/hc/en-us/articles/223136027-Auth-Tokens-and-How-to-Change-Them).",
    "3-0": "_Callback URL_",
    "3-1": "Enter the URL where delivery or error callbacks must be posted after sending the SMS. By default, CleverTap's callback URL will be pre-populated. If you wish to send the callbacks to a custom URL instead, you can also set it here. For more information on setting a custom callback URL, refer to [Custom callback URL](doc:twilio#custom-callback-url).  \n  \n**Note**: This feature is currently in Public Beta.",
    "4-0": "_Restore_",
    "4-1": "Click _Restore_ to reinstate CleverTap's callback URL. This will remove any custom callback URLs.",
    "5-0": "_From Number_",
    "5-1": "Enter phone numbers obtained under the Twilio console → _Manage-numbers_ → _Active number_ section.",
    "6-0": "_Service SID (Copilot)_",
    "6-1": "Enter Service SID details obtained from the Twilio dashboard. The Copilot Service SID, a Twilio identifier, streamlines message management. It automates number selection and formatting, enhancing engagement by optimizing message delivery based on location and carrier requirements.",
    "7-0": "_Template ID_",
    "7-1": "It is a unique template ID for each SMS template that you want to use. Selecting this option will make it mandatory to input the template ID when saving the provider.",
    "8-0": "_Mark as default_",
    "8-1": "Select _Mark this as default_ to make this SMS provider the default provider to send the SMS."
  },
  "cols": 2,
  "rows": 9,
  "align": [
    "left",
    "left"
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b919c54-Twilio_Account_Details_on_CT_Dashboard.png",
        "",
        "Add Twilio as a SMS Provider"
      ],
      "align": "center",
      "border": true,
      "caption": "Add Twilio as an SMS Provider"
    }
  ]
}
[/block]


4. Click **Save** to save the details.

## Send a Test SMS

To ensure that the integration is successful, send a test SMS as follows:

1. Click the _Send Test SMS_ hyperlink before creating SMS campaigns and journeys.
2. Enter the following details:
   - _Country Code _ and _ Mobile Number_: Enter the country code and mobile number to which you want to send the message.
   - _Message_: This is a test message.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/02ee2f3-Send_a_Test_SMS_.png",
        "",
        "Send a Test SMS"
      ],
      "align": "center",
      "sizing": "70% ",
      "border": true,
      "caption": "Send a Test SMS"
    }
  ]
}
[/block]


> 🚧 Twilio Trial Account
> 
> With a Twilio trial account, you can only send SMS campaigns only to numbers registered on the Twilio dashboard.

> 📘 Encoding
> 
> The messages sent out from CleverTap are encoded in the UTF-8 charset.

# Twilio Callbacks

> 📘 Public Beta
> 
> Currently, this feature is in Public Beta.

The Twilio callback functionality enhances the tracking of SMS interactions originating from the CleverTap dashboard. Twilio's webhooks allow your Twilio phone number to receive incoming text messages. Within CleverTap's setup, the Callback URL is seamlessly generated and prefilled in the provider configuration under _Settings_ > _Channels_ > _SMS_ > _+Provider_. Users can replace this URL with their own, which must be configured on our end to receive callbacks. 

The callback mechanism between Twilio and CleverTap is designed to facilitate communication regarding SMS status updates. The Clevertap callback URL tracks for Delivered (SMS delivered to the user), Failed (SMS delivery error), and Replied (user response to SMS) events from Twilio.

## Default Callback URL

In the default setup, Twilio directly sends the information to CleverTap's callback URL. The flow involves the following steps:

1. Twilio generates the callback.
2. Twilio sends the callback directly to CleverTap on the default URL.
3. CleverTap processes the callback.
4. Upon receiving callbacks from Twilio, the comprehensive stats are displayed on the CleverTap dashboard. For more information, refer to [Stats](doc:twilio#stats).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d4b24c8-Default_callback_URL_flowchart.png",
        "",
        "SMS Default Callback Working"
      ],
      "align": "center",
      "border": true,
      "caption": "Twilio SMS Callback Working for Default URL"
    }
  ]
}
[/block]


## Custom Callback URL

Twilio sends the callback to a custom URL, which may belong to your customer. The customer is then responsible for replaying the callback to CleverTap. The flow is as follows: 

1. Twilio generates the callback.
2. Twilio sends the callback directly to the customer's custom URL.
3. The customer's custom URL relays the callback to CleverTap.
4. CleverTap processes the callback.
5. Upon receiving callbacks from Twilio, the comprehensive stats are displayed on the CleverTap dashboard. For more information, refer to [Stats](https://staging.docs.user.clevertap.net/docs/twilio#stats).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/07ae324-Custom_Callback_URLflowchart.png",
        "",
        "SMS Custom Callback Working"
      ],
      "align": "center",
      "border": true,
      "caption": "Twilio SMS Callback Working for Custom URL"
    }
  ]
}
[/block]


> 📘 Callback Data Passing
> 
> When the  callback is sent through a custom URL, CleverTap's callback endpoint requires all fields from the request payload received from Twilio to be relayed back exactly as received.

## Set Up Message Payload

In the Twilio callback integration with CleverTap, you can access dynamic parameters provided by Twilio in callback updates. This applies specifically when using a custom callback URL. Twilio provides meta details that should be forwarded to CleverTap as part of the integration.

- Key Name: meta 
- Description: Denotes information that CleverTap uses for attributing delivery, failure, etc., to specific campaigns, profiles, and SMS providers is included in the callback update by CleverTap. CleverTap passes this parameter in the ongoing SMS to Twilio, and Twilio, in turn, passes the same parameter back to the callback URL. 
- Sample Value: 919101699729.1200000000.1691686363.20230810.0.wzrk_default.-493000

## Sample Request Payload

This section provides information about the sample request payload sent to SMS providers. 

### Delivered

 The following is a sample request payload for **Delivered** from Twilio.

```Text cURL
curl --location 'https://sk1.cb.wzrkt.com/sms/twilio?account=YOUR_ACCOUNT_ID&meta=9999999999.1200000000.1691686363.20230810.0.wzrk_default.-4930006' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'RawDlrDoneDate=2308102223' \
--data-urlencode 'SmsSid=SMXXXXXXXXXXXXX' \
--data-urlencode 'SmsStatus=delivered' \
--data-urlencode 'MessageStatus=delivered' \
--data-urlencode 'To=00000000000' \
--data-urlencode 'MessagingServiceSid=MGXXXXXXXXXXXX' \
--data-urlencode 'MessageSid=SMXXXXXXXXXXXX' \
--data-urlencode 'AccountSid=AC0000000000' \
--data-urlencode 'From=0000000000' \
--data-urlencode 'ApiVersion=2010-04-0'
```

## Replied

The following is a sample request payload for **Replied** from Twilio.

```curl
curl --location 'https://sk1-staging-9.wzrkt.com/sms/twilio/response?account=YOUR_ACCOUNT_ID&providerId=YOUR_PROVIDER_ID' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'Body=Hello CleverTap' \
--data-urlencode 'To=XXXXXXXXXX' \
--data-urlencode 'From=XXXXXXXX'
```

The following table provides information about the key-value pair present in the above sample request:

| Key Name            | Description                                                                                                                                                                                                                                                                                                                                                                                    | Sample Value                       |
| :------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :--------------------------------- |
| RawDlrDoneDate      | <li> Available on SMS Delivered or Undelivered events only.</li> <li> This parameter is a passthrough of the Done Date included on the DLR (Delivery Receipt) that Twilio receives from its carrier partners. </li> <li> It takes the format of YYMMDDhhmm where: YY = last two digits of the year (00-99), MM = month (01-12), DD = day (01-31), hh = hour (00-23), mm = minute (00-59) </li> | 2302172359                         |
| SmsSid              | <li> Same value as MessageSid. </li> <li> Deprecated and included for backward compatibility. </li>                                                                                                                                                                                                                                                                                            | SMXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX |
| MessageStatus       | <li> Indicates the status of the message. </li> <li> The following are the possible values: be sent, failed, delivered, undelivered, and received. </li>                                                                                                                                                                                                                                       | delivered                          |
| SmsStatus           | <li> Same as the `MessageStatus` value. </li> <li> Deprecated and included for backward compatibility. </li>                                                                                                                                                                                                                                                                                   | delivered                          |
| AccountSid          | The 34-character ID of the Account the message is associated with.                                                                                                                                                                                                                                                                                                                             | ACXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX |
| MessagingServiceSid | The 34-character ID of the Messaging Service associated with the message.                                                                                                                                                                                                                                                                                                                      | MGXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX |
| From                | The phone number or channel address that sent this message.                                                                                                                                                                                                                                                                                                                                    | \+14017122661                      |
| To                  | The phone number or channel address of the recipient.                                                                                                                                                                                                                                                                                                                                          | \+15558675310                      |
| NumMedia            | The number of media items associated with your message                                                                                                                                                                                                                                                                                                                                         | 0                                  |
| FromCity            | The city of the sender.                                                                                                                                                                                                                                                                                                                                                                        | SAN FRANCISCO                      |
| FromState           | The state or province of the sender.                                                                                                                                                                                                                                                                                                                                                           | CA                                 |
| FromZip             | The postal code of the called sender.                                                                                                                                                                                                                                                                                                                                                          | 94103                              |
| FromCountry         | The country of the named sender.                                                                                                                                                                                                                                                                                                                                                               | US                                 |
| ToCity              | The city of the recipient.                                                                                                                                                                                                                                                                                                                                                                     | SAUSALITO                          |
| ToState             | The state or province of the recipient.                                                                                                                                                                                                                                                                                                                                                        | CA                                 |
| ToZip               | The postal code of the recipient.                                                                                                                                                                                                                                                                                                                                                              | 94965                              |
| ToCountry           | The country of the recipient.                                                                                                                                                                                                                                                                                                                                                                  | US                                 |

For more information, refer to Twilio's request [parameter](https://www.twilio.com/docs/messaging/guides/webhook-request#parameters-in-twilios-request-to-your-application). 

## Incoming Payload Mapping to System Events

CleverTap maps the following incoming payloads with their respective system events. You can view these on the CleverTap dashboard.

[block:parameters]
{
  "data": {
    "h-0": "Event",
    "h-1": "Sample Payload Structure",
    "h-2": "Mapping to CleverTap System Events",
    "0-0": "Notification Delivered",
    "0-1": "curl --location '<https://sk1.cb.wzrkt.com/sms/twilio?account=YOUR_ACCOUNT_ID&meta=9999999999.1200000000.1691686363.20230810.0.wzrk_default.-4930006'>   --header 'Content-Type: application/x-www-form-urlencoded'   --data-urlencode 'RawDlrDoneDate=2308102223'   --data-urlencode 'SmsSid=SMXXXXXXXXXXXXX'   --data-urlencode 'SmsStatus=delivered'   --data-urlencode 'MessageStatus=delivered'   --data-urlencode 'To=00000000000'   --data-urlencode 'MessagingServiceSid=MGXXXXXXXXXXXX'   --data-urlencode 'MessageSid=SMXXXXXXXXXXXX'   --data-urlencode 'AccountSid=AC0000000000'   --data-urlencode 'From=0000000000'   --data-urlencode 'ApiVersion=2010-04-0'",
    "0-2": "Maps to Notification Delivered event. For more information, refer to [Events](doc:events#system-events).",
    "1-0": "Notification Replied",
    "1-1": "curl --location '<https://sk1.cb.wzrkt.com/sms/twilio?account=YOUR_ACCOUNT_ID&meta=000000000.1200000000.1691686363.20230810.0.wzrk_default.-4930006'>  \n--header 'Content-Type: application/x-www-form-urlencoded'  \n--data-urlencode 'ToCountry=US'  \n--dat\ta-urlencode 'ToState=MA'  \n--data-urlencode 'SmsSid=SMXXXXXXXXXXXXX'  \n--data-urlencode 'FromState=CA'  \n--data-urlencode 'FromCity=SAN+FRANCISCO'  \n--data-urlencode 'FromCountry=US'  \n--data-urlencode 'SmsStatus=received'  \n--data-urlencode 'Body=Test+Reply+Message+2'  \n--data-urlencode 'To=00000000000'  \n--data-urlencode 'MessagingServiceSid=MGXXXXXXXXXXXX'  \n--data-urlencode 'MessageSid=SMXXXXXXXXXXXX'  \n--data-urlencode 'AccountSid=AC000000000000'  \n--data-urlencode 'From=00000000000'  \n--data-urlencode 'ApiVersion=2010-04-0'",
    "1-2": "Value of `Body` in the payload is populated in the Notification Replied event. For more information, refer to [Events](doc:events#system-events)."
  },
  "cols": 3,
  "rows": 2,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


## Error Codes

If there is an error in the SMS delivery, these error codes indicate the nature of an error encountered. Each error code corresponds to a specific error description. The error descriptions are displayed within the _Errors_ tab in the campaign stats section in case of delivery-related failures. The following table provides information about the acceptable error codes:

| Error Codes | Error Description                   | Details                                                                                                                                                                                                                                               |
| :---------- | :---------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 30001       | Queue overflow                      | Indicates that the rate limit was exceeded for sending messages, causing the queue to overflow. To resolve this issue, please wait a while before sending your message again.                                                                         |
| 30002       | Account suspended                   | Indicates that the account was temporarily suspended between sending the message and its delivery. Kindly get in touch with Twilio for further assistance.                                                                                            |
| 30003       | Unreachable destination handset     | Indicates that the recipient's mobile device is either turned off or presently not reachable.                                                                                                                                                         |
| 30004       | Message blocked                     | Indicates that the recipient's number you are attempting to contact is blocked from receiving this message, possibly due to being blacklisted.                                                                                                        |
| 30005       | Unknown destination handset         | Indicates that the attempt to reach the specified number encounters an unfamiliar recipient, which may suggest an invalid or non-existent contact.                                                                                                    |
| 30006       | Landline or unreachable carrier     | Indicates that the destination number is unable to receive this message. This can arise when contacting a landline or encountering an unreachable carrier, particularly with shortcodes.                                                              |
| 30007       | Carrier violation                   | Indicates that the carrier has detected the message content as objectionable, prompting the activation of content or spam filtering to safeguard their subscribers. For a deeper understanding of carrier filtering, consult supplementary resources. |
| 30008       | Unknown error                       | This error does not conform to any predefined categories mentioned above.                                                                                                                                                                             |
| 30009       | Missing segment                     | Indicates that one or more segments associated with your multipart inbound message were not received.                                                                                                                                                 |
| 30010       | Message price exceeds the max price | Indicates that the cost of the message surpasses the maximum price parameter set.                                                                                                                                                                     |
| 21614       | Invalid Mobile Number               | Indicates that the user's number is not valid.                                                                                                                                                                                                        |
| 21610       | Unsubscribed recipient              | Indicates that the individual you are attempting to message has chosen not to receive messages from your Twilio phone number, Channels sender, or Messaging Service.                                                                                  |

### Sample Payload

The following is a sample error payload:

```
curl --location 'https://sk1.cb.wzrkt.com/sms/twilio?account=YOUR_ACCOUNT_ID&meta=000000000.1200000000.1691686363.20230810.0.wzrk_default.-4930006' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'ErrorCode=30005' \
--data-urlencode 'SmsSid=SMXXXXXXXXXXXXXXXXXXXXXXX' \
--data-urlencode 'SmsStatus=failed' \
--data-urlencode 'MessageStatus=failed' \
--data-urlencode 'To=000000000000' \
--data-urlencode 'MessagingServiceSid=MGXXXXXXXXXXXX' \
--data-urlencode 'MessageSid=SMXXXXXXXXXXXXXXX' \
--data-urlencode 'AccountSid=AAAAAAA000000' \
--data-urlencode 'From=0000000000' \
--data-urlencode 'ApiVersion=2010-04-0'
```

# Stats

CleverTap displays comprehensive stats such as Errors, Delivered, Clicked, and CTRs upon receiving callbacks from Twilio. After setting up the provider on the CleverTap dashboard, you can view these statistics from the following pages on the CleverTap dashboard:

- _Stats_ tab of the Campaigns. For more information, refer to [SMS Stats](doc:sms-stats).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/907e612-Twilio_Campaign_Stats.png",
        "",
        "Twilio Campaign Stats"
      ],
      "align": "center",
      "border": true,
      "caption": "Twilio Campaign Stats"
    }
  ]
}
[/block]


> 📘 Note
> 
> The stats for _Clicked_ event is available only if you use CleverTap's [Click Tracking](<>) feature.

- _Stats_ tab under _Provider_ setup. For more information, refer to the [Provider Stats](https://docs.clevertap.com/docs/sms-provider-operations#view-provider-stats).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/37199a0-SMS_Provider_Stats.png",
        "",
        "Twilio Campaign Stats"
      ],
      "align": "center",
      "border": true,
      "caption": "Twilio Provider Stats"
    }
  ]
}
[/block]


You can also analyze the _Notification Delivered_ and _Notification Replied_ events by navigating to the _Analytics_ > _Events_ page, as shown in the following image:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/eb5134e-image.png",
        null,
        "Analyze Notification Delivered"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Analyze Notification Delivered"
    }
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/50e5a6f-2023-09-13_17-36-47_1.gif",
        null,
        "Analyze Incoming Text"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Analyze Notification Replied"
    }
  ]
}
[/block]