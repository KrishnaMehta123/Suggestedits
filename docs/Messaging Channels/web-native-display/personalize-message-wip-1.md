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

<Image title="web native display personalization.png" alt={1850} className="border" border={true} src="https://files.readme.io/33cf886-web_native_display_personalization.png" />

# Liquid Tags

Click the ![Personalization](https://files.readme.io/b852e7f-Personalization_setting.png) icon in the editor to open personalization options.

Liquid tags offer great flexibility while composing personalized messages. They allow adding logic using a scripting language, which can be leveraged to change the look and feel of your message. Following is an example to send personalized coupon codes based on the type of membership:

<Image title="Liquid Tags.png" alt={1134} className="border" border={true} src="https://files.readme.io/03628fb-Liquid_Tags.png" />

Each notification is personalized to the receiver as shown in the following example. 

```html Output - Liquid
Hi John!

Here's a special code for you - MUM50
```

For more information on using tags, refer to [Liquid Tags](doc:liquid-tags).

# Recommendations

Click the ![Personlization](https://files.readme.io/b852e7f-Personalization_setting.png) icon in the editor to open personalization options. 

After you have uploaded a catalog, you can display personalized recommendations to your customers. For example, you can have a sliding carousel displayed to your customers based on their personal likes. For more information on recommendations, see [Recommendations](doc:recommendations).

<Image title="Recommendation_Sample.png" alt={1752} className="border" border={true} src="https://files.readme.io/6264702-Recommendation_Sample.png" />
