---
title: Create Message
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
  pages:
    - type: link
      title: Personalize Message
      url: https://docs.clevertap.com/docs/personalise-message
    - type: link
      title: Web Personalization Stats
      url: https://docs.clevertap.com/docs/web-personalisation-stats
---
## Create a New Campaign

Create a campaign to deliver your message.\
To create a new campaign:

1. From the dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **Personalization**. 

<Image title="WP1.png" alt={2846} width="80%" border={true} src="https://files.readme.io/56b72f9-WP1.png">
  Select Messaging Channel
</Image>

The campaign page displays.

<Image title="WP2.png" alt={2852} width="80%" border={true} src="https://files.readme.io/067aec5-WP2.png">
  Create Campaign
</Image>

Define all the sections and publish the campaign. 

## Start Campaign

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

<Image title="control group.png" alt={825} border={true} src="https://files.readme.io/99861e7-control_group.png">
  Control Group
</Image>

## Define the Message Content

Now, you need to set up the *What* section which is the campaign content, with four different options:

* Single Message
* AB Test
* Split Delivery
* By User Property

Click *Go To Editor* to create your message. 

### Web Personalization Templates

<Image title="WP3 templates.png" alt={1816} className="border" border={true} src="https://files.readme.io/25ed755-WP3_templates.png" />

#### Basic Templates

There are three basic templates that marketers can use for delivering engaging and personalized user experience:

* Custom key values
* Banner
* Banner Carousel

#### Custom Key Value

The custom key-value can have any value. 

For example, if you want to change the carousel images for your users based on their language and favorite food, you can set the custom key-value pairs for this change.

<Image title="Native_display_custom_key_value_pairs.png" alt={695} className="border" border={true} src="https://files.readme.io/7d13320-Native_display_custom_key_value_pairs.png" />

### Banner

Using the Banner template, marketers can create eye-catching personalized banners for delivering contextual and personalized engagement experiences for web users. Marketers can define the banner content (title, description, images), add a custom CTA, and also configure the styling for the respective banner from the editor. Refer to the image below for better clarity.

![1318](https://files.readme.io/f9b1054-wp_banner.png "wp banner.png")

The text in the *Title* and *Description* fields can be personalized using the '@' ( personalization based on user properties). For more information, refer to the Personalization document. Marketers also have an option to upload an image or define the URL of a hosted image. Additionally, they can also use separate images for mobile and desktop devices by defining them in the *Image* section

### Banner Carousel

The Banner Carousel template is a multi-slide template where you create up to five slides containing images with content. The carousel on the website displays as a sliding banner in the hero unit that can be scrolled to the left or right. It is a rich template that can be used for promoting a list of products or movies that will release this weekend. The gif below represents a sample carousel banner from Amazon.

Similar to the configurations of *Banner* template, marketers can define the content and appearance for the desired number of banner carousel slides. 

![1012](https://files.readme.io/d1de53f-wp_banner_carousel.png "wp banner carousel.png")

### Supported File Formats

The supported file formats include .jpg, .jpeg, .png, .gif (.png's convert to .jpeg using selected background color).

Following are the supported media types: 

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Template
      </th>

      <th>
        Template Category
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Custom key-value
      </td>

      <td>
        NA
      </td>
    </tr>

    <tr>
      <td>
        Banner
      </td>

      <td>
        Media (images, gif), text
      </td>
    </tr>

    <tr>
      <td>
        Banner Carousel
      </td>

      <td>
        Media (images, gif), text
      </td>
    </tr>
  </tbody>
</Table>

### Web Personalization Editor

The editor for *Web Personalization* is where you can define the content and appearance of your respective templates to engage your targeted audience. You can also define custom key values basis the target use case.

#### Compose

This section varies basis the template you choose. It allows you to define the content of the overall message for the campaigns.

#### Style

This section allows you to configure the look and appearance (such as background color, text color, and message color) for your web personalization campaigns.

### Preview & Test

Once you are all done setting up the content of your campaign in the *What* section, you have the option to send a test notification to any CleverTap user profile you have marked as a *Test profile*\
Click the **Preview & Test** button from the message editor to test a message.

## Message Types

You can create the following types of messages:

* Single Message
* AB Test
* Split Delivery
* By User Property

#### Single Message

In this campaign, we send the same message to all users who qualify as your target audience. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between properties such as language, geography, or any other user properties.

### A/B Testing

A/B testing helps you understand what type of message copy works best to get clicks from users.

You can test up to three message variants on a test group and the variant that gets the most clicks is declared the winning variant and is automatically sent to the rest of your target audience.

When you create multiple variants for a campaign, you can also auto-copy what is already present in a current variant.

### Split Delivery

With split delivery, you can decide what percentage of your audience receives each message variant for the duration of the campaign.

<Image title="campaign_split_delivery.png" alt={577} className="border" border={true} src="https://files.readme.io/73d579a-campaign_split_delivery.png" />

#### Split Delivery to Live User Segments

With campaigns sent to live user segments (triggered campaigns), messages are delivered immediately when a user’s activity matches the criteria you have selected. For example, you can send a message when the user has completed a booking or purchase. Since it is not possible to determine the reach of triggered campaigns upfront, you need to decide how many total messages to send for A/B testing before a winner is declared.

> 👍 Triggered Campaign Example
>
> If you select 500 users as your test audience, we will alternate delivery of Variant A and Variant B as users qualify for the campaign. After a total of messages are sent (Variant A – 250 and Variant B – 250), we then decide the winner based on the number of clicks and continue only with this winning message for the duration of the campaign.

Deciding on a test audience for A/B testing triggered campaigns requires some estimation. We recommend you check the total messages that were sent for similar triggered campaigns in the past to get a sense of how many users may qualify. If you select a test audience that is too small such as 25 users, you will get a statistically insignificant sample. If your test group size exceeds the total number of users who ultimately qualify for that campaign, then no winner will be declared and each message variant will be alternatively delivered for the duration of the campaign.

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, you can use the + button to add multiple variants based on a user property value. In the example below, we have used the *Customer Type* user property so users with different customer type property values will receive corresponding copies of the campaign based on their different levels (Silver, Gold, or Platinum). 

<Image title="user_properties_all.png" alt={486} className="border" border={true} src="https://files.readme.io/6db3703-user_properties_all.png" />

## Define the Campaign Schedule

The delivery preferences for Live campaigns can be set as follows:

* Start Date and Time
* End Date and Time
* Set Delay

<Image title="Campaign_When_Live_segment.png" alt={974} className="border" border={true} src="https://files.readme.io/0637733-Campaign_When_Live_segment.png" />

### Delivery preferences

#### Set frequency

From the Delivery preferences section, select the days and the time frame to deliver the message.\
Click *Apply to all* to copy the choices from the selected day to all other days. 

<Image title="delivery_preferences.png" alt={1085} className="border" border={true} src="https://files.readme.io/f4ad363-delivery_preferences.png" />

## Publish Campaign

After testing and once you are satisfied with the appearance of your campaign, finalize your campaign with the following steps:

1. Click **Continue** to view your campaign summary. The overview page displays.
2. View your campaign summary, then click **Publish Campaign**.

<Image title="campaign_Publish.png" alt={1193} className="border" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png" />
