---
title: Campaign Overview
excerpt: Understand how to engage with users through Campaigns.
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

Marketing campaigns promote products through different types of media. They are designed with different goals in mind, including building a brand image, introducing a new product, and increasing sales of an existing product.  
Defining a campaign's goal usually dictates how much marketing is needed and what media are most effective for reaching a specific segment.

# Messaging Channels

CleverTap offers different messaging channels that enable creating engagement strategies to reach your users with a personalized message at the right time. 

### [Push](doc:push)

Push notifications enable you to communicate with your users when they are not in your app. Depending on the platform and user configuration, these messages appear on a user's lock screen or in a top/bottom banner. 

### [In-App Messages](doc:in-app)

In-app messages are pop-up messages that are shown to the user while they are in your app. While the user views push notifications outside the app, in-app notifications are viewed inside the app.  
In-app notifications are great for showing contextual messages, such as discount offers while the user is within the app or communicating with users who have turned off push notifications.

### [App Inbox](doc:app-inbox)

App Inbox is a messaging channel that provides the ability to deliver rich, individually customized content to your users. Messages sent to the App Inbox get saved on the user's device. 

### [Email](doc:email)

In CleverTap, you create the email content, specify the target audience, and determine when the campaign activates. CleverTap delivers the email messages to the third-party [email service provider](doc:email-partners) of your choosing via a simple configuration in the Dashboard.

### Web Channels

**[Web Push](doc:web-push)**  
Web Push notifications are browser-based messages you can send to your desktop or mobile web users even if they are not currently visiting your website. 

**[Web Pop-up](doc:web-pop-ups)**  
Web pop-ups are interstitial messages displayed to the user while they are on the desktop or mobile website.

**[Web Exit Intent](doc:web-exit-intent-overview) **  
Exit Intent messages are similar to Web Pop-ups, except they are triggered when a user navigates away from your website.

### [Native Display](doc:native-display)

Native Display provides the ability to embed content natively within your app screen without interrupting the app experience. It also provides the ability to change your app's content dynamically and deliver relevant and contextual content to your users.

### [Webhooks](doc:webhooks-overview)

CleverTap webhooks enable developers to monitor specific user events and receive push notifications to their servers when those events happen. Each qualified user's details are sent to the endpoint, which exports data to a third-party system.

### [SMS](doc:sms)

SMS notifications enable you to send short communication to your users, such as one-time passwords to authorize their use of the app or even links allowing the users to download the latest version of the mobile app.

### Remarketing Channels

**[Facebook Audiences](doc:facebook-audiences)**  
Facebook Custom Audience is a great way to re-engage your users outside of your app through ads on Facebook. The Facebook Audience module on the CleverTap Dashboard makes it easy to set up Facebook Audience ads for all your users or specific user segments. You can create segments based on past user behavior, user properties, or a combination of past user behavior and properties. 

**[Google Adwords](doc:google-adwords)**  
Remarketing with Google Ads is a great way to re-engage with users outside your app or website via the Google Ads network.

**[TikTok Remarketing](doc:tiktok-remarketing)**

Leveraging TikTok's audience can significantly enhance remarketing efforts as it offers a highly engaged and diverse user base. Using TikTok's advanced targeting capabilities, marketers can retarget users who have previously interacted with the content or shown interest in similar products. This targeting is based on the user's past events and interactions, allowing for more relevant messaging. CleverTap's segmentation capabilities allow you to create and export target audiences to TilkTok based on your business goals.

# Campaigns

You can create new campaigns and view existing ones under **Campaigns**, which is available in the left pane. Once a campaign is published, you can stop it but cannot pause it. 

## Campaigns Operations

You can perform different actions on the campaigns from the _ All Campaigns _ page. The following sections briefly discuss each operation.

### Filter Campaigns

You can quickly search your campaigns by applying the required filters. To do so: 

1. Navigate to _Messages_ > _Campaigns_ from the CleverTap dashboard. The _All Campaigns_ page opens.
2. Click the ![](https://files.readme.io/ac0ed6a-Filter_icon.png) icon. The Filter Campaigns window opens on the right side of the screen.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fbf5087fbe1294fd42ffd5cb82fd3af9a700ac6acf9d276225ad5365e6fc93ce-Filter_Campaigns.png",
        "",
        "Filter Campaigns"
      ],
      "align": "center",
      "border": true,
      "caption": "Filter Campaigns"
    }
  ]
}
[/block]


