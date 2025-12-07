---
title: Formstack
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

[Formstack](https://www.formstack.com/) is a powerful online form-building and workflow automation platform that allows businesses to create custom forms, surveys, and data collection workflows without coding. It supports features such as conditional logic, hidden fields, payment integrations, and workflow automation.

Integrating Formstack with CleverTap via Zapier enables you to:

- **Capture Leads from Embedded Forms**: Embed Formstack forms in CleverTap campaigns (In-App Messages, Emails, or Web Popups) to [create or update user profiles](doc:formstack#createupdate-user-profiles) in real time.
- **Personalize Feedback Workflows**: Use hidden fields to capture user details and map them to CleverTap profiles.
- **Trigger Automated Engagement**: Record submissions as events in CleverTap by [uploading events](doc:formstack#upload-event) through Zapier.

# Prerequisites for Integration

To integrate Formstack with CleverTap via Zapier, ensure the following:

- Access to your **Formstack** account
- Access to an active **Zapier** account
- A CleverTap account with a valid **Account ID** and **Passcode**.

# Integrate Formstack with CleverTap Using Zapier

The integration involves the following four major steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:formstack#create-a-passcode-on-the-clevertap-dashboard)
2. [Configure Formstack Form](doc:formstack#configure-formstack-form)
3. [Configure CleverTap Campaign](doc:formstack#configure-clevertap-campaign)
4. [Connect Formstack and CleverTap via Zapier](doc:formstack#connect-formstack-and-clevertap-via-zapier)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Configure Formstack Form

Create a Formstack form that captures user inputs like contact details, feedback, or preferences. To do so, perform the following steps:

1. Go to your Formstack dashboard and create a form. For this example, create a simple Contact Form and save it.
2. Click the **Share** tab at the top and copy the **Website Embed** code snippet.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/02f27c66c84498aa010d2865549079bcf8805d2c96afbba3925f9f4a06704417-image.png",
        null,
        "Website Embed"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Website Embed"
    }
  ]
}
[/block]


Once the form is ready, it can be configured with CleverTap campaigns

## Configure CleverTap Campaign

Configure a CleverTap campaign to display your Formstack Form. This allows users to submit responses without leaving the app. To do so, perform the following steps:

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


3. Paste the Website Embed code copied in _Step 2_ of [Configure Formstack Form](doc:formstack#configure-formstack-form) into the _Custom HTML_ editor. Ensure the _Include JavaScript_ option is enabled.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e697931a25121c9f43ba2287eaa18c8bb0f29f6771c5e835877404b9ebf42f33-7603fda7-d6be-4e0d-a4fe-fe1494527df0.png",
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
5. Publish the campaign only after configuring the Zap as [Create/Update User Profiles](doc:formstack#createupdate-user-profiles) or [Upload Event](doc:formstack#upload-event).

## Connect Formstack and CleverTap via Zapier

Zapier acts as the automation bridge between Formstack and CleverTap. Whenever a user submits a Formstack response, Zapier captures the submission and forwards the data to CleverTap in real time. This allows you to:

- **Enrich or create user profiles** in CleverTap with the submitted attributes, or
- **Track each submission as an event** for segmentation, analytics, and automated engagement campaigns.

The integration supports two options depending on your use case:

- [Create/Update User Profiles](doc:formstack#createupdate-user-profiles)
- [Upload Event](doc:formstack#upload-event)

### Create/Update User Profiles

Consider an example where you want to automatically sync contact details captured in Formstack with CleverTap to enable personalized campaigns. This automation ensures that new submissions update user profiles in real time.  
To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**. Zapier can connect different applications, such as Formstack.

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
   1. Select Formstack from the App section. This starts the Zap when a trigger event occurs on Formstack.
   2. Select _Trigger Event_ from the dropdown list and then select _New Form_ for this use case.
   3. Select Account and sign in using your Formstack account credentials.

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
        "https://files.readme.io/0cd8695f2eb3892763c04048540bd8902da133a2025be8161ac0229cef23890e-image.png",
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
        "https://files.readme.io/2007e776ea6b55ae94e762b80b60bd9d22cbaf03c18490ee8546d4aa062244a6-2025-09-05_01-02-24_1.gif",
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


6. **Configure the Action**. Map Formstack data fields to CleverTap fields as follows:

| CleverTap Field    | Formstack Field                                                               |
| ------------------ | ----------------------------------------------------------------------------- |
| Identity           | Email or unique user identifier                                               |
| Object ID          | Leave blank if Identity is provided                                           |
| Creation Date      | Submission date or timestamp                                                  |
| Profile Properties | Form responses in JSON format (for example, name, email, rating, campaign ID) |

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


8. Click **Publish**. Also, publish the campaign you have created in [Configure CleverTap Campaign](<>). After this, users will receive an In-app message campaign as shown below, and the responses will be sent back to CleverTap via Zapier.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c79ba193af64541cf8e158e4dd8c8ea6cdb53ce0553631c9176e73476c481ef5-image.png",
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

1. Follow _Step 1_ to _Step 4_ from [Create/Update User Profiles](doc:formstack#createupdate-user-profiles) to configure Formstack as the trigger.
2. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:

   1. Select _CleverTap_ from the _App_ dropdown.
   2. Select _Upload Event_ from the Action event dropdown.
   3. Select Account to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:formstack#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

   [block:image]{"images":[{"image":["https://files.readme.io/2007e776ea6b55ae94e762b80b60bd9d22cbaf03c18490ee8546d4aa062244a6-2025-09-05_01-02-24_1.gif","","Select the Action for Zap"],"align":"center","sizing":"75% ","border":true,"caption":"Select the Action for Zap"}]}[/block]
3. **Configure the Action**. Map Formstack data fields to CleverTap fields as follows:

| CleverTap Field  | Formstack Field                                                              |
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

### Can I embed Formstack forms in Email or Web Popups?

Yes. Formstack forms can be embedded in any CleverTap campaign that supports custom HTML, including Email, In-App Messages, and Web Popups.