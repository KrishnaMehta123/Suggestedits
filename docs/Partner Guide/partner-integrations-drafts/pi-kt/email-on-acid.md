---
title: Email on Acid
excerpt: Email Template
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
> ❗️ Note:
> 
> **A credit card is required to test emails on the entire account.**
> 
> This partner functions more like an Email Service Provider (ESP) than just a template tool. Please confirm whether we should categorize them as an Email Template partner or an Email Service Provider partner.

# Overview

[Email on Acid](https://www.emailonacid.com/) is a platform for email testing, previewing, and optimizing campaigns across multiple clients and devices. With this integration, you can design and validate your emails in Email on Acid, then embed the approved HTML into CleverTap campaigns.

Integrating CleverTap with Email on Acid, you can:

- Import thoroughly tested and optimized email templates directly into CleverTap campaigns.
- Deliver emails that render consistently across popular clients and devices.
- Personalize campaigns using CleverTap’s Liquid tags on top of Email on Acid–validated templates.
- Automate sending and track performance using CleverTap’s analytics and segmentation tools.

This document explains integrating Email on Acid with CleverTap and using exported HTML in CleverTap campaigns.

# Prerequisites for Integration

The following are the prerequisites for this integration:

- An active Email on Acid account.
- A CleverTap account with a valid Account ID and Passcode.
- (Optional) Brand assets and images hosted on a public CDN (Content Delivery Network).

# Integrate Email on Acid with CleverTap

The integration process involves the following two major steps:

1. [Create and Export Template in Email on Acid](doc:email-on-acid#create-and-export-template-in-email-on-acid).
2. [Configure Email Campaign](doc:email-on-acid#configure-email-campaign).

## Create and Export Template in Email on Acid

Consider an example where a marketing team wants to send a promotional campaign. They can create or customize a template in Email on Acid, test it across clients, and then export the HTML for CleverTap. To do so, perform the following steps:

1. Log in to your Email on Acid account.

2. From the dashboard, either:

   - Create a **new email template** from scratch, or
   - Choose a **predefined template** and modify it with your own content (text, images, branding).

   <br />

3. Customize the template with your campaign details:

   - Update text and CTAs.
   - Add images and logos.
   - Adjust layout for responsiveness.

4. Run **previews and tests** across multiple email clients and devices.

5. Optimize your code for accessibility, subject lines, and spam filter checks.

6. Once finalized, click **Export HTML** or **Copy HTML Code**.

<br />

Your email is now ready for use in a CleverTap campaign.

## Configure Email Campaign

Set up and personalize your campaign in CleverTap using the exported HTML template from Email on Acid. To do so, perform the following steps:

1. Go to the **Campaigns** page in CleverTap, click **+ Campaign**, and select _Email_.

2. Under the _What_ section, click **Go to Editor** and perform the following steps:

   1. Select a _Blank Template_.
   2. Switch to **Source** mode in the email editor.
   3. Paste the copied HTML code from [Create and Export Template in Email on Acid](doc:email-on-acid#create-and-export-template-in-email-on-acid).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/46fbf4bb496469893b9c9b6620fc7e6f92e1b795dbcabc9ffeca9aa66b22c10f-2025-09-19_12-09-47_1.gif",
        "",
        "Paste Code in CleverTap Editor"
      ],
      "align": "center",
      "sizing": "85% ",
      "border": true,
      "caption": "Paste Code in CleverTap Editor"
    }
  ]
}
[/block]


3. (Optional) Add [Liquid tags](doc:personalize-message-all#liquid-tags) for personalization.
4. Click **Preview & Test** to verify personalization and formatting.

> 📘 Preview Campaign
> 
> The preview in CleverTap may render colors differently than in Email on Acid. The final campaign renders correctly to recipients.

5. Once confirmed, click **Publish**.

Your validated email, tested in Email on Acid and integrated with CleverTap, is now ready to send. You can also save the HTML design as a template for future reuse within CleverTap campaigns. For more information about this, refer to [Content Manager Templates](doc:content-manager-templates).