---
title: SurveyNoodle
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

[SurveyNoodle](https://surveynoodle.com/) is an online survey creation and distribution platform that enables businesses to design, share, and collect responses from surveys across multiple channels. It offers an intuitive interface for building forms, quizzes, and polls without coding, along with powerful response analytics. With flexible embedding options, SurveyNoodle can be integrated into websites, apps, and third-party platforms, making it a versatile tool for gathering customer feedback, lead information, and market insights.

Integrating SurveyNoodle with CleverTap via Zapier enables you to:

* **Capture User Details Seamlessly**: Create surveys in SurveyNoodle and use them in CleverTap campaigns (In-App, Email, or Web Popups) to [create or update user profiles](doc:surveynoodle#createupdate-user-profiles).
* **Collect Feedback Directly in Campaigns**: Embed SurveyNoodle surveys inside CleverTap campaigns to capture user responses in real time.
* **Automate Data Sync**: Use Zapier to forward survey responses to CleverTap as user profile updates or as events for personalization and segmentation.

# Prerequisites for Integration

To integrate SurveyNoodle with CleverTap via Zapier, ensure the following:

* Access to your **SurveyNoodle** account
* Access to an active **Zapier** account
* A CleverTap account with a valid **Account ID** and **Passcode**.

# Integrate SurveyNoodle with CleverTap Using Zapier

The integration involves the following four major steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:surveynoodle#create-a-passcode-on-the-clevertap-dashboard)
2. [Create SurveyNoodle Form](doc:surveynoodle#create-surveynoodle-form)
3. [Configure CleverTap Campaign](doc:surveynoodle#configure-clevertap-campaign)
4. [Connect SurveyNoodle and CleverTap via Zapier](doc:surveynoodle#connect-surveynoodle-and-clevertap-via-zapier)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create SurveyNoodle Form

Create a survey form that captures user inputs like contact details, feedback, or preferences. To do so, perform the following steps:

1. Go to the SurveyNoodle dashboard and create a survey. For this example, create a simple survey form and save the survey.

<Image alt="Create survey" align="center" width="65% " border={true} src="https://files.readme.io/4ae8eb7b914179592ff92a6112c91371801077f74d8c1c3d78acc2d37a87d4ac-Screenshot_2025-08-13_at_2.07.53_PM-20250813-083756.png">
  Create Survey
</Image>

2. Go to *Embed Survey*. You will see an *HTML code* snippet.
3. Copy *HTML code* snippet to configure it in the CleverTap campaign.

<Image alt="Copy HTML Code" align="center" width="75% " border={true} src="https://files.readme.io/fd61c2a37d8404efe6858f0df2ae9e77a5f1603afa87301c3fb260b5ec4be71b-Screen_Recording_2025-08-13_at_2.10.00_PM_1.gif">
  Copy HTML Code
</Image>

## Configure CleverTap Campaign

Configure a CleverTap campaign to display your survey. This allows users to submit responses without leaving the app. To do so, perform the following steps:

1. In the CleverTap dashboard, create a new [In-App Message](doc:create-message-in-app) campaign (you can also use [Email](doc:create-message-email) or [Web Popups](doc:create-message-web-popup) that support HTML).
2. In the *What* section, select a **Custom HTML Template** such as *Interstitial*.

<Image alt="Custom HTML Templates" align="center" width="75% " border={true} src="https://files.readme.io/bba3ad2b5f24447d2d31901ac4b17efe32de2cadc35424f7d8ad323841e5869f-image.png">
  Custom HTML Templates
</Image>

3. Replace the existing code inside the *Custom HTML* section and paste the HTML snippet copied from *Step 3* of [Create SurveyNoodle Form](doc:surveynoodle#create-surveynoodle-form).

<Image alt="Preview and Test" align="center" width="65% " border={true} src="https://files.readme.io/8edaf48711f41f6b38bc14971da6b7647adf8d2a989950374bc9f7e5b86541e4-86e1e5d3-74ad-4352-b124-83d5ec5e9ac0.png">
  Preview and Test
</Image>

4. Click **Preview and Test** to verify that the form renders correctly.
5. Publish the campaign only after configuring the Zap as [Create/Update User Profiles](doc:surveynoodle#createupdate-user-profiles) or [Upload Event](doc:surveynoodle#upload-event).

## Connect SurveyNoodle and CleverTap via Zapier

Zapier acts as the automation bridge between SurveyNoodle and CleverTap. Whenever a user submits a Survey response, Zapier captures the submission and forwards the data to CleverTap in real time. This allows you to:

* **Enrich or create user profiles** in CleverTap with the submitted attributes, or
* **Track each submission as an event** for segmentation, analytics, and automated engagement campaigns.

The integration supports two options depending on your use case:

* [Create/Update User Profiles](doc:surveynoodle#createupdate-user-profiles)
* [Upload Event](doc:surveynoodle#upload-event)

### Create/Update User Profiles

Consider an example where you want to automatically sync details captured in SurveyNoodle with CleverTap to drive personalized engagement. This ensures that each new submission updates the user’s profile in CleverTap in real time. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**. Zapier can connect different applications, such as SurveyNoodle.

<Image alt="Create a Zap on Zapier Dashboard" align="center" width="75% " border={true} src="https://files.readme.io/830b60a9c8f926bca524bfae5fa8a9aa021dad3d7e712f438b95c0486994e000-image.png">
  Create a Zap on Zapier Dashboard
</Image>

2. **Set up a Trigger**. To do so, perform the following steps:
   1. Select SurveyNoodle from the App section. This starts the Zap when a trigger event occurs on SurveyNoodle.
   2. Select *Trigger Event* from the dropdown list and then select *New Survey Answer* for this use case.
   3. Select Account and sign in using your SurveyNoodle account credentials.

<Image alt="Set Up Trigger Event" align="center" width="75% " border={true} src="https://files.readme.io/acccdd8091bf5c40bf49b936964ad911de13f18d2c80f38f760f3bfd9667092e-2025-09-06_12-49-55_1.gif">
  Set Up Trigger Event
</Image>

3. Click **Test Trigger**. This ensures that the correct account is connected and the trigger is set up correctly.\
   After testing the trigger, you will see a sample of the most recent responses to the form.

<Image alt="Details of Pulled Records" align="center" width="50% " border={true} src="https://files.readme.io/d1d4a215289e1d42445488f4390086ae1fd035433e003ee98fdcaeb7a34e62c5-751096c9-2655-4b4c-bab4-0d3ac64f3930_1.png">
  Details of Pulled Records
</Image>

4. Click **Continue with selected record**.
5. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:
   1. Select *CleverTap* from the *App* dropdown.
   2. Select *Create/Update User Profile* from the Action event dropdown. This implies that whenever a new response is generated, a new user profile is created, or an existing user profile is updated with the new information.
   3. Select *Account* to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:surveynoodle#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

<Image alt="Select the Action for Zap" align="center" width="75% " border={true} src="https://files.readme.io/b62f0bd05ba38200bba2111412d5cf0cc417e5e9165ad24eaeff67f3dce6e264-2025-09-06_12-54-46_1.gif">
  Select the Action for Zap
</Image>

6. **Configure the Action**. Map SurveyNoodle data fields to CleverTap fields as follows:

| CleverTap Field    | SurveyNoodle Field                                                        |
| ------------------ | ------------------------------------------------------------------------- |
| Identity           | Email or unique user identifier                                           |
| Object ID          | Leave blank if Identity is provided                                       |
| Creation Date      | Submission date or timestamp                                              |
| Profile Properties | Form responses in JSON format (for example, name, email, campaign source) |

> 🚧 Mapping Identity and Object ID
>
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

7. Click **Continue**, and click **Test Step** to test the zap after mapping the files.

<Image alt="Test Zap" align="center" width="75% " border={true} src="https://files.readme.io/577d4059c2ab5d94ca101e57af0a211d283959fcc408efefc45c7170276d69f3-image.png">
  Test Zap
</Image>

8. Click **Publish**. Also, publish the campaign you have created in [Configure CleverTap Campaign](doc:surveynoodle#configure-clevertap-campaign). After this, users will receive an In-App message campaign as shown below, and the responses will be sent back to CleverTap via Zapier.

<Image alt="In-app message" align="center" width="25% " border={true} src="https://files.readme.io/81abacb22ee43cd05700cecd65d75260943b43fac52af16d3e5d220a4aa0dca7-9cd2108e-137c-4636-905b-6f711b27d9a1.png">
  In-App Message
</Image>

### Upload Event

Consider an example where you want to track survey submissions as events in CleverTap instead of updating user profiles. This automation ensures that every submission is logged for analytics and segmentation.

1. Follow *Step 1* to *Step 4* from [Create/Update User Profiles](doc:surveynoodle#createupdate-user-profiles) to configure SurveyNoodle as the trigger.
2. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:

   1. Select *CleverTap* from the *App* dropdown.
   2. Select *Upload Event* from the Action event dropdown.
   3. Select *Account* to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:surveynoodle#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

<Image alt="Select the Action for Zap" align="center" width="75% " border={true} src="https://files.readme.io/5e4a1918fb775baafbe76491e8b47b0aee9eb75c3c4cf048d7154836eb5031c5-2025-09-06_12-59-12_1.gif">
  Select the Action for Zap
</Image>

3. **Configure the Action**. Map SurveyNoodle data fields to CleverTap fields as follows:

| CleverTap Field  | SurveyNoodle Field                                                           |
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

<Image alt="Verify on the CleverTap dashboard" align="center" width="75% " border={true} src="https://files.readme.io/d5ad478c5b2945c7ba3196b8d1cf94a76ae5aca344b90bee1591a6a5107df1f8-99db3877-182b-4da3-9e3d-c0b7aa031fd2.png">
  Verify on the CleverTap dashboard
</Image>
