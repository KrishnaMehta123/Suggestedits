---
title: Yay! Forms
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

[Yay! Forms](https://yayforms.com/) is a user-friendly online form builder that enables businesses to create customizable forms without writing code. With features like conditional logic, hidden fields, and Zapier integrations, Yay! Forms makes it easy to collect user responses and feed them into your marketing workflows.

Integrating Yay! Forms with CleverTap via Zapier enables you to:

* **Collect Responses Seamlessly**: Embed forms inside CleverTap campaigns (In-App Messages, Emails, or Web Popups) and capture user data in real time.
* **Personalize Campaigns**: Pass identifiers such as email or identity through hidden fields or URL parameters for accurate response mapping.
* **Trigger Automated Workflows**: Forward responses as CleverTap events or update user profiles to segment users and deliver personalized follow-up campaigns.

# Prerequisites for Integration

Before integrating Yay! Forms with CleverTap via Zapier, ensure the following:

* Access to your **Yay! Forms** account
* Access to an active **Zapier** account
* A CleverTap account with a valid **Account ID** and **Passcode**.

# Integrate Yay! Forms with CleverTap Using Zapier

The integration involves the following four major steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:yay-forms#create-a-passcode-on-the-clevertap-dashboard)
2. [Create Form in Yay! Forms](doc:yay-forms#create-form-in-yay-forms)
3. [Configure CleverTap Campaign](doc:yay-forms#configure-clevertap-campaign)
4. [Connect Yay! Forms and CleverTap via Zapier](doc:yay-forms#connect-yay-forms-and-clevertap-via-zapier)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create Form in Yay! Forms

Create a survey form that captures user inputs like contact details, feedback, or preferences. To do so, perform the following steps:

1. Go to the Yay! Forms, dashboard and create a survey. For this example, create a simple rating form and save it.
2. Once the form is ready, go to the **Share** tab. Under **Hidden Fields**, add parameters you want to capture (for example, `email`).

<Image alt="Create survey" align="center" width="65% " border={true} src="https://files.readme.io/0eb6c8ec1307085f9f7e774b45e7f8260d70d52537b163339bc9c13c6b380605-f07bc68a-915e-4304-9efa-a10630bd008c.png">
  Create Survey
</Image>

3. Copy *HTML code* snippet to configure it in the CleverTap campaign.

## Configure CleverTap Campaign

Configure a CleverTap campaign to display your survey. This allows users to submit responses without leaving the app. To do so, perform the following steps:

1. In the CleverTap dashboard, create a new [In-App Message](doc:create-message-in-app) campaign (you can also use [Email](doc:create-message-email) or [Web Popups](doc:create-message-web-popup) that support HTML).
2. In the *What* section, select a **Custom HTML Template** such as *Interstitial* template.

<Image alt="Custom HTML Templates" align="center" width="75% " border={true} src="https://files.readme.io/bba3ad2b5f24447d2d31901ac4b17efe32de2cadc35424f7d8ad323841e5869f-image.png">
  Custom HTML Templates
</Image>

3. Replace the existing code inside the *Custom HTML* section and paste the HTML snippet copied from *Step 3* of [Create Form in Yay! Forms](doc:yay-forms#create-form-in-yay-forms).
4. Assigned the value of parameter `email` as `{{ Profile.Email | default: "[test@gmail.com](mailto:test@gmail.com)" }}`. For example:

```html
<iframe 
 src="https://yayforms.link/9KoVjV4?email={{ Profile.Email | default: "test@gmail.com" }}" 
 width="100%" 
 height="600" 
 frameborder="0">
</iframe>
```

4. Click **Preview and Test** to verify that the form renders correctly.

<Image align="center" className="border" width="75% " border={true} src="https://files.readme.io/e99a5c6e7f02011691b5238b8bc1103d5d261de1e8d817a7c2f0b2bcc5921ee0-image.png" />

5. Publish the campaign only after configuring the Zap as [Create/Update User Profiles](doc:yay-forms#createupdate-user-profiles) or [Upload Event](doc:yay-forms#upload-event).

## Connect Yay! Forms and CleverTap via Zapier

Zapier acts as the automation bridge between Yay! Forms and CleverTap. Whenever a user submits a Survey response, Zapier captures the submission and forwards the data to CleverTap in real time. This allows you to:

* **Enrich or create user profiles** in CleverTap with the submitted attributes, or
* **Track each submission as an event** for segmentation, analytics, and automated engagement campaigns.

The integration supports two options depending on your use case:

* [Create/Update User Profiles](doc:yay-forms#createupdate-user-profiles)
* [Upload Event](doc:yay-forms#upload-event)

### Create/Update User Profiles

Consider an example where you want to automatically sync details captured in Yay! Forms with CleverTap to drive personalized engagement. This ensures that each new submission updates the user’s profile in CleverTap in real time. To do so, perform the following steps:

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**. Zapier can connect different applications, such as Yay! Forms.

<Image alt="Create a Zap on Zapier Dashboard" align="center" width="75% " border={true} src="https://files.readme.io/830b60a9c8f926bca524bfae5fa8a9aa021dad3d7e712f438b95c0486994e000-image.png">
  Create a Zap on Zapier Dashboard
</Image>

2. **Set up a Trigger**. To do so, perform the following steps:
   1. Select Yay! Forms from the App section. This starts the Zap when a trigger event occurs on Yay! Forms.
   2. Select *Trigger Event* from the dropdown list and then select *New Response* for this use case.
   3. Select Account and sign in using your Yay! Forms account credentials.

<Image alt="Set Up Trigger Event" align="center" width="75% " border={true} src="https://files.readme.io/7ed73f7b9d1f2f8b4ffe81cc4d8cf11e4975f5f7868638f127687b4a6cc34edb-2025-09-07_02-49-50_1.gif">
  Set Up Trigger Event
</Image>

3. Click **Test Trigger**. This ensures that the correct account is connected and the trigger is set up correctly.\
   After testing the trigger, you will see a sample of the most recent responses to the form.

<Image alt="Details of Pulled Records" align="center" width="50% " border={true} src="https://files.readme.io/970962d65cfbf45812e450bbe826cc944ba688b230502ab7576bc7eff51f3a91-14fd61e6-427e-4537-afa3-0bb0bc4a5811.png">
  Details of Pulled Records
</Image>

4. Click **Continue with selected record**.
5. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:
   1. Select *CleverTap* from the *App* dropdown.
   2. Select *Create/Update User Profile* from the Action event dropdown. This implies that whenever a new response is generated, a new user profile is created, or an existing user profile is updated with the new information.
   3. Select *Account* to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:yay-forms#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

<Image alt="Select the Action for Zap" align="center" width="75% " border={true} src="https://files.readme.io/dbaf9bcddeb7c69667c29b473dca07d5de3423053643231f54334958120ed03e-2025-09-07_02-59-41_1.gif">
  Select the Action for Zap
</Image>

6. **Configure the Action**. Map Yay! Forms data fields to CleverTap fields as follows:

| CleverTap Field    | Yay! Forms Field                                                                                          |
| ------------------ | --------------------------------------------------------------------------------------------------------- |
| Identity           | Email or unique identifier from hidden fields                                                             |
| Object ID          | Leave blank if Identity is provided                                                                       |
| Creation Date      | Submission timestamp                                                                                      |
| Profile Properties | Form responses in JSON format (for example: `{"name": "Alex", "email": "alex@example.com", "rating": 5}`) |

> 🚧 Mapping Identity and Object ID
>
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

7. Click **Continue**, and click **Test Step** to test the zap after mapping the files.

<Image alt="Test Zap" align="center" width="75% " border={true} src="https://files.readme.io/577d4059c2ab5d94ca101e57af0a211d283959fcc408efefc45c7170276d69f3-image.png">
  Test Zap
</Image>

8. Click **Publish**. Also, publish the campaign you have created in [Configure CleverTap Campaign](doc:yay-forms#configure-clevertap-campaign). After this, users will receive an In-App message campaign as shown below, and the responses will be sent back to CleverTap via Zapier.

<Image alt="In-app message" align="center" width="25% " border={true} src="https://files.readme.io/79603fe7c956e3ee9802cd0adacc84ed7d048a717063199d7a9fd4c4812192ab-12756bd1-6c5b-4c53-bc18-7618dc8f1900.png">
  In-App Message
</Image>

### Upload Event

Consider an example where you want to track survey submissions as events in CleverTap instead of updating user profiles. This automation ensures that every submission is logged for analytics and segmentation.

1. Follow *Step 1* to *Step 4* from [Create/Update User Profiles](doc:surveynoodle#createupdate-user-profiles) to configure Yay! Forms as the trigger.
2. **Select the Action** that the zap must perform after the trigger event occurs. To do so, perform the following steps:

   1. Select *CleverTap* from the *App* dropdown.
   2. Select *Upload Event* from the Action event dropdown.
   3. Select *Account* to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:yay-forms#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

<Image alt="Select the Action for Zap" align="center" width="75% " border={true} src="https://files.readme.io/9f6f3a486286dfa35e969e2a3e9efe5a765eb415cfc94187dd6acccbf74c5193-2025-09-07_02-59-41_1.gif">
  Select the Action for Zap
</Image>

3. **Configure the Action**. Map Yay! Forms data fields to CleverTap fields as follows:

| CleverTap Field  | Yay! Forms Field                                                                             |
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
5. Click **Publish**. Also, publish the campaign you have created in [Configure CleverTap Campaign](doc:yay-forms#configure-clevertap-campaign). Each submission will now be logged as an event in CleverTap.

# FAQs

### Can I update profiles instead of uploading events?

Yes. Depending on your use case, you can select either **Create/Update User Profile** or **Upload Event** as the action in Zapier. This gives you the flexibility to update CleverTap user attributes or log submissions as events.
