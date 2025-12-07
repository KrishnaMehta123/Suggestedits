---
title: Create Message
excerpt: ''
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
3. From the _Messaging Channels_ list, select **Web Native Display**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5226f37d1b9ef6522fb2baa32207dcf762492cadb19748c7abddb00ec6b4b6dd-native.png",
        "Campaign Button Lists All Channels",
        "Create a New Web Native Display Campaign "
      ],
      "align": "center",
      "sizing": "100",
      "border": true,
      "caption": "Create a New Web Native Display Campaign"
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
        "https://files.readme.io/aecb9e8-Native_display_web.png",
        "Expand Each Section",
        1472
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Web Native Display Campaign Setup"
    }
  ]
}
[/block]


Define all the sections and publish the campaign. 

## Start Campaign

The _Start here_ section displays the setup information. 

This section has the following parts:

- Set a goal: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. This selection is optional.

The campaign goal can be as generic or as specific as you want. It can answer questions from "_How many users were influenced for purchasing an X amount?_" to "_How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount?_ ". 

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

You must indicate the target audience for your campaign. You can specify your target audience from the _Target segment_ section. Here, you can create a new segment or use a previously saved user segment from the _segment_ list. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f1fee47-campaign_Who_Live_segment.png",
        "Define the Target Segment",
        964
      ],
      "align": "center",
      "border": true,
      "caption": "Define the Target Audience"
    }
  ]
}
[/block]


### Segment

If you want to create an ad-hoc segment, you can select a type of segment on which to base your campaign. You can create the target based on user properties or live (ongoing) user behavior. The latter is helpful to send out real-time, triggered campaigns.

### Deliver Action-Based Web Native Display Campaign

You can trigger a web native display campaign based on an action. Users receive this campaign when they perform an action on the website. For example, creating a campaign that displays a personalized contextual banner with images of fitness equipment for users who have shown interest in the fitness category.  
It makes the web experience more contextual and increases conversion. 

### Filter Users Based on Past Behavior

You can also target users basis their past behavior. For example, you might want to create a personalized campaign for a set of customers who have purchased a specific product in the past. 

### Filter by User Properties

Using the _With user properties_ filter in the _Who_ section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can create a web native display campaign specifically for female users who live in the United States. The image below represents a sample target segment that is filtered using specific user properties to target the required audience.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d3dca2d-user_prop.png",
        "Filter by User Properties",
        2202
      ],
      "align": "center",
      "border": true,
      "caption": "Filter by User Properties"
    }
  ]
}
[/block]


The following table explains the various property types:

[block:parameters]
{
  "data": {
    "h-0": "Property Type",
    "h-1": "Description",
    "h-2": "Example",
    "0-0": "User Properties",
    "0-1": "Custom [user profile properties](https://docs.clevertap.com/docs/user-profiles#section-user-profile-data-model) that you define and send to CleverTap.",
    "0-2": "Customer Type = Platinum",
    "1-0": "Demographics",
    "1-1": "Demographics filters include _Age_ and _Gender_.",
    "1-2": "Age = 25 to 40 years  \nGender = Female",
    "2-0": "Geography",
    "2-1": "User's coarse location. Filters include _Country_, _Region_, and _City_. CleverTap's SDK can automatically detect this from the user's IP address.",
    "2-2": "Country = United States  \nState = California  \nCity = San Francisco",
    "3-0": "Reachability",
    "3-1": "Reachability filters include _Has email address_, _Has phone number_, _Unsubscribed email_, and _Unsubscribed SMS_.",
    "3-2": "Unsubscribed email = No",
    "4-0": "App Fields",
    "4-1": "App fields filters include _App Version_, _Device Make_, _Device Model_, _OS Version_, and CleverTap _SDK Version_. This information is sent by CleverTap's SDK for each device that has your app which means a single user can have multiple devices associated with their user profile.",
    "4-2": "OS Version = 10"
  },
  "cols": 3,
  "rows": 5,
  "align": [
    "left",
    "left",
    "left"
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
        "https://files.readme.io/99861e7-control_group.png",
        "Define Control Group",
        825
      ],
      "align": "center",
      "border": true,
      "caption": "Set Control Group"
    }
  ]
}
[/block]


## Message Types

You can create the following types of messages:

- Single Message
- AB Test
- Split Delivery
- By User Property

### Single Message

Here, a standard web campaign is rolled out for all the users who qualify as your target audience. This type of campaign is best suited for use cases where the campaign communication does not vary based on the differences between properties such as language, geography, or any other user properties.

### A/B Testing

A/B testing helps you understand what type of message copy works best to get clicks from users.

You can test up to three message variants on a test group and the variant that gets the most clicks is declared the winning variant and is automatically sent to the rest of your target audience.

When you create multiple variants for a campaign, you can also auto-copy what is already present in a current variant.

### Split Delivery

With split delivery, you can decide what percentage of your audience receives each message variant for the duration of the campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/73d579a-campaign_split_delivery.png",
        "Split Delivery for Web Native Display Campaigns",
        577
      ],
      "align": "center",
      "border": true,
      "caption": "Split Delivery for Web Native Display Campaigns"
    }
  ]
}
[/block]


#### Split Delivery to Live User Segments

With campaigns sent to live user segments (triggered campaigns), messages are delivered immediately when a user’s activity matches the criteria you have selected. For example, you can send a message when the user has completed a booking or purchase. Since it is not possible to determine the reach of triggered campaigns upfront, you need to decide how many total messages to send for A/B testing before a winner is declared.

> 👍 Triggered Campaign Example
> 
> If you select 500 users as your test audience, we will alternate delivery of Variant A and Variant B as users qualify for the campaign. After a total of messages are sent (Variant A – 250 and Variant B – 250), we then decide the winner based on the number of clicks and continue only with this winning message for the duration of the campaign.

Deciding on a test audience for A/B testing triggered campaigns requires some estimation. We recommend you check the total messages that were sent for similar triggered campaigns in the past to get a sense of how many users may qualify. If you select a test audience that is too small such as 25 users, you will get a statistically insignificant sample. If your test group size exceeds the total number of users who ultimately qualify for that campaign, then no winner will be declared and each message variant will be alternatively delivered for the duration of the campaign.

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

## Web Native Display Editor

The Web Native Display Editor offers instant access to ready-to-use templates for creating personalized campaigns. For more information, refer to the [Web Native Display Editor](https://staging.docs.user.clevertap.net/docs/web-native-display-editor) document.

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
        "Define the Campaign Schedule",
        974
      ],
      "align": "center",
      "border": true,
      "caption": "Define Campaign Schedule"
    }
  ]
}
[/block]


### Delivery preferences

#### Set frequency

From the _Delivery preferences_ section, select the days and the time frame to deliver the message.  
Click _Apply to all_ to copy the choices from the selected day to all other days. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f4ad363-delivery_preferences.png",
        "Set up Delivery Preferences",
        1085
      ],
      "align": "center",
      "border": true,
      "caption": "Set Campaign Delivery Preferences"
    }
  ]
}
[/block]


## Publish Campaign

After testing and once you are satisfied with the appearance of your campaign, finalize your campaign with the following steps:

1. Click **Continue** to view your campaign summary. The overview page displays.
2. View your campaign summary, then click **Publish Campaign**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b521e92-campaign_Publish.png",
        "Publish Campaign",
        1193
      ],
      "align": "center",
      "border": true,
      "caption": "Publish Campaign"
    }
  ]
}
[/block]