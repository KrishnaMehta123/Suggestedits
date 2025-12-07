---
title: Managing WhatsApp Templates (Edit, Delete, Import)
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Template Operations

You can edit a template and add or remove a language or other information. However, note that:

- Templates can be edited only once every 24 hours. 
- You cannot edit a template that is being reviewed.
- If you edit a template, then all the campaigns and journeys using this template will be stopped.

If you delete a template, all the campaigns and journeys using this template will be stopped. 

### Edit, Delete or Refresh WhatsApp Message Templates

To edit or delete an existing template:

1. Navigate to _Settings > Channels > WhatsApp Direct > Templates_.
2. Select any template and click the ellipsis icon adjacent to it.
3. Click **Overview** and then perform the desired operation.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dc49e19-overview.png",
        "",
        "Template Overview"
      ],
      "align": "center",
      "sizing": "45% ",
      "border": true,
      "caption": "Template Overview"
    }
  ]
}
[/block]


4. Similarly, select **Refresh Status** from the ellipsis menu to refresh the approval status of an existing template.

### Import Templates

> 🚧 Template Import Limitations for External Providers
> 
> Importing templates is supported only for CleverTap BSP. For all other providers, you must recreate templates separately within their interfaces.

CleverTap allows you to easily import templates from your WhatsApp Business Manager Account to streamline managing your WhatsApp templates. Follow the steps below to import them directly into the CleverTap dashboard with a few clicks:

1. Go to the CleverTap dashboard and navigate to **_Settings_** > **_Channels_** > **_WhatsApp_**.
2. From the list of available providers, select the appropriate provider's nickname. 
3. Click the **Templates** tab and select **Import Templates**. The _Import Template_ button is visible only for CleverTap BSP. Clicking it will open a window for importing templates.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8afb1f1-import_temp.png",
        null,
        "Import Template "
      ],
      "align": "center",
      "border": true,
      "caption": "Import Template "
    }
  ]
}
[/block]


The _Import Template_ window opens.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d629f40-2023-09-25_17-21-03.jpg",
        null,
        "Import WhatsApp Templates "
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Replace or add new WhatsApp Templates "
    }
  ]
}
[/block]


4. Click _Import_. Select this option to replace all existing templates on your CleverTap dashboard. This action will delete all current templates and import the latest approved templates from the Meta dashboard. This ensures CleverTap has the most up-to-date templates with their respective content and statuses.
5. Click **Continue** to replace or add templates.  The CleverTap dashboard shows the new templates. Your previous templates are mailed to your email account.

> 📘 Impact of Template Import on Failing WhatsApp Campaigns
> 
> Importing templates will not automatically resolve errors or issues related to the existing WhatsApp campaigns or journeys. These campaigns and journeys will continue to fail until you manually update the imported template in the affected campaign's What section.
> 
> To address campaign failures resulting from template-related errors, please follow the below steps:
> 
> 1. Identify the specific campaign or journey that is encountering the error.
> 2. Access the _What_ section of the campaign or the specific journey node.
> 3. Edit the campaign or journey and select the specific imported templates.
> 4. Save and publish the changes, and check that the campaigns and journeys use the updated templates.

> 📘 Track Button Clicks
> 
> Check the URL defined to track the button clicks in the META dashboard. For example, _ct1.io.//{{1}}_. This URL will be imported with the template in the CleverTap dashboard. This link cannot be updated later.