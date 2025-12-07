---
title: Calendly
excerpt: Workflow Automation
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

[Calendly](https://calendly.com/) is a powerful scheduling platform that simplifies meeting coordination by allowing users to share booking links and automate calendar events. Integrating Calendly with CleverTap automates notifications, logs meeting data, and personalizes follow-ups whenever a meeting is booked.Integrating Calendly with CleverTap via Zapier allows you to: 

* **Capture Meeting Events Automatically**: Sync new meeting bookings from Calendly to CleverTap in real time.
* **Send Instant Notifications**: Trigger automated emails to hosts or teams when a new meeting is scheduled.
* **Track Engagement and Activity**: Log events such as “Meeting Scheduled” for campaign segmentation and analytics.
* **Personalize Follow-ups**: Use meeting details (invitee name, email, meeting time) in CleverTap campaigns.

# Prerequisites for Integration

The following are the prerequisites for this integration:

* Access to your **Calendly** account
* Access to an active **Zapier** account
* A CleverTap account with a valid **Account ID** and **Passcode**

# Integrate Calendly with CleverTap Using Zapier

Suppose you use Calendly to schedule meetings with prospects and want those bookings to appear instantly in CleverTap for notifications or follow-ups.

This integration connects Calendly, Zapier, and CleverTap, so every new meeting is automatically logged in CleverTap as an event, enabling real-time alerts, campaign triggers, and personalized engagement.

The integration involves the following four major steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:calendly#create-a-passcode-on-the-clevertap-dashboard)
2. [Generate a Meeting Link in Calendly](doc:calendly#generate-a-meeting-link-in-calendly)
3. [Connect Calendly and CleverTap via Zapier](doc:calendly#connect-calendly-and-clevertap-via-zapier)
4. [Create a CleverTap Campaign to Notify Hosts](doc:calendly#create-a-clevertap-campaign-to-notify-hosts)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Generate a Meeting Link in Calendly

Set up a meeting link in Calendly that your customers or leads can use to book time with you. This link forms the foundation for capturing meeting data later in the integration process.

1. Log in to your Calendly dashboard.
2. Create or select an existing event type (for example, *30-Minute Meeting*).
3. Click **Share** or **Copy link** to copy your Calendly booking URL. You can share this link with users via email or embed it on your website to facilitate scheduling.

<Image alt="Generate a Meeting Link in Calendly" align="center" width="75% " border={true} src="https://files.readme.io/4fc94b12a4151fa2e0a7884f8c62b5f790b28372633e503e98b301509ab23b9b-image.png">
  Generate a Meeting Link in Calendly
</Image>

## Connect Calendly and CleverTap via Zapier

Zapier acts as an automation bridge between Calendly and CleverTap. Whenever a meeting invitee books a slot using your Calendly link, Zapier captures the booking details and sends them to CleverTap.\
This ensures every meeting is logged as a custom event that can trigger notifications, analytics, and personalized engagement.

### Create a Zap in Zapier

Create a Zap that listens for new meetings in Calendly. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**. Zapier can connect different applications such as Calendly.

<Image alt="Create a Zap on Zapier Dashboard" align="center" border={true} src="https://files.readme.io/96761991c8fb492b440f9263688a51532df31698f124bdc68351d49fc354e88d-image.png">
  Create a Zap on Zapier Dashboard
</Image>

2. **Set up a Trigger**: To do so, perform the following steps:
   1. Select *Calendly* from the App section.
   2. Select *Invitee Created* as the Trigger Event.
   3. Connect your Calendly account.

<Image alt="Set up a Trigger" align="center" width="75% " border={true} src="https://files.readme.io/61ac2696c70462bf8c7093faf2f550b4c061f04d6df838b6ab9dd7be18492586-2025-10-14_12-57-19_1.gif">
  Set up a Trigger
</Image>

3. Configure the event type and scope that should trigger this workflow.

<Image align="center" className="border" width="75% " border={true} src="https://files.readme.io/0840fc9dff4c1c0b28852d66eef90a71c611ca97ff89e34d7691d87ebe6fce52-image.png" />

4. Test the trigger to fetch a sample event (for example, the most recent scheduled meeting). And click **Continue with selected record**.

<Image alt="Set up the Calendly Trigger" align="center" width="65% " border={true} src="https://files.readme.io/6db877018a971fd5f9155ac06c59442f9e20d5fedf5510dd3f50039b398c04af-image.png">
  Set up the Calendly Trigger
</Image>

5. Select the *Action* that zap must perform after the trigger event occurs. To do so, perform the following steps:
   1. Select *CleverTap* from the App event dropdown.
   2. Select *Upload Event* from the Action event dropdown.
   3. Select the Account to connect the CleverTap account. The Zapier window opens.
   4. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained in the [Create a Passcode on CleverTap Dashboard](doc:calendly#create-a-passcode-on-the-clevertap-dashboard) step.
   5. Click **Continue** after your account is successfully connected.

<Image alt="Set up the CleverTap Action" align="center" width="75% " border={true} src="https://files.readme.io/84bca8a28bac93517e0719b70d6c9374ed0cb57a5a6e5b0d940b5b4e6de4538a-2025-11-03_14-54-07_1.gif">
  Set up the CleverTap Action
</Image>

6. **Configure the Action**. Map Calendly data fields to CleverTap fields as follows:

| CleverTap Field  | Calendly Field                                                                                                                                        |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| User ID          | Calendly host’s email or a unique user identifier.                                                                                                    |
| Object ID        | Leave blank if User ID is provided.                                                                                                                   |
| Creation Date    | Date of the user’s creation in Calendly.                                                                                                              |
| Event Name       | Custom event name (for example: `Meeting Scheduled`)                                                                                                  |
| Event Properties | Metadata in JSON format (for example: `{"invitee_name": "John Doe", "invitee_email": "john@example.com", "meeting_url": "https://calendly.com/..."}`) |

> 🚧 Mapping Identity and Object ID
>
> You can provide either **User ID** or **Object ID**, but not both.

<Image alt="Configure the Action" align="center" width="65% " border={true} src="https://files.readme.io/1ae05584a3a3fba4a8b35517d831209a8f53613ee148bd7a8e7e843c441c1469-bae3ce48-8ed9-46dc-8ca1-bdc5146761ee.png">
  Configure the Action
</Image>

7. Click **Continue** and click **Test Step** to test the zap after mapping the files.
8. Click **Publish**.
9. Check your CleverTap dashboard to verify that the event has been logged.

<Image alt="Verify Event in CleverTap" align="center" width="95% " border={true} src="https://files.readme.io/e593248bc79b26e5e42cd8f4c2f49c5b9b6ba4fa12fecd3227cc521dae62609d-image.png">
  Verify Event in CleverTap
</Image>

## Create a CleverTap Campaign to Notify Hosts

Once the integration is active, you can create a CleverTap campaign to automatically notify the host (sales rep or team member) whenever a meeting is scheduled. To do so, perform the following steps:

1. Go to the *Campaigns* page, click **+ Campaign**, and select *Email* from the list of messaging channels.
2. In the *Qualification Criteria*, set the trigger to *Live Behavior*.

<Image align="center" className="border" width="75% " border={true} src="https://files.readme.io/2fa0b2d9943b7353b9a1a49e26635ed804bd5a3e7efc33240d7ca21962bae9c6-image.png" />

3. Add Qualifying events (for example: *30 Minute Meeting scheduled*) as the qualifying condition.

<Image alt="Qualifying Condition" align="center" width="75% " border={true} src="https://files.readme.io/719b4c6bc86a907f77d6c07c04e730e59f3be1125a65fc746448a6b8564dd7c6-image.png">
  Qualifying Condition
</Image>

4. Go to the *What* section while configuring the campaign, then use [Liquid tags](doc:liquid-tags) to get the data corresponding to the event in *Body* to show it to the user, as shown in example below.

#### Example email content:

```html
Hey {{ Profile.name | default:"There!" }},

A new meeting has been scheduled by {{ Event["invitee_name"] | default:"NULL" }} at {{ Event["meeting_date"] | default:"TBD" }}.
Here’s the link to join: {{ Event["meeting_url"] | default:"N/A" }}.
```

<Image alt="Example Email Content" align="center" border={true} src="https://files.readme.io/2026902f8014aba9405e6b7592aa168d36920d805dda4ef3f9f161c8573a8197-image.png">
  Example Email Content
</Image>

5. Click **Preview and Test** to ensure event data is correctly rendered in the email.
6. Click **Publish** to make the campaign live.

Once a customer books a meeting, the host automatically receives an email with the meeting details.

<Image alt="Email Personalization with Liquid Tags" align="center" border={true} src="https://files.readme.io/209230b3f027d816ee4212d647876c0fafe955fcd35a8baed5f328ded991d17e-image.png">
  Email Personalization with Liquid Tags
</Image>

# FAQs

### Can I trigger multiple campaigns based on different meeting types?

Yes. You can configure separate Zaps in Zapier for each meeting type (for example, 15-minute, 30-minute, 60-minute meetings) and map them to unique CleverTap events. Then, use these events as triggers in specific campaigns or journeys.

### Can I send notifications to multiple team members?

Yes. You can add additional email addresses or user groups within your CleverTap campaign configuration to notify multiple recipients when a new meeting is booked.

### Why aren’t my meetings appearing in CleverTap?

Ensure your Zap is published and the correct CleverTap account credentials (Account ID and Passcode) are used. Test the trigger and action steps in Zapier to confirm successful data mapping.
