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

# Campaigns

You can create new campaigns and see existing ones under **Campaigns**, which is available in the left pane. Once a campaign is published, you can stop the campaign but cannot pause it. After the campaign is published, your ability to make edits is restricted; and this limitation may vary based on the factors outlined below:

* **For Campaigns Scheduled for Later**: You can edit the following sections of the campaign: Who, What, and When.
* **For Campaigns Awaiting Next Run and Live Campaigns**: You can edit only the campaign message, name, and labels.
* **For Campaigns with Creator Approver Workflow**

<Table align={["left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Campaign State
      </th>

      <th>
        Scenario
      </th>

      <th>
        Expected Behavior (Creator)
      </th>

      <th>
        Expected Behavior (Approver)
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Scheduled**
      </td>

      <td>
        Before scheduled time
      </td>

      <td>
        The creator of the campaign can edit all the\
        campaign information and send it to the approver for approval
      </td>

      <td>
        The Approver can edit all the campaign information and publish the campaign. (@Suvidhi: When we say publish here - will it be published immediately or at the scheduled time?)
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        After scheduled time
      </td>

      <td>
        A popup, indicating that the changes made by the creator will be discarded, opens.
      </td>

      <td>
        A popup, indicating that the changes made by the approver will be discarded, opens.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        **Awaiting Next Run**
      </td>

      <td>
        Before scheduled time
      </td>

      <td>
        The creator can only modify the WHAT section of the campaign and send it to the approver for approval.
      </td>

      <td>
        The approver can only modify the WHAT section of the campaign and publish the campaign.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        After scheduled time
      </td>

      <td>
        A popup, indicating that the changes made by the creator will be discarded, opens.
      </td>

      <td>
        A popup, indicating that the changes made by the approver will be discarded, opens.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        **Running** 
      </td>

      <td>
        During execution
      </td>

      <td>
        The creator can only edit the WHAT section of the campaign for **Live campaigns** and send it to the approver for approval.
      </td>

      <td>
        The approver can only edit the WHAT section of the campaign for **Live campaigns** and publish the campaign.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        **Pending For Approval**
      </td>

      <td>
        First run is yet to start
      </td>

      <td>
        The creator can edit all the campaign information **before the scheduled time** and send it to the approver for approval.
      </td>

      <td>
        The approver can edit all the campaign information **before the scheduled time** and approve the campaign.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>
        The creator can edit all the campaign information **after the scheduled time** and send it to the approver for approval.
      </td>

      <td>
        A popup indicating that the campaign was scheduled in the past time. The approver can edit all the campaign information and publish the campaign.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        First run was completed and awaiting the next run
      </td>

      <td>
        The creator can edit only the WHAT section **before the scheduled time** and send it to the approver for approval.
      </td>

      <td>
        The approver can edit only the WHAT section **before the scheduled time** and publish the campaign.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>
        If the creator tries to edit the campaign **after the scheduled time**, a popup opens. The popup indicates that the changes made by the creator will be discarded.
      </td>

      <td>
        If the approver tries to edit the campaign **after the scheduled time**, a popup opens. The popup indicates that the changes made by the creator will be discarded.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        **Rejected**
      </td>

      <td>
        First run is yet to start
      </td>

      <td>
        The creator can edit all the campaign information **before the scheduled time** and send it to the approver for approval.
      </td>

      <td>
        The approver can edit only the WHAT section **before the scheduled time** and send it to the approver for approval.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>
        The creator can edit all the campaign information **after the scheduled time** and send it to the approver for approval.
      </td>

      <td>
        If the approver tries to edit the campaign **after the scheduled time**, a popup opens. The popup indicates that the changes made by the approver will be discarded.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>
        First run was completed and awaiting the next run
      </td>

      <td>
        The creator can edit only the WHAT section **before the scheduled time** and send it to the approver for approval.
      </td>

      <td>
        The approver can edit only the WHAT section **before the scheduled time** and publish the campaign.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>
        If the creator tries to edit the campaign **after the scheduled time**, they can edit only the WHAT section and send it to the approver for approval.
      </td>

      <td>
        The approver can only edit the WHAT section of the campaign after the scheduled time. Also, a popup indicates that the campaign can be run today or tomorrow.
      </td>
    </tr>
  </tbody>
</Table>

## Campaign Reports

Selecting *Campaigns* from the CleverTap Dashboard opens the Campaign Reports table where you can see all your campaigns across every channel in one consolidated view.

Campaign Reports include the channel, delivery status, and key statistics to assess and compare performance. 

Use quick filters to isolate campaigns of interest and the email report option to deliver a CSV file to your inbox that includes all the information in the table.

<Image title="Filter Campaigns and view Campaign reports on CleverTap dashboard." alt={1422} align="center" border={true} src="https://files.readme.io/04a4edc-Campaign_reports.gif">
  Filter Campaigns and View Campaign Reports
</Image>

# Journeys

[Journeys](doc:journeys) is a visual campaign builder to create an omnichannel messaging experience for your users. Journeys are ideal for engaging users across the lifecycle of your app. 

Here are a few sample use cases for Journeys:

* Build User Onboarding Journeys that engage users over several days or weeks and on different channels as you educate them about your service.
* Build Promotional Journeys to entice your users to transact at different points in time.
* Long-running re-engagement campaigns to pull users back into your service if they begin to slip away.

# Message Labels

Message Labels allow you to tag campaigns with descriptive names or themes. Once applied, labels allow you to group your various messaging campaigns such that you can isolate their performance or identify behaviors of users that were displayed in this group of messages.

For example, you can create a label called *Onboarding* to identify all the messaging campaigns (across all channels) that are related to onboarding your new users. Or you can create a label named *Reengage* to denote campaigns used to bring back users who have dropped off. Similarly, you can create a label called *Score Updates* to identify only that class of notifications that were used to update users on the match.

You can create labels under the *Message Settings* menu. You can create multiple labels at one time (see figure below). The labels cannot start with or contain the following symbols: ”, \, %, >, \<, and !.

<Image alt="Create Multiple Message Labels" align="center" border={true} src="https://files.readme.io/d3592a1-Creating_Multiple_Campaign_Labels.gif">
  Create Multiple Message Labels
</Image>

You can apply labels to individual messaging campaigns while you create them or via the *Edit Campaign* option on the *All Campaigns* page.

## Segments and Message Labels

One of the more powerful uses of Labels is the combination with CleverTap Segmentation features. Each time a message is delivered to a user, CleverTap will record a Notification Sent event. As a Property of this event, we include any label that you have assigned to that messaging campaign. 

Then from our Find People, Create Segment, or any other Analytics feature, you can isolate users who have been sent a messaging campaign with a particular Label.

For example, you may want to see the 30-day retention of users who were sent Onboarding messages to judge whether these messages were having an impact. After creating a label called *Onboarding* and associating it with all the relevant campaigns, you can create a new segment and then filter your cohort analysis for 30-day retention to isolate the performance of only these users.

<Image title="Campaign optimization using Segments and Message Labels." alt={1404} align="center" border={true} src="https://files.readme.io/b961bc7-Filter_by_Users.png">
  Segments and Message Labels
</Image>
