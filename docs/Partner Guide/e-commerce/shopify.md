---
title: Shopify
excerpt: Learn how to integrate your Shopify store with CleverTap.
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

CleverTap plugin provides an easy way to integrate your Shopify stores within minutes without any code. All you need is a CleverTap account and you can have a seamless flow of events and user data from your Shopify store. You can also send personalized messages to your users through channels such as [Web Push](doc:web-push), [Web Pop-up](doc:web-pop-ups), [Web Exit Intent](doc:web-exit-intent), and [Web Native Display](https://docs.clevertap.com/docs/web-native-display).  

For more details on Shopify features, refer to the following documents:

- [Import Existing Shopify Data into CleverTap](https://staging.docs.user.clevertap.net/docs/import-existing-shopify-data-into-clevertap)
- [Cart Abandonment Use Case](https://staging.docs.user.clevertap.net/docs/cart-abandonment-use-case)
- [Advanced Customization](https://staging.docs.user.clevertap.net/docs/advanced-customization)

# Integrate Shopify

You can install the [CleverTap App](https://apps.shopify.com/clevertapapp) from the [Shopify App Store](https://help.shopify.com/en/manual/apps/installing-apps).  Login to the CleverTap dashboard and follow the steps to complete the integration:

Follow the steps to locate the Shopify plugin on the CleverTap dashboard:

1. Login to your CleverTap account. 
2. Open _Settings_ >  _Project_ > _Shopify_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0679d38ea0225a454b29096f5981d759169d7c9cb04c4cb4ca1dc7a7fb231eb7-shopify_integration.png",
        null,
        "Locate the Shopify Plugin"
      ],
      "align": "center",
      "border": true,
      "caption": "Locate the Shopify Plugin"
    }
  ]
}
[/block]


3. The _Shopify_ window displays. Click ** Integrate Store** to start the integration. 

The integration includes the following steps: 

1. [Install and Connect App](https://docs.clevertap.com/docs/shopify#install-and-connect-app)
2. [Configure Web Push](https://docs.clevertap.com/docs/shopify#configure-web-push) 
3. [Customize Profile Properties](https://docs.clevertap.com/docs/shopify#profile-properties)
4. [Customize Events](https://docs.clevertap.com/docs/shopify#events)
5. [Enable App Embed](https://docs.clevertap.com/docs/shopify#enable-app-embed)

## Install and Connect App

If you have already installed the app from the Shopify App Store,  _App Installed _ is displayed next to your store name. However, if you are installing the app for the first time, you can install it from the Shopify dashboard.

Follow the steps below to install the CleverTap app:

1. Click the_ Install CleverTap on Shopify dashboard_ link. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e58a9a96d1d155be825aab2847e1dae6946d050a6be7299c66d51f3b4ff01ee1-store_integrate.png",
        null,
        "Install from CleverTap "
      ],
      "align": "center",
      "sizing": "100% ",
      "border": true,
      "caption": "Install from CleverTap "
    }
  ]
}
[/block]


2. The link opens the _Shopify App Store_  page. Check that you are logged in to the store and click **Install**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0f34d65-Shopify_app_store_install.jpg",
        null,
        "Install CleverTap App from Shopify Store"
      ],
      "align": "center",
      "border": true,
      "caption": "Install CleverTap App"
    }
  ]
}
[/block]


3. You can now connect your store from the CleverTap dashboard and click **Continue**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f3aa81c4494537c21943cdb8d6876112e0432760fcf0e24731abf102e370338c-johnshoes.png",
        "",
        "Enter Shopify Store Name"
      ],
      "align": "center",
      "border": true,
      "caption": "Enter Shopify Store Name"
    }
  ]
}
[/block]


4. Enter your credentials if you are not logged in to your Shopify store and continue the process.

