---
title: Engage Forms
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

[Engage Forms](https://www.engageforms.com/) is a no-code form builder that allows businesses to create and share interactive forms, surveys, and quizzes. With flexible embedding and integration support, it enables fast user data collection across channels.

Integrating Engage Forms with CleverTap via Zapier enables you to:

- **Capture User Details Seamlessly**: Embed forms into CleverTap campaigns (In-App Messages, Emails, or Web Popups) to [create or update user profiles](doc:engage-forms#createupdate-user-profiles) in real time.
- **Drive Personalization at Scale**: Sync user responses to CleverTap instantly and use them to segment audiences or trigger workflows.
- **Collect Feedback and Leads**: Log submission events in CleverTap to analyze responses and power automated engagement.

# Prerequisites for Integration

To integrate Engage Forms with CleverTap via Zapier, ensure the following:

- Access to your **Engage Forms** account
- Access to an active **Zapier** account
- A CleverTap account with a valid **Account ID** and **Passcode**.

# Integrate Engage Forms with CleverTap Using Zapier

The integration involves the following four major steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:engage-forms#create-a-passcode-on-the-clevertap-dashboard)
2. [Create and Configure Form in Engage Forms](doc:engage-forms#create-and-configure-form-in-engage-forms)
3. [Configure CleverTap Campaign](doc:engage-forms#configure-clevertap-campaign)
4. [Connect Engage Forms and CleverTap via Zapier](doc:engage-forms#connect-engage-forms-and-clevertap-via-zapier)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create and Configure Form in Engage Forms

Create an Engage Forms that captures user inputs like contact details, feedback, or preferences. To do so, perform the following steps:

1. Go to the Engage Forms dashboard and create a form. For this example, create a simple Contact Form that collects Name and Email ID. Save the form.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bcd89f55d7154c2de13289eb57959b04cead8667ab2204af1a033596d8cbf5cb-image.png",
        null,
        "Create Form"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Create Form"
    }
  ]
}
[/block]


2. Click the **Share** tab and mark the form as **Active**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/abc6a05ec26c0e3afdbe15ca3e7e46c6775923576d43347a47fb5b9057737fd5-782e7e5e-461a-4787-a179-99bffaa4ab87.png",
        null,
        "Share and Active Form"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Share and Active Form"
    }
  ]
}
[/block]


3. Copy the provided HTML snippet in the _Embed Engagement_ section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7ec6d9949ca0d7413256ce0b528aaa1c2db8caebdbdd03b82132a8333ecb7933-image.png",
        null,
        "Embed Engagement"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Embed Engagement"
    }
  ]
}
[/block]


By activating and embedding your form, you prepare it for CleverTap campaigns.

## Configure CleverTap Campaign

Configure a CleverTap campaign to display your Engage Form. This allows users to submit responses without leaving the app. To do so, perform the following steps:

1. In the CleverTap dashboard, create a new [In-App Message](doc:create-message-in-app) campaign (you can also use [Email](doc:create-message-email) or [Web Popups](doc:create-message-web-popup) that support HTML).
2. In the _What_ section, select a **Custom HTML Template** such as _Interstitial_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bba3ad2b5f24447d2d31901ac4b17efe32de2cadc35424f7d8ad323841e5869f-image.png",
        null,
        "Custom HTML Templates"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Custom HTML Templates"
    }
  ]
}
[/block]


3. Replace the existing code in the _Custom HTML_ editor with the Engage Forms snippet copied in _Step 3_ of [Create and Configure Form in Engage Forms](<>). Ensure the _Include JavaScript_ option is enabled.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e3e6a5daea1f5f567ba9b11de1bb59a6c750f4fad56f74ca48512ad606841813-image.png",
        null,
        "Preview and Test"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Preview and Test"
    }
  ]
}
[/block]


4. Click **Preview and Test** to verify that the form renders correctly.
5. Publish the campaign only after configuring the Zap as [Create/Update User Profiles](doc:engage-forms#createupdate-user-profiles) or [Upload Event](doc:engage-forms#upload-event).

## Connect Engage Forms and CleverTap via Zapier

Zapier acts as the automation bridge between Engage Forms and CleverTap. Whenever a user submits a Engage Forms response, Zapier captures the submission and forwards the data to CleverTap in real time. This allows you to:

- **Enrich or create user profiles** in CleverTap with the submitted attributes, or
- **Track each submission as an event** for segmentation, analytics, and automated engagement campaigns.

The integration supports two options depending on your use case:

- [Create/Update User Profiles](doc:engage-forms#createupdate-user-profiles)
- [Upload Event](doc:engage-forms#upload-event)

### Create/Update User Profiles

Consider an example where you want to automatically sync details captured in Engage Forms with CleverTap to drive personalized engagement. This ensures that each new submission updates the user’s profile in CleverTap in real time. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**. Zapier can connect different applications, such as Engage Forms.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/830b60a9c8f926bca524bfae5fa8a9aa021dad3d7e712f438b95c0486994e000-image.png",
        null,
        "Create a Zap on Zapier Dashboard"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Create a Zap on Zapier Dashboard"
    }
  ]
}
[/block]


