---
title: Webflow
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

[Webflow](https://webflow.com/) is a visual web design and development platform that allows you to build and host responsive websites with integrated forms for lead capture, signup, and contact submissions. Integrating Webflow with CleverTap via Zapier enables you to automatically send form submission data to CleverTap, helping you capture leads, create user profiles, and trigger personalized engagement flows in real time.

Integrating Webflow with CleverTap via Zapier allows you to:

- **Capture Leads Instantly**: Automatically sync Webflow form submissions into CleverTap.
- **Create or Update User Profiles**: Build real-time user records enriched with Webflow form data.
- **Trigger Campaigns Effortlessly**: Launch onboarding or engagement campaigns right after a user submits a form.
- **Streamline Lead Management**: Keep CleverTap data up to date without developer intervention.

# Prerequisites for Integration

Before integrating Webflow with CleverTap via Zapier, ensure the following:

- Access to your **Webflow** account with an active website
- Access to an active **Zapier** account
- A CleverTap account with a valid **Account ID** and **Passcode**

# Integrate Webflow with CleverTap Using Zapier

Suppose you use Webflow to collect leads or signups through embedded forms and want those submissions to appear instantly in CleverTap for segmentation or automated engagement.  

This integration connects Webflow, Zapier, and CleverTap, ensuring every form submission is automatically transferred to CleverTap, either as a user profile or an event enabling real-time onboarding, campaign triggers, and personalized communication.

The integration involves the following three major steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:webflow#create-a-passcode-on-the-clevertap-dashboard)
2. [Create or Configure a Form in Webflow](doc:webflow#create-or-configure-a-form-in-webflow)
3. [Connect Webflow and CleverTap via Zapier](doc:webflow#connect-webflow-and-clevertap-via-zapier)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API call must include Account ID and Passcode as request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create or Configure a Form in Webflow

Go to your [Webflow account](https://webflow.com/dashboard) and open the website project you’ve already created.  
For this example, you’ll add a **form field** to that website to capture user input such as name, email, or preferences.

To create or configure your form in Webflow, follow these steps:

1. Go to [Webflow dashboard](https://webflow.com/dashboard) and open your existing website project.
2. Add a [Form Block](https://university.webflow.com/videos/site-build-form) to the desired page if one doesn’t already exist.
3. Customize your form fields (for example, **Name**, **Email**, **Preferences**) based on your data collection needs.
4. Click **Publish** to make your changes live on your Webflow site.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a76f0ceba47e144bbc7c00b374d1108cc81f6331eb1c5e97d903a957696a42ab-image.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true
    }
  ]
}
[/block]


For more details on creating or configuring forms in Webflow, refer to [Webflow University’s Forms](https://university.webflow.com/?_gl=1*1pkq960*webflow_gcl_au*MTQzNzE3NDUxLjE3NjIyNDQxMDA.).

## Connect Webflow and CleverTap via Zapier

Zapier acts as the automation bridge between Webflow and CleverTap. Whenever a visitor submits a form on your Webflow website, Zapier captures the form data and sends it to CleverTap, where it can be used to update or create user profiles.

### Create a Zap in Zapier

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**.
2. **Set up the Trigger:**

   1. Select _Webflow_ as the Trigger App.
   2. Select _New Form Submission_ as the Trigger Event.
   3. Connect your Webflow account and authorize the workspace you want Zapier to access.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bc91be729402637e6d9c2187a31762105c721ad22ae6f0c4717b1e60ac13d7d8-2025-11-09_00-43-53_1.gif",
        "",
        "Set up the Webflow Trigger"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Set up the Webflow Trigger"
    }
  ]
}
[/block]


3. Select the site and form you wish to act as the trigger.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1e29ff916e3640544bbc457906ee4930f8069f5b55354f026cd1dc4f59354cd5-image.png",
        null,
        "Configure the Site"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Configure the Site"
    }
  ]
}
[/block]


4. Test the trigger to ensure Zapier can retrieve recent form submissions.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3ee79215c537ecb8dea3a9074b77a161359e25a4e71570b81d59c59f01bd2246-image.png",
        null,
        "Test Trigger"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Test Trigger"
    }
  ]
}
[/block]


5. Set up the Action:
   1. Select _CleverTap_ as the Action App.
   2. Select Create/Update User Profile from the Action event dropdown.
   3. Select _Account_ to connect the CleverTap account. The Zapier window opens. Enter all the required details to connect to the CleverTap account. Enter the same passcode you obtained during the [Create a Passcode on CleverTap Dashboard](doc:webflow#create-a-passcode-on-the-clevertap-dashboard) step.
   4. Click **Continue** after successfully connecting your account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/78c096c1a3e648a5708a00088c8ec828490e1682f2645e610571716560a18f8f-2025-11-09_00-51-06_1.gif",
        "",
        "Set up the CleverTap Action"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Set up the CleverTap Action"
    }
  ]
}
[/block]


6. Configure the Action. Map Webflow data fields to CleverTap fields as follows:

| CleverTap Field    | Webflow Field                                                                                                 |
| ------------------ | ------------------------------------------------------------------------------------------------------------- |
| Identity           | Webflow user ID, email, or any unique identifier                                                              |
| Object ID          | Leave blank if Identity is provided                                                                           |
| Creation Date      | Form submission timestamp                                                                                     |
| Profile Properties | Responses in JSON format (for example: `{"name": "Alex", "email": "alex@example.com", "role": "Subscriber"}`) |

> 🚧 Mapping Identity and Object ID
> 
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

7. Click **Continue**. Click **Test Step** to test the zap after mapping the files.
8. Click **Publish Zap** to activate the workflow.
9. Check your CleverTap dashboard to verify that a user profile has been created or updated.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ee4eb03b3d0e7bfa52bc8ca71b9d871a6951b4ae99b4714f44408b0bbb50b8af-image.png",
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


# FAQs

### Can I track Webflow form submissions as events instead of profiles?

Yes. Instead of choosing **Upload/Update User Profile**, select **Upload Event** in Zapier. This will log each form submission as an event in CleverTap (for example: `Form Submitted`, `Contact Request`, `Newsletter Signup`).

### Can I capture multiple forms from different Webflow sites?

Yes. You can create separate Zaps for each site or form in Webflow, connecting them to distinct CleverTap actions or events for precise tracking.