---
title: In-App Editor Gamification templates
excerpt: Learn how to edit and design In-App campaigns from the CleverTap dashboard.
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

 The In-App editor enables you to add content to pre-built templates or customize and build them. You can select the ready-to-use template of your choice or create a custom HTML template as per your requirements. From the _What_ section in the In-App builder, select the _Message Type_ and click** Go to Editor.**

The In-App Editor tool displays

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0d4cd27-image_interstitial.png",
        "",
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


# In-App Templates

The following are the four main types of In-App templates for creating engaging and personalized In-App campaigns:

- [_Basic Templates_](doc:in-app-editor#basic-templates)
- [_Ratings Templates_ ](doc:in-app-editor#ratings-template)
- [_Lead Generation Templates_](doc:in-app-editor#lead-generation-template)
- [_Custom HTML Templates_](doc:in-app-editor#custom-templates)

## Basic Templates:

Basic Templates are ready-to-use templates that enable you to send tailored and personalized In-App engagements to your mobile users. You can use both text and images with CTAs to send personalized In-App messages basis your business use case.

Using basic templates, you can create the following two types of In-App messages:

- [Content with Image notifications](doc:in-app-editor#content-with-image-notifications)
- [Image-only notifications](doc:in-app-editor#image-only-notifications)

### Content with Image Notifications

These templates allow you to use images in combination with text for effective messaging. Based on your use case, you can choose from a range of templates, such as _Cover_, _Half Interstitial_, _Interstitial_, _Header_, _Footer_, and _Alert_.

### Image-only Notifications

These templates allow you to send visually engaging images that can quickly capture users' attention and encourage them to engage with the message when they launch the app. When selecting an _image only_ template, you can send a message containing only an image (without CTAs, title, or message).

You can choose from the following four types of image-only notifications:

#### Cover

It is a full-screen notification template that is valuable when the intention is to direct the user's focus toward essential actions, such as requiring them to install a necessary app update.

#### Half Interstitial

It is a center-aligned image notification template that drives better engagement. You can use this template when you want to attract the user's attention to a sale or discount.

#### Interstitial

 It is a center-aligned image notification template you can use to drive better engagement during app launch.

#### Image Interstitial

> 📘 Availability
> 
> The **Image Interstitial** template is available only with CleverTap Advanced and Cutting Edge plans.

This template helps craft personalized In-App messages that match your app's aesthetics seamlessly. You upload an image and elevate the experience by incorporating up to 10 interactive hotspots, each with its own unique actions. For example, you can use this template to create a rewarding offer for your gaming app users. The following image represents a sample In-App campaign for rewarding users using the Image Interstitial template:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7da5c6a-Image_Interstitial_full.png",
        "",
        "Sample In-App Campaign using Image Interstitial Template"
      ],
      "align": "center",
      "border": true,
      "caption": "Sample In-App Campaign using Image Interstitial Template"
    }
  ]
}
[/block]


The Image Interstitial template primarily comprises the following three elements:

- **Overlay**: This element is a middle layer between your In-App message and your app in the background. By default, it is transparent; however, you can select a color of your choice or upload an image to it. Using the Overlay configuration, you can:
  - Opt for a semi-transparent color to softly mask the app in the background, drawing more attention to the in-app message in the foreground.
  - Upload a patterned image to create a captivating, full-screen, layered in-app message experience.
- **Content**: It is the core element of the template. Click in the center of a blank device or select the **Content** option from the _Element_ dropdown to activate it. Further, upload an image (JPG, PNG, or GIF) consisting of all In-App message elements such as background, text, and buttons.  
  The editor fits the image within the Content container while preserving its aspect ratio without cropping. By default, a 10% margin is applied to the Content container. However, you can change that from the _Margin_ field.
- **Buttons**:  The Image Interstitial buttons are transparent regions you can place over a Content layer. You can easily move and adjust their size to align with the button elements on the image. 

The selection area within the Content Container automatically adapts to various device screen sizes, eliminating the need to create multiple versions for different devices. To see how the image and buttons scale across different aspect ratios, use the dropdown menu with different device viewport sizes located at the top for a preview.

> 📘 Preview & Test
> 
> - The _Preview & Test_ feature for sending tests on the device is not available for iOS or Android SDK versions lower than **6.0.0** and Unity **3.0.0.** If you need to test on a device with a lower SDK version, send the campaign exclusively to the user first, and then recreate and send it to the intended audience.

### Guidelines for Template Aspect Ratio and File Size

The following tables include the guidelines that you must keep in mind when creating In-App messages:

[block:parameters]
{
  "data": {
    "h-0": "Canvas Type",
    "h-1": "Canvas Aspect Ratio",
    "h-2": "Sample Image Sizes",
    "h-3": "Image Type Supported",
    "h-4": "Image Sample",
    "0-0": "Cover",
    "0-1": "Full Screen",
    "0-2": "Screen Resolution",
    "0-3": "Image",
    "0-4": "<ul>\n<li><a href=\"https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Cover-iPad.jpg\">Cover iPad</a></li>\n<li><a href=\"https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Cover.jpg\">Cover</a> </li>\n</ul>  \n  \n<br />",
    "1-0": "Interstitial",
    "1-1": "1.78:1",
    "1-2": "16:9",
    "1-3": "Image, gif, audio, video",
    "1-4": "<ul>\n<li><a href=\"https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Interstitial-iPad-Pro.jpg\">Interstitial iPad Pro</a></li>\n<li><a href=\"https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Interstitial-iPad.jpg\">Interstitial iPad</a></li>\n<li><a href=\"https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Intertitial.jpg\">Interstitial</a> </li>\n</ul>  \n  \n<br />",
    "2-0": "Half Interstitial",
    "2-1": "1.30:1",
    "2-2": "3:4",
    "2-3": "Image",
    "2-4": "<ul>\n<li><a href=\"https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Half-Interstitial-ipad-Pro.jpg\">Half Interstitial iPad Pro</a></li>\n<li><a href=\"https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Half-Interstitial-ipad.jpg\">Half Interstitial iPad</a></li>\n<li><a href=\"https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Half-Intertitial.jpg\">Half Interstitial</a> </li>\n</ul>  \n  \n<br />",
    "3-0": "Header",
    "3-1": "Height: 1:1  \nWidth: Fit to screen",
    "3-2": "N/A",
    "3-3": "Logo Image",
    "3-4": "Title :parameters]  \n{  \n, Message {  \n    \"h-0\": \"C\\* Title e\",  \n    \"h-1\": , Message pect Ratio\",  \n   Title : \"Sample Image, Message \\[75 Characters",
    "4-0": "Footer",
    "4-1": "Height: 1:1  \nWidth: Fit to screen",
    "4-2": "N/A",
    "4-3": "Logo Image",
    "4-4": "",
    "5-0": "Alert",
    "5-1": "Native",
    "5-2": "N/A",
    "5-3": "N/A",
    "5-4": "",
    "6-0": "Image Only Cover",
    "6-1": "",
    "6-2": "",
    "6-3": "",
    "6-4": "",
    "7-0": "Image Only Half Interstitial",
    "7-1": "",
    "7-2": "",
    "7-3": "",
    "7-4": "",
    "8-0": "Image Only Interstitial",
    "8-1": "",
    "8-2": "",
    "8-3": "",
    "8-4": ""
  },
  "cols": 5,
  "rows": 9,
  "align": [
    "left",
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]


#### File Size Guidelines

- **Image**: Less than 500 kb.
- **Audio**: Less than 5 Mb.
- **Video**: Less than 50 Mb.

#### Message Character Limit

| Language | Title           | Message          |
| :------- | :-------------- | :--------------- |
| English  | 30              | 128              |
| Chinese  | 9 (Approximate) | 38 (Approximate) |
| Arabic   | 9 (Approximate) | 38 (Approximate) |

> 🚧 Image Cropping
> 
> Due to the multiple phone sizes on both Android and iOS, we will center crop images if the image does not fit the screen resolution.  
> We scale the image uniformly (maintaining the image's aspect ratio) so that both dimensions (width and height) of the image will be equal to or larger than the corresponding dimension of the phone (minus padding). The image is then center-aligned.
> 
> **Image Cropping does not apply for Image Interstitial template.**

> 🚧 Video Messages
> 
> When adding video messages to In-App, ensure an audio track is always present.  
> If required, insert a blank audio track to the video.

## Ratings Template

Marketers can now create feedback-related popups for their mobile app users using the _Ratings Template._  
They can now create two types of rating templates for gaining feedback from their customers:

- User Rating Popup - It helps assess how happy your customers are with your services by taking feedback in the form of star ratings.
- NPS Popup - It enables you to measure the loyalty of your customers by distinguishing them in three categories - **Promoters**, **Passives**, **Detractors**.  One can view the NPS performance by navigating to the [NPS board](doc:nps-board) available under the _Boards_ section.

The following images represent a sample _User Rating Popup_ and _NPS popup_ in a mobile app.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cc3f275-inapp.png",
        "Capture User Rating",
        568
      ],
      "align": "center",
      "sizing": "25% ",
      "border": true,
      "caption": "User Ratings Popup"
    }
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3d18243-in-app_nps.png",
        "Capture NPS",
        542
      ],
      "align": "center",
      "sizing": "25% ",
      "border": true,
      "caption": "NPS Popup"
    }
  ]
}
[/block]


