---
title: Best Time Campaign
excerpt: >-
  Learn how you can optimize the campaign conversion rates using the Best Time
  Campaign feature
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

_Best Time_ is a feature that identifies the contextual Best Time for users. This ensures that each user receives messages at the most opportune moments, tailored to their individual contexts. This optimizes the message send-time for each user based on their time zone and the period they are most active with your application. These time-based messages help achieve the following for the Campaigns and Journeys built using the Best Time feature:

* Increased Engagement
* Personalized Experience
* Improved Conversion Rates

# Best Time Overview Video

Learn how to send campaigns based on contextual Best Time for users with a sample use case.

<HTMLBlock>{`
<div
              style="
                position: relative;
                padding-bottom: 56.25%;
                height: 0;
                border-radius: 0;
                box-shadow: 0 15px 40px rgba(63,58,79,.3);
                overflow: hidden;
                min-width:320px"><iframe
              src="https://clevertap.portal.trainn.co/share/nFqLzQnNpQ3vd5hgBHmiyg/embed?autoplay=false"
              frameborder="0"
              webkitallowfullscreen
              mozallowfullscreen
              allowfullscreen
              allow="autoplay; fullscreen"
              style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
`}</HTMLBlock>

<br />

It enables you can create a Best Time Config based on the event and its properties. The Best Time Config refers to an event that triggers the determination of the best time to send a notification to your users. Thereby ensuring the optimal time to send messages or notifications to individual users based on their historical behavior and engagement patterns.

With this feature, you can:

* Configure up to 10 different configurations based on specific event filters along with the properties.
* View the distribution of optimal times for your users, thereby maximizing the impact of the campaigns.
* Select a fallback time for those without a clear best time.

<Image align="center" alt={2122} border={true} width="smart" src="https://files.readme.io/aeedcd6-Best_Time_Campaigns.png" title="Best Time Campaigns.png" className="border" />

# How It Works

CleverTap identifies the best time based on a selected config. The  _Best Time_ campaigns are sent by splitting a day into 12 buckets of two hours each in absolute clock time. The users are then assigned to one of these buckets based on their contextual Best Time. The user is then sent the campaign or journey in that two-hour window. If any user has not performed the selected event in the last 180 days, you can identify the fallback time for sending the campaign based on the user distribution graph.

For example, you want to send personalized discount offers to your users based on the Product Viewed in the last 180 days. With the Best Time feature, you can optimize the timing of these messages to maximize user engagement and conversion rates based on user distribution.

<Image align="center" alt="Sample Best Time Config" border={true} caption="Sample Best Time Config" src="https://files.readme.io/a8a4f2d-Sample_Best_Time_Config.png" width="75% " />

> 👍 Bucket Example
>
> For example, if a _Best Time_ campaign is created on January 1 at 5:15 PM, the campaign will start running based on the upcoming best time slot i.e. 6 P.M. and the users will receive campaigns based on the slot in which they are most active on the application.

> 📘 Best Time Campaign Handling During DND
>
> If the Best Time bucket coincides with the DND period defined by the user, then the campaign message is discarded.

# Create Best Time Campaigns

This is a two-step process that includes the following steps:

1. [Set Up the Best Time Config](https://docs.clevertap.com/docs/best-time#set-up-best-time-event).
2. [Create a Campaign using the Best Time feature](https://docs.clevertap.com/docs/best-time#create-a-campaign-using-the-best-time-feature).

## Set Up Best Time Config

You can configure the best time option for one-time or recurring campaigns for **Email**, **SMS**, **Push**, **WhatsApp**, and **Web Push** channels. To set up Best Time campaigns:

1. Navigate to _Settings_ > _Setup_ > _Best Time_ from the CleverTap dashboard.
2. Click **+ Best-Time Config**.

<Image align="center" alt="Set Up Best Time Event " border={true} caption="Set Up Best Time Event" src="https://files.readme.io/8a845b3-Set_Up_Best_Time_Event.png" />

3. Enter the _Config name_ to uniquely identify the Best Time event.
4. Select the system/custom event for which you want to define the Best Time campaign.
5. Click **+ Filter** to target a particular set of users for the campaign.  
   Consider an example where you want to send Best Time campaigns to users who have performed the _Added To Cart_ event for the product _Ironman Helmet_ on their mobile devices.
6. (Optional) Click **Preview User Distribution** to check the user distribution for the selected event in the last 180 days. You can also change the filter based on the user distribution to achieve optimal conversion rates.

<Image align="center" alt="Define Best Time Config" border={true} caption="Define Best Time Config" src="https://files.readme.io/de72691-Define_Best_Time_Config.gif" />

7. Click **Save** to save the Best Time event.

Currently, you can create journeys using the default Best Time config. So, it is mandatory to mark one of the Best Time configs as Default to refer to it later. You can do so by clicking the ![](https://files.readme.io/3b92fb0-Ellipses.png) icon and selecting _Mark as Default_.

<Image align="center" alt="Marking Best Time Event as Default" border={true} caption="Marking Best Time Event as Default" src="https://files.readme.io/612bfbe-Mark_as_Default.png" />

Similarly, you can also delete a particular Best Time event by clicking the ![](https://files.readme.io/3b92fb0-Ellipses.png) icon and then selecting _Delete_.

> 📘 Default Best Time Events
>
> The default Best Time events cannot be deleted. Also, deleting such events does not impact the already running campaigns.

## Create a Campaign using the Best Time Feature

Here, consider an example of the Best Time email campaign. To create a campaign with this feature, perform the following steps:

1. Navigate to _Campaigns_ from the CleverTap dashboard.
2. Click **+ Campaign**.

<Image align="center" alt={1571} border={true} caption="Create a Campaign" title="2x Create a campaign.png" src="https://files.readme.io/5de46d2-2x_Create_a_campaign.png" />

3. Select _Email_ from the list of messaging channels.

4. Define all the following information for the campaign:

   * Qualification Criteria
   * Email Service Provider
   * Campaign Goal
   * Who
   * What

   For more information about configuring the above details on the CleverTap dashboard, refer to [Create Email Campaign](doc:create-message-email).

5. Define the Best Time campaign schedule:  
   a. From the _When_ section of the campaign, select _Schedule for later_ or _Set as Recurring_ under the Data and time section, depending on the nature of your campaign.  
   b. Select the date to send the campaign and select _Best time for every user_ from the dropdown.

<Image align="center" alt={1332} border={true} caption="Define Best Time Campaign Schedule" title="Select Best Time option.gif" src="https://files.readme.io/d60c6db-Select_Best_Time_option.gif" />

Best Time feature works with the following campaign types:

* One-time campaign, which is scheduled for a later time
* Campaigns scheduled for multiple dates
* Campaign scheduled for multiple dates
* Recurring campaign

> 🚧 Campaign Time Overlap
>
> If you have the Best Time campaign scheduled for the present day, you cannot schedule a Fixed Time campaign for the next day to avoid campaign time overlap between two dates.

c. Click **Done**.  
d.  Select the _Best Time event_ under the _Delivery preferences_ section or select _Ad hoc event_ to define the Best Time event here if not done earlier.

<Image align="center" alt="Select Best Time Event" border={true} caption="Select Best Time Event" src="https://files.readme.io/b2581a5-Select_Best_Time_Event.gif" />

e. Select the _Fallback time frame_ if the best time is unavailable for the users or the user has not performed the selected event in the last 180 days.

> 🚧 Fallback Time Frame
>
> Ensure that the fallback time frame that you set up does not overlap with the designated Do Not Disturb (DDND) hours configured for the campaign.

The campaign is now ready to publish.

# Create Best Time Journeys

For campaigns following a past behavior segment, messages can be delivered at the best time with any of the following channels: [email](doc:email), [push notifications](doc:push), [web push](doc:web-push), and [SMS](doc:SMS).

1. [Set Up the Best Time Event](doc:best-time#set-up-best-time-event).
2. [Create Journeys with Best Time Feature](doc:best-time#create-a-campaign-using-the-best-time-feature).

## Create Journeys with Best Time Feature

To create journeys using the Best time feature:

1. [Create a journey](https://docs.clevertap.com/docs/journeys) as per your requirement.
2. Click on the ![](https://files.readme.io/834daaa-Timer_icon.png) icon between the segment and the consecutive message node.
3. Select the _Best time_ option to send a message at the best time. Currently, you can create journeys using the default Best Time config. So, it is mandatory to mark one of the Best Time configs as Default to refer to it later.
4. Click **Save & Close**.

<Image align="center" alt={1547} border={true} caption="Define Delivery Options" title="4 Click sleep time.png" src="https://files.readme.io/5660e8b-4_Click_sleep_time.png" />

# Advanced Options

If _Best Time_ is chosen as the delivery option, the following advanced options are applicable:

* User time zone: Considering the _Best Time_ feature chooses the time when the user is most active, the [user time zone](https://docs.clevertap.com/docs/notification-delivery-options#section-delivery-in-user-s-timezone) is always implicitly applied.
* Global throttle limits: Cannot be applied with the _Best Time_ feature.

# External Best Time (User Property)

External Best Time lets you schedule campaign delivery based on a time value provided per user, instead of CleverTap’s system-calculated Best Time. This is useful when you already compute optimal send times using your own models or data pipelines.

> 📘 Private Beta
>
> Currently, this feature is a Private Beta Release. If you want access to this feature, contact your Account Manager.

## When should you use this?

Use External Best Time if:

* You already calculate the best send time for each user outside CleverTap.
* You want CleverTap to deliver messages exactly at the time you provide for each user.
* You want to avoid creating multiple time-based campaigns or segments.

## How External Best Time works / Campaign setup

To use the External Best Time feature:

1. Pass a **time value** as a user property in the user profile. The value represents the exact time at which the message should be sent for that user.
2. When configuring the Send Time for a campaign:
   1. Select **External Best Time (User Property)** as the send-time option. @ss
   2. Choose the user property that contains the time value. @ss
   3. Add the Start time (mandatory) and End time (optional). If End Time is not specified, the campaign runs for **24 hours**. CleverTap sends the message to each user based on the time stored in that property.

<Callout icon="📘" theme="info">
  ## Note

  * This option is available for Past Behaviour Campaigns.
  * Campaign-level throttling and limits apply as usual.
  * External Best Time uses the account timezone, not the user’s local timezone.
  * The send time is locked in when the campaign begins running. The message delivery is not affected by the updates made to the user property after dispatch begins.
  * Supported time format:
    * The user property must be passed in the following 24 hour format: `HH:MM` For example,`09:30` or `18:45`.
    * Seconds are not supported.
</Callout>

## Fallback behavior

You can configure how CleverTap should proceed when the External Best Time value cannot be applied for a user. If the selected user property is missing or contains an invalid value, you can choose to send the message immediately (default behavior), use CleverTap Best Time, or skip the user entirely.

If the External Best Time has expired or already passed for the current day, you can choose to send the message at a specific time, deliver it at the same time on the next day, or discard the message for that user.

<br />
