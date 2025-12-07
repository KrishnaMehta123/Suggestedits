---
title: Reminders
excerpt: Learn how you can send automated reminders before or after a specific date.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Introduction

Reminders allow users to send personalized messages or notifications so they can take specific actions before or after a certain date. The primary aim of Reminders is to enhance user engagement and productivity by proactively prompting them to complete tasks, meet deadlines, or adhere to schedules. By leveraging personalized notifications and flexible scheduling options, Reminders empower users to stay on top of their tasks and commitments, ultimately leading to improved time management.

# Key Features

The following are the key features of Reminder Campaigns:

* Personalization: Reminders can be personalized to suit individual preferences and requirements, ensuring relevance and effectiveness.
* Flexibility: Users can set Reminders for various tasks, events, or deadlines, accommodating diverse scheduling needs.
* Scheduling: Users can schedule Reminders to trigger at specific times or dates or at a fixed time of their choice in a day or at the best time for the user, allowing for precise timing of notifications.
* Recurrence: Users can schedule recurring reminders, automating the process of reminding users about tasks or events. The message content can vary for each date, or messages can also be grouped together for a specified date range.
* Disqualification Upon Cancellation: Cancellation automatically removes users from future notifications. For example, should you cancel a flight booking for any reason, you will be disqualified from receiving any further reminders associated with that booking.

# Use Cases

The following are some of the use cases for the Reminders feature:

### FinTech

You can send a reminder before or after the due date for different utility bill payments, such as electricity, credit card, postpaid bills, broadband, gas, and so on. The reminder can include personalization parameters, such as Bill amount, Bill ID, Bill date, and so on. 

In the case of pre-due date reminders, you can prompt your customers to make the payment before the due date to avoid penalties. For post-due date reminder notifications, inform your customers about the penalty incurred due to late payment and encourage them to settle the outstanding amount promptly.

### Subscription

In this case, the Reminders feature helps manage subscription renewals efficiently. You can send a reminder before the customer's subscription to OTT or FoodTech services expires.  In the case of pre-expiry reminders, you can prompt your customers to renew their subscriptions to avoid service interruption. For post-expiry reminders, you can send reminders with offers to incentivize renewal. You can send your customers special offers or discounts to encourage them to renew their subscriptions.

### EdTech

In this case, the Reminders feature ensures timely completion of an online course for which students have enrolled. The student receives a reminder before the end date of the course. This encourages the student to review their progress and complete any remaining coursework to meet the deadline.

### Transactional

In this case, the Reminders feature helps customers stay informed and organized regarding upcoming bookings. For pre-event reminders, you can send a reminder before the scheduled booking date for a movie, event, or flight to remind your customers about upcoming events. The reminder provides essential details such as the date, time, and location of the booking, ensuring the customer is prepared for the event. Additionally, for post-event reminders, you can send notifications soliciting feedback on their flight experience or requesting movie reviews.

# Set Up a Reminder

Before creating a reminder campaign, you must set up a Reminder:

1. Go to *Reminders* page from the CleverTap dashboard and click **Create Reminder**. 

<Image alt="Navigating to Reminders Page" align="center" border={true} src="https://files.readme.io/6be41bb-Create_a_Reminder.gif">
  Navigating to Reminders Page
</Image>

The *Setup* page opens.

2. Enter the following details:

<Image alt="Set Up a Reminder" align="center" border={true} src="https://files.readme.io/1dc4b6a-Set_Up_a_Reminder.gif">
  Set Up a Reminder
</Image>

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Reminder Name
      </td>

      <td>
        Enter the name to uniquely identify your reminder.
      </td>
    </tr>

    <tr>
      <td>
        Duration
      </td>

      <td>
        Indicates the amount of time the reminder data is stored for each user and how long campaigns can be sent.
      </td>
    </tr>

    <tr>
      <td>
        Set Reminder
      </td>

      <td>
        Define the event to qualify users for the reminder campaigns. For example, you want to set up a reminder to pay the electricity bill. In this case, `Bill Reminder` can be the event that can qualify users for the Reminders campaign. <li> Reminder ID: Select the property that uniquely identifies the reminder. For this example, the Reminder ID  can be *biller\_name*, indicating that we are setting up a reminder for an electricity bill</li> <li> Due Date: Refers to the deadline or scheduled time by which a particular action or task needs to be completed or addressed. This due date serves as a reference point for triggering reminders to users, ensuring that they are prompted to take necessary actions before the specified deadline. For example, the due date for paying the electricity bill. </li> <li> Event Properties for Personalization: Refers to the customizable attributes or details associated with specific events or actions that can be used to personalize reminder messages sent to users. These event properties allow for tailoring reminders to individual users based on their specific interactions, preferences, or characteristics. You can add up to 10 properties for personalization. For example, biller\_name, amount, custid, and so on.</li>
      </td>
    </tr>

    <tr>
      <td>
        Clear Reminder/Cancel Reminder
      </td>

      <td>
        Refers to the action taken by a user or an administrator to deactivate or stop a scheduled reminder from being sent to a particular recipient.\
        Select the event that will be raised when the user stops the scheduled reminder.\
        Reminder ID: Select the property that uniquely identifies the reminder. For this example, the Reminder ID  can be *biller\_name*, indicating that we are setting up a reminder for an electricity bill.
      </td>
    </tr>

    <tr>
      <td>
        Snooze Reminder
      </td>

      <td>
        If a user receives a reminder about a task they need to complete but are currently occupied, they can choose to snooze the reminder for a certain duration (for example, 1 day). During this snooze period, the reminder will not be sent. <li> Select the event that will be raised when the user stops the scheduled reminder. </li> <li> Reminder ID: Select the property that uniquely identifies the reminder. For this example, the Reminder ID  can be *biller\_name*, indicating that we are setting up a reminder for an electricity bill. </li> <li> Reminder Until: Select the date until which you want to snooze the reminder.</li>
      </td>
    </tr>
  </tbody>
