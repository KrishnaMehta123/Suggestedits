---
title: Types of Segments
excerpt: Understand the types of Segments available in CleverTap
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

CleverTap's Segmentation feature helps personalize user experiences and optimize your marketing strategies. In this document, you will learn about the types of segments available in CleverTap.

# System User Segments

Before creating any segment on the CleverTap dashboard, default system segments are already present. To view these system segments:

1. Navigate to _Segments_ > _Segments_ from the CleverTap dashboard.
2. Click the ![](https://files.readme.io/1d37ff4-Filter_Icon.png) icon.
3. From the _Created By_ dropdown, select _System_.

   <Image align="center" alt="Filter System User Segments" border={true} caption="Filter System User Segments" src="https://files.readme.io/7614538-System_Segments.png" />
4. Click _Apply_, and all the system user segments display.

<Image align="center" alt="View All System User Segments" border={true} caption="View All System User Segments" src="https://files.readme.io/46f2bf6-View_System_Segments.png" />

The following are the system-defined user segments that are available for your use:

* **First time App Users - Live View**: This system segment includes users who have recently installed and launched the app for the first time. First-time app users are crucial for businesses to understand, as they represent potential new customers or users. Analyzing this segment can help organizations tailor onboarding experiences, send targeted welcome messages, and implement strategies to encourage further engagement.
* **Engaged Users - at least 4 times in the past week**: This segment comprises users who have demonstrated high engagement with the app. To qualify for this segment, users must have interacted with the app at least four times within the past week. Analyzing the behavior of these users provides insights into the features that are popular and help businesses design targeted campaigns or promotions to retain and further engage this user segment.
* **All Users**: This user segment contains all the users added to your project.
* **Test Users**: The Test User segment is a default user segment in CleverTap that businesses can use to test their Campaigns, Journeys, and Product Experiences before sending them to actual users. This segment allows businesses to experiment with new features, messaging, and campaigns in a safe and controlled environment. Using Test Users helps businesses measure the effectiveness of their ideas before rolling them out to a larger audience. Test Users can be manually created from the CleverTap dashboard or imported through a CSV file and segmented based on various criteria. For more information, refer to [Mark a User Profile as a Test Profile](https://developer.clevertap.com/docs/concepts-user-profiles#mark-a-user-profile-as-a-test-profile).

# Types of Segments

The following are the three types of segments that can be created from the CleverTap dashboard:

* [Past Behavior Segments](doc:types-of-segments#past-behavior-segments)
* [Live User Segments](doc:types-of-segments#live-user-segments)
* [Custom List Segments](doc:types-of-segments#custom-list-segments)

<Image align="center" alt="Types of Segments" border={true} caption="Types of Segments" src="https://files.readme.io/9adfb41-All_Segments.png" />

## Past Behavior Segments

Past behavior segments allow you to group users based on actions or inactions they have performed in the past, combined with their user properties. Segments evaluate behavioral events relative to the date selected in the Today filter, while user properties evaluate on the actual calendar date unless otherwise specified.  

For example, you can create a segment of users from California who are female, have launched the application within the last 30 days, and have not made any purchases from the app.    

### Additional Use Cases

**Use case:** Find users who launched the app two days ago but did not launch today

This segment identifies users who performed an app launch exactly two days before the date selected in the Today filter and excludes users who launched the app on the selected date.

**Outcome:**
The system evaluates the segment relative to T-1 of the Today filter. When viewed on 3 December, the segment returns users who launched the app on 2 December and did not launch on 3 December.

**Use case:** Find users whose birthday is today

This segment identifies users whose birthday matches the current date on the calendar.

**Outcome:**
The system evaluates user properties based on the actual date of the event. As of 3 December 2025, the segment returns users whose birthday falls on the same date.

Segmentation behavior for Past Behavior Segments varies based on the data type. Event-based conditions are evaluated relative to the Today filter, while user properties are assessed on the actual date.

## Live User Segments

While past behavior segments let you evaluate users based on historical criteria, live user segments allow you to track what is happening in your app right now. When you define a set of behaviors of interest, CleverTap monitors them as they occur in your app and immediately adds a user to a segment when their behavior matches your action criteria. You can create the following types of live user segments:

* **Live - User Actions**: Add users to a segment as soon as they perform an event. For example, users who booked a movie ticket from your app.
* **Live - Inaction in Time Frame**: Add users to a segment when they perform an event but not another within a specific time. For example, users who have added a product to the cart but did not purchase it within 10 minutes of adding it.
* **Live - On a Date or Time**: Add users to a segment based on date and time property value. For example, users who have an appointment five days from today.
* **Live - Page Visit**: Add users to a segment as soon as they visit a specific URL on your website. For example, users who have viewed the landing page of a festival sale.
* **Live - Referrer Entry**: Add users to a segment based on a referring website or campaign. For example, users who have visited your website via a specific external referrer URL.
* **Live - Page count**: Add users to a segment based on the number of pages visited by them. For example, users who have visited five web pages on your website.

## Custom - List Based Segments

A custom - list based segment is a list of users from any source, including third-party tools or internal databases. You can deliver personalized messages to these users based on their past or real-time behavior in the app. For more information, refer to [Custom List Segment](doc:create-segments#create-custom---list-based-segments).
