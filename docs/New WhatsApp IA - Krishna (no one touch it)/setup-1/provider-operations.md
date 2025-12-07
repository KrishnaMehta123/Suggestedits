---
title: Provider Operations
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
This section describes the different user actions for the available WhatsApp service providers.

<Image title="Service Provider Operations" alt="The image represents the WhatsApp service provider operations available for the end users." align="center" border={true} src="https://files.readme.io/eaa04e2-Service_Provider_Operations.png">
  Service Provider Operations
</Image>

## Edit Settings

You can edit the WhatsApp provider settings to update the provider configurations.

Follow the steps to edit provider settings:

* From the CleverTap dashboard, navigate to *Settings* > *Channels* > *WhatsApp* > Providers tab.
* Click the ellipsis next to the provider.
* Select *Edit settings* from the list. The provider credentials window displays.
* Update the required information.
* Click Send Test WhatsApp (Is this a button, please highlight) to check that the provider is working correctly. (I think a valid screenshot will help better understanding here)
* Click **Save**.

## Archive Service Providers

You can archive any of the current WhatsApp service providers from the settings. Archiving the WhatsApp service provider stops any active Campaigns or Journeys for this provider. The archived provider will not be available for use in the future. 

Follow the steps to archive a WhatsApp service provider:

* From the CleverTap dashboard, navigate to *Settings* > *Channels* > *WhatsApp* > Providers (highlight this as well) tab.
* Click the ellipsis next to the provider.
* Select *Archive* from the list. 

## Delete Service Providers

You can delete any of the current WhatsApp service providers from the settings. Deleting the WhatsApp service provider will remove all existing data from our system and stop any active Campaigns or Journeys. The deleted provider will not be available for use in the future.

Follow the steps to delete a WhatsApp service provider:

* From the CleverTap dashboard, navigate to *Settings* > *Channels* >*WhatsApp* > Providers tab.
* Click the ellipsis next to the provider.
* Select *Delete* from the list.

## Opt-in Users into WhatsApp

Most people do not like receiving unsolicited messages on WhatsApp. Therefore, it is important for you to explicitly request permission before sending messages to your users on their WhatsApp account. 

By default, CleverTap keeps all the profiles opted out of WhatsApp. To opt-in profiles, update the profile using the following code:

```json
"MSG-whatsapp":true
```

You have the following two ways to opt-in users for WhatsApp:

* [Opt-in via updating the user's profile property](https://developer.clevertap.com/docs/concepts-user-profiles#section-updating-the-user-profile). 
* [Opt-in via the API profile update](https://developer.clevertap.com/docs/upload-user-profiles-api). 

## Message Templates in WhatsApp

WhatsApp restricts brand-initiated messages (the messages that you send via campaigns) to pre-approved templates. You can fill in the variables in the templates to personalize a message. 

For example:

*Hello \{\{1}}, Congratulations on your ticket booking. Here is your ticket number: \{\{2}}. Please ensure you visit us on \{\{3}}. Enjoy your experience.*

The variables *\{\{1}}* or *\{\{2}}* or *\{\{3}}* can be replaced by a text of your choice. You can use CleverTap's event and profile personalization to personalize the message for your audience.

To set up a message template, follow the steps listed under [Sending Message Templates](https://developers.facebook.com/docs/whatsapp/message-templates/creation) documentation on Facebook.

## Configure Message Templates

All your message templates must be approved by WhatsApp. At CleverTap, we help you with the verification. For more information on how to create message templates, refer to the [Creating Message Templates](https://developers.facebook.com/docs/whatsapp/message-templates/creation/) documentation by Facebook. 

The media message templates allow you to expand the content you can send to the recipients beyond the standard messages. The template is organized primarily into four sections - *Header*, *Body*, *Footer*, and *Buttons*.

Using this template, you can attach media files (image, video, document, location) within the **Header** along with the message body. 

Additionally, WhatsApp also allows marketers to include **CTAs** or **Quick Reply** buttons in the text or media message templates for making the conversations more interactive. 

* Call-to-Action (CTAs) — Enables the customer to make a phone call or visit a website.
* Quick Reply — Allows your customer to respond with a simple text message.

Once your interactive message templates have been created and approved, you can use them in notification messages as well as customer service/care messages.

The images below represent different templates that marketers can create for engaging their customers effectively.

<Image title="Templates.png" alt={2318} align="center" border={true} src="https://files.readme.io/fa88774-Templates.png">
  WhatsApp Message Templates
</Image>

After your templates are verified, you can add them in the WhatsApp settings under the *Templates* tab.

To use WhatsApp with CleverTap, it is important to copy the templates accurately in the settings by performing the following steps:

1. From the dashboard, navigate to *Account > Settings > Engage > Channels > WhatsApp*. 
2. Click one of the Provider names.

<Image title="image.png" alt={1894} align="center" border={true} src="https://files.readme.io/c423fd6-image.png">
  WhatsApp Providers
</Image>

3. Navigate to the **Templates** tab.
4. Click **+ Template** .

<Image title="Screenshot 2021-09-21 at 8.37.29 PM.png" alt={2346} align="center" border={true} src="https://files.readme.io/af37717-Screenshot_2021-09-21_at_8.37.29_PM.png">
  Add Template
</Image>

5. Now, enter the *Namespace* for your template.

> 🚧 Namespace Format
>
> When copying the message templates from the WABA dashboard, use the following format for the namespace: \<template*namespace>:\<template\_name>. You can find the \_Namespace* value from the *Message templates* section on the WABA dashboard as shown in the image below:

<Image title="namespace.png" alt={2879} align="center" border={true} src="https://files.readme.io/f755093-namespace.png">
  Message Template Namespace
</Image>

Following is an example of *Namespace* format

<Image title="Screenshot 2021-09-23 at 1.01.12 PM.png" alt={1354} align="center" border={true} src="https://files.readme.io/d7f6250-Screenshot_2021-09-23_at_1.01.12_PM.png">
  Namespace Format
</Image>

6. Copy and save the approved message templates from your WABA dashboard.

<Image title="Whatsapp interactive.png" alt={1452} align="center" border={true} src="https://files.readme.io/5729acc-Whatsapp_interactive.png">
  Save WhatsApp Template
</Image>

7. Click **Save Template** to save the message template.  

> 📘 Language Support
>
> * For Vonage (Nexmo), if you don't find the required language support on the CleverTap dashboard, contact our support team to enable the required language for your account.
> * Gupshup supports and handles all languages automatically, hence you do not need to add them on the CleverTap dashboard.
