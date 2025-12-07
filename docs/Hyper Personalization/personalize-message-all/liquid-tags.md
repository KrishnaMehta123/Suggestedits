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
> * Liquid terms are adapted from [shopify's documentation](https://shopify.github.io/liquid/basics/introduction/) for use in CleverTap.  However, CleverTap supports only the terms listed under [Using Liquid Tags](https://staging.docs.user.clevertap.net/docs/liquid-tags-use-cases).
> * When referencing properties, use `Profile.` and `Event.` with capital “P” and “E”, followed by a period.
> * Profile properties are available for all segments. Liquid tags personalization using event properties are supported only for live user segments.
> * The @ Personalization is supported only outside the tags.

# Supported Channels

You can use Liquid Tags with the following messaging channels:​

* Email
* Mobile Push
* SMS
* Webhooks
* App Inbox
* In-App
* Native Display
* WhatsApp

# Video Tutorial

For further information, you can watch the following video on liquid tags:

<Embed url="https://www.youtube.com/watch?v=8LX2GcG3V8k&list=PLTXk2GzdxAChuuVW4i_H3VwQ9obTRs1L8&index=14" title="Product Demo: Liquid Tags" favicon="https://www.youtube.com/s/desktop/006e516c/img/favicon.ico" image="https://i.ytimg.com/vi/8LX2GcG3V8k/hqdefault.jpg" provider="youtube.com" href="https://www.youtube.com/watch?v=8LX2GcG3V8k&list=PLTXk2GzdxAChuuVW4i_H3VwQ9obTRs1L8&index=14" html="%3Ciframe%20class%3D%22embedly-embed%22%20src%3D%22%2F%2Fcdn.embedly.com%2Fwidgets%2Fmedia.html%3Fsrc%3Dhttps%253A%252F%252Fwww.youtube.com%252Fembed%252F8LX2GcG3V8k%253Flist%253DPLTXk2GzdxAChuuVW4i_H3VwQ9obTRs1L8%26display_name%3DYouTube%26url%3Dhttps%253A%252F%252Fwww.youtube.com%252Fwatch%253Fv%253D8LX2GcG3V8k%26image%3Dhttps%253A%252F%252Fi.ytimg.com%252Fvi%252F8LX2GcG3V8k%252Fhqdefault.jpg%26key%3Df2aa6fc3595946d0afc3d76cbbd25dc3%26type%3Dtext%252Fhtml%26schema%3Dyoutube%22%20width%3D%22854%22%20height%3D%22480%22%20scrolling%3D%22no%22%20title%3D%22YouTube%20embed%22%20frameborder%3D%220%22%20allow%3D%22autoplay%3B%20fullscreen%22%20allowfullscreen%3D%22true%22%3E%3C%2Fiframe%3E" />

**\{\{@Meenal I have added the new video below for liquid tags}}**

<HTMLBlock>{`
<div
              style="
                position: relative;
                padding-bottom: 56.25%;
                height: 0;
                border-radius: 0;
                box-shadow: 0 15px 40px rgba(63,58,79,.3);
                overflow: hidden;
                min-width:320px"><iframe
              src="https://clevertap.portal.trainn.co/share/9vrJTcuXpv8PGXDWIgM32w/embed?autoplay=false"
              frameborder="0"
              webkitallowfullscreen
              mozallowfullscreen
              allowfullscreen
              allow="autoplay; fullscreen"
              style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
`}</HTMLBlock>

# Resources

<HTMLBlock>{`
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 1.5rem;
  max-width: 1000px;
  margin: 2rem auto;
  padding: 1rem;
  justify-content: center;
}

.integration-card {
  display: flex;
  align-items: center;
  padding: 1.5rem;
  background: white;
  border-radius: 12px;
  border: 1px solid rgba(0, 0, 0, 0.1);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);
  transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
  text-decoration: none;
}

.integration-card:hover {
  box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.1);
  transform: translateY(-2px);
}

.logo-container {
  display: flex;
  align-items: center;
  padding-right: 1rem;
  border-right: 1px solid rgba(0, 0, 0, 0.1);
  margin-right: 1rem;
}

.logo {
  width: 50px;
  height: 50px;
  object-fit: contain;
  flex-shrink: 0;
  border-radius: 5px;
}

.content {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.name {
  font-size: 1rem;
  font-weight: 600;
  color: #000;
  margin-bottom: 0.3rem;
}

.category {
  font-size: 0.8rem;
  color: #666;
}

@media (max-width: 768px) {
  .grid {
    grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
  }
}

@media (max-width: 480px) {
  .grid {
    grid-template-columns: 1fr;
  }
    }
  </style>
  </head>
<div class="grid">

<body>
<a href="https://staging.docs.user.clevertap.net/docs/liquid-tags-use-cases" class="integration-card">
    <div class="logo-container">
      <img src="https://files.readme.io/91ef0c59410c6c8d25c7b02059c94f26fca6c39d77c91c5e7f94d7fc4445fc81-9a4b1fd7-750e-4c9c-9f63-48afc5419a51.png" alt="Using Liquid Tags" class="logo">
    </div>
    <div class="content">
      <div class="name">Using Liquid Tags</div>
      <div class="category"></div>
    </div>
  </a>
  <a href="https://staging.docs.user.clevertap.net/docs/liquid-tags-use-cases#common-use-case" class="integration-card">
    <div class="logo-container">
      <img src="https://files.readme.io/ce865c2412d07b3e92a61f9e1b17169c6e0ec589c226a3af42b52e10a988f891-d0a8a368-305c-4ada-a4e1-3fe7b480fc76.png" alt="Common Use Cases" class="logo">
    </div>
    <div class="content">
      <div class="name">Common Use Cases</div>
      <div class="category"></div>
    </div>
  </a>
 <a href="https://staging.docs.user.clevertap.net/docs/faqs-3" class="integration-card">
    <div class="logo-container">
      <img src="https://img.icons8.com/fluency/48/faq.png" alt="FAQs" class="logo">
    </div>
    <div class="content">
      <div class="name">FAQs</div>
      <div class="category"></div>
    </div>
  </a>
  </div>
</body>
</html>
`}</HTMLBlock>
