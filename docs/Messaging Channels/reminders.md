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

- Personalization: Reminders can be personalized to suit individual preferences and requirements, ensuring relevance and effectiveness.
- Flexibility: Users can set Reminders for various tasks, events, or deadlines, accommodating diverse scheduling needs.
- Scheduling: Users can schedule Reminders to trigger at specific times or dates or at a fixed time of their choice in a day or at the best time for the user, allowing for precise timing of notifications.
- Recurrence: Users can schedule recurring reminders, automating the process of reminding users about tasks or events. The message content can vary for each date, or messages can also be grouped together for a specified date range.
- Disqualification Upon Cancellation: Cancellation automatically removes users from future notifications. For example, should you cancel a flight booking for any reason, you will be disqualified from receiving any further reminders associated with that booking.

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

1. Go to _Reminders_ page from the CleverTap dashboard and click **Create Reminder**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6be41bb-Create_a_Reminder.gif",
        "",
        "Navigating to Reminders Page"
      ],
      "align": "center",
      "border": true,
      "caption": "Navigating to Reminders Page"
    }
  ]
}
[/block]


The _Setup_ page opens.

2. Enter the following details:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1dc4b6a-Set_Up_a_Reminder.gif",
        "",
        "Set Up a Reminder"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up a Reminder"
    }
  ]
}
[/block]


[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "0-0": "Reminder Name",
    "0-1": "Enter the name to uniquely identify your reminder.",
    "1-0": "Duration",
    "1-1": "Indicates the amount of time the reminder data is stored for each user and how long campaigns can be sent.",
    "2-0": "Set Reminder",
    "2-1": "Define the event to qualify users for the reminder campaigns. For example, you want to set up a reminder to pay the electricity bill. In this case, `Bill Reminder` can be the event that can qualify users for the Reminders campaign. <li> Reminder ID: Select the property that uniquely identifies the reminder. For this example, the Reminder ID  can be _biller_name_, indicating that we are setting up a reminder for an electricity bill</li> <li> Due Date: Refers to the deadline or scheduled time by which a particular action or task needs to be completed or addressed. This due date serves as a reference point for triggering reminders to users, ensuring that they are prompted to take necessary actions before the specified deadline. For example, the due date for paying the electricity bill. </li> <li> Event Properties for Personalization: Refers to the customizable attributes or details associated with specific events or actions that can be used to personalize reminder messages sent to users. These event properties allow for tailoring reminders to individual users based on their specific interactions, preferences, or characteristics. You can add up to 10 properties for personalization. For example, biller_name, amount, custid, and so on.</li>",
    "3-0": "Clear Reminder/Cancel Reminder",
    "3-1": "Refers to the action taken by a user or an administrator to deactivate or stop a scheduled reminder from being sent to a particular recipient.  \nSelect the event that will be raised when the user stops the scheduled reminder.  \nReminder ID: Select the property that uniquely identifies the reminder. For this example, the Reminder ID  can be _biller_name_, indicating that we are setting up a reminder for an electricity bill.",
    "4-0": "Snooze Reminder",
    "4-1": "If a user receives a reminder about a task they need to complete but are currently occupied, they can choose to snooze the reminder for a certain duration (for example, 1 day). During this snooze period, the reminder will not be sent. <li> Select the event that will be raised when the user stops the scheduled reminder. </li> <li> Reminder ID: Select the property that uniquely identifies the reminder. For this example, the Reminder ID  can be _biller_name_, indicating that we are setting up a reminder for an electricity bill. </li> <li> Reminder Until: Select the date until which you want to snooze the reminder.</li>"
  },
  "cols": 2,
  "rows": 5,
  "align": [
    "left",
    "left"
  ]
}
[/block]


# Create a Campaign Using Reminders

After setting up the reminder, you can create a campaign using reminders:

1. From the Setup page, click **Create Campaign**. The _Select the channels for your Reminder campaigns_ popup opens.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b8f9cf0-image.png",
        null,
        "Select Channels for Reminder Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Select Channels for Reminder Campaign"
    }
  ]
}
[/block]


2. Select the channel for your Reminder campaign. For our example, we will select Push Notification. The _New Push Notification Reminder_ popup opens from the right side.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c44c59a-New_Push_Notification_Reminder.png",
        "",
        "New Push Notification Reminder"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "New Push Notification Reminder"
    }
  ]
}
[/block]


