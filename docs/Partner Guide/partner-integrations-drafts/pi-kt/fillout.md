---
title: Fillout
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

[Fillout](https://www.fillout.com/) is a flexible form builder that allows marketers and product teams to create surveys, feedback forms, and onboarding experiences with dynamic personalization. Integrating Fillout with CleverTap via Zapier enables you to collect structured data from users directly within CleverTap in-app campaigns and automatically sync responses back to CleverTap for segmentation, personalization, and follow-up actions.

Integrating Fillout with CleverTap via Zapier allows you to:

* **Collect Structured User Input Seamlessly**: Capture data such as feedback, preferences, or onboarding details directly in CleverTap campaigns.
* **Personalize Forms Dynamically**: Pass CleverTap user properties (e.g., name, email) into Fillout forms as dynamic parameters.
* **Sync Responses Automatically**: Use Zapier to route Fillout form submissions into CleverTap as events or profile updates.
* **Enable Data-Driven Journeys**: Trigger contextual campaigns based on form submissions.

# Prerequisites for Integration

Before integrating Fillout with CleverTap via Zapier, ensure the following:

* Access to your **Fillout** account
* Access to an active **Zapier** account
* A CleverTap account with a valid **Account ID** and **Passcode**.

# Integrate Fillout with CleverTap Using Zapier

The integration involves the following four major steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:fillout#create-a-passcode-on-the-clevertap-dashboard)
2. [Create a Form in Fillout](doc:fillout#create-a-form-in-fillout)
3. [Configure CleverTap Campaign](doc:fillout#configure-clevertap-campaign)
4. [Connect Fillout and CleverTap via Zapier](doc:fillout#connect-fillout-and-clevertap-via-zapier)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create a Form in Fillout

Consider an example where you want to capture user feedback or preferences through a Fillout form embedded in a CleverTap in-app campaign. To do so, perform the following steps:

1. Log in to your Fillout dashboard and click **Create Form** to start from scratch or use a *Template*.

<Image alt="Create and Configure a Form in Fillout" align="center" width="65% " border={true} src="https://files.readme.io/3be325758be7f3b3a46b1f3bdf046fac834132b335434b926b61aadf63ae2740-image.png">
  Create and Configure a Form in Fillout
</Image>

2. Customize your form questions based on your use case (for example, feedback, survey, or onboarding).
3. In the *Settings* tab, open *URL Parameters* and add dynamic parameters such as `name` and `email` to pass CleverTap profile data.

<Image alt="Set up URL Parameters" align="center" width="65% " border={true} src="https://files.readme.io/2ef1860eb23cad8c35222bd8c052b31759ca486315b16f01a53c2ddbcd9d9b5c-image.png">
  Set up URL Parameters
</Image>

4. Click **Publish** to make your form live.

<Image alt="Publish Form" align="center" width="65% " border={true} src="https://files.readme.io/4ca7dc750453d227acc71a1fc2aa2f33c23944f1f36177a8d8ae8a8e13050f68-image.png">
  Publish Form
</Image>

5. Go to the *Share* tab > *Embed Form*, select *Embed type* as  *Standard*, click on **\</>Get the code**, to copy the embed code.

<Image alt="Copy Embed Code" align="center" width="65% " border={true} src="https://files.readme.io/438f6842f4c90db0bec692d88f70dae6d183952a0bec133784fd553c52d19879-image.png">
  Copy Embed Code
</Image>

> 📘 Note:
>
> To pass custom URL parameters in the embed, add `data-[parameter]` attributes to the code snippet (for example, `data-email="xxx"`).

## Configure CleverTap Campaign

You can embed a Fillout form into a CleverTap campaign to collect responses directly through in-app notifications, emails, or web popups. In this use case, we'll configure a CleverTap in-app campaign. To do so, follow these steps:

1. In the CleverTap dashboard, create a new [In-App Message](doc:create-message-in-app) campaign (you can also use [Email](doc:create-message-email) or [Web Popups](doc:create-message-web-popup) that support HTML).
2. In the *What* section, select a **Custom HTML Template** such as *Interstitial*.
3. Replace the existing code with the HTML snippet copied from *Step 5* of [Create a Form in Fillout](doc:fillout#create-a-form-in-fillout).

<Image alt="Embed Fillout Form in CleverTap Campaign" align="center" width="65% " border={true} src="https://files.readme.io/95713037d15f7a806a3e66e16897b060d3685f5bd23b1137dfaccf49f0d150d9-image.png">
  Embed Fillout Form in CleverTap Campaign
</Image>

4. Configure the remaining campaign parameters (target audience, display rules, and so on) as needed.
5. Publish the campaign only after configuring the Zap as [Create/Update User Profiles](doc:fillout#createupdate-user-profiles) or [Upload Event](doc:fillout#upload-event).

## Connect Fillout and CleverTap via Zapier

Zapier acts as a bridge between Fillout Form and CleverTap. When a user submits a response, Zapier captures it and sends the data to CleverTap in real time. You can either update user profiles or log submissions as events.

The integration supports two use cases:

* [Create/Update User Profiles](doc:fillout#createupdate-user-profiles)
* [Upload Event](doc:fillout#upload-event)

### Create/Update User Profiles

Use this option if you want Fillout responses to update user profiles in CleverTap for personalization and segmentation. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**. Zapier can connect various applications, including Fillout.

<Image alt="Create a Zap on Zapier Dashboard" align="center" width="75% " border={true} src="https://files.readme.io/830b60a9c8f926bca524bfae5fa8a9aa021dad3d7e712f438b95c0486994e000-image.png">
  Create a Zap on Zapier Dashboard
</Image>

2. **Set up a Trigger**. To do so, perform the following steps:
   1. Select *Fillout Form* in the App section. This starts the Zap when a trigger event occurs on the Fillout form.
   2. Select *Trigger Event* from the dropdown list and then select *New Submission* for this use case.
   3. Select Account and sign in using your Fillout account credentials.

<Image alt="Set Up Trigger Event" align="center" width="75% " border={true} src="https://files.readme.io/5842f5f60cd2794d00752952febcfe700e11eebcd0dd9a4765b5bb44b6be430e-2025-11-09_17-41-57_1.gif">
  Set Up Trigger Event
</Image>

3. Click **Test Trigger**. This ensures that the correct account is connected and the trigger is set up correctly.\
   After testing the trigger, you will see a sample of the most recent responses to the form.

<Image alt="Details of Pulled Records" align="center" width="65% " border={true} src="https://files.readme.io/d7a353ac9804ed2687967dee1abb4fba2796ca74c0859afb98e47592d4cbd7ea-image.png">
  Details of Pulled Records
</Image>

4. Click **Continue with selected record**.
5. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:
   1. Select *CleverTap* from the *App* dropdown.
   2. Select *Create/Update User Profile* from the Action event dropdown. This implies that whenever a new response is generated, a new user profile is created, or an existing user profile is updated with the new information.
   3. Select *Account* to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:fillout#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

<Image alt="Select the Action for Zap" align="center" width="75% " border={true} src="https://files.readme.io/02b2ee93834c3070e98a67596b7ae15c25a8f33ca5869cb2eefdab8142c38bcd-2025-11-09_17-45-54_1.gif">
  Select the Action for Zap
</Image>

6. **Configure the Action**. Map Fillout data fields to CleverTap fields as follows:

| CleverTap Field    | Fillout Field                                                                                                    |
| ------------------ | ---------------------------------------------------------------------------------------------------------------- |
| User ID            | Fillout user ID, email, or unique identifier.                                                                    |
| Object ID          | Unique identifier for the user.                                                                                  |
| Creation Date      | Date of the user’s creation in Fillout.                                                                          |
| Profile Properties | Responses in JSON format (for example: `{"name": "Alex", "email": "alex@example.com", "interests": "Webinars"}`) |

> 🚧 Mapping Identity and Object ID
>
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

7. Click **Continue**, and click **Test Step** to test the Zap after mapping the fields.

<Image alt="Test Zap" align="center" width="75% " border={true} src="https://files.readme.io/577d4059c2ab5d94ca101e57af0a211d283959fcc408efefc45c7170276d69f3-image.png">
  Test Zap
</Image>

8. Click **Publish**. Also, publish the campaign you have created in [Configure CleverTap Campaign](doc:fillout#configure-clevertap-campaign). After this, users will receive the form you have created, and the responses will be reflected in your CleverTap dashboard. If the user doesn’t exist, a new user will be created.

<Image alt="Verify on the CleverTap dashboard" align="center" width="65% " border={true} src="https://files.readme.io/67c7784504dd0c845351a6098feff92380ee9cc3d818a6f441254b417224061e-image.png">
  Verify on the CleverTap dashboard
</Image>

### Upload Event

Consider an example where you want to track form submissions as events in CleverTap instead of updating user profiles. This automation ensures that every submission is logged for analytics and segmentation.

1. Follow *Step 1* to *Step 4* from [Create/Update User Profiles](doc:fillout#createupdate-user-profiles) to configure Fillout as the trigger.
2. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:

   1. Select *CleverTap* from the *App* dropdown.
   2. Select *Upload Event* from the Action event dropdown.
   3. Select *Account* to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:fillout#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

<Image alt="Select the Action for Zap" align="center" border={true} src="https://files.readme.io/3942272058be57f6d086d539bc57c34eba36276df4852526e92089cd52fae58c-image.png">
  Select the Action for Zap
</Image>

3. **Configure the Action**. Map Fillout data fields to CleverTap fields as follows:

| CleverTap Field  | Fillout Field                                                                                              |
| ---------------- | ---------------------------------------------------------------------------------------------------------- |
| User ID          | Fillout user ID, email, or unique identifier                                                               |
| Object ID        | Leave blank if User ID is provided                                                                         |
| Creation Date    | Date of the user’s creation in Fillout.                                                                    |
| Event Name       | Select a descriptive event name (for example: `Feedback Submitted`, `Form Completed`)                      |
| Event Properties | Metadata in JSON format (for example: `{"rating": 5, "comment": "Great service!", "delivery": "On Time"}`) |

> 🚧 Mapping Identity and Object ID
>
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

4. Click **Continue**. Click **Test Step** to test the Zap after mapping the fields.
5. Click **Publish**. Also, publish the campaign you have created in [Configure CleverTap Campaign](doc:fillout#configure-clevertap-campaign). Each submission will now be logged as an event in CleverTap.

Once the campaign is published, the user will be shown the form as shown in the image below for the In-App campaign, and their responses will be reflected in the CleverTap dashboard.

<Image alt="In-App Message" align="center" width="25% " border={true} src="https://files.readme.io/30b1c847706b02eca7b600f547a5627f6f24b5f8f0f2f699bbcb765c926481c5-7e389343-4e60-4ac5-920d-aae5919446c5.png">
  In-App Message
</Image>

# FAQs

### Can I pass multiple parameters dynamically?

Yes. Fillout supports multiple `data-[parameter]` attributes. For example:

```html
data-name="{{ Profile.name }}" data-email="{{ Profile.Email }}" data-phone="{{ Profile.Phone }}"
```

These parameters will automatically populate when the CleverTap campaign is delivered.
