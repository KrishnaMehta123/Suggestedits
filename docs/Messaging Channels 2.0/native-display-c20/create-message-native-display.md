---
title: Create Message
excerpt: Understand how to create a native display message.
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
      title: Native Display Personalize Message
      url: https://docs.clevertap.com/docs/personalize-message-native-display
    - type: link
      title: Native Display Campaign Stats
      url: https://docs.clevertap.com/docs/native-display-campaign-stats
---
## Create a New Campaign

Create a campaign to deliver your message.\
To create a new campaign:

1. From the dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select the messaging channel. 

<Image title="Select_all_channel.png" alt={1360} width="80%" border={true} src="https://files.readme.io/11e04b4-Select_all_channel.png">
  Select Messaging Channel
</Image>

The campaign page displays.

<Image title="Campaign_Creation_Page.jpg" alt={1404} width="80%" border={true} src="https://files.readme.io/a805f56-Campaign_Creation_Page.jpg">
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

<Image title="Control_Group_Editor.png" alt={933} border={true} src="https://files.readme.io/0eacc15-Control_Group_Editor.png">
  Control Group
</Image>

## Define the Message Content

Now, you can set up the *What* which is the campaign content, with four different options:

* Single Message
* AB Test
* Split Delivery
* By User Property

Click *Go To Editor* to create your message. 

### Native Display Templates

<Image title="native_display_templates.png" alt={876} className="border" border={true} src="https://files.readme.io/d88c7c0-native_display_templates.png" />

You have the following types of message templates:

#### Content with image notifications

1. Simple Message \`
2. Carousel Message
3. Message with icon
4. Custom key-value

#### Image only notifications

1. Carousel Message 

#### Simple Message

A simple message consists of the following elements:\
(a) Title.\
(b) Message.\
(c) Media (optional): jpg, gif, mp4 video, and mp3 formats are supported.\
(d) Call to action (optional\
(e) Custom key-value pairs

#### Carousel Message with Content

This template is a multi-slide template where you can draft up to five slides containing images with content. The carousel in the user app displays in the form of right and left scrolls. This is a rich template that can be used to promote a list of products or movies that will release this weekend.

#### Carousel Message without Content (Image Only)

This template is similar to the *Carousel Message with Content* template but without a title, text, and messages. 

#### Message with Icon

This template is similar to the *Simple Message* template with the extra ability to include an additional icon placeholder.

#### Custom Key Value

The custom key-value can have any value. 

For example, if you want to change the carousel images for your users based on their language and favorite food, you can set the custom key-value pairs for this change.

<Image title="Native_display_custom_key_value_pairs.png" alt={695} className="border" border={true} src="https://files.readme.io/7d13320-Native_display_custom_key_value_pairs.png" />

### Supported File Formats

The supported file formats include .jpg, .jpeg, .png, .gif, .mp3, .mp4 (.png's convert to .jpeg using selected background color).

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
        Simple Message
      </td>

      <td>
        Media (images, gif, video) only
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        Media (images, gif, video) + Text
      </td>
    </tr>

    <tr>
      <td>
        Carousel Message
      </td>

      <td>
        Media (images, gif) only
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        Media (images, gif) + Text
      </td>
    </tr>

    <tr>
      <td>
        Message with icon
      </td>

      <td>
        Media (images, gif, video) only
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        Media (images, gif, video) + Text
      </td>
    </tr>

    <tr>
      <td>
        Custom key value
      </td>

      <td>
        Any
      </td>
    </tr>
  </tbody>
</Table>

### Native Display Editor

The message builder for *Native Display* is where you can create a rich message to engage your targeted audience.

Enter your text and message.

<Image title="Native_display_editor.png" alt={1201} className="border" width="80%" border={true} src="https://files.readme.io/bf40671-Native_display_editor.png" />

#### Compose

You can upload media from your image library or use personalized media to compose your messages. 

Enter the title, message, and upload or personalize media as required. 

*Native Display* enables various types of call to action (CTA) to cater to different use cases.

 Choose from one of the following  actions (Optional):

  \*On-message CTA URL: A click on this URL opens a deep link when you click anywhere on the message (text or image or both).

* Open URL CTA: The user can open deep links for iOS or Android. 
* Custom key-value pairs CTA: The key-value pairs send back custom data when a user clicks the *Native Display* button. This data is not visible to the user. 

#### Style

Select the style for your notification such as background color, text color, and message color. 

### Preview & Test

Once you are all done setting up the content of your campaign in the *What* section, you have the option to send a test notification to any CleverTap user profile you have marked as a *Test profile*\
Click the **Preview & Test** button from the message editor to test a message.

### Message Types

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
