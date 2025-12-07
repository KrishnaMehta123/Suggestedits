---
title: Forms.app
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

[Forms.app](https://forms.app/) is an intuitive online form builder that enables businesses to create customizable forms, surveys, and quizzes without coding. It supports hidden fields, conditional logic, and Zapier integrations, making it a powerful tool to capture actionable data. Forms can be embedded via iframe or shared via links, enabling seamless integration into marketing campaigns.

Integrating Forms.app with CleverTap via Zapier enables you to:

- **Collect Data Seamlessly**: Embed forms inside CleverTap campaigns (In-App, Email, or Web Popups) and capture user responses in real time.
- **Personalize Experiences**: Pass hidden parameters such as email or identity from CleverTap to tie responses back to user profiles.
- **Trigger Automated Workflows**: Log form submissions as events or update profiles in CleverTap to power segmentation and personalized campaigns.

# Prerequisites for Integration

Before integrating forms.app with CleverTap via Zapier, ensure the following:

- Access to your **Forms.app** account
- Access to an active **Zapier** account
- A CleverTap account with valid **Account ID**, **Passcode**, and **Region**

# Integrate forms.app with CleverTap Using Zapier

The integration involves the following four steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:formsapp#create-a-passcode-on-the-clevertap-dashboard)
2. [Create a Form in Forms.app](doc:formsapp#create-a-form-in-formsapp)
3. [Configure CleverTap Campaign](doc:formsapp#configure-clevertap-campaign)
4. [Connect forms.app and CleverTap via Zapier](doc:formsapp#connect-formsapp-and-clevertap-via-zapier)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create a Form in Forms.app

Consider an example where you want to capture user ratings and link the response to their CleverTap profile. To do this, you first need to create a form in Forms.app, To do so, perform the following steps:

1. Go to your forms app dashboard and create a new form (for example, a simple ratings form). For this example, we will create a simple form that gathers ratings from users about their experience.
2. Add an _Email field_. In the field settings, enable both _Get values from URL_ and _Hidden Field_ to capture the user’s email via URL parameters.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c84c4af512b4795da40e6547ee04ddab301ade218689cd1820bb98b419d0474c-image.png",
        null,
        "Create Reating form"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Create Rating Form"
    }
  ]
}
[/block]


3. Copy the form URL under the _Get values from URL_ option.

## Configure CleverTap Campaign

Configure a CleverTap campaign to display your form created in form.app. This allows users to submit responses without leaving the app. To do so, perform the following steps:

1. In the CleverTap dashboard, create a new [In-App Message](doc:create-message-in-app) campaign (you can also use [Email](doc:create-message-email) or [Web Popups](doc:create-message-web-popup) that support HTML).
2. In the _What_ section, select a **Custom HTML Template** such as _Interstitial_ template.

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


3. Replace the existing code inside the _Custom HTML_ section and paste the URL snippet copied from _Step 3_ of [Create a Form in Forms.app](doc:formsapp#create-a-form-in-formsapp).

```html
<iframe 
 id="" 
 allowtransparency="true" 
 allowfullscreen="true" 
 allow="geolocation" 
 src="https://show.forms.app/form/68876c6dc2528d0002e54960#68876c32198cc1cb56bfefbf={{ Profile.Email | default: \"test@gmail.com\" }}" 
 frameborder="0" 
 style="width: 100vw; min-width:100%; height:600px; border:none;">
</iframe>
```

In this example, [Liquid tags](https://docs.clevertap.com/docs/liquid-tags) dynamically pass the email parameter from the CleverTap user profile.

4. Click **Preview and Test** to verify that the form renders correctly.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/23466c8a1cbfdf08b18ae6c858e0855db9b44954d4b35926b38d5387df25944d-19bdf2ad-0c92-4c32-bfde-6e4508a356e6.png",
        null,
        "Preview and Test"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Preview and Test"
    }
  ]
}
[/block]


5. Publish the campaign only after configuring the Zap as [Create/Update User Profiles](doc:formsapp#createupdate-user-profiles) or [Upload Event](doc:formsapp#upload-event).

## Connect Forms.app and CleverTap via Zapier

Zapier acts as the automation bridge between Forms.app and CleverTap. Whenever a user submits a Survey response, Zapier captures the submission and forwards the data to CleverTap in real time. This allows you to:

- **Enrich or create user profiles** in CleverTap with the submitted attributes, or
- **Track each submission as an event** for segmentation, analytics, and automated engagement campaigns.

The integration supports two options depending on your use case:

- [Create/Update User Profiles](doc:formsapp#createupdate-user-profiles)
- [Upload Event](doc:formsapp#upload-event)

### Create/Update User Profiles

Consider an example where you want to automatically sync details captured in Forms.app with CleverTap to drive personalized engagement. This ensures that each new submission updates the user’s profile in CleverTap in real time. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**. Zapier can connect different applications, such as Forms.app.

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
   1. Select Forms.app from the App section. This starts the Zap when a trigger event occurs on Forms.app.
   2. Select _Trigger Event_ from the dropdown list and then select _New Form Submission_ for this use case.
   3. Select Account and sign in using your Form.app account credentials.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9bb4b5f4edf15d70f19d037733865c4674c862db68659a2d81cdd5e52cf30b70-2025-09-18_13-44-00_1.gif",
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


3. Select the form/survey you wish to act as the trigger.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3ae875e7b00dc64e27c3e87e25450f4b8f7a5e93346998e663bd77f63f6407b4-image.png",
        null,
        "Form Trigger"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Form Trigger"
    }
  ]
}
[/block]


