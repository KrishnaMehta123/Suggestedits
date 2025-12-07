---
title: Personalize Messages_2.0
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
# Overview

When you create campaigns in CleverTap, you can personalize messages for each user based on user profile properties.
[block:callout]
{
  "type": "success",
  "body": "If you run a multilingual news application, you can personalize each message based on the user's preferred language. \n\nUsing this feature, instead of making one campaign for each language and splitting your campaign stats, you can create one campaign and see its result as a whole, and for each language individually.",
  "title": "Personalization Example"
}
[/block]


# Step 1: Pick the User Property to Personalize Messages
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c134047-Select_User_Property_to_personalize.png",
        "Select User Property to personalize.png",
        2654,
        432,
        "#faf6f7"
      ],
      "border": true
    }
  ]
}
[/block]
# Step 2: Create Default Message Copy

In this campaign, you have to specify a default copy, which will go to all users in your target segment that doesn’t have a user property you have selected a copy for. 

**Example**
If you are sending a message based on language and your app supports 50 languages, you may choose to create a copy for English and Spanish, and keep your default copy as Spanish, which will be sent to everyone else.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/229c3e4-Personalize_Message.png",
        "Personalize Message.png",
        2852,
        3946,
        "#f2f1f6"
      ],
      "border": true
    }
  ]
}
[/block]
# Step 3: Choose and Create Your Message Copy Based on User Properties

After you have selected your default copy, you need to select the various user properties for which you’d like to create copies. Please note no message copy can be left blank.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/87fbd2b-Create_copies.png",
        "Create copies.png",
        2856,
        1294,
        "#e7e6ea"
      ],
      "border": true
    }
  ]
}
[/block]