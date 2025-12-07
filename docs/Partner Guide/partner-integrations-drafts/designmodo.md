---
title: Designmodo
excerpt: Email Templates
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

[Designmodo](https://designmodo.com) is a design platform that allows you to create, duplicate, and customize marketing templates. You can copy or export your design code and use it directly inside CleverTap campaigns.

With this integration, you can:

- Create or duplicate reusable templates in Designmodo.
- Copy or export the template code.
- Embed the design into CleverTap campaigns for personalization and automation.

This document explains how to prepare templates in Designmodo and integrate them into CleverTap campaigns.

# Prerequisites for Integration

The following are the prerequisites for this integration:

- An active Designmodo account.
- A CleverTap account with a valid Account ID and Passcode.

# Integrate Designmodo with CleverTap

The integration process involves the following two major steps:

1. [Create or Duplicate Template in Designmodo](doc:designmodo#create-or-duplicate-template-in-designmodo).
2. [Configure Email Campaign](doc:designmodo#configure-email-campaign).

## Create or Duplicate Template in Designmodo

Consider an example where a marketing team wants to send a branded onboarding email. They can create or duplicate a template in Designmodo, customize it, and then copy the code into CleverTap. To do so, perform the following steps:

1. Log in to your Designmodo account and open the _Templates_ section.

2. Either create a new template or duplicate an existing one.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c235c3712df4651671ff97900b11554acbd56b1e047f0d8b6cd19df8c13dc4a0-image.png",
        null,
        "Templates in Designmodo"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Templates in Designmodo"
    }
  ]
}
[/block]


3. Customize the duplicated template with text, images, buttons, and brand elements.
4. When ready, click **Copy Code** or **Export HTML**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/98328be437d948cd178ed87b1d5f979f6584fb9d413d04f508e82c4a59b6f9af-2025-09-20_15-11-07_1.gif",
        "",
        "Export or Copy HTML from Designmodo"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Export or Copy HTML from Designmodo"
    }
  ]
}
[/block]


Your template code is now ready to be embedded into a CleverTap campaign.

## Configure Email Campaign

Set up and personalize your campaign in CleverTap using the exported template code from Designmodo. To do so, perform the following steps:

1. Go to the _Campaigns_ page in CleverTap, click **+ Campaign**, and select _Email_.

2. Under the _What_ section, click **Go to Editor** and perform the following steps:

   1. Select a _Blank Template_.
   2. Switch to **Source** mode in the email editor.
   3. Paste the code copied from [Create or Duplicate Template in Designmodo](doc:designmodo#create-or-duplicate-template-in-designmodo).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7059f971bf5130fddb26229432798b842c626d2520fcc908c45ed55c5c4731e2-2025-09-20_15-12-11_1.gif",
        "",
        "Pasting Designmodo Code in CleverTap"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Pasting Designmodo Code in CleverTap"
    }
  ]
}
[/block]


3. (Optional) Edit the HTML as needed. You can also add [Liquid tags](doc:personalize-message-all#liquid-tags) for personalization.
4. Click **Preview & Test** to verify personalization and formatting.

> 📘 Preview Campaign
> 
> The preview in CleverTap may render colors differently than what you designed in Designmodo. The final campaign renders correctly to recipients.

5. Once confirmed, click **Publish**.

Your customized email, designed in Designmodo and integrated with CleverTap, is now ready to send. You can also save your HTML design as a template for future reuse within CleverTap campaigns. For more information about this, refer to [Content Manager Templates](doc:content-manager-templates).