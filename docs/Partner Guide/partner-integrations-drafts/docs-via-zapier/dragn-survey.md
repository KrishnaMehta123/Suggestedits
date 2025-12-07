---
title: Drag’n Survey
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

[Drag’n Survey](https://www.dragnsurvey.com/) is an online survey platform that enables businesses to design, distribute, and analyze surveys with ease. With its drag-and-drop interface and customizable templates, you can quickly create forms, quizzes, and polls, no coding required. Surveys can be embedded in websites, emails, or apps and integrated with platforms like Zapier for automation.

Integrating Drag’n Survey with CleverTap via Zapier enables you to:

- **Capture Leads Seamlessly**: Create surveys in Drag’n Survey and use them in CleverTap campaigns (In-App, Email, or Web Popups) to [create or update user profiles](doc:dragn-survey#createupdate-user-profiles).
- **Run Quick Polls and Feedback Campaigns**: Collect preferences directly inside your app and sync them to CleverTap.
- **Automate Personalized Engagement**: Upload survey responses as events in CleverTap to trigger workflows and segment audiences.

# Prerequisites for Integration

To integrate Drag’n Survey with CleverTap via Zapier, ensure the following:

- Access to your **Drag’n Survey** account
- Access to an active **Zapier** account
- A CleverTap account with a valid **Account ID** and **Passcode**.

# Integrate Drag'n Survey with CleverTap Using Zapier

The integration involves the following four major steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:dragn-survey#create-a-passcode-on-the-clevertap-dashboard)
2. [Create Drag’n Survey Form](doc:dragn-survey#create-dragn-survey-form)
3. [Configure CleverTap Campaign](doc:dragn-survey#configure-clevertap-campaign)
4. [Connect Drag'n Survey and CleverTap via Zapier](doc:dragn-survey#connect-dragn-survey-and-clevertap-via-zapier)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create Drag’n Survey Form

Create a survey form that captures user inputs like contact details, feedback, or preferences. To do so, perform the following steps:

1. Go to the Drag’n Survey dashboard and create a survey. For this example, create a simple survey form that collects Name and Email ID. Save the survey.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cddb9c8213dda15e2bf368868c32dfd3d051e92a4f5a0f27687baf405c972996-5a743436-8291-4043-8ee6-427d72515fa8_1.png",
        null,
        "Create survey"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Create Survey"
    }
  ]
}
[/block]


2. From the available distribution options, select _HTML Widget_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/de013ffdb51add9e5492d72adfc0e49f5c586bb2fc62ae09f18e2bcc0b9c5449-ffffe.png",
        "",
        "Distribution Options"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Distribution Options"
    }
  ]
}
[/block]


3. Set the _Height_ and _Width_ of the survey as required.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9842b0174cea33e87ddad7ffacf46b02eaf1a4a563cc7eab413f897533c03dad-image.png",
        null,
        "Set HTML Widget"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Set HTML Widget"
    }
  ]
}
[/block]


4. Click the **Create Collector** button, and you will be provided with an _HTML code_ snipper.
5. Click **Copy Link** to copy the _HTML Widget_, which will be used to configure it into the CleverTap campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/35f9c8421764d2691ab3dc8bc64dba5ba6792d7969eb908f11f7170f30dbcd76-24484df8-dfba-49a5-92e3-df81ac2a74cb.png",
        null,
        "Copy HTML Widget"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Copy HTML Widget"
    }
  ]
}
[/block]


## Configure CleverTap Campaign

Configure a CleverTap campaign to display your survey. This allows users to submit responses without leaving the app. To do so, perform the following steps:

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


3. Replace the existing code inside the _Custom HTML_ section and paste the HTML snippet copied from _Step 5_ of [Create Drag’n Survey Form](doc:dragn-survey#create-dragn-survey-form).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a75b60da1b5d304aa941ed69ba847ad73443e7d0b76af6f97bd235cdc01862d6-ff.png",
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
5. Publish the campaign only after configuring the Zap as [Create/Update User Profiles](doc:dragn-survey#createupdate-user-profiles) or [Upload Event](doc:dragn-survey#upload-event).

## Connect Drag’n Survey and CleverTap via Zapier

Zapier acts as the automation bridge between Drag’n Survey and CleverTap. Whenever a user submits a Survey response, Zapier captures the submission and forwards the data to CleverTap in real time. This allows you to:

- **Enrich or create user profiles** in CleverTap with the submitted attributes, or
- **Track each submission as an event** for segmentation, analytics, and automated engagement campaigns.

The integration supports two options depending on your use case:

- [Create/Update User Profiles](doc:dragn-survey#createupdate-user-profiles)
- [Upload Event](doc:dragn-survey#upload-event)

### Create/Update User Profiles

Consider an example where you want to automatically sync details captured in Drag’n Survey with CleverTap to drive personalized engagement. This ensures that each new submission updates the user’s profile in CleverTap in real time. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**. Zapier can connect different applications, such as Drag’n Survey.

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
   1. Select Drag'n Survey from the App section. This starts the Zap when a trigger event occurs on Drag'n Survey.
   2. Select _Trigger Event_ from the dropdown list and then select _Respondent Answers_ for this use case.
   3. Select Account and sign in using your Drag’n Survey account credentials.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/969d43e1da5e8eb667c1d6bb5dfdd95bd2b2d3d82b8941a85c8b7e2b3be0d424-2025-09-06_00-31-06_1.gif",
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
        "https://files.readme.io/450b58edd50593f6d1851f5ed7d20abc0ccd9a407a0f4d8a3443706540da4e20-71d1b985-a5ee-4d5c-ba30-a1a609842bcd.png",
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
   2. Select _Create/Update User Profile_ from the Action event dropdown. This implies that whenever a new responses is generated, a new user profile is created, or an existing user profile is updated with the new information.
   3. Select _Account_ to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:dragn-survey#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7e0701457b948af7de4d344701fd624dac25edbbb286e66d781f3ec1aace5eb5-2025-09-06_00-36-34_1.gif",
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


6. **Configure the Action**. Map Drag'n Survey data fields to CleverTap fields as follows:

| CleverTap Field    | Drag'n Survey Field                                                       |
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


8. Click **Publish**. Also, publish the campaign you have created in [Configure CleverTap Campaign](doc:dragn-survey#configure-clevertap-campaign). After this, users will receive an In-app message campaign as shown below, and the responses will be sent back to CleverTap via Zapier.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1c76356e4acf261ad4bde75d73305be880e5b506f921aa56010ce24a85dfbd65-652bd61a-a9df-4c51-9658-ccbec2e9a776.png",
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

1. Follow _Step 1_ to _Step 4_ from [Create/Update User Profiles](doc:dragn-survey#createupdate-user-profiles) to configure Drag'n Survey as the trigger.
2. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:

   1. Select _CleverTap_ from the _App_ dropdown.
   2. Select _Upload Event_ from the Action event dropdown.
   3. Select _Account_ to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:dragn-survey#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bd19b886cdda636b6c77860fb646d6f8c475b3558171e5da7b455eb95fa26383-2025-09-06_00-36-34_1.gif",
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


3. **Configure the Action**. Map Drag'n Survey data fields to CleverTap fields as follows:

| CleverTap Field  | Drag'n Survey Field                                                          |
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

Once published, every new survey response submission will automatically appear in CleverTap as an event, enabling deeper analytics, segmentation, and campaign targeting.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6df0d273fbae48921af841cc8eb7a67667b76c4bcba536c24b61f8874efdaaa3-image.png",
        null,
        "Verify on the CleverTap dashboard"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Verify on the CleverTap dashboard"
    }
  ]
}
[/block]