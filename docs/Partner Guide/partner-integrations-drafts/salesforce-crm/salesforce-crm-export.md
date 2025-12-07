---
title: Salesforce Export
excerpt: >-
  Learn how to sync CleverTap with Salesforce CRM to export user data via OAuth
  2.0 webhooks for real-time segmentation and campaign automation.
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

Integrate CleverTap with Salesforce CRM to export user profile data in real time using a secure webhook. This integration uses the OAuth 2.0 Username-Password flow for authentication and enables CleverTap to push user data directly into Salesforce via a custom Apex REST API. The setup supports seamless CRM data enrichment and workflow automation using CleverTap campaigns.

This document provides a step-by-step implementation, divided into two parts:

- **[Salesforce Dashboard Setup](doc:salesforce-crm-export#salesforce-dashboard-setup)**: Configure OAuth credentials, custom objects, and Apex classes required for data ingestion.
- **[CleverTap Dashboard Setup](doc:salesforce-crm-export#clevertap-dashboard-setup)**: Set up a webhook using OAuth 2.0 authentication and use it in a campaign to trigger profile exports.

# Use Cases

This integration is suitable for multiple real-time CRM enrichment use cases, including:

- **Log NPS Responses from CleverTap**: Send Net Promoter Score (NPS) feedback to Salesforce and associate it with the custom objects or user records.
- **Push Leads from Campaigns**: Export lead details captured through CleverTap campaigns into Salesforce to facilitate timely follow-up by your sales team.
- **Sync Event and Product Feedback**: Capture user responses to in-app surveys, webinars, product launches, or promotional events, and send this data into Salesforce for tracking or triggering workflows.
- **Enrich CRM with Behavioral Data**: Add product usage metrics, feature interaction logs, and event-level insights to Salesforce user profiles to effective segmentation and targeting.   

# Prerequisites

Before you begin, ensure the following technical and account-level configurations are in place. These prerequisites are essential for setting up authentication, receiving data in Salesforce, and ensuring secure API communication.

- A valid Salesforce account with API access.
- Permission to access _Object Manager_, _App Manager_, and _Apex Classes_ on Salesforce.
- Permission to [create a Connected App in Salesforce](https://help.salesforce.com/s/articleView?id=sf.connected_app_create.htm). 
- [Username-Password OAuth Flow](https://help.salesforce.com/s/articleView?id=sf.remoteaccess_oauth_username_password_flow.htm) enabled under _Setup > OAuth and OpenID Connect Settings_ on the Salesforce dashboard.
- A [security token](https://help.salesforce.com/s/articleView?id=sf.user_security_token.htm) for the Salesforce user if IP restrictions are enabled.
- Admin access to the CleverTap dashboard to configure Webhooks and create campaigns.

# Salesforce Dashboard Setup

To configure Salesforce to receive data from CleverTap, perform the following steps:

1. **[Create a Connected App](doc:salesforce-crm-export#create-connected-app)**  
   Generate the Client ID and Client Secret required for OAuth authentication.
2. **[Create a Custom Object](doc:salesforce-crm-export#configure-custom-object-and-apex-rest-class)**  
   Define a custom object (for example, CleverTap NPS) in Object Manager to store incoming user data.
3. **[Create an Apex REST Class](doc:salesforce-crm-export#add-custom-apex-rest-class)**  
   Develop a custom Apex class that defines a POST endpoint to handle webhook requests and insert data into the custom object.

## Create Connected App

To generate the authentication credentials, you must create a [Connected App](https://help.salesforce.com/s/articleView?id=sf.connected_app_create.htm) in Salesforce as follows:

1. Select the _Setup_ tab on the Salesforce dashboard.

2. Go to _Platform Tools_ > _Apps_ > _External Client Apps_. 

3. Toggle ON the _Allow access to External Client App consumer secrets via REST API_ and _Allow creation of connected apps_ options.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e9ea8f9db181888256880aff025dc70b30fa3d8afd91c1f7478ca4276bfffef7-Screenshot_2025-07-10_at_10.33.17_AM.png",
        "",
        "Connected App - Salesforce"
      ],
      "align": "center",
      "border": true,
      "caption": "Connected App - Salesforce"
    }
  ]
}
[/block]


3. Click **New Connected App** and fill in the form with the required fields:

   [block:image]{"images":[{"image":["https://files.readme.io/d7d8a73451c271a7add7c8bcb90027d43726da557080ebd363c5e1fbb7c73777-image.png",null,"Fill Form for New Connected App"],"align":"center","sizing":"75% ","border":true,"caption":"Fill Form for New Connected App"}]}[/block]

   <br />
4. Click **Save**. It may take 2–10 minutes for the changes to take effect. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/26be75838fbb07d4e04ee035773126587b583944f4a01bedafdc6a0bb6ede8a0-Screenshot_2025-07-08_at_5.15.20_PM.png",
        "",
        "New Connected App - Salesforce"
      ],
      "align": "center",
      "sizing": "70% ",
      "border": true,
      "caption": "New Connected App - Salesforce"
    }
  ]
}
[/block]


<br />

| Section                         | Field/Option                                                                          | Description                                                                   |
| ------------------------------- | ------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| **Basic Information**           | Connected App Name                                                                    | Enter a descriptive name for the app (e.g., `CleverTap Integration`).         |
|                                 | API Name                                                                              | Use the auto-generated value or specify a custom name if required.            |
|                                 | Contact Email                                                                         | Enter a valid email address for integration-related notifications.            |
| **API (Enable OAuth Settings)** | Enable OAuth Settings                                                                 | Check this box to configure OAuth 2.0 authentication for the app.             |
|                                 | Callback URL                                                                          | Use `https://login.salesforce.com/services/oauth2/success` as a placeholder.  |
|                                 | Selected OAuth Scopes                                                                 | Select **Full Access (full)** and click **Add** to authorize all permissions. |
|                                 | Enable Client Credentials Flow                                                        | Check this to allow OAuth token generation via client credentials.            |
|                                 | Enable Authorization Code and Credentials Flow                                        | Enable this to support additional OAuth flows if needed.                      |
|                                 | Enable Token Exchange Flow                                                            | Check this to support token exchange as part of the OAuth flow.               |
|                                 | Require Secret for Token Exchange Flow                                                | Enable to ensure client secret is required for token exchange.                |
|                                 | Require Secret for Web Server Flow                                                    | Enable to secure the Web Server OAuth flow with a client secret.              |
|                                 | Require Secret for Refresh Token Flow                                                 | Enforce the use of client secret when refreshing tokens.                      |
| **Other Options**               | All remaining settings, such as digital signatures, refresh token rotation, JWT, etc. | Leave these disabled unless specifically required by your Salesforce org.     |

<br />

3. Go to _App Manager_ > _[Your Connected App]_ > and select _Manage Consumer Details_ from the list of actions. 
   1. [block:image]{"images":[{"image":["https://files.readme.io/bad6c472d33e7f831d129bbff5e98c5ef4a530193f3216fd611452dd7e06b506-2025-07-03_14-34-48_1.gif","","App Manager - Salesforce"],"align":"center","border":true,"caption":"App Manager - Salesforce"}]}[/block]
4. Copy and save the following credentials securely. These values will be required later when configuring the webhook in CleverTap for OAuth 2.0 authentication.

   - **Client ID**: Identifies your Connected App.
   - **Client Secret**: Authenticates the app during token generation. 
     1. - [block:image]{"images":[{"image":["https://files.readme.io/f8d88b7075bf5407457a0ccf993c28d607b54cf31c52cb65835c6d1a0d2182df-Client_ID__Secret.png","","Client ID and Client Secret - Salesforce"],"align":"center","border":true,"caption":"Copy Client ID and Client Secret"}]}[/block]
5. Go back to the Manage Connected Apps page, select _Edit_ from the list of actions, and disable IP restrictions.

## Configure Custom Object and Apex REST Class

To enable CleverTap to push user-level data into Salesforce, you must configure the necessary structures and endpoints in your Salesforce environment. These steps will result in a custom Apex REST endpoint that acts as the destination URL for CleverTap’s webhook, allowing it to receive user data in real time.

This setup includes creating a [custom object](https://help.salesforce.com/s/articleView?id=sf.customobjects_defining.htm) to store incoming data and implementing a [custom Apex REST class](https://developer.salesforce.com/docs/atlas.en-us.apexcode.meta/apexcode/apex_rest.htm) to handle POST requests from CleverTap. Using custom Apex classes provides greater control over how incoming webhook data is parsed, validated, and written to Salesforce. This is especially helpful when data needs to be transformed or routed before storage.

### Create Custom Object

To store incoming data from CleverTap in Salesforce, create a custom object that defines the structure of the data you want to capture.

(@Krishna: screenshots are missing from this section. Please add.)

1. Go to _Setup_ > _Object Manager_.

2. Click _Create > Custom Object_.

3. Enter the following details:

   - **Label**: For example, `CleverTap NPS`
   - **Object Name**: For example, `CleverTap__NPS`
   - **Record Name**: Keep the default (`Name`)

4. (Optional) Enable _Launch New Custom Tab Wizard after saving this custom object_ and click **Save**.

5. Under _Fields & Relationships_, click **+ New Field** to add relevant data fields. For example:

   - Field Label: `userId`, Data Type: **Text**
   - Field Label: `npsScore`, Data Type: **Number**
   - Field Label: `timestamp`, Data Type: **Date/Time**

### Add Custom Apex REST Class

To receive and process data from CleverTap, create a custom Apex REST class that defines a `POST` endpoint for handling incoming webhook requests.

1. Go tup_Setup_ _Apex Classes_ and click **New**.  
   andPaste the following example code:

   ```java Apex
   @RestResource(urlMapping='/InsertNPSFeedback')
   global with sharing class InsertNPSFeedback {

       global class NPSRequest {
           public String userId;
           public Integer npsScore;
           public String timestamp;
       }

       @HttpPost
       global static String doPost() {
           try {
               NPSRequest input = (NPSRequest) JSON.deserialize(RestContext.request.requestBody.toString(), NPSRequest.class);

               String recordName = 'User: ' + input.userId + ', Score: ' + input.npsScore + ', Time: ' + input.timestamp;

               CleverTap__NPS__c record = new CleverTap__NPS__c(
                   Name = recordName
               );

               insert record;
               return 'Success';
           } catch (Exception e) {
               return 'Error: ' + e.getMessage();
           }
       }
   }
   ```

2. Click **Save** to compile and activate the Apex class. After the Apex class is saved, note the value defined in the `@RestResource(urlMapping='/...')` annotation. This value represents the URL mapping path used to construct the _Destination URL_ in your CleverTap webhook configuration.  
   In this example, the URL mapping is `/InsertNPSFeedback`. Combined with your Salesforce instance domain, the final destination URL will be:
   ```
   https://instanceURL/services/apexrest/InsertNPSFeedback
   ```
   Save this URL mapping path (`InsertNPSFeedback`) separately. It is required when setting up the webhook in CleverTap.

# Keep Credentials for OAuth 2.0 Setup Handy

Before you begin setting up the OAuth 2.0 webhook in CleverTap, ensure that you have the following values ready. These were generated during the Connected App configuration and Apex setup steps:

(@Krishna: We need not explain these again here - Just list down what all we need for CT setup. PLease optimize this section. @parth, if you want I will remove it, I think it collates all the information that you need before you start the integration, because we don't have a reference point earlier in the doc for username, password and access token URL.)  

- **Destination URL**: This is the Apex REST endpoint that receives the webhook payload. Temporarily use the placeholder format below during initial setup. Once the access token is generated, replace `instanceURL` with the actual instance value returned in the token response:

```
https://instanceURL/services/apexrest/InsertNPSFeedback
```

This ensures that CleverTap sends data to the correct Salesforce environment.

- **Client ID**: Generated from your Salesforce Connected App.

- **Client Secret**: Also generated from the same Connected App.

- **Access Token URL**: The Salesforce token endpoint used for OAuth authentication.

  ```
  https://login.salesforce.com/services/oauth2/token
  ```

- _Salesforce Username_: The integration user's login email.

- _Salesforce Password_: The integration user’s login password, **appended with a security token** if IP restrictions are enabled. You can retrieve or reset the [security token here](https://help.salesforce.com/s/articleView?id=sf.user_security_token.htm).

These credentials are required to programmatically generate the access token and authenticate outbound webhook requests from CleverTap.

# CleverTap Dashboard Setup

Once your Salesforce setup is complete, you must configure two components in the CleverTap dashboard to enable data transfer:

- **[Set Up OAuth 2.0 Webhook](doc:salesforce-crm-export#set-up-oauth-20-webhook-in-clevertap)**: Define the webhook endpoint and authentication to send data to Salesforce securely.
- **[Create Webhook Campaign](doc:salesforce-crm-export#create-webhook-campaign-in-clevertap)**: Format and trigger the outbound data from CleverTap using the configured webhook.

## Set Up OAuth 2.0 Webhook in CleverTap

To push user data from CleverTap to Salesforce, configure a webhook using OAuth 2.0 authentication with the Client Credentials grant type. The webhook will deliver profile-level data to your custom Apex REST endpoint in Salesforce.

### Define Webhook Properties

Begin by setting up the basic webhook configuration in CleverTap.

1. Go to _Settings_ > _Channels_ > _Webhook_ on the CleverTap dashboard.

2. Click **+ Add Webhook** to create a new webhook.

3. Enter a name for the webhook (for example, **Salesforce Export Webhook**).

4. Set the **HTTP Method** to `POST`.

5. In the _Destination URL_, temporarily enter the Salesforce token endpoint:

   ```
   https://instanceURL/services/apexrest/InsertNPSFeedback
   ```

   This placeholder URL will be updated later with the actual Apex REST endpoint using the format `https://<instance_url>/services/apexrest/<url_mapping>` once the access token is generated.

### Configure OAuth 2.0 Authentication

Set up the webhook authentication parameters using the OAuth 2.0 Client Credentials flow with Username-Password grant.

1. Under _Authentication Type_, select **OAuth 2.0** from the dropdown.
2. Under _Grant Type_, select **Client Credentials**.
3. In **Client ID**, enter the value copied from the Client ID field in the Create [Connected App](doc:salesforce-crm-export#create-webhook-campaign-in-clevertap:~:text=Copy%20and%20save%20the%20following%20credentials%20securely.%20These%20values%20will%20be%20required%20later%20when%20configuring%20the%20webhook%20in%20CleverTap%20for%20OAuth%202.0%20authentication.) in the Salesforce section.
4. In **Client Secret**, enter the value copied from the Client Secret field in the Create [Connected App](doc:salesforce-crm-export#create-webhook-campaign-in-clevertap:~:text=Copy%20and%20save%20the%20following%20credentials%20securely.%20These%20values%20will%20be%20required%20later%20when%20configuring%20the%20webhook%20in%20CleverTap%20for%20OAuth%202.0%20authentication.) in the Salesforce section.
5. In the _Access Token URL_, enter:

   ```
   https://login.salesforce.com/services/oauth2/token
   ```

   This endpoint is used to generate the access token during authentication.
6. Select **Send Bearer Authentication in Header**.  
   This setting ensures the access token is securely passed in the HTTP header when making the webhook request.
7. Under _Additional Parameters_, click **+ Key Value Pairs** and add the following values:

   | Key         | Value                                                      |
   | ----------- | ---------------------------------------------------------- |
   | grant\_type | `password`                                                 |
   | username    | Your Salesforce integration user’s login email             |
   | password    | Your password, appended with the Salesforce security token |

   These parameters are required to complete the Username-Password OAuth flow. They authenticate the token generation request with Salesforce.
8. Click **Generate Token**. CleverTap will connect with Salesforce and request a new access token using the above values. 

   [block:image]{"images":[{"image":["https://files.readme.io/6b1c45c916e7fd46c81d24380ff6fbcb73ff696c7e8db779a3c97ba70792634b-Screenshot_2025-07-08_at_5.06.06_PM.png","","Create Webhook - CleverTap"],"align":"center","sizing":"50% ","border":true,"caption":"Set Up OAuth 2.0 Webhook in CleverTap"}]}[/block]

### Configure Token Mapping and Destination URL

After successful token generation, complete the webhook setup with the correct destination URL.

1. Once the token is generated successfully, map the returned **Access Token** and **Expiry** fields in the UI to finalize the configuration. These mappings are used to inject the token into future webhook calls automatically. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d65fb49a1866b6ff6f396182079e7bd3e9bdaae3593abebb912bc59ed69f65ca-Screenshot_2025-07-08_at_5.07.57_PM.png",
        "",
        "Access Token Expiry - CleverTap"
      ],
      "align": "center",
      "sizing": "45% ",
      "border": true,
      "caption": "Access Token Expiry - CleverTap"
    }
  ]
}
[/block]


2. Update the webhook URL before saving. After receiving the access token, update the destination URL in the following format:

```
https://<instance_url>/services/apexrest/<url_mapping>
```

- The `<instance_url>` refers to the Salesforce domain returned in the access token response.
- The `<url_mapping_path>` is defined in the Apex class using the `@RestResource(urlMapping='/...')` annotation.  
  For example, in our NPS use case, the URL mapping path is `CleverTap__NPS`, so the final destination URL would be:

```
https://<instance_url>/services/apexrest/CleverTap__NPS
```

This format ensures that CleverTap sends the webhook payload to the intended custom Apex REST endpoint in Salesforce.

3. Click **Save**.

## Create Webhook Campaign in CleverTap

Configure a Webhook campaign in CleverTap to send user-specific data to Salesforce.

1. Go to _Campaigns_ from the CleverTap and click **+ Campaign**.
2. Select **Webhook** from the list of messaging channels..
3. Select the **What** section and under **Webhook Content**, set the format to **JSON**.
4. Select **Custom Body** and define the request payload based on the structure defined in your Salesforce Apex REST API.

Use the `{{}}` and `@` buttons, or manually enter `{`, to insert dynamic profile fields and event attributes into the payload.

Example:

```
{
  "user_id": "{{Profile.identity}}",
  "email": "{{Profile.email}}",
  "nps_score": "{{Event.NPS Score}}"
}
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5dd62382c5e5178a464af76cb0e39f63a140ef161add2aacab1fa5756d0586c3-Screenshot_2025-06-19_at_4.03.41_PM-20250619-103347.png",
        "",
        "Create Webhook Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Create Webhook Campaign"
    }
  ]
}
[/block]


7. Click **Preview** to test the payload against sample user data.
8. Verify that the data appears correctly in your Salesforce system. If your Salesforce org syncs with Snowflake, check that the records appear there as well.
9. Once validated, click **Publish**. 

   [block:image]{"images":[{"image":["https://files.readme.io/02ce2104d7a0e7368301aeca960c931d20c16df85904babb618bae1fcbdea1bf-Screenshot_2025-06-19_at_4.07.03_PM.png","","Published Webhook Campaign"],"align":"center","border":true,"caption":"Published Webhook Campaign"}]}[/block]

This completes the Salesforce webhook integration. All qualifying users will now be pushed to your Salesforce instance via the configured Apex endpoint.