Marketers get the complete flexibility to explicitly define the rating scale, style, shape (Star, Heart, Emojis), labels, and the overall content of the popup. One can also choose to add a comment box to get accurate user feedback/comments.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d76e790-in_app_styles.png",
        "Style Rating Template Elements",
        2044
      ],
      "align": "center",
      "border": true,
      "caption": "In-App Editor Style"
    }
  ]
}
[/block]


Besides, additional styling, such as configuring the color for the message, question, background, and rating scale is also possible from the editor, as shown in the image above. The In-App notification text fields shown below can be personalized for every user based on specific user property or event property values. To learn more about tracking and monitoring user rating data, refer to [Analysing User Rating](doc:user-ratings).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ae7f02c-rate.png",
        "Compose In-App Message for Ratings Template",
        1694
      ],
      "align": "center",
      "border": true,
      "caption": "Compose In-App Message"
    }
  ]
}
[/block]


### Follow-up Question Templates

A follow-up question to your ratings can provide more insights about the user experience. CleverTap provides the following Follow-up Question templates:

- NPS with Follow-up Question
- User Ratings with Follow-up Question

For example, after a user has submitted a rating on your app, you can ask follow-up questions such as _What did you like most about us?_ and provide reply choices such as Variety, Prices, Quality, Customer Service, Delivery Process, and Website Usability. This can help you get more specific feedback to improve your product and services. Following is an image from the in-app editor: 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4766cd8-inapp_followup_nps.jpg",
        null,
        "Short Keyword Choices"
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true,
      "caption": "Short Keyword-Based Choices"
    }
  ]
}
[/block]


