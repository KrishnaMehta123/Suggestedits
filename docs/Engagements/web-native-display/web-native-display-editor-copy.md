---
title: Web Native Display Editor (COPY)
excerpt: >-
  Learn how to leverage Web Native Display Editor for creating personalized
  experiences.
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

The Web Native Display editor offers several templates to personalize your customer's website experiences. For example, based on past events, you can personalize the banner or banner carousels on your customers' websites. These templates are mobile responsive, which means marketers can deliver personalized campaigns across devices (mobiles, tablets, desktops, etc.). Additionally, the visual editor template helps you customize the look and feel of the website in real time  through a user-friendly interface and zero development effort.

From the What section in the Web Native Display campaign builder, select the message type and click **Go to Editor.** The Web Native Display Editor displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b71dad4-visual_editor.jpg",
        "",
        "Web Native Display Editor."
      ],
      "align": "center",
      "border": true,
      "caption": "Web Native Display Editor."
    }
  ]
}
[/block]


# Basic Templates

The Web Native Display editor offers six basic templates:

- [Custom key values](doc:web-native-display-editor#custom-key-value)
- [Banner](doc:web-native-display-editor#banner)
- [Banner Carousel](doc:web-native-display-editor#banner-carousel)
- [Banner with Text](doc:web-native-display-editor#banner-with-text)
- [Banner Carousel with Text](doc:web-native-display-editor#banner-carousel-with-text)
- [Visual Editor](doc:web-native-display-editor#visual-editor)

### Custom Key Value

Marketers can use the custom Key-Value template to deliver an engaging and personalized user experience.  
The custom key value can have any value. 

> 🚧 Note
> 
> The first key of your object will always be **topic**. The marketer can provide the relevant value of this key while configuring the campaign. The developer must use this value to access the right payload for that campaign.

For example, if you want to change the carousel images for your users based on their language and favorite products, you can set the custom key-value pairs for this change.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bd5c152-web_native_display_key_value.png",
        "Configure Custom Key-Value Pairs",
        1596
      ],
      "align": "center",
      "border": true,
      "caption": "Define Custom Key-Value Pairs "
    }
  ]
}
[/block]


Refer to the [sample key-value pair web native display campaign](https://developer.clevertap.com/docs/web-native-display#sample-key-value-web-native-display-campaign). It explains the steps you need to perform after creating a campaign in detail.

### Banner

The banner template allows you to create visually appealing banners for your website. You can directly upload the banner image or add a URL to the banner. You also have the flexibility to upload a dedicated image for mobile users to deliver an optimal experience for mobile audiences. 

You must enter the [Div ID](https://developer.clevertap.com/docs/web-native-display#banner-templates) for the relevant container where you wish to render the banner on your website. Optionally, you can also define the Div height to adjust the appearance of your banner.  
You can also provide a URL to redirect users to a specific web page when they click a banner.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/79e565b-banner_1.png",
        "Configuring a Banner Template",
        2558
      ],
      "align": "center",
      "border": true,
      "caption": "Banner Template"
    }
  ]
}
[/block]


### Banner with Text

Similar to the Banner template, the Banner with Text template allows you to create visually appealing banners with personalized messages for contextual communications. Marketers can add Titles and Descriptions to their banners and personalize them to deliver individualized experiences. For example, marketers can target their audience by personalizing names in the banner title for enhanced engagement.

You must enter the [Div ID](https://developer.clevertap.com/docs/web-native-display#banner-templates) for the relevant container where you wish to render the banner on your website. Optionally, you can also define the Div height to adjust the appearance of your banner.  
You can also provide a URL to redirect users to a specific web page when they click the banner.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fe8f080-banner_text.png",
        "Setting up a Banner with Text Template",
        2868
      ],
      "align": "center",
      "border": true,
      "caption": "Banner With Text"
    }
  ]
}
[/block]


Under the _Style_ tab in the editor, you also have the option to align the title and description of your banner as per your design guidelines. You can also define the font style, size,  and color of the title and description.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/12ecfc1-banner_font_2.png",
        "Style your Banner",
        2544
      ],
      "align": "center",
      "border": true,
      "caption": "Banner with Text Editor"
    }
  ]
}
[/block]


### Banner Carousel

Banner Carousels allow you to display up to seven rotating banners that help you deliver engaging content faster. They primarily let you display broader and more engaging content within a restricted area on your website.

Using the Banner Carousel template, you can create promotional and engaging banner slides that can auto-rotate. You can use this template for various purposes, such as displaying the latest product releases on e-commerce sites, banners of web series on OTT platforms, and displaying festive offers on your application's home page. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ec98127-banner_carousel_gif_1.gif",
        "Banner with Carousel",
        1272
      ],
      "align": "center",
      "border": true,
      "caption": "Banner with Carousel"
    }
  ]
}
[/block]


