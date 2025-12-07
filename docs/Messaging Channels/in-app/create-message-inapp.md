---
title: Create Message
excerpt: Learn how to create an In-App campaign using the CleverTap dashboard.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Create a New Campaign

Create a campaign to deliver your message.  
To create a new campaign:

1. From the dashboard, select _Campaigns_.
2. Click **+ Campaign**.
3. From the _Messaging Channels_ list, select the messaging channel.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/96daa464ae4b7114af776e3f5e741695b014052420c51fe575bd1db744a6f9fd-Select_In-App_Campaign.png",
        "SCampaign Button Lists All Channels",
        2720
      ],
      "align": "center",
      "sizing": "smart",
      "border": true,
      "caption": "Select Messaging Channel"
    }
  ]
}
[/block]


The _Campaign_ page displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a805f56-Campaign_Creation_Page.jpg",
        "Expand Each Section",
        1404
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Create Campaign"
    }
  ]
}
[/block]


Define all the sections and publish the campaign. 

## Start Campaign Setup

The _Start here_ section displays the setup information. 

This section has the following parts:

- Set a goal: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. This selection is optional.

The campaign goal can be as generic or as specific as you want. It can answer questions from _How many users were influenced for purchasing an X amount?_ to _How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount?_ ". 

Define the conversion period by selecting the _Conversion Time_. You can define your conversion goal further by filtering an event by event properties.  For more information on event properties, see [Events](https://docs.clevertap.com/docs/events#event-properties). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4fbbeb2-Push_notification_set_goal_track_conversion.png",
        "Track Conversions",
        919
      ],
      "align": "center",
      "border": true,
      "caption": "Set a Goal"
    }
  ]
}
[/block]


## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the  _Target segment_ section. Here, you can create a new segment or use a previously saved user segment from the _segment_ list. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f1fee47-campaign_Who_Live_segment.png",
        "Define Target Audience",
        964
      ],
      "align": "center",
      "border": true,
      "caption": "Define Target Segment - Who"
    }
  ]
}
[/block]


> ❗️ Source Event Property
> 
> The CleverTap source event property is not supported for web pop-up and mobile in-app campaigns.

### Deliver Action Based Messages

You can trigger a message based on an action. Users receive messages when they perform an action in the app instead of waiting for the next app launch. It makes the messages more contextual and increases conversion. 

### Ad-hoc Segment

You can create an ad-hoc segment by specifying the live (ongoing) user behavior that will trigger the in-app message in real-time (e.g. App Launched). You can also segment your campaign to only reach users who meet specific criteria on the basis of past behavior and user properties. For example, you can trigger the in-app for only English-speaking female users who live in the United States.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3d4faa2-Filter_By_User_Properties.png",
        "Add Multiple User Properties",
        486
      ],
      "align": "center",
      "border": true,
      "caption": "Filter by User Properties"
    }
  ]
}
[/block]


### Saved Segment

You can also select a pre-defined Live user segment if you have already created one in the Segments dashboard and use it directly or further enrich it with additional filters in the campaign. Refer to [Live Segments](doc:segments#create-live-user-segments) to learn more.

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information, refer to [Control Groups](doc:control-groups).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/524abbf-control_group.png",
        "Control Group and Target Cap",
        "Control Group"
      ],
      "align": "center",
      "border": true,
      "caption": "Control Group"
    }
  ]
}
[/block]


## Define the Message Content

Now, you need to set up the _What_ section to define the campaign content, with four different options:

- Single Message
- AB Test
- Split Delivery
- By User Property
- Legacy 

Click _Go To Editor_ to create your message. 

### In-App Templates

Select the template and fill in the required details.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/73135a9-image_interstitial.png",
        "Select Template",
        2068
      ],
      "align": "center",
      "border": true,
      "caption": "In-App Template Types"
    }
  ]
}
[/block]


There are three types of templates available. 

### Basic Templates

