---
title: Cart Abandonment Use Case
excerpt: Learn how CleverTap achieves the Cart Abandonment Use Case.
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

Cart personalization allows businesses to send dynamic cart abandonment emails displaying all the products users have left in their cart without making a purchase. Events such as _Add to Cart_ store the most recent product added to the cart. This limitation prevents a real-time view of all the products in the cart, making it difficult to run campaigns that fully reflect the user’s cart activity.

CleverTap uses a combination of User Properties and Catalog Personalization to achieve the card abandonment use case:

- User Properties: Stores variant IDs in an array format when users add items to their cart. These properties update dynamically when items are added or removed during checkout.
- Catalogs: These contain additional product details, such as product name, image URL, and price, and are synced in the CleverTap dashboard using the Shopify Catalog Sync feature. 

This approach enables businesses to create dynamic campaigns that accurately reflect the state of the user’s cart. By combining user properties with catalogs and advanced personalization techniques like liquid tags, CleverTap enhances the effectiveness of cart abandonment campaigns, delivering an effortless shopping experience.

> 📘 Note
> 
> Cart Personalization works only if the _Added to Cart, Charged_, and _Removed from Cart_ events are sourced through the CleverTap Shopify plugin. Custom implementations of these events are not supported.

# Live Action Email Campaign

Learn how to create personalized cart abandonment emails using CleverTap's Live Action Email campaigns. 

### Scenario

A user visits an e-commerce store and adds multiple items to their shopping cart. However, the user leaves the website without making a purchase.

### Objective

Using Cart Personalization, you can:

- Encourage users to complete their purchases by sending tailored, timely reminders via Email.
- Recover potential lost revenue.
- Provide a personalized and seamless shopping experience for the users.

### Steps to Implement Cart Abandonment Campaigns

To set up an Email campaign, follow these steps on the CleverTap Dashboard:

1. **Toggle the _Catalog Sync_ feature:**

Toggle the _ [Catalog Sync](doc:shopify#catalog-sync)_ feature to automatically sync product data between customers' Shopify and CleverTap accounts. 

2. **Toggle the _Cart Tracking_ feature:**  
   This feature ensures that the variant IDs from the users' cart are stored in their CleverTap profile. For example, when a user adds a product to their cart, the variant ID will be saved as a user property in an array format in the user's profile, under the _shopify_cart_ids_. Similarly, when a user removes a product from the cart, the variant ID will be removed automatically. To enable Cart Tracking in your dashboard:
   1. Go to the Shopify Integration page within CleverTap.
   2. Toggle on the _Cart Tracking_ feature.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/68c76d7e1236082829a728af587a5f4e367305a9feb24bf30af844a862ea6e8f-Cart_Tracking.png",
        "",
        "Cart Sync Toggle"
      ],
      "align": "center",
      "border": true,
      "caption": "Cart Sync Toggle"
    }
  ]
}
[/block]


3. **Create the Campaign:**

Define the campaign as an inaction campaign targeting users who added products to the cart but did not complete a checkout action within 15 minutes.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/adf624ca6ddb47cb4b9e46c437ecfff5dafd548a710f3c2aa9bb60e51ac05c08-Screenshot_2024-12-05_at_11.27.46_AM.png",
        null,
        "Inaction Campaign"
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Inaction Campaign"
    }
  ]
}
[/block]


For more information, refer to [Create an Email Campaign](doc:create-message-email).

4. **Mapping the campaign with Catalog:**
   1. Go to _What_ section of the campaign editor and click on _Personalization_. 
   2. From the _Catalog_ tab, select _shopify-catalog_.
   3. Select the _shopify_cart_ids_ user property and map it to the _Identity_ column in the catalog. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ec0aefb4bb66864d8dbcdc65e7631e30176716400cb2ba588cbdcba56a8f8b8d-2025-02-17_19-02-10.png",
        null,
        "Mapping the Catalog"
      ],
      "align": "center",
      "border": true,
      "caption": "Mapping the Catalog"
    }
  ]
}
[/block]


5. **Set Up _Personalization_ with Liquid Tags:**
   1. In the _What_ section of the email body editor, drag a _Text_ field into the email body.
   2. Click on **More** and select the _Customize with Liquid tags_ option. 
   3. Use Liquid Tags to dynamically fetch the  product details (name, image, price, etc.) from the catalog's CSV file.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/17734120560e5e20a2df3dfd1126e1d61124115cdf586a37fd88937874a783a0-Image_4.jpeg",
        null,
        "Liquid Tags"
      ],
      "align": "center",
      "border": true,
      "caption": "Liquid Tags"
    }
  ]
}
[/block]


For example, you can use HTML tags to create a table and `For loop` in Liquid tags to traverse the Catalog. The `For loop` will run until it covers all the Variant IDs in the Profile property.

```text
<inline-editor>
  {% for item in Catalog.Samplecatalog1 %}
  <table border='1' style='border-collapse:collapse'>
    <tr>
      <td>
        <img src="{{ item.ImageURL | default: 'No Image' }}" width="100" height="100">
      </td>
      <td width="100" height="100">
        {{ item.Identity }}
      </td>
      <td width="100" height="100">
        {{ item.Name }}
      </td>
    </tr>
  </table>
  {% endfor %}
</inline-editor>
```

> ℹ️ Key Considerations
> 
> If a user empties the cart without performing the Charged event, the `For loop` in the liquid tags will not run. Consequently, the Email will be delivered without product data, as the user remains eligible for the campaign despite having no variant IDs. Therefore, ensure that the email templates are designed to handle scenarios where the product table does not render, maintaining a professional appearance.

6. **Apply Frequency Caps:**

To prevent multiple emails on every _Add to Cart_ event trigger for a single user, apply a frequency cap within the campaign to send only one email per cart addition.

7. **Test the Email to ensure correctness:**

You can test the campaign to ensure personalized rendering of product details from the products left in your cart.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0f42d963a2e2370541c1d499465a3e1afae88f8176d11faa7f961bb7ed5a875e-Image_5.jpeg",
        null,
        "Final look of the Email"
      ],
      "align": "center",
      "border": true,
      "caption": "Final View of the Email"
    }
  ]
}
[/block]


CleverTap's cart abandonment campaigns allow businesses to recover revenue by re-engaging users with personalized messages, thus driving conversions.