Your store is now connected to your CleverTap account. You can start customizing it per your requirements. For more details, refer to [Advanced Customization](https://staging.docs.user.clevertap.net/docs/advanced-customization).

## Enable App Embed Status

The _App Embed_ status informs you if the app embed block is active. By default, app embed blocks are deactivated after an app is installed. 

The _App Embed_ status displays as _Enabled_ if enabled already. However, if the _App Embed_ status is _Disabled_ , merchants must activate app embed blocks in the theme editor, from their Shopify theme settings. Refer to this detailed document on [App embeds](https://shopify.dev/apps/online-store/theme-app-extensions/extensions-framework#app-embed-blocks) to learn more. To enable _CleverTap-Shopify App Embed_ on your Shopify store:

1. Navigate to your Shopify store's theme settings page using the following URL:

```
https\://<Your-Shopify-store-name>.myshopify.com/admin/themes/current/editor?context=apps&activateAppId=2566991a-cd89-49d8-997d-74717582b9ed/app-embed.
```

2. Toggle ON the _Clevertap-Shopify_ App embed and click  **Save** at the top right corner.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/22c77b8-CT_shopify_app_embed.png",
        "Navigate to your Shopify store and toggle ON the CleverTap-Shopify option",
        2846
      ],
      "align": "center",
      "border": true,
      "caption": "Toggle ON CleverTap-Shopify"
    }
  ]
}
[/block]


To check if the _CleverTap-Shopify_ App embed is enabled:

1. Navigate to your Shopify store,  right-click and, select _Inspect_. 
2. Navigate to _Sources_ tab and select _Page_. 
3. Search for the _clevertap-shopify.js_ file in the _extensions_ folder under _cdn.Shopify.com_. Refer to the following image:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4f64635-shopify_app_ambed.png",
        "Verifying if CleverTap-Shopify app embed is enabled",
        2262
      ],
      "align": "center",
      "border": true,
      "caption": "Verify if CleverTap-Shopify App Embed is Enabled"
    }
  ]
}
[/block]


# Create Web Campaigns

The CleverTap Shopify plugin provides support for web channels such as [Web Push](doc:web-push) , [Web Pop-up](doc:web-pop-ups) , and [Web Exit Intent](doc:web-exit-intent) without the need for any manual code integration.

To create a Web campaign:

1. From the dashboard, navigate to _Campaigns_.
2. Click **+ Campaign**.
3. Create a [Web Push](doc:web-push) , [Web Pop-up](doc:web-pop-ups) , or [Web Exit Intent](doc:web-exit-intent) campaign to engage your users.

# FAQs

### Does my current billing plan include integration with the Shopify plugin?

Yes. This Shopify plugin is available for all CleverTap billing plans.

### I have a Shopify web store and a mobile app. How do I target users who have performed an event on my Shopify store?

To target the users who have performed the event on your store:

1. Select the event (for example, added to cart) in the CleverTap segment builder.
2. Filter by event property _CT Source_ equal to _Shopify_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f955291-shopify_segment_identify.png",
        "Filtering Shopify users from Find People page",
        1005
      ],
      "align": "center",
      "border": true,
      "caption": "Filtering Shopify Users from Find People Page  "
    }
  ]
}
[/block]


### I see a warning _Shopify installation seems to have a few missing files_ displayed at the end of the Project page. How do I resolve this warning?

CleverTap recommends reinstalling the plugin by clicking **Reinstall**.

### Will this plugin work for Shopify Plus customers?

Yes. This Plugin works for Shopify Plus customers too.

# Video Tutorial - Integrating Shopify Store with CleverTap

[block:html]
{
  "html": "<div\n              style=\"\n                position: relative;\n                padding-bottom: 56.25%;\n                height: 0;\n                border-radius: 0;\n                box-shadow: 0 15px 40px rgba(63,58,79,.3);\n                overflow: hidden;\n                min-width:320px\"><iframe\n              src=\"https://clevertap.portal.trainn.co/share/1tlxbIKZMm3pdrBujijGXQ/embed?autoplay=false\"\n              frameborder=\"0\"\n              webkitallowfullscreen\n              mozallowfullscreen\n              allowfullscreen\n              allow=\"autoplay; fullscreen\"\n              style=\"position: absolute; top: 0; left: 0; width: 100%; height: 100%;\"></iframe></div>"
}
[/block]