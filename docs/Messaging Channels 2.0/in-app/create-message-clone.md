---
title: Create Message [CLONE]
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
[block:api-header]
{
  "title": "Create a New Campaign"
}
[/block]
Create a campaign to deliver your message. 
To create a new campaign:

1. From the dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select the messaging channel.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5647f75-Select_Messaging_Channel.png",
        "Select Messaging Channel.png",
        2720,
        1316,
        "#f7f7fa"
      ],
      "border": true,
      "sizing": "smart",
      "caption": "Select Messaging Channel"
    }
  ]
}
[/block]
The *Campaign* page displays.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a805f56-Campaign_Creation_Page.jpg",
        "Campaign_Creation_Page.jpg",
        1404,
        619,
        "#fbfafb"
      ],
      "border": true,
      "sizing": "80",
      "caption": "Create Campaign"
    }
  ]
}
[/block]
Define all the sections and publish the campaign. `

## Start Campaign Setup

The *Start here* section displays the setup information. 

This section has the following parts:

* Set a goal: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. This selection is optional.

The campaign goal can be as generic or as specific as you want. It can answer questions from *How many users were influenced for purchasing an X amount?* to *How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount?* ". 

Define the conversion period by selecting the *Conversion Time*. You can define your conversion goal further by filtering an event by event properties.  For more information on event properties, see [Events](https://docs.clevertap.com/docs/events#event-properties). 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4fbbeb2-Push_notification_set_goal_track_conversion.png",
        "Push_notification_set_goal_track_conversion.png",
        919,
        361,
        "#fafafc"
      ],
      "border": true,
      "caption": "Set a Goal"
    }
  ]
}
[/block]

## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the  *Target segment* section. Here, you can create a new segment or use a previously saved user segment from the *segment* list. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f1fee47-campaign_Who_Live_segment.png",
        "campaign_Who_Live_segment.png",
        964,
        439,
        "#f6f6fc"
      ],
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "danger",
  "body": "The CleverTap source event property is not supported for web pop-up and mobile in-app campaigns.",
  "title": "Source Event Property"
}
[/block]

### Segment
If you want to create an ad-hoc segment, you can select a type of segment on which to base your campaign. You can create the target based on user properties or live (ongoing) user behavior. The latter is helpful to send out real-time, triggered campaigns.

### Deliver Action Based Messages
You can trigger a message based on an action. Users receive messages when they perform an action in the app instead of waiting for the next app launch. It makes the messages more contextual and increases conversion. Campaigns with delays and app inbox coupled with a push message do not trigger instant messages.

### Ad-hoc Segment
If you want to create an ad-hoc segment, you can select a type of segment on which to base your In-App campaign. You can create the target on the basis of user properties, or live (ongoing) user behavior (the latter is useful to send out real-time, triggered In-App campaigns).

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can send a push notification to English-speaking female users who live in the United States. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3d4faa2-Filter_By_User_Properties.png",
        "Filter By User Properties.png",
        486,
        216,
        "#f6f8fc"
      ],
      "border": true,
      "caption": "Filter by User Properties"
    }
  ]
}
[/block]
To know more about what segments can be used, see [Segments](doc:segments).

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information, refer to [Control Groups](doc:control-groups).
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0eacc15-Control_Group_Editor.png",
        "Control_Group_Editor.png",
        933,
        549,
        "#fbfbfc"
      ],
      "caption": "Control Group"
    }
  ]
}
[/block]

## Define the Message Content

Now, you need to set up the *What* section to define the campaign content, with four different options:

  * Single Message
  * AB Test
  * Split Delivery
  * By User Property

Click *Go To Editor* to create your message. 


### In-App Templates 

Select the template and fill in the required details.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5bada89-Inapp1.png",
        "Inapp1.png",
        2068,
        1566,
        "#e6e3eb"
      ],
      "border": true
    }
  ]
}
[/block]
There are three types of templates available. 

### Basic Templates

These are templates available to you for creating a message. Select a template with or without images. 

#### Image only notifications 
When selecting an *image only* template, you can send a message which only contains an image (without CTAs and/or title and/or message).

#### Content with image notifications
When selecting a *With Content Notification* template, you can send a message with a background image, title, message, and CTAs.


#### Template Aspect Ratio and File Size Guide 

Follow this guide while creating in-app messages:
[block:parameters]
{
  "data": {
    "h-0": "Canvas Type",
    "h-1": "Canvas Aspect Ratio",
    "h-2": "Sample Image Sizes",
    "0-0": "Cover",
    "0-1": "Full Screen",
    "1-0": "Interstitial",
    "1-1": "1.78:1",
    "2-0": "Half Interstitial",
    "3-0": "Header",
    "4-0": "Footer",
    "5-0": "Alert",
    "3-1": "Height: 1:1\nWidth: Fit to screen",
    "4-1": "Height: 1:1\nWidth: Fit to screen",
    "5-1": "Native",
    "5-2": "N/A",
    "h-3": "Image Type Supported",
    "0-3": "Image",
    "1-3": "Image, gif, audio, video",
    "2-3": "Image",
    "3-3": "Logo Image",
    "4-3": "Logo Image",
    "5-3": "N/A",
    "3-2": "N/A",
    "0-2": "Screen Resolution",
    "2-1": "1.30:1",
    "1-2": "16:9",
    "2-2": "4:3",
    "4-2": "N/A",
    "6-0": "Image Only Cover",
    "7-0": "Image Only Half Interstitial",
    "8-0": "Image Only Interstitial",
    "6-1": "<<harsh to provide>>",
    "7-1": "<<harsh to provide>>",
    "8-1": "<<harsh to provide>>",
    "h-4": "Image Sample",
    "0-4": "  * [Cover iPad](https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Cover-iPad.jpg)\n  * [Cover](https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Cover.jpg) ",
    "2-4": "  *  [Half Interstitial iPad Pro](https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Half-Interstitial-ipad-Pro.jpg)\n  * [Half Interstitial iPad](https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Half-Interstitial-ipad.jpg)\n  * [Half Interstitial](https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Half-Intertitial.jpg) ",
    "1-4": "  * [Interstitial iPad Pro](https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Interstitial-iPad-Pro.jpg)\n  *  [Interstitial iPad](https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Interstitial-iPad.jpg)\n  *  [Interstitial](https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Intertitial.jpg) ",
    "h-5": "Text Limit",
    "3-4": "Title [22 Characters], Message [75 Characters]* \n\nTitle [30 Characters], Message [128 Characters]\n\nTitle [22 Characters], Message [75 Characters\n\n<<@harsh, got three of these from the FAQs. Which one is true ?>>",
    "2-5": "Title [25 Characters], Message [100 Characters]",
    "1-5": "Title [20 Characters], Message [75 Characters]"
  },
  "cols": 6,
  "rows": 9
}
[/block]
#### File Size
  * Image: Less than 500 kb.
  * Audio: Less than 5 Mb.
  * Video: Less than 50 Mb.

### Message Character Limit
[block:parameters]
{
  "data": {
    "h-1": "Title",
    "h-2": "Message",
    "h-0": "Language",
    "0-0": "English",
    "1-0": "Chinese",
    "1-1": "9",
    "1-2": "38",
    "0-1": "30",
    "0-2": "128"
  },
  "cols": 3,
  "rows": 2
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "Image Cropping",
  "body": "Due to the multiple phone sizes on both Android and iOS, we will center crop images if the image does not fit the screen resolution.\n\nWe scale the image uniformly (maintaining the image's aspect ratio) so that both dimensions (width and height) of the image will be equal to or larger than the corresponding dimension of the phone (minus padding). The image is then centered in the view."
}
[/block]
### Ratings Template

Marketers can now create feedback-related popups for their mobile app users using the *Ratings Template.*
They can now create two types of rating templates for gaining feedback from their customers:

* User Rating Popup - It helps assess how happy your customers are with your services by taking feedback in the form of star ratings.
* NPS Popup - It enables you to measure the loyalty of your customers by distinguishing them in three categories - **Promoters**, **Passives**, **Detractors**.  One can view the NPS performance, navigate to the [NPS board](https://docs.clevertap.com/docs/nps-board) available under the *Boards* section.

The images below represent a sample *User Rating Popup* and *NPS popup* in a mobile app.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cc3f275-inapp.png",
        "inapp.png",
        568,
        1150,
        "#454345"
      ],
      "border": true,
      "sizing": "smart",
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
        "in-app nps.png",
        542,
        1096,
        "#474547"
      ],
      "sizing": "smart",
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
        "in app styles.png",
        2044,
        1398,
        "#e9e3ed"
      ],
      "border": true
    }
  ]
}
[/block]
Besides, additional styling such as configuring the color for the message, question, background, and the rating scale is also possible from the editor as shown in the image above. The in-app notification text fields shown below can be personalized for every user based on specific user property or event property values. Refer to the Analysing [User Rating document](https://docs.clevertap.com/docs/user-ratings_c20) to learn more about tracking and monitoring user rating data.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ae7f02c-rate.png",
        "rate.png",
        1694,
        1404,
        "#efecf6"
      ],
      "border": true
    }
  ]
}
[/block]
### Custom Templates

You can use create in-app with custom HTML. Add more customization to the in-app messages with Javascript. 
Check that you select the *Include Javascript* box to add custom Javascript. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5638bd2-in-app_journey_custom_HTML.png",
        "in-app_journey_custom_HTML.png",
        1108,
        1252,
        "#f2eef5"
      ],
      "border": true
    }
  ]
}
[/block]
### Time to Live (TTL)

You can configure the number of days (or hours) to keep the message on the user's device by setting the *time to live*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/35148df-in-app_time_to_live.png",
        "in-app_time_to_live.png",
        630,
        198,
        "#fafbfc"
      ],
      "border": true
    }
  ]
}
[/block]
The TTL can range from 1 day to 60 days. The default value for TTL is 2 days. You can define the TTL for a maximum of 28 days. The message on the user's device stays there for the specified TTL after which it is automatically removed. You can also have *Infinite TTL* which means the message will never be deleted from the user's device. 
[block:callout]
{
  "type": "warning",
  "title": "Choosing the Right TTL",
  "body": "You should choose a TTL that resonates with the purpose of your campaign. Some messages need to stay on the user's device for a longer period (coupon codes which are valid for a month) while some should last for a day or two (weekend discount offers)."
}
[/block]
<<@harsh to verify. TTL window has no validation>>

### In-App Editor

The In-App Editor has two types of templates, that is, *Basic* and *Custom*. You can use the *Basic* template to create HTML in-apps via a drag-drop method. As an alternative, you can also use the *Custom HTML* option to build your own campaign. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1b9254f-campaign_inapp_message_editor.png",
        "campaign_inapp_message_editor.png",
        1206,
        2017,
        "#f4f2f8"
      ],
      "sizing": "80",
      "border": true
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
        "in-app_compose.png",
        968,
        674,
        "#d8d1dc"
      ],
      "border": true
    }
  ]
}
[/block]
You can use different types of call to actions (CTAs) to cater to different use cases.

 Choose from one of the following  actions (Optional):

  *Close Notification: A click on this button closes the in-app message.  
  * Open URL CTA: The user can open deep links for iOS or Android.
  * Custom key-value pairs CTA: The key-value pairs send back custom data when a user clicks the *Native Display* button. This data is not visible to the user. 


#### Style

Select the style for your notification such as background color, text color, and message color. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/82fe885-in-app_Style.png",
        "in-app_Style.png",
        963,
        668,
        "#d8d2dc"
      ],
      "border": true
    }
  ]
}
[/block]
#### Action buttons 
Mobile in-app enables various types of call-to-action (CTA) to cater to different use cases for clients, such as the following: 

  * Close notification: It closes the notification after a tap. 
  * Open URL: A special type of CTA that enables the user to open a deeplink for Android or iOS.
  * Custom key-value pairs: The key-value pairs send back custom data when a user clicks the in-app button.

#### Select media 
Some things to consider when selecting media with orientation: 

  * Using the background option in in-app, you can choose the media you want your end-users to see when the app is in portrait and landscape mode.
  * You can choose to add the same image with different form factors or completely different images to give a unique experience on portrait and landscape. 

To [personalize](https://docs.clevertap.com/docs/personalize-message-inapp) the message, click the **Personalization** icon in the editor. All the available personalization options for the channel display.
[block:callout]
{
  "type": "info",
  "title": "Create Interactive In-Apps",
  "body": "You can create interactive in-app campaigns such as scratch card campaigns and swipe interaction campaigns using JavaScript.\n\nUsing the *Custom HTML* option, you can use Javascript in the HTML and create deep interactive in-app campaigns by adding the JavaScript code along with the HTML code. \n\nJavaScript-based campaigns are available for versions 3.5.0 and above."
}
[/block]
Enter all the necessary information to create a message. 
[block:callout]
{
  "type": "warning",
  "body": "We do not currently support Typeform because its rendering requires access to local storage which is a security risk. CleverTap SDK WebView does not allow access to local storage.\n\nThe character limit for a message in English is 30 for the title and 128 for the message. \nThe character limit for a message in Chinese is 9 for the title and 38 for the message.",
  "title": "Typeform and Character Limit"
}
[/block]
### Preview & Test

Once you are all done setting up the content of your campaign in the *What* section, you have the option to send a test notification to any CleverTap user profile you have marked as a *Test profile* 
Click the **Preview & Test** button from the message editor to test a message.


### Message Types 
You can create the following types of messages:

  * Single Message
  * AB Test
  * Split Delivery
  * By User Property

### Single Message
In this campaign, we send the same message to all users who qualify as your target audience. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between properties such as language, geography, or any other user properties.


### A/B Testing
A/B testing helps you understand what type of message copy works best to get clicks from users.

You can test up to three message variants on a test group, and the variant that gets the most clicks is declared the winning variant and is automatically sent to the rest of your target audience.

When creating multiple variants for a campaign, you can also auto-copy what is already present in a current variant.


###Split Delivery
With split delivery, you can decide what percentage of your audience receives each message variant for the campaign duration.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/26bbd1f-app_inbox_split_delivery.png",
        "app_inbox_split_delivery.png",
        582,
        588,
        "#fafbfb"
      ],
      "border": true
    }
  ]
}
[/block]

#### Split Delivery to Live User Segments 

With campaigns sent to live user segments (triggered campaigns), messages are delivered immediately when a user's activity matches the criteria you have selected. For example, you can send a message when the user has completed a booking or purchase. Since it is not possible to determine the reach of triggered campaigns upfront, you need to decide how many total messages to send for A/B testing before a winner is declared.
[block:callout]
{
  "type": "success",
  "body": "If you select 500 users as your test audience, we will alternate delivery of Variant A and Variant B as users qualify for the campaign. After a total of messages are sent (Variant A – 250 and Variant B – 250), we then decide the winner based on the number of clicks and continue only with this winning message for the duration of the campaign.",
  "title": "Triggered Campaign Example"
}
[/block]
Deciding on a test audience for A/B testing triggered campaigns requires some estimation. We recommend you check the total messages that were sent for similar triggered campaigns in the past to get a sense of how many users may qualify. If you select a test audience that is too small such as 25 users, you will get a statistically insignificant sample. If your test group size exceeds the total number of users who ultimately qualify for that campaign, then no winner will be declared, and each message variant will be alternatively delivered for the duration of the campaign.

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, you can use the + button to add multiple variants based on a user property value. In the example below, we have used the *Customer Type* user property so users with different customer type property values will receive corresponding copies of the campaign based on their different levels (Silver, Gold, or Platinum).

## Define the Campaign Schedule 

The delivery preferences for Live campaigns can be set as follows:
  * Start Date and Time
  * End Date and Time
  * Set Delay

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0637733-Campaign_When_Live_segment.png",
        "Campaign_When_Live_segment.png",
        974,
        476,
        "#faf9f7"
      ]
    }
  ]
}
[/block]

###Delivery preferences

#### Set frequency 
From the Delivery preferences section, select the days and the time frame to deliver the message. 
Click *Apply to all *to copy the choices from the selected day to all other days. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f4ad363-delivery_preferences.png",
        "delivery_preferences.png",
        1085,
        752,
        "#f7f8fc"
      ],
      "border": true
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
        "campaign_Publish.png",
        1193,
        356,
        "#f0f0fc"
      ],
      "border": true
    }
  ]
}
[/block]