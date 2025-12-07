---
title: Formless
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

[Formless](https://formless.ai/) is a no-code, AI-powered form builder designed to create conversational and interactive forms that drive higher engagement. Unlike traditional static forms, Formless offers a chat-like experience that feels more natural to users, making it ideal for collecting feedback, generating leads, running surveys, or capturing event responses.

Integrating Formless with CleverTap via Zapier allows you to:

* **Capture User Inputs in Real Time**: Automatically sync user responses collected from Formless into CleverTap.
* **Update Profiles Dynamically**: Create or update user profiles based on form submissions.
* **Trigger Automated Journeys**: Launch CleverTap flows such as thank-you campaigns or escalation journeys immediately after form submissions.

# Prerequisites for Integration

Before integrating Formless with CleverTap via Zapier, ensure the following:

* Access to your **Formless** account
* Access to an active **Zapier** account
* A CleverTap account with a valid **Account ID** and **Passcode**

# Integrate Formless with CleverTap Using Zapier

The integration involves the following four major steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:formless#create-a-passcode-on-the-clevertap-dashboard)
2. [Create a Form in Formless](doc:formless#create-a-form-in-formless)
3. [Configure CleverTap Campaign](doc:formless#configure-clevertap-campaign)
4. [Connect Formless and CleverTap via Zapier](doc:formless#connect-formless-and-clevertap-via-zapier)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create a Form in Formless

Consider an example where you want to capture user details such as Name, Email, and Feedback via a Formless survey inside a CleverTap campaign. To do so, perform the following steps:

1. Log in to your Formless dashboard and create a form that meets your requirements.
2. Once the form is ready, go to the *Share* tab, select **Embed**, and choose **Full Screen**.
3. Copy the embed code snippet to use this form inside CleverTap campaigns.

<Image alt="Create a Form in Formless" align="center" width="75% " border={true} src="https://files.readme.io/5237b6c07f9bb06e315d41a6442e4d95c37c5716df84a2d937e05739bc7ef91d-Screen_Recording_2025-07-22_at_2.01.53_PM_1.gif">
  Create a Form in Formless
</Image>

## Configure CleverTap Campaign

Configure a CleverTap campaign to display your form created in Formless. This allows users to submit responses without leaving the app. To do so, perform the following steps:

1. In the CleverTap dashboard, create a new [In-App Message](doc:create-message-in-app) campaign (you can also use [Web Popups](doc:create-message-web-popup) that support HTML).
2. In the *What* section, select a **Custom HTML Template** such as *Interstitial*.
3. Replace the existing code inside the *Custom HTML* section with the embed snippet copied from *Step 3* of [Create a Form in Formless](doc:formless#create-a-form-in-formless).

<Image alt="Custom HTML Templates" align="center" width="75% " border={true} src="https://files.readme.io/85f9845a741ceb00d26f58a4d93183b2a7b250985569f08d1f87c167cde1c4fc-Screenshot_2025-07-22_at_2.20.13_PM.png">
  Custom HTML Templates
</Image>

4. Add dynamic parameters to capture user details:

```html
<iframe width="100%" height="900px" src="<form_link>?name={{ Profile.name | default: \"NULL\" }}&email={{ Profile.Email | default: \"null@gmail.com\" }}"></iframe>
```

Use [Liquid tags](https://docs.clevertap.com/docs/personalize-message-webhooks#liquid-tags) to personalize your form with CleverTap profile attributes (such as name and email).

<Image alt="Add Dynamic Parameters" align="center" width="75% " border={true} src="https://files.readme.io/6c7574288365c19c75de243b7f65856bffb0ec6bb8c9cbb09bf83de06986052b-image.png">
  Add Dynamic Parameters
</Image>

5. Click **Preview and Test** to verify that the form renders correctly.
6. Publish the campaign only after configuring the Zap as [Create/Update User Profiles](doc:formless#createupdate-user-profiles) or [Upload Event](doc:formless#upload-event).

## Connect Formless and CleverTap via Zapier

Zapier acts as the automation bridge between Formless and CleverTap. Whenever a user submits a survey response, Zapier captures the submission and forwards the data to CleverTap in real time. This allows you to:

* **Enrich or create user profiles** in CleverTap with the submitted attributes, or
* **Track each submission as an event** for segmentation, analytics, and automated engagement campaigns.

The integration supports two options depending on your use case:

* [Create/Update User Profiles](doc:formless#createupdate-user-profiles)
* [Upload Event](doc:formless#upload-event)

### Create/Update User Profiles

Consider an example where you want to automatically sync details captured in Formless surveys with CleverTap to drive personalized engagement. This ensures that each new submission updates the user’s profile in CleverTap in real time. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**. Zapier can connect different applications such as Formless.

<Image alt="Create a Zap on Zapier Dashboard" align="center" border={true} src="https://files.readme.io/81d24bf2bb62b05403da728cf54af63674995a31f21a25485fac5d5a980c24d4-image.png">
  Create a Zap on Zapier Dashboard
</Image>

2. **Set up a Trigger**: To do so, perform the following steps:
   1. Select Formless from the App section.
   2. Select *New Response* as the Trigger Event.
   3. Connect your Formless account.

<Image alt="Set up a Trigger" align="center" width="75% " border={true} src="https://files.readme.io/fbcee2d3e913013487fbf3dca2392a9b9149f4a02b2e1944e6298b3b2aee5612-2025-09-23_00-23-25_1.gif">
  Set up a Trigger
</Image>

3. Select the form/survey you wish to act as the trigger.

<Image alt="Form Trigger" align="center" width="45% " border={true} src="https://files.readme.io/e58bb0dfd18ac21f204ac4b1f5ceae516e22917623df0dc896794b7c11d56967-image.png">
  Form Trigger
</Image>

4. Click **Test Trigger** to confirm Zapier pulls the most recent responses.

<Image alt="Details of Pulled Records" align="center" width="35% " border={true} src="https://files.readme.io/7f1fcbc477ca8568c5367ec4bd8e4ac12f1efaa3c2b5e63178658c54c51ca4a8-image.png">
  Details of Pulled Records
</Image>

5. **Set up the Action**:
   1. Select *CleverTap* from the App dropdown.
   2. Select *Create/Update User Profile* as the Action Event. This ensures that whenever a new form submission is captured, a user profile is created or updated.
   3. Connect your CleverTap account using the Account ID and Passcode obtained in [Create a Passcode on the CleverTap Dashboard](doc:formless#create-a-passcode-on-the-clevertap-dashboard).

<Image alt="Set up the Action" align="center" width="75% " border={true} src="https://files.readme.io/14f6131374828e1e0a577c3b53741886618f1d7e2b1b2051c89d3178764b67b2-2025-09-23_00-28-43_1.gif">
  Set up the Action
</Image>

6. **Configure the Action**. Map Formless data fields to CleverTap fields as follows:

| CleverTap Field    | Formless Field                                                                                                |
| ------------------ | ------------------------------------------------------------------------------------------------------------- |
| Identity           | Formless user ID, email, or any unique identifier                                                             |
| Object ID          | Leave blank if Identity is provided                                                                           |
| Creation Date      | Submission timestamp                                                                                          |
| Profile Properties | Responses in JSON format (for example: `{"name": "Alex", "email": "alex@example.com", "feedback": "Great!"}`) |

> 🚧 Mapping Identity and Object ID
>
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

7. Click **Continue**, and click **Test Step** to test the zap after mapping the files.

<Image alt="Test Zap" align="center" width="65% " border={true} src="https://files.readme.io/77c60c125de8493c4ecd4684395029090dbf3869d90eff9044fff10d3b40884a-image.png">
  Test Zap
</Image>

8. Click **Publish**. Also publish the campaign created in [Configure CleverTap Campaign](doc:formless#configure-clevertap-campaign).

<Image alt="In-App Message" align="center" width="35% " border={true} src="https://files.readme.io/0abfa1b352bd7b07519fd224919cab04d26b93c8a78f91d1f52e25105c5c994b-image.png">
  In-App Message
</Image>

### Upload Event

Consider an example where you want to track Formless survey submissions as events in CleverTap instead of updating user profiles. This automation ensures that every submission is logged for analytics, segmentation, and campaign triggers. To do so, perform the following steps:

1. Repeat *Step 1* to *Step 4* from [Create/Update User Profiles](doc:formless#createupdate-user-profiles) to configure Formless as the trigger.
2. **Set up the Action**. To do so, perform the following steps:

   1. Select *CleverTap* from the App dropdown.
   2. Select *Upload Event* as the Action Event. This ensures that each submission is recorded as an event in CleverTap.
   3. Connect your CleverTap account using the Account ID and Passcode obtained in [Create a Passcode on the CleverTap Dashboard](doc:formless#create-a-passcode-on-the-clevertap-dashboard).

<Image alt="Set up the Action" align="center" width="75% " border={true} src="https://files.readme.io/6a7b22641feede47f819c4c0c81e5f959b874244f9468327c688faf242016c44-2025-09-23_00-32-25_1.gif">
  Set up the Action
</Image>

3. **Configure the Action**. Map Formless data fields to CleverTap fields as follows:

| CleverTap Field  | Formless Field                                                                                        |
| ---------------- | ----------------------------------------------------------------------------------------------------- |
| User ID          | Formless user ID or email                                                                             |
| Object ID        | Leave blank if User ID is provided                                                                    |
| Creation Date    | Submission timestamp                                                                                  |
| Event Name       | Choose a descriptive event name (for example: `"Feedback Submitted"` or `"Survey Completed"`)         |
| Event Properties | Responses in JSON format (for example: `{"name": "Alex", "email": "alex@example.com", "score": "5"}`) |

> 🚧 Mapping Identity and Object ID
>
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

4. Click **Continue**, then click **Test Step** to validate that the event is sent successfully to CleverTap.
5. Click **Publish**. Also publish the campaign created in [Configure CleverTap Campaign](doc:formless#configure-clevertap-campaign). Each submission will now be logged as an event in CleverTap, enabling segmentation and automated journeys.

# FAQs

### Can I use both profile updates and events together?

Yes. You can set up multiple Zaps, one for updating user profiles and another for uploading events. This way, you can enrich CleverTap profiles with attributes while also logging submissions for analytics and campaign triggers.
