---
title: Personalize (WIP)
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
# Overview

You can personalize the Web Push title and message body for every user based on specific user property or event property values. For more information on user profile properties and events (dynamic replacements), refer to [User Profiles](https://docs.clevertap.com/docs/user-profiles) and [Events](doc:events).

# Personalization

To invoke the personalization menu, type the @ symbol in the title or the text fields while creating the Web Push message.

You can also add dynamic replacements in the title and body to send personalized Web Push notifications. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/90233f0-WEB_PUSH_PER.png",
        "WEB PUSH PER.png",
        1578,
        948,
        "#eeebf6"
      ],
      "border": true
    }
  ]
}
[/block]

In addition to the title and the message body, you can personalize media URLs, deep links, and button URLs. An **@** icon in a box indicates that it can be personalized.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/41fe3ef-p1.png",
        "p1.png",
        1502,
        1132,
        "#000000"
      ]
    }
  ]
}
[/block]
#Liquid Tags

Click the ![Personalization](https://files.readme.io/b852e7f-Personalization_setting.png) icon in the editor to open personalization options.

Liquid tags offer great flexibility while composing personalized messages. They allow adding logic using a scripting language, which can be leveraged to change the look and feel of your message. Following is an example of sending personalized coupon codes for customers belonging to a particular city:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/03628fb-Liquid_Tags.png",
        "Liquid Tags.png",
        1134,
        752,
        "#000000"
      ],
      "caption": "",
      "border": true
    }
  ]
}
[/block]
Each notification is personalized to the receiver as shown in the following example. 
[block:code]
{
  "codes": [
    {
      "code": "Hi John!\n\nHere's a special code for you - MUM50\n",
      "language": "html",
      "name": "Output - Liquid"
    }
  ]
}
[/block]
For more information on using tags, refer to [Liquid Tags](doc:liquid-tags).


# Linked Content

Linked content allows personalizing your Web Push messages with rich and contextual data available outside of the CleverTap platform. With linked content, you can send messages with send-time personalization.

For example, you deliver food across different geographies, and you want to personalize offers to each user based on the weather and location. The location can come from CleverTap personalization, and the weather information can come from an API that provides the current weather. If you want to add more information, you can opt for any source, such as third-party tools and in-house software, to include in your message.
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
For more information, refer to [Linked Content](doc:linked-content#write-linked-content).

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
# Recommendations

Click the ![Personalization](https://files.readme.io/b852e7f-Personalization_setting.png) icon in the editor to open personalization options. 

After you have uploaded a [Catalog](doc:catalog), you can display personalized recommendations to your customers. Imagine sending a Web Push notification with shoe recommendations to a user who recently added shoes to their cart but didn't purchase. For more information on recommendations, refer to [Recommendations](doc:recommendations).