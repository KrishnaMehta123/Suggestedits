---
title: Pro Forms
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

[Pro Forms](https://pro-forms.co.uk/) is a versatile online form builder designed for lead capture, surveys, and customer data collection. With its customizable form templates and sharing options, Pro Forms enables businesses to collect user data across multiple touchpoints.

Integrating Pro Forms with CleverTap via Zapier allows you to:

* **Capture Leads Seamlessly**: Automatically sync user data collected from Pro Forms into CleverTap.
* **Update Profiles in Real Time**: Create or update user profiles based on form submissions.
* **Trigger Automated Campaigns**: Start CleverTap journeys such as welcome campaigns immediately after form submissions.
* **Enrich Profiles for Segmentation**: Add specific form responses (e.g., webinar signup, content download) to CleverTap profiles for better targeting.

# Prerequisites for Integration

Before integrating Pro Forms with CleverTap via Zapier, ensure the following:

* Access to your **Pro Forms** account
* Access to an active **Zapier** account
* A CleverTap account with a valid **Account ID** and **Passcode**.

# Integrate Pro Forms with CleverTap Using Zapier

The integration involves the following four major steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:pro-forms#create-a-passcode-on-the-clevertap-dashboard)
2. [Create a Form in Pro Forms](doc:pro-forms#create-a-form-in-pro-forms)
3. [Configure CleverTap Campaign](doc:pro-forms#configure-clevertap-campaign)
4. [Connect Pro Forms and CleverTap via Zapier](doc:pro-forms#connect-pro-forms-and-clevertap-via-zapier)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create a Form in Pro Forms

Consider an example where you want to capture user details such as Name, Email, and Preferences via a Pro Forms survey inside a CleverTap campaign. To do so, perform the following steps:

1. Log in to your Pro Forms dashboard and create a form that meets your requirements.
2. Once the form is ready, go to the *Publish* tab and click on **Share as iframe**.
3. This will copy the code snippet to use this form inside CleverTap campaigns.

<Image alt="Create a Form in Pro Forms" align="center" width="75% " border={true} src="https://files.readme.io/b0ba445433f57f5f342dbe1e042d19c4b38a7638a3d44678de7dc3bd69830a2c-image.png">
  Create a Form in Pro Forms
</Image>

## Configure CleverTap Campaign

Configure a CleverTap campaign to display your form created in Pro Forms. This allows users to submit responses without leaving the app. To do so, perform the following steps:

1. In the CleverTap dashboard, create a new [In-App Message](doc:create-message-in-app) campaign (you can also use [Email](doc:create-message-email) or [Web Popups](doc:create-message-web-popup) that support HTML).
2. In the *What* section, select a **Custom HTML Template** such as *Interstitial* template.

<Image alt="Custom HTML Templates" align="center" width="75% " border={true} src="https://files.readme.io/bba3ad2b5f24447d2d31901ac4b17efe32de2cadc35424f7d8ad323841e5869f-image.png">
  Custom HTML Templates
</Image>

3. Replace the existing code inside the *Custom HTML* section with the URL snippet copied from *Step 3* of [Create a Form in Pro Forms](doc:pro-forms#create-a-form-in-pro-forms).
4. In the snippet, update the form source URL to use the `HTTPS` version provided by Pro Forms instead of `HTTP`.

```html
<iframe width="100%" height="900px" src="https://web.pro-forms.co.uk/onlineForms/entry.phtml?code=qwot2arm"></iframe>
```

5. Click **Preview and Test** to verify that the form renders correctly.

<Image alt="Preview and Test" align="center" width="75% " border={true} src="https://files.readme.io/c5d8ce035166f5b7cbdbb3777479247c5c44707ab8bfe6883e537afda4da5a11-6f8a53b1-6b07-4a09-9742-9712c34badd5.png">
  Preview and Test
</Image>

6. Publish the campaign only after configuring the Zap as [Create/Update User Profiles](doc:pro-forms#createupdate-user-profiles) or [Upload Event](doc:pro-forms#upload-event).

## Connect Pro Forms and CleverTap via Zapier

Zapier acts as the automation bridge between Pro Forms and CleverTap. Whenever a user submits a Survey response, Zapier captures the submission and forwards the data to CleverTap in real time. This allows you to:

* **Enrich or create user profiles** in CleverTap with the submitted attributes, or
* **Track each submission as an event** for segmentation, analytics, and automated engagement campaigns.

The integration supports two options depending on your use case:

* [Create/Update User Profiles](doc:pro-forms#createupdate-user-profiles)
* [Upload Event](doc:pro-forms#upload-event)

### Create/Update User Profiles

Consider an example where you want to automatically sync details captured in Pro Forms with CleverTap to drive personalized engagement. This ensures that each new submission updates the user’s profile in CleverTap in real time. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**. Zapier can connect different applications, such as Pro Forms.

<Image alt="Create a Zap on Zapier Dashboard" align="center" width="75% " border={true} src="https://files.readme.io/830b60a9c8f926bca524bfae5fa8a9aa021dad3d7e712f438b95c0486994e000-image.png">
  Create a Zap on Zapier Dashboard
</Image>

2. **Set up a Trigger**. To do so, perform the following steps:
   1. Select Pro Forms from the App section. This starts the Zap when a trigger event occurs on Pro Forms.
   2. Select *Trigger Event* from the dropdown list and then select *New Submission* for this use case.
   3. Select Account and sign in using your Pro Forms account credentials.

<Image alt="Set Up Trigger Event" align="center" width="75% " border={true} src="https://files.readme.io/0c3b75f63f564279c7d38df93dc61d79018ff901788ae756784a667b52a2cc06-2025-09-18_17-04-06_1.gif">
  Set Up Trigger Event
</Image>

3. Select the form/survey you wish to act as the trigger.

<Image alt="Form Trigger" align="center" width="75% " border={true} src="https://files.readme.io/d66e9c17b9eeb04a45de4231281e17bd92f165a2ce3ac6aba6d8f682450c809a-2cf14213-b843-425f-9358-b2d0cda9b890.png">
  Form Trigger
</Image>

4. Click **Test Trigger**. This ensures that the correct account is connected and the trigger is set up correctly.\
   After testing the trigger, you will see a sample of the most recent responses to the form.

<Image alt="Details of Pulled Records" align="center" width="50% " border={true} src="https://files.readme.io/c039f6489499f193a231985d97f03e7758d570d82ec308f6968b2a5fb370b289-d7776e4f-1912-449d-be5b-9587863f786a.png">
  Details of Pulled Records
</Image>

5. Click **Continue with selected record**.
6. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:
   1. Select *CleverTap* from the *App* dropdown.
   2. Select *Create/Update User Profile* from the Action event dropdown. This implies that whenever a new response is generated, a new user profile is created, or an existing user profile is updated with the new information.
   3. Select *Account* to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:pro-forms#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

<Image alt="Select the Action for Zap" align="center" width="75% " border={true} src="https://files.readme.io/c6fbe69e56e1972aba0455efb9f8768c374ef44047a2e361c0b25284e71d104c-2025-09-18_17-06-50_1.gif">
  Select the Action for Zap
</Image>

7. **Configure the Action**. Map Pro Forms data fields to CleverTap fields as follows:

| CleverTap Field    | Pro Forms Field                                                                                                  |
| ------------------ | ---------------------------------------------------------------------------------------------------------------- |
| Identity           | Pro Forms user ID field, email, or any unique identifier                                                         |
| Object ID          | Leave blank if Identity is provided                                                                              |
| Creation Date      | Submission timestamp                                                                                             |
| Profile Properties | Responses in JSON format (for example: `{"name": "Alex", "email": "alex@example.com", "interests": "Webinars"}`) |

> 🚧 Mapping Identity and Object ID
>
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

8. Click **Continue**, and click **Test Step** to test the zap after mapping the files.

<Image alt="Test Zap" align="center" width="75% " border={true} src="https://files.readme.io/577d4059c2ab5d94ca101e57af0a211d283959fcc408efefc45c7170276d69f3-image.png">
  Test Zap
</Image>

9. Click **Publish**. Also, publish the campaign you have created in [Configure CleverTap Campaign](doc:pro-forms#configure-clevertap-campaign). After this, users will receive an In-App message campaign as shown below, and the responses will be sent back to CleverTap via Zapier.

<Image alt="In-app message" align="center" width="25% " border={true} src="https://files.readme.io/2da1e39f60927e66be00a066f6c307ef3e71371904cf97c5136003b40dcf89be-89eecb01-a0cc-4ab3-863f-a9bb63cdde83.png">
  In-App Message
</Image>

### Upload Event

Consider an example where you want to track form submissions as events in CleverTap instead of updating user profiles. This automation ensures that every submission is logged for analytics and segmentation.

1. Follow *Step 1* to *Step 4* from [Create/Update User Profiles](doc:pro-forms#createupdate-user-profiles) to configure Pro Forms as the trigger.
2. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:

   1. Select *CleverTap* from the *App* dropdown.
   2. Select *Upload Event* from the Action event dropdown.
   3. Select *Account* to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:pro-forms#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

<Image alt="Select the Action for Zap" align="center" width="75% " border={true} src="https://files.readme.io/d5f8075b5818961947893bad492ef236aa53ca1f47a49cab450daf1019e0d334-2025-09-18_17-08-30_1.gif">
  Select the Action for Zap
</Image>

3. **Configure the Action**. Map Pro Forms data fields to CleverTap fields as follows:

| CleverTap Field  | Pro Forms Field                                                                                                    |
| ---------------- | ------------------------------------------------------------------------------------------------------------------ |
| User ID          | Pro Forms user ID field or email                                                                                   |
| Object ID        | Leave blank if User ID is provided                                                                                 |
| Creation Date    | Submission timestamp                                                                                               |
| Event Name       | Choose a descriptive event name (for example: `"Form Submitted"` or `"Webinar Registered"`)                        |
| Event Properties | Responses in JSON format (for example: `{"name": "Alex", "email": "alex@example.com", "topic": "AI Trends 2025"}`) |

> 🚧 Mapping Identity and Object ID
>
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

4. Click **Continue**. Click **Test Step** to test the zap after mapping the files.
5. Click **Publish**. Also, publish the campaign you have created in [Configure CleverTap Campaign](doc:pro-forms#configure-clevertap-campaign). Each submission will now be logged as an event in CleverTap.

<Image alt="Verify Event Tracking in CleverTap" align="center" width="75% " border={true} src="https://files.readme.io/199d02e55f52aadadebfdc8c1d6721d73ad7a60ad94c41f13ee6bab98b56bbc7-7542bfb1-e958-47ca-b3ba-621fb586bd86.png">
  Verify Event Tracking in CleverTap
</Image>

# FAQs

### Can I use both profile updates and events together?

Yes. You can set up multiple Zaps, one for updating user profiles and another for uploading events. This way, you can both enrich CleverTap profiles with attributes and log submissions for analytics and campaign triggers.
