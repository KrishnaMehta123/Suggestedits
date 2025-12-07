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
## Create a New Campaign

Create a campaign to deliver your message.\
To create a new campaign:

1. From the dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select the messaging channel.

<Image title="Select Messaging Channel.png" alt={2720} width="smart" border={true} src="https://files.readme.io/5647f75-Select_Messaging_Channel.png">
  Select Messaging Channel
</Image>

The *Campaign* page displays.

<Image title="Campaign_Creation_Page.jpg" alt={1404} width="80%" border={true} src="https://files.readme.io/a805f56-Campaign_Creation_Page.jpg">
  Create Campaign
</Image>

Define all the sections and publish the campaign. \`

## Start Campaign Setup

The *Start here* section displays the setup information. 

This section has the following parts:

* Set a goal: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. This selection is optional.

The campaign goal can be as generic or as specific as you want. It can answer questions from *How many users were influenced for purchasing an X amount?* to *How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount?* ". 

Define the conversion period by selecting the *Conversion Time*. You can define your conversion goal further by filtering an event by event properties.  For more information on event properties, see [Events](https://docs.clevertap.com/docs/events#event-properties). 

<Image title="Push_notification_set_goal_track_conversion.png" alt={919} border={true} src="https://files.readme.io/4fbbeb2-Push_notification_set_goal_track_conversion.png">
  Set a Goal
</Image>

## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the  *Target segment* section. Here, you can create a new segment or use a previously saved user segment from the *segment* list. 

<Image title="campaign_Who_Live_segment.png" alt={964} className="border" border={true} src="https://files.readme.io/f1fee47-campaign_Who_Live_segment.png" />

> ❗️ Source Event Property
>
> The CleverTap source event property is not supported for web pop-up and mobile in-app campaigns.

### Segment

If you want to create an ad-hoc segment, you can select a type of segment on which to base your campaign. You can create the target based on user properties or live (ongoing) user behavior. The latter is helpful to send out real-time, triggered campaigns.

### Deliver Action Based Messages

You can trigger a message based on an action. Users receive messages when they perform an action in the app instead of waiting for the next app launch. It makes the messages more contextual and increases conversion. Campaigns with delays and app inbox coupled with a push message do not trigger instant messages.

### Ad-hoc Segment

If you want to create an ad-hoc segment, you can select a type of segment on which to base your In-App campaign. You can create the target on the basis of user properties, or live (ongoing) user behavior (the latter is useful to send out real-time, triggered In-App campaigns).

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can send a push notification to English-speaking female users who live in the United States. 

<Image title="Filter By User Properties.png" alt={486} border={true} src="https://files.readme.io/3d4faa2-Filter_By_User_Properties.png">
  Filter by User Properties
</Image>

To know more about what segments can be used, see [Segments](doc:segments).

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information, refer to [Control Groups](doc:control-groups).

<Image title="Control_Group_Editor.png" alt={933} src="https://files.readme.io/0eacc15-Control_Group_Editor.png">
  Control Group
</Image>

## Define the Message Content

Now, you need to set up the *What* section to define the campaign content, with four different options:

* Single Message
* AB Test
* Split Delivery
* By User Property

Click *Go To Editor* to create your message. 

### In-App Templates

Select the template and fill in the required details.

<Image title="Inapp1.png" alt={2068} className="border" border={true} src="https://files.readme.io/5bada89-Inapp1.png" />

There are three types of templates available. 

### Basic Templates

These are templates available to you for creating a message. Select a template with or without images. 

#### Image only notifications

When selecting an *image only* template, you can send a message which only contains an image (without CTAs and/or title and/or message).

#### Content with image notifications

When selecting a *With Content Notification* template, you can send a message with a background image, title, message, and CTAs.

#### Template Aspect Ratio and File Size Guide

Follow this guide while creating in-app messages:

<Table align={["left","left","left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Canvas Type
      </th>

      <th>
        Canvas Aspect Ratio
      </th>

      <th>
        Sample Image Sizes
      </th>

      <th>
        Image Type Supported
      </th>

      <th>
        Image Sample
      </th>

      <th>
        Text Limit
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Cover
      </td>

      <td>
        Full Screen
      </td>

      <td>
        Screen Resolution
      </td>

      <td>
        Image
      </td>

      <td>
        * [Cover iPad](https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Cover-iPad.jpg)
        * [Cover](https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Cover.jpg) 
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Interstitial
      </td>

      <td>
        1.78:1
      </td>

      <td>
        16:9
      </td>

      <td>
        Image, gif, audio, video
      </td>

      <td>
        * [Interstitial iPad Pro](https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Interstitial-iPad-Pro.jpg)
        * [Interstitial iPad](https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Interstitial-iPad.jpg)
        * [Interstitial](https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Intertitial.jpg) 
      </td>

      <td>
        Title [20 Characters], Message [75 Characters]
      </td>
    </tr>

    <tr>
      <td>
        Half Interstitial
      </td>

      <td>
        1.30:1
      </td>

      <td>
        4:3
      </td>

      <td>
        Image
      </td>

      <td>
        * [Half Interstitial iPad Pro](https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Half-Interstitial-ipad-Pro.jpg)
        * [Half Interstitial iPad](https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Half-Interstitial-ipad.jpg)
        * [Half Interstitial](https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Half-Intertitial.jpg) 
      </td>

      <td>
        Title [25 Characters], Message [100 Characters]
      </td>
    </tr>

    <tr>
      <td>
        Header
      </td>

      <td>
        Height: 1:1\
        Width: Fit to screen
      </td>

      <td>
        N/A
      </td>

      <td>
        Logo Image
      </td>

      <td>
        Title [22 Characters], Message [75 Characters]\* 

        Title [30 Characters], Message [128 Characters]

        Title [22 Characters], Message \[75 Characters

        \<\<@harsh, got three of these from the FAQs. Which one is true ?>>
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Footer
      </td>

      <td>
        Height: 1:1\
        Width: Fit to screen
      </td>

      <td>
        N/A
      </td>

      <td>
        Logo Image
      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Alert
      </td>

      <td>
        Native
      </td>

      <td>
        N/A
      </td>

      <td>
        N/A
      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Image Only Cover
      </td>

      <td>
        {user["harsh to provide"]}
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Image Only Half Interstitial
      </td>

      <td>
        {user["harsh to provide"]}
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Image Only Interstitial
      </td>

      <td>
        {user["harsh to provide"]}
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>
  </tbody>
</Table>

#### File Size

* Image: Less than 500 kb.
* Audio: Less than 5 Mb.
* Video: Less than 50 Mb.

### Message Character Limit

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Language
      </th>

      <th>
        Title
      </th>

      <th>
        Message
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        English
      </td>

      <td>
        30
      </td>

      <td>
        128
      </td>
    </tr>

    <tr>
      <td>
        Chinese
      </td>

      <td>
        9
      </td>

      <td>
        38
      </td>
    </tr>
  </tbody>
</Table>

> 📘 Image Cropping
>
> Due to the multiple phone sizes on both Android and iOS, we will center crop images if the image does not fit the screen resolution.
>
> We scale the image uniformly (maintaining the image's aspect ratio) so that both dimensions (width and height) of the image will be equal to or larger than the corresponding dimension of the phone (minus padding). The image is then centered in the view.

### Ratings Template

Marketers can now create feedback-related popups for their mobile app users using the *Ratings Template.*\
They can now create two types of rating templates for gaining feedback from their customers:

* User Rating Popup - It helps assess how happy your customers are with your services by taking feedback in the form of star ratings.
* NPS Popup - It enables you to measure the loyalty of your customers by distinguishing them in three categories - **Promoters**, **Passives**, **Detractors**.  One can view the NPS performance, navigate to the [NPS board](https://docs.clevertap.com/docs/nps-board) available under the *Boards* section.

The images below represent a sample *User Rating Popup* and *NPS popup* in a mobile app.

<Image title="inapp.png" alt={568} width="smart" border={true} src="https://files.readme.io/cc3f275-inapp.png">
  User Ratings Popup
</Image>

<Image title="in-app nps.png" alt={542} width="smart" border={true} src="https://files.readme.io/3d18243-in-app_nps.png">
  NPS Popup
</Image>

Marketers get the complete flexibility to explicitly define the rating scale, style, its shape (Star, Heart, Emojis), labels, and the overall content of the popup. One can also choose to add a comment box to get accurate user feedback/comments.

<Image title="in app styles.png" alt={2044} className="border" border={true} src="https://files.readme.io/d76e790-in_app_styles.png" />

Besides, additional styling such as configuring the color for the message, question, background, and the rating scale is also possible from the editor as shown in the image above. The in-app notification text fields shown below can be personalized for every user based on specific user property or event property values. Refer to the Analysing [User Rating document](https://docs.clevertap.com/docs/user-ratings_c20) to learn more about tracking and monitoring user rating data.

<Image title="rate.png" alt={1694} className="border" border={true} src="https://files.readme.io/ae7f02c-rate.png" />

### Custom Templates

You can use create in-app with custom HTML. Add more customization to the in-app messages with Javascript.\
Check that you select the *Include Javascript* box to add custom Javascript. 

<Image title="in-app_journey_custom_HTML.png" alt={1108} className="border" border={true} src="https://files.readme.io/5638bd2-in-app_journey_custom_HTML.png" />

### Time to Live (TTL)

You can configure the number of days (or hours) to keep the message on the user's device by setting the *time to live*.

<Image title="in-app_time_to_live.png" alt={630} className="border" border={true} src="https://files.readme.io/35148df-in-app_time_to_live.png" />

The TTL can range from 1 day to 60 days. The default value for TTL is 2 days. You can define the TTL for a maximum of 28 days. The message on the user's device stays there for the specified TTL after which it is automatically removed. You can also have *Infinite TTL* which means the message will never be deleted from the user's device. 

> 🚧 Choosing the Right TTL
>
> You should choose a TTL that resonates with the purpose of your campaign. Some messages need to stay on the user's device for a longer period (coupon codes which are valid for a month) while some should last for a day or two (weekend discount offers).

\<\<@harsh to verify. TTL window has no validation>>

### In-App Editor

The In-App Editor has two types of templates, that is, *Basic* and *Custom*. You can use the *Basic* template to create HTML in-apps via a drag-drop method. As an alternative, you can also use the *Custom HTML* option to build your own campaign. 

<Image title="campaign_inapp_message_editor.png" alt={1206} className="border" width="80%" border={true} src="https://files.readme.io/1b9254f-campaign_inapp_message_editor.png" />

#### Compose

You can upload media from your image library or use personalized media to compose your messages. 

Enter the title, message, and upload or personalize media as required. 

<Image title="in-app_compose.png" alt={968} className="border" border={true} src="https://files.readme.io/752462f-in-app_compose.png" />

You can use different types of call to actions (CTAs) to cater to different use cases.

 Choose from one of the following  actions (Optional):

  \*Close Notification: A click on this button closes the in-app message.  

* Open URL CTA: The user can open deep links for iOS or Android.
* Custom key-value pairs CTA: The key-value pairs send back custom data when a user clicks the *Native Display* button. This data is not visible to the user. 

#### Style

Select the style for your notification such as background color, text color, and message color. 

<Image title="in-app_Style.png" alt={963} className="border" border={true} src="https://files.readme.io/82fe885-in-app_Style.png" />

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

> 📘 Create Interactive In-Apps
>
> You can create interactive in-app campaigns such as scratch card campaigns and swipe interaction campaigns using JavaScript.
>
> Using the *Custom HTML* option, you can use Javascript in the HTML and create deep interactive in-app campaigns by adding the JavaScript code along with the HTML code. 
>
> JavaScript-based campaigns are available for versions 3.5.0 and above.

Enter all the necessary information to create a message. 

> 🚧 Typeform and Character Limit
>
> We do not currently support Typeform because its rendering requires access to local storage which is a security risk. CleverTap SDK WebView does not allow access to local storage.
>
> The character limit for a message in English is 30 for the title and 128 for the message.\
> The character limit for a message in Chinese is 9 for the title and 38 for the message.

### Preview & Test

Once you are all done setting up the content of your campaign in the *What* section, you have the option to send a test notification to any CleverTap user profile you have marked as a *Test profile*\
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

### Split Delivery

With split delivery, you can decide what percentage of your audience receives each message variant for the campaign duration.

<Image title="app_inbox_split_delivery.png" alt={582} className="border" border={true} src="https://files.readme.io/26bbd1f-app_inbox_split_delivery.png" />

#### Split Delivery to Live User Segments

With campaigns sent to live user segments (triggered campaigns), messages are delivered immediately when a user's activity matches the criteria you have selected. For example, you can send a message when the user has completed a booking or purchase. Since it is not possible to determine the reach of triggered campaigns upfront, you need to decide how many total messages to send for A/B testing before a winner is declared.

> 👍 Triggered Campaign Example
>
> If you select 500 users as your test audience, we will alternate delivery of Variant A and Variant B as users qualify for the campaign. After a total of messages are sent (Variant A – 250 and Variant B – 250), we then decide the winner based on the number of clicks and continue only with this winning message for the duration of the campaign.

Deciding on a test audience for A/B testing triggered campaigns requires some estimation. We recommend you check the total messages that were sent for similar triggered campaigns in the past to get a sense of how many users may qualify. If you select a test audience that is too small such as 25 users, you will get a statistically insignificant sample. If your test group size exceeds the total number of users who ultimately qualify for that campaign, then no winner will be declared, and each message variant will be alternatively delivered for the duration of the campaign.

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, you can use the + button to add multiple variants based on a user property value. In the example below, we have used the *Customer Type* user property so users with different customer type property values will receive corresponding copies of the campaign based on their different levels (Silver, Gold, or Platinum).

## Define the Campaign Schedule

The delivery preferences for Live campaigns can be set as follows:

* Start Date and Time
* End Date and Time
* Set Delay

![974](https://files.readme.io/0637733-Campaign_When_Live_segment.png "Campaign_When_Live_segment.png")

### Delivery preferences

#### Set frequency

From the Delivery preferences section, select the days and the time frame to deliver the message.\
Click *Apply to all* to copy the choices from the selected day to all other days. 

<Image title="delivery_preferences.png" alt={1085} className="border" border={true} src="https://files.readme.io/f4ad363-delivery_preferences.png" />

## Publish Campaign

After testing and once you are satisfied with the appearance of your campaign, finalize your campaign with the following steps:

1. Click **Continue** to view your campaign summary. The overview page displays.
2. View your campaign summary, and then click **Publish Campaign**.

<Image title="campaign_Publish.png" alt={1193} className="border" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png" />
