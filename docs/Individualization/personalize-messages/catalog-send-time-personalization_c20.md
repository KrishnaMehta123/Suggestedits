---
title: Catalog Send-Time Personalization
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
[block:api-header]
{
  "title": "Overview"
}
[/block]
Catalog send-time personalization provides the ability to personalize messages with external data pulled from an uploaded catalog at the time a campaign is sent. Automatically include dynamic information directly in a message such as product price, product category, available inventory levels, and more. 
[block:callout]
{
  "type": "success",
  "title": "E-commerce App Example",
  "body": "A user adds a laptop to the cart, then exits. By providing additional details in the engagement message such as the image, size, latest price, and specifications of the laptop, the user can be nudged to purchase the item. Using catalog send-time personalization helps keep users engaged in a meaningful way."
}
[/block]
After you have uploaded the catalog, you can start using it in a campaign. For more information, refer to [Catalog](https://docs.clevertap.com/docs/catalog).

#Event Property

Follow the steps below to personalize a catalog by event property:

1. Create a [campaign](doc:intro-to-campaigns).

2. Click the **Personalization** link to select a catalog. Once the personalization setup window displays, you can map the required catalog columns to event properties and user properties. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d72233a-Select_Catalog.png",
        "Select Catalog.png",
        2878,
        1164,
        "#e4dee9"
      ],
      "border": true
    }
  ]
}
[/block]
3. Click the **Catalog** tab and select the required catalog from the list. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1266641-Catalog_Personalization.png",
        "Catalog Personalization.png",
        1898,
        1368,
        "#f8f9fb"
      ],
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]
4. Select the event. You can personalize your message based on the property values of this event. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/be98af1-Select_Catalog_Send-Time_Values.png",
        "Select Catalog Send-Time Values.png",
        1894,
        1366,
        "#f7f8fa"
      ],
      "border": true,
      "sizing": "80"
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "Recent Occurrence",
  "body": "The most recent occurrence of the event is used to select the relevant item from the catalog. If the campaign is a triggered campaign, then the event that triggered the campaign is considered."
}
[/block]

5. Select the event property to map to the catalog column. This mapping is important to identify the catalog column that matches the event property. For example, we map *Product Name*, such as a laptop (from the *Viewed* event) to the *Name* column in the catalog. 

Repeat this step to map more properties. 
[block:callout]
{
  "type": "info",
  "title": "Map Multiple Properties",
  "body": "If required, map multiple properties. Every addition to the mapping is treated as an *and* condition. For example, map the name, the color, and the brand to personalize the message for the user."
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fad7eeb-Map_Catalog_Columns.png",
        "Map Catalog Columns.png",
        1896,
        1370,
        "#f8f8fa"
      ],
      "border": true,
      "sizing": "80"
    }
  ]
}
[/block]

6. Click **Save** to set up the personalization. 

7. Use [liquid tags](doc:liquid-tags) to create a personalized message for your target audience. 

In this example, the syntaxes for using different catalog columns are shown below:
[block:code]
{
  "codes": [
    {
      "code": "{{ Catalog.[\"Sample Catalog\"].Name | default: \"Laptop\" }}\n{{ Catalog.[\"Sample Catalog\"].Amount | default: \"0\" }}",
      "language": "liquid",
      "name": "Liquid Tag"
    }
  ]
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3069384-catalog_personalization_liquid_message.png",
        "catalog_personalization_liquid_message.png",
        1173,
        639,
        "#f2f3f6"
      ],
      "border": true
    }
  ]
}
[/block]
You can now use the latest amount for the last added to cart item, such as the laptop. 

#User Property 
Follow the steps below to personalize a catalog by user property:

1.  Create a [campaign](doc:intro-to-campaigns).
2. Click the **Personalization** link to select a catalog. After the personalization setup window displays, you can map the required catalog columns to event properties and user properties. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/98a92e5-Select_Catalog.png",
        "Select Catalog.png",
        2878,
        1164,
        "#e4dee9"
      ],
      "border": true
    }
  ]
}
[/block]
3. Click the **Catalog** tab and select the required catalog from the list. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/18b28fa-Catalog_Personalization.png",
        "Catalog Personalization.png",
        1898,
        1368,
        "#f8f9fb"
      ],
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]
4. Select the user property to map to the catalog column. For example, you can recommend the top restaurant in New York with rich details about the restaurant from the catalog to a user with the user property *City* set as New York. 
[block:callout]
{
  "type": "info",
  "title": "Note",
  "body": "If required, map multiple properties. Every addition to the mapping is treated as an *and* condition. For example, map the city, the top-rated restaurants, and the Chinese restaurants to personalize the message for the user."
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3f75e23-Map_Catalog_Columns_Event_Property.png",
        "Map Catalog Columns_Event Property.png",
        1900,
        1370,
        "#f8f8fa"
      ],
      "border": true,
      "sizing": "80"
    }
  ]
}
[/block]

5. Click **Apply** to set up the personalization. 
6. Use [liquid tags](doc:liquid-tags) to create a personalized message for your target audience. 

In this example, the syntax for using a catalog column is shown below:
[block:code]
{
  "codes": [
    {
      "code": "{{ Catalog.Sample_Catalog.[\"City Restaurants\"] | default:\"New York Top Restaurant\" }}",
      "language": "liquid",
      "name": "Liquid Tag"
    }
  ]
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cc955ed-catalog_personalization_liquid_message_User_property.png",
        "catalog_personalization_liquid_message_User_property.png",
        1081,
        705,
        "#f0f1f4"
      ],
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "Map Multiple Properties",
  "body": "Create personalization by combining catalog send-time personalization with [constant event property](https://docs.clevertap.com/docs/constant-property#section-advanced-constant-property-with-catalog-personalization)."
}
[/block]

#Video Tutorial
For further information, you can watch the following video on catalog send-time personalization:
[block:embed]
{
  "html": "<iframe class=\"embedly-embed\" src=\"//cdn.embedly.com/widgets/media.html?src=https%3A%2F%2Fwww.youtube.com%2Fembed%2FTVltd1_rpG4&display_name=YouTube&url=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3DTVltd1_rpG4&image=http%3A%2F%2Fi.ytimg.com%2Fvi%2FTVltd1_rpG4%2Fhqdefault.jpg&key=f2aa6fc3595946d0afc3d76cbbd25dc3&type=text%2Fhtml&schema=youtube\" width=\"854\" height=\"480\" scrolling=\"no\" title=\"YouTube embed\" frameborder=\"0\" allow=\"autoplay; fullscreen\" allowfullscreen=\"true\"></iframe>",
  "url": "https://www.youtube.com/watch?v=TVltd1_rpG4&list=PLTXk2GzdxAChuuVW4i_H3VwQ9obTRs1L8&index=5",
  "title": "Product Demo: Send-Time Personalization",
  "favicon": "https://www.youtube.com/s/desktop/404f9720/img/favicon.ico",
  "image": "http://i.ytimg.com/vi/TVltd1_rpG4/hqdefault.jpg"
}
[/block]