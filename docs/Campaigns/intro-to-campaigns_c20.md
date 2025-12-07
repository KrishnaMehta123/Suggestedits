---
title: Campaign Optimization
excerpt: >-
  Understand how to use different messaging channels to build campaigns in
  CleverTap.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
  pages:
    - type: link
      title: A/B Multivariate testing
      url: https://docs.clevertap.com/docs/ab-multivariate-testing_c20
    - type: link
      title: Notification Delivery Options
      url: https://docs.clevertap.com/docs/notification-delivery-options_c20
    - type: link
      title: Recommended Delay for Inaction Campaigns
      url: https://docs.clevertap.com/docs/recommended-delay_c20
    - type: link
      title: Regex
      url: https://docs.clevertap.com/docs/regex_c20
    - type: link
      title: Best Time
      url: https://docs.clevertap.com/docs/best-time_c20
    - type: link
      title: Constant Event Property
      url: https://docs.clevertap.com/docs/constant-property_c20
    - type: link
      title: Geofencing
      url: https://docs.clevertap.com/docs/geofencing_c20
    - type: link
      title: API
      url: https://docs.clevertap.com/docs/api-campaigns_c20
    - type: link
      title: Campaign Reports
      url: https://docs.clevertap.com/docs/campaign-reports_c20
---
# Overview

Marketing campaigns promote products through different types of media. Campaigns are designed with different goals in mind, including building a brand image, introducing a new product, increasing sales of an existing product.\
Defining a campaign's goal usually dictates how much marketing is needed and what media are most effective for reaching a specific segment.

# Messaging Channels

CleverTap offers seven different messaging channels that enable creating engagement strategies to reach your users with a personalized message at the right time. 

## Mobile Channels

The mobile channels include:

### [Push](doc:push)

Push notifications enable you to communicate with your users when they are not in your app. Depending on the platform and user configuration, these messages appear on a user's lock screen or in a top/bottom banner. 

### [In-App Messages](doc:in-app)

In-app messages are pop-up messages that are shown to the user while they are in your app. While the user views push notifications outside the app, in-app notifications are viewed inside the app.\
In-app notifications are great for showing contextual messages, such as discount offers while the user is within the app or communicating with users who have turned off push notifications.

### [App Inbox](doc:app-inbox)

App Inbox is a messaging channel that provides the ability to deliver rich, individually customized content to your users. Messages sent to App Inbox get saved on the user's device. 

### [Native Display](doc:native-display)

Native Display provides the ability to embed content natively within your app screen without interrupting the app experience. It also provides the ability to change your app's content dynamically and deliver relevant and contextual content to your users. 

## Web Channels

**[Web Push](doc:web-push)**\
Web Push notifications are browser-based messages you can send to your desktop or mobile web users even if they are not currently visiting your website. 

**[Web Pop-up](doc:web-pop-ups)**\
Web pop-ups are interstitial messages displayed to the user while they are on the desktop or mobile website.

**[Web Exit Intent](doc:web-exit-intent-overview)**\
Exit Intent messages are similar to Web Pop-ups, except they are triggered when a user navigates away from your website.

## Additional Channels

**[Email](doc:email)**

In CleverTap, you create the email content, specify the target audience, and determine when the campaign activates. CleverTap delivers the email messages to the third-party [email service provider](doc:email-partners) of your choosing via a simple configuration in the Dashboard.

**[Webhooks](doc:webhooks-overview)**\
CleverTap webhooks enable developers to monitor specific user events and receive push notifications to their server when those events happen. Each qualified user's details are sent to the endpoint, which exports data to a third-party system.

### [SMS](doc:sms)

SMS notifications enable you to send short communication to your users, such as one-time passwords to authorize their use on the app or even links allowing the users to download the latest version of the mobile app.

## Remarketing

**[Facebook Audiences](doc:facebook-audiences)**\
Facebook Custom Audience is a great way to re-engage your users outside of your app through ads on Facebook. The Facebook Audience module on the CleverTap Dashboard makes it easy to set up Facebook Audience ads for all your users or specific user segments. Base these segments on past user behavior, user properties, or a combination of past user behavior and properties. 

**[Google Adwords](doc:google-adwords)**\
Remarketing with Google Ads is a great way to re-engage with users outside your app or website via the Google Ads network.

# Campaigns

You can create new campaigns and see existing ones under **Campaigns** available in the left pane.

## Campaign Reports

Selecting *Campaigns* from the CleverTap Dashboard opens the Campaign Reports table where you can see all your campaigns across every channel in one consolidated view.

Campaign Reports include the channel, delivery status, and key statistics to assess and compare performance. 

Use quick filters to isolate campaigns of interest and the email report option to deliver a CSV file to your inbox that includes all the information in the table.

<Image title="Campaign_reports.gif" alt={1422} className="border" border={true} src="https://files.readme.io/04a4edc-Campaign_reports.gif" />

# Journeys

[Journeys](doc:journeys) is a visual campaign builder to create an omnichannel messaging experience for your users. Journeys are ideal for engaging users across the lifecycle of your app. 

Here are a few sample use cases for Journeys:

* Build User Onboarding Journeys that engage users over several days or weeks and on different channels as you educate them about your service.
* Build Promotional Journeys to entice your users to transact at different points in time.
* Long-running re-engagement campaigns to pull users back into your service if they begin to slip away.

# Message Labels

Message Labels allow you to tag campaigns by descriptive names or themes. Once applied, labels allow you to group your various messaging campaigns such that you can isolate their performance or identify behaviors of users that were displayed this group of messages.

For example, you can create a label called *Onboarding* to identify all the messaging campaigns (across all channels) that are related to onboarding your new users. Or you can create a label named *Reengage* to denote campaigns used to bring back users who have dropped off. Similarly, you can create a label called *Score Updates* to identify only that class of notifications that were used to update users on the match.

Create labels under the *Message Settings* menu. Apply labels to individual messaging campaigns while you create them or via the *Edit Campaign* option in the *Campaign Report* table.

## Segments and Message Labels

One of the more powerful uses of Labels is the combination with CleverTap Segmentation features. Each time a message is delivered to a user, CleverTap will record a Notification Sent event. As a Property of this event, we include any label that you have assigned to that messaging campaign. 

Then from our Find People, Create Segment, or any other Analytics feature, you can isolate users who have been sent a messaging campaign with a particular Label.

For example, you may want to see the 30-day retention of users who were sent Onboarding messages to judge whether these messages were having an impact. After creating a label called *Onboarding* and associating it with all the relevant campaigns, you can create a new segment, and then filter your cohort analysis for 30-day retention to isolate the performance of only these users.

<Image title="Filter_by_Users.png" alt={1404} className="border" border={true} src="https://files.readme.io/b961bc7-Filter_by_Users.png" />
