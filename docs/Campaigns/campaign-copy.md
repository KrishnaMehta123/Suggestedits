---
title: Campaign Optimization
excerpt: Understand how to engage with users through Campaigns.
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

Marketing campaigns promote products through different types of media. They are designed with different goals in mind, including building a brand image, introducing a new product, and increasing sales of an existing product.\
Defining a campaign's goal usually dictates how much marketing is needed and what media are most effective for reaching a specific segment.

# Messaging Channels

CleverTap offers different messaging channels that enable creating engagement strategies to reach your users with a personalized message at the right time. 

### [Push](doc:push)

Push notifications enable you to communicate with your users when they are not in your app. Depending on the platform and user configuration, these messages appear on a user's lock screen or in a top/bottom banner. 

### [In-App Messages](doc:in-app)

In-app messages are pop-up messages that are shown to the user while they are in your app. While the user views push notifications outside the app, in-app notifications are viewed inside the app.\
In-app notifications are great for showing contextual messages, such as discount offers while the user is within the app or communicating with users who have turned off push notifications.

### [App Inbox](doc:app-inbox)

App Inbox is a messaging channel that provides the ability to deliver rich, individually customized content to your users. Messages sent to the App Inbox get saved on the user's device. 

### [Email](doc:email)

In CleverTap, you create the email content, specify the target audience, and determine when the campaign activates. CleverTap delivers the email messages to the third-party [email service provider](doc:email-partners) of your choosing via a simple configuration in the Dashboard.

### Web Channels

**[Web Push](doc:web-push)**\
Web Push notifications are browser-based messages you can send to your desktop or mobile web users even if they are not currently visiting your website. 

**[Web Pop-up](doc:web-pop-ups)**\
Web pop-ups are interstitial messages displayed to the user while they are on the desktop or mobile website.

**[Web Exit Intent](doc:web-exit-intent-overview)**\
Exit Intent messages are similar to Web Pop-ups, except they are triggered when a user navigates away from your website.

### [Native Display](doc:native-display)

Native Display provides the ability to embed content natively within your app screen without interrupting the app experience. It also provides the ability to change your app's content dynamically and deliver relevant and contextual content to your users.

### [Webhooks](doc:webhooks-overview)

CleverTap webhooks enable developers to monitor specific user events and receive push notifications to their servers when those events happen. Each qualified user's details are sent to the endpoint, which exports data to a third-party system.

### [SMS](doc:sms)

SMS notifications enable you to send short communication to your users, such as one-time passwords to authorize their use of the app or even links allowing the users to download the latest version of the mobile app.

### Remarketing Channels

**[Facebook Audiences](doc:facebook-audiences)**\
Facebook Custom Audience is a great way to re-engage your users outside of your app through ads on Facebook. The Facebook Audience module on the CleverTap Dashboard makes it easy to set up Facebook Audience ads for all your users or specific user segments. You can create segments based on past user behavior, user properties, or a combination of past user behavior and properties. 

**[Google Adwords](doc:google-adwords)**\
Remarketing with Google Ads is a great way to re-engage with users outside your app or website via the Google Ads network.

(@Suvudhi: Asking the respective writer to add Tik Tok Remarketing here.)

# Campaigns

You can create new campaigns and view existing ones under **Campaigns**, which is available in the left pane. Once a campaign is published, you can stop it but cannot pause it. 

## Campaigns Operations

You can perform different actions on the campaigns from the *All Campaigns* page. The following sections briefly discuss each operation.

### Filter Campaigns

You can quickly search your campaigns by applying the required filters. To do so: 