3. Select from the following filters and click **Apply**:
   - **Channel**: Filters based on the type of messaging channel used. The following are the available options: Email, SMS, Push Notifications, Mobile In-app, Web, Audiences, Web Push, Webhooks, Google Ads,  App Inbox, WhatsApp, Partner, Native Display, and Web Native Display.
   - **Type**: Filters based on the type of campaign. The campaign can be a Single Message, A/B Test, or Message on user property type of campaign.
   - **Status**: Filters campaign based on the current status of the campaign. The following are the possible statuses: Scheduled, Running, Stopped, Completed, Draft, Awaiting Next Run, Approval Pending, and Rejected. For more information, refer to [Campaign States](doc:intro-to-campaigns#campaigns-status).
   - **Created by:** Filters based on the email ID of the person who created the campaign.
   - **Label**: Filters based on the labels assigned to the campaigns.
   - **Delivery**: Filters based on the delivery type of the campaign. The following are the available options: One Time, Inaction, Action, On a date/time, Recurring, API, and Multiple Date.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/80bdbc6-Apply_Campaign_Filter.gif",
        "",
        "Apply Campaign Filters"
      ],
      "align": "center",
      "border": true,
      "caption": "Apply Campaign Filters"
    }
  ]
}
[/block]


All the campaigns that meet the criteria are listed under the _All Campaigns_ page. Also, you can save the filter by clicking the _Save Filter_ link.

You can also apply quick filters from the top of the _All Campaigns_ page.

### Archive Campaigns

Archiving campaigns helps to keep your CleverTap account organized and clutter-free, making it easy to find and view the campaigns you want. To do so:

1. Go to _Messages_ > _Campaigns_ from the CleverTap dashboard. The _All Campaigns_ page opens.
2. Select the campaigns you may want to archive and click the ![](https://files.readme.io/b46b84b-Archive_icon.png) icon.
3. Click **Save** to archive the selected campaigns or click **Cancel** to undo the action.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/65f3a7d89e189d529f8e9017160947cf6ca85a38901927ebc060e9984b47aa9a-Archive_Campaigns.gif",
        "",
        "Archive Selected Campaigns"
      ],
      "align": "center",
      "border": true,
      "caption": "Archive Selected Campaigns"
    }
  ]
}
[/block]


### Archival Behavior

[block:parameters]
{
  "data": {
    "h-0": "**Behavior**",
    "h-1": "**Description**",
    "0-0": "**Auto-archival**",
    "0-1": "Campaigns in the _Completed_, _Stopped_, or _Draft_ state are automatically archived 6 months after their last active date. You cannot disable this behavior.<br><br>**Examples:**<br>• **Completed:** “Diwali 2024 – Push” completed on **Mar 10 2024**, auto-archived on **Sep 10 2024**.<br>• **Stopped:** “Summer Sale – Email” stopped on **Jan 15 2025**, auto-archived on **Jul 15 2025**.<br>• **Draft:** “Promo Dec 2024” created on **Dec 1 2024**, auto-archived on **Jun 1 2025**.<br><br>To reuse an auto-archived campaign, **clone it**, edit as needed, and publish the clone.",
    "1-0": "**View archived campaigns**",
    "1-1": "Toggle the **Archive Campaigns** filter on the _All Campaigns_ page to view archived items.",
    "2-0": "**Edit restrictions**",
    "2-1": "Archived campaigns (including drafts) are read-only. You can view details, but cannot edit or publish them. ",
    "3-0": "**Recovery method**",
    "3-1": "To continue working on an archived campaign, **clone** it. The clone is a new campaign that can be saved, scheduled, or published. "
  },
  "cols": 2,
  "rows": 4,
  "align": [
    null,
    null
  ]
}
[/block]


### Stop Campaigns

You may want to stop a particular campaign after monitoring and evaluating its efficacy. To do so:

1. Navigate to _Messages_ > _Campaigns_ from the CleverTap dashboard. The _All Campaigns_ page opens.
2. Select the running campaigns you may want to stop and click the ![](https://files.readme.io/c2fcde8-Stop_icon.png) icon.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e4ba1596611e5ec12b7ce1d2ba899ca33952b7a70206a9e9f9a193427fa73e1b-Stop_Campaigns.png",
        "",
        "Stop Selected Campaigns"
      ],
      "align": "center",
      "border": true,
      "caption": "Stop Selected Campaigns"
    }
  ]
}
[/block]