These are templates available to you for creating a message. Select a template with or without images. 

#### Image only notifications

When selecting an _image only_ template, you can send a message which only contains an image (without CTAs and/or title and/or message).

#### Content with image notifications

When selecting a _With Content Notification_ template, you can send a message with a background image, title, message, and CTAs.

#### Template Aspect Ratio and File Size Guide

Follow this guide while creating in-app messages:

[block:parameters]
{
  "data": {
    "h-0": "Canvas Type",
    "h-1": "Canvas Aspect Ratio",
    "h-2": "Sample Image Sizes",
    "h-3": "Image Type Supported",
    "h-4": "Image Sample",
    "h-5": "Text Limit",
    "0-0": "Cover",
    "0-1": "Full Screen",
    "0-2": "Screen Resolution",
    "0-3": "Image",
    "0-4": "<ul>\n<li><a href=\"https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Cover-iPad.jpg\">Cover iPad</a></li>\n<li><a href=\"https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Cover.jpg\">Cover</a> </li>\n</ul>",
    "0-5": "",
    "1-0": "Interstitial",
    "1-1": "1.78:1",
    "1-2": "16:9",
    "1-3": "Image, gif, audio, video",
    "1-4": "<ul>\n<li><a href=\"https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Interstitial-iPad-Pro.jpg\">Interstitial iPad Pro</a></li>\n<li><a href=\"https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Interstitial-iPad.jpg\">Interstitial iPad</a></li>\n<li><a href=\"https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Intertitial.jpg\">Interstitial</a> </li>\n</ul>",
    "1-5": "Title :parameters]  \n{  \n, Message {  \n    \"h-0\": \"C",
    "2-0": "Half Interstitial",
    "2-1": "1.30:1",
    "2-2": "3:4",
    "2-3": "Image",
    "2-4": "<ul>\n<li><a href=\"https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Half-Interstitial-ipad-Pro.jpg\">Half Interstitial iPad Pro</a></li>\n<li><a href=\"https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Half-Interstitial-ipad.jpg\">Half Interstitial iPad</a></li>\n<li><a href=\"https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Half-Intertitial.jpg\">Half Interstitial</a> </li>\n</ul>",
    "2-5": "Title :parameters]  \n{  \n, Message {  \n    \"h-0\": \"Ca",
    "3-0": "Header",
    "3-1": "Height: 1:1  \nWidth: Fit to screen",
    "3-2": "N/A",
    "3-3": "Logo Image",
    "3-4": "Title :parameters]  \n{  \n, Message {  \n    \"h-0\": \"C\\* Title e\",  \n    \"h-1\": , Message pect Ratio\",  \n   Title : \"Sample Image, Message \\[75 Characters",
    "3-5": "",
    "4-0": "Footer",
    "4-1": "Height: 1:1  \nWidth: Fit to screen",
    "4-2": "N/A",
    "4-3": "Logo Image",
    "4-4": "",
    "4-5": "",
    "5-0": "Alert",
    "5-1": "Native",
    "5-2": "N/A",
    "5-3": "N/A",
    "5-4": "",
    "5-5": "",
    "6-0": "Image Only Cover",
    "6-1": "",
    "6-2": "",
    "6-3": "",
    "6-4": "",
    "6-5": "",
    "7-0": "Image Only Half Interstitial",
    "7-1": "",
    "7-2": "",
    "7-3": "",
    "7-4": "",
    "7-5": "",
    "8-0": "Image Only Interstitial",
    "8-1": "",
    "8-2": "",
    "8-3": "",
    "8-4": "",
    "8-5": ""
  },
  "cols": 6,
  "rows": 9,
  "align": [
    "left",
    "left",
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]


#### File Size

- Image: Less than 500 kb.
- Audio: Less than 5 Mb.
- Video: Less than 50 Mb.

#### Message Character Limit

| Language | Title | Message |
| :------- | :---- | :------ |
| English  | 30    | 128     |
| Chinese  | 9     | 38      |

> 📘 Image Cropping
> 
> Due to the multiple phone sizes on both Android and iOS, we will center crop images if the image does not fit the screen resolution.
> 
> We scale the image uniformly (maintaining the image's aspect ratio) so that both dimensions (width and height) of the image will be equal to or larger than the corresponding dimension of the phone (minus padding). The image is then centered in the view.

> 🚧 Video Messages
> 
> When adding video messages to In-App, ensure an audio track is available.  
> If required, insert a blank audio track to the video.

#### Ratings Template

Marketers can now create feedback-related popups for their mobile app users using the _Ratings Template._  
They can now create two types of rating templates for gaining feedback from their customers:

- User Rating Popup - It helps assess how happy your customers are with your services by taking feedback in the form of star ratings.
- NPS Popup - It enables you to measure the loyalty of your customers by distinguishing them in three categories - **Promoters**, **Passives**, **Detractors**.  One can view the NPS performance, navigate to the [NPS board](https://docs.clevertap.com/docs/nps-board) available under the _Boards_ section.

The images below represent a sample _User Rating Popup_ and _NPS popup_ in a mobile app.

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
      "sizing": "40% ",
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
      "sizing": "40% ",
      "border": true,
      "caption": "NPS Popup"
    }
  ]
}
[/block]