You can also list descriptive choices such as,_ I like the available options and variety_, _I like the quality and durability of the products_, and so on. Following is an image from the in-app editor:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0decade-inapp_followup_qs_list.jpg",
        null,
        "Long Sentence Choices"
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true,
      "caption": "Descriptive Choices"
    }
  ]
}
[/block]


You can configure the follow-up question from the Web Popup editor with a short keyword-based grid (up to six choices) or a longer sentence-based list (up to four choices).

The label will be the text you want to display to your users. If you want to allow the user to select multiple choices, select _Allow multiple selections_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fd33f9a-image_18.png",
        null,
        "Configure Follow-up Popup"
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "Configure Follow-up Popup"
    }
  ]
}
[/block]


> 📘 Note
> 
> In the case of the User Ratings template, the _Notification Clicked_ event is raised that records the user's clicks on the CTA buttons and the Close button

## Lead Generation Template

We know that a significant number of App users may remain anonymous. This poses a challenge to continue engaging with potential customers after they leave your App. A lead generation template can solve this issue.

Integrating a lead generation form into your App lets you get important customer details such as name, email address, phone number, etc. This information is helpful for further communication through channels such as SMS, Email, WhatsApp, and others. This post-visit communication helps stay connected with your audience and opens doors for future business opportunities. You can turn anonymous visitors into loyal customers with your App's CleverTap Lead Generation Template.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3658161-InApp_Lead_Gen_sample_window.png",
        null,
        "Sample Lead Generation Template"
      ],
      "align": "center",
      "sizing": "40% ",
      "border": true,
      "caption": "Sample Lead Generation Template"
    }
  ]
}
[/block]


### Post Submit Actions

When a user submits information on your Lead Generation template:

- A _Notification Clicked_ event is raised that records the click on the CTA. 

- A custom event named _Lead Submitted_ records the details submitted by the user as of event properties. Following is a sample form image:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0cae15f-Lead_Gen_Template_preview_with_fields.png",
        null,
        "Form Submit Actions"
      ],
      "align": "center",
      "sizing": "50% ",
      "caption": "Form Submit Actions"
    }
  ]
}
[/block]


Following is a table that records the relevant properties for the fields displayed on the form:

| Submitted Event Properties | Sample Property Value               |
| :------------------------- | :---------------------------------- |
| First Name                 | John                                |
| Last Name                  | Smith                               |
| Email ID                   | [john@abc.com](mailto:john@abc.com) |
| Phone Number               | \+11234567890                       |
| Campaign ID                | 121110987654                        |
| Variant                    | wzrk_default                        |

- The user profile is automatically updated with the submitted event properties. For example, the lead generation template can ask for additional details from an anonymous user, such as first name, last name, email, and phone number. His profile will be updated with these details, and now you can identify the user as _John Smith_.

### Lead Generation Template Variants

The following are the two types of Lead Generation templates:

- **Text**: You can create a text-only lead generation template to record user information. 
- **Image on Top**: You can add an image on top of the lead generation template. 

Create the content to record information from your users. The following image displays a preview of the form:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/035a137-lead_gen.png",
        null,
        "Create Lead Generation Template"
      ],
      "align": "center",
      "border": true,
      "caption": "Create Lead Generation Template"
    }
  ]
}
[/block]


Select the button style and card positions from the _Style_ tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/06cbbe4-In-App_Template_Lead_Gen_Content_Editor.png",
        null,
        "Style Lead Generation Elements"
      ],
      "align": "center",
      "border": true,
      "caption": "Style Lead Generation Elements"
    }
  ]
}
[/block]


Enter all the required information. 

- _Text_: Personalize the Title and Description. 
- _Media_: Add the image URL or upload an image. 
- _Input Fields_: You can add up to four input fields. Select input fields such as Name, Phone Number, Birthday, or Email Address for the template. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6a87857-Lead_Gen_Template_Input_Fields.png",
        "Lead Gen Template Input Fields.png",
        1304
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Upto Four Input Fields "
    }
  ]
}
[/block]


