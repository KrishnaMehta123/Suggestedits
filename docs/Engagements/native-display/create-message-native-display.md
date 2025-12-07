---
title: Create Message
excerpt: Learn how to create a Native Display campaign using the CleverTap dashboard.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Create a New Campaign

You can create and publish Native Display campaigns to deliver targeted messages to your users. Follow these steps to engage your audience effectively with rich, context-aware messages.

1. From the CleverTap dashboard, select **Campaigns**.
2. Click **+ Campaign**.
3. From the _Messaging Channels_ list, select **Native Display**.

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


4. Define all campaign settings.
5. Review and publish the campaign.

# Start Campaign Setup

The _Start here_ section helps you define key setup information.

## Set a Goal

Setting a goal allows you to track your campaign’s effectiveness and measure conversions based on specific user actions.

- **Conversion Tracking**: Goals can be general (for example, “how many users made a purchase?”) or specific (for example, “how many first-time visitors purchased red shoes worth at least X amount and blue jackets worth at least Y amount?”).
- Define the **Conversion time** to set the period during which conversions are tracked.
- Further refine goals by filtering events using _Revenue Property_. For more details, see [Events](https://docs.clevertap.com/docs/events#event-properties).

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


# Define the Audience

In this section, you can define the target audience for your campaign. You can create a new segment or use a previously saved user segment from the segment list.

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


### Deliver Action-Based Web Native Display Campaign

You can trigger a native display campaign based on an action. Users receive this campaign when they perform an action on the website. For example, you could create a campaign that displays a personalized contextual banner with images of fitness equipment for users who have shown interest in the fitness category. This would make the experience more contextual and increase conversion.

### Filter Users Based on Past Behavior

You can also target users based on their past behavior. For example, you might want to create a personalized campaign for a set of customers who have purchased a specific product in the past.

### Ad-hoc Segment

An ad-hoc segment is a temporary audience segment created while setting up a campaign or analyzing user behavior. Unlike saved segments, ad-hoc segments are not stored for future use and exist only for the activity for which they are created.

You can create an ad-hoc segment to target users based on:

- **User Properties**: For example, language, location, or device type.
- **Live Behavior**: For example, users who performed a specific action, such as launching the app or completing a purchase.

### Filter by User Properties

Using the With user properties filter in the Who section, you can segment your campaign to only reach users who meet specific criteria.

For example, you can create a native display campaign for female United States users. The image below represents a sample target segment filtered using specific user properties to reach the required audience.

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


### Calculate Estimated Reach 

The Estimated Reach option allows you to preview how many users meet your targeting criteria in an online trigger campaign before publishing it. This helps you validate audience size and adjust filters to ensure the campaign reaches the intended users. 

Estimated Reach is particularly useful when you select the _Filter on past behavior and user properties_ option. You can view both the estimated user count and device count. 

To calculate the estimated reach, perform the steps below: 

1. Select **Filter on past behavior and user properties**. 
2. Click **Calculate** in the right panel. The result shows the estimated number of users or devices for that segment. You can view the following: 
   - **Total Users**: The number of users that match the filters. 
   - **Breakdown by Platform and Devices**: The users count on Android, iOS, or both, and on different devices. 
   - **Visual Indicator**: A chart summarizing the share by operating system. 
   The estimate, based on the latest available event data, updates each time you apply or modify filters. It reflects stored event data and is not a real-time count. This helps you plan and refine your audience before sending the campaign. 

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
      "sizing": "85% ",
      "border": true,
      "caption": "Calculate Estimate Reach"
    }
  ]
}
[/block]


### Control Group and Target Segment Cap

Define a control group to compare campaign results with users who did not receive the message. For more information, refer to [Control Groups](doc:control-groups).

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


# Define the Message Content

The _What_ section allows you to create your campaign content using different message types:

## Message Types

You can choose how you want to communicate with your audience by selecting the appropriate message type. Depending on your campaign objective, you can send a uniform message, experiment with different variants, control delivery proportions, or personalize content based on user attributes. The following message types help you tailor your campaign for maximum engagement and effectiveness:

- **Single Message**: Sends the same message to all users.
- **A/B Testing**: Test up to three variants and send the best-performing message to users.
- **Split Delivery**: Control the percentage of users receiving each variant.
- **By User Property**: Send different messages based on user attributes.

### Split Delivery

