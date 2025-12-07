---
title: Talon.One
excerpt: Loyalty Partner
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
# Introduction

[Talon.One](https://www.talon.one/) is a platform that allows you to create highly customizable promotional campaigns with the help of the *Campaign Manager* feature. With this integration, you can automate coupon generation and delivery to specific customer segments. You can embed Talon.One generated coupon codes directly into messages delivered through CleverTap. Thereby, optimizing the reach by sending campaigns at the right time on the right channels. 
For any issues with this integration, contact [Talon.One Support team](mailto:support@talon.one).

# Prerequisites for Integration
The following are the prerequisites for setting up the integration:
* Must have integrated Talon.One SDK or API. For more information about detailed steps, refer to [Talon.One Integration](https://docs.talon.one/docs/dev/tutorials/integrating-talon-one).
* Must have access to CleverTap account.

# Send Talon.One Coupon Code Through CleverTap
To send the Talon.One coupon code through CleverTap:

## I. Set Up Webhook in Talon.One

To set up a [webhook](https://docs.talon.one/docs/dev/getting-started/webhooks#using-parameters-in-a-webhook) in Talon.One:
   1. Ensure that you set up the payload as per the parameter and authentication headers recommended by Clevertap. For more information, refer to [Upload Events API](https://developer.clevertap.com/docs/upload-events-api#section-http-method).
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2279edc-Create_a_Webhook.png",
        "Create a Webhook.png",
        3006,
        1630,
        "#fcfcfc"
      ],
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "body": "Ensure that you select *Display in Rule Builder* checkbox to enable webhook for your campaign.",
  "title": "*Display in Rule Builder* Checkbox"
}
[/block]
 
   2. Select the request *Verb* from the dropdown list and then enter the *URL*. The following table lists down the API endpoint for the region of your account:
[block:parameters]
{
  "data": {
    "h-0": "Region",
    "h-1": "CleverTap Dashboard URL",
    "h-2": "API Endpoint",
    "0-0": "EU",
    "1-0": "IN",
    "2-0": "US",
    "3-0": "Singapore",
    "0-1": "[https://eu1.dashboard.clevertap.com/login.html#/](https://eu1.dashboard.clevertap.com/login.html#/)",
    "1-1": "[https://in1.dashboard.clevertap.com/login.html#/](https://in1.dashboard.clevertap.com/login.html#/)",
    "2-1": "[https://us1.dashboard.clevertap.com/login.html#](https://us1.dashboard.clevertap.com/login.html#/)",
    "3-1": "[https://sg1.dashboard.clevertap.com/login.html#/](https://sg1.dashboard.clevertap.com/login.html#/)",
    "0-2": "[api.clevertap.com](api.clevertap.com)",
    "1-2": "[in1.api.clevertap.com](in1.api.clevertap.com)",
    "2-2": "[us1.api.clevertap.com](us1.api.clevertap.com)",
    "3-2": "[sg1.api.clevertap.com](sg1.api.clevertap.com)"
  },
  "cols": 3,
  "rows": 4
}
[/block]
   3. Enter the following CleverTap account details to set up the authentication headers:
  * Project ID
  * Passcode

  These details are obtained by navigating to the *Settings* page of the CleverTap dashboard.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/040af03-CT_Project_Details.png",
        "CT Project Details.png",
        1660,
        866,
        "#dddee6"
      ],
      "border": true
    }
  ]
}
[/block]
  4. Set up the parameters in the webhook payload for sending coupon codes 
 and update them to match your campaign requirements.