- _Buttons_: The _Close_ button is selected by default. Add a button name such as _Submit_ or _Upload_. 
- _Subtext_: Add subtext such as _privacy policy_ to your lead generation template.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bb6e1f2-Lead_Gen_Template_SubText_preview.png",
        "Lead Gen Template SubText preview.png",
        "Add Subtext"
      ],
      "align": "center",
      "sizing": "55% ",
      "border": true,
      "caption": "Add Subtext"
    }
  ]
}
[/block]


The hyperlinked part must be closed between two asterisks. Add the URL where the user will be directed. You can also add a checkbox for your subtext.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d740b86-Lead_Gen_Template_SubText.png",
        "Lead Gen Template SubText.png",
        "Subtext and redirect URL"
      ],
      "align": "center",
      "sizing": "55% ",
      "border": true,
      "caption": "Subtext and redirect URL"
    }
  ]
}
[/block]


- _Acknowledgement_: You can show appreciation to your user by adding an Acknowledgement popup. Select the auto-close timer for the popup.

Select the button style and card positions from the _Style_ tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/92ac44f-In-App_Template_Types_Lead_Gen_Style.png",
        null,
        "Card Orientation"
      ],
      "align": "center",
      "sizing": "55% ",
      "border": true,
      "caption": "Card Orientation"
    }
  ]
}
[/block]


## Custom Templates

You can use the Custom HTML templates in the In-App editor to add more customization to the In-App messages with JavaScript. These templates let you go beyond static messages by adding gamified logic, dynamic visuals, and custom user interactions.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5638bd2-in-app_journey_custom_HTML.png",
        "Custom Template with HTML and Javascript",
        1108
      ],
      "align": "center",
      "border": true,
      "caption": "Custom HTML and Actions"
    }
  ]
}
[/block]


Select the _Include JavaScript_ option to add your custom JavaScript code.

> 📘 Create Interactive In-App Messages
> 
> You can create interactive in-app campaigns such as scratch card campaigns and swipe interaction campaigns using JavaScript.
> 
> Using the _Custom HTML_ option, you can use Javascript in the HTML and create deep interactive in-app campaigns by adding the JavaScript code along with the HTML code. 
> 
> JavaScript-based campaigns are available for versions 3.5.0 and above.

### In-App Gamification Templates

Use CleverTap's out-of-the-box (OOTB) **Scratch the Card** and **Spin the Wheel** In-App message templates to engage users through interactive rewards, and can be easily customized using editable HTML settings.

Gamification templates let you create interactive in-app experiences with minimal effort. With CleverTap, you can:

- Increase engagement and conversions through game-like interfaces
- Offer personalized rewards dynamically
- Fully customize the look and feel using the _Custom HTML Templates_ tab

These templates include configurable variables for visuals, copy, animation, rewards, and behavior.

**Using the Templates**

1. Go to _Create In-App Message > Single Message_.
2. Select the **Custom HTML Templates** tab.
3. Select either:

   - [Spin the Wheel](doc:in-app-editor-copy#spin-the-wheel-template)
   - [Scratch the Card](doc:in-app-editor-copy#scratch-the-card-template)
4. Edit the settings and the Custom HTML to publish.

### Spin the Wheel Template

This template adds a fun, gamified interaction to your In-App by letting users spin a virtual wheel to unlock a discount, reward, or surprise offer directly within it. This interactive format helps boost engagement and click-through rates while creating a sense of excitement and urgency.

#### Interactive Elements

- Wheel animation with easing
- Pointer interaction + spin trigger
- Shimmer effect on reveal

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bdfae57effccaa9fa2e956e102045ef43faf8762bbd7cced7826bd60c406f820-image.png",
        null,
        "Spin "
      ],
      "align": "center",
      "sizing": "25% ",
      "caption": "Spin the Wheel Template"
    }
  ]
}
[/block]


<details>

<summary><b>Expand to know more about the template.</b></summary>

### Use Case Examples

- Drive conversions during sales events or festivals with spin-to-win deals.
- Run promotional campaigns that reward users with random offers.
- Re-engage dormant users with a playful incentive.
- Launch loyalty or referral-based programs with interactive rewards.

### Template Customization Variables

This template allows you to tweak the appearance, messaging, and reward logic without the need to understand or modify the full code. Each setting explained here lets you control how the in-app experience looks and behaves, so you can launch high-converting, on-brand campaigns effortlessly. The following are the settings:

- `includeDmissButton`: Show or hide the close (X) button.
- `background`: Set the modal background color or gradient.
- `enableConfettiOnWin `: Toggle confetti animation after a win.
- `spinDurationSeconds`: Set how long the wheel spins (in seconds).
- `spinButton`: Customize the spin button’s text, color, background, and visibility.
- `claimButton`: Configure the claim button after spinning, text, color, background, and link (URL).
- `mainTitle`: Set the main headline text, font size, and color.
- `subtitle`: Set the subheading or description under the title, text, font size, and color.
- `copyInstruction`: Define the message color before and after users copy a reward code.
- `centerCircle`: Style the center hub of the wheel — color, border, and size.
- `rewards`: Define each reward option with the following:
  - `title`: Message shown on winning
  - `text`: Reward label (shown on wheel)
  - `value`: Copyable code
  - `subtitle`: Description/details
  - `probability`: Win chance
  - `colour`: Slice background color

