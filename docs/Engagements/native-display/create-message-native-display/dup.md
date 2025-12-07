---
title: Dup
excerpt: ''
deprecated: false
hidden: true
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
        "https://files.readme.io/9af0f8b74ceda81b46e3e6e24646432e1d681f83237257daa31d98472f91eac2-Select_Native_DIsplay_Campaign.png",
        "Click +Campaign and Select Web Native Display",
        1360
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Select Native Display Campaign"
    }
  ]
}
[/block]


The campaign page displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a805f56-Campaign_Creation_Page.jpg",
        "Create a new native display campaign",
        1404
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Creating a Native Display Campaign"
    }
  ]
}
[/block]


Define all the sections and publish the campaign. 

## Start Campaign

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
        "Enable Goal Conversion Tracking",
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

You must indicate the target audience for your campaign. You can specify your target audience from the  _Target segment_ section. You can create a new segment or use a previously saved user segment from the _segment_ list. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f1fee47-campaign_Who_Live_segment.png",
        "Define the target audience for your campaign",
        964
      ],
      "align": "center",
      "border": true,
      "caption": "Define Target Audience"
    }
  ]
}
[/block]


> ❗️ Source Event Property
> 
> The CleverTap source event property is not supported for web pop-up and mobile in-app campaigns.

> 🚧 Warning
> 
> In the scenario where multiple Native Display Campaigns are created for a single event schedued to be running at the same time, CleverTap delivers only the first campaign that was created in majority of the cases.

### Segment

If you want to create an ad-hoc segment, you can select a type of segment on which to base your campaign. You can create the target based on user properties or live (ongoing) user behavior. The latter helps send out real-time, triggered campaigns.

### Deliver Action Based Messages

(@Meenakshi: All this content must be updated per the Native Display channel behavior. Please check with the developer about the behavior.)

You can trigger a message based on an action. Users receive messages when they perform an action in the app instead of waiting for the next app launch. It makes the messages more contextual and increases conversion. Campaigns with delays and app inbox coupled with a push message do not trigger instant messages.

### Calculate Estimated Reach

Estimated Reach allows you to preview how many users meet your targeting criteria in an online trigger campaign before you publish it. This feature is useful when you apply Mini WHO filters such as behavioral conditions (for example, users who did or did not perform an action) and user properties (for example, app version, platform, or location).

You see the estimated user count and device count. This visibility helps you ensure your campaign reaches the intended audience and adjust filters before finalizing it.

To calculate the Estimated reach, perform the steps below:

- Select **Filter on past behavior and user properties**.
- Click **Calculate **in the right panel. The result shows the estimated number of users or devices for that segment.

You can view the following:

**Total Users: **The number of users that match your conditions and delivery filters.  
**Breakdown by Platform and Devices: **The count of users on Android or iOS or Both and on different devices.  
**Visual Indicator: **A doughnut chart summarizing the share by operating system.

The estimate updates based on the latest filters and event data available when you calculate it.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/44bb9f5c34466e181b1934a67365951c488221905a4373e546dfa48b7b152db8-2025-09-08_16-57-15_1.gif",
        "",
        "Calculate Estimate Reach"
      ],
      "align": "center",
      "border": true,
      "caption": "Calculate Estimate Reach"
    }
  ]
}
[/block]


The estimate includes the following:

- Users who qualify for the segment based on your trigger event and filters.
- Users whom you can message based on platform and device settings.
- Only those currently eligible for delivery (for example, users who have not uninstalled or unsubscribed).

The count reflects the event summary data stored in the system and does not perform a live or real-time lookup.

### Ad-hoc Segment

If you want to create an ad-hoc segment, you can select a type of segment on which to base your In-App campaign. You can create the target based on user properties or live (ongoing) user behavior (the latter is useful for sending out real-time, triggered In-App campaigns).

### Filter by User Properties

