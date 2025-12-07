---
title: Tally
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

[Tally](https://tally.so/) is a no-code form builder that allows brands to collect data, feedback, and user preferences through interactive and customizable forms. By integrating Tally with CleverTap via Zapier, you can seamlessly route user responses into CleverTap for real-time personalization, segmentation, and campaign automation.

Integrating Tally with CleverTap via Zapier allows you to:

- **Capture User Feedback Seamlessly**: Collect and send Tally form responses to CleverTap in real time.
- **Trigger Personalized Campaigns**: Use form responses to trigger context-aware CleverTap journeys.
- **Update User Profiles Automatically**: Enrich user profiles with submitted form data for deeper segmentation.
- **Enable Form-Driven Journeys**: Convert form responses into actionable engagement flows.

# Prerequisites for Integration

Before integrating Tally with CleverTap via Zapier, ensure the following:

- Access to your **Tally** account
- Access to an active **Zapier** account
- A CleverTap account with a valid **Account ID** and **Passcode**

# Integrate Tally with CleverTap Using Zapier

The integration involves the following four major steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:tally#create-a-passcode-on-the-clevertap-dashboard)
2. [Create a Form in Tally](doc:tally#create-a-form-in-tally)
3. [Configure CleverTap Campaign](doc:tally#configure-clevertap-campaign)
4. [Connect Tally and CleverTap via Zapier](doc:tally#connect-tally-and-clevertap-via-zapier)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate API requests. Every CleverTap API call must include Account ID and Passcode as request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create a Form in Tally

Consider an example where you want to collect feedback after a purchase using Tally. To do so, perform the following steps:

1. Log in to your Tally dashboard.
2. Create a new form based on your use case (for example, customer feedback, lead capture, survey).
3. Click **Publish** to make the form live.
4. Go to the _Share_ tab, scroll down to the _Embed Form_ section.
5. Select _Full Page_ and click **Get Code**.
6. Copy the generated HTML embed snippet.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9a945ab2549a754fe8166c94cf05a3f01eca6b03135e7ecdfa8e2195520e00d7-Screen_Recording_2025-07-16_at_2.59.58PM_1.gif",
        "",
        "Create a Form in Tally"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Create a Form in Tally"
    }
  ]
}
[/block]


## Configure CleverTap Campaign

You can embed a Tally form into a CleverTap campaign to collect responses directly through in-app notifications, emails, or web popups. In this use case, you’ll configure a CleverTap in-app campaign. To do so, follow these steps:

1. In the CleverTap dashboard, create a new _In-App Message_ campaign (you can also use [Web Popups](doc:create-message-web-popup) or [Email](doc:create-message-email) campaigns that support HTML).
2. In the _What_ section, select a _Custom HTML Template_ such as _Interstitial_.
3. Replace the existing code with the HTML snippet copied from _Step 6_ of [Create a Form in Tally](doc:tally#create-a-form-in-tally).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9c506f80e7329d279b7c8c8b6d02059c6bb2e0baf08fe7c7e840425c3f0b81fc-image.png",
        null,
        "Embed Tally Form in CleverTap Campaign"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Embed Tally Form in CleverTap Campaign"
    }
  ]
}
[/block]