### Configurable Settings in Template Explained

The following is a description of the customizable variables in CleverTap's Spin the Wheel gamification template.

#### includeDismissButton

Shows or hides the close (X) button on the modal. Set this to `false` if you want users to stay on the message until they take action.

```js
includeDismissButton: true,
```

#### background

Defines the background style of the spin screen. You can use a flat color or a gradient to match your campaign theme.

```js
background: "linear-gradient(180deg, #FF3672 0%, #8332F9 46.63%, #6708BC 84.62%, #4E15DD 100%)",
```

#### enableConfettiOnWin

Adds celebratory confetti after the wheel stops to boost delight. Use it to make wins feel exciting.

```js
enableConfettiOnWin: true,
```

#### spinDurationSeconds

Sets the number of seconds the wheel spins before revealing the reward. A longer duration adds suspense.

```js
spinDurationSeconds: 5,
```

#### spinButton

Customize the call-to-action (CTA) that users click to start the spin. Update the text to match your promotion (for example, "Try Your Luck", "Spin to Save").

```js
spinButton: {
  enabled: true,
  text: "Spin Now",
  background: "#ffffff",
  color: "#1d1d1d",
},
```

#### claimButton

Configure the button that appears after a spin. You can drive users to a landing page or apply a reward using a custom link.

```js
claimButton: {
  enabled: true,
  text: "Collect Now",
  background: "#F4357D",
  color: "#ffffff",
  url: "wzkr://thisleadstonowhere",
},
```

#### mainTitle

Control the headline at the top of the spin modal. Use this to grab attention with bold and fun messaging.

```js
mainTitle: {
  text: "🎉 Spin the Wheel <br>& Win Big!",
  fontSize: "24px",
  color: "#ffffff",
},
```

#### subtitle

Add supportive messaging under the title. This is where you reinforce the benefit (for example, savings, gifts, exclusives).

```js
subtitle: {
  text: "Your chance to score discounts, free gifts, and exclusive perks is just a spin away.",
  fontSize: "14px",
  color: "#e8f5ff",
},
```

#### copyInstruction

Set the message and color when users copy a reward code. You can highlight that the code was successfully copied.

```js
copyInstruction: {
  color: "#606060",
  copiedColor: "#F4357D",
},
```

#### centerCircle

Adjust the style of the central hub of the wheel (the spinner core). You can tweak the color, border, and size to match your brand.

```js
centerCircle: {
  color: "#914DFF",
  borderColor: "#2B2B2B33",
  borderWidth: 2,
  radius: 15,
},
```

#### rewards

It is the core of the experience. Each entry defines a reward slice on the wheel: what it says, the code it provides, a description, color, and the chance it gets selected. Check that the probabilities add up reasonably (they don’t need to equal 1).

```js
rewards: [
  {
    title: "Congrats! You just won a Promo Code!",
    text: "10% OFF",
    value: "DISCOUNT10",
    subtitle: "Use DISCOUNT10 at checkout to get 10% off your order. Valid through April 30.",
    probability: 0.15,
    colour: "#ffffff",
  },
  {
    title: "Congrats! You just won a Free Shipping!",
    text: "Free Shipping",
    value: "FREESHIP",
    subtitle: "Use FREESHIP at checkout to enjoy free shipping on your order. Valid through April 30.",
    probability: 0.15,
    colour: "#fc2b46",
  },
  // Add more rewards as needed
],
```

</details>

### Scratch the Card Template

This interactive template is designed to gamify the user experience by letting users "scratch" to reveal a reward, such as a coupon, discount, or points. The surprise element boosts engagement and reactivation rates while offering a delightful experience.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/18e7bedad81f6ebb2df2ed18065f64f4e12e11a0c151fb59338b1b7fa60e19b3-image.png",
        null,
        "Scratch the Card Template"
      ],
      "align": "center",
      "sizing": "25% ",
      "caption": "Scratch the Card Template"
    }
  ]
}
[/block]


### Interactive Elements

- Scratch-to-reveal animation
- Shimmer effect on reward
- Confetti animation post-reveal
- Claim button redirect
- Copy reward to clipboard

<details>

<summary><b>Expand to know more about the template.</b></summary>

### Use Case Examples

- Engage users during festive or seasonal campaigns with surprise offers.
- Reactivate dormant users by giving them a chance to win a reward.
- Reward loyal customers with a fun, interactive coupon reveal.
- Launch a limited-time “scratch-to-win” contest to drive urgency and clicks.

### Template Customization Variables

This template allows you to tweak the appearance, messaging, and reward logic without the need to understand or modify the full code. Each setting explained here lets you control how the in-app experience looks and behaves, so you can launch high-converting, on-brand campaigns effortlessly. The following are the settings:

