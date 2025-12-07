---
title: Create Message_clone_standard_template
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

Define all the sections and publish the campaign. 

## Start Campaign Setup

The *Start here* section displays the setup information. 

This section has the following parts:

* **Start here**:  Displays the information for platforms such as FCM, Xiaomi, or iOS. Check that the required platforms are integrated and ready for campaigns. 
* **Qualification criteria**: Deliver the notification by Past Behavior, Custom List, Live behavior, or trigger via API. For more information about segmenting users, refer to [Segments](https://docs.clevertap.com/docs/segments).
* **Set a goal**: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. You can define your conversion goal further by filtering an event by event properties. This selection is optional.

The campaign goal can be as generic or as specific as you want. It can answer questions from *How many users were influenced for purchasing an X amount?* to *How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount?*. 

<Image title="Push_notification_set_goal_track_conversion.png" alt={919} border={true} src="https://files.readme.io/4fbbeb2-Push_notification_set_goal_track_conversion.png">
  Set a Goal
</Image>

## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the *Target segment* section. Here, you can create a new segment or use a previously saved user segment from the *segment* list. 

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

You can also target users basis their past behavior. For past behavior campaigns, you also have an option to calculate estimated reach. The estimated reach shows the number of users that qualify for the campaign criteria and the number of reachable users via mobile push.

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can send a push notification to English-speaking female users who live in the United States. 

<Image title="Filter By User Properties.png" alt={486} border={true} src="https://files.readme.io/3d4faa2-Filter_By_User_Properties.png">
  Filter by User Properties
</Image>

To know more about what segments can be used, see [Segments](doc:segments).

### Constant event property (Optional)

You can also hold a property constant across the selected events.  For more information, see [Constant Event Property](doc:constant-property).

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information on control groups, refer to [Control Groups](doc:control-groups).

<Image title="Control_Group_Editor.png" alt={933} src="https://files.readme.io/0eacc15-Control_Group_Editor.png">
  Control Group
</Image>

### Targeting Cap

You can limit the number of users receiving the message. 

A relevant example is a limited offer where you want to distribute a fixed number of coupon codes. If the total reach for your campaign exceeds the number of coupon codes available, then you can limit the number of users who will receive the message.

<Image title="Target_Cap.jpg" alt={835} src="https://files.readme.io/20d412f-Target_Cap.jpg">
  Target Cap
</Image>

This section explains the campaign creation flow when determining the target audience for your message. Under the *Estimated Reach* section, select the option to limit the delivery of messages to the specified number.\
You can configure the campaign limits using the following options: 

* **All target segment users**: Send the campaign to all the target segment users. You can also prevent sending out unwanted campaigns by *Don't send the campaign if target segment exceeds* option and entering the value for the number of users. When selecting this option, a campaign does not run if the number of qualified users exceeds the safety limit. The campaign creator receives an email alert for further action.
* **Only**: Select this option to limit the number of users for each campaign run.

The campaign for triggered campaigns based on live user segments ends after delivering the specified number of messages to the qualified users. When creating Live campaigns, you can also use the past behavior and user properties by selecting the *Filter on past behavior and user properties* checkbox. On selecting the checkbox, you can further filter your target segment as shown in the following image:

<Image title="Past Behavior Segment filter for Live Campaigns.png" alt={2226} className="border" border={true} src="https://files.readme.io/9505843-Past_Behavior_Segment_filter_for_Live_Campaigns.png" />

## Define the Message Content

Now, you can set up the *What* which is the campaign content with four different options:

* Single Message
* AB Test
* Split Delivery
* By User Property

Click *Go To Editor* to create your message. 

## Message Editor

{user["Write the message editor details here "]}>

### Message Types

You can create the following types of messages:

* [Single Message](https://docs.clevertap.com/docs/push-creation#section-single-message)
* [AB Test](https://docs.clevertap.com/docs/push-creation#section-a-b-testing)
* [Split Delivery](https://docs.clevertap.com/docs/push-creation#section-split-delivery)
* [By User Property](https://docs.clevertap.com/docs/push-creation#section-by-user-property)

### Single Message

This message type allows a single message copy to be set up for the entire audience. This message copy can be [personalized](https://docs.clevertap.com/docs/personalize-message-all) for each qualifying user. This message type is best suited for use cases where the message doesn’t vary much based on user properties such as language, geography, and so on.

### A/B Testing

A/B testing helps you understand what type of message copy works best to get clicks from users.

You can test up to three message variants on a test group and the variant that gets the most clicks is declared the winning variant and is automatically sent to the rest of your target audience.

When you create multiple variants for a campaign, you can also auto-copy what is already present in a current variant.

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

After all 300,000 messages have been delivered, we calculate the winning message over this test group based on the number of click-throughs. In this example, we then automatically send the winning message to the remainder of your target audience which is 1,700,000 users in this example.

Note that for A/B testing, we ensure there is always an equal number of messages sent for each variant, so there is no bias introduced during the test phase and that the best-performing message is always declared the winner.

#### Split Delivery to Live User Segments

With campaigns sent to live user segments (triggered campaigns), messages are delivered immediately when a user’s activity matches your selected criteria. For example, you can send a message when the user has completed a booking or purchase. Because it is impossible to determine the reach of triggered campaigns upfront, you need to decide how many total messages to send for A/B testing before a winner is declared.

> 👍 Triggered Campaign Example
>
> If you select 500 users as your test audience, we will alternate delivery of Variant A and Variant B as users qualify for the campaign. After a total of messages are sent (Variant A – 250 and Variant B – 250), we then decide the winner based on the number of clicks and continue only with this winning message for the duration of the campaign.

Deciding on a test audience for A/B testing triggered campaigns requires some estimation. We recommend you check the total messages that were sent for similar triggered campaigns in the past to get a sense of how many users may qualify. If you select a test audience that is too small such as 25 users, you will get a statistically insignificant sample. Suppose your test group size exceeds the total number of users who ultimately qualify for that campaign. In that case, no winner will be declared and each message variant will be alternatively delivered for the duration of the campaign.

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, you can use the + button to add multiple variants based on a user property value. In the example below, we have used the *Customer Type* user property so users with different customer type property values will receive corresponding copies of the campaign based on their different levels (Silver, Gold, or Platinum).

> 📘 For Writers only
>
> Link to the "What" section for messaging channels.

## Define the Campaign Schedule

You can set up the *When* to schedule the campaign start and end using the options below:

The delivery preferences for Past behavior campaigns can be set as follows:

* Send Now
* Schedule for later
* Set as Recurring

The delivery preferences for Live campaigns can be set as follows:

* Start Date and Time
* End Date and Time
* Set Delay

### Delivery preferences

You can apply global campaign limits to determine how many push notifications each app user receives per day. If you want to override these settings for an important campaign, you can select the *Don’t apply global campaign limits to this campaign* checkbox.

You can also click the *Advanced* checkbox to specify *Do Not Disturb* (DND) hours during which notifications from this push campaign are prevented from going out, either by discarding them or delaying delivery after DND hours, such as 9 PM to 9 AM.

Since past behavior campaigns can have scheduled times, you have the option to stop a campaign delivery after a certain cut-off time, or even deliver at the specified time in the user’s timezone. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

<Image title="Delivery_Preferences.png" alt={478} className="border" border={true} src="https://files.readme.io/4f1a688-Delivery_Preferences.png" />

> 📘 Recurring Day
>
> If you specify a recurring day for a campaign such as the 7th of each month, then the campaign will start for the specified day and ignore the creation date. This is a precaution to avoid sending a campaign unintentionally on a prior date.

## Publish Campaign

After testing and previewing the appearance of your campaign, finalize your campaign by clicking **Publish Campaign**.

<Image title="campaign_Publish.png" alt={1193} className="border" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png" />
