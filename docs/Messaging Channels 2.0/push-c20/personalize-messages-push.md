---
title: Personalize Message
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
  pages:
    - type: basic
      slug: catalog
      title: Catalogs
    - type: basic
      slug: linked-content
      title: Linked Content
    - type: basic
      slug: liquid-tags
      title: Liquid Tags
    - type: basic
      slug: recommendations
      title: Recommendations
    - type: basic
      slug: bulletins
      title: Bulletins
---
# Overview

You can personalize the message for every user based on specific user property or event property values. For more information on user profile properties and events (dynamic replacements), refer to [User Profiles](https://docs.clevertap.com/docs/user-profiles) and [Events](https://docs.clevertap.com/docs/events#event-properties).

# Inline Personalization 

To invoke the personalization menu, type the *@* or the *{{}} *symbol in the title or the text fields while creating a message.

You can also add dynamic replacements in the title and body. Notice a preview as displayed below.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/281aede-campaign_push_personalization.png",
        "campaign_push_personalization.png",
        1095,
        624,
        "#d9d6e0"
      ],
      "border": true
    }
  ]
}
[/block]
In addition to title, body, you can also personalize many other things such as media URLs, deep links, or button text. An *@ * icon in a box indicates that it can be personalized. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ae0ec11-Personalization_.png",
        "Personalization_@.png",
        748,
        178,
        "#f8f8fa"
      ],
      "border": true
    }
  ]
}
[/block]
#Liquid Tags

Click the ![Personalization](https://files.readme.io/b852e7f-Personalization_setting.png) icon in the editor to open personalization options. 

Liquid tags offer great flexibility while composing personalized messages. Liquid tags allow adding logic using a scripting language, which can be leveraged to change the look and feel of your message. Following is an example to send personalized coupon codes based on the type of membership:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ed642bf-campaigns_liquid_tags_common_example.png",
        "campaigns_liquid_tags_common_example.png",
        1357,
        470,
        "#fafafb"
      ],
      "caption": "",
      "border": true
    }
  ]
}
[/block]
Each notification is personalized to the receiver. 
[block:code]
{
  "codes": [
    {
      "code": "Hello John!\n\nHere is a special coupon for you: Gold4All\n",
      "language": "html",
      "name": "Output - Liquid"
    }
  ]
}
[/block]
For more information on using tags, refer to [Liquid Tags](doc:liquid-tags).


# Linked Content

Linked content provides the ability to personalize emails with rich and contextual data available outside of the CleverTap platform. With linked content, you can send messages with send-time personalization.

For example, you deliver food across different geographies, and you want to personalize offers to each user based on the weather and location. The location can come from CleverTap personalization, and the weather information can come from an API that provides the current weather. If you want to add more information, you can opt for any source such as third-party tools and in-house software to include in your message.
[block:code]
{
  "codes": [
    {
      "code": "Hi {{ Profile.name | default:\"there!\" }},\n\n{% if Linked.cityBasedWeather.temp > 30 %}\nIt is a bright sunny day in {{ Profile.location | default:\"your city\" }}. How about a barbeque today?\n\nUse the coupon code (BARBQ).\nThese are the top 5 restaurants near you:\n{% for restaurant in Linked.RestaurantAPI.restaurants_info limit:5%} \n{{restaurant.name}}  {{restaurant.user_rating.rating_text}}\n{% endfor %}\n\n\n{% elsif Linked.cityBasedWeather.temp < 10 %}\nIt is indeed cold today in {{ Profile.location | default:\"your city\" }}!! \nTime for some hot pizza!\n                                         \nUse the coupon code (PIZZA). These are the top 5 restaurants near you:\n{% for restaurant in Linked.RestaurantAPI.restaurants_info limit:5%} \n{{restaurant.name}}  {{restaurant.user_rating.rating_text}}\n{% endfor %}\n                                          \n{% else %}\n                                          \nIt has  been a while in {{ Profile.location | default:\"your city\" }}. \nOrder something exotic!\n                                          \nUse the coupon code (EXOTIC).These are the top 5 restaurants near you:           {% for restaurant in Linked.RestaurantAPI.restaurants_info limit:5%} \n{{restaurant.name}}  {{restaurant.user_rating.rating_text}}\n{% endfor %}\n                                          \n{% endif %}",
      "language": "liquid"
    }
  ]
}
[/block]
For more information, refer to [Linked Content](https://docs.clevertap.com/docs/linked-content#write-linked-content).

# Recommendations

Click the ![Personlization](https://files.readme.io/b852e7f-Personalization_setting.png) icon in the editor to open personalization options. 

After you have uploaded a catalog, you can display personalized recommendations to your customers. For example, you can have a sliding carousel displayed to your customers based on their personal likes!  For more information on recommendations, see [Recommendations](doc:recommendations).
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6264702-Recommendation_Sample.png",
        "Recommendation_Sample.png",
        1752,
        1184,
        "#f9fafb"
      ],
      "border": true
    }
  ]
}
[/block]
# Catalog 

Click the ![Personlization](https://files.readme.io/b852e7f-Personalization_setting.png) icon in the editor to open personalization options.  Select a catalog from the list. 

A *Catalog* provides the ability to personalize campaigns with dynamic information in messages from product prices to inventory levels. You can create a new product catalog by uploading a file that contains one row for each item in your product catalog. A *Catalog* can be uploaded directly on the CleverTap dashboard via a CSV file that is generated by your inventory management system. For more information on *Catalogs*, see [Catalogs](doc:catalog).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5077276-catalog_sample.png",
        "catalog_sample.png",
        1560,
        786,
        "#f7f8fa"
      ],
      "border": true
    }
  ]
}
[/block]

# Constant event property 

Constant Event Property allows you to engage the user on multiple actions and inactions. For example, person A added to cart a white coat and person B added to cart a pair of blue jeans, but they both did not purchase the items. 

You can either create a campaign for each product that was added to the cart or you can use a *constant event property* to personalize the campaign to each user that did not purchase the item. 

For example, you can map the *prod_name* property of the *charged* event to the *product_name* property of the *added to cart* event. You can then hold this property constant across both events. Based on this property, you can now personalize the message received by each user. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/790bd5c-Constant_property_sample.png",
        "Constant_property_sample.png",
        1374,
        946,
        "#d6d4d9"
      ],
      "border": true
    }
  ]
}
[/block]
 For more information on using a constant event property, see [Constant Event Property](doc:constant-property).