- `imageUrl`: URL of the image displayed above the scratch card (e.g., treasure chest).
- `includeDismissButton`: Toggle visibility of the close (X) button.
- `background`: Initial background color or gradient.
- `revealedBackground`: Background after scratching completes.
- `enableConfettiOnReveal`: Show celebratory confetti after reveal.
- `revealButton`: CTA before scratching. Customize text, color, and background.
- `claimButton`: CTA after reveal. Customize text, color, background, and destination URL.
- `mainTitle`: Controls headline text, color, font size, and optional text shadow.
- `subtitle`: Supports descriptive text below the title. Customize color and size.
- `rewards` – Define each potential reward with:
  - `title`: Message shown after reveal
  - `value`: Copyable code
  - `subtext`: Description or redemption details
  - `probability`: Chance of appearing

#### Config Snippets Explained

The following is a description of the customizable variables in CleverTap's _Scratch the Card_ gamification template.

#### imageUrl

Sets the image shown above the scratch card.

```js
imageUrl: "https://.../scratch-the-card-chest.png",
```

#### includeDismissButton

Set to `false` if you want the user to complete the interaction.

```js
includeDismissButton: true,
```

#### background

Defines the initial background of the scratch card.

```js
background: "linear-gradient(180deg, #41F4BC 0%, #35ABFF 37.98%, #0060A5 100%)",
```

#### revealedBackground

Changes the background after the reward is revealed.

```js
revealedBackground: "linear-gradient(180deg, #41F4BC 0%, #35ABFF 100%)",
```

#### enableConfettiOnReveal

Celebratory animation to increase visual delight.

```js
enableConfettiOnReveal: true,
```

#### revealButton

Customize the call-to-action before the reward is shown.

```js
revealButton: {
  enabled: true,
  text: "Reveal My Prize",
  background: "#ffffff",
  color: "#1d1d1d",
},
```

#### claimButton

Configure how users can claim or use the reward.

```js
claimButton: {
  enabled: true,
  text: "Claim",
  background: "linear-gradient(180deg, #A4FFE4 -0.8%, #41F2BE 99.2%)",
  color: "#000000",
  url: "wzkr://thisleadstonowhere"
},
```

#### mainTitle

Control the primary heading inside the card.

```js
mainTitle: {
  text: "Scratch & Win: <br>A Surprise Awaits!",
  fontSize: "24px",
  color: "#ffffff",
  textShadow: "0 2px 4px rgba(0, 0, 0, 0.3)",
},
```

#### subtitle

Supplementary text below the title.

```js
subtitle: {
  text: "Feeling lucky? Scratch the card to reveal your reward...",
  fontSize: "14px",
  color: "#e8f5ff",
},
```

#### rewards

Each reward entry has:

```js
rewards: [
  {
    title: "Congrats! You just won a Promo Code!",
    value: "DISCOUNT10",
    subtext: "Use DISCOUNT10 at checkout...",
    probability: 0.45,
  },
  // Add more reward options here
],
```

</details>

## Best Practices

- Keep reward probabilities realistic; the total does **not** need to equal 1.
- Use high-contrast text over bright gradients for readability.
- Add expiration dates in reward subtext to create urgency.
- Use consistent reward identifiers across campaigns for tracking.

## Custom Code Templates {@sunil to remove it}

You can easily import your custom designs into CleverTap using custom code templates. It allows you to maintain your app's unique look and feel. This integration will enable you to conveniently control message delivery preferences, frequency, and other aspects. The custom templates can be used as key-value pairs, providing a simple way to create highly complex and customized messages without needing to write any code. This integration also eliminates the need for third-party tools to update your messaging. CleverTap gives you complete control over message delivery, frequency, and limits without requiring code modifications. You can use your designs and CleverTap's robust delivery capabilities to ensure design, rendering, and visualization consistency.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bee5455-image.png",
        null,
        "Sample custom in-app"
      ],
      "align": "center",
      "border": true,
      "caption": "Sample Custom In-App"
    }
  ]
}
[/block]


The key-value pairs can be a string, number, image, or file type. Your developers can send the code to CleverTap using the CleverTap SDK. For more information about the integration, refer to the {in-app dev doc}. After the integration, you can begin creating templates from the CleverTap dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/75f1c5a-image.png",
        null,
        "Editing a Custom Code Template"
      ],
      "align": "center",
      "border": true,
      "caption": "Edit Custom Code Template"
    }
  ]
}
[/block]


## App Functions

App functions are functions provided by CleverTap that can trigger native OS prompts (Android or iOS) for different use cases. These App Functions trigger native prompts to engage users from within the app at the right moment. These prompts are the following: 

- App Rating -  Encourage app ratings during high-satisfaction moments from within the app.
- Push Permission -  Increase opt-in rates for push notifications from within the app.
- Open URL - Guide users to external links or deep-linked screens at key user moments  to improve engagement from within the app.

These functions are designed to be embedded within in-app messages (as button actions) or launched directly as standalone in-app campaigns.

Using app functions as a button in an in-app 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7dd551689091fc009864e7abcb42f5cf5ad3076f096b1541df5cde697dfdc322-image.png",
        null,
        "System App Functions"
      ],
      "align": "center",
      "border": true,
      "caption": "System App Functions"
    }
  ]
}
[/block]


