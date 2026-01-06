---
title: Zendesk
excerpt: Support Partner
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
# Overview

[Zendesk Support Suite](https://www.zendesk.com/support-suite/) (ZSS) allows businesses to have natural conversations with their customers through omnichannel support using email, webchat, voice, or social messaging applications. Zendesk offers a streamlined ticketing system that tracks and prioritizes interactions, allowing businesses to have a unified historical view of their customers.

This integration helps you to create a support ticket using a CleverTap webhook. For example, you send out a CleverTap [Rating In-app](https://docs.clevertap.com/docs/create-message-inapp#ratings-template) campaign, and the customer provides negative feedback. CleverTap can automatically create a support ticket on Zendesk for this feedback, allowing your support team to follow up with the customer.

# Prerequisites for Integration

The following are the prerequisites for this integration:

* You must have a Zendesk Admin account and an API token to send requests from CleverTap to Zendesk for creating tickets.
* You must have an account with CleverTap.

# Integrate CleverTap with Zendesk

This integration involves the following two major steps:

1. [Set Up a Webhook](doc:zendesk#set-up-webhook).
2. [Create a CleverTap Campaign to create support tickets](doc:zendesk#create-a-webhook-campaign).

## Set up Webhook

Set up a webhook to send HTTP API requests with all the information. To set up a webhook:

1. Navigate to _Settings_ > _Engage_ > _Channels_ > _Webhooks_ from the CleverTap dashboard.
2. Click **+ Add Webhook**.

<Image align="center" alt={2858} border={true} src="https://files.readme.io/1967920-Add_Webhook.png" title="Set up a Webhook from CleverTap dashboard" className="border" />

Set Up a Webhook from CleverTap Dashboard

3. Configure the webhook template by adding the following details:

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
        Name
      </td>

      <td>
        Enter the nickname for your webhook to uniquely identify the webhook.
      </td>
    </tr>

    <tr>
      <td>
        Destination URL
      </td>

      <td>
        Enter the following URL:  
        https://\{\{your_sub_domain}}.zendesk.com/api/v2/tickets.json.
      </td>
    </tr>

    <tr>
      <td>
        Method
      </td>

      <td>
        Select the _POST_ method from the dropdown.
      </td>
    </tr>

    <tr>
      <td>
        Basic Authorization
      </td>

      <td>
        Enable this option.
      </td>
    </tr>

    <tr>
      <td>
        Username
      </td>

      <td>
        Enter the username as follows:  
        _\<emailaddress>/token_
      </td>
    </tr>

    <tr>
      <td>
        Password
      </td>

      <td>
        Enter the password as `<API Token>`. To obtain the API token, refer to [Generating a new API token](https://support.zendesk.com/hc/en-us/articles/4408889192858).
      </td>
    </tr>
  </tbody>
</Table>

<Image align="center" alt={1006} border={true} width="80%" src="https://files.readme.io/fb5dbd8-Create_webhook_template.png" title="Enter all the required details and create a Webhook template" className="border" />

Create a Webhook Template

## Create a Webhook Campaign

To create a webhook campaign:

1. **Define the audience**.  
   The **Rating Submitted** event is raised when a user submits their feedback through [NPS Campaign](https://docs.clevertap.com/docs/user-ratings). The campaign targets users who give ratings of less than **3**.

<Image align="center" alt={3182} border={true} src="https://files.readme.io/31c11b3-Define_the_audience.png" title="Define Target Audience for Webhook campaign" className="border" />

Define Target Audience for Webhook Campaign

2. **Define the campaign content.**  
   a. Click **Go To Editor** to create your message.  
   b. Select _Custom JSON Body_ and use the following example to help structure your payload and enter the desired fields:
   <br />
   ```json

    "ticket":{
      		"requester_id": "@Profile - Identity | default:"1"",
      		"requester": {
       			 "name": "@Profile - Full Name | default: "CleverTap"",
       			 "email": "@Profile - Email | default: "integrations@clevertap.com"",
       			 "phone": "@Profile - Phone | default: "+919999999999""},
      			"type": "task",
      			"subject": "Rating Submitted - @Rating Submitted - User Rating | default:"3"",
      			"comment": {
        				"body": "@Rating Submitted - Comment | default:"Rating submitted""
      			},
      			"priority": "urgent",
      			"status": "new"
    		}
   }
   ```
   <br />

<Image align="center" alt={3178} border={true} caption="Custom Body for Webhook Campaign" title="Define custom body for Webhook campaign" src="https://files.readme.io/90c30d4-Define_campaign_content.png" width="80%" />

Ticket details are extensible and customized based on the [Zendesk ticket API](https://developer.zendesk.com/api-reference/ticketing/tickets/tickets/#create-ticket). To learn more about creating a webhook, refer to [Create a Webhook Campaign](doc:create-message-webhook).

# Common Identifier

If you have a common identifier between CleverTap and Zendesk, we recommend using this identifier as the `requester_id`. This helps unify the two sets of users. Alternatively, if this is not the case, we recommend passing a group of identifying attributes such as name, email address, phone number, or others.
