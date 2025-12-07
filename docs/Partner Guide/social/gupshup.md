---
title: Gupshup
excerpt: Enable WhatsApp Messaging via Gupshup
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

CleverTap supports customers who send and receive WhatsApp messages using Gupshup as their provider. Once a provider is selected, the user must create a template before creating a WhatsApp campaign.

## Select Gupshup Provider

Follow these steps to choose Gupshup as your messaging provider for WhatsApp.

1. Navigate to _Settings_ and select **Channels** from the CleverTap dashboard.
2. Select _WhatsApp_ > _WhatsApp Connect_. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/55c4289-non_CT_Provider_add_template.jpg",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


> 🚧 Note
> 
> Only one WhatsApp Provider account is supported per CleverTap project.

3. Click **+Providers**, and select Gupshup from the Provider list. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b567a1a-gupshup_new_ss.png",
        "gupshup new ss.png",
        1094
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Provider Setup"
    }
  ]
}
[/block]


4. Enter the following credentials: 

- Nickname: Enter the nickname for this set of credentials.
- Inbound message callback URL: This is a non-editable field.

Note that Gupshup must use the following payload format to configure incoming message callbacks on their end.

```json
CleverTap_Sandbox Incoming Hits - Calling URL :: POST :: https://cb.wzrkt.com/gupshup/response?a=XXX-XXX-XXXX ==> {
  "waNumber": "91XXXXXXXXXX",
  "mobile": "91XXXXXXXXXX",
  "name": "John Doe",
  "text": "incoming text",
  "type": "text",
  "timestamp": "1658261071000"
}
```

- Delivery reports callback URL: This is a non-editable field.

Note that Gupshup must use the following payload format to configure DLR callbacks on their end.

```json Delivery report callback payload format
2022-02-25 01:22:30 ################ KEYVALUE Forwarding: https://cb.wzrkt.com/gupshup/status?a=XXX-XXX-XXXX => headers:  => body: [response:[{
  "srcAddr": "CLVTAP",
  "extra": "9|1658264893|20220720|9|wzrk_default",
  "channel": "WHATSAPP",
  "externalId": "4687162516402008133-497817541934555810",
  "cause": "READ",
  "errorCode": "026",
  "destAddr": "+91XXXXXXXXXX",
  "eventType": "READ",
  "eventTs": 1658264959000
}]]
```

- HSM account ID: Enter the HSM account user ID.
- HSM account password: Enter the HSM account password.
- Two-way account user ID: Enter the two-way account user ID.
- Two-way account password: Enter the two-way account password.
- Mobile Number: Enter either a Gupshup phone number or a shortcode. You can enter phone numbers or shortcodes under the Gupshup dashboard > Numbers > Your Numbers.

> 📘 Non-Editable Fields
> 
> The inbound message callback URL and delivery reports callback URL are non-editable fields. These values must be set up in your Gupshup account to allow CleverTap to receive inbound messages from end-users and delivery reports for messages sent through Gupshup.

> 📘 Auto Reply Checkbox
> 
> Select the checkbox if you want to set auto-replies for users who are not tracked in CleverTap. If a message is received from a phone number for which a profile is not present with CleverTap, then this default message is sent to the user.

5. Send a Test WhatsApp notification: 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c384922-sendtest.png",
        "sendtest.png",
        1488
      ],
      "align": "center",
      "caption": "Send Test Message on WhatsApp"
    }
  ]
}
[/block]


   To ensure that the integration is successful:  
   a. Click the _Send Test WhatsApp_ hyperlink before creating WhatsApp campaigns and journeys. To begin with, activate the conversation window by following any one of the following methods:  
      i. Save the business contact and send a WhatsApp message to that number.  
      ii. Copy and share the link with the user to whom you want to send the test notification. Further, ask the user to click the link and send a WhatsApp message to initiate a conversation.  
      iii. If you want to send a test notification to yourself, you can click the link and initiate a WhatsApp conversation.

   b. Enter the following details:  
      _ **Country Code and Mobile Number**: Enter the country code and mobile number of the user to whom you want to send the test message.  
      _ **Message**: Here, you can enter the sample text message you want to send to the test user. Once you click on _Send Test_, the success or failure response displays on the dashboard. If the message is not delivered, you can copy the response payload and share it with the Gupshup team to debug the issue.

6. Click **Save**. 

## Select Template

1. Refer to this guide on [how to create a WhatsApp template](https://docs.clevertap.com/docs/whatsapp-message-templates#create-whatsapp-template).
2. The following are the template types for Gupshup on CleverTap:

- [Basic Templates](https://docs.clevertap.com/docs/whatsapp-message-templates#basic-templates-1)
- [Limited-Time Offer Templates](https://docs.clevertap.com/docs/whatsapp-message-templates#limited-time-offer-templates-1)
- [Carousel Templates](https://docs.clevertap.com/docs/whatsapp-message-templates#carousel-templates)

## Testing a Message Template

Refer to this [document](https://docs.clevertap.com/docs/whatsapp-message-templates#testing-a-message-template) to understand how to test a template.

## Create Campaign

To create a WhatsApp campaign using Gupshup as the provider, refer to [Creating a WhatsApp Campaign](https://docs.clevertap.com/docs/whatsapp#section-creating-a-whatsapp-campaign) for detailed instructions.

## Troubleshooting

### IP Whitelisting

Restricted IPs can cause errors during integration. Check that no IP restrictions are enabled on the Gupshup account. To check the IPs from the CleverTap dashboard, go to _Settings > Channels > WhatsApp_. The _FCM credentials \_section lists the IPs used to send WhatsApp requests.  These IPs must be whitelisted on both the \_one-way \_and \_two-way_ account IDs of Gupshup.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/622dcd4-ips_whatsapp.png",
        "ips whatsapp.png",
        "Restricted IPs"
      ],
      "align": "center",
      "border": true,
      "caption": "Restricted IPs"
    }
  ]
}
[/block]