Using the _With user properties_ filter in the _Who_ section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can send a push notification to English-speaking female users who live in the United States. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3d4faa2-Filter_By_User_Properties.png",
        "Filter By User Properties",
        486
      ],
      "align": "center",
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
        "https://files.readme.io/08e8220-Control_Group_and_Target_Cap.png",
        "Control Group and Target Cap",
        "Set a Control Group"
      ],
      "align": "center",
      "caption": "Set a Control Group"
    }
  ]
}
[/block]


## Define the Message Content

Now, you can set up the _What_, which is the campaign content, with four different options:

- Single Message  
  AB Test
- Split Delivery
- By User Property

#### Content with image notifications

1. Simple Message \`  
   Carousel Message  
   Message with icon  
   Custom key-value  
   Carousel Message 

### Supported File Formats

The supported file formats include .jpg, .jpeg, .png, .gif, .mp3, .mp4 (.png's convert to .jpeg using selected background color).

Following are the supported media types: 

| Template          | Template Category                 |
| :---------------- | :-------------------------------- |
| Simple Message    | Media (images, gif, video) only   |
|                   | Media (images, gif, video) + Text |
| Carousel Message  | Media (images, gif) only          |
|                   | Media (images, gif) + Text        |
| Message with icon | Media (images, gif, video) only   |
|                   | Media (images, gif, video) + Text |
| Custom key value  | Any                               |

### Native Display Editor

The message builder for _Native Display_ is where you can create a rich message to engage your targeted audience.

Enter your text and message.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/20202472bd346ee3dbf1ab4168bd51dfbeb4c33c74ede38aeb47453687bf2355-image.png",
        null,
        "Native Display Editor"
      ],
      "align": "center",
      "border": true,
      "caption": "Native Display Editor"
    }
  ]
}
[/block]


#### Compose

You can upload media from your image library or use personalized media to compose your messages. 

Enter the title, message, and upload or personalize media as required. 

_Native Display_ enables various types of call to action (CTA) to cater to different use cases.

 Choose from one of the following  actions (Optional):

  \*On-message CTA URL: A click on this URL opens a deep link when you click anywhere on the message (text or image or both).

- Open URL CTA: The user can open deep links for iOS or Android. 
- Custom key-value pairs CTA: The key-value pairs send back custom data when a user clicks the _Native Display_ button. This data is not visible to the user. 

#### Style

Select the style for your notification such as background color, text color, and message color. 

### Preview & Test

Once you are all done setting up the content of your campaign in the _What_ section, you have the option to send a test notification to any CleverTap user profile you have marked as a _Test profile_  
Click the **Preview & Test** button from the message editor to test a message.

### Message Types

You can create the following types of messages:

- Single Message
- AB Test
- Split Delivery
- By User Property

#### Single Message

In this campaign, we send the same message to all users who qualify as your target audience. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between properties such as language, geography, or any other user properties.

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
        "Configure Split Delivery for Native Display Campaign",
        577
      ],
      "align": "center",
      "border": true,
      "caption": "Split Delivery in Native Display"
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

Similar to creating A/B test variants, you can use the + button to add multiple variants based on a user property value. In the example below, we have used the _Customer Type_ user property so users with different customer type property values will receive corresponding copies of the campaign based on their different levels (Silver, Gold, or Platinum). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6db3703-user_properties_all.png",
        "Define User Properties",
        486
      ],
      "align": "center",
      "border": true,
      "caption": "Define User Properties"
    }
  ]
}
[/block]


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

From the Delivery preferences section, select the days and the time frame to deliver the message.  
Click _Apply to all_ to copy the choices from the selected day to all other days. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/703c11a-Delivery_preferences_-_Native_Display.png",
        "Set the Delivery Preferences",
        1085
      ],
      "align": "center",
      "border": true,
      "caption": "Set Delivery Preferences"
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
        "Publish the Campaign",
        1193
      ],
      "align": "center",
      "border": true,
      "caption": "Publish Campaign"
    }
  ]
}
[/block]