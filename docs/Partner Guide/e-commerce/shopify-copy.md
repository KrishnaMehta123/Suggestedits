---
title: Shopify (COPY) New workflow Sunil
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

> 📘 Release Date
>
> The new Shopify plugin was released on June 25, 2021.

# Integrate Shopify

You can install the [CleverTap App](https://apps.shopify.com/clevertapapp) from the [Shopify App Store](https://help.shopify.com/en/manual/apps/installing-apps).  Login to the CleverTap dashboard and follow the steps to complete the integration:

Follow the steps to locate the Shopify plugin on the CleverTap dashboard:

1. Login to your CleverTap account. 
2. Open *Settings* >  *Project* > *Shopify*.

<Image align="center" className="border" border={true} src="https://files.readme.io/0ecc3db-CleverTap_Dashboard.png" />

3. The Shopify window displays. Click **Integrate Store** to start the integration. 

The integration includes the following steps:

1. [Check App Installation](https://docs.clevertap.com/docs/shopify-copy#app-installation).
2. [Select integration preferences](https://docs.clevertap.com/docs/shopify-copy#integration-preferences).
3. [Configure Web Push](https://docs.clevertap.com/docs/shopify-copy#web-push-configuration).
4. [Check App Embed Status](https://docs.clevertap.com/docs/shopify-copy#enable-app-embed).

## App Installation

Enter your store name and click **Continue** .  If you have already installed the app from the Shopify App Store, you will see \_App Installed \_next to your store name. 

<Image align="center" className="border" width="50% " border={true} src="https://files.readme.io/d99c87b-CT_Dashboard_Shopify_Steps.png" />

1. If you have not installed the CleverTap app in the first step, click the *Install CleverTap app on the Shopify dashboard* link. 

<Image align="center" className="border" width="60% " border={true} src="https://files.readme.io/2e2baf8-Shopify_App_Not_Installed.png" />

2. The link opens the Shopify App Store page. Click **Add App**.

<Image align="center" className="border" border={true} src="https://files.readme.io/1c3796e-Shopify_Store_Add_CleverTap_App.png" />

4. Click **Install App**. \<\<@sunil to magnify the install app button>> 


<Image align="center" className="border" border={true} src="https://files.readme.io/83f9977-Install_Shopify_App_from_App_Store.png" />

## Integration Preferences

After installing the CleverTap App from the Shopify App store, log in to your CleverTap dashboard to specify integration preferences. 

We have already setup your Shopify store to receive events from Shopify Webhooks. You will automatically receive a few events for your Shopify store from [Shopify Webhooks](https://docs.clevertap.com/docs/shopify-copy#setup-shopify-webhook). You can [manually subscribe](https://docs.clevertap.com/docs/shopify#setup-shopify-webhook) to additional events from your Shopify dashboard.

Select \_Receive events through SDK \_if you want CleverTap to record [supported events](https://docs.clevertap.com/docs/shopify-copy#web-push-configuration) from your Shopify store. 

<Image align="center" className="border" width="50% " border={true} src="https://files.readme.io/a91e42e-CT_Dashboard_Shopify_Integration_Preferences.png" />

## Web Push Configuration

You can send personalized communication to your users through Web Push notifications. However, you must enable them first from the CleverTap dashboard.

Select *Integrate with Web Push*  to use CleverTap Web Push notifications. If the Web Push is not configured, you must  [configure the Web Push](https://docs.clevertap.com/docs/setup-web-push)  from the CleverTap dashboard.

<Image align="center" className="border" width="50% " border={true} src="https://files.readme.io/db6c884-CT_Dashboard_Shopify_Web_Push_Configuration.png" />

## Enable App Embed

The *App Embed\_status displays as \_Enabled* if it has been enabled already. 

<Image align="center" className="border" width="50% " border={true} src="https://files.readme.io/0a29575-CT_Dashboard_Shopify_App_Embed_Status.png" />

The \_App Embed \_status informs you if it is active. By default, app embed blocks are deactivated after an app is installed. Merchants must activate app embed blocks in the theme editor, from their Shopify theme settings. Refer to this detailed document on [App embeds](https://shopify.dev/apps/online-store/theme-app-extensions/extensions-framework#app-embed-blocks) to learn more.

To enable CleverTap-Shopify App Embed on your Shopify store:


1. Navigate to your Shopify store's theme settings page using the following URL:\
   https\://&lt;Your-Shopify-store-name&gt;.myshopify.com/admin/themes/current/editor?context=apps\&activateAppId=2566991a-cd89-49d8-997d-74717582b9ed/app-embed.
2. Toggle ON the *Clevertap-Shopify* App embed and click the **Save** button at the top right corner.

<Image title="Navigate to your Shopify store and toggle ON the CleverTap-Shopify option" alt={2846} align="center" border={true} src="https://files.readme.io/22c77b8-CT_shopify_app_embed.png">  Toggle ON CleverTap-Shopify











To check whether the *CleverTap-Shopify* App embed is enabled:

1. Navigate to your Shopify store -> right-click and select *Inspect* -> navigate to *Sources* tab -> *Page*. 
2. Search for the *clevertap-shopify.js* file in the *extensions* folder under *cdn.Shopify.com*. Refer to the image below for a better understanding.

<Image title="Verifying if CleverTap-Shopify app embed is enabled" alt={2262} align="center" border={true} src="https://files.readme.io/4f64635-shopify_app_ambed.png">  Verifying if CleverTap-Shopify App Embed is Enabled











# Supported Events

The following table displays all the events supported by the new plugin.
<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Event Name
      </th>

      <th>
        Description
      </th>

      <th>
        Properties
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Page Browse
      </td>

      <td>
        This event is recorded when the user visits a page
      </td>

      <td>
        <ul>  
        <li>Page - The store page. For example, Index page.</li>  
        <li>Title - Title of the page. For example, Acme home.</li>  
        <li>URL - URL of the page. For example, <a href="https://mystore.myshopify.com/">https\://mystore.myshopify.com/</a>.</li>  
        </ul>
      </td>
    </tr>

    <tr>
      <td>
        Product Viewed
      </td>

      <td>
        When the user views a product
      </td>

      <td>
        <ul>  
        <li>Available - Availability of the product. For example, TRUE.</li>  
        <li>Currency - Shopify store currency. For example, INR. </li>  
        <li>Handle - Product Handle. For example, nike-sneakers-shoe.</li>  
        <li>ID - Product ID. For example, 6744256675993.</li>  
        <li>Price - Product Price. For example, 2999.</li>  
        <li>Title - Product Title. For example, Nike Sneakers Shoe. </li>  
        <li>TotalVariants - Number of variants available. For example, 3.</li>  
        <li>URL - URL of the product page. For example, /products/nike-sneakers-shoe.</li>  
        </ul>
      </td>
    </tr>

    <tr>
      <td>
        Searched Product
      </td>

      <td>
        When a product is searched
      </td>

      <td>
        <ul>  
        <li>Currency - Shopify store currency.</li>  
        <li>Term - Search terms used. For example, red shoe.</li>  
        <li>TotalItems - Number of items in search results. For example, 1.</li>  
        </ul>
      </td>
    </tr>

    <tr>
      <td>
        Added To Cart
      </td>

      <td>
        When a product is added to cart
      </td>

      <td>
        <ul>  
        <li>Currency - Shopify store currency. For example, INR.</li>  
        <li>Image - URL of the product image. For example, <a href="https://cdn.shopify.com/s/files/products/RedT-shirt.jpg">https\://cdn.shopify.com/s/files/products/RedT-shirt.jpg</a>.</li>  
        <li>Price - Product Price. For example, 2999.</li>  
        <li>ProductId - Product ID. For example, 6744249139353.</li>  
        <li>ProductType - Type of the product. For example, T-shirts.</li>  
        <li>Quantity - Product Quantity. For example, 1.</li>  
        <li>Title - Product Title. For example, Red T-shirt.</li>  
        <li>URL - Product URL. For example, /products/red-t-shirt-1?variant=39972529471641.</li>  
        <li>VariantId - Variant ID. For example, 39972529471641.</li>  
        <li>VariantTitle - Variant Title. For example, Nike Sneakers Shoe.</li>  
        <li>Vendor - Vendor name. For example, Acme stores.</li>  
        </ul>
      </td>
    </tr>

    <tr>
      <td>
        Removed from Cart
      </td>

      <td>
        When a product is removed from cart
      </td>

      <td>
        <ul>  
        <li>Currency - Shopify store currency. For example, INR.</li>  
        <li>Image - URL of the product image. For example, <a href="https://cdn.shopify.com/s/files/products/RedT-shirt.jpg">https\://cdn.shopify.com/s/files/products/RedT-shirt.jpg</a>.</li>  
        <li>Price - Product Price. For example, 2999.</li>  
        <li>ProductId - Product ID. For example, 6744249139353.</li>  
        <li>ProductType - Type of the product. For example, T-shirts.</li>  
        <li>Quantity - Product Quantity. For example, 1.</li>  
        <li>Title - Product Title. For example, Red T-shirt.</li>  
        <li>URL - Product URL. For example, /products/red-t-shirt-1?variant=39972529471641.</li>  
        <li>VariantId - Variant ID. For example, 39972529471641.</li>  
        <li>VariantTitle - Variant Title. For example, Nike Sneakers Shoe.</li>  
        <li>Vendor - Vendor name. For example, Acme stores.</li>  
        </ul>
      </td>
    </tr>

    <tr>
      <td>
        Customer Registered
      </td>

      <td>
        When a customer registers on the Shopify store
      </td>

      <td>
        <ul>  
        <li>Email - Customer's email address. For example, jack@acme.com.</li>  
        <li>Name - Customer's name. For example, John Doe </li>  
        <li>FirstName - Customer's first name. For example, John. </li>  
        <li>LastName - Customer's last name. For example, Doe.</li>  
        <li>ID - Customer ID. For example, 5204453556377.</li>  
        </ul>
      </td>
    </tr>

    <tr>
      <td>
        Customer Logged In
      </td>

      <td>
        When a customer logs in to the Shopify store.
      </td>

      <td>
        <ul>  
        <li>Email - Customer's email address. For example, jack@acme.com.</li>  
        <li>Name - Customer's name. For example, John Doe </li>  
        <li>FirstName - Customer's first name. For example, John. </li>  
        <li>LastName - Customer's last name. For example, Doe.</li>  
        <li>ID - Customer ID. For example, 5204453556377.</li>  
        </ul>
      </td>
    </tr>

    <tr>
      <td>
        Customer Logged Out
      </td>

      <td>
        When a customer logs out of the Shopify store.
      </td>

      <td>
        None.
      </td>
    </tr>

    <tr>
      <td>
        Checkout
      </td>

      <td>
        When a customer checks out items.\
        (Note that this event will only be available on CleverTap
      </td>

      <td>
        <ul>  
        <li>TotalItems - Number of items in the cart. For example, 5. </li>  
        <li>Currency - Shopify store currency. For example, INR.</li>  
        </ul>
      </td>
    </tr>

    <tr>
      <td>
        Charged
      </td>

      <td>
        When a customer successfully completes the purchase .
      </td>

      <td>
        <ul>  
        <li>Items - List of items charged with individual item properties such as Title, Vendor, quantity, price, productID and so on. For example, Items | 6612076593358|Running. Shoe|1|Acme, where  Product ID -  6612076593358,<br />  
        Product Title - Running Shoe,<br />  
        Quantity - 1, and<br />  
        Vendor - Acme.</li>  
        <li>TotalItems - Total number of Items charged. For example, 3.</li>  
        <li>Currency - Shopify store currency. For example, INR.</li>  
        </ul>
      </td>
    </tr>
  </tbody>
</Table>


> 📘 Note
>
> The Charged and Checkout events are received through Shopify Webhooks. Hence, these events will be received at CleverTap only for the users who have logged in.

# Supported User Properties

The following table displays all the user properties supported by the plugin.


| User Property     | Property Description                                                                                                                                                                                             |
| :---------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Name              | The customer's name. For example, Jack.                                                                                                                                                                          |
| Phone             | The customer's mobile number. For example, 97650000.                                                                                                                                                             |
| Email             | The customer's email address. For example, [jack@acme.com](mailto:jack@acme.com).                                                                                                                                |
| Identity          | The customer's  CleverTap ID. For example, 3645910.                                                                                                                                                              |
| Tags              | The list of tags associated with the customer. For example, Gold customer.                                                                                                                                       |
| City              | The customer's city. For example, Mumbai.                                                                                                                                                                        |
| Accepts Marketing | This property returns the value as *true* if the customer accepts marketing. If the customer does not accept then returns the value as *false*.                                                                  |
| Has Account       | This property returns the value as *true* if the email associated with the customer is linked to a customer account. The property returns the value as false if the email is not linked to the customer account. |
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
2. Go to *Settings > Notifications*. 
3. Scroll down to the *Webhooks* section.
4. Click **Create Webhook**. The *Add webhook* window appears.

<Image title="Create Webhook and configure event" alt={435} align="center" border={true} src="https://files.readme.io/06a6309-Shopify_webhook.png" />  Create Webhook











5. Select the [supported event](https://docs.clevertap.com/docs/shopify_webhooks#section-webhook-supported-events) from the list.
6. Enter the CleverTap endpoint URL. For example, [https://api.clevertap.com/shopify/m/<Account-ID>](https://api.clevertap.com/shopify/m/\&ltAccount-ID\&gt)
7. Click Save.

## Webhook Supported Events

The following events are supported via the Shopify webhook:

* Checkout Created
* Checkout Updated
* Checkout Deleted 
* Customer Created
* Customer Updated
* Draft Order Created
* Draft Order Updated
* Fulfillment Created 
* Fulfillment Updated
* Order Cancelled 
* Order Created
* Order Fulfilled
* Charged
* Order Partially Fulfilled
* Order Updated

> 📘 Note
>
> All the above-listed webhook events will only be captured for logged-in users.

> 📘 Checkout and Order events
>
> The Checkout Created, Checkout Updated, Checkout Deleted, Charged, Customer Created, and Customer updated events are available automatically via webhooks for all Shopify plugin installs/reinstalls after 1st October 2021. There is no need to subscribe to these events manually.

# Create Web Campaigns

The CleverTap Shopify plugin provides support for web channels such as [Web Push](doc:web-push) , [Web Pop-up](doc:web-pop-ups) , and [Web Exit Intent](doc:web-exit-intent) without the need for any manual code integration.

To create a Web campaign:

1. From the dashboard, navigate to *Campaigns*.
2. Click **+ Campaign**.
3. Create a [Web Push](doc:web-push) , [Web Pop-up](doc:web-pop-ups) , or [Web Exit Intent](doc:web-exit-intent) campaign to engage your users.

# Migrate from Previous Plugin
The new version of the Shopify plugin was released on June 25, 2021. The previous version of this plugin supports events such as Search, Category Viewed, Product Viewed, Added to Cart, and Charged. This version also provides support for  [Web Pop-up](doc:web-pop-ups) and [Web Exit Intent](doc:web-exit-intent) channels.

If you want to upgrade to the latest version of the plugin, please reach out to your *Customer Success* personnel or raise a support ticket from the dashboard.

# FAQs

### Q. Does my current billing plan include integration with the Shopify plugin?

Yes. This Shopify plugin is available for all CleverTap billing plans.

### Q. I have already installed CleverTap’s Shopify plugin. How can I migrate to the new Shopify Plugin released by CleverTap on June 25, 2021?

Please reach out to your *Customer Success* personnel or raise a support ticket from the dashboard.

### Q. I have a Shopify web store and a mobile app. How do I target users who have performed an event on my Shopify store?

Follow the steps:

1. Select the event (for example, added to cart) in the CleverTap segment builder.
2. Filter by event property CT Source equal to Shopify.

<Image title="Filtering Shopify users from Find People page" alt={1005} align="center" border={true} src="https://files.readme.io/f955291-shopify_segment_identify.png" />  Filtering Shopify Users from Find People Page

### Q. I see a warning "Shopify installation seems to have a few missing files" displayed at the end of the Project page. How do I resolve this warning?

It is recommended to reinstall the plugin by clicking **Reinstall**.

### Q. Will this plugin work for Shopify Plus customers?

Yes. This Plugin works for Shopify Plus customers too.