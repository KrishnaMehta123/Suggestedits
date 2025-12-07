---
title: Jotform
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

[Jotform](https://www.jotform.com/) is a versatile online form builder that helps businesses collect user data, leads, feedback, and documents. By integrating Jotform with CleverTap through Zapier, you can automate the flow of form submission data into CleverTap. This allows marketers to update user profiles, log events, and trigger personalized engagement campaigns in real time.

Integrating Jotform with CleverTap via Zapier enables you to:

- **Sync User Data Automatically**: Send Jotform submissions to CleverTap without manual intervention.
- **Update or Create Profiles Instantly**: Keep user information such as name, email, and preferences up to date.
- **Trigger Automated Campaigns**: Initiate CleverTap journeys based on form submissions or document signings.
- **Enhance Targeting and Personalization**: Enrich CleverTap profiles with form data for better segmentation.

# Prerequisites for Integration

The following are the prerequisites for this integration:

- Access to your **Jotform** account
- Access to an active **Zapier** account
- A CleverTap account with a valid **Account ID** and **Passcode**

# Integrate Jotform with CleverTap Using Zapier

The integration involves the following four major steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:jotform#create-a-passcode-on-the-clevertap-dashboard)
2. [Create a Form in Jotform](doc:jotform#create-a-form-in-jotform)
3. [Connect Jotform and CleverTap via Zapier](doc:jotform#connect-jotform-and-clevertap-via-zapier)
4. [Configure CleverTap Campaign (Optional)](doc:jotform#configure-clevertap-campaign-optional)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate API requests. Every CleverTap API call must include Account ID and Passcode as request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create a Form in Jotform

Consider an example where you want to capture onboarding details such as Name, Email, and Preferences using Jotform. To do so, perform the following steps:

1. Log in to your **Jotform dashboard**.
2. Click **+ Create Form** and select a form type such as _Start From Scratch_ or _Use Template_.
3. Customize your form fields as needed.
4. Click **Publish** to make the form live.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/190399e6cc6b7a01c2bf5927a8d51d2dc5773a9f3e14ed0976bd32a37c98f52d-Screen_Recording_2025-07-14_at_2.18.45_PM_1.gif",
        "",
        "Create a Form in Jotform"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Create a Form in Jotform"
    }
  ]
}
[/block]


## Connect Jotform and CleverTap via Zapier

Zapier acts as the automation bridge between Jotform and CleverTap. Whenever a user submits a form or signs a document, Zapier captures the submission and forwards it to CleverTap. This helps automate user management and campaign triggers.

### Create a Zap in Zapier

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**.
2. **Set up the Trigger:**

   1. Select _Jotform_ as the Trigger App.
   2. Select _New Submission_ as the Trigger Event.
   3. Connect your Jotform account and follow the on-screen instructions to authenticate.
   4. Select the form you wish to associate with this trigger.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4f6b2ccf174a3a0b5055c327c2232c899295ce7f99d21420433c42e8825d9ca3-2025-10-06_11-02-45_1.gif",
        "",
        "Set up the Jotform Trigger"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Set up the Jotform Trigger"
    }
  ]
}
[/block]


3. Click **Test Trigger**. This ensures that the correct account is connected and the trigger is set up correctly.  
   After testing the trigger, Zapier will fetch the most recent responses of the form.
4. **Set up the Action:**

   1. Select _CleverTap_ as the Action App.
   2. Select _Create/Update User Profile_ from the Action event dropdown.
   3. Select _Account_ to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:outgrow#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f0cf2f86c09089d9993dd29b8ca95ff5c2fff6f8e467dfccf3a2733f40ff5bca-2025-10-05_12-26-06_1.gif",
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


5. **Configure the Action**. Map Jotform data fields to CleverTap fields as follows:

| CleverTap Field    | Jotform Field                                                                                              |
| ------------------ | ---------------------------------------------------------------------------------------------------------- |
| Identity           | Jotform user ID, email, or any unique identifier                                                           |
| Object ID          | Unique identifier for the user.                                                                            |
| Creation Date      | Form submission timestamp                                                                                  |
| Profile Properties | Responses in JSON format (for example: `{"name": "Alex", "email": "alex@example.com", "role": "Manager"}`) |

> 🚧 Mapping Identity and Object ID
> 
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

4. Click **Continue**. Click **Test Step** to test the zap after mapping the files.
5. Click **Publish Zap** to activate the workflow.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/636844348adc7589790c52e54183e37b00157fdc1ab5d2ee1ea7a07c1252013e-image.png",
        null,
        "Verify User Profile in CleverTap"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Verify User Profile in CleverTap"
    }
  ]
}
[/block]


## Configure CleverTap Campaign (Optional)

You can also display your Jotform forms inside CleverTap **In-App** or **Web Popup** campaigns using Custom HTML templates.

To embed a Jotform form:

1. Copy your Jotform _form URL_ or _embed code_. This can be copied after creating and publishing the form from your Jotform dashboard. Refer to [Create a Form in Jotform](doc:jotform#create-a-form-in-jotform)
2. In the CleverTap dashboard, create a new [In-App Message](doc:create-message-in-app) campaign that supports HTML
3. In the _What_ section, select a **Custom HTML Template** such as _Blank Template_.
4. Replace the content with your Jotform embed code.

```html
<iframe
 src="https://form.jotform.com/251941814280456"
 width="100%"
 height="800"
 frameborder="0"
 style="border:none;"
 allowfullscreen>
</iframe>
```

5. Click **Preview and Test** to ensure the form renders correctly within the campaign.
6. Publish the campaign to display the form to users.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e7acef3170b249d289806b962ab5da4b411e8eb4864bb94ac219a1e6f939c7e5-image.png",
        null,
        "Embed Jotform in CleverTap Campaign"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Embed Jotform in CleverTap Campaign"
    }
  ]
}
[/block]


# FAQs

### Can I log form submissions as events instead of updating profiles?

Yes. Instead of selecting **Upload/Update User Profile**, choose **Upload Event** in the Zapier Action step. This will log each Jotform submission as an event in CleverTap (for example: `Form Submitted`, `Survey Completed`).

### Can I use Jotform responses to trigger CleverTap journeys?

Yes. Once Jotform data reaches CleverTap, you can use **Events** or **User Properties** as entry triggers in your CleverTap Journeys for targeted automation.