Marketers get the complete flexibility to explicitly define the rating scale, style, its shape (Star, Heart, Emojis), labels, and the overall content of the popup. One can also choose to add a comment box to get accurate user feedback/comments.

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


Besides, additional styling such as configuring the color for the message, question, background, and the rating scale is also possible from the editor as shown in the image above. The in-app notification text fields shown below can be personalized for every user based on specific user property or event property values. Refer to the Analysing [User Rating document](https://docs.clevertap.com/docs/user-ratings) to learn more about tracking and monitoring user rating data.

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


#### Follow-up Question Templates

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
> In the case of the User Ratings template, the _Notification Clicked_ event is raised that records the user's clicks on the CTA buttons and the Close button.

#### Lead Generation Template

We know that a significant number of App users may remain anonymous. This poses a challenge to continue engaging with potential customers after they leave your App. A lead generation template can solve this issue.

By integrating a lead generation form in your App, you can get important customer details such as name, email address, phone number, and so on. This information is helpful for further communication through channels such as SMS, Email, WhatsApp, and others. This post-visit communication not only helps to stay connected with your audience but also opens doors for future business opportunities. You can turn anonymous visitors into loyal customers with the CleverTap Lead Generation Template in your App.

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
      "caption": "Sample Lead Generation Template"
    }
  ]
}
[/block]


The following are the two types of Lead Generation templates:

- _Text_: Generate a text-only lead generation template to record user information. 
- _Image on Top_: Add an image on the top to the lead generation template. 

Create the content to record information from your users. The following image displays a preview of the form.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e53ae68-In-App_Template_Types_Lead_Gen_Templates.png",
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
      "border": true,
      "caption": "Card Orientation"
    }
  ]
}
[/block]


#### Custom Templates

You can use create in-app with custom HTML. Add more customization to the in-app messages with Javascript.  
Check that you select the _Include Javascript_ box to add custom Javascript. 

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


### Time to Live (TTL)

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


The TTL can range from 1 day to 60 days. The default value for TTL is two days. You can define the TTL for a maximum of 28 days. The message on the user's device stays there for the specified TTL, after which it is automatically removed. You can also have _Infinite TTL_, which means the message will never be deleted from the user's device. 

> 🚧 Choosing the Right TTL
> 
> You should choose a TTL that resonates with the purpose of your campaign. Some messages need to stay on the user's device for a longer period (coupon codes which are valid for a month) while some should last for a day or two (weekend discount offers).

### In-App Editor

