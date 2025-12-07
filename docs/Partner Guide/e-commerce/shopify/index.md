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

* [Import Existing Shopify Data into CleverTap](https://staging.docs.user.clevertap.net/docs/import-existing-shopify-data-into-clevertap)
* [Cart Abandonment Use Case](https://staging.docs.user.clevertap.net/docs/cart-abandonment-use-case)
* [Advanced Customization](https://staging.docs.user.clevertap.net/docs/advanced-customization)

# Integrate Shopify

You can install the [CleverTap App](https://apps.shopify.com/clevertapapp) from the [Shopify App Store](https://help.shopify.com/en/manual/apps/installing-apps).  Login to the CleverTap dashboard and follow the steps to complete the integration:

Follow the steps to locate the Shopify plugin on the CleverTap dashboard:

1. Login to your CleverTap account. 
2. Open *Settings* >  *Project* > *Shopify*.

<Image alt="Locate the Shopify Plugin" align="center" border={true} src="https://files.readme.io/0679d38ea0225a454b29096f5981d759169d7c9cb04c4cb4ca1dc7a7fb231eb7-shopify_integration.png">
  Locate the Shopify Plugin
</Image>

3. The *Shopify* window displays. Click **Integrate Store** to start the integration. 

The integration includes the following steps: 

1. [Install and Connect App](https://docs.clevertap.com/docs/shopify#install-and-connect-app)
2. [Configure Web Push](https://docs.clevertap.com/docs/shopify#configure-web-push) 
3. [Customize Profile Properties](https://docs.clevertap.com/docs/shopify#profile-properties)
4. [Customize Events](https://docs.clevertap.com/docs/shopify#events)
5. [Enable App Embed](https://docs.clevertap.com/docs/shopify#enable-app-embed)

## Install and Connect App

If you have already installed the app from the Shopify App Store,  *App Installed* is displayed next to your store name. However, if you are installing the app for the first time, you can install it from the Shopify dashboard.

Follow the steps below to install the CleverTap app:

1. Click the *Install CleverTap on Shopify dashboard* link. 

<Image alt="Install from CleverTap " align="center" width="100% " border={true} src="https://files.readme.io/e58a9a96d1d155be825aab2847e1dae6946d050a6be7299c66d51f3b4ff01ee1-store_integrate.png">
  Install from CleverTap 
</Image>

2. The link opens the *Shopify App Store*  page. Check that you are logged in to the store and click **Install**.

<Image alt="Install CleverTap App from Shopify Store" align="center" border={true} src="https://files.readme.io/0f34d65-Shopify_app_store_install.jpg">
  Install CleverTap App
</Image>

3. You can now connect your store from the CleverTap dashboard and click **Continue**. 

<Image alt="Enter Shopify Store Name" align="center" border={true} src="https://files.readme.io/f3aa81c4494537c21943cdb8d6876112e0432760fcf0e24731abf102e370338c-johnshoes.png">
  Enter Shopify Store Name
</Image>

4. Enter your credentials if you are not logged in to your Shopify store and continue the process.

Your store is now connected to your CleverTap account. You can start customizing it per your requirements. For more details, refer to [Advanced Customization](https://staging.docs.user.clevertap.net/docs/advanced-customization).

## Enable App Embed Status

The *App Embed* status informs you if the app embed block is active. By default, app embed blocks are deactivated after an app is installed. 

The *App Embed* status displays as *Enabled* if enabled already. However, if the *App Embed* status is *Disabled* , merchants must activate app embed blocks in the theme editor, from their Shopify theme settings. Refer to this detailed document on [App embeds](https://shopify.dev/apps/online-store/theme-app-extensions/extensions-framework#app-embed-blocks) to learn more. To enable *CleverTap-Shopify App Embed* on your Shopify store:

1. Navigate to your Shopify store's theme settings page using the following URL:

```
https\://<Your-Shopify-store-name>.myshopify.com/admin/themes/current/editor?context=apps&activateAppId=2566991a-cd89-49d8-997d-74717582b9ed/app-embed.
```

2. Toggle ON the *Clevertap-Shopify* App embed and click  **Save** at the top right corner.

<Image title="Navigate to your Shopify store and toggle ON the CleverTap-Shopify option" alt={2846} align="center" border={true} src="https://files.readme.io/22c77b8-CT_shopify_app_embed.png">
  Toggle ON CleverTap-Shopify
</Image>

To check if the *CleverTap-Shopify* App embed is enabled:

1. Navigate to your Shopify store,  right-click and, select *Inspect*. 
2. Navigate to *Sources* tab and select *Page*. 
3. Search for the *clevertap-shopify.js* file in the *extensions* folder under *cdn.Shopify.com*. Refer to the following image:

<Image title="Verifying if CleverTap-Shopify app embed is enabled" alt={2262} align="center" border={true} src="https://files.readme.io/4f64635-shopify_app_ambed.png">
  Verify if CleverTap-Shopify App Embed is Enabled
</Image>

# Create Web Campaigns

The CleverTap Shopify plugin provides support for web channels such as [Web Push](doc:web-push) , [Web Pop-up](doc:web-pop-ups) , and [Web Exit Intent](doc:web-exit-intent) without the need for any manual code integration.

To create a Web campaign:

1. From the dashboard, navigate to *Campaigns*.
2. Click **+ Campaign**.
3. Create a [Web Push](doc:web-push) , [Web Pop-up](doc:web-pop-ups) , or [Web Exit Intent](doc:web-exit-intent) campaign to engage your users.

# FAQs

### Does my current billing plan include integration with the Shopify plugin?

Yes. This Shopify plugin is available for all CleverTap billing plans.

### I have a Shopify web store and a mobile app. How do I target users who have performed an event on my Shopify store?

To target the users who have performed the event on your store:

1. Select the event (for example, added to cart) in the CleverTap segment builder.
2. Filter by event property *CT Source* equal to *Shopify*.

<Image title="Filtering Shopify users from Find People page" alt={1005} align="center" border={true} src="https://files.readme.io/f955291-shopify_segment_identify.png">
  Filtering Shopify Users from Find People Page  
</Image>

### I see a warning *Shopify installation seems to have a few missing files* displayed at the end of the Project page. How do I resolve this warning?

CleverTap recommends reinstalling the plugin by clicking **Reinstall**.

### Will this plugin work for Shopify Plus customers?

Yes. This Plugin works for Shopify Plus customers too.

# Video Tutorial - Integrating Shopify Store with CleverTap

<HTMLBlock>{`
<div
              style="
                position: relative;
                padding-bottom: 56.25%;
                height: 0;
                border-radius: 0;
                box-shadow: 0 15px 40px rgba(63,58,79,.3);
                overflow: hidden;
                min-width:320px"><iframe
              src="https://clevertap.portal.trainn.co/share/1tlxbIKZMm3pdrBujijGXQ/embed?autoplay=false"
              frameborder="0"
              webkitallowfullscreen
              mozallowfullscreen
              allowfullscreen
              allow="autoplay; fullscreen"
              style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
`}</HTMLBlock>