{@Amrita, when selecting the Split delivery, it doesn't expand as shown in the image, so can we remove the below image?}

Define how the audience is split across message variants.

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


For example, if you select 500 users as the test group:

- Variant A is sent to 250 users.
- Variant B is sent to 250 users.

The variant with the most clicks becomes the winner.

#### Split Delivery for Live Segments

For triggered campaigns, messages are delivered instantly when users match the criteria.

> 📘 Note
> 
> Estimate the test group size carefully. A group that is too small may lead to unreliable results.

### By User Property

Send different message variants based on user attributes such as language or customer type.  
{@Amrita, the user property window looks different in DB; the image below is the one it shows}

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1ed27bc59c6e6517233af4087fbe3b559a17d524533f3992a9ea8ce4a6694046-image.png",
        null,
        "Define User Properties"
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Define User Properties"
    }
  ]
}
[/block]


{@Amrita, the below one seems to be old, I believe, we can remove}

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


For example, different messages for English-speaking customers.

## Native Display Editor

You can personalize your message with text and media.

### Content

1. Enter the **Title** and **Message** in the _Text_ section.
2. You can include CTAs in the _Actions_ section. _Native Display_ enables various types of call to action (CTA) to cater to different use cases. Choose from one of the following actions (Optional):  
   {@Amrita, In the DB, we have only** iOS and Android **CTA URLs}
   - **On-message URL**: Opens a deep link when users click anywhere on the message.
   - **Open URL CTA**: Opens deep links for iOS or Android devices.
3. Upload or personalize media (images, GIFs, videos, or audio) in the _Media_ section.  
   The supported file formats include .jpg, .jpeg, .png, .gif, .mp3, and .mp4 (.png can be converted to .jpeg using the selected background color).

The following are the supported media types: 

| Template          | Template Category                 |
| :---------------- | :-------------------------------- |
| Simple Message    | Media (images, gif, video) only   |
|                   | Media (images, gif, video) + Text |
| Carousel Message  | Media (images, gif) only          |
|                   | Media (images, gif) + Text        |
| Message with icon | Media (images, gif, video) only   |
|                   | Media (images, gif, video) + Text |
| Custom key value  | Any                               |

4. Custom key-value pairs

Use custom key-value pairs to send additional data when a user clicks on the message button. This data is not visible to the user and can be used for tracking or integration purposes. You can add multiple key-value pairs as needed to enhance your campaign’s functionality.

Use the Native Display editor to craft visually engaging messages.

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


## Style

The _ Style_ tab allows you to customize the look and feel of your message to ensure it aligns with your brand and captures users’ attention. You can adjust the following elements:

**Title color:** Select the color for the message title. Ensure that the text is easily readable against the background.

**Message color:** Customize other visual elements such as borders, buttons, or accents to enhance the overall appearance and user experience.

**Background color:** Choose the color that appears behind the message content. This helps your message stand out and match your brand’s visual identity.

By tailoring these style options, you can create engaging and visually appealing messages that resonate with your audience while maintaining consistency with your brand guidelines. Test different combinations to find the most effective design before publishing your campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/97e7c4a61196ade266cc17d1dfdbc8af06b48aaa75de19714d8dfd42bf08dfbd-image.png",
        null,
        "Set your Style Options"
      ],
      "align": "center",
      "border": true,
      "caption": "Set your Style Options"
    }
  ]
}
[/block]


### Preview & Test

Once you have set up your message, you can send a test notification to any test profile you have configured.

1. Click **Preview & Test** in the message editor.
2. Verify how the message looks and behaves before publishing.

# Define Campaign Schedule

Set the delivery schedule for live campaigns in the _When _ section including:

- **Start date and time**
- **End date and time**
- **Set Delay** for message delivery {@Amrita, do we have this option?, I don't see in the DB}

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


## Delivery Preferences

### Set Frequency

Select the days and time windows for message delivery. If you do not set a frequency, messages are delivered based on the account’s time zone. Click **Apply to all** to copy preferences across days.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/eee9a39d24af56479de1e81faed430fc86ed1a882f1ed58a46c4871ad4792f28-image.png",
        null,
        "Set Delivery Preferences"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Delivery Preferences"
    }
  ]
}
[/block]


# Publish Campaign

After completing the setup and testing, follow these steps to publish your campaign:

1. Click **Continue** to view the campaign summary.
2. Review all settings and content.
3. Click **Publish Campaign**.

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