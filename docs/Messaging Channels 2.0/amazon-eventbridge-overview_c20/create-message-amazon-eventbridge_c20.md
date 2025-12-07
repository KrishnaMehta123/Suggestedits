---
title: Create Message
excerpt: Learn how to create a campaign for Amazon EventBridge
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: >-
    Refer to the pages listed below to learn more about the following Amazon
    Eventbridge sections:
  pages:
    - type: link
      title: Personalize Message
      url: >-
        https://docs.clevertap.com/docs/personalize-message-amazon-eventbridge_c20
    - type: link
      title: Amazon Eventbridge Campaign Stats
      url: https://docs.clevertap.com/docs/stats-for-amazon-eventbridge_c20
---
[block:api-header]
{
  "title": "Create a New Campaign"
}
[/block]
Create a campaign to deliver your Amazon Eventbridge message. 
To create a new campaign:

1. From the CleverTap dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **Amazon Eventbridge **. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3d6fb90-Select_Amamzon_EventBridge.png",
        "Select Amamzon EventBridge.png",
        2858,
        2682,
        "#f1f2f6"
      ],
      "border": true
    }
  ]
}
[/block]
The *Campaigns* page displays.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/97597d8-New_Amamzon_Eventbridge_campaign.png",
        "New Amamzon Eventbridge campaign.png",
        2748,
        1424,
        "#fbfbfb"
      ],
      "border": true,
      "sizing": "80"
    }
  ]
}
[/block]
Define all the sections and publish the campaign.

## Start Campaign Setup
The *Start here* section displays the setup information. 

This section has the following parts:
* **Start here**: Displays the information for platforms such as FCM, Xiaomi, or iOS. Check that the required platforms are integrated and ready for campaigns.

* **Qualification criteria**: Deliver the notification by Past Behavior, Custom List, or Live behavior.
Past/Custom List: Select this option to deliver notifications to users based on an activity they performed or have been performing. 
  Live Behavior: Select this option to deliver notifications to users as soon as they perform or fail to perform an activity. 
  For more information about segmenting users, refer to [Segments](https://docs.clevertap.com/docs/segments).

* **Set a goal**: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve with the campaign. You can define your conversion goal by selecting the Event and Conversion time. This selection is optional.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/32d63db-Push_notification_set_goal_track_conversion.png",
        "Push_notification_set_goal_track_conversion.png",
        919,
        361,
        "#fafafc"
      ],
      "border": true
    }
  ]
}
[/block]
## Define the Audience
You must indicate the target audience for your Amazon EventBridge campaign. You can specify your target audience from the *Target Segment* section. Here, you can create a new segment or use a previously saved user segment from the *segment* list.

You can create the target based on past user behavior and user properties or live (ongoing) user behavior. The latter is helpful to send out real-time, triggered Amazon Eventbridge campaigns.

For instance, you can create a live *Inaction within time* campaign that targets users as soon as they add a product to their cart but do not finish transacting within 10 minutes; that is the golden window within which most users transact on iOS and Android app platforms.

### Target Segment
#### Deliver Notifications based on Past Behavior (PBS)

You can also target users based on their past user behavior. For past behavior campaigns, you also have an option to calculate *Estimated reach*. The *Estimated reach* shows the number of users that qualify for the campaign criteria and the number of reachable users via Amazon Eventbridge.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d9c8455-Push_notification_editor_Who.png",
        "Push_notification_editor_Who.png",
        1168,
        771,
        "#f8f8fc"
      ],
      "border": true
    }
  ]
}
[/block]
#### Deliver Action Based Notifications
You can trigger an Amazon Eventbridge message based on an action. Users receive Amazon Eventbridge notifications when they perform an action in the app instead of waiting for the next app launch. It makes the messages more contextual and increases conversion. The Amazon Eventbridge message is not triggered for campaigns with delays.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e6bdd94-Target_Segment_Live_Behavior.png",
        "Target Segment_Live Behavior.png",
        2282,
        530,
        "#fafbfc"
      ],
      "border": true
    }
  ]
}
[/block]
### Filter by User Properties
Using the *With user properties* filter in the *Who* section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can send an Amazon EventBridge notification to English-speaking female users who live in the United States. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7989d1a-Filter_By_User_Properties.png",
        "Filter By User Properties.png",
        486,
        216,
        "#f6f8fc"
      ],
      "border": true
    }
  ]
}
[/block]
To know more about what segments can be used, refer to [Segments](doc:segments).

#### Constant event property
You can also hold a property constant across the selected events. For more information, refer to [Constant Event Property](https://docs.clevertap.com/docs/constant-property).

### Control Group and Targeting Cap

#### Set Control Group
You can define the control group to compare and measure the results of your campaign. For more information on control groups, refer to [Control Groups](doc:control-groups).
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b79e920-Control_Group_Editor.png",
        "Control_Group_Editor.png",
        933,
        549,
        "#fbfbfc"
      ],
      "border": true
    }
  ]
}
[/block]
#### Set Cap for Targeting
You can limit the number of users receiving the message.

