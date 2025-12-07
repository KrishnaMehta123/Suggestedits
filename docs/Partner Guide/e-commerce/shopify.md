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

CleverTap plugin provides an easy way to integrate your Shopify stores within minutes without any code. All you need is a CleverTap account and you can have a seamless flow of events and user data from your Shopify store. You can also send personalized messages to your users through channels such as [Web Push](doc:web-push) notifications, [Web Pop-up](doc:web-pop-ups), [Web Exit Intent](doc:web-exit-intent), and [Web Native Display](https://docs.clevertap.com/docs/web-native-display). 

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
              style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>`}</HTMLBlock>


<br />

# Integrate Shopify

You can install the [CleverTap App](https://apps.shopify.com/clevertapapp) from the [Shopify App Store](https://help.shopify.com/en/manual/apps/installing-apps).  Login to the CleverTap dashboard and follow the steps to complete the integration:

Follow the steps to locate the Shopify plugin on the CleverTap dashboard:

1. Login to your CleverTap account. 
2. Open *Settings* >  *Project* > *Shopify*.

<Image alt="Locate the Shopify Plugin" align="center" border={true} src="https://files.readme.io/0c97c60-Shopify_start_screen.jpg" />  Locate the Shopify Plugin











3. The *Shopify* window displays. Click **Integrate Store** button to start the integration. 

The integration includes the following steps:
1. [Install and Connect App](https://docs.clevertap.com/docs/shopify#install-and-connect-app)
2. [Advanced Customization ](https://docs.clevertap.com/docs/shopify#advanced-customization)
   * [Configure Web Push](https://docs.clevertap.com/docs/shopify#configure-web-push) 
   * [Customize Profile Properties](https://docs.clevertap.com/docs/shopify#profile-properties)
   * [Customize Events](https://docs.clevertap.com/docs/shopify#events)
3. [Enable App Embed](https://docs.clevertap.com/docs/shopify#enable-app-embed)

## Install and Connect App

If you have already installed the app from the Shopify App Store,  *App Installed* is displayed next to your store name. However, if you are installing the app for the first time, you can install it from the Shopify dashboard.

Follow the steps below to install the CleverTap app:

1. Click the *Install CleverTap on Shopify dashboard* link. 

<Image alt="Install from CleverTap " align="center" width="60% " border={true} src="https://files.readme.io/5cf4728-Shopify_click_link.jpg" />  Install from CleverTap 











2. The link opens the *Shopify App Store*  page. Check that you are logged in to the store and click **Install**.

<Image alt="Install CleverTap App from Shopify Store" align="center" border={true} src="https://files.readme.io/0f34d65-Shopify_app_store_install.jpg" />  Install CleverTap App











3. You can now connect your store from the CleverTap dashboard and click **Continue**. 

<Image title="Quick Integration" alt="Enter Shopify Store Name" align="center" width="50% " border={true} src="https://files.readme.io/81362ad-Shopify_store_name.jpg" />  Enter Shopify Store Name











4. Enter your credentials if you are not logged in to your Shopify store and continue the process.

Your store is now connected to your CleverTap account. 

## Advanced Customization

After your store is connected and installed, you can start customizing it per your requirements. You can configure the web push for your store and also customize the event data received from your Shopify store. 

### Configure Web Push

You can send personalized communication to your users through Web Push notifications. However, you must enable them first from the CleverTap dashboard.

Check that Web Push is configured for your store. If not configured, you must  [configure the Web Push](https://docs.clevertap.com/docs/setup-web-push)  from the CleverTap dashboard.
After the Web Push is configured, enable the notification prompts. Click *Web Push configuration* and toggle ON *Send notification permission prompt* to enable CleverTap Web Push notifications.

<Image alt="Integrate with Web Push" align="center" width="50%" border={true} src="https://files.readme.io/b28da80-Shopify_enable_web_pus.jpg" /> Enable Web Push

### Customize Event Data

Event data customization includes event and profile data. You can choose to receive only the required data and opt out of receiving any data that is not required.

#### Profile Properties

CleverTap allows you to select only the required Profile properties. To select the Profile properties, follow the steps listed below:

1. Go to *Settings* > *Project* > *Shopify* > Advanced Customization > Event Data Customization.
2. Click *Edit*.
3. Click the *Profile properties* list and select the required properties.
4. Click **Apply**.

<Image alt="Select required profile properties" align="center" width="70%" border={true} src="https://files.readme.io/a7ef3be-Shopify_profile_properties.jpg" /> Select the Required Profile Properties

The following table displays all the user properties supported by the Shopify plugin:
| User Property           | Property Description                                                                                                                                                                                             |
| :---------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Email                   | The customer's email address. For example, [jack@acme.com](mailto:jack@acme.com).                                                                                                                                |
| Phone                   | The customer's mobile number. For example, 97650000.                                                                                                                                                             |
| Tags                    | The list of tags associated with the customer. For example, Gold customer.                                                                                                                                       |
| City                    | The customer's city. For example, Mumbai.                                                                                                                                                                        |
| Orders Count            | The total number of orders from a customer.                                                                                                                                                                      |
| Total Spent             | Total amount spent on all orders. For example, 5400.                                                                                                                                                             |
| Shopify ID              | The Shopify ID of the customer.  For example, 29873645910.                                                                                                                                                       |
| First Name              | The customer's first name.                                                                                                                                                                                       |
| LastName                | The customer's first name.                                                                                                                                                                                       |
| Last Order ID           | The order ID of the last order placed by the customer.                                                                                                                                                           |
| Has Account             | This property returns the value as *true* if the email associated with the customer is linked to a customer account. The property returns the value as false if the email is not linked to the customer account. |
| Tax Exempt              | Whether or not the customer is exempt from taxes.                                                                                                                                                                |
| Email Marketing Consent | Records the consent status of the customer for receiving marketing communication through Email.                                                                                                                  |
| SMS Marketing Consent   | Records the consent status of the customer for receiving marketing communication through SMS.                                                                                                                    |
| Note                    | A note left by the customer to the merchant, either in their cart or during checkout.                                                                                                                            |
| Currency                | The currency of purchase.                                                                                                                                                                                        |


#### Events

CleverTap receives events from the following two sources:

* *Shopify Webhook* :  After you integrate your store, CleverTap subscribes to the selected Webhook events for your Shopify store.
* *Web SDK* :These are the [supported events](https://docs.clevertap.com/docs/shopify-copy#web-push-configuration) that CleverTap Web SDK captures from your Shopify store.

Select the events you want to receive from the Shopify Webhook and the Web SDK.

<Image alt="Receive Events from SDK" align="center" width="50%" border={true} src="https://files.readme.io/be06cd1-Shopify_receive_events.jpg" /> Receive Events from CleverTap SDK and Shopify Webhook

You can also select to *Receive data for Charged* event or opt-out. Select either of the following events that you want CleverTap to record as a *Charged* event:

* **Order Paid** : This event is passed to CleverTap by the Shopify webhook when an order is paid.
* **Order Created** : This event is passed to CleverTap by the Shopify webhook when an order is created.

##### Web SDK Supported Events

The following table displays all the events supported by the CleverTap Web SDK:
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
        <ul> <li>Page - The store page. For example, Index page.</li> <li>Title - Title of the page. For example, Acme home.</li> <li>URL - URL of the page. For example, <a href="https://mystore.myshopify.com/">https\://mystore.myshopify.com/</a>.</li> </ul>
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
        <ul> <li>Available - Availability of the product. For example, TRUE.</li> <li>Currency - Shopify store currency. For example, INR. </li> <li>Handle - Product Handle. For example, nike-sneakers-shoe.</li> <li>ID - Product ID. For example, 6744256675993.</li> <li>Price - Product Price. For example, 2999.</li> <li>Title - Product Title. For example, Nike Sneakers Shoe. </li> <li>TotalVariants - Number of variants available. For example, 3.</li> <li>URL - URL of the product page. For example, /products/nike-sneakers-shoe.</li> </ul>
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
        <ul> <li>Currency - Shopify store currency.</li> <li>Term - Search terms used. For example, red shoe.</li> <li>TotalItems - Number of items in search results. For example, 1.</li> </ul>
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
        <ul> <li>Currency - Shopify store currency. For example, INR.</li> <li>Image - URL of the product image. For example, <a href="https://cdn.shopify.com/s/files/products/RedT-shirt.jpg">https\://cdn.shopify.com/s/files/products/RedT-shirt.jpg</a>.</li> <li>Price - Product Price. For example, 2999.</li> <li>ProductId - Product ID. For example, 6744249139353.</li> <li>ProductType - Type of the product. For example, T-shirts.</li> <li>Quantity - Product Quantity. For example, 1.</li> <li>Title - Product Title. For example, Red T-shirt.</li> <li>URL - Product URL. For example, /products/red-t-shirt-1?variant=39972529471641.</li> <li>VariantId - Variant ID. For example, 39972529471641.</li> <li>VariantTitle - Variant Title. For example, Nike Sneakers Shoe.</li> <li>Vendor - Vendor name. For example, Acme stores.</li> </ul>
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
        <ul> <li>Currency - Shopify store currency. For example, INR.</li> <li>Image - URL of the product image. For example, <a href="https://cdn.shopify.com/s/files/products/RedT-shirt.jpg">https\://cdn.shopify.com/s/files/products/RedT-shirt.jpg</a>.</li> <li>Price - Product Price. For example, 2999.</li> <li>ProductId - Product ID. For example, 6744249139353.</li> <li>ProductType - Type of the product. For example, T-shirts.</li> <li>Quantity - Product Quantity. For example, 1.</li> <li>Title - Product Title. For example, Red T-shirt.</li> <li>URL - Product URL. For example, /products/red-t-shirt-1?variant=39972529471641.</li> <li>VariantId - Variant ID. For example, 39972529471641.</li> <li>VariantTitle - Variant Title. For example, Nike Sneakers Shoe.</li> <li>Vendor - Vendor name. For example, Acme stores.</li> </ul>
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
        <ul> <li>Email - Customer's email address. For example, [jack@acme.com.](mailto:jack@acme.com.)</li> <li>Name - Customer's name. For example, John Doe </li> <li>FirstName - Customer's first name. For example, John. </li> <li>LastName - Customer's last name. For example, Doe.</li> <li>ID - Customer ID. For example, 5204453556377.</li> </ul>
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
        <ul> <li>Email - Customer's email address. For example, [jack@acme.com.](mailto:jack@acme.com.)</li> <li>Name - Customer's name. For example, John Doe </li> <li>FirstName - Customer's first name. For example, John. </li> <li>LastName - Customer's last name. For example, Doe.</li> <li>ID - Customer ID. For example, 5204453556377.</li> </ul>
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
  </tbody>
</Table>


> 📘 Note
>
> The Charged and Checkout events are received through Shopify Webhooks. Therefore, these events are be received at CleverTap only for the users who have logged in.

##### Webhook Supported Events

The following events are supported via the Shopify Webhook:


<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Sr. No
      </th>

      <th>
        Events
      </th>

      <th>
        Event Properties
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        1
      </td>

      <td>
        **Customer Created**  

        **Customer Update**
      </td>

      <td>
        <table><tr><th>Event Properties </th><th>Event Properties</th></tr><tr><td>customer-id</td><td>customer email</td></tr><tr><td>customer accepts marketing</td><td>customer created at</td></tr><tr><td>customer updated at</td><td>customer first name</td></tr><tr><td>customer last name</td><td>orders count</td></tr><tr><td>total spent</td><td>customer phone</td></tr><tr><td>TAGS</td><td></td></tr></table>
      </td>
    </tr>

    <tr>
      <td>
        2
      </td>

      <td>
        **Checkout Create**  

        **Checkout Updated**  

        * \*Checkout Deleted\
          \*\*\
          **Draft Order Created**\
            

        **Draft Order Updated**
      </td>

      <td>
        <table><tr><th>Event Properties</th><th>Event Properties</th></tr><tr><td>email</td><td>buyer accepts marketing</td></tr><tr><td>Created At</td><td>Updated At</td></tr><tr><td>user id</td><td>location id</td></tr><tr><td>device id</td><td>phone</td></tr><tr><td>customer locale</td><td>name</td></tr><tr><td>source</td><td>abandoned checkout url</td></tr><tr><td>source name</td><td>total price</td></tr><tr><td>subtotal price</td><td>Currency</td></tr><tr><td>gateway</td><td>billing address zip</td></tr><tr><td>billing address province</td><td>billing address country</td></tr><tr><td>billing address city</td><td>billing address province code</td></tr><tr><td>billing address country code</td><td>ship address zip</td></tr><tr><td>ship address province</td><td>ship address country</td></tr><tr><td>ship address city</td><td>ship address province code</td></tr><tr><td>ship address country code</td><td>default address zip</td></tr><tr><td>default address province</td><td>default address country</td></tr><tr><td>default address city</td><td>default address province code</td></tr><tr><td>default address country code</td><td>TAGS</td></tr><tr><td>customer-id</td><td>customer email</td></tr><tr><td>customer accepts marketing</td><td>customer created at</td></tr><tr><td>customer updated at</td><td>customer first name</td></tr><tr><td>customer last name</td><td>orders count</td></tr><tr><td>total spent</td><td>customer phone</td></tr></table>
      </td>
    </tr>

    <tr>
      <td>
        3
      </td>

      <td>
        **Fulfillment Created**  

        **Fulfillment Updated**
      </td>

      <td>
        <table><tr><th>Event Properties</th><th>Event Properties</th></tr><tr><td>id</td><td>destinationfirstname</td></tr><tr><td>orderid</td><td>destinationlastname</td></tr><tr><td>status</td><td>destinationaddress1</td></tr><tr><td>CreatedAt</td><td>destinationphone</td></tr><tr><td>UpdatedAt</td><td>destinationcity</td></tr><tr><td>email</td><td>destinationzip</td></tr><tr><td>service</td><td>destinationprovince</td></tr><tr><td>trackingcompany</td><td>destinationcountry</td></tr><tr><td>shipmentstatus</td><td>destinationaddress2</td></tr><tr><td>locationid</td><td>destinationcompany</td></tr><tr><td>trackingnumber</td><td>destinationlatitude</td></tr><tr><td>trackingurl</td><td>destinationlongitude</td></tr><tr><td>name</td><td>destinationname</td></tr><tr><td>destinationcountrycode</td><td>destinationprovincecode</td></tr></table>
      </td>
    </tr>

    <tr>
      <td>
        4
      </td>

      <td>
        **Order Created**  

        **Order Updated**  

        **Order Cancelled**  

        **Order Fulfilled**  

        **Order Partially Fulfilled**
      </td>

      <td>
        <table><tr><th>Event Properties</th><th>Event Properties</th></tr><tr><td>number</td><td>number</td></tr><tr><td>closed at</td><td>token</td></tr><tr><td>gateway</td><td>test</td></tr><tr><td>total weight</td><td>total tax</td></tr><tr><td>taxes included</td><td>financial status</td></tr><tr><td>confirmed</td><td>total discounts</td></tr><tr><td>total line items price</td><td>cart token</td></tr><tr><td>buyer accepts marketing</td><td>name</td></tr><tr><td>referring site</td><td>landing site</td></tr><tr><td>cancelled at</td><td>cancel reason</td></tr><tr><td>total price usd</td><td>checkout token</td></tr><tr><td>reference</td><td>source identifier</td></tr><tr><td>source url</td><td>processed at</td></tr><tr><td>device id</td><td>app id</td></tr><tr><td>browser ip</td><td>landing site ref</td></tr><tr><td>order number</td><td>processing method</td></tr><tr><td>checkout id</td><td>source name</td></tr><tr><td>fulfillment status</td><td>contact email</td></tr><tr><td>order status url</td><td>presentment currency</td></tr><tr><td>total line items amount</td><td>total line items currency</td></tr><tr><td>total discount amount</td><td>total discount currency</td></tr><tr><td>total shipping amount</td><td>total shipping currency</td></tr><tr><td>Total Price amount</td><td>Total Price currency</td></tr><tr><td>Total Tax amount</td><td>Total Tax currency</td></tr><tr><td>email</td><td>buyer accepts marketing</td></tr><tr><td>Created At</td><td>Updated At</td></tr><tr><td>user id</td><td>location id</td></tr><tr><td>device id</td><td>phone</td></tr><tr><td>customer locale</td><td>name</td></tr><tr><td>source</td><td>abandoned checkout url</td></tr><tr><td>source name</td><td>total price</td></tr><tr><td>subtotal price</td><td>Currency</td></tr><tr><td>gateway</td><td>billing address zip</td></tr><tr><td>billing address province</td><td>billing address country</td></tr><tr><td>billing address city</td><td>billing address province code</td></tr><tr><td>billing address country code</td><td>ship address zip</td></tr><tr><td>ship address province</td><td>ship address country</td></tr><tr><td>ship address city</td><td>ship address province code</td></tr><tr><td>ship address country code</td><td>default address zip</td></tr><tr><td>default address province</td><td>default address country</td></tr><tr><td>default address city</td><td>default address province code</td></tr><tr><td>default address country code</td><td>TAGS</td></tr><tr><td>customer-id</td><td>customer email</td></tr><tr><td>customer accepts marketing</td><td>customer created at</td></tr><tr><td>customer updated at</td><td>customer first name</td></tr><tr><td>customer last name</td><td>orders count</td></tr><tr><td>total spent</td><td>customer phone</td></tr></table>
      </td>
    </tr>

    <tr>
      <td>
        5
      </td>

      <td>
        **Order Paid**
      </td>

      <td>
        <table><tr><th>Event Properties</th><th>Event Properties</th></tr><tr><td>Amount</td><td>Currency</td></tr><tr><td>email</td><td>Ship_country</td></tr><tr><td>Ship_region</td><td>Ship_city</td></tr><tr><td>Items (Will be part of event prop if ORDERS_PAID is selected as charged)</td><td>Checkout ID</td></tr><tr><td>Charged ID</td><td>number</td></tr><tr><td>closed at</td><td>token</td></tr><tr><td>gateway</td><td>test</td></tr><tr><td>total weight</td><td>total tax</td></tr><tr><td>taxes included</td><td>financial status</td></tr><tr><td>confirmed</td><td>total discounts</td></tr><tr><td>total line items price</td><td>cart token</td></tr><tr><td>buyer accepts marketing</td><td>name</td></tr><tr><td>referring site</td><td>landing site</td></tr><tr><td>cancelled at</td><td>cancel reason</td></tr><tr><td>total price usd</td><td>checkout token</td></tr><tr><td>reference</td><td>source identifier</td></tr><tr><td>source url</td><td>processed at</td></tr><tr><td>device id</td><td>app id</td></tr><tr><td>browser ip</td><td>landing site ref</td></tr><tr><td>order number</td><td>processing method</td></tr><tr><td>checkout id</td><td>source name</td></tr><tr><td>fulfillment status</td><td>contact email</td></tr><tr><td>order status url</td><td>presentment currency</td></tr><tr><td>total line items amount</td><td>total line items currency</td></tr><tr><td>total discount amount</td><td>total discount currency</td></tr><tr><td>total shipping amount</td><td>total shipping currency</td></tr><tr><td>Total Price amount</td><td>Total Price currency</td></tr><tr><td>Total Tax amount</td><td>Total Tax currency</td></tr><tr><td>email</td><td>buyer accepts marketing</td></tr><tr><td>Created At</td><td>Updated At</td></tr><tr><td>user id</td><td>location id</td></tr><tr><td>device id</td><td>phone</td></tr><tr><td>customer locale</td><td>name</td></tr><tr><td>source</td><td>abandoned checkout url</td></tr><tr><td>source name</td><td>total price</td></tr><tr><td>subtotal price</td><td>Currency</td></tr><tr><td>gateway</td><td>billing address zip</td></tr><tr><td>billing address province</td><td>billing address country</td></tr><tr><td>billing address city</td><td>billing address province code</td></tr><tr><td>billing address country code</td><td>ship address zip</td></tr><tr><td>ship address province</td><td>ship address country</td></tr><tr><td>ship address city</td><td>ship address province code</td></tr><tr><td>ship address country code</td><td>default address zip</td></tr><tr><td>default address province</td><td>default address country</td></tr><tr><td>default address city</td><td>default address province code</td></tr><tr><td>default address country code</td><td>TAGS</td></tr><tr><td>customer-id</td><td>customer email</td></tr><tr><td>customer accepts marketing</td><td>customer created at</td></tr><tr><td>customer updated at</td><td>customer first name</td></tr><tr><td>customer last name</td><td>orders count</td></tr><tr><td>total spent</td><td>customer phone</td></tr></table>
      </td>
    </tr>
  </tbody>
</Table>


<br />

> 📘 Note
>
> All the above-listed Webhook events will only be captured for logged-in users.

### Catalog Sync

The Shopify Catalog Sync feature simplifies product catalog management by automating the process of syncing product data between Shopify and CleverTap. 

With the introduction of the Catalog Sync Automation option in the Advanced Customization section of the Shopify Integration page, users can now enable automated catalog updates. This integration ensures up-to-date catalogs are readily available for seamless personalization across marketing channels like email and SMS.

> ℹ️
>
> This synchronization runs daily at 8:00 AM, pulling the latest product data from Shopify and updating it on the CleverTap Cloud dashboard.

<Image alt="Catalog Sync Feature for Shopify" align="center" border={true} src="https://files.readme.io/ae483bc6e383a109bd3bdac8268039910b12796d4215290ce302ef24d9509685-image.png" />  Catalog Sync Feature for Shopify











To enable Catalog Sync in your dashboard:

1. Navigate to the Shopify Integration page within CleverTap.
2. Access the Advanced Customization section.
3. Toggle on the Product Catalog Sync feature.
4. Once enabled, the system automatically syncs product details daily, ensuring the catalog remains current and eliminating the need for manual uploads.

<br />

## Enable App Embed Status

The *App Embed* status displays as *Enabled* if enabled already. 

The *App Embed* status informs you if it is active. By default, app embed blocks are deactivated after an app is installed. However, if the *App Embed* status is *Disabled* , merchants must activate app embed blocks in the theme editor, from their Shopify theme settings. Refer to this detailed document on [App embeds](https://shopify.dev/apps/online-store/theme-app-extensions/extensions-framework#app-embed-blocks) to learn more.

To enable *CleverTap-Shopify App Embed* on your Shopify store:

1. Navigate to your Shopify store's theme settings page using the following URL:\
   https://&lt;Your-Shopify-store-name&gt;.myshopify.com/admin/themes/current/editor?context=apps&activateAppId=2566991a-cd89-49d8-997d-74717582b9ed/app-embed.
2. Toggle ON the *Clevertap-Shopify* App embed and click  **Save** at the top right corner.

<Image title="Navigate to your Shopify store and toggle ON the CleverTap-Shopify option" alt={2846} align="center" border={true} src="https://files.readme.io/22c77b8-CT_shopify_app_embed.png" />  Toggle ON CleverTap-Shopify
To check if the *CleverTap-Shopify* App embed is enabled:

1. Navigate to your Shopify store,  right-click and, select *Inspect*. 
2. Navigate to *Sources* tab and select *Page*. 
3. Search for the *clevertap-shopify.js* file in the *extensions* folder under *cdn.Shopify.com*. Refer to the following image:

<Image title="Verifying if CleverTap-Shopify app embed is enabled" alt={2262} align="center" border={true} src="https://files.readme.io/4f64635-shopify_app_ambed.png" /> Verify if CleverTap-Shopify App Embed is Enabled

# Create Web Campaigns

The CleverTap Shopify plugin provides support for web channels such as [Web Push](doc:web-push) , [Web Pop-up](doc:web-pop-ups) , and [Web Exit Intent](doc:web-exit-intent) without the need for any manual code integration.

To create a Web campaign:

1. From the dashboard, navigate to *Campaigns*.
2. Click **+ Campaign**.
3. Create a [Web Push](doc:web-push) , [Web Pop-up](doc:web-pop-ups) , or [Web Exit Intent](doc:web-exit-intent) campaign to engage your users.

# FAQs

### Q. Does my current billing plan include integration with the Shopify plugin?

Yes. This Shopify plugin is available for all CleverTap billing plans.

### Q. I have a Shopify web store and a mobile app. How do I target users who have performed an event on my Shopify store?

To target the users who have performed the event on your store:

1. Select the event (for example, added to cart) in the CleverTap segment builder.
2. Filter by event property *CT Source* equal to *Shopify*.

<Image title="Filtering Shopify users from Find People page" alt={1005} align="center" border={true} src="https://files.readme.io/f955291-shopify_segment_identify.png" /> Filtering Shopify Users from Find People Page

### Q. I see a warning *Shopify installation seems to have a few missing files* displayed at the end of the Project page. How do I resolve this warning?

CleverTap recommends reinstalling the plugin by clicking **Reinstall**.

### Q. Will this plugin work for Shopify Plus customers?

Yes. This Plugin works for Shopify Plus customers too.