</Table>

# Create a Campaign Using Reminders

After setting up the reminder, you can create a campaign using reminders:

1. From the Setup page, click **Create Campaign**. The *Select the channels for your Reminder campaigns* popup opens.

<Image alt="Select Channels for Reminder Campaign" align="center" border={true} src="https://files.readme.io/b8f9cf0-image.png">
  Select Channels for Reminder Campaign
</Image>

2. Select the channel for your Reminder campaign. For our example, we will select Push Notification. The *New Push Notification Reminder* popup opens from the right side.

<Image alt="New Push Notification Reminder" align="center" width="90% " border={true} src="https://files.readme.io/c44c59a-New_Push_Notification_Reminder.png">
  New Push Notification Reminder
</Image>

2. Define the *Start here* section for the campaign.
3. Define the *Who* section. Here, you must define the duration for which engagements need to be sent. You can also filter your target audience further.

<Image alt="Define Target Segment for Reminder Segment" align="center" width="75% " border={true} src="https://files.readme.io/2955c85-image.png">
  Define Target Segment for Reminder Campaign
</Image>

4. Define the content for your Reminder campaigns.
5. Define the *Date and time* to send the reminder campaign and also define the *Delivery preferences*.

## Define Message for Reminder Campaigns

Consider the same example where you want to remind your customers about their upcoming electricity bill due date. When defining the target audience, we chose to send reminders two days before the due date, one reminder on the due date, and one reminder one day after the due date. Here, you can create different message variants for each day, that is, a different reminder message copy for -2 day, -1 day, due date, and +1 day. This customization allows for targeted messaging that aligns with the evolving context or objectives of each day.

<Image alt="Create Reminder Message for Each Day " align="center" width="65% " border={true} src="https://files.readme.io/679b331-Create_Reminder_Notification_for_Each_Day.png">
  Create Reminder Message for Each Day 
</Image>

You also have the option to define the common message for multiple days. In our example, you may want to send the same reminder copy before the due date (-2 days to -1 day, a different copy for the reminder to be sent on the due date, and a different reminder message copy to be sent one day after the due date (+1 day).

<Image alt="Define Common Reminder Copy For Date Range" align="center" width="75% " border={true} src="https://files.readme.io/1cfe543-Create_Common_Reminder_Copy_for_Date_Range.gif">
  Define Common Reminder Copy For Date Range
</Image>

You also have the option to copy a particular message copy and reuse it with minor or no changes, as shown in the following image:

<Image alt="Copy Message from a Particular Variant" align="center" border={true} src="https://files.readme.io/48a4863-Copy_Message_from_a_Particular_Variant.png">
  Copy Message from a Particular Variant
</Image>

## Define Schedule and Delivery Preferences

You can set up the *When* section to schedule the reminder campaign based on the following available options:

### Data and Time

You can deliver the Reminder campaigns at:

* Per the due date time: Selecting this option allows you to deliver the reminder campaign on and around the due date. (@Abhinav: I need your help to elaborate better here.)
* Best time for every user: Selecting this option allows you to send the reminder campaign to every user based on their most active time throughout the day. For more information, refer to [Best Time Campaigns](doc:best-time) .
* A fixed time: Selecting this option allows you to send the reminder campaign to the users at a fixed time during the day.

<Image alt="Select Delivery Option for Reminder Campaigns " align="center" width="75% " border={true} src="https://files.readme.io/88a07fb-Date_and_Time_for_Reminder_Campaigns.png">
  Select Delivery Option for Reminder Campaigns 
</Image>

### Delivery Preferences

You can apply global campaign limits to determine how many notifications each app user receives per day. If you want to override these settings for an important campaign, you can click on the Don’t apply global campaign limits to this campaign checkbox.

You can also click the Advanced checkbox to specify Do Not Disturb (DND) hours during which notifications from this campaign are prevented from going out, either by discarding them or delaying delivery after DND hours, such as 9 PM to 9 AM.

Since past behavior campaigns can have scheduled times, you have the option to stop a campaign delivery after a certain cut-off time or even deliver at the specified time in the user’s timezone. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

<Image alt="Set Up Delivery Preferences for Reminder Campaign" align="center" width="65% " border={true} src="https://files.readme.io/d5c96d8-image.png">
  Set Up Delivery Preferences for Reminder Campaign
</Image>

> 📘 Recurring Day
>
> If you specify a recurring day for a campaign such as the 7th of each month, then the campaign will start for the specified day and ignore the creation date. This is a precaution to avoid sending a campaign unintentionally on a prior date.

#### Time To Live

Time to Live is the persistence of a notification sent to an end user. Push services such as FCM, APNS, XPS, Baidu, and HMS manage Time to Live. They regulate the time the system monitors user device status to deliver a push notification. Whenever the user is online during the set TTL period, the notification is delivered. Any user not coming online will not receive the push notification, and no notifications are attempted after the TTL period is over.

#### Do Not Disturb (DND)

Select this option to avoid sending messages during certain times of the day. By default, DND limits are based on the user's timezone. 

#### Cut-off

The campaign cut-off time ensures no notifications are sent after the specified time. Clevertap does not send notifications to the push services after the cut-off. This is useful if the campaign is time-sensitive and a later time makes the notification irrelevant.\
Select *Cut-off*  and specify the time to stop sending the notification when the number of target users is large. This will cause a significant delay in processing the user queue, ensuring that no notification is sent after the set time.
