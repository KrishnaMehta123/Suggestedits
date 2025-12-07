---
title: Personalize Message (WIP)
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

You can personalize the message for every user based on specific user property or event property values. For more information on user profile properties and events (dynamic replacements), refer to [User Profiles](https://docs.clevertap.com/docs/user-profiles) and [Events](https://docs.clevertap.com/docs/events#event-properties).

# Event and Profile Property Personalization

To invoke the personalization menu, type the *@* symbol in the *Values* field while creating a message.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/33cf886-web_native_display_personalization.png",
        "web native display personalization.png",
        1850,
        968,
        "#efebf6"
      ],
      "border": true
    }
  ]
}
[/block]

#Liquid Tags

Click the ![Personalization](https://files.readme.io/b852e7f-Personalization_setting.png) icon in the editor to open personalization options.

Liquid tags offer great flexibility while composing personalized messages. They allow adding logic using a scripting language, which can be leveraged to change the look and feel of your message. Following is an example to send personalized coupon codes based on the type of membership:
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

# Recommendations

Click the ![Personlization](https://files.readme.io/b852e7f-Personalization_setting.png) icon in the editor to open personalization options. 

After you have uploaded a catalog, you can display personalized recommendations to your customers. For example, you can have a sliding carousel displayed to your customers based on their personal likes. For more information on recommendations, see [Recommendations](doc:recommendations).
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