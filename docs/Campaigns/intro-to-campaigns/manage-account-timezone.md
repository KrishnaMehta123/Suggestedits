---
title: Manage Account Timezone
excerpt: Learn how to manage account timezone from the CleverTap dashboard
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

A timezone is a geographical region where all locations observe the same standard time. CleverTap uses the timezone to ensure that data and events recorded in the platform are aligned with the local time of the end users.

# Change Account Timezone

A change in the timezone can impact the metrics on a dashboard that tracks events with timestamps and campaigns based on account timezones.

For example, if your account timezone is set to *(GMT+5:30) Asia/Kolkata* (an Indian Standard Time) on the dashboard and a campaign is scheduled to run every day at 7:00 AM in the *(GMT+5:30) Asia/Kolkata* timezone, CleverTap will deliver the message at 9:30 PM for the users situated in *(GMT-8:00) US/Pacific* timezone (a Pacific Standard Time) because IST is always 14:30 hours ahead of PST. This can result in the campaign running at different times or skipping a day, depending on how the dashboard handles the change in the timezone.

(@bajrang: This example is not valid for changing a timezone - this is basically the difference in account timezone and the user's timezone - which is not the case here. We need to describe the impact of changing the account timezone from one timezone to another.)

Similarly, events with timestamps will be impacted by a change in timezone, as the timestamp will be displayed differently in the new timezone. For example, if an event with a timestamp of 7:00 AM IST occurs, it will be recorded as having occurred at 9:30 PM PST.\
(@bajrang - Same comment as above.)

> 📘 Note
>
> If you use the account timezone while sending the campaigns, the message will be delivered to the *Account Timezone* set from your dashboard. If you want to deliver your campaigns' messages in the user's timezone, you must use the *User Timezone* option. To know more about the usage of Account and User timezones, refer to [Notification Delivery Options](doc:notification-delivery-options#overview).
>
> (@Bajrang - this note is not at all clear - Discuss this with me.)

## Change in CleverTap Timezone

Changing the account timezone from the CleverTap dashboard changes all the user data times into the respective timezone, and the analytics and engagement metrics also change. It also changes the timestamps of the events on the CleverTap dashboard. The campaigns and events will be displayed differently in different timezones, leading to confusion and inaccuracies in the metrics. Still, if you want to change the account timezone to meet your business use case, you can change it from the CleverTap dashboard.\
(@Bajrang - not at all clear.)

To change the account timezone:

1. Navigate to *Settings* > *Project* and click the \**Edit Icon* for Timezone.

<Image title="Timezone.png" alt={2510} className="border" border={true} src="https://files.readme.io/c43440c-Timezone.png" />

2. Select the timezone of your account.

<Image title="Change Timezone.png" alt={2114} className="border" border={true} src="https://files.readme.io/7a572f8-Change_Timezone.png" />

3. After selecting the timezone, click **Change**.

(@Bajrang: What happens after this - do we show any warning that it can impact the already running campaigns and journeys on the UI before changing the timezone - or we directly change it?) 

# FAQs

## Q. What happens on changing the timezone again?

If you change the timezone again, the impact on the metrics on your dashboard will depend on the new timezone that you set. The campaigns and events will be displayed based on the new timezone, and the timestamps will be adjusted accordingly.

(@Bajrang: let's discuss this with the PM.)

Similarly, events with timestamps will be displayed based on the new timezone, and their timestamps will be adjusted accordingly. It is important to note that changing the timezone will not change the actual time the events or campaigns took place; it will only affect how they are displayed in the dashboard.

## Q. What would happen to the exports?

A time zone change will also impact exports from the dashboard containing timestamps. The exported data will reflect the new timezone, and the timestamps will be adjusted accordingly.

It is important to consider the impact of a change in a timezone on exported data, especially if the data will be used for analysis or shared with others who may be in a different timezone. In such cases, it may be necessary to include information about the original timezone or to convert the timestamps to a common timezone to ensure that the exported data is accurately understood and usable.

## Q. What happens if the end user's timezone differs from the dashboard's account timezone?

Suppose a user's local timezone differs from the account timezone set on the dashboard. In that case, they will see timestamps and campaigns displayed based on their local timezone rather than the account timezone.\
For example, an account timezone is set as 11 AM on the dashboard as per the India region. Now if you send a campaign to the users sitting in Singapore, they will receive the message at 1:30 PM as Singapore is 2:30 hours ahead of India. This can lead to confusion and inaccuracies, as the same event or campaign may occur at a different time for different users, depending on their local timezone.\
(@Bajrang - Let's discuss this with the PM.)
