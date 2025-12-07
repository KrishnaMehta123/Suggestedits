---
title: Gupshup
excerpt: Understand how to use Gupshup as your WhatsApp provider.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
# Overview
CleverTap supports customers sending and receiving WhatsApp messages using Gupshup as their provider. Once a provider is selected the user needs to create a template before creating a WhatsApp campaign.

## Select Gupshup Provider
Perform the following steps to select Gupshup as the messaging provider for WhatsApp.

1. From the CleverTap dashboard, navigate to *Settings* and click on **Channels**.
2. Select *WhatsApp*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/496ab50-2020-06-25_09-04-14_Add_provider.png",
        "2020-06-25_09-04-14_Add provider.png",
        647,
        252,
        "#f2f4f8"
      ],
      "border": true
    }
  ]
}
[/block]
3. Click**+Providers** then select *Gupshup* from the dropdown menu. 
Nexmo is the default provider.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/14ce97c-2020-06-25_09-12-35_Provider_credentials.png",
        "2020-06-25_09-12-35_Provider credentials.png",
        429,
        847,
        "#f2f4f7"
      ],
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]
  4. Enter the following credentials:

   * Nickname: Enter the nickname for this set of credentials.
   * Inbound message callback URL: This is a non-editable field. Gupshup maps this URL to receive the incoming messages in the CleverTap dashboard. 
   * Delivery reports callback URL: This is a non-editable field. Gupshup maps this URL to receive the notification delivery status for messages in the CleverTap dashboard. 
   * Notification account user ID: Enter the Notification Account/ HSM /1-way user ID.
   * Notification account password: Enter the Notification/ HSM /1-way account password.
   * Two-way account user ID: Enter the two-way account user ID.
   * Two-way account password: Enter the two-way account password.
   * App Name:  Enter the user name from Gupshup's analytics/unify dashboard.
   * Mobile Number: Enter either a Gupshup phone number or a shortcode. You can enter phone numbers or shortcodes listed under the Gupshup dashboard > profile > your account >WhatsApp Business Number.
    * Facebook URL: Enter the Facebook URL from the Gupshup dashboard.

[block:callout]
{
  "type": "info",
  "body": "The inbound message callback URL and delivery reports callback URL are non-editable fields. These values must be set up in your Gupshup account to allow CleverTap to receive inbound messages from end-users and delivery reports for messages sent through Gupshup.",
  "title": "Non-Editable Fields"
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cf55c41-2020-06-25_09-12-35_Provider_credentials1.png",
        "2020-06-25_09-12-35_Provider credentials1.png",
        704,
        1211,
        "#f8f9fa"
      ],
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "Auto Reply Checkbox",
  "body": "Select the checkbox if you want to set auto-replies for users not tracked by CleverTap. If a message is received from a phone number for which a profile is not present with CleverTap, then this default message is sent to the user."
}
[/block]
5. Click **Save**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4fbb7a9-2020-06-26_16-05-32_Saving_credentials.png",
        "2020-06-26_16-05-32_Saving credentials.png",
        729,
        332,
        "#f6f6f8"
      ],
      "border": true
    }
  ]
}
[/block]
##Add Multiple WhatsApp Phone Numbers
[block:callout]
{
  "type": "info",
  "title": "Adding Multiple Numbers",
  "body": "Customers can add multiple phone numbers for WhatsApp irrespective of their service provider. In case the business has multiple numbers, the autoresponse, FAQ response, and agent replies will go from the number that received the last message from customers."
}
[/block]
To add a phone number to your WhatsApp profile, follow step 3 onwards [here](https://docs.clevertap.com/docs/gupshup#select-gupshup-provider)

##Select Template

Once you have selected Gupshup as the provider, create a template for the campaign.

1. Select the *Templates* option, and click **+Template**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4e41af4-2020-06-25_10-21-57_Select_Templates.png",
        "2020-06-25_10-21-57_Select Templates.png",
        934,
        563,
        "#f7f7fa"
      ],
      "border": true
    }
  ]
}
[/block]
2. Enter the template name in the *namespace* field.
3. Choose the type of template header (Text or Media). For Media headers, you can use *Image*, *Video*, *Document*, and *Location*
4. Enter the message content.
5. You can also choose to add a Footer text and a Button (Quick Reply or a Call To Action).


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e54d574-gupshup_new_template.png",
        "gupshup new template.png",
        2200,
        1362,
        "#f3f3f7"
      ],
      "border": true
    }
  ]
}
[/block]
5. Click **Save**.

## Create Campaign

To create a WhatsApp campaign using Gupshup as the provider, refer to [Creating a WhatsApp Campaign](https://docs.clevertap.com/docs/whatsapp#section-creating-a-whatsapp-campaign) for detailed instructions.

## Troubleshooting

Errors during integration
Restricted IPs can cause errors during integration. Check that there are no IP restrictions enabled on the Gupshup account. To check the IPs from the CleverTap dashboard, go to *Settings > Channels > Mobile push*. The *FCM credentials *section lists the IPs that are used to send Whatsapp requests.  These IPs must be whitelisted on both the *one-way *and *two-way* account IDs of Gupshup.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e24891a-Gupshup_Whitelist_IPs.png",
        "Gupshup_Whitelist_IPs.png",
        810,
        405,
        "#f9f8fa"
      ]
    }
  ]
}
[/block]