The In-App Editor has two types of templates, that is, _Basic_ and _Custom_. You can use the _Basic_ template to create HTML in-apps via a drag-drop method. As an alternative, you can also use the _Custom HTML_ option to build your own campaign. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1b9254f-campaign_inapp_message_editor.png",
        "Basic Editor",
        1206
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "In-App Editor"
    }
  ]
}
[/block]


#### Compose

You can upload media from your image library or use personalized media to compose your messages. 

Enter the title, message, and upload or personalize media as required. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/752462f-in-app_compose.png",
        "Compose In-App Message",
        968
      ],
      "align": "center",
      "border": true,
      "caption": "Compose In-App In Editor"
    }
  ]
}
[/block]


You can use different types of call to actions (CTAs) to cater to different use cases.

 Choose from one of the following  actions (Optional):

  \*Close Notification: A click on this button closes the in-app message.  

- Open URL CTA: The user can open deep links for iOS or Android.
- Custom key-value pairs CTA: The key-value pairs send back custom data when a user clicks the _Native Display_ button. This data is not visible to the user. 

#### Style

Select the style for your notification such as background color, text color, and message color. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/82fe885-in-app_Style.png",
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


#### Action buttons

Mobile in-app enables various types of call-to-action (CTA) to cater to different use cases for clients, such as the following: 

- Close notification: It closes the notification after a tap. 
- Open URL: A special type of CTA that enables the user to open a deeplink for Android or iOS.
- Custom key-value pairs: The key-value pairs send back custom data when a user clicks the in-app button.

#### Select media

Some things to consider when selecting media with orientation: 

- Using the background option in in-app, you can choose the media you want your end-users to see when the app is in portrait and landscape mode.
- You can choose to add the same image with different form factors or completely different images to give a unique experience on portrait and landscape. 

To [personalize](https://docs.clevertap.com/docs/personalize-message-inapp) the message, click the **Personalization** icon in the editor. All the available personalization options for the channel display.

> 📘 Create Interactive In-Apps
> 
> You can create interactive in-app campaigns such as scratch card campaigns and swipe interaction campaigns using JavaScript.
> 
> Using the _Custom HTML_ option, you can use Javascript in the HTML and create deep interactive in-app campaigns by adding the JavaScript code along with the HTML code. 
> 
> JavaScript-based campaigns are available for versions 3.5.0 and above.

Enter all the necessary information to create a message. 

> 🚧 Typeform and Character Limit
> 
> We do not currently support Typeform because its rendering requires access to local storage which is a security risk. CleverTap SDK WebView does not allow access to local storage.
> 
> The character limit for a message in English is 30 for the title and 128 for the message.  
> The character limit for a message in Chinese is 9 for the title and 38 for the message.

### Preview & Test

Once you are all done setting up the content of your campaign in the _What_ section, you have the option to send a test notification to any CleverTap user profile you have marked as a _Test profile_  
Click the **Preview & Test** button from the message editor to test a message.

### Message Types

You can create the following types of messages:

- Single Message
- AB Test
- Split Delivery
- By User Property

### Single Message

In this campaign, we send the same message to all users who qualify as your target audience. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between properties such as language, geography, or any other user properties.

### A/B Testing

A/B testing helps you understand what type of message copy works best to get clicks from users.

You can test up to three message variants on a test group, and the variant that gets the most clicks is declared the winning variant and is automatically sent to the rest of your target audience.

When creating multiple variants for a campaign, you can also auto-copy what is already present in a current variant.

### Split Delivery

With split delivery, you can decide what percentage of your audience receives each message variant for the campaign duration.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/26bbd1f-app_inbox_split_delivery.png",
        "Control Variant Distribution",
        582
      ],
      "align": "center",
      "border": true,
      "caption": "Split Delivery Variant Distribution"
    }
  ]
}
[/block]


#### Split Delivery to Live User Segments

