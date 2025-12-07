---
title: KickBox
excerpt: Email Validator
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

[Kickbox](https://kickbox.com) helps verify email addresses in real time to ensure that only valid and deliverable emails enter your database. By integrating Kickbox with CleverTap, you can automatically validate email addresses entered through forms, sign-ups, or other data collection points.

This integration helps maintain clean and reliable email lists, improve campaign deliverability, and prevent invalid or disposable email addresses from being added to your marketing database.

The Kickbox integration helps verify emails instantly at multiple entry points, such as:

- Account creation
- Mobile app registration
- Newsletter subscription
- Reservation or demo request forms
- Any other form that collects user email addresses

For additional details about Kickbox response parameters, refer to the [Kickbox API documentation](https://docs.kickbox.com/docs).

> 🚧 Support for Integration
> 
> This integration is managed and continuously improved by Kickbox. The CleverTap and Kickbox integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [Kickbox](https://kickbox.com/contact/) for support and resolution.

# Prerequisites for Integration

The following are the prerequisites:

- Access to your Kickbox account and dashboard.
- Permission to create and configure API Keys.
- Access to your CleverTap Dashboard with rights to create and manage Linked Content and Campaigns.

# Integrate Kickbox with CleverTap

Integrating Kickbox with CleverTap allows you to verify user email addresses in real time as part of your CleverTap campaigns. The setup involves connecting CleverTap to Kickbox’s verification API through _Linked Content_, and then using the connection in a campaign to validate user data dynamically.

The process includes three key configurations:

1. [Obtain Kickbox API Key](doc:kickbox#obtain-kickbox-api-key)
2. [Configure Linked Content](doc:kickbox#configure-linked-content)
3. [Configure Campaign in CleverTap](doc:kickbox#configure-the-campaign-in-clevertap)

## Obtain Kickbox API Key

Begin the integration by generating an API Key in Kickbox. This key will authenticate CleverTap requests to the Kickbox API. To do so, perform the following steps:

1. Log in to your Kickbox Dashboard.
2. Go to _Settings_ > _API Keys_.
3. Click **Generate API Key** to create a new key.
4. Assign permissions as required for your use case. For this example, full permissions are granted.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/37c1b638e9e07285f2cd8821829f7ccc489440b607e563e0b02a1fc7860846e6-Screen_Recording_2025-07-01_at_1.29.40PM_1.gif",
        "",
        "Obtain Kickbox API Key"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Obtain Kickbox API Key"
    }
  ]
}
[/block]


The API Key acts as your authentication token, allowing CleverTap to securely communicate with Kickbox during each email validation request.

## Configure Linked Content

Once you have the API Key, set up a Linked Content configuration in CleverTap. This enables CleverTap to call the Kickbox API whenever it needs to validate an email address in real time.

To configure Linked Content:

1. Go to _Settings_ > _Setup_ > _Linked Content_ from the CleverTap dashboard.
2. Click **+ Linked Content** and enter the following:

[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Value",
    "0-0": "**Name**",
    "0-1": " Provide a name for the Linked Content. For example: `Kickbox Email Verification`",
    "1-0": "**Request Type**",
    "1-1": "Select `GET` method.",
    "2-0": "**Endpoint URL**",
    "2-1": "Enter the following endpoint URL: `https://api.kickbox.com/v2/verify?email={{Profile.Email}}&apikey=API_KEY`  \n  \n- The `email` parameter is dynamically mapped from CleverTap’s user profile data.\n- The `apikey` must be replaced with the Kickbox API Key generated earlier."
  },
  "cols": 2,
  "rows": 3,
  "align": [
    "left",
    "left"
  ]
}
[/block]


3. Click **Test Linked Content** to verify the connection. A successful response will look similar to the following sample:

```json
{
  "success": true,
  "result": "deliverable",
  "reason": "accepted_email",
  "disposable": false,
  "free": true,
  "email": "example@gmail.com",
  "domain": "gmail.com"
}
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4da2809a5c062849472c7c319df6572f5b54b5f0528b0dc2290e63b61a0aa6fc-image.png",
        null,
        "Linked Content Setup"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Linked Content Setup"
    }
  ]
}
[/block]


This response confirms that the connection between CleverTap and Kickbox is active and functioning correctly.

4. Click **Test and Save** to complete your Linked Content configuration.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f3c8d36cb3a3c519913e7ce1264832eb7b72bfda7d84994768ac5441f5834d8c-image.png",
        null,
        "Test and Save"
      ],
      "align": "center",
      "sizing": "45% ",
      "border": true,
      "caption": "Test and Save"
    }
  ]
}
[/block]


## Configure the Campaign in CleverTap

After the Linked Content setup is complete, you can integrate it into a campaign. This allows CleverTap to verify user email addresses dynamically and use the verification results to personalize communication or trigger actions. To do so, perform the following steps:

1. Go to the _Campaigns_ page, click **+ Campaign**, and select _Push Notification_ from the list of messaging channels.
2. Define the campaign’s target segment, qualification criteria, and delivery schedule.
3. Click **Go to Editor** under the _What_ section.
   1. Click **Personalization** in the top-right corner.
   2. Select the Linked Content configured in [Configure Linked Content](doc:kickbox#configure-linked-content).
   3. Map the email parameter to:
      ```
      {{ Profile.Email | default: "NULL" }}
      ```

This mapping ensures that CleverTap passes the user’s email to Kickbox for verification each time the campaign is triggered.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e81e3c810f5e9fae180f94c11d62748afd622a71a92bff3aa8c2890d9a33fb56-image.png",
        null,
        "Personalization Setup"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Personalization Setup"
    }
  ]
}
[/block]


4. Use [Liquid tags](doc:personalize-message-all#liquid-tags) to personalize your message based on email validity. For example:

```liquid
{% assign emailStatus = linkedcontent.result %}
{% if emailStatus == "deliverable" %}
  The email address you provided is valid and deliverable.
{% else %}
  The email address you entered is invalid or undeliverable. Please check and try again.
{% endif %}
```

This logic dynamically displays different messages depending on the verification result returned by Kickbox.

> 📘 Note
> 
> When using _Linked Content_ responses, extract only the specific fields needed for display to maintain clarity and prevent unnecessary data exposure.

5. Click **Preview and Test** to verify that the response values from Kickbox appear as expected.
6. Once confirmed, click **Publish** to activate the campaign.

When triggered:

- If the email address is **not valid**, the user receives a notification indicating the issue.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e871eaa0751902bd255276e32501eb846d285341da8cdde3683145f027bff433-image.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "35% ",
      "border": true
    }
  ]
}
[/block]


- If the email address is **valid**, a confirmation message is sent.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cf8721ef564488c469b0f00ec7b1d0e9cff6ecdf0005677787839cfa7bdd55c4-image.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "35% ",
      "border": true
    }
  ]
}
[/block]


The Kickbox–CleverTap integration enables real-time email validation for clean, reliable data across your campaigns.