3. Click **Save** to archive the selected campaigns or click **Cancel** to undo the action.

### Clone Campaign

Cloning a campaign helps to create a new campaign from an already existing campaign with minor or no modifications. To do so:

1. Navigate to _Messages_ > _Campaigns_ from the CleverTap dashboard. The _All Campaigns_ page opens.
2. Select the running campaigns you may want to clone and click the ![](https://files.readme.io/e6ac3e4-Clone_icon.png) icon.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9d6d2ad-Clone_Campaigns.png",
        "",
        "Clone Selected Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Clone Selected Campaign"
    }
  ]
}
[/block]


3. Click **Save** to archive the selected campaigns or click **Cancel** to undo the action.

## Campaign States

Campaign Status helps track progress and manage campaigns efficiently. Each campaign state has distinct characteristics that determine what actions can be performed. The following are the campaign states:

- _Draft_: Indicates that the campaign is still not published.
- _Scheduled_: Indicates that the campaign is set to go live at a future time.
- _Awaiting Next Run_: Indicates that the recurring campaign is waiting for its next scheduled execution
- _Running_: Indicates that the campaign is actively being executed
- _Pending for Approval_: Indicates that the campaign with Creator Approver workflow is awaiting review and approval from the designated approver before it can be published or scheduled for execution
- _Rejected_: Indicates that the campaign with Creator Approver workflow is not approved by the designated approver.
- _Stopped_: Indicates that the campaign has been permanently halted.
- _Completed_: Indicates that the campaign has finished running and is no longer active.

For Campaigns Scheduled for Later, you can edit the following sections of the campaign: Who, What, and When.

For Live Campaigns Awaiting Next Run, you can edit the following: _What_ section, Campaign name, and Message labels.

For Campaigns with Creator Approver Workflow, refer to the following table:

| Campaign State           | Scenario                                           | Creator's Action                                                                                                                                                   | Approver's Action                                                                                                                                                                                                                                              |
| :----------------------- | :------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Scheduled **           | Before scheduled time                              | Can edit all campaign information and send it for approval.                                                                                                        | Can edit all campaign information and publish.                                                                                                                                                                                                                 |
|                          | After scheduled time                               | Cannot edit; popup indicating discarded changes displays                                                                                                           | Can only approve; popup indicating discarded changes..                                                                                                                                                                                                         |
|                          |                                                    |                                                                                                                                                                    |                                                                                                                                                                                                                                                                |
| **Awaiting Next Run**    | Before scheduled time                              | Can modify only the _What_ section and send it for approval.                                                                                                       | Can modify only the _What_ section and publish.                                                                                                                                                                                                                |
|                          | After scheduled time                               | Cannot edit; popup indicating discarded changes displays.                                                                                                          | Can only approve; popup indicating discarded changes.                                                                                                                                                                                                          |
|                          |                                                    |                                                                                                                                                                    |                                                                                                                                                                                                                                                                |
| **Running**              | During execution                                   | Can modify only the _What_ section of Live campaigns and send them for approval.                                                                                   | Can modify only the _What_ section of Live campaigns and publish.                                                                                                                                                                                              |
|                          |                                                    |                                                                                                                                                                    |                                                                                                                                                                                                                                                                |
| **Pending For Approval** | Before First run                                   | Can edit all campaign information before and after the scheduled time and send it for approval.                                                                    | <li>Can edit all the campaign information **before the scheduled time** and approve the campaign.</li><li>Popup indicating that the campaign was scheduled in the past time; The approver can edit all the campaign information and publish the campaign.</li> |
|                          | First run was completed, and awaiting the next run | Can only edit the _What_ section before the next scheduled time.                                                                                                   |                                                                                                                                                                                                                                                                |
|                          |                                                    | The creator can edit only the WHAT section **before the scheduled time** and send it to the approver for approval.                                                 | The approver can edit only the WHAT section **before the scheduled time** and publish the campaign.                                                                                                                                                            |
|                          |                                                    | If the creator tries to edit the campaign **after the scheduled time**, a popup opens. The popup indicates that the changes made by the creator will be discarded. | If the approver tries to edit the campaign **after the scheduled time**, a popup opens. The popup indicates that the changes made by the creator will be discarded.                                                                                            |
|                          |                                                    |                                                                                                                                                                    |                                                                                                                                                                                                                                                                |
| **Rejected**             | First run is yet to start                          | The creator can edit all the campaign information **before the scheduled time** and send it to the approver for approval.                                          | The approver can edit only the WHAT section **before the scheduled time** and send it to the approver for approval.                                                                                                                                            |
|                          |                                                    | The creator can edit all the campaign information **after the scheduled time** and send it to the approver for approval.                                           | If the approver tries to edit the campaign **after the scheduled time**, a popup opens. The popup indicates that the changes made by the approver will be discarded.                                                                                           |
|                          |                                                    |                                                                                                                                                                    |                                                                                                                                                                                                                                                                |
|                          | First run was completed, and awaiting the next run | The creator can edit only the WHAT section **before the scheduled time** and send it to the approver for approval.                                                 | The approver can edit only the WHAT section **before the scheduled time** and publish the campaign.                                                                                                                                                            |
|                          |                                                    | If the creator tries to edit the campaign **after the scheduled time**, they can edit only the WHAT section and send it to the approver for approval.              | The approver can only edit the WHAT section of the campaign after the scheduled time. Also, a popup indicates that the campaign can be run today or tomorrow.                                                                                                  |

