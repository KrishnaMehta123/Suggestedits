---
title: Shopify (WIP New workflow)
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
## Overview

CleverTap plugin provides an easy way to integrate your Shopify stores within minutes without any code. All you need is a CleverTap account and you can have a seamless flow of events and user data from your Shopify store. You can also send personalized messages to your users through channels such as [Web Push](doc:web-push) notifications, [Web Pop-up](doc:web-pop-ups), and [Web Exit Intent](doc:web-exit-intent). 

> 📘 Note
> 
> Enable the [Web Push](https://docs.clevertap.com/docs/shopify#section-enable-web-push) notifications from the CleverTap dashboard before integrating the plugin with your Shopify store.

# Integrate Your Shopify Store With CleverTap

You can integrate your Shopify store with CleverTap in a few minutes without having to code. This integration enables you to send events and user data from Shopify to CleverTap. Post integration,  
you can send personalized communication to your users through Web Push notifications, and Pop-ups. 

Follow the steps below to integrate your Shopify store with CleverTap.

## Step 1: Install the CleverTap app on Your Shopify Dashboard.

To install the CleverTap app on your Shopify Dashboard:

1. Visit the [Shopify App Store](https://apps.shopify.com/) and install the [CleverTap app](https://apps.shopify.com/clevertapapp) in your store.
2. You need to enter your Shopify store name and click _Continue_.

> 📘 Note
> 
> If the CleverTap app is not installed on your store, you need to install the app first to proceed further.  
> In case you have already installed the app, try uninstalling and reinstalling the app again. Learn more about app troubleshooting [here](https://docs.clevertap.com/docs/clevertap-shopify-app-troubleshooting).

## Step 2: Select Your Integration Preferences

After you install the CleverTap app successfully, you need to checkmark the _Receive events through Webhook SDK as well_ checkbox and click **Continue** to integrate the CleverTap SDK with your Shopify store.

## Step 3: Web Push Configuration

After setting the integration preferences, select your Web Push configuration preference, i.e whether you wish to integrate the web push feature or not. Basis your selection, click either _Continue_ or _Abort Integration_.

Upon selecting the _Integrate with web push_ option, you need to configure the Web Push channel from the _Settings_ section of the CleverTap dashboard. After the configuration, click the Refresh icon.

> 📘 Note
> 
> In case you choose to proceed without the web push integration, you will have to disconnect the plugin and perform the Shopify re-integration steps again.

## Step 4: App Embedment

As a final step, you need to ensure that you turn on the CleverTap-Shopify App Embed toggle from your Shopify store's dashboard to receive events through the SDK. 

Enable Web Push  
To enable Web Push:

1. Navigate to _Settings > Channels > Web Push _. 
2. Save the keys for Chrome and Firefox, and turn on the toggles for Web Push.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9db32c4-Shopify_enable_webpush.png",
        "Shopify_enable_webpush.png",
        946
      ],
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]

> 📘 Disable Web Push
> 
> If you do not want to continue sending personalized communication to your users through Web Push notifications, you can disable it by turning off the toggles for Chrome and Firefox.

## Step 2: Integrate Shopify Store with CleverTap

To integrate your Shopify store with CleverTap: 

1. Log in to the dashboard and navigate to _Settings > Project > Shopify_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c7b853e-Shopify_screen_new.png",
        "Shopify screen_new.png",
        2516
      ],
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]

Alternatively, you can also click **Integrate on other platforms**. The integration page displays. Select _Shopify_ from the list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/22dd870-Shopify_CT_Dashboard_menu.png",
        "Shopify_CT_Dashboard_menu.png",
        1037
      ],
      "border": true
    }
  ]
}
[/block]

2. Enter the _Shopify store name_ and then click **Connect**. The Shopify login page opens in a new tab.

3. Enter your Shopify username and password and proceed with the suggested steps to install the CleverTap app. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/41f03fc-Shopify_Store_credentials.png",
        "Shopify_Store_credentials.png",
        580
      ],
      "border": true
    }
  ]
}
[/block]

After connecting successfully, CleverTap starts receiving events and user properties of users visiting your Shopify store.

> 📘 Release Date
> 
> The new Shopify plugin was released on June 25, 2021.

# Supported Events

The following table displays all the events supported by the new plugin.  

