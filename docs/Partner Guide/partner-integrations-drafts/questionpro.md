---
title: QuestionPro
excerpt: Dynamic Content
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

[QuestionPro](https://www.questionpro.com/) is a leading online survey and research platform that helps businesses collect actionable feedback across web, mobile, and email channels.

Integrating CleverTap with QuestionPro allows you to:

* Embed personalized surveys within CleverTap email or In-App campaigns.
* Pass CleverTap user attributes to QuestionPro to customize survey links.
* Collect and analyze responses in QuestionPro to enhance marketing and product strategies.

This integration helps you close the feedback loop by capturing customer sentiment in context. For example, you can trigger a survey after a user completes a purchase or interacts with a new feature.

# Use Case

Trigger a QuestionPro feedback survey two days after a user's first purchase to measure satisfaction and gather product insights.

# Prerequisites for Integration

The following are the prerequisites for QuestionPro:

* A valid **QuestionPro** account with survey creation and distribution access.
* Ensure you have a **CleverTap** account.

> 🚧 Support for Integration
>
> This integration is managed and continuously improved by QuestionPro. The CleverTap and QuestionPro integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [QuestionPro](https://www.questionpro.com/help/) for support and resolution.

## Integrate QuestionPro with CleverTap

You can use CleverTap campaigns to distribute QuestionPro surveys through supported messaging channels, such as Email or In-App Messages. Follow these two major steps:

1. [Create Survey in QuestionPro](doc:questionpro#create-survey-in-questionpro)
2. [Configure CleverTap Campaign with Survey Link](doc:questionpro#configure-clevertap-campaign-with-survey-link)

## Create Survey in QuestionPro

Start by creating a survey in QuestionPro that you’ll later embed in a CleverTap campaign. To do so, follow these steps:

1. Log in to your **QuestionPro** account.
2. Click **+ New Survey** and either start from a blank template or select from the available templates. For more information, refer to [QuestionPro Create a Survey](https://www.questionpro.com/help/create-survey.html) .

<Image align="center" alt="Create New Survey" border={true} caption="Create New Survey" src="https://files.readme.io/a03cdc38887da4192c137264f9de0b21ed9534f4b5c2b56ff45ae123b5d97dcc-image.png" width="65% " />

3. Add your desired question types, such as NPS, CSAT, or multiple-choice.
4. When ready, locate the **Survey URL** in the top-right corner of your dashboard.

<Image align="center" alt="Survey URL in QuestionPro" border={true} caption="Survey URL in QuestionPro" src="https://files.readme.io/f22e4d33ce04703c19acce592be2e9050b2f02dabaddd32e23d889f9d541da28-image.png" width="65% " />

5. Copy the **Survey URL**. You’ll use it to distribute your survey via CleverTap campaigns.

Add custom variables (such as, `Name`, `Email`) to personalize survey links and track individual responses. For details, refer to [QuestionPro Custom Variables Guide](https://www.questionpro.com/help/).

## Configure CleverTap Campaign with Survey Link

The [QuestionPro survey](doc:questionpro#create-a-survey-in-questionpro) can be used in any CleverTap messaging channel that supports HTML or image URLs. While this guide includes an example for an email campaign, you can also use QuestionPro content in [Push Notification](doc:create-message-push), [In-App campaigns](doc:create-message-in-app), and other CleverTap messaging channels that support dynamic visuals.

To integrate a QuestionPro survey into your CleverTap Email campaign, perform the following steps:

1. Go to the _Campaigns_ page, click **+ Campaign**, and select _Email_ from the list of messaging channels.
2. Click **Go to Editor** under the _What_ section.
   1. Select a _Basic Template_ or _Saved Template_.
   2. Switch to **Source** mode in the email editor to edit the HTML code of the email body.
3. Paste the HTML Snippet copied in _step 5_ of [Create a Survey in QuestionPro](doc:questionpro#create-a-survey-in-questionpro) inside the `<body>` tag.

<Image align="center" alt="Insert the HTML Code Snippet" border={true} caption="Insert the HTML Code Snippet" src="https://files.readme.io/82a52d9f81856a7df6178eae5e9d585735b7aef4410cd90c67a1250f316d9bc3-2025-05-11_21-52-41_1.gif" width="75% " />

4. If you have defined any custom variables while creating the survey in QuestionPro, append those variables to the survey URL. For example:

```html
SURVEY_URL?Name=
```

Use [CleverTap Liquid Tags](doc:personalize-message-all#liquid-tags) to dynamically populate values for the custom variables. Always set a default value to ensure a fallback is displayed when the data is unavailable. For example:

```html
SURVEY_URL?Name={{ Profile.name | default: 'Human' }}
```

If no custom variables are defined, you can directly paste the survey link into the URL placeholder.

5. Send a test email to verify personalization and ensure the QuestionPro integration functions correctly.

<Image align="center" alt="Send a test email" border={true} caption="Send Test Email" src="https://files.readme.io/843f0d45b3fe5e33f3591b663bdd9fcf2b03d458566a7a322e3a791d534c2330-image.png" width="65% " />

6. Publish the email campaign once verification is complete. Users will receive personalized emails based on the configured Liquid Tags and settings.

Using CleverTap Liquid Tags with QuestionPro survey links enables personalized survey distribution across campaigns. For more information, refer to [CleverTap Liquid Tags](doc:personalize-message-all#liquid-tags).

## Best Practices

Follow these recommendations for an optimal integration experience:

* Keep surveys short (3–5 questions) to improve completion rates.
* Use personalization tags to make questions contextually relevant.
* Test survey links in preview mode before publishing campaigns.
* Monitor responses in QuestionPro’s analytics dashboard to measure engagement and satisfaction.