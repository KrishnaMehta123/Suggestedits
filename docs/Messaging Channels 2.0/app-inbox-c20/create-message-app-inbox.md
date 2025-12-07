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
      title: App Inbox Personalize Message
      url: https://docs.clevertap.com/docs/personalize-message-app-inbox
    - type: link
      title: App Inbox Stats
      url: https://docs.clevertap.com/docs/app-inbox-stats
    - type: link
      title: App Inbox Troubleshooting
      url: https://docs.clevertap.com/docs/troubleshooting-app-inbox
---
Get started with creating an app inbox message by using the following steps:

## Create a New Campaign

Create a campaign to deliver your message.\
To create a new campaign:

1. From the dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select the messaging channel.

<Image title="Select Messaging Channel.png" alt={2720} width="smart" border={true} src="https://files.readme.io/5647f75-Select_Messaging_Channel.png">
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

* Qualification criteria: Deliver the notification by Past Behavior, Custom List, or Live behavior. For more information about segmenting users, refer to [Segments](https://docs.clevertap.com/docs/segments).
* Set a goal: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. This selection is optional.

The campaign goal can be as generic or as specific as you want. It can answer questions from *How many users were influenced for purchasing an X amount?* to *How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount?* ". 

Define the conversion period by selecting the *Conversion Time*. You can define your conversion goal further by filtering an event by event properties.  For more information on event properties, see [Events](doc:events). 

<Image title="Push_notification_set_goal_track_conversion.png" alt={919} border={true} src="https://files.readme.io/4fbbeb2-Push_notification_set_goal_track_conversion.png">
  Set a Goal
</Image>

## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the  *Target segment* section. Here, you can create a new segment or use a previously saved user segment from the *segment* list. 

For Past Behavior segments, you also calculate the estimated reach. 

<Image title="Push_notification_editor_Who.png" alt={1168} width="80%" border={true} src="https://files.readme.io/030202d-Push_notification_editor_Who.png">
  Define - Who
</Image>

### Segment

If you want to create an ad-hoc segment, you can select a type of segment on which to base your campaign. You can create the target based on past user behavior and user properties or live (ongoing) user behavior. The latter is helpful to send out real-time, triggered campaigns.

For instance, you can create a live *Inaction within time* campaign that targets users as soon as they add a product to their cart but do not finish transacting within 10 minutes.

On this basis, you would then set up the *Who* by sending this campaign to all users who qualify or limit the users who qualify under *Estimated reach*. 

### Deliver Action Based Messages

You can trigger a message based on an action. Users receive messages when they perform an action in the app instead of waiting for the next app launch. It makes the messages more contextual and increases conversion. Campaigns with delays and app inbox coupled with a push message do not trigger instant messages.

### Deliver Messages based on Past Behavior (PBS)

You can also target users basis their past behavior. For past behavior campaigns, you also have an option to calculate estimated reach to view how many:

* Number of users that qualify for the campaign criteria.
* Number of users that are reachable via mobile push as of now.

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can send a push notification to English-speaking female users who live in the United States. 

<Image title="user_properties_all.png" alt={486} border={true} src="https://files.readme.io/cbc719c-user_properties_all.png">
  Filter by User Properties
</Image>

The following table explains the various property types:

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Property Type
      </th>

      <th>
        Description
      </th>

      <th>
        Example
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        User Properties
      </td>

      <td>
        Custom [user profile properties](https://docs.clevertap.com/docs/user-profiles#section-user-profile-data-model) that you define and send to CleverTap.
      </td>

      <td>
        Customer Type = Platinum
      </td>
    </tr>

    <tr>
      <td>
        Demographics
      </td>

      <td>
        Demographics filters include *Age* and *Gender*.
      </td>

      <td>
        Age = 25 to 40 years\
        Gender = Female
      </td>
    </tr>

    <tr>
      <td>
        Geography
      </td>

      <td>
        User's coarse location. Filters include *Country*, *Region*, and *City*. CleverTap's SDK can automatically detect this from the user's IP address.
      </td>

      <td>
        Country = United States\
        State = California\
        City = San Francisco
      </td>
    </tr>

    <tr>
      <td>
        Geography Radius
      </td>

      <td>
        User's exact location. You can select a city, and then define the target radius. You can also select multiple cities. You can send this information using CleverTap's SDK. For more information, refer to the [iOS](https://developer.clevertap.com/docs/ios#section-send-location-information-to-clevertap) and [Android](https://developer.clevertap.com/docs/android#section-manually-updating-user-location) developer guides.
      </td>

      <td>
        Locations = San Francisco, USA; Paris, France
      </td>
    </tr>

    <tr>
      <td>
        Reachability
      </td>

      <td>
        Reachability filters include *Has email address*, *Has phone number*, *Unsubscribed email*, and *Unsubscribed SMS*.
      </td>

      <td>
        Unsubscribed email = No
      </td>
    </tr>

    <tr>
      <td>
        App Fields
      </td>

      <td>
        App fields filters include *App Version*, *Device Make*, *Device Model*, *OS Version*, and CleverTap *SDK Version*. This information is sent by CleverTap's SDK for each device that has your app which means a single user can have multiple devices associated with their user profile.
      </td>

      <td>
        OS Version = 10
      </td>
    </tr>
  </tbody>
</Table>

To know more about what segments can be used, see [Segments](doc:segments).

### Constant event property

You can also hold a property constant across the selected events.  For more information, see [Constant Event Property](doc:constant-property).

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information, refer to [Control Groups](doc:control-groups).

<Image title="Control_Group_Editor.png" alt={933} border={true} src="https://files.readme.io/0eacc15-Control_Group_Editor.png">
  Control Group
</Image>

### Targeting Cap

You can limit the number of users receiving the message. 

A relevant use case is a limited offer where you want to distribute a fixed number of coupon codes. If the total reach for your campaign exceeds the number of coupon codes you can distribute, then you can limit the number of users who will receive the message to precisely the number of coupons you want to distribute.

<Image title="Target_Cap.jpg" alt={835} border={true} src="https://files.readme.io/20d412f-Target_Cap.jpg">
  Target Cap
</Image>

## Define the Message Content

Now, you can set up the *What* which is the campaign content with four different options:

* Single Message
* AB Test
* Split Delivery
* By User Property

Click *Go To Editor* to create your message. 

### App Inbox Templates

You have the following four choices of message templates to create your message:

<Image title="App_Inbox_templates.png" alt={807} className="border" border={true} src="https://files.readme.io/63a8c31-App_Inbox_templates.png" />

#### Simple Message

A simple message consists of the following elements:\
(a) Title.\
(b) Message.\
(c) Media (optional): jpg, gif, mp4 video, and mp3 formats are supported.\
(c) Call to action (optional).

For example, the user receives the app inbox message stating "Your order has been accepted by the restaurant after placing an order. 

<Image title="app_inbox_simple_message.png" alt={232} className="border" width="smart" border={true} src="https://files.readme.io/6ee6624-app_inbox_simple_message.png" />

#### Carousel Message with Content

This is a multi-slide template where you can draft up to five slides containing images with content. The carousel in the user app displays in the form of right and left scrolls. This is a rich template that can be used in situations such as, promoting a list of products or movies that will release this weekend.\
You can also add a link for each carousel message to navigate the users to that particular page. 

<Image title="app_inbox_carousel-1.png" alt={222} width="smart" border={true} src="https://files.readme.io/cc1b308-app_inbox_carousel-1.png">
  First Carousel Image
</Image>

<Image title="app_inbox_carousel-2.png" alt={226} width="smart" border={true} src="https://files.readme.io/52b3d81-app_inbox_carousel-2.png">
  Second Carousel Image
</Image>

For example, along with the advertising images, you can add the related headline in the message content along and use personalization in these messages.

#### Carousel Message without Content

This template is similar to the one right above but without a title text and messages. Carousel messages without content can be made in an attractive way that can grab the user's attention and also convey your purpose for the campaign. You can add promotional campaign creatives about your products as an image here without any text message. 

#### Message with Icon

This template is similar to the simple message with the extra ability to include an additional icon placeholder. You can just add a single image in the given format along with any personalized or generic title and text that you would like to send to the users. 

<Image title="message_with_icon.png" alt={245} className="border" border={true} src="https://files.readme.io/6a9e5c2-message_with_icon.png" />

### App Inbox Editor

The message builder for *App Inbox* is where you can create a rich message to engage your targeted audience.

Enter your text and message.

<Image title="App_Inbox_editor_create_message.png" alt={1205} className="border" width="80%" border={true} src="https://files.readme.io/18bc49e-App_Inbox_editor_create_message.png" />

#### Call to Action

*App Inbox* enables various types of call to action (CTA) to cater to different use cases for the client.

 Choose from one of the following five types (Optional):

* Click-on-message CTA: This opens a deep link when you click anywhere on the message (text or image or both).
* Click-on-link CTA: You can add additional, colored links at the bottom of your message to attract the user's attention. 
* Copy to clipboard CTA: The user can copy text to their clipboard such as, copying discount codes to your products and applying them at the time of checkout.
* Open URL CTA: The user can open deep links for iOS or Android.
* Custom key-value pairs CTA: The key-value pairs send back custom data when a user clicks the *App Inbox* button. This data is not visible to the user. This feature is available for apps that use Clevertap Android SDK version 3.6.1 or above and iOS SDK version 3.7.1 or above. 

<Image title="App_Inbox_editor_call_to_action.png" alt={681} className="border" width="80%" border={true} src="https://files.readme.io/3f0fd39-App_Inbox_editor_call_to_action.png" />

#### Message Tags

You can tag an inbox message with one or more comma-separated strings (Optional). 

These tags help you identify the messages inside the user's device. Also, these tags help you classify your messages into different tabs in your app.

<Image title="App_Inbox_editor_message_tags.png" alt={678} className="border" border={true} src="https://files.readme.io/19799ac-App_Inbox_editor_message_tags.png" />

> 📘 Using Message Tags
>
> Message tags are an excellent way to engage your users contextually. For example, some of your app users might be interested in offers while others in news updates. You can have two separate tabs to categorize your inbox messages into those two buckets. Note that it is not compulsory to have tabs.
>
> You can define the names of the inbox tabs during the configuration of *App Inbox* with your app. The same names should be entered as tags. In case you do not specify any tag, the message will go into the default bucket *All*.

### Time to Live (TTL)

*App Inbox* campaigns are by design persisted on the user device for a number of days. 

1. You can configure the number of days (or hours) to keep the message on the user's device by setting the *time to live*.

<Image title="Campaigns_message_time_to_live.png" alt={710} className="border" border={true} src="https://files.readme.io/bbd5393-Campaigns_message_time_to_live.png" />

The TTL can range from 1 day to 60 days. The default value for TTL is 2 days. You can define the TTL for a maximum of 28 days. The message on the user's device stays there for the specified TTL after which it is automatically removed. You can also have *Infinite TTL* which means the message will never be deleted from the user's device. 

> 🚧 Choosing the Right TTL
>
> You should choose a TTL that resonates with the purpose of your campaign. Some messages need to stay on the user's device for a longer period (coupon codes which are valid for a month) while some should last for a day or two (weekend discount offers).

> 📘 How a Message is Accounted For
>
> Each message stored on the CleverTap platform for *App Inbox* is accounted for as a user event.

### Supported Media Types

The supported media types include:

<Table align={["left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Media Type
      </th>

      <th>
        16:9 Aspect Ratio
      </th>

      <th>
        1:1 Aspect Ratio
      </th>

      <th>
        Max Size
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Image (jpg, png, gif)
      </td>

      <td>
        Yes
      </td>

      <td>
        Yes
      </td>

      <td>
        500 KB
      </td>
    </tr>

    <tr>
      <td>
        Video (mp4)
      </td>

      <td>
        Yes
      </td>

      <td>
        Yes
      </td>

      <td>
        50 MB
      </td>
    </tr>

    <tr>
      <td>
        Audio (mp3)
      </td>

      <td>
        N/A
      </td>

      <td>
        N/A
      </td>

      <td>
        5 MB
      </td>
    </tr>
  </tbody>
</Table>

### Preview & Test

Once you are all done setting up the content of your campaign in the *What* section, you have the option to send a test notification to any CleverTap user profile you have marked as a *Test profile*\
Click the **Preview & Test** button from the message editor to test a message.

### Message Types

You can create the following types of messages:

* Single Message
* A/B Test 
* Split Delivery
* By User Property

### Single Message

In this campaign, we send the same message to all users who qualify as your target audience. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between language, geography, or any other user properties.

### A/B Testing

A/B testing helps you understand what type of message copy works best to get clicks from users.

You can test up to three message variants on a test group, and the variant that gets the most clicks is declared the winning variant and is automatically sent to the rest of your target audience.

When creating multiple variants for a campaign, you can also auto-copy what is already present in a current variant.

### Split Delivery

With split delivery, you can decide what percentage of your audience receives each message variant for the campaign duration.

<Image title="Push_notification_split_delivery.png" alt={992} className="border" border={true} src="https://files.readme.io/890fc40-Push_notification_split_delivery.png" />

#### Split Delivery to Past Behavior Segments

For campaigns sent to *Past Behavior Segments* (grouping of users based on what they have done in the past), you have two options: launch the A/B test to a percentage of your target audience or send out an absolute number of messages. In either case, we deliver the variants equally to the test audience.

For example:

* If you are testing three messages (e.g., Variant A, Variant B, Variant C).
* Your campaign reach is 2,000,000 users.
* You choose a test population of 15% of campaign reach (300,000 users).

Then, we send:

* Variant A to 100,000 users.
* Variant B to 100,000 users.
* Variant C to 100,000 users.

After all 300,000 messages have been delivered, we calculate the winning message over this test group based on the number of click-throughs. We then automatically send the winning message to the remainder of your target audience which is 1,700,000 users in this example.

Note that for A/B testing, we ensure there is always an equal number of messages sent for each variant, so there is no bias introduced during the test phase and that the best-performing message is always declared the winner.

#### Split Delivery to Live User Segments

With campaigns sent to live user segments (triggered campaigns), messages are delivered immediately when a user’s activity matches the criteria you have selected. For example, you can send a message when the user has completed a booking or purchase. Since it is not possible to determine the reach of triggered campaigns upfront, you need to decide how many total messages to send for A/B testing before a winner is declared.

> 👍 Triggered Campaign Example
>
> If you select 500 users as your test audience, we will alternate delivery of Variant A and Variant B as users qualify for the campaign. After a total of messages are sent (Variant A – 250 and Variant B – 250), we then decide the winner based on the number of clicks and continue only with this winning message for the duration of the campaign.

Deciding on a test audience for A/B testing triggered campaigns requires some estimation. We recommend you check the total messages that were sent for similar triggered campaigns in the past to get a sense of how many users may qualify. If you select a test audience that is too small such as 25 users, you will get a statistically insignificant sample. If your test group size exceeds the total number of users who ultimately qualify for that campaign, then no winner will be declared and each message variant will be alternatively delivered for the duration of the campaign.

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, you can use the + button to add multiple variants based on a user property value. In the example below, we have used the *Customer Type* user property so users with different customer type property values will receive corresponding copies of the campaign based on their different levels (Silver, Gold, or Platinum).

> 📘 For Writers only
>
> Link to the "What" section for messaging channels.

## Define the Campaign Schedule

You can set up the *When* to schedule the campaign start and end using the options below:

Past behavior campaigns can be scheduled to run:

* On a specific date and time.
* On multiple specified dates and times.
* Recurring at a periodicity you set.

Live campaigns can be set up on a specific event:

* In response to a user event.
* User event/inaction combination (e.g., abandoned cart scenario).
* Based on a date event property value of an event (for example,  a reminder for upcoming travel booking).

### Delivery preferences

#### Delivery in User’s Timezone

CleverTap gives the option for delivering notifications in the user’s timezone while creating scheduled campaigns or journeys. This is a relevant feature for businesses that have international users and who want to send time-sensitive notifications to their users. If you select this option, CleverTap staggers the delivery of notifications and qualifies users according to their timezone.

#### Do Not Disturb

You can specify *Do Not Disturb* (DND) hours during which notifications from this App Inbox campaign are prevented from going out, either by discarding them or delaying delivery to after DND hours complete, such as 9 PM to 9 AM.

#### Cut-off

Since past behavior campaigns can have scheduled times, you have the option to stop a campaign delivery after a certain cut-off time, or even deliver at the specified time in the user’s timezone. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

<Image title="Push_notification_editor_when.png" alt={978} className="border" border={true} src="https://files.readme.io/4b6e217-Push_notification_editor_when.png" />

> 📘 Recurring Day
>
> If you specify a recurring day for a campaign such as the 7th of each month, then the campaign will start for the specified day and ignore the creation date. This is a precaution to avoid sending a campaign unintentionally on a prior date.

## Publish Campaign

After testing and once you are satisfied with the appearance of your campaign, finalize your campaign with the following steps:

1. Click **Continue** to view your campaign summary. The overview page displays.
2. View your campaign summary, then click **Publish Campaign**.

<Image title="campaign_Publish.png" alt={1193} className="border" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png" />