| <p>Event Name</p>          | <p>Description</p>                                           | <p>Properties</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| :------------------------- | :----------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Page Browse</p>         | <p>This event is recorded when the user visits a page</p>    | <ul><li>Page - The store page. For example, Index page.</li><li>Title - Title of the page. For example, Acme home.</li><li>URL - URL of the page. For example, <a href="https://mystore.myshopify.com/">https://mystore.myshopify.com/</a>.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <p>Product Viewed</p>      | <p>When the user views a product</p>                         | <ul><li>Available - Availability of the product. For example, TRUE.</li><li>Currency - Shopify store currency. For example, INR. </li><li>Handle - Product Handle. For example, nike-sneakers-shoe.</li><li>ID - Product ID. For example, 6744256675993.</li><li>Price - Product Price. For example, 2999.</li><li>Title - Product Title. For example, Nike Sneakers Shoe. </li><li>TotalVariants - Number of variants available. For example, 3.</li><li>URL - URL of the product page. For example, /products/nike-sneakers-shoe.</li></ul>                                                                                                                                                                                                                                                                                                  |
| <p>Searched Product</p>    | <p>When a product is searched</p>                            | <ul><li>Currency - Shopify store currency.</li><li>Term - Search terms used. For example, red shoe.</li><li>TotalItems - Number of items in search results. For example, 1.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <p>Added To Cart</p>       | <p>When a product is added to cart</p>                       | <ul><li>Currency - Shopify store currency. For example, INR.</li><li>Image - URL of the product image. For example, <a href="https://cdn.shopify.com/s/files/products/RedT-shirt.jpg">https://cdn.shopify.com/s/files/products/RedT-shirt.jpg</a>.</li><li>Price - Product Price. For example, 2999.</li><li>ProductId - Product ID. For example, 6744249139353.</li><li>ProductType - Type of the product. For example, T-shirts.</li><li>Quantity - Product Quantity. For example, 1.</li><li>Title - Product Title. For example, Red T-shirt.</li><li>URL - Product URL. For example, /products/red-t-shirt-1?variant=39972529471641.</li><li>VariantId - Variant ID. For example, 39972529471641.</li><li>VariantTitle - Variant Title. For example, Nike Sneakers Shoe.</li><li>Vendor - Vendor name. For example, Acme stores.</li></ul> |
| <p>Removed from Cart</p>   | <p>When a product is removed from cart</p>                   | <ul><li>Currency - Shopify store currency. For example, INR.</li><li>Image - URL of the product image. For example, <a href="https://cdn.shopify.com/s/files/products/RedT-shirt.jpg">https://cdn.shopify.com/s/files/products/RedT-shirt.jpg</a>.</li><li>Price - Product Price. For example, 2999.</li><li>ProductId - Product ID. For example, 6744249139353.</li><li>ProductType - Type of the product. For example, T-shirts.</li><li>Quantity - Product Quantity. For example, 1.</li><li>Title - Product Title. For example, Red T-shirt.</li><li>URL - Product URL. For example, /products/red-t-shirt-1?variant=39972529471641.</li><li>VariantId - Variant ID. For example, 39972529471641.</li><li>VariantTitle - Variant Title. For example, Nike Sneakers Shoe.</li><li>Vendor - Vendor name. For example, Acme stores.</li></ul> |
| <p>Customer Registered</p> | <p>When a customer registers on the Shopify store</p>        | <ul><li>Email - Customer's email address. For example, jack@acme.com.</li><li>Name - Customer's name. For example, John Doe </li><li>FirstName - Customer's first name. For example, John. </li><li>LastName - Customer's last name. For example, Doe.</li><li>ID - Customer ID. For example, 5204453556377.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <p>Customer Logged In</p>  | <p>When a customer logs in to the Shopify store.</p>         | <ul><li>Email - Customer's email address. For example, jack@acme.com.</li><li>Name - Customer's name. For example, John Doe </li><li>FirstName - Customer's first name. For example, John. </li><li>LastName - Customer's last name. For example, Doe.</li><li>ID - Customer ID. For example, 5204453556377.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <p>Customer Logged Out</p> | <p>When a customer logs out of the Shopify store.</p>        | <p>None.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <p>Checkout</p>            | <p>When a customer checks out items.</p>                     | <ul><li>TotalItems - Number of items in the cart. For example, 5. </li><li>Currency - Shopify store currency. For example, INR.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <p>Charged</p>             | <p>When a customer successfully completes the purchase .</p> | <ul><li>Items - List of items charged with individual item properties such as Title, Vendor, quantity, price, productID and so on. For example, Items | 6612076593358|Running. Shoe|1|Acme, where  Product ID -  6612076593358,<br>Product Title - Running Shoe,<br>Quantity - 1, and<br>Vendor - Acme.</li><li>TotalItems - Total number of Items charged. For example, 3.</li><li>Currency - Shopify store currency. For example, INR.</li></ul>                                                                                                                                                                                                                                                                                                                                                                                             |

# Supported User Properties

The following table displays all the user properties supported by the plugin.

| User Property     | Property Description                                                                                                                                                                                             |
| :---------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name              | The customer's name. For example, Jack.                                                                                                                                                                          |
| Phone             | The customer's mobile number. For example, 97650000.                                                                                                                                                             |
| Email             | The customer's email address. For example, jack@acme.com.                                                                                                                                                        |
| Identity          | The customer's  CleverTap ID. For example, 3645910.                                                                                                                                                              |
| Tags              | The list of tags associated with the customer. For example, Gold customer.                                                                                                                                       |
| City              | The customer's city. For example, Mumbai.                                                                                                                                                                        |
| Accepts Marketing | This property returns the value as _true_ if the customer accepts marketing. If the customer does not accept then returns the value as _false_.                                                                  |
| Has Account       | This property returns the value as _true_ if the email associated with the customer is linked to a customer account. The property returns the value as false if the email is not linked to the customer account. |
| Orders Count      | The total number of orders from a customer.                                                                                                                                                                      |
| Tax Exempt        | Whether or not the customer is exempt from taxes.                                                                                                                                                                |
| Total Spent       | Total amount spent on all orders. For example, 5400.                                                                                                                                                             |
| Shopify Id        | The Shopify ID of the customer.  For example, 29873645910.                                                                                                                                                       |
| First Name        | The customer's first name.                                                                                                                                                                                       |
| LastName          | The customer's first name.                                                                                                                                                                                       |

