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

[Talon.One](https://www.talon.one/) is a platform that allows you to create highly customizable promotional campaigns with the help of the *Campaign Manager* feature. With this integration, you can automate coupon generation and delivery to specific customer segments. You can embed Talon.One generated coupon codes directly into messages delivered through CleverTap. Thereby, optimizing the reach by sending campaigns at the right time on the right channels.\
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

<Image title="Create a Webhook.png" alt={3006} className="border" border={true} src="https://files.readme.io/2279edc-Create_a_Webhook.png" />

> 📘 *Display in Rule Builder* Checkbox
>
> Ensure that you select *Display in Rule Builder* checkbox to enable webhook for your campaign.

2. Select the request *Verb* from the dropdown list and then enter the *URL*. The following table lists down the API endpoint for the region of your account:

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Region
      </th>

      <th>
        CleverTap Dashboard URL
      </th>

      <th>
        API Endpoint
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        EU
      </td>

      <td>
        [https://eu1.dashboard.clevertap.com/login.html#/](https://eu1.dashboard.clevertap.com/login.html#/)
      </td>

      <td>
        [api.clevertap.com](api.clevertap.com)
      </td>
    </tr>

    <tr>
      <td>
        IN
      </td>

      <td>
        [https://in1.dashboard.clevertap.com/login.html#/](https://in1.dashboard.clevertap.com/login.html#/)
      </td>

      <td>
        [in1.api.clevertap.com](in1.api.clevertap.com)
      </td>
    </tr>

    <tr>
      <td>
        US
      </td>

      <td>
        [https://us1.dashboard.clevertap.com/login.html#](https://us1.dashboard.clevertap.com/login.html#/)
      </td>

      <td>
        [us1.api.clevertap.com](us1.api.clevertap.com)
      </td>
    </tr>

    <tr>
      <td>
        Singapore
      </td>

      <td>
        [https://sg1.dashboard.clevertap.com/login.html#/](https://sg1.dashboard.clevertap.com/login.html#/)
      </td>

      <td>
        [sg1.api.clevertap.com](sg1.api.clevertap.com)
      </td>
    </tr>
  </tbody>
</Table>

3. Enter the following CleverTap account details to set up the authentication headers:

* Project ID
* Passcode

  These details are obtained by navigating to the *Settings* page of the CleverTap dashboard.

<Image title="CT Project Details.png" alt={1660} className="border" border={true} src="https://files.readme.io/040af03-CT_Project_Details.png" />

4. Set up the parameters in the webhook payload for sending coupon codes\
   and update them to match your campaign requirements.

```json Webhook Payload for Sending Coupon Codes
{
  "d": [
     {
         "type": "event",
         "evtName": "Coupon Generated",
         "$source": "Talon.One",
         "identity": "${Profile ID}",
         "evtData": {
             "CouponGenerated":"${$CouponCode}"
         }
     }
     ]
     
 }
```

> 📘 Payload Parameters
>
> * The `evtName` parameter defines the EventName displayed on the CleverTap dashboard when selecting the campaign action. You can define the `evtName` as per your preference.
> * The `identity` is a mandatory parameter. This parameter is passed as the `userID`/`ProfileID`, which CleverTap uses to trigger the required engagement action effectively.

## II. Set Up a Campaign in Talon.One

To set up a campaign in Talon.One:

1. [Create a campaign](https://docs.talon.one/docs/product/campaigns/creating-campaigns#creating-a-campaign-from-scratch).
2. Ensure that you add the **Create a Coupon Code** [effect](https://docs.talon.one/docs/product/rules/effects/available-effects/#create-effects).
3. Select the *Store generated value in session* checkbox to send the effect-generated coupon code to CleverTap.

> 📘 Applying Effects to Campaigns
>
> When applying effects to the campaign, ensure that you [*Create the Coupon Code*](https://docs.talon.one/docs/product/campaigns/coupons/creating-coupons) and then *Create a Webhook Trigger*.

<Image title="Apply Effects to Campaigns.png" alt={2474} className="border" border={true} src="https://files.readme.io/881db3d-Apply_Effects_to_Campaigns.png" />

> 📘 Identify User
>
> Use a universal ID as the `profile ID` to identify the user across Talon.One and Clevertap dashboards.

## III. Create a Campaign in CleverTap

You can use Email, SMS, and Push channels on the CleverTap dashboard to send coupon codes generated on Talon.One dashboard.

### Create an Email Campaign

1. Navigate to *Messages* > *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select the messaging channel.

<Image title="Selecting Message Channel.png" alt={2720} className="border" border={true} src="https://files.readme.io/b4d7b43-Selecting_Message_Channel.png" />

The *Campaign* page displays.

<Image title="Campaign_Creation_Page.jpeg" alt={1404} className="border" border={true} src="https://files.readme.io/9221b40-Campaign_Creation_Page.jpeg" />

4. Select *Live behavior* under *Start here* section and then click **Done**.
5. *Select Service Provider* from the dropdown list.\
   You can also [Add a Service Provider](https://docs.clevertap.com/docs/generic-smtp) by clicking **Add a new service provider** link. After adding a provider, click **Refresh** to reflect the changes.

<Image title="Select Email Service Provider.png" alt={2612} className="border" border={true} src="https://files.readme.io/9f27992-Select_Email_Service_Provider.png" />

6. Click **Done**.
7. (Optional) Set a goal for your campaign and then click **Done**.
8. Select *Single action:New segment* from the *Find user from segment* list with conditions as shown in the following figure:

<Image title="Selecting the evtName.png" alt={2600} className="border" border={true} src="https://files.readme.io/2d725a8-Selecting_the_evtName.png" />

9. Fetch the coupon code by typing “@” in the Email Editor under *What* section, which invokes a dropdown with the relevant event attributes. 
10. Select the coupon code that was pushed as the attribute pushed in the webhook.

<Image title="Email editor.png" alt={2124} className="border" border={true} src="https://files.readme.io/da93788-Email_editor.png" />

<Image title="Email campaign preview.png" alt={2154} className="border" border={true} src="https://files.readme.io/21abd23-Email_campaign_preview.png" />

For the remaining steps, follow the steps listed under [Create an Email Campaign](https://docs.clevertap.com/docs/email#email-campaign-creation-steps) to create your email campaign.
