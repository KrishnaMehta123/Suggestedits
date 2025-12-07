---
title: Lokalise
excerpt: Email Translation Partner
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

[Lokalise ](https://lokalise.com/) is a platform that streamlines the translation and localization of digital content for multilingual support. Integrate CleverTap with Lokalise to automate the translation of email templates. By exporting templates from CleverTap to Lokalise for translation and then importing them back, you can deliver personalized campaigns in your users' preferred languages, enhancing engagement and streamlining your localization process.

# Prerequisites for Integration

Ensure that you have the following:

- Lokalise account 
- CleverTap account

> 📘 Private Beta
> 
> This feature is released in Private Beta. For any queries or assistance required with integrating CleverTap and Lokalise, contact the [Lokalise Support](https://docs.lokalise.com/en/) team.

# Integrate CleverTap with Lokalise

To set up the CleverTap integration with your Lokalise account:

1. Set Up Project with CleverTap App on Lokalise Dashboard
2. Get Email Templates or Content Blocks from CleverTap and push them back to CleverTap
3. Find Translated Email templates or Content Blocks in CleverTap

# Set Up Project with CleverTap App on Lokalise Dashboard

1. Navigate to _Project > New Project_ and select **Marketing and support**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/de416561d68967244d3eb788d598daab4fc9534fdb8a31803b601c8a512fd330-Lokalise_2.png",
        "",
        "Marketing and support"
      ],
      "align": "center",
      "border": true,
      "caption": "Marketing and support"
    }
  ]
}
[/block]


2. Add information in the following fields:

- **Project Name**: Add a name for the project.
- **Base language**: Select the language in which the emails have been created from the drop-down menu.
- **Target languages**: Select the languages in which the created emails need to be translated from the drop-down menu.
- **Select content integration**: Select **CleverTap** from the drop-down menu.

3. Click on **Create Project**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8de124f468b3d3d0f3129ed39283dd1df5cc0b23c3c31449c68c5a3e770f7d9b-CleverTap_23.png",
        "",
        "Create Project - Lokalise"
      ],
      "align": "center",
      "sizing": "70% ",
      "border": true,
      "caption": "Create Project - Lokalise"
    }
  ]
}
[/block]


4. Enter the following details:

- **Account ID **: Locate the Project ID under _Settings_ > _Project_ from the CleverTap dashboard.
- **Passcode**: Locate Passcode under _Settings_ > _Project_ from the CleverTap dashboard. To know more, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).
- **Region**: Locate Region for the API endpoint you want to select under _Settings_ > _Project_ from the CleverTap dashboard. To identify the region for your account, refer to the following table:

| Region              | CleverTap Dashboard URL                           |
| :------------------ | :------------------------------------------------ |
| Indonesia           | <https://aps3.dashbaord.clevertap.com/login.html> |
| Europe (default)    | <https://eu1.dashboard.clevertap.com/login.html>  |
| India               | <https://in1.dashboard.clevertap.com/login.html>  |
| Middle East (UAE)   | <https://mec1.dashboard.clevertap.com/login.html> |
| Singapore           | <https://sg1.dashboard.clevertap.com/login.html>  |
| United States (U.S) | <https://us1.dashboard.clevertap.com/login.html>  |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d6907e7-Taxi_Project_ID.png",
        "Project ID and Region",
        "Locate Project ID and Region on CleverTap Dashboard"
      ],
      "align": "center",
      "border": true,
      "caption": "Locate Project ID and Region on CleverTap Dashboard"
    }
  ]
}
[/block]


5. Click on **Authorize**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b7c297451b073f564bf149757d7ec490501daa6688ac9d66a193e4276eb0a520-Lokalise_15.png",
        "",
        "Account ID, Passcode and Region"
      ],
      "align": "center",
      "border": true,
      "caption": "Account ID, Passcode and Region"
    }
  ]
}
[/block]


# Get Email Templates from CleverTap and push back translated templates to CleverTap

1. Navigate to _Content Management_  and all the templates under _Content Manager > Templates > Email_ from the CleverTap dashboard will be imported to Lokalise. {@krishna, please fix this}Click on **Refresh** if any changes are made to the templates on the CleverTap Dashboard. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4daec4fabac58dc7ba8f9c63d1fca76f61e6db69c9648f54e2f42ec858cede81-Lokalise_19.png",
        "",
        "Import from CleverTap and Refresh"
      ],
      "align": "center",
      "border": true,
      "caption": "Import from CleverTap and Refresh"
    }
  ]
}
[/block]


6. Select the template that needs to be translated, and click on **Import from CleverTap**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bf80cf3b3b84f0957224dcc3ce7f18964d35ebb070e1dc3a3c09194c72c2bac0-Lokalise_20.png",
        "",
        "Import from CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Import from CleverTap"
    }
  ]
}
[/block]


7. The template will then appear in the Imported tab. Click on **View Content** from the confirmation message or navigate to the **Editor** tab to view translated content.

> 🚧 Personalization
> 
> CleverTap allows email personalization using **{}** formats. When importing emails from CleverTap into Lokalise, these personalized values are included. Make sure not to translate them while exporting content back to CleverTap.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ba322d02fd63f883915ed67366aa25932ebdb6d7ff3dfff4d7dd22eb627e97d7-Lokalise_22.png",
        "",
        "Lokalise Editor"
      ],
      "align": "center",
      "border": true,
      "caption": "Lokalise Editor"
    }
  ]
}
[/block]


8. After reviewing the translated content, navigate back to _Content Manager > Imported_, select the template and click on **Export to CleverTap**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/394bfb85a2db7b03a5a2b2d5444af6c1bfee7495ed153216e835f7d07b023ff0-Lokalise_21.png",
        "",
        "Export to CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Export to CleverTap"
    }
  ]
}
[/block]