With campaigns sent to live user segments (triggered campaigns), messages are delivered immediately when a user's activity matches the criteria you have selected. For example, you can send a message when the user has completed a booking or purchase. Since it is not possible to determine the reach of triggered campaigns upfront, you need to decide how many total messages to send for A/B testing before a winner is declared.

> 👍 Triggered Campaign Example
> 
> If you select 500 users as your test audience, we will alternate delivery of Variant A and Variant B as users qualify for the campaign. After a total of messages are sent (Variant A – 250 and Variant B – 250), we then decide the winner based on the number of clicks and continue only with this winning message for the duration of the campaign.

Deciding on a test audience for A/B testing triggered campaigns requires some estimation. We recommend you check the total messages that were sent for similar triggered campaigns in the past to get a sense of how many users may qualify. If you select a test audience that is too small such as 25 users, you will get a statistically insignificant sample. If your test group size exceeds the total number of users who ultimately qualify for that campaign, then no winner will be declared, and each message variant will be alternatively delivered for the duration of the campaign.

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, you can use the + button to add multiple variants based on a user property value. In the example below, we have used the _Customer Type_ user property so users with different customer type property values will receive corresponding copies of the campaign based on their different levels (Silver, Gold, or Platinum).

### Legacy

Allows you to create and send a single campaign to users on both old and new versions of the application. 

Legacy message type is for customers whose entire audience has not updated their app to support the native in-app capability.

Post releasing the app update, there will be users on both old and new app versions. In this case, to send a campaign to both your user base, follow the below steps.

> 📘 Note
> 
> You will _not_ be able to use the A/B test and message on user property with this option.

Based on your SDK version, use one of the following steps to create in-app campaigns:

#### New Version (SDK 3.3.0 and Above)

To create In-App campaigns with the new version of the SDK:

1. Go to _Message Type_ > _Legacy_ and click **Go to Editor**.
2. Select _New In-app_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/99d8457-New_In-App_.png",
        "More Templates with New SDK",
        2938
      ],
      "align": "center",
      "border": true,
      "caption": "Templates for New SDK (3.3.0 and Above)"
    }
  ]
}
[/block]


3. Create your message and click **Save Draft**.

#### Legacy Version (SDK 3.2.0 and Below)

To create In-App campaigns with the older version of SDK:

1. Go to _Message Type_ > _Legacy_ and click **Go to Editor**.
2. Select _Legacy In-app_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a8118aa-Legacy_In-App.png",
        "Fewer Templates with Legacy SDK",
        2920
      ],
      "align": "center",
      "border": true,
      "caption": "Templates for Legacy SDK (3.2.0 and Below)"
    }
  ]
}
[/block]


3. Create your message and click **Save Draft**.

## Define the Campaign Schedule

The delivery preferences for Live campaigns can be set as follows:

- Start Date and Time
- End Date and Time
- Set Delay

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0637733-Campaign_When_Live_segment.png",
        "Campaign_When_Live_segment.png",
        "Schedule a Campaign "
      ],
      "align": "center",
      "caption": "Set Message Schedule "
    }
  ]
}
[/block]


### Delivery preferences

#### Set frequency

From the Delivery preferences section, select the days and the time frame to deliver the message.  
Click \_Apply to all \_to copy the choices from the selected day to all other days. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f4ad363-delivery_preferences.png",
        "Select Days and Frequency",
        1085
      ],
      "align": "center",
      "border": true,
      "caption": "Set Message Frequency"
    }
  ]
}
[/block]


## Publish Campaign

After testing and once you are satisfied with the appearance of your campaign, finalize your campaign with the following steps:

1. Click **Continue** to view your campaign summary. The overview page displays.
2. View your campaign summary, and then click **Publish Campaign**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b521e92-campaign_Publish.png",
        "Publish Final Campaign",
        1193
      ],
      "align": "center",
      "border": true,
      "caption": "Publish Campaign"
    }
  ]
}
[/block]