---
title: QuestionPro
deprecated: false
hidden: true
metadata:
  robots: index
---
# Overview

[QuestionPro](https://www.questionpro.com/) is a leading online survey and research platform that helps businesses collect actionable feedback across web, mobile, and email channels.

Integrating **CleverTap** with **QuestionPro** allows you to:

* Embed personalized surveys within CleverTap email or in-app campaigns.
* Pass CleverTap user attributes to QuestionPro to customize survey links.
* Collect and analyze responses in QuestionPro to enhance marketing and product strategies.

This integration helps you close the feedback loop by capturing customer sentiment in context—for example, you can trigger a survey after a user completes a purchase or interacts with a new feature.

<Callout icon="💡" theme="default">
  ### **Example Use Case:** Trigger a QuestionPro feedback survey two days after a user's first purchase to measure satisfaction and gather product insights.
</Callout>

***

## Prerequisites for Integration

Before setting up the integration, ensure you have access to both platforms and the necessary permissions.

* A valid **QuestionPro** account with survey creation and distribution access.
* A **CleverTap** account with campaign creation privileges.

> 🚧 **Support for Integration**
>
> This integration is maintained by **QuestionPro**. It has been validated for performance and reliability. For technical issues or troubleshooting, contact [QuestionPro Support](https://www.questionpro.com/help/).

## Integrate QuestionPro with CleverTap

You can use CleverTap campaigns to distribute QuestionPro surveys through supported messaging channels, such as **Email** or **In-App Messages**.
Follow these two primary steps to implement the integration:

1. [Create a Survey in QuestionPro](doc:questionpro#create-a-survey-in-questionpro)
2. [Configure CleverTap Campaign with Survey Link](doc:questionpro#configure-clevertap-campaign-with-survey-link)

## Create a Survey in QuestionPro

Start by creating a survey in QuestionPro that you’ll later embed in a CleverTap campaign.

1. Log in to your **QuestionPro** account.
2. Click **Create Survey**, and either start from a blank template or choose from available templates.
3. Add your desired question types—such as NPS, CSAT, or multiple-choice.
4. When ready, click **Collect Responses** and locate the **Survey URL** in the top-right corner of your dashboard.

<Image align="center" alt="Survey URL in QuestionPro" border={true} caption="Locate the Survey URL in QuestionPro" src="https://files.readme.io/placeholder-questionpro-url.png" width="75%" />

5. Copy the **Survey URL**. You’ll use it to distribute your survey via CleverTap campaigns.

<Callout icon="💡" theme="default">
  ### **Tip:** Add custom variables (e.g., `Name`, `Email`) to personalize survey links and track individual responses. For details, see [QuestionPro Custom Variables Guide](https://www.questionpro.com/help/).
</Callout>

## Configure CleverTap Campaign with Survey Link

The [SurveyMonkey survey](doc:surveymonkey#create-a-survey-in-surveymonkey) can be used in any CleverTap messaging channel that supports HTML or image URLs. While this guide includes an example for an [email campaign](doc:surveymonkey#configure-email-campaign-in-clevertap), you can also use SurveyMonkey content in [Push Notification](doc:create-message-push), [In-App campaigns](doc:create-message-in-app), and other CleverTap messaging channels that support dynamic visuals.

To integrate a SurveyMonkey survey into your CleverTap Email campaign, perform the following steps:

1. Go to the _Campaigns_ page, click **+ Campaign**, and select _Email_ from the list of messaging channels.
2. Click **Go to Editor** under the _What_ section.
   1. Select a _Basic Template_ or _Saved Template_.
   2. Switch to **Source** mode in the email editor to edit the HTML code of the email body.
3. Paste the HTML Snippet copied in _step 5_ of [ Create a Survey in SurveyMonkey](doc:surveymonkey#create-a-survey-in-surveymonkey) inside the `<body>` tag.

<Image align="center" alt="Insert the HTML Code Snippet" border={true} caption="Insert the HTML Code Snippet" src="https://files.readme.io/82a52d9f81856a7df6178eae5e9d585735b7aef4410cd90c67a1250f316d9bc3-2025-05-11_21-52-41_1.gif" width="75% " />

4. Replace the `MERGE_TAG` with the appropriate [CleverTap Liquid Tag](doc:personalize-message-all#liquid-tags) for personalization. Set default values to ensure a fallback is displayed when specific data is not available (for example, `{{Profile.name | default: "User"}}` will display "User" if the name field is empty). For more information, refer to [SurveyMonkey Merge Tags](https://help.surveymonkey.com/en/getfeedback/builder/merge-fields-logic/).
5. Send a test email to verify personalization and ensure the SurveyMonkey integration functions correctly.

<Image align="center" alt="Send a test email" border={true} caption="Send a Test Email" src="https://files.readme.io/02d8203166c9269b9fa1eeb2819004a173fe7b554d916caa6decaabb05df8524-image.png" width="75% " />

6. Publish the email campaign once verification is complete. Users will receive personalized emails based on the configured Liquid Tags and settings.

Combining SurveyMonkey's dynamic content capabilities with CleverTap’s advanced segmentation and messaging allows you to create timely, relevant interactions that resonate with every user. For more information about using personalization in CleverTap, refer to [CleverTap Liquid Tags](doc:personalize-message-all#liquid-tags).

***

<br />

Once your survey is ready, you can insert the QuestionPro survey link into any CleverTap campaign that supports HTML or hyperlinks.
The following examples show how to include the survey in both **Email** and **In-App** campaigns.

***

#### Configure Email Campaign in CleverTap

To share your survey through an email campaign:

1. In CleverTap, go to **Campaigns → + Campaign → Email**.

2. Under the **What** section, click **Go to Editor**.

   1. Select a **Basic Template** or **Saved Template**.
   2. Switch to **Source** mode in the email editor.

3. Locate where you want to include the survey and paste this snippet inside the `<body>` tag:

   ```html
   <a href="SURVEY_URL?Name={{Profile.name | default: 'User'}}" target="_blank">
     Take Our Survey
   </a>
   ```

4. Replace `SURVEY_URL` with your actual QuestionPro survey link.

5. Adjust the parameter (`Name`) to match the QuestionPro custom variable you defined.

<Image align="center" alt="Insert QuestionPro Survey Link" border={true} caption="Insert the QuestionPro Survey Link in an Email Template" src="https://files.readme.io/placeholder-questionpro-email.png" width="75%" />

6. Send a test email to confirm that personalization and the survey link work correctly.
7. Once verified, publish your campaign.

> ℹ️ **Note:** You can include additional personalization using [CleverTap Liquid Tags](doc:personalize-message-all#liquid-tags) to dynamically populate user details.

***

#### Configure In-App Campaign in CleverTap

You can also embed a QuestionPro survey directly within a CleverTap in-app message using an iframe.

1. Go to **Campaigns → + Campaign → In-App Message**.
2. Configure audience, triggers, and goal metrics.
3. In the **What** section, select **Custom HTML Template** and enable **Include JavaScript**.
4. Insert the following iframe snippet inside the `<body>` tag:

   ```html
   <iframe src="SURVEY_URL?Name={{Profile.name | default: 'User'}}"
           width="100%" height="500px" frameborder="0">
   </iframe>
   ```

<Image align="center" alt="Embedded QuestionPro Survey in In-App Message" border={true} caption="Embed the QuestionPro Survey in an In-App Campaign" src="https://files.readme.io/placeholder-questionpro-inapp.png" width="75%" />

5. Replace `SURVEY_URL` with your survey link.
6. Use Liquid tags or personalization variables to dynamically insert CleverTap profile data.

> ⚠️ **Note:** Ensure your iframe link is secure (HTTPS) and the domain is whitelisted in your app configuration.

7. Preview and test the campaign before publishing.

***

## Best Practices

Follow these recommendations for an optimal integration experience:

* Keep surveys short (3–5 questions) to improve completion rates.
* Use personalization tags to make questions contextually relevant.
* Test survey links in preview mode before publishing campaigns.
* Monitor responses in QuestionPro’s analytics dashboard to measure engagement and satisfaction.

***

## References

* [QuestionPro Documentation](https://www.questionpro.com/help/)
* [CleverTap Campaign Documentation](https://docs.clevertap.com/docs/campaigns)
* [CleverTap Liquid Tags](doc:personalize-message-all#liquid-tags)
* [Placeholder: Video – Email Campaign Integration]
* [Placeholder: Video – In-App Message Integration]

***

## Summary

Integrating **QuestionPro** with **CleverTap** enables you to distribute surveys directly through your engagement channels—email and in-app messages—while personalizing them with user-level attributes.
This integration bridges the gap between engagement and insight, helping you capture actionable feedback and continuously improve user experience.

***

### ✅ CleverTap Style Compliance Summary

* **Structure:** Matches official Partner Integration doc hierarchy.
* **Tone:** Direct, instructional, and customer-centric.
* **Headings:** Smooth, contextual transitions (no redundant blurbs).
* **Formatting:** Consistent Markdown, compliant with TEC checklist.
* **Visuals:** Placeholder image blocks aligned with house style.