4. Click **Test Trigger**. This ensures that the correct account is connected and the trigger is set up correctly.  
   After testing the trigger, you will see a sample of the most recent responses to the form.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5fd2aeff0817072b4bcb33205e23b4b63056e98ed44c6b7e24d7194b5b6bb445-429aaa45-1d98-4334-8c68-1ad766164de2.png",
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
   2. Select _Create/Update User Profile_ from the Action event dropdown. This implies that whenever a new response is generated, a new user profile is created, or an existing user profile is updated with the new information.
   3. Select _Account_ to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:formsapp#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8869e2a1cbf9c0aebdb7b8eccfa5dc3171f093862ffb29535208ae368700faad-2025-09-18_13-49-02_1.gif",
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


6. **Configure the Action**. Map Form.app data fields to CleverTap fields as follows:

| CleverTap Field    | Form.app Field                                                                                            |
| ------------------ | --------------------------------------------------------------------------------------------------------- |
| Identity           | Email or unique identifier from hidden fields                                                             |
| Object ID          | Leave blank if Identity is provided                                                                       |
| Creation Date      | Submission timestamp                                                                                      |
| Profile Properties | Form responses in JSON format (for example: `{"name": "Alex", "email": "alex@example.com", "rating": 5}`) |

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
      "sizing": "75% ",
      "border": true,
      "caption": "Test Zap"
    }
  ]
}
[/block]


8. Click **Publish**. Also, publish the campaign you have created in [Configure CleverTap Campaign](doc:formsapp#configure-clevertap-campaign). After this, users will receive an In-App message campaign as shown below, and the responses will be sent back to CleverTap via Zapier.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/69465862d2b58eda3bedc10e930c257b0a64ca09eb421430461e1ebf8bc847b4-604c3b5b-fb10-43b8-9aba-50286ce9ca95.png",
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

Consider an example where you want to track survey submissions as events in CleverTap instead of updating user profiles. This automation ensures that every submission is logged for analytics and segmentation.

1. Follow _Step 1_ to _Step 4_ from [Create/Update User Profiles](doc:formsapp#createupdate-user-profiles) to configure Forms.app as the trigger.
2. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:

   1. Select _CleverTap_ from the _App_ dropdown.
   2. Select _Upload Event_ from the Action event dropdown.
   3. Select _Account_ to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:formsapp#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6f055e87bf0dccdad506a64ef384f41daa95d924037889f5ad8273d4639170b6-2025-09-18_13-51-16_1.gif",
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


3. **Configure the Action**. Map Forms.app data fields to CleverTap fields as follows:

| CleverTap Field  | Forms.app Field                                                                              |
| ---------------- | -------------------------------------------------------------------------------------------- |
| User ID          | Email or unique identifier from hidden fields                                                |
| Object ID        | Leave blank if User ID is provided                                                           |
| Creation Date    | Submission timestamp                                                                         |
| Event Name       | Choose a descriptive event name (for example: `"Feedback Submitted"` or `"Rating Captured"`) |
| Event Properties | Responses in JSON format (for example: `{"rating": 5, "comment": "Great app!"}`)             |

> 🚧 Mapping Identity and Object ID
> 
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

4. Click **Continue**. Click **Test Step** to test the zap after mapping the files.
5. Click **Publish**. Also, publish the campaign you have created in [Configure CleverTap Campaign](doc:formsapp#configure-clevertap-campaign). Each submission will now be logged as an event in CleverTap.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/16443ad907e1f3f0668d1b40fac6a0dd0795ea876a80ef28f360f842286062c3-image.png",
        null,
        "Verify Event Tracking in CleverTap"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Verify Event Tracking in CleverTap"
    }
  ]
}
[/block]


# FAQs

### Can I update profiles instead of uploading events?

Yes. Depending on your use case, you can choose either **Create/Update User Profile** or **Upload Event** as the action in Zapier. This gives you the flexibility to either update CleverTap user attributes or log submissions as events.