## Campaign Reports

Selecting _Campaigns_ from the CleverTap Dashboard opens the Campaign Reports table where you can see all your campaigns across every channel in one consolidated view.

Campaign Reports include the channel, delivery status, and key statistics to assess and compare performance. 

Use quick filters to isolate campaigns of interest and the email report option to deliver a CSV file to your inbox that includes all the information in the table.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/04a4edc-Campaign_reports.gif",
        "Filter Campaigns and view Campaign reports on CleverTap dashboard.",
        1422
      ],
      "align": "center",
      "border": true,
      "caption": "Filter Campaigns and View Campaign Reports"
    }
  ]
}
[/block]


# Message Labels

Message Labels allow you to tag campaigns with descriptive names or themes. Once applied, labels allow you to group your various messaging campaigns so that you can view their performance or identify user behaviors.

For example, you can create a label called _Onboarding_ to identify all the messaging campaigns (across all channels) related to onboarding your new users. You can also create a label named _Reengage_ to denote campaigns used to bring back users who have dropped off. Similarly, you can create a label called _Score Updates_ to identify only that class of notifications that were used to update users on the match.

You can create and apply labels from the _All Campaigns_ or the _All Journeys_ page. 

> 📘 Naming Labels
> 
> The labels cannot start with or contain the following symbols: ”, \, %, >, \<, and !.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d3592a1-Creating_Multiple_Campaign_Labels.gif",
        null,
        "Create Multiple Message Labels"
      ],
      "align": "center",
      "border": true,
      "caption": "Create and Assign Multiple Message Labels"
    }
  ]
}
[/block]


You can view and export all labels to a CSV file from the _Settings_ >  _Setup_  > _Labels_  page. You can also edit or delete labels from this page.

You can create a maximum of 900 labels on the CleverTap dashboard. Labels can be applied to individual campaigns from the All Campaigns page during creation.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e96d91674fd5178c48dcf69813fcd9110249717e1d5ffe42e5ed79ab4c8a7dcc-image.png",
        null,
        "View Labels"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "View Labels"
    }
  ]
}
[/block]


## Segments and Message Labels

One of the more powerful uses of Labels is their combination with CleverTap Segmentation features. Each time a message is delivered to a user, CleverTap records a _Notification Sent_ event. As a property of this event, we include any label that you have assigned to that messaging campaign. 

Then from our Find People, Create Segment, or any other Analytics feature, you can isolate users who have been sent a messaging campaign with a particular Label.

For example, you may want to check the 30-day retention of users who were sent Onboarding messages to judge whether these messages were having an impact. After creating a label called _Onboarding_ and associating it with all the relevant campaigns, you can create a new segment and then filter your cohort analysis for 30-day retention to isolate the performance of only these users.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b961bc7-Filter_by_Users.png",
        "Campaign optimization using Segments and Message Labels.",
        1404
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Segments and Message Labels"
    }
  ]
}
[/block]