2. Define the _Start here_ section for the campaign.
3. Define the _Who_ section. Here, you must define the duration for which engagements need to be sent. You can also filter your target audience further.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2955c85-image.png",
        null,
        "Define Target Segment for Reminder Segment"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Define Target Segment for Reminder Campaign"
    }
  ]
}
[/block]


4. Define the content for your Reminder campaigns.
5. Define the _Date and time_ to send the reminder campaign and also define the _Delivery preferences_.

## Define Message for Reminder Campaigns

Consider the same example where you want to remind your customers about their upcoming electricity bill due date. When defining the target audience, we chose to send reminders two days before the due date, one reminder on the due date, and one reminder one day after the due date. Here, you can create different message variants for each day, that is, a different reminder message copy for -2 day, -1 day, due date, and +1 day. This customization allows for targeted messaging that aligns with the evolving context or objectives of each day.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/679b331-Create_Reminder_Notification_for_Each_Day.png",
        "",
        "Create Reminder Message for Each Day "
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Create Reminder Message for Each Day "
    }
  ]
}
[/block]


You also have the option to define the common message for multiple days. In our example, you may want to send the same reminder copy before the due date (-2 days to -1 day, a different copy for the reminder to be sent on the due date, and a different reminder message copy to be sent one day after the due date (+1 day).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1cfe543-Create_Common_Reminder_Copy_for_Date_Range.gif",
        "",
        "Define Common Reminder Copy For Date Range"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Define Common Reminder Copy For Date Range"
    }
  ]
}
[/block]


You also have the option to copy a particular message copy and reuse it with minor or no changes, as shown in the following image:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/48a4863-Copy_Message_from_a_Particular_Variant.png",
        "",
        "Copy Message from a Particular Variant"
      ],
      "align": "center",
      "border": true,
      "caption": "Copy Message from a Particular Variant"
    }
  ]
}
[/block]


## Define Schedule and Delivery Preferences

You can set up the _When_ section to schedule the reminder campaign based on the following available options:

### Data and Time

You can deliver the Reminder campaigns at:

- Per the due date time: Selecting this option allows you to deliver the reminder campaign on and around the due date. (@Abhinav: I need your help to elaborate better here.)
- Best time for every user: Selecting this option allows you to send the reminder campaign to every user based on their most active time throughout the day. For more information, refer to [Best Time Campaigns](doc:best-time) .
- A fixed time: Selecting this option allows you to send the reminder campaign to the users at a fixed time during the day.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/88a07fb-Date_and_Time_for_Reminder_Campaigns.png",
        "",
        "Select Delivery Option for Reminder Campaigns "
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Select Delivery Option for Reminder Campaigns "
    }
  ]
}
[/block]


### Delivery Preferences

You can apply global campaign limits to determine how many notifications each app user receives per day. If you want to override these settings for an important campaign, you can click on the Don’t apply global campaign limits to this campaign checkbox.

You can also click the Advanced checkbox to specify Do Not Disturb (DND) hours during which notifications from this campaign are prevented from going out, either by discarding them or delaying delivery after DND hours, such as 9 PM to 9 AM.

Since past behavior campaigns can have scheduled times, you have the option to stop a campaign delivery after a certain cut-off time or even deliver at the specified time in the user’s timezone. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d5c96d8-image.png",
        null,
        "Set Up Delivery Preferences for Reminder Campaign"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Set Up Delivery Preferences for Reminder Campaign"
    }
  ]
}
[/block]


> 📘 Recurring Day
> 
> If you specify a recurring day for a campaign such as the 7th of each month, then the campaign will start for the specified day and ignore the creation date. This is a precaution to avoid sending a campaign unintentionally on a prior date.

#### Time To Live

Time to Live is the persistence of a notification sent to an end user. Push services such as FCM, APNS, XPS, Baidu, and HMS manage Time to Live. They regulate the time the system monitors user device status to deliver a push notification. Whenever the user is online during the set TTL period, the notification is delivered. Any user not coming online will not receive the push notification, and no notifications are attempted after the TTL period is over.

#### Do Not Disturb (DND)

Select this option to avoid sending messages during certain times of the day. By default, DND limits are based on the user's timezone. 

#### Cut-off

The campaign cut-off time ensures no notifications are sent after the specified time. Clevertap does not send notifications to the push services after the cut-off. This is useful if the campaign is time-sensitive and a later time makes the notification irrelevant.  
Select _Cut-off_  and specify the time to stop sending the notification when the number of target users is large. This will cause a significant delay in processing the user queue, ensuring that no notification is sent after the set time.