[block:code]
{
  "codes": [
    {
      "code": "{\n  \"d\": [\n     {\n         \"type\": \"event\",\n         \"evtName\": \"Coupon Generated\",\n         \"$source\": \"Talon.One\",\n         \"identity\": \"${Profile ID}\",\n         \"evtData\": {\n             \"CouponGenerated\":\"${$CouponCode}\"\n         }\n     }\n     ]\n     \n }",
      "language": "json",
      "name": "Webhook Payload for Sending Coupon Codes"
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "Payload Parameters",
  "body": "* The `evtName` parameter defines the EventName displayed on the CleverTap dashboard when selecting the campaign action. You can define the `evtName` as per your preference.\n* The `identity` is a mandatory parameter. This parameter is passed as the `userID`/`ProfileID`, which CleverTap uses to trigger the required engagement action effectively."
}
[/block]
## II. Set Up a Campaign in Talon.One
To set up a campaign in Talon.One:
1. [Create a campaign](https://docs.talon.one/docs/product/campaigns/creating-campaigns#creating-a-campaign-from-scratch).
2. Ensure that you add the **Create a Coupon Code** [effect](https://docs.talon.one/docs/product/rules/effects/available-effects/#create-effects).
3. Select the *Store generated value in session* checkbox to send the effect-generated coupon code to CleverTap.
[block:callout]
{
  "type": "info",
  "body": "When applying effects to the campaign, ensure that you [*Create the Coupon Code*](https://docs.talon.one/docs/product/campaigns/coupons/creating-coupons) and then *Create a Webhook Trigger*.",
  "title": "Applying Effects to Campaigns"
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/881db3d-Apply_Effects_to_Campaigns.png",
        "Apply Effects to Campaigns.png",
        2474,
        886,
        "#e8ecf8"
      ],
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "body": "Use a universal ID as the `profile ID` to identify the user across Talon.One and Clevertap dashboards.",
  "title": "Identify User"
}
[/block]

## III. Create a Campaign in CleverTap
You can use Email, SMS, and Push channels on the CleverTap dashboard to send coupon codes generated on Talon.One dashboard.

### Create an Email Campaign
1. Navigate to *Messages* > *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select the messaging channel.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b4d7b43-Selecting_Message_Channel.png",
        "Selecting Message Channel.png",
        2720,
        1316,
        "#f7f7fa"
      ],
      "border": true
    }
  ]
}
[/block]
The *Campaign* page displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9221b40-Campaign_Creation_Page.jpeg",
        "Campaign_Creation_Page.jpeg",
        1404,
        619,
        "#fbfafb"
      ],
      "border": true
    }
  ]
}
[/block]
4. Select *Live behavior* under *Start here* section and then click **Done**.
5. *Select Service Provider* from the dropdown list. 
You can also [Add a Service Provider](https://docs.clevertap.com/docs/generic-smtp) by clicking **Add a new service provider** link. After adding a provider, click **Refresh** to reflect the changes.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9f27992-Select_Email_Service_Provider.png",
        "Select Email Service Provider.png",
        2612,
        1528,
        "#faf8fb"
      ],
      "border": true
    }
  ]
}
[/block]
6. Click **Done**.
7. (Optional) Set a goal for your campaign and then click **Done**.
8. Select *Single action:New segment* from the *Find user from segment* list with conditions as shown in the following figure:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2d725a8-Selecting_the_evtName.png",
        "Selecting the evtName.png",
        2600,
        1221,
        "#f9f6fa"
      ],
      "border": true
    }
  ]
}
[/block]
9. Fetch the coupon code by typing “@” in the Email Editor under *What* section, which invokes a dropdown with the relevant event attributes. 
10. Select the coupon code that was pushed as the attribute pushed in the webhook.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/da93788-Email_editor.png",
        "Email editor.png",
        2124,
        1112,
        "#fafafa"
      ],
      "border": true
    }
  ]
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/21abd23-Email_campaign_preview.png",
        "Email campaign preview.png",
        2154,
        1114,
        "#fbfbfc"
      ],
      "border": true
    }
  ]
}
[/block]

For the remaining steps, follow the steps listed under [Create an Email Campaign](https://docs.clevertap.com/docs/email#email-campaign-creation-steps) to create your email campaign.