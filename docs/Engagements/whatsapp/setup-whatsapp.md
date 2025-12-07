---
title: Setup
excerpt: Understand how to set up WhatsApp as a channel for your marketing campaigns
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: >-
    Refer to the pages listed below to learn more about the following WhatsApp
    sections:
---
# Overview

CleverTap offers WhatsApp as a paid add-on, allowing businesses to communicate with their customers effectively and efficiently.

To enable WhatsApp as a communication channel for your organization, you need to raise a request on [sales@clevertap.com](mailto:sales@clevertap.com).

# Getting Started

To use WhatsApp as a channel for your marketing campaigns and customer journeys, you need access to the WhatsApp Business API.\
CleverTap currently supports no-code integration with the following partners:

* Gupshup
* Nexmo
* ValueFirst
* Exotel

If you have access to the WhatsApp Business API through a service provider that is not currently supported by CleverTap, you can use CleverTap's [Generic WhatsApp APIs](https://docs.clevertap.com/docs/generic-whatsapp) to integrate your service provider with CleverTap. 

Alternatively, you can request your service provider to become a supported WhatsApp partner by integrating CleverTap's generic API with their native messaging APIs using middleware.

By enabling your service (check for all such instances) provider with CleverTap, you'll be able to utilize all the features and benefits offered by our platform.

> 📘 Note
>
> To access the WhatsApp Business API directly through CleverTap, refer to the detailed [integration document](https://docs.clevertap.com/docs/clevertap-bsp).

# Setup WhatsApp Service Provider

To setup a WhatsApp service provider, perform the following steps:

* From the dashboard, navigate to *Settings* > *Channels* > *WhatsApp*.
* Click **+ Provider** to add a provider.

<Image title="Add WhatsApp Service Provider" alt="Click the +Provider button to add a new service provider for WhatsApp" align="center" border={true} src="https://files.readme.io/70663ad-Add_WhatsApp_Service_Provider.png">
  Add WhatsApp Service Provider
</Image>

* Add the WhatsApp service provider's information.
* Click **Send Test WhatsApp** to check if the provider has been set up correctly and can send WhatsApp messages. 

<Image title="Save Provider Details" alt="Click the Save button to save the WhatsApp provider details." align="center" border={true} src="https://files.readme.io/043a64e-Save_Provider_Details.png">
  Save Provider Details
</Image>

* Click **Save** 

Refer to the following integration guides for more details:

* [Adding Gupshup as a provider](https://docs.clevertap.com/docs/gupshup).
* [Adding Nexmo as a provider](https://docs.clevertap.com/docs/nexmo-whatsapp).
* [Adding ValueFirst as a provider](https://docs.clevertap.com/docs/valuefirst-digital-whatsapp).
* [Adding Exotel as a provider](https://docs.clevertap.com/docs/exotel-whatsapp). 

# Provider Operations

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

## Enable Click Tracking for WhatsApp

You can track button clicks from your WhatsApp message. To enable click tracking:

1. From the dashboard, navigate to *Account > Settings > Engage > Channels > WhatsApp*. 
2. Click one of the Provider names.
3. Click **+ Template** .
4. Add a CTA button. 
5. Select the URL type. 
   1. Static : Add a static link.
   2. Dynamic: Add a dynamic link. 
   3. CleverTap Link Tracking : Add the link for tracking user clicks. For example, [www.ct1.io/\{\{1}}](http://www.ct1.io/\{\{1}}). The URL will be automatically displayed for CleverTap BSP.