# Setup Shopify Webhook

Webhooks are a useful tool for apps that want to sync with Shopify or take some action after a specific event occurs in the shop. You can use webhook subscriptions to receive notifications about particular events in a shop. For example, you might want to trigger an action such as an SMS or email when a customer places an order.

Follow these steps to configure each event through Shopify webhooks.

1. Go to the Shopify admin panel in your store. 
2. Go to _Settings > Notifications_. 
3. Scroll down to the _Webhooks_ section.
4. Click **Create Webhook**. The _Add webhook_ window appears.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/06a6309-Shopify_webhook.png",
        "Shopify_webhook.png",
        435
      ],
      "border": true
    }
  ]
}
[/block]

5. Select the [supported event](https://docs.clevertap.com/docs/shopify_webhooks#section-webhook-supported-events) from the list.
6. Enter the CleverTap endpoint URL. For example, [https://api.clevertap.com/shopify/m/\<Account-ID>](https://api.clevertap.com/shopify/m/&ltAccount-ID&gt)
7. Click Save.

## Webhook Supported Events

The following events are supported via the Shopify webhook:

- Checkout Created
- Checkout Updated
- Checkout Deleted 
- Customer Created
- Customer Updated
- Draft Order Created
- Draft Order Updated
- Fulfillment Created 
- Fulfillment Updated
- Order Cancelled 
- Order Created
- Order Fulfilled
- Charged
- Order Partially Fulfilled
- Order Updated

> 📘 Checkout and Order events
> 
> The Checkout Created, Checkout Updated, Checkout Deleted and Charged events are available automatically via webhooks for all Shopify plugin installs/reinstalls after 1st October 2021. There is no need to subscribe to these events manually.

# Create Web Campaigns

The CleverTap Shopify plugin provides support for web channels such as [Web Push](doc:web-push) , [Web Pop-up](doc:web-pop-ups) , and [Web Exit Intent](doc:web-exit-intent) without the need for any manual code integration.

To create a Web campaign:

1. From the dashboard, navigate to _Campaigns_.
2. Click **+ Campaign**.
3. Create a [Web Push](doc:web-push) , [Web Pop-up](doc:web-pop-ups) , or [Web Exit Intent](doc:web-exit-intent) campaign to engage your users.

# Migrate from the Previous Plugin

The new version of the Shopify plugin was released on June 25, 2021. The previous version of this plugin supports events such as Search, Category Viewed, Product Viewed, Added to Cart, and Charged. This version also provides support for  [Web Pop-up](doc:web-pop-ups) and [Web Exit Intent](doc:web-exit-intent) channels.

If you want to upgrade to the latest version of the plugin, please reach out to your _Customer Success_ personnel or raise a support ticket from the dashboard.

# Enable App Embed

By default, app embed blocks are deactivated after an app is installed. Merchants need to activate app embed blocks in the theme editor, from their Shopify theme settings. Refer to this detailed document on [App embeds](https://shopify.dev/apps/online-store/theme-app-extensions/extensions-framework#app-embed-blocks) to learn more.

To enable CleverTap's Shopify App Embed on your Shopify store:

1. Navigate to your Shopify store's theme settings page using the following URL  
   https\:// \< Your-Shopify-store-name>. myshopify.com/admin/themes/current/editor?context=apps&activateAppId=2566991a-cd89-49d8-997d-74717582b9ed/app-embed 
2. Toggle on the _Clevertap-Shopify_ App embed

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/22c77b8-CT_shopify_app_embed.png",
        "CT shopify app embed.png",
        2846
      ],
      "border": true
    }
  ]
}
[/block]

# FAQs

### Q. Does my current billing plan include integration with the Shopify plugin?

Yes. This Shopify plugin is available for all CleverTap billing plans.

### Q. I have already installed CleverTap’s Shopify plugin. How can I migrate to the new Shopify Plugin released by CleverTap on June 25, 2021?

Please reach out to your _Customer Success_ personnel or raise a support ticket from the dashboard.

### Q. I have a Shopify web store and a mobile app. How do I target users who have performed an event on my Shopify store?

Follow the steps:

1. Select the event (for example added to cart) in the CleverTap segment builder.
2. Filter by event property CT Source equal to Shopify.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f955291-shopify_segment_identify.png",
        "shopify_segment_identify.png",
        1005
      ],
      "border": true
    }
  ]
}
[/block]

### Q. I see a warning "Shopify installation seems to have a few missing files" displayed at the end of the Project page. How do I resolve this warning?

It is recommended to reinstall the plugin by clicking **Reinstall**.

### Q. Will this plugin work for Shopify Plus customers?

Yes. This Plugin works for Shopify Plus customers too.