# Find Translated Email templates in CleverTap

For users with a Content Manager subscription in CleverTap, the exported translated templates from Lokalise can be found under _Content Manager > Templates > Email_. Each language has its own separate template. (@Sunil: How do we identify which language the template??)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ad56bfcc4cb4563dc7133e94c9f3d1b37db975c55f4cf831d0686101f772a851-Lokalise_24.png",
        "",
        "Translated Email Template - CMS"
      ],
      "align": "center",
      "border": true,
      "caption": "Translated Email Template - CMS"
    }
  ]
}
[/block]


For users without a Content Manager subscription (by subscription do we mean add-on??? or is it part of some plan??), the exported translated templates appear under _Campaigns > + Campaigns > Emails > What Section > Saved Templates_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bd727e756fd86db027e700d858b1d7c1df16cb5d7fb8d5cf35cb1c3bcd47b800-Lokalise_26.png",
        "",
        "Translated Email Template - Saved Template in Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Translated Email Template - Saved Template in Campaign"
    }
  ]
}
[/block]


# Translate Content Blocks

All the content blocks from the CleverTap dashboard are imported into Lokalise automatically. (@Sunil: You mean translated automatically?)

(@Sunil: a small use case will help - when we will have to translate content blocks. establish connection between the main heading translate and import and export sections)

## Import Content Blocks in Lokalise

 Open the Lokalise dashboard. To import the content blocks for translation into Lokalise, perform the following steps:

1. Click **Refresh** to sync any changes made in the CleverTap dashboard. - (@Sunil: from where on Lokalise dashboard)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7946035bbf4a0e7902f4330065af0257049f277c6ee64ab1863fe6a346487915-image.png",
        null,
        "Import Content Block from CleverTap and Refresh"
      ],
      "align": "center",
      "border": true,
      "caption": "Import Content Block from CleverTap and Refresh"
    }
  ]
}
[/block]


2. Select the content block that requires translation and click **Import from CleverTap**. The imported content block will appear under the _Imported_ tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d5f2a474b01c766fe3bb7d18bfb3252b5c5af11150e626cccab31f5e151e9871-image.png",
        null,
        "Import Content Block from CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Import Content Block from CleverTap"
    }
  ]
}
[/block]


2. Click  **View Content** from the confirmation message or select the _Editor_ tab to review and translate the content.

> 🚧 Personalization
> 
> CleverTap allows content personalization using **{}** formats (@Sunil: Using Liquid Tags you mean??). When importing content blocks from CleverTap into Lokalise, these personalized values are included. Do not translate these personalization values while exporting content back to CleverTap.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0cc0cf237b371dd3b935e33ffadd7ac7d273729bb545fbcfce938cc6585de61d-image.png",
        null,
        "Lokalise Editor - Content Block"
      ],
      "align": "center",
      "border": true,
      "caption": "Lokalise Editor - Content Block"
    }
  ]
}
[/block]


## Export Translated Content Blocks to CleverTap

After reviewing the translated content in the Lokalise editor, follow these steps:

1. Go to _Content Manager > Imported_, select the content block, and click **Export to CleverTap**. The content blocks will now be exported to CleverTap, and they can be viewed from the CleverTap dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/eb5c2833563cf61a832575e9de23bd3bef043e1367e313105e82581944130467-image.png",
        null,
        "Export Content Blocks to CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Export Content Blocks to CleverTap"
    }
  ]
}
[/block]


## Find Translated Content Blocks in CleverTap

Users with a Content Manager subscription in CleverTap can find the exported translated content blocks from Lokalise under _Content Manager > Blocks_. Each language has a version marked with a suffix for easy identification.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e8a3557687507e9ca859a954569bcd5e6c590eaba12a6bdaa506786412e74517-image.png",
        null,
        "Translated Content Block in CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Translated Content Block in CleverTap"
    }
  ]
}
[/block]


# FAQs

### Why are only base templates fetched from CleverTap to Lokalise?

Currently, only base templates are integrated, which limits the availability of translated templates.

### Why are translated templates not matching the drag-and-drop (@Sunil/Krishna: is this how its written on the dashboard) base email templates?\*\*  

Translating JSON to match the "drag-and-drop" template format presents challenges, leading CleverTap to store translated templates in HTML format instead.

### Why do translated templates include the locale present in the base template?

- The locale for the base template is not currently set, making it difficult to differentiate between the base locale and the translated locale.
- To streamline this, translated templates are created as "Base Template name\_{Locale}." These are considered child templates.
- When base templates are fetched and translated templates are pushed back, CleverTap updates child templates with the specified locale. For instance, a base template named "Welcome to the App" with the locale "en" will result in three templates upon translating to "fr" and "es": "Welcome to the App_en," "Welcome to the App_fr," and "Welcome to the App_es."

### How can translated templates be used for sending email campaigns from CleverTap?  

When creating an email campaign, the ["By User Property"](https://docs.clevertap.com/docs/create-message-email#by-user-property) option can be utilized to set the property to match the locale of the translated campaign.

### What happens if a translated email template currently in use is updated?

- When an email template from CleverTap CMS or saved templates is used in a campaign, separate instances are created for each send. This ensures personalization and localization are tailored to each email.
- Edits made to an existing template do not impact campaigns created with earlier versions of that template.
- Changes to the main email template in the CMS or saved templates do not retroactively apply to previously created or sent campaigns.
- New campaigns will utilize the updated template, while campaigns in draft or scheduled status require manual updates with the new version.