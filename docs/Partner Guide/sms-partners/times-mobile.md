---
title: Times Mobile
excerpt: SMS Provider
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
# Introduction

Times Mobile (part of Times Internet Limited) is a leading communication platform that empowers businesses to connect with their users through SMS channels. This document highlights the integration of CleverTap and Times Mobile, empowering businesses to elevate their SMS communication using Times Mobile's infrastructure.

CleverTap's integration with Times Mobile facilitates sending bulk SMS campaigns, receiving real-time delivery updates, and automating personalized texts for your sales and marketing engagement using Times Internet's auto-scalable infrastructure.

For any queries or further assistance, contact [support@timesmobile.in](mailto:support@timesmobile.in).

# Prerequisities for Integration

Before you begin with integration, ensure you have:

* A CleverTap account with SMS setup enabled.
* A Times Mobile SMS account with respective SMS Push API details.
* The DLT-approved information, including templates and headers, if your account region is in India.

# Times Mobile Setup

This process involves the following three significant steps:

1. [Configure Times Mobile dashboard](doc:times-internet#configure-times-internet-dashboard).
2. [Add Times Mobile details to CleverTap dashboard](doc:times-internet#configure-clevertap-dashboard).
3. [Send a test SMS](doc:times-internet#configure-clevertap-dashboard).

## Configure Times Mobile Dashboard

Configuring the Times Mobile dashboard involves the following steps: obtaining SMS Push API credentials and setting up the CleverTap DLR Callback webhook.

To configure the Times Mobile dashboard:

1. Log in to the Times Mobile Dashboard using your credentials.

   <Image align="center" border={true} src="https://files.readme.io/ce13378-Times_Internet_.png" className="border" />
2. Navigate to _Sender ID Management_ > _Request Sender_ and click **Request For Sender** to request a new sender ID.
3. Enter the following DLT-approved header details: **Sender Name**, **Account Type** (either trans or pro), and  **DLT Principal Entity Id**. **Sender Name** should be six characters or digits as per your account type.

<Image align="center" alt="Configure Sender IDs " border={true} width="100%" src="https://files.readme.io/8dae093-Times_Internet_Request_Sender.png" className="border" />

Configure Sender IDs

4. After adding the header details, click  **Create Sender Request** to create the sender request.
5. Navigate to _Bulk SMS_ > _HTTP_ from the Times Mobile dashboard to access your SMS Push API credentials. These credentials are required for configuration within the CleverTap platform. CleverTap recommends keeping these credentials handy before configuring them on the CleverTap dashboard.

<Image align="center" alt="Configure CleverTap DLR Callback Webhook" border={true} src="https://files.readme.io/3d80859-SMS_Push_Credentials-_Times_internet.png" className="border" />

Obtain SMS Push API Credentials

6. Click **Username** > **Profile** from the Times Mobile Dashboard.
7. Under the **Delivery Report Post Back URL** section, configure the CleverTap DLR Callback Webhook for real-time SMS delivery updates. For more information, refer to the callback URL column in the [Configure CleverTap Dashboard ](doc:times-internet#configure-clevertap-dashboard) section.

<Image align="center" alt="Obtain SMS Push API Credentials" border={true} src="https://files.readme.io/a12ee6f-Times_Internet-_Delivery_Report_Post_Back_URL.png" className="border" />

Configure CleverTap DLR Callback Webhook

If you encounter any issues while configuring, contact [support@timesmobile.in](mailto:support@timesmobile.in) for further assistance.

## Configure CleverTap Dashboard

To add Times Mobile details on the CleverTap dashboard:

1. From the CleverTap Dashboard, navigate to _Settings_ > _Engage_ > _Channels_ > _SMS_.
2. Click **+Add Provider**. The _Add SMS Provider_ page opens.

<Image align="center" alt="Add SMS Provider" border={true} width="90% " src="https://files.readme.io/090cf81-SMS_Add_Provider.png" className="border" />

Add SMS Provider

3. Select the _Setup_ tab and enter the following details:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        _Provider_
      </td>

      <td>
        Select _Other(Generic)_ from the dropdown list.
      </td>
    </tr>

    <tr>
      <td>
        * _Nickname_
      </td>

      <td>
        Uniquely identifies the provider.
      </td>
    </tr>

    <tr>
      <td>
        * _Callback URL_
      </td>

      <td>
        Enter the callback URL with Times Mobile to post or update the Message Delivery Status to CleverTap.
      </td>
    </tr>

    <tr>
      <td>
        _Request Type_
      </td>

      <td>
        Select _GET_ or _POST_ based on the HTTP endpoint.
      </td>
    </tr>

    <tr>
      <td>
        _HTTP Endpoint_
      </td>

      <td>
        Enter the Times Mobile SMS Push endpoint along with its respective credentials.
      </td>
    </tr>

    <tr>
      <td>
        _Authentication_
      </td>

      <td>
        Select from the following authentication types:

        <li> No Authentication_ : For GET_  endpoint, select this option.</li><li>*Basic Authentication* : For *POST* endpoint, select this option. Also, provide Times Mobile API *Username* and *Password* details.</li><li>*OAuth 2.0*: Enter client URL, client ID, secret key, and key-value pairs (optional).</li>
      </td>
    </tr>

    <tr>
      <td>
        _Parameters_
      </td>

      <td>
        Select _x-www-form-unlenencoded_ or _JSON_ for _Type_ column.  
        For the _POST_ endpoint, select _JSON_ and enter the JSON payload structure. This field appears when you select _POST_ in the _Request Type_ column.  
        POST endpoint: `https://bsms.timesapi.in/ct/api/v1/message`  
        For more information, refer to the following:

        <li> [Get endpoint](https://bsms.timesapi.in/ct/api/v1/send?username=%3Capiusername%3E&password=%3Capipassword%3E&unicode=false&from=%3Csenderid%3E&to=$$To&text=$$Body&dltContentId=$$TemplateID&corelationid=$$MessageID)</li>  
        <li> [Post endpoint](https://bsms.timesapi.in/ct/api/v1/message)</li>  
        <li> [Sample Payload](doc:times-internet#set-up-message-payload)</li>
      </td>
    </tr>

    <tr>
      <td>
        _Headers_
      </td>

      <td>
        For the _POST_ endpoint, enter the following key-value pairs:

        1. _Key_: Content-Type | _Value_: application/JSON
        2. _Key_: Accept | _Value_: application/JSON
      </td>
    </tr>

    <tr>
      <td>
        _Custom Key-value pairs in campaign_
      </td>

      <td>
        Select this option to pass custom key-value pairs when sending your campaigns.
      </td>
    </tr>

    <tr>
      <td>
        _Mark this as default_
      </td>

      <td>
        Select _Mark this as default_ to make this SMS provider the default provider to send the SMS.
      </td>
    </tr>
  </tbody>
</Table>

***The fields marked with asterisk mark (*) are mandatory fields.**

<Image align="center" alt="Add Times Internet as an SMS Provider" border={true} width="70%" src="https://files.readme.io/7946b37-Times_Internet_Provider.png" className="border" />

Add Times Mobile as an SMS Provider

4. Click **Save** to save the details.

## Send a Test SMS

To ensure that the integration is successful, send a test SMS as follows:

1. Click the _Send Test SMS_ option before creating SMS campaigns and journeys.

2. Enter the following details:

   * _Country Code_ and _Mobile Number_: Enter the country code and mobile number you want to send the message to.
   * _Message_: This is a test message.

   <Image align="center" alt="Send a Test SMS" border={true} width="75%" src="https://files.readme.io/8543b05-Send_a_Test_SMS_.png" className="border" />

   Send a Test SMS

3. Click **Send Test** to send the test campaign.

# Times Mobile Callbacks

In the default setup, Times Mobile sends the information to CleverTap's callback URL as follows:

1. CleverTap generates the callback that customers need to set up on the  Times Mobile dashboard.
2. TimesInternet sends the callback directly to CleverTap on the default URL.
3. CleverTap processes the callback.

Upon receiving callbacks from Times Mobile, the comprehensive stats are displayed on the CleverTap dashboard. For more information, refer to the [Stats](doc:times-internet#stats) section.

## Set Up Message Payload

This section provides information about the sample request payload sent to SMS providers.

```json
{

   "username": "<apiusername>",
   "password": "<apipassword>",
   "unicode": "false",
   "from": "<senderid>",
   "to": "$$To",
   "text": "$$Body",
   "dltContentId": "$$TemplateID",
   "corelationid": "$$MessageID"
}
```

# Stats

CleverTap displays comprehensive stats such as Errors, Delivered, Clicked, and CTRs upon receiving callbacks from Times Mobile. After setting up the provider on the CleverTap dashboard, you can view these statistics from the following pages on the CleverTap dashboard:

* For [SMS Stats](https://docs.clevertap.com/docs/sms-stats), select the _Stats_ tab of the Campaigns.
* For [Provider Stats](https://docs.clevertap.com/docs/sms-provider-operations), select the _Stats_ tab under _Provider_ setup.

# Troubleshooting

If you encounter issues when sending test messages or saving the configuration, check that the Times Mobile endpoint and parameters are correctly added. Endpoints are case-sensitive. If the issue persists, raise a support ticket with the CleverTap team to obtain error codes. Once you have the error codes, connect with the  [Times Mobile Support](mailto:support@timesmobile.in) team.

# Frequently Asked Questions (FAQs)

Explore the FAQs for comprehensive insights and answers to common queries.

### Where can I check DLT guidelines for sending service/promotional SMS?

A. You can check the DLT guidelines for sending service/promotional SMS [here](https://docs.timesmobile.in/cpaas/DLT.pdf).

### What are DLT-approved SMS templates, and what is the approval process?

A. You can find more details about DLT-approved SMS Templates [here](https://docs.timesmobile.in/cpaas/DLT.pdf).

### What is a DLT-approved Header/Sender ID, and how do you get it approved?

A. You can find more details about DLT-approved Header/Sender ID [here](https://docs.timesmobile.in/cpaas/DLT.pdf).
