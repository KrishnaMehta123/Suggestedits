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

> 👍 Personalization Example
>
> If you run a multilingual news application, you can personalize each message based on the user's preferred language. 
>
> Using this feature, instead of making one campaign for each language and splitting your campaign stats, you can create one campaign and see its result as a whole, and for each language individually.

# Step 1: Pick the User Property to Personalize Messages

<Image title="Select User Property to personalize.png" alt={2654} className="border" border={true} src="https://files.readme.io/c134047-Select_User_Property_to_personalize.png" />

# Step 2: Create Default Message Copy

In this campaign, you have to specify a default copy, which will go to all users in your target segment that doesn’t have a user property you have selected a copy for. 

**Example**\
If you are sending a message based on language and your app supports 50 languages, you may choose to create a copy for English and Spanish, and keep your default copy as Spanish, which will be sent to everyone else.

<Image title="Personalize Message.png" alt={2852} className="border" border={true} src="https://files.readme.io/229c3e4-Personalize_Message.png" />

# Step 3: Choose and Create Your Message Copy Based on User Properties

After you have selected your default copy, you need to select the various user properties for which you’d like to create copies. Please note no message copy can be left blank.

<Image title="Create copies.png" alt={2856} className="border" border={true} src="https://files.readme.io/87fbd2b-Create_copies.png" />
