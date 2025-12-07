---
title: Gupshup (WIP)
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

CleverTap partners with Gupshup to help customers send and receive the following type of WhatsApp messages:

* Sending just-in-time offers to customers to drive purchases
* Gathering feedback on the services
* Keeping customers informed and more

# Prerequisites for Integration

@jash: Are there no prerequisites for this integration?

# Integrate CleverTap with Gupshup

@Jash: Pls speak to Deepak and list down all the steps for integration.

## Select Gupshup Provider

Perform the following steps to select Gupshup as the messaging provider for WhatsApp.

1. From the CleverTap dashboard, navigate to *Settings* and click on **Channels**.
2. Select *WhatsApp*.

<Image title="2020-06-25_09-04-14_Add provider.png" alt="Add Provider" align="center" className="border" width="% " border={true} src="https://files.readme.io/496ab50-2020-06-25_09-04-14_Add_provider.png" />

> 🚧 Note
>
> Only one WhatsApp Provider account is supported per CleverTap project.

3. Click **+Providers** then select *Gupshup* from the dropdown menu. Nexmo is the provider default.

<Image title="2020-06-25_09-12-35_Provider credentials.png" alt={429} align="center" className="border" width="80%" border={true} src="https://files.readme.io/14ce97c-2020-06-25_09-12-35_Provider_credentials.png" />

4. Enter the following credentials:

* Nickname: Enter the nickname for this set of credentials.
* Inbound message callback URL: This is a non-editable field.

Note that the Gupshup must use the following payload format to configure incoming message callbacks at their end.

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

* Delivery reports callback URL: This is a non-editable field.

Note that the Gupshup must use the following payload format to configure DLR callbacks at their end.

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

* Notification account user ID: Enter the notification account user ID.
* Notification account password: Enter the notification account password.
* Two-way account user ID: Enter the two-way account user ID.
* Two-way account password: Enter the two-way account password.
* App name:  Enter the App name from the Gupshup dashboard.
  * Mobile Number: Enter either a Gupshup phone number or a shortcode. You can enter phone numbers or shortcodes listed under the Gupshup dashboard > Numbers > Your Numbers.
  * Facebook URL: Enter the Facebook URL from the Gupshup dashboard.

> 📘 Non-Editable Fields
>
> The inbound message callback URL and delivery reports callback URL are non-editable fields. These values must be set up in your Gupshup account to allow CleverTap to receive inbound messages from end-users and delivery reports for messages sent through Gupshup.

<Image title="2020-06-25_09-12-35_Provider credentials1.png" alt={704} align="center" className="border" width="80%" border={true} src="https://files.readme.io/cf55c41-2020-06-25_09-12-35_Provider_credentials1.png" />

> 📘 Auto Reply Checkbox
>
> Select the checkbox if you want to set auto-replies for users who are not tracked in CleverTap. If a message is received from a phone number for which a profile is not present with CleverTap, then this default message is sent to the user.

5. Send a Test WhatsApp notification: 

![](https://files.readme.io/c384922-sendtest.png "sendtest.png")

   To ensure that the integration is successful:\
   a. Click the *Send Test WhatsApp* hyperlink before you start creating WhatsApp campaigns and journeys. To begin with, activate the conversation window by following any one of the following methods:\
      i. Save the business contact and send a WhatsApp message to that number.\
      ii. Copy and share the link with the user you want to send the test notification to. Further, ask the user to click on the link and send a WhatsApp message to initiate a conversation.\
      iii. If you want to send a test notification to yourself, you can click the link and initiate a WhatsApp conversation.

   b. Enter the following details:\
      ***Country Code and Mobile Number**: Enter the country code and mobile number of the user to whom you want to send the test message.\&#xA;* **Message**: Here, you can enter the sample text message you want to send to the test user. Once you click on *Send Test*, the success or failure response displays on the dashboard. If the message is not delivered, you can copy the response payload and share it with the Gupshup team to debug the issue.

6. Click **Save**.

<Image title="2020-06-26_16-05-32_Saving credentials.png" alt={729} align="center" className="border" width="80%" border={true} src="https://files.readme.io/4fbb7a9-2020-06-26_16-05-32_Saving_credentials.png" />

## Add Multiple WhatsApp Phone Numbers

> 📘 Adding Multiple Numbers
>
> Customers can add multiple phone numbers for WhatsApp, irrespective of their service provider. If the business has multiple numbers, the autoresponse, FAQ response, and agent replies will go from the number that received the last customer message.

To add a phone number to your WhatsApp profile, repeat steps *3* through *6*, listed under [Select Gupshup Provider](doc:gupshup#select-gupshup-provider), for each provider.

## Select Template

After selecting Gupshup as the provider, create a template for the campaign as follows:

1. Select the *Templates* option, and click **+Template**.

<Image title="2020-06-25_10-21-57_Select Templates.png" alt={934} align="center" className="border" border={true} src="https://files.readme.io/4e41af4-2020-06-25_10-21-57_Select_Templates.png" />

2. Enter the template name in the *Namespace* field.
3. Select the *Type* of the template header (Text or Media). For Media headers, you can use *Image*, *Video*, *Document*, and *Location*
4. Enter the message content under the *Body* field.
5. (Optional) Select the *Footer* text and *Button* (for Quick Reply or a Call To Action).

<Image title="gupshup new template.png" alt={2200} align="center" className="border" border={true} src="https://files.readme.io/e54d574-gupshup_new_template.png" />

6. Click **Save Template**.

## Testing a Message Template

You can send a test message using the saved templates from the CleverTap dashboard as follows:

1. Hover over the desired template for which you want to send a test notification.
2. Click *Send Test*.
3. Select the test profiles or manually enter the mobile number to whom you want to send the test message and click *Send Test*.  

<Image title="test template.png" alt={1304} align="center" className="border" border={true} src="https://files.readme.io/fbf00f7-test_template.png" />

The success or failure response is displayed on the dashboard. If the message is not delivered, you can copy the response payload and share it with the Gupshup team to debug the issue, as shown in the following figure:

<Image title="sendtest campaign.png" alt={728} align="center" className="border" width="80%" border={true} src="https://files.readme.io/363a140-sendtest_campaign.png" />

## Create Campaign

To create a WhatsApp campaign using Gupshup as the provider, refer to [Creating a WhatsApp Campaign](doc:whatsapp#section-creating-a-whatsapp-campaign).

## Troubleshooting

This section lists the errors occurring at the time of integration.\
Restricted IPs can cause errors during integration. Ensure that there are no IP restrictions enabled on the Gupshup account. To check the IPs from the CleverTap dashboard, go to *Settings* > *Channels* > *Mobile push*. The *FCM credentials* section lists the IPs used to send WhatsApp requests. These IPs must be whitelisted on both the *one-way\_and \_two-way* account IDs of Gupshup.

![](https://files.readme.io/e24891a-Gupshup_Whitelist_IPs.png "Gupshup_Whitelist_IPs.png")