4. Configure the remaining campaign parameters (target audience, display rules, and so on) as needed.
5. Publish the campaign only after configuring the Zap as [Create/Update User Profiles](doc:tally#createupdate-user-profiles) or [Upload Event](doc:tally#upload-event).

## Connect Tally Form and CleverTap via Zapier

Zapier acts as a bridge between Tally Form and CleverTap. When a user submits a response, Zapier captures it and sends the data to CleverTap in real time. You can either update user profiles or log submissions as events.

The integration supports two use cases:

- [Create/Update User Profiles](doc:tally#createupdate-user-profiles)
- [Upload Event](doc:tally#upload-event)

### Create/Update User Profiles

Use this option if you want Tally responses to update user profiles in CleverTap for personalization and segmentation. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**. Zapier can connect various applications, including Outgrow.

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
   1. Select Tally from the App section. This starts the Zap when a trigger event occurs on the Tally form.
   2. Select _Trigger Event_ from the dropdown list and then select _New Submission_ for this use case.
   3. Select Account and sign in using your Tally account credentials.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/681b91d5f9553af0d6c3bbce96567fd5e4e9c0c2ce1cef6f5d9501985c5eb629-2025-11-09_01-21-17_1.gif",
        null,
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
        "https://files.readme.io/fdeb6e5b1761c910da7b51c638be4150ca425b41e19b06ee52bfce1a11af98ac-0475f058-844e-4780-988c-41e0d0dcf7e1.png",
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
   3. Select _Account_ to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:tally#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4fde4ae1ef630fdc81d379646281f48961a10731663daa12c42cf3486ad8b62f-2025-11-09_01-24-41_1.gif",
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


6. **Configure the Action**. Map Tally data fields to CleverTap fields as follows:

| CleverTap Field    | Tally Field                                                                                                      |
| ------------------ | ---------------------------------------------------------------------------------------------------------------- |
| User ID            | Tally user ID, email, or unique identifier.                                                                      |
| Object ID          | Unique identifier for the user.                                                                                  |
| Creation Date      | Date of the user’s creation in Tally.                                                                            |
| Profile Properties | Responses in JSON format (for example: `{"name": "Alex", "email": "alex@example.com", "interests": "Webinars"}`) |

> 🚧 Mapping Identity and Object ID
> 
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

7. Click **Continue**, and click **Test Step** to test the Zap after mapping the fields.

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


8. Click **Publish**. Also, publish the campaign you have created in [Configure CleverTap Campaign](doc:tally#configure-clevertap-campaign). After this, users will receive the form you have created, and the responses will be reflected in your CleverTap dashboard. If the user doesn’t exist, a new user will be created.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bb57bc21dea524bdef5301df393f06b8102f24c163b5feb51023a1a02f75d626-image.png",
        null,
        "Verify on the CleverTap dashboard"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Verify on the CleverTap dashboard"
    }
  ]
}
[/block]


### Upload Event

Consider an example where you want to track form submissions as events in CleverTap instead of updating user profiles. This automation ensures that every submission is logged for analytics and segmentation.

1. Follow _Step 1_ to _Step 4_ from [Create/Update User Profiles](doc:tally#createupdate-user-profiles) to configure Outgrow as the trigger.
2. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:

   1. Select _CleverTap_ from the _App_ dropdown.
   2. Select _Upload Event_ from the Action event dropdown.
   3. Select _Account_ to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:tally#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f56e5f33a14ccac6849bc7dd883bda50dfe70a1adfaca1947cfde6b7ef673583-image.png",
        null,
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


3. **Configure the Action**. Map Tally data fields to CleverTap fields as follows:

| CleverTap Field  | Tally Field                                                                                                |
| ---------------- | ---------------------------------------------------------------------------------------------------------- |
| User ID          | Tally user ID, email, or unique identifier                                                                 |
| Object ID        | Leave blank if User ID is provided                                                                         |
| Creation Date    | Date of the user’s creation in Tally.                                                                      |
| Event Name       | Choose a descriptive event name (for example: `Feedback Submitted`, `Form Completed`)                      |
| Event Properties | Metadata in JSON format (for example: `{"rating": 5, "comment": "Great service!", "delivery": "On Time"}`) |

> 🚧 Mapping Identity and Object ID
> 
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

4. Click **Continue**. Click **Test Step** to test the Zap after mapping the fields.
5. Click **Publish**. Also, publish the campaign you have created in [Configure CleverTap Campaign](doc:tally#configure-clevertap-campaign). Each submission will now be logged as an event in CleverTap.

Once the campaign is published, the user will be shown the form as shown in the image below for the In-App campaign, and their responses will be reflected in the CleverTap dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f5f215b12728d6d6bd6988cb8b18a2e61e4e5cae609188d3910f534ba47cc6ce-image.png",
        null,
        "In-App Message"
      ],
      "align": "center",
      "sizing": "25% ",
      "border": true,
      "caption": "In-App Message"
    }
  ]
}
[/block]


# FAQs

### Can I use both profile updates and events together?

Yes. You can set up multiple Zaps, one for updating user profiles and another for uploading events. This way, you can both enrich CleverTap profiles with attributes and log submissions for analytics and campaign triggers.