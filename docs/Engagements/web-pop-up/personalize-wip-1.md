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

You can personalize the Web Popup title and message body for every user based on specific user property or event property values. For more information on user profile properties and events (dynamic replacements), refer to [User Profiles](https://docs.clevertap.com/docs/user-profiles) and [Events](doc:events).

# Personalization

To invoke the personalization menu, type the @ symbol in the title or the text fields while creating the Web Popup message.

You can also add dynamic replacements in the Web Popup title and body. Notice a preview of the available Web Popup notification as displayed below.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e810241-Web_Popup_Personalizatiom.png",
        "Web Popup Personalizatiom.png",
        2374,
        990,
        "#f1f1f7"
      ],
      "border": true
    }
  ]
}
[/block]
In addition to the title, and the message body, you can also personalize media URLs, deep links, or button URLs. An **@** icon in a box indicates that it can be personalized.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5b5b5b1-Web_Popup_Image_Personalization.png",
        "Web Popup Image Personalization.png",
        1534,
        1038,
        "#eeebf6"
      ]
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
        "https://files.readme.io/f5eac5d-Liquid_Tags.png",
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
Each notification is personalized to the receiver. 
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

# Recommendations

Click the ![Personalization](https://files.readme.io/b852e7f-Personalization_setting.png) icon in the editor to open personalization options. 
After you have uploaded a catalog, you can display personalized recommendations to your customers. Imagine having a rolling carousel displayed to your customers based on their personal likes!  For more information on recommendations, see [Recommendations](doc:recommendations).