2. **Set up a Trigger**. To do so, perform the following steps:
   1. Select Engage Forms from the App section. This starts the Zap when a trigger event occurs on Engage Forms.
   2. Select _Trigger Event_ from the dropdown list and then select _New Form_ for this use case.
   3. Select Account and sign in using your Engage Forms account credentials.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/44c9fa6df35f92d2ba8b43ec16127df92f923e6d7d18a9a40a514949da96fa08-2025-09-05_00-54-00_1.gif",
        "",
        "Set Up Trigger Event"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Set Up Trigger Event"
    }
  ]
}
[/block]


3. Click **Test Trigger**. This ensures that the correct account is connected and the trigger is set up correctly.  
   After testing the trigger, you will see a sample of the most recent responses to the form.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c64583b4649865c3059b3adb00738aa635b8bd4367adc7d0da36fbeb27362930-svsvscvsv.png",
        null,
        "Details of Pulled Records"
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true,
      "caption": "Details of Pulled Records"
    }
  ]
}
[/block]


4. Click **Continue with selected record**.
5. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:
   1. Select _CleverTap_ from the _App_ dropdown.
   2. Select _Create/Update User Profile_ from the Action event dropdown. This implies that whenever a new entry is generated, a new user profile is created, or an existing user profile is updated with the new information.
   3. Select Account to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:formstack#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6c1d337e77c0065877db7a400c6cdae01a55b96874d89a71a32a4d1bc2645005-2025-09-05_20-55-22_1.gif",
        "",
        "Select the Action for Zap"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Select the Action for Zap"
    }
  ]
}
[/block]


6. **Configure the Action**. Map Engage Forms data fields to CleverTap fields as follows:

| CleverTap Field    | Engage Forms Field                                                        |
| ------------------ | ------------------------------------------------------------------------- |
| Identity           | Email or unique user identifier                                           |
| Object ID          | Leave blank if Identity is provided                                       |
| Creation Date      | Submission date or timestamp                                              |
| Profile Properties | Form responses in JSON format (for example, name, email, campaign source) |

> 🚧 Mapping Identity and Object ID
> 
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

7. Click **Continue**, and click **Test Step** to test the zap after mapping the files.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/577d4059c2ab5d94ca101e57af0a211d283959fcc408efefc45c7170276d69f3-image.png",
        null,
        "Test Zap"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Test Zap"
    }
  ]
}
[/block]


8. Click **Publish**. Also, publish the campaign you have created in [Configure CleverTap Campaign](doc:engage-forms#configure-clevertap-campaign). After this, users will receive an In-app message campaign as shown below, and the responses will be sent back to CleverTap via Zapier.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/41a496c5abb031c28c58d6d17d97cd870b5fb932d9886f6eb4751780433d5423-fff.png",
        null,
        "In-app message"
      ],
      "align": "center",
      "sizing": "25% ",
      "border": true,
      "caption": "In-App Message"
    }
  ]
}
[/block]


### Upload Event

Consider an example where you want to track form submissions as events in CleverTap instead of updating user profiles. This automation ensures that every submission is logged for analytics and segmentation.

1. Follow _Step 1_ to _Step 4_ from [Create/Update User Profiles](doc:engage-forms#createupdate-user-profiles) to configure Engage Forms as the trigger.
2. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:

   1. Select _CleverTap_ from the _App_ dropdown.
   2. Select _Upload Event_ from the Action event dropdown.
   3. Select Account to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:engage-forms#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6c1d337e77c0065877db7a400c6cdae01a55b96874d89a71a32a4d1bc2645005-2025-09-05_20-55-22_1.gif",
        "",
        "Select the Action for Zap"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Select the Action for Zap"
    }
  ]
}
[/block]


3. **Configure the Action**. Map Engage Forms data fields to CleverTap fields as follows:

| CleverTap Field  | Engage Forms Field                                                           |
| ---------------- | ---------------------------------------------------------------------------- |
| User ID          | Email or unique user identifier                                              |
| Event Name       | Descriptive event name, such as "Form Submitted" or "Feedback Captured"      |
| Creation Date    | Submission timestamp                                                         |
| Event Properties | Responses in JSON format (for example, answers, ratings, campaign reference) |

> 🚧 Mapping Identity and Object ID
> 
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

4. Click **Continue**. Click **Test Step** to test the zap after mapping the files.
5. Click **Publish**.

Once published, every new form submission will automatically appear in CleverTap as an event, enabling deeper analytics, segmentation, and campaign targeting.

# FAQs

### Can I embed Engage Forms in Email or Web Popups?

Yes. The integration works with any CleverTap campaign that supports custom HTML, including **Email**, **Web Popups**, and **In-App Messages**.