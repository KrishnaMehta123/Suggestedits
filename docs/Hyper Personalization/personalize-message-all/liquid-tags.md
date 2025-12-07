---
title: Liquid Tags
excerpt: >-
  Learn how you can use Liquid Tags to personalize user communications across
  channels such as Email, SMS, Push, and more.
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

Liquid Tags offer tremendous flexibility and dynamically allow you to personalize content across multiple communication channels. By incorporating real-time user attributes and behaviors, you can craft a single message with multiple variations.

To personalize your messages using Liquid Tags, you can incorporate [User Profile ](https://docs.clevertap.com/docs/user-profiles) properties and [Event](https://docs.clevertap.com/docs/events#event-properties) properties. You can use any available Profile or Event properties within Liquid Tags. Start typing `Profile.` or `Event.` in the editor to automatically view a list of supported properties.

Here is an example that shows how to personalize content using the user property Preferred Language with a Liquid Tag:

```liquid Liquid Tag
{% if Profile.PREFERED_LANGUAGE == "Spanish" %} 
Hola!
{% elsif Profile.PREFERED_LANGUAGE == "English" %}
Hello!
{% endif %}
```

The greeting appears in Spanish if the user's preferred language is Spanish. 

```text Output - Liquid Tag
Hola!
```

The greeting appears in English if the user's preferred language is English.  

```text Output - Liquid Tag
Hello!
```

> 📘 Key Points to Remember
> 
> - Liquid terms are adapted from [shopify's documentation](https://shopify.github.io/liquid/basics/introduction/) for use in CleverTap.  However, CleverTap supports only the terms listed under [Using Liquid Tags](https://staging.docs.user.clevertap.net/docs/liquid-tags-use-cases).
> - When referencing properties, use `Profile.` and `Event.` with capital “P” and “E”, followed by a period.
> - Profile properties are available for all segments. Liquid tags personalization using event properties are supported only for live user segments.
> - The @ Personalization is supported only outside the tags.

# Supported Channels

You can use Liquid Tags with the following messaging channels:​

- Email
- Mobile Push
- SMS
- Webhooks
- App Inbox
- In-App
- Native Display
- WhatsApp

# Video Tutorial

For further information, you can watch the following video on liquid tags:

[block:embed]
{
  "html": "<iframe class=\"embedly-embed\" src=\"//cdn.embedly.com/widgets/media.html?src=https%3A%2F%2Fwww.youtube.com%2Fembed%2F8LX2GcG3V8k%3Flist%3DPLTXk2GzdxAChuuVW4i_H3VwQ9obTRs1L8&display_name=YouTube&url=https%3A%2F%2Fwww.youtube.com%2Fwatch%3Fv%3D8LX2GcG3V8k&image=https%3A%2F%2Fi.ytimg.com%2Fvi%2F8LX2GcG3V8k%2Fhqdefault.jpg&key=f2aa6fc3595946d0afc3d76cbbd25dc3&type=text%2Fhtml&schema=youtube\" width=\"854\" height=\"480\" scrolling=\"no\" title=\"YouTube embed\" frameborder=\"0\" allow=\"autoplay; fullscreen\" allowfullscreen=\"true\"></iframe>",
  "url": "https://www.youtube.com/watch?v=8LX2GcG3V8k&list=PLTXk2GzdxAChuuVW4i_H3VwQ9obTRs1L8&index=14",
  "title": "Product Demo: Liquid Tags",
  "favicon": "https://www.youtube.com/s/desktop/006e516c/img/favicon.ico",
  "image": "https://i.ytimg.com/vi/8LX2GcG3V8k/hqdefault.jpg",
  "provider": "youtube.com",
  "href": "https://www.youtube.com/watch?v=8LX2GcG3V8k&list=PLTXk2GzdxAChuuVW4i_H3VwQ9obTRs1L8&index=14"
}
[/block]


**{{@Meenal I have added the new video below for liquid tags}}**

[block:html]
{
  "html": "<div\n              style=\"\n                position: relative;\n                padding-bottom: 56.25%;\n                height: 0;\n                border-radius: 0;\n                box-shadow: 0 15px 40px rgba(63,58,79,.3);\n                overflow: hidden;\n                min-width:320px\"><iframe\n              src=\"https://clevertap.portal.trainn.co/share/9vrJTcuXpv8PGXDWIgM32w/embed?autoplay=false\"\n              frameborder=\"0\"\n              webkitallowfullscreen\n              mozallowfullscreen\n              allowfullscreen\n              allow=\"autoplay; fullscreen\"\n              style=\"position: absolute; top: 0; left: 0; width: 100%; height: 100%;\"></iframe></div>"
}
[/block]


# Resources

[block:html]
{
  "html": "<html lang=\"en\">\n<head>\n  <meta charset=\"UTF-8\" />\n  <meta name=\"viewport\" content=\"width=device-width, initial-scale=1.0\"/>\n  <style>\n    * {\n      margin: 0;\n      padding: 0;\n      box-sizing: border-box;\n    }\nbody {\n  font-family: -apple-system, BlinkMacSystemFont, \"Segoe UI\", Roboto, sans-serif;\n}\n\n.grid {\n  display: grid;\n  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));\n  gap: 1.5rem;\n  max-width: 1000px;\n  margin: 2rem auto;\n  padding: 1rem;\n  justify-content: center;\n}\n\n.integration-card {\n  display: flex;\n  align-items: center;\n  padding: 1.5rem;\n  background: white;\n  border-radius: 12px;\n  border: 1px solid rgba(0, 0, 0, 0.1);\n  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);\n  transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;\n  text-decoration: none;\n}\n\n.integration-card:hover {\n  box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);\n  transform: translateY(-2px);\n}\n\n.logo-container {\n  display: flex;\n  align-items: center;\n  padding-right: 1rem;\n  border-right: 1px solid rgba(0, 0, 0, 0.1);\n  margin-right: 1rem;\n}\n\n.logo {\n  width: 50px;\n  height: 50px;\n  object-fit: contain;\n  flex-shrink: 0;\n  border-radius: 5px;\n}\n\n.content {\n  display: flex;\n  flex-direction: column;\n  justify-content: center;\n}\n\n.name {\n  font-size: 1rem;\n  font-weight: 600;\n  color: #000;\n  margin-bottom: 0.3rem;\n}\n\n.category {\n  font-size: 0.8rem;\n  color: #666;\n}\n\n@media (max-width: 768px) {\n  .grid {\n    grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));\n  }\n}\n\n@media (max-width: 480px) {\n  .grid {\n    grid-template-columns: 1fr;\n  }\n    }\n  </style>\n  </head>\n<div class=\"grid\">\n\n<body>\n<a href=\"https://staging.docs.user.clevertap.net/docs/liquid-tags-use-cases\" class=\"integration-card\">\n    <div class=\"logo-container\">\n      <img src=\"https://files.readme.io/91ef0c59410c6c8d25c7b02059c94f26fca6c39d77c91c5e7f94d7fc4445fc81-9a4b1fd7-750e-4c9c-9f63-48afc5419a51.png\" alt=\"Using Liquid Tags\" class=\"logo\">\n    </div>\n    <div class=\"content\">\n      <div class=\"name\">Using Liquid Tags</div>\n      <div class=\"category\"></div>\n    </div>\n  </a>\n  <a href=\"https://staging.docs.user.clevertap.net/docs/liquid-tags-use-cases#common-use-case\" class=\"integration-card\">\n    <div class=\"logo-container\">\n      <img src=\"https://files.readme.io/ce865c2412d07b3e92a61f9e1b17169c6e0ec589c226a3af42b52e10a988f891-d0a8a368-305c-4ada-a4e1-3fe7b480fc76.png\" alt=\"Common Use Cases\" class=\"logo\">\n    </div>\n    <div class=\"content\">\n      <div class=\"name\">Common Use Cases</div>\n      <div class=\"category\"></div>\n    </div>\n  </a>\n <a href=\"https://staging.docs.user.clevertap.net/docs/faqs-3\" class=\"integration-card\">\n    <div class=\"logo-container\">\n      <img src=\"https://img.icons8.com/fluency/48/faq.png\" alt=\"FAQs\" class=\"logo\">\n    </div>\n    <div class=\"content\">\n      <div class=\"name\">FAQs</div>\n      <div class=\"category\"></div>\n    </div>\n  </a>\n  </div>\n</body>\n</html>"
}
[/block]