Enter the Div ID for the relevant container on your website where you wish to render the banner carousel. Optionally, you can define the Div height to adjust the appearance of the banner carousel.

You can also provide a URL to redirect users to a specific web page when they click a specific banner slide. Additionally, you can use a different image for mobile users to optimize the viewing experience for your mobile audience.

You need to define the _Slider Time_ (in seconds) so that the banner slides auto-rotate after the defined time. You also have the option to enable the _Carousel dots_ and _Navigation arrows_ to scroll banner slides manually.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/37db7f7-Screenshot_2022-12-11_at_4.35.07_PM.png",
        "Set the Slider Time for Auto Scroll",
        1454
      ],
      "align": "center",
      "border": true,
      "caption": "Define Scroll Time"
    }
  ]
}
[/block]


### Banner Carousel with Text

This template is similar to the _Banner Carousel_ template with an additional option of adding a Title and Description on top of each banner in the carousel. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3fa56dc-banner_carousel.gif",
        "Set up Banner Carousel with Text Template",
        1264
      ],
      "align": "center",
      "border": true,
      "caption": "Banner Carousel with Text"
    }
  ]
}
[/block]


Under the _Style_ tab in the editor, you also have the option to align the title and description of your banner as per your design guidelines. You can also define the font style, size,  and color of the title and description.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5ee93bf-font.png",
        "Customize Web Inbox Appearance",
        2554
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


### Visual Editor

> 📘 Note
> 
> - The Visual Editor feature is currently under Private Beta.
> - CleverTap offers Visual Editor as a paid add-on. Contact your customer success manager to enable this feature for your account.

The Visual Editor template empowers marketers to tailor specific elements on their website, enhancing the user experience for their target audience. This feature lets marketers personalize various content types, such as text or images, using custom HTML or JSON. For instance, marketers can modify the textual content to better resonate with their audience or adjust image content to be more visually appealing and relevant, all through a user-friendly interface and zero development effort.

> 📘 Prerequisites
> 
> - **Web SDK v1.8.0** and above support the Visual Editor. To check your Web SDK version, use the `clevertap.getSDKVersion` method.
> - Ensure that the Content Security Policy (CSP) value for `frame-ancestors` contains `self` value. Without this configuration, the Visual Editor will not work.

To get started with this editor:

1. Select the Visual Editor.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/47fecda-ve_1.jpg",
        "",
        "Visual Editor"
      ],
      "align": "center",
      "border": true,
      "caption": "Visual Editor"
    }
  ]
}
[/block]


2. Enter the webpage URL that you want to personalize and click **Continue**. The web page loads within the editor in a new tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4abc617-url.jpg",
        "",
        "Define Webpage URL"
      ],
      "align": "center",
      "border": true,
      "caption": "Enter Webpage URL"
    }
  ]
}
[/block]


3. After the website loads successfully in the editor, you can hover over the web page, highlighting the web elements.
4. When you select an element for the first time, the system prompts you to choose the editor type (Form, HTML, or JSON).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e5eb090-Editor_type.jpg",
        "",
        "Select Editor"
      ],
      "align": "center",
      "border": true,
      "caption": "Select Editor"
    }
  ]
}
[/block]


4. Select the type of editor (Form, HTML, JSON) you require and click **Continue**.

   1. The Form editor helps you customize multiple aspects of an element. It offers multiple fields for customizing the selected element. 
   2. For example, if you select a text element, the _Form_ editor allows you to modify the Font, Font size, Font Weight, Text Style, Text Color, Margin, Padding, and so on.

      [block:image]{"images":[{"image":["https://files.readme.io/7010855-Form.gif","","Customize Text using Form Editor"],"align":"center","border":true,"caption":"Customize Text using Form Editor"}]}[/block]
   3. If you select an image for customizing, the _Form_ editor allows you to modify the image URL, on-click operations, and overall image dimensions across device types.

      [block:image]{"images":[{"image":["https://files.readme.io/fc23665-image_form.jpg","","Customize Image using Form Editor"],"align":"center","border":true,"caption":"Customize Image using Form Editor"}]}[/block]

<!----->

5. You can also change the Editor by clicking the **Change** button at the top of the page.
   1. If you select the HTML editor, modify the HTML per your use case for the selected element, as shown in the following image:[block:image]{"images":[{"image":["https://files.readme.io/99f0b63-custom_html.jpg","","Custom HTML"],"align":"center","border":true,"caption":"Custom HTML"}]}[/block]
   2. Alternatively, you can define custom JSON using JSON editor.
6. You can Toggle on the **Browse mode** to make the page interactive. It helps you access elements that require user interactions, like dropdowns, menus, and so on.
7. Click the **Preview** button at the top right corner to preview the HTML changes in a new tab.
8. Click **Save** after making the required changes.