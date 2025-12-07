---
title: Best Time Campaigns (COPY) _for amrita review
excerpt: Time your messages to maximize conversion.
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

*Best Time* is an intelligent feature that learns from your user's activity over period\<\<@amrita, do we know how long it takes to learn?>> and recommends the most optimal time for each user in a  campaign or a journey. This optimizes the message send-time for each user based on their time zone and the period of the day \<\<@amrita please verify this>> when they are most active in your application. These time-based messages improve the conversion rates for the campaigns and Journeys built using the Best Time feature.

<Image title="Best Time Campaigns.png" alt={2122} align="center" className="border" width="smart" border={true} src="https://files.readme.io/aeedcd6-Best_Time_Campaigns.png" />

# How It Works

CleverTap identifies the best time based on a selected event.\
The  *Best Time* campaigns are sent by splitting a day into 12 buckets of two hours each. The users are then assigned to one of these buckets based on the time of the day they are most active on the app. The user is then sent a campaign or journey in that two-hour window.\
If any user has not performed the selected event in the last 180 days, you can choose the time you want to send the campaign based on the user distribution. \<\<@amrita, did not understand this sentence>>

> 👍 Bucket Example
>
> For example, if a *Best Time* campaign is created on January 1 at 5:15 PM, the users will start receiving the campaigns based on the upcoming best time bucket.  The users who are most active in that bucket will receive the message.

> 📘 Best Time Campaign Handling During DND
>
> If the Best Time bucket coincides with the DND period defined by the user then the campaign message is discarded.

# Create Best Time Campaigns

This is a two-step process that includes the following steps:

