---
title: Notification Delivery Options
excerpt: Understand how to choose from various delivery preferences.
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

CleverTap provides the capability of delivering notifications in the user’s timezone while creating scheduled campaigns or journeys. This is a relevant feature for businesses having international users and who want to send time-sensitive notifications to their users. If you select this option, CleverTap staggers the delivery of notifications and qualifies users according to their timezone.

<Image title="Timezone.png" alt={1020} className="border" width="smart" border={true} src="https://files.readme.io/10fa2dd-Timezone.png" />

# Use Case

A marketer in San Francisco (Pacific Time) creates a campaign at 4:14 PM in their CleverTap dashboard. The campaign is scheduled to deliver messages to users at 8:00 PM in their local timezone.

At 5:00 PM Pacific Time (account’s timezone), the first set of messages will deliver to users on the East Coast (8:00 PM in the Eastern timezone). One hour later (6:00 PM Pacific or 8:00 PM Central Time), the second set gets delivered to anyone qualifying in this timezone. Two hours after that (8:00 PM Pacific), the next set is delivered to users on the West Coast, and so forth. A campaign executes for timezones around the globe delivering messages to users qualifying for each timezone.

After the marketer finishes creating the campaign, it moves into a scheduled state. Once the campaign starts executing, it moves into a running state where you can see that the campaign is scheduled to deliver in the user's timezone on the overview page. 

# User Timezone for Campaigns

Set the users' timezone via the Tz key in the profile update push.

To set up a campaign for message delivery in the user’s timezone:

1. From the dashboard, navigate to *Campaigns*. 
2. Click **+ Campaign**.
3. Select a messaging channel.

<Image title="2x Create a campaign.png" alt={1571} className="border" border={true} src="https://files.readme.io/5de46d2-2x_Create_a_campaign.png" />

4. Navigate to *When* > *Delivery preferences*.
5. Select *Timezone*.
6. Select a delivery option: *Drop the campaign* or *Deliver the campaign the next day*.
7. Click **Done**.

## How the Delivery Options Work 

The following example involves a marketer located in the Midwest (Central Time). At 11:30 AM, a lunchtime campaign has been scheduled to be delivered in each user’s local time. The campaign start time is set to 12:00 PM and the first set of messages will go out at noon Central Time. Two hours later, West Coast users receive the campaign.

Since this campaign was initiated at 11:30 AM Central, it was already 12:30 PM Eastern Time which is after the specified delivery time for the East Coast users.

The campaign continues to deliver messages each timezone moving from East to West until it reaches the first timezone.

If you select *Drop the campaign*, any user whose timezone has already passed when the campaign kicked off will not receive this campaign.

If you selected *Deliver the campaign the next day*, then the campaign runs for timezones around the globe and eventually delivers the campaign to the East Coast users at noon (Eastern Time) the next day.

> 📘 Critical Delivery Dates
>
> If it is critical for a campaign to be delivered on a certain calendar day (e.g., an Easter campaign) and the message has to arrive on Easter Sunday or not at all, choose the *Drop the campaign* option.

# Do Not Disturb Hours

CleverTap provides the option for setting the Do Not Disturb hours for notification delivery while creating a campaign. You can set this to ensure that the users who get qualified for the campaign are not disturbed during the specified DND hours.

If a user qualifies for a notification in DND hours, you can decide to completely discard the notification or specify to deliver the notification to the user after the end of DND hours.

<Image title="DND_doc.png" alt={1766} className="border" border={true} src="https://files.readme.io/d436c32-DND_doc.png" />

## Set DND for Mobile Push, SMS, Email, Web Push, or WhatsApp

To set DND for mobile push, SMS, email, web push, or WhatsApp campaigns, perform the following steps:

1. From the new campaign page, navigate to *When* > *Delivery preferences*. 
2. Select the *Do Not Disturb (DND)* checkbox to display the DND options. 
3. Select the days and input the times you do not want to send campaign notifications. If you want to use the same time inactive period for each day, click the *Copy Time To All* link.
4. Select a message handling type.
5. Click **Done**.

<Image title="DND_Options.png" alt={446} className="border" border={true} src="https://files.readme.io/a1bd274-DND_Options.png" />

# Campaign Frequency for Mobile In-App or Web Pop-up

Campaign frequency provides the ability to define when the user qualifies for a message. If a user qualifies outside this window, the message is discarded.

To set campaign frequency for mobile In-App or web popup campaigns, perform the following steps: 

1. Under *When* select the **Set frequency** checkbox.

2. Select the days and input the times you do not want to send campaign notifications. If you want to use the same time inactive period for each day, click **Apply to all**.

3. Select **Deliver how often** from the available options.

<Image title="Campaign_frequency.png" alt={617} className="border" border={true} src="https://files.readme.io/fce5d09-Campaign_frequency.png" />

4. **Click** Done\*\*.

# Campaign Cut-off

CleverTap gives the option for setting the campaign cut-off time for every scheduled campaign while creating it. You can set this to ensure that the delivery of notifications is stopped after the specified cut-off time. This is useful if the campaign is time-sensitive and if the notification will not be relevant later.

<Image title="Campaign_Cut_Off.png" alt={472} className="border" border={true} src="https://files.readme.io/9a38d84-Campaign_Cut_Off.png" />

# Message Frequency Caps

If you have multiple marketing campaigns running simultaneously for any one channel, the same user may qualify to receive a message from more than one campaign in a given day, week, or month. Frequency caps provide you the capability to limit the number of notifications a user will receive from all the campaigns running for that channel.

Frequency is channel-specific. Frequency caps let you limit the total notifications received in a given timeframe for one delivery channel and not across all the channels as a whole.

To set frequency caps, navigate to **Settings** > *Engage* > **Setup** > **Campaign Limits**:

<Image title="564c098-Screenshot_2020-06-09_at_9.01.49_PM.png" alt={984} className="border" border={true} src="https://files.readme.io/20ad6dc-564c098-Screenshot_2020-06-09_at_9.01.49_PM.png" />

## Error Reporting with Frequency Caps

In the error reporting section of the campaign report, you can find the number of users who did not receive the campaign because of this frequency cap setting.

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Non-technical Errors
      </th>

      <th>
        Android
      </th>

      <th>
        iOS
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Frequency Caps Exceeded
      </td>

      <td>
        1158
      </td>

      <td>
        73
      </td>
    </tr>

    <tr>
      <td>
        Profile not reachable
      </td>

      <td>
        237
      </td>

      <td>
        0
      </td>
    </tr>

    <tr>
      <td>
        Undelivered Due to App Uninstall
      </td>

      <td>
        351
      </td>

      <td>
        120
      </td>
    </tr>

    <tr>
      <td>
        Count
      </td>

      <td>
        1746
      </td>

      <td>
        193
      </td>
    </tr>
  </tbody>
</Table>
