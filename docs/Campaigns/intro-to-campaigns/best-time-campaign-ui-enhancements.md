---
title: Best Time Campaigns
excerpt: >-
  Learn how you can optimize the campaign conversion rates using the Best Time
  Campaign feature
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

_Best Time_ is a feature that learns from your user's activity over time to recommend the most optimal time to send a message to each user for a  campaign or a journey. This optimizes the message send-time for each user based on their time zone and the period they are most active with your application. These time-based messages improve the conversion rates for the campaigns and Journeys built using the Best Time feature.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/aeedcd6-Best_Time_Campaigns.png",
        "Best Time Campaigns.png",
        2122
      ],
      "align": "center",
      "sizing": "smart",
      "border": true
    }
  ]
}
[/block]



# How It Works

CleverTap identifies the best time based on a selected event. The  _Best Time_ campaigns are sent by splitting a day into 12 buckets of two hours each. The users are then assigned to one of these buckets based on the time of the day they are most active on the app. The user is then sent the campaign or journey in that two-hour window. If any user has not performed the selected event in the last 180 days, you can select the time slot (fallback time) when you want to send the campaign based on the user distribution.

> 👍 Bucket Example
> 
> For example, if a _Best Time_ campaign is created on January 1 at 5:15 PM, the campaign will start running based on the upcoming best time slot and the users will receieve camapigns based on the slot in which they are most active on the application.

> 📘 Best Time Campaign Handling During DND
> 
> If the Best Time bucket coincides with the DND period defined by the user, then the campaign message is discarded.

# Create Best Time Campaigns

This is a two-step process that includes the following steps:

1. [Set Up the Best Time Event](doc:best-time-campaign-ui-enhancements#set-up-best-time-event). 
2. [Create a Campaign using the Best Time feature](doc:best-time-campaign-ui-enhancements#create-a-campaign-using-the-best-time-feature).

## Set Up Best Time Event

You can configure the best time option for one-time or recurring campaigns for **Email**, **SMS**, **Push**, **WhatsApp**, and **Web Push** channels. To set up Best Time campaigns:

1. Navigate to _Settings_ > _Setup_ > _Best Time_ from the CleverTap dashboard.
2. Click **+ Best-Time Config**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8a845b3-Set_Up_Best_Time_Event.png",
        null,
        "Set Up Best Time Event "
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up Best Time Event "
    }
  ]
}
[/block]

3. Enter the _Config name_ to uniquely identify the Best Time event. 
4. Select the system/custom event for which you want to define the Best Time campaign. 
5. Click **+ Filter** to target a particular set of users for the campaign.  
   Consider an example where you want to send Best Time campaigns to users who have performed the _Added To Cart_ event for the product _Ironman Helmet_ on their mobile devices.
6. (Optional) Click **Preview User Distribution** to check the user distribution for the selected event in the last 180 days. You can also change the filter based on the user distribution to achieve optimal conversion rates.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/de72691-Define_Best_Time_Config.gif",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



7. Click **Save** to save the Best Time event.

Currently, you can create journeys using the default Best Time config. So, it is mandatory to mark one of the Best Time configs as Default to refer to it later. You can do so by clicking the ![lEllipses](https://files.readme.io/3b92fb0-Ellipses.png) icon and then selecting _Mark as Default_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/612bfbe-Mark_as_Default.png",
        null,
        "Marking Best Time Event as Default"
      ],
      "align": "center",
      "border": true,
      "caption": "Marking Best Time Event as Default"
    }
  ]
}
[/block]

Similarly, you can also delete a particular Best Time event by clicking the ![lEllipses](https://files.readme.io/3b92fb0-Ellipses.png) icon and then selecting _Delete_.

> 📘 Default Best Time Events
> 
> The default Best Time events cannot be deleted. Also, deleting such events does not impact the already running campaigns.

## Create a Campaign using the Best Time Feature

Here, consider an example of the Best Time email campaign. To create a campaign with this feature, perform the following steps:

1. Navigate to _Campaigns_ from the CleverTap dashboard.
2. Click **+ Campaign**.
3. Select _Email_ from the list of messaging channels.
4. Define all the following information for the campaign:

   - Qualification Criteria
   - Email Service Provider
   - Campaign Goal
   - Who
   - What

   For more information about configuring the above details on the CleverTap dashboard, refer to [Create Email Campaign](doc:create-message-email).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5de46d2-2x_Create_a_campaign.png",
        "2x Create a campaign.png",
        1571
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



5. Define the Best Time campaign schedule:  
   a. From the _When_ section of the campaign, select _Schedule for later_ or _Set as Recurring_ under the Data and time section, depending on the nature of your campaign.  
   b. Select the date to send the campaign and select _Best time for every user_ from the dropdown.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d60c6db-Select_Best_Time_option.gif",
        "Select Best Time option.gif",
        1332
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



   Best Time feature works with the following campaign types:

- One-time campaign, which is scheduled for a later time
- Campaigns scheduled for multiple dates
- Campaign scheduled for multiple dates 
- Recurring campaign

> 🚧 Campaign Time Overlap
> 
> If you have the Best Time campaign scheduled for the present day, you cannot schedule a Fixed Time campaign for the next day to avoid campaign time overlap between two dates.

  c. Click **Done**.  
  d.  Select the _Best Time event_ under _Delivery preferences_ section or select _Ad hoc event_ to define the Best Time event here if not done earlier.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b2581a5-Select_Best_Time_Event.gif",
        null,
        "Select Best Time Event"
      ],
      "align": "center",
      "border": true,
      "caption": "Select Best Time Event"
    }
  ]
}
[/block]

  e. Select the _Fallback time frame_ if the best time is unavailable for the users or the user has not performed the selected event in the last 180 days.  
  f. Set up the remaining fields under the _When_ section of the campaign and click **Done**.

The campaign is now ready to publish.

# Create Best Time Journeys

For campaigns following a past behavior segment, messages can be delivered at the best time with any of the following channels: [email](doc:email), [push notifications](doc:push), [web push](doc:web-push), and [SMS](doc:SMS).

1. [Set Up the Best Time Event](doc:best-time-campaign-ui-enhancements#set-up-best-time-event).
2. [Create Journeys with Best Time Feature](doc:best-time-campaign-ui-enhancements#create-journeys-with-best-time-feature).

## Create Journeys with Best Time Feature

To create journeys using the Best time feature:

1. [Create a journey](https://docs.clevertap.com/docs/journeys) as per your requirement.
2. Click on the ![Timer](https://files.readme.io/834daaa-Timer_icon.png) icon between the segment and the consecutive message node.
3. Select the _Best time_ option to send a message at the best time. Currently, you can create journeys using the default Best Time config. So, it is mandatory to mark one of the Best Time configs as Default to refer to it later.
4. Click **Save & Close**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5660e8b-4_Click_sleep_time.png",
        "4 Click sleep time.png",
        1547
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



# Advanced Options

If _Best Time_ is chosen as the delivery option, the following advanced options are applicable:

- User time zone: Considering the _Best Time_ feature chooses the time when the user is most active, the [user time zone](https://docs.clevertap.com/docs/notification-delivery-options#section-delivery-in-user-s-timezone) is always implicitly applied.
- Global throttle limits: Cannot be applied with the _Best Time_ feature.