1. [Set Up the Best Time Event](doc:best-time-campaign-ui-enhancements#set-up-best-time-event). 
2. [Create a Campaign using the Best Time feature](doc:best-time-campaign-ui-enhancements#create-a-campaign-using-the-best-time-feature).

## Set Up Best Time Event

You can configure the best time option for one-time or recurring campaigns for **Email**, **SMS**, **Push**, **WhatsApp**, and **Web Push** channels. To set up Best Time campaigns:

1. Navigate to *Settings* > *Setup* > *Best Time* from the CleverTap dashboard.
2. Click **+ Best-Time Config**.

<Image alt="Set Up Best Time Event " align="center" border={true} src="https://files.readme.io/8a845b3-Set_Up_Best_Time_Event.png">
  Set Up Best Time Event 
</Image>

3. Enter the *Config name* to uniquely identify the Best Time event. 
4. Click **Charged** to select the system/custom event for which you want to define the Best Time campaign. \<\<@amrita, this sentence is wrong. The user has to select the event for best time from here. it doesnt necessarily be charged>>>
5. Click **+ Filter** to target a particular set of users for the campaign.\
   Consider an example where you want to send Best Time campaigns to users who have performed the *Added To Cart* event for the product *Ironman Helmet* on their mobile devices.
6. (Optional) Click **Preview User Distribution** to check the user distribution for the selected event in the last 180 days. You can also change the filter based on the user distribution to achieve optimal conversion rates. \<\<@amrita, what is the benefit of doing this ?>>>

<Image align="center" className="border" border={true} src="https://files.readme.io/de72691-Define_Best_Time_Config.gif" />

7. Click **Save** to save the Best Time event.

You can mark a particular Best Time event as Default by clicking the ![lEllipses](https://files.readme.io/3b92fb0-Ellipses.png) icon and then selecting *Mark as Default*. These default events are used when creating Journeys for Best Time delivery. So, it is mandatory to mark the required Best Time event as default to refer to it later. \<\<@amrita, rephrase this sentence. it is circular>>

<Image title="Mark as Default.png" alt={1800} align="center" className="border" border={true} src="https://files.readme.io/ac06a17-Mark_as_Default.png" />

Similarly, you can also delete a particular Best Time event by clicking the ![lEllipses](https://files.readme.io/3b92fb0-Ellipses.png) icon and then selecting *Delete*. \<\<@amrita, what happens to the running campaigns when you delete this event ?>>>

> 📘 Default Best Time Events
>
> The default Best Time events cannot be deleted. Also, deleting such events does not impact the already running campaigns.

## Create a Campaign using the Best Time Feature

Here, consider an example of the Best Time email campaign. To create a campaign with this feature, perform the following steps:

1. Navigate to *Campaigns* from the CleverTap dashboard.
2. Click **+ Campaign**.
3. Select *Email* from the list of messaging channels.
4. Define all the following information for the campaign:

   * Qualification Criteria
   * Email Service Provider
   * Campaign Goal
   * Who
   * What

   For more information about configuring the above details on the CleverTap dashboard, refer to [Create Email Campaign](doc:create-message-email).

<Image title="2x Create a campaign.png" alt={1571} align="center" className="border" border={true} src="https://files.readme.io/5de46d2-2x_Create_a_campaign.png" />

5. Define the Best Time campaign schedule:\
   a. From the *When* section of the campaign, select *Schedule for later* or *Set as Recurring* under Data and time section, depending on the nature of your campaign.\
   b. Select the date to send the campaign and select *Best time for every user* from the dropdown.

<Image title="Select Best Time option.gif" alt={1332} align="center" className="border" border={true} src="https://files.readme.io/d60c6db-Select_Best_Time_option.gif" />

   Best Time feature works with the following campaign types:

* One-time campaign, which is scheduled for a later time
* Campaigns scheduled for multiple dates
* Campaign scheduled for multiple dates 
* Recurring campaign

> 🚧 Campaign Time Overlap
>
> If you have the Best Time campaign scheduled for the present day, you cannot schedule a Fixed Time campaign for the next day to avoid campaign time overlap between two dates.

  c. Click **Done**.\
  d.  Select the *Best Time event* under *Delivery preferences* section or select *Ad-hoc event* to define the Best Time event if not done earlier.

<Image title="Select Best Time event.gif" alt={1072} align="center" className="border" border={true} src="https://files.readme.io/63f7f62-Select_Best_Time_event.gif" />

  e. Select the *Fallback time frame* if the best time is unavailable for the users.\
  f. Set up the remaining fields under the *When* section of the campaign and click **Done**.

The campaign is now ready to publish.

# Create Best Time Journeys

For campaigns following a past behavior segment, messages can be delivered at the best time with any of the following channels: [email](doc:email), [push notifications](doc:push), [web push](doc:web-push), and [SMS](doc:SMS).

1. [Set Up the Best Time Event](doc:best-time-campaign-ui-enhancements#set-up-best-time-event).
2. [Create Journeys with Best Time Feature](doc:best-time-campaign-ui-enhancements#create-journeys-with-best-time-feature).

## Create Journeys with Best Time Feature

1. Create a journey to set up a message to deliver at the best time. For more information, refer to [Journeys](doc:journeys). 
2. Click on the ![Timer](https://files.readme.io/834daaa-Timer_icon.png) icon between the segment and the consecutive message node.
3. Select the *Best time* option to send a message at the best time. In the case of journeys, the Best Time event is the same as the default event defined under the *Settings* > *Setup* > *Best Time* page.
4. Click **Save & Close**.

<Image title="4 Click sleep time.png" alt={1547} align="center" className="border" border={true} src="https://files.readme.io/5660e8b-4_Click_sleep_time.png" />

# Advanced Options

If *Best Time* is chosen as the delivery option, the following advanced options are applicable:

* User time zone: Considering the *Best Time* feature chooses the time when the user is most active, the [user time zone](https://docs.clevertap.com/docs/notification-delivery-options#section-delivery-in-user-s-timezone) is always automatically applied.
* Global throttle limits: Cannot be applied with the *Best Time* feature. \<\<@amrita, is this still true ?>>
