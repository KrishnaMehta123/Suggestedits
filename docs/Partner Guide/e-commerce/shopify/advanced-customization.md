---
title: Advanced Customization
excerpt: Learn how to configure Shopify based on your customizations.
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

After your store is connected and installed, you can start customizing it per your requirements. You can configure the web push for your store and also customize the event data received from your Shopify store. 

### Configure Web Push

You can send personalized communication to your users through Web Push notifications. However, you must enable them first from the CleverTap dashboard.

Check that Web Push is configured for your store. If not configured, you must [configure the Web Push](https://docs.clevertap.com/docs/setup-web-push)  from the CleverTap dashboard.

After the Web Push is configured, enable the notification prompts. Click *Web Push configuration*  and toggle ON  *Send notification permission prompt*  to enable CleverTap Web Push notifications. 

<Image alt="Enable Web Push" align="center" border={true} src="https://files.readme.io/9d626e3078a7692ac7755413755ece1ce16380975b1b2b1d5145e3188b5632e8-web_push_enable.png">
  Enable Web Push
</Image>

### Customize Event Data

Event data customization includes event and profile data. You can choose to receive only the required data and opt out of receiving any data that is not required. 

#### Profile Properties

CleverTap allows you to select only the required Profile properties. To select the Profile properties, follow the steps listed below: 

1. Go to  *Settings* >  *Project* > *Shopify* > *Data Tracking Setup*.
2. Click *Edit*. 
3. Click the *Profile properties* list and select the required properties. 
4. Click **Apply**. 

<Image alt="Select the required Profile Properties" align="center" border={true} src="https://files.readme.io/67242cdeb24892b8fb2b69838cc5b5c148a4ab9aa7fd26fdc211882b542786bc-profile_properties.png">
  Select the required Profile Properties
</Image>

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

CleverTap receives events from the following three sources:

* *Shopify Webhook* :  After you integrate your store, CleverTap subscribes to the selected Webhook events for your Shopify store.
* *Web SDK* :These are the [supported events](https://docs.clevertap.com/docs/shopify-copy#web-push-configuration) that CleverTap Web SDK captures from your Shopify store.
* *App Pixel*: Shopify allows listening to several events via the App Pixel API, which provides rich insights about customer behavior and their current journey stage. The CleverTap dashboard provides an option to select which App Pixel events you want to capture. You can view the complete list of [supported events,](https://shopify.dev/docs/api/web-pixels-api/standard-events) configure them to track checkout, and other custom pixel events. Once selected, CleverTap will only listen to those specific events.

You can also select to  *Receive custom pixel events* or opt-out.

<Image alt="Events Data" align="center" border={true} src="https://files.readme.io/050b59e363ad81e09ba73edd927050f2a77ca1c66dbfdd62aa0a20e9e874f39a-image.png">
  Events Data
</Image>

##### Web SDK Supported Events

The following table displays all the events supported by the CleverTap Web SDK:

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
>
> Ensure that events are not duplicated across Webhook, SDK, and App Pixel sources.

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

> 📘 Note
>
> All the above-listed Webhook events will only be captured for logged-in users.

### Catalog Sync

The *Catalog Sync* feature simplifies catalog management by automating product data sync between customers' Shopify and CleverTap accounts. This integration ensures up-to-date catalogs are readily available for personalization across marketing channels like Email and WhatsApp, eliminating manual uploads.

<Image alt="Catalog Sync Feature for Shopify" align="center" border={true} src="https://files.readme.io/47e858de0bce4b3c99fb39d0a84152434009a1b212a925f01011c255a0f8f980-catalog_sync.png">
  Catalog Sync Feature for Shopify
</Image>

> ℹ️ Note
>
> This synchronization runs daily at 8:00 AM IST, syncing the latest product catalog data between Shopify and CleverTap.

To enable Catalog Sync in your dashboard:

1. Go to the Shopify Integration page within CleverTap.
2. Toggle on the *Catalog Sync* feature.
