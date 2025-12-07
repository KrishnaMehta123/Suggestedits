---
title: Personalize Message (WIP)
excerpt: >-
  Understand how to personalize Web Exit Intent Popups to engage better with
  your customers
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

You can personalize the Web Exit Intent message Title and message body for every user based on specific user property or event property values. For more information on user profile properties and events (dynamic replacements), refer to [User Profiles](https://docs.clevertap.com/docs/user-profiles) and [Events](doc:events).

# Message Personalization

To invoke the personalization menu, type the @ symbol in the title or the text fields while creating the Web Exit Intent message.

You can also add dynamic replacements in the Web Exit Intent title and body. Notice a preview of the available Web Exit Intent notification.

<Image title="Screenshot 2021-10-19 at 4.57.26 PM.png" alt={2874} align="center" className="border" border={true} src="https://files.readme.io/8e7c117-Screenshot_2021-10-19_at_4.57.26_PM.png" />

In addition to the title, and the message body, you can also personalize media URLs, deep links, or button text. An **@** icon in a box indicates that it can be personalized.

<Image title="web exit image personalization.png" alt={1388} align="center" className="border" border={true} src="https://files.readme.io/f2d1808-web_exit_image_personalization.png" />

# Liquid Tags

Click the ![Personalization](https://files.readme.io/b852e7f-Personalization_setting.png) icon in the editor to open personalization options.

Liquid tags offer great flexibility while composing personalized messages. They allow adding logic using a scripting language, which can be leveraged to change the look and feel of your message. Following is an example to send personalized coupon codes based on the type of membership:

<Image title="Liquid Tags.png" alt={1134} align="center" className="border" border={true} src="https://files.readme.io/03628fb-Liquid_Tags.png" />

Each notification is personalized to the receiver as shown in the following example. 

```html Output - Liquid
Hi John!

Here's a special code for you - MUM50
```

For more information on using tags, refer to [Liquid Tags](doc:liquid-tags).

# Recommendations

Click the ![Personalization](https://files.readme.io/b852e7f-Personalization_setting.png) icon in the editor to open personalization options. 

After you have uploaded a catalog, you can display personalized recommendations to your customers. Imagine having a rolling carousel displayed to your customers based on their personal likes!  For more information on recommendations, see [Recommendations](doc:recommendations).