* Past Behavior Segment
  A relevant use case is a limited offer where you want to send a fixed number of coupon codes you want to distribute. If the total reach for your campaign exceeds the number of coupon codes you can distribute, you can limit the number of users who will receive the message to precisely the number of coupons you want to distribute.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a51ee27-Set_a_cap_for_targeting.png",
        "Set a cap for targeting.png",
        1454,
        350,
        "#fbfbfc"
      ],
      "border": true
    }
  ]
}
[/block]
This section explains the campaign creation flow when you are determining who to send your message to. Under the *Estimated reach* section, select the option to limit the delivery of the messages to a specified number.
  The campaign limits can also be configured using the following options: 
**All target segment users**: Select this option to send the campaign to all the target segment users. You can also prevent sending out unwanted campaigns by *Don't send the campaign if target segment exceeds* checkbox and entering the value for the number of users. When selecting this option, a campaign does not run if the number of qualified users exceeds the safety limit. The campaign creator receives an email alert for further action.
**Only**: Select this option to limit the number of users for each run of a campaign.

* Live Behavior Segment
  For triggered campaigns based on live user segments, the users receive a message as they qualify until the total quantity specified has been delivered after which the campaign ends.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/94d8049-Targeting_Cap_Live_Behavior.png",
        "Targeting Cap_Live Behavior.png",
        1290,
        312,
        "#fbfbfc"
      ],
      "border": true
    }
  ]
}
[/block]
  The campaign limits can be configured using the following options: 
**All target segment users**: Select this option to send the campaign to all the target segment users.  
**Only**: Select this option to limit the number of users for each run of a campaign.
***Only per day**: Select this option to limit the number of users for each run of a campaign per day.
[block:callout]
{
  "type": "success",
  "body": "A customer has a budget for distributing 1,000 discount coupons but the qualified user count is 10,000. If you select the safety check, the campaign does not run and prevents the sender from spending over budget.",
  "title": "Safety Check Example"
}
[/block]
## Define the Message Content
Now, to set up the *What* for the Amazon EventBridge campaign content, perform the following steps: 
1. Click *Go To Editor* to create your message.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2f8d628-campaign_what_single_message.png",
        "campaign_what_single_message.png",
        1165,
        178,
        "#f9f2f5"
      ],
      "border": true
    }
  ]
}
[/block]
2. Select the *User Profiles Attributes* and/or GCM/APNS Tokens to send in the payload if required.
3. Click **+Key-Value Pair** and enter your *Custom key-value pairs*. For more information about customizing the key-value pair, refer to [Personalize Message](https://docs.clevertap.com/docs/personalize-message-amazon-eventbridge_c20).
4. Click **Done**.

You can also use custom key-value pairs to send custom data.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d199531-amazon_eventbridge_editor_create_messge.png",
        "amazon_eventbridge_editor_create_messge.png",
        989,
        638,
        "#c8c4d2"
      ],
      "border": true
    }
  ]
}
[/block]
## Define the Campaign Schedule

You can set up the *When* to schedule the campaign start and end using the options below: 

### Date and Time
The *Date and time* for Past behavior campaigns can be set as follows:

  * Send Now: Select this option to send the campaign right away. 
  * Schedule for later: Select this option to send the campaign on a specific date and time.
  * Set as Recurring: Selec this option to send the campaign at defined intervals.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ed19319-Push_notification_editor_when.png",
        "Push_notification_editor_when.png",
        978,
        485,
        "#fbfaf8"
      ],
      "border": true
    }
  ]
}
[/block]
The *Date and time*  for Live campaigns can be set as follows:
  * Start Date and Time: Select this option to send the campaign right away or on a specific date and time. 
  * End Date and Time: Select this option to run the campaign indefinitely or define the end date of the campaign.
  * Set Delay: Select this option to send the campaign as soon as the user qualifies for the segment or define the delay.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2884f9b-Delivery_Preferences_Live_Behavior.png",
        "Delivery Preferences_Live Behavior.png",
        2274,
        764,
        "#fbfcfd"
      ],
      "border": true
    }
  ]
}
[/block]
### Delivery preferences
For both Past Behavior and Live Campaigns, you can also set the *Do Not Disturb* (DND) hours during which notifications from the campaign are prevented from going out, either by discarding them or delaying delivery to after DND hours complete, such as 9 PM to 9 AM.

For Past Behavior Campaigns, if you want your campaign to adapt delivery times according to the user’s timezone, check the *Timezone* checkbox. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

Since past behavior campaigns can have scheduled times, you have the option to stop a campaign delivery after a certain cut-off time, or even deliver at the specified time in the user’s timezone. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e8e7226-amazon_eventbridge_delivery_preference.png",
        "amazon_eventbridge_delivery_preference.png",
        936,
        397,
        "#fbfbfd"
      ],
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "Recurring Day",
  "body": "If you specify a recurring day for a campaign such as the 7th of each month, then the campaign will start for the specified day and ignore the creation date. This is a precaution to avoid sending a campaign unintentionally on a prior date."
}
[/block]

## Publish Campaign
After testing and previewing the appearance of your campaign, finalize your campaign by clicking **Publish Campaign**.


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