1. Navigate to *Messages* > *Campaigns* from the CleverTap dashboard. The *All Campaigns* page opens.
2. Click the ![](https://files.readme.io/ac0ed6a-Filter_icon.png) icon. The Filter Campaigns window opens on the right side of the screen.

<Image alt="Filter Campaigns" align="center" border={true} src="https://files.readme.io/fbf5087fbe1294fd42ffd5cb82fd3af9a700ac6acf9d276225ad5365e6fc93ce-Filter_Campaigns.png">
  Filter Campaigns
</Image>

3. Select from the following filters and click **Apply**:
   * **Channel**: Filters based on the type of the type of messaging channel used. The following are the available options: Email, SMS, Push Notifications, Mobile In-app, Web, Audiences, Web Push, Webhooks, Google Ads,  App Inbox, WhatsApp, Partner, Native Display, and Web Native Display.
   * **Type**: Filters based on the type of campaign. The campaign can be a Single Message, A/B Test, or Message on user property type of campaign.
   * **Status**: Filters campaign based on the current status of the campaign. The following are the possible statuses: Scheduled, Running, Stopped, Completed, Draft, Awaiting Next Run, Approval Pending, and Rejected. For more information, refer to [Campaign Status](doc:intro-to-campaigns#campaigns-status).
   * **Created by:** Filters based on the email ID of the person who created the campaign.
   * **Label**: Filters based on the labels assigned to the campaigns.
   * **Delivery**: Filters based on the delivery type of the campaign. The following are the available options: One Time, Inaction, Action, On a date/time, Recurring, API, and Multiple Date.

<Image alt="Apply Campaign Filters" align="center" border={true} src="https://files.readme.io/80bdbc6-Apply_Campaign_Filter.gif">
  Apply Campaign Filters
</Image>

All the campaigns that meet the criteria are listed under the *All Campaigns* page. Also, you can save the filter by clicking the *Save Filter* link.

You can also apply quick filters from the top of the *All Campaigns* page.

### Archive Campaigns

Archiving campaigns helps to keep your CleverTap account organized and clutter-free, making it easy to find and view the campaigns you want. To do so:

1. Go to *Messages* > *Campaigns* from the CleverTap dashboard. The *All Campaigns* page opens.
2. Select the campaigns you may want to archive and click the ![](https://files.readme.io/b46b84b-Archive_icon.png) icon.
3. Click **Save** to archive the selected campaigns or click **Cancel** to undo the action.

<Image alt="Archive Selected Campaigns" align="center" border={true} src="https://files.readme.io/65f3a7d89e189d529f8e9017160947cf6ca85a38901927ebc060e9984b47aa9a-Archive_Campaigns.gif">
  Archive Selected Campaigns
</Image>

> 📘 Note
>
> Toggle the *Archive Campaigns* option to view the archived campaigns.

<br />

### Stop Campaigns

You may want to stop a particular campaign after monitoring and evaluating its efficacy. To do so:

1. Navigate to *Messages* > *Campaigns* from the CleverTap dashboard. The *All Campaigns* page opens.
2. Select the running campaigns you may want to stop and click the ![](https://files.readme.io/c2fcde8-Stop_icon.png) icon.

<Image alt="Stop Selected Campaigns" align="center" border={true} src="https://files.readme.io/e4ba1596611e5ec12b7ce1d2ba899ca33952b7a70206a9e9f9a193427fa73e1b-Stop_Campaigns.png">
  Stop Selected Campaigns
</Image>

3. Click **Save** to archive the selected campaigns or click **Cancel** to undo the action.

### Clone Campaign

Cloning a campaign helps to create a new campaign from an already existing campaign with minor or no modifications. To do so:

1. Navigate to *Messages* > *Campaigns* from the CleverTap dashboard. The *All Campaigns* page opens.
2. Select the running campaigns you may want to clone and click the ![](https://files.readme.io/e6ac3e4-Clone_icon.png) icon.

<Image alt="Clone Selected Campaign" align="center" border={true} src="https://files.readme.io/9d6d2ad-Clone_Campaigns.png">
  Clone Selected Campaign
</Image>

3. Click **Save** to archive the selected campaigns or click **Cancel** to undo the action.

## Campaign Status

After the campaign is published, your ability to make edits is restricted; and this limitation may vary based on the factors outlined below:

* **For Campaigns Scheduled for Later**: You can edit the following sections of the campaign: Who, What, and When.
* **For Campaigns Awaiting Next Run and Live Campaigns**: You can edit only the campaign message, name, and labels.