### App Function as Button {@sunil to rethink the headings}

{@martin to share the rendered app rating screenshot}

How ths can be used.

Embed app function as a button in in-app.

{@martin, the app functions as button can be used only from advanced in-app builder right ? should we keep this section here then ?}

Increase the likelihood that a user will allow a push on the device or provide a positive app rating.

Using app function as an action button in in-apps allows you to 

Use App Functions as button actions to trigger native app prompts, such as requesting ratings, push permissions, or opening URLs, directly when a user taps a button in your in-app message.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/afc88054ed2adc8e072e5c216b13905469e64289a6e2f74b762bbb8430e33c6e-image.png",
        null,
        "App Function as a button"
      ],
      "align": "center",
      "border": true,
      "caption": "App Function as a Button"
    }
  ]
}
[/block]


To use an app function as a button in an in-app message:

1. Create In-App campaign.  
2. Go to the _What_ section and open the Advanced In-App Builder.
3. Add a button to your message layout.
4. In the On Tap list for the button, select App Function.
5. Select any one of the following App Functions:

Choose one of the following **App Functions** in the button action dropdown:

[block:parameters]
{
  "data": {
    "h-0": "App Function",
    "h-1": "Description",
    "h-2": "Considerations and  Recommended Use Cases",
    "0-0": "**Request App Rating**",
    "0-1": "Displays the native app store rating prompt.",
    "0-2": "- OS platforms control when and how often the prompt appears (may not always show). <br> - No analytics events are tracked.<br> Use after a positive interaction (e.g., subscription renewal, milestone).",
    "1-0": "**Request Push Permission**",
    "1-1": "Prompts the user for push notification permissions.",
    "1-2": "- Prompt won’t show if permission is already granted. <br> - If previously denied, redirects to app settings.<br> Use after value explanation in a prior screen.",
    "2-0": "**Open URL**",
    "2-1": "Opens a web page or app deep link.",
    "2-2": "- URL open events are not tracked.<br> - Ensure URL is valid and accessible across platforms.<br>  Use for external content, offers, or account linking."
  },
  "cols": 3,
  "rows": 3,
  "align": [
    null,
    null,
    null
  ]
}
[/block]


> 📘 Tip
> 
> Always include a context-setting message before triggering system prompts. For example, explain the value of enabling notifications before displaying the push permission dialog.

### App Function as Campaign

{@martin to share the rendered app rating screenshot}

You can use App Functions as a campaign when you want to engage the user after specific actions. For example, a user is more likely to accept push prompts from the app after purchasing to track the item's delivery.  

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7d621f9905b1c6cc33e754396027174215e7376ea7915c7f391b20c85e25afb4-image.png",
        null,
        "App Function as a campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "App Function as a campaign"
    }
  ]
}
[/block]


To use an app function as a stand-alone campaign: 

1. Create In-App campaign.  
2. Go to the _What_ section and open the In-App Editor. 
3. Click the _App Functions_ tab. The app functions will display. 
4. Select from the following App functions to run as a standalone campaign: 

[block:parameters]
{
  "data": {
    "h-0": "App Function",
    "h-1": "Description",
    "h-2": "System Behavior",
    "0-0": "**Request App Rating**",
    "0-1": "Prompts the native app store rating dialog.",
    "0-2": "- May not always appear (controlled by OS)<br>- Cannot be forced or tracked",
    "1-0": "**Request Push Permission**",
    "1-1": "Triggers the OS-level push notification permission prompt.",
    "1-2": "- If **granted**: prompt is skipped<br>- If **denied**: user is redirected to Settings<br>- If **not yet asked**: prompt is shown",
    "2-0": "**Open URL**",
    "2-1": "Opens a web page or deep link.",
    "2-2": "- Tracks `Notification Viewed` for campaign<br>- URL click itself is **not** tracked"
  },
  "cols": 3,
  "rows": 3,
  "align": [
    null,
    null,
    null
  ]
}
[/block]


> 📘 **Note**
> 
> App Functions triggered as standalone campaigns do **not** display an in-app message overlay. These are native system calls executed directly from CleverTap.

### Event Tracking Matrix

Understand what system events are tracked when using each App Function. Tracking behavior differs between **button-triggered** functions and **standalone** in-app campaigns.

| App Function                | Used As             | `Notification Viewed` | `Notification Clicked` | Other Events Tracked? | Notes                                                                  |
| --------------------------- | ------------------- | --------------------- | ---------------------- | --------------------- | ---------------------------------------------------------------------- |
| **Request App Rating**      | Button Action       | Yes                   | Yes                    | No                    | Tracks standard in-app events only, not rating prompt outcome.         |
|                             | Standalone Campaign | No                    | No                     | No                    | OS restricts tracking when system rating dialog is triggered directly. |
| **Request Push Permission** | Button Action       | Yes                   | Yes                    | No                    | Tracks campaign events, but **not** the native push prompt             |
|                             | Standalone Campaign | Yes                   | No                     | No                    | Tracks prompt **view**, but not **click** or OS permission result.     |
| **Open URL**                | Button Action       | Yes                   | Yes                    | No                    | Tracks only the in-app message interaction.                            |
|                             | Standalone Campaign | Yes                   | No                     | No                    | Only campaign view tracked; URL destination is not tracked.            |

> 📘 **Note**
> 
> _Notification Viewed_ and _Clicked_ refer to **in-app campaign events**, not the system prompt itself. CleverTap cannot track actions performed within OS-native dialogs.

### Using App Functions

Turn any in-app that is created on our editor into a pre-permission campaign by connecting it to the in-app function. Native app prompts are generally irreversible and one-time actions. App functions can act as a first and reversible layer for user action and prime the user before presenting the user with the system prompt, such as rating the app or requesting push permission on the device. {@sunil to reuse this section later}

#### Push Pre-Permission

{add a visual here}

Imagine having to ask for permission to deliver a push to the user's device. A native prompt is available in the device OS (Android or iOS) to achieve this. However, this being a native app prompt, it will be executed only once. The user has only one chance to either accept or reject it. There is no chance for regret. However, you can add an introductory layer

The user can create an in-app message using our editor by simply having a button with this function. fast-track and achieve the push pre-permission use case by using the Out of the box structure provided by clevertap. 

Same for app rating

No steps required. 

#### App Rating Lead-In

{add a visual here}

as a button

as a campaign

How to achive push permission {with images}

How to achieve the ask for rating {with images}

Martin wants to add a separate page for app functions.

1. What are app functions
2. How easy it is to create native app prompts using CleverTap 
3. use cases such as app rating, push pre-permissions

<https://docs.leanplum.com/docs/push-pre-permission-message>

<https://docs.leanplum.com/docs/app-function>

# Time to Live (TTL)

You can configure the number of days (or hours) to keep the message on the user's device by setting the _time to live_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/35148df-in-app_time_to_live.png",
        "Configure Time to Live for In-App Message",
        630
      ],
      "align": "center",
      "border": true,
      "caption": "Time to Live for a Message"
    }
  ]
}
[/block]


The TTL can range from 1 day to 365 days. The default value for TTL is two days. The message on the user's device stays for the specified TTL, after which it is automatically removed.

> 🚧 Choosing the Right TTL
> 
> You should choose a TTL that resonates with the purpose of your campaign. Some messages need to stay on the user's device for a longer period (coupon codes which are valid for a month) while some should last for a day or two (weekend discount offers).

# In-App Editor

Use the In-App editor to craft your In-app campaign with the desired messaging and styling best suited for your business. You can choose from a range of In-App templates. Alternatively, you can also use the Custom HTML option to build your own campaign.

The elements of the editor vary based on the type of template you select for creating your In-App campaign.

The following image represents the _Content with image notifications_ template editor. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6b590c3-in-app_editor.png",
        "Basic Editor",
        1206
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "In-App Editor for Content with Image notifications"
    }
  ]
}
[/block]


At a high level, the In-App editor has the following two primary sections: _Content_ and _Style_.

### Content

The Content section allows you to define your In-App message's overall text and visual content. Use this section to create engaging, and personalized In-App messages by entering enticing Title and Message. To [personalize](https://docs.clevertap.com/docs/personalize-message-inapp) the message, click the **Personalization (@)**  icon in the _Title_ and _Description_ fields.

Using the _Insert image_ option, you can upload the desired image to make your In-App campaign visually appealing when the app is in Portrait or Landscape mode.

You can choose to add the same image with different form factors or completely different images to give a unique experience on portrait and landscape.

Additionally, you can add up to two CTAs and configure their On Click Action as per your requirement. You can use the following three types of action buttons:

- Close notification: It closes the notification after a tap. 
- Open URL: A special type of CTA that enables the user to open a deep link for Android or iOS.
- Custom key-value pairs: The key-value pairs send back custom data when a user clicks the in-app button

You can also configure the number of days (or hours) to keep the In-App message on the user's device by setting the Message Time to Live field as per your use case. 

> 📘 Image Interstitial Template Exception
> 
> The elements of the In-App editor for the _Image only notifications_ templates are similar to those of the  _Content with Image notifications_ templates except for the _Title_ and _Message_ fields.

### Style

The Style section enables you to customize the appearance of your In-App message elements, such as title color, background color, message color, button text color, and so on. 

Customize the overall In-App message elements as per your brand style guidelines to make them visually appealing.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c9edbb1-In-App_Message.png",
        "Define Elements Style",
        963
      ],
      "align": "center",
      "border": true,
      "caption": "Style Elements from Editor"
    }
  ]
}
[/block]


> 🚧 Typeform and Character Limit
> 
> We do not currently support Typeform because its rendering requires access to local storage which is a security risk. CleverTap SDK WebView does not allow access to local storage.
> 
> The character limit for a message in English is 30 for the title and 128 for the message.  
> The character limit for a message in Chinese is 9 for the title and 38 for the message.