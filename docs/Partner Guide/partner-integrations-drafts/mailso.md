---
title: Mail.so
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
# Overview

Mail.so is an email infrastructure platform that provides reliable tools for sending, receiving, and validating emails. It helps businesses ensure that user email addresses are accurate, deliverable, and safe to use.

When integrated with CleverTap, Mail.so enables real-time email validation through Linked Content. This allows marketers and developers to verify email addresses dynamically during campaign execution or user interactions. The integration ensures that campaigns reach valid users, improves engagement accuracy, and reduces the chances of sending messages to invalid or disposable addresses.

### Use Case

When a user submits an email through your app or website, CleverTap triggers a **Push Notification campaign**.  
CleverTap’s **Linked Content** feature sends the email to Mail.so for verification and retrieves the validation result in real time.

Based on the response:

- **If the email is valid:** The user continues the process seamlessly.
- **If the email is invalid:** An in-app or push message prompts the user to correct the email address.

This ensures that only valid, deliverable addresses are added to your system, improving campaign performance and data integrity.

# Prerequisites for Integration

The following are the prerequisites for this integration:

- Access to your Mail.so dashboard and Mail.so API key.
- Access to your CleverTap Dashboard with rights to create and manage Linked Content and Campaigns.

# Integrate Mail.so with CleverTap

This section explains how to connect Mail.so with CleverTap using Linked Content. Once configured, CleverTap can call Mail.so’s verification API to validate user email addresses dynamically whenever a campaign is triggered.

The process includes three key configurations:

1. [Obtain the Mail.so API Key](<>)
2. [Configure Linked Content](<>)
3. [Configure Campaign in CleverTap](<>)

## Obtain the Mail.so API Key

To enable communication between CleverTap and Mail.so, you need a Mail.so API key. This key authenticates CleverTap’s requests to Mail.so and ensures secure data exchange. To do so, perform the following steps:

1. Log in to your Mail.so Dashboard.
2. Go to _API_ from the top navigation panel.
3. Copy the _API Key_ displayed in this section.
4. Keep it secure; it will be used in the Linked Content configuration step.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dd0453010af50fa59c5291e92bc27f5a9c21879684b76e2a4114c1f94f199ec1-image.png",
        null,
        "Mail.so API Key page"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Mail.so API Key page"
    }
  ]
}
[/block]


For additional details, refer to the [Mail.so API Documentation](https://mail.so/docs).

## Configure Linked Content

Once the API key is ready, create a _Linked Content_ configuration in CleverTap. Linked Content allows CleverTap to fetch live data from Mail.so’s verification API whenever a campaign runs.

To configure Linked Content:

1. Go to _Settings_ > _Setup_ > _Linked Content_ from the CleverTap dashboard.

2. Click **+ Linked Content** and enter the following:

[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Value",
    "0-0": "**Name**",
    "0-1": "Provide a name for the Linked Content. For example: `Mail.so Email Validation`",
    "1-0": "**Request Type**",
    "1-1": "Select `GET` method.",
    "2-0": "**Endpoint URL**",
    "2-1": "Enter the following endpoint URL: `https://api.mails.so/v1/validate?email={{email}}`  \n  \n- The `{{email}}` parameter dynamically retrieves the user’s email from CleverTap.\n- The endpoint validates that email in real time through Mail.so’s API.",
    "3-0": "**Headers**",
    "3-1": "Add key-value pair as:  \nKey: `x-mails-api-key`  \nValue: `<YOUR_API_KEY>`"
  },
  "cols": 2,
  "rows": 4,
  "align": [
    "left",
    "left"
  ]
}
[/block]


3. Click **Test Linked Content** to verify the connection. A successful response will look similar to the following sample:

```json
{
  "data": {
    "email": "user@example.com",
    "provider": "gmail",
    "score": 100,
    "is_disposable": false,
    "is_free": true,
    "result": "deliverable",
    "reason": "accepted_email"
  },
  "error": null
}
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d36834cdf3040ca49a7d0ebab85629522e18cddf38c6367926657441afd91c58-image.png",
        null,
        null
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true
    }
  ]
}
[/block]


4. Click **Autofill Objects with Response** to map the data automatically.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a2234f9f6d4912a49e4c8daf056d1f2d341fe341afcb94bdb9ce881b43486e49-image.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "45% ",
      "border": true
    }
  ]
}
[/block]


5. Click **Test and Save** to complete your Linked Content configuration.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/82403b215a4d6080c96d54ad01528db3f022816e401409c63af03d0dd4a97616-f3c8d36cb3a3c519913e7ce1264832eb7b72bfda7d84994768ac5441f5834d8c-image.png",
        "",
        "Test and Save"
      ],
      "align": "center",
      "sizing": "55% ",
      "border": true,
      "caption": "Test and Save"
    }
  ]
}
[/block]


## Configure the Campaign in CleverTap

With Linked Content set up, you can now use it inside a campaign. This example demonstrates how to incorporate Mail.so verification results into a **Push Notification campaign** in CleverTap.

1. In your **CleverTap Dashboard**, navigate to **Campaigns → + Campaign**.

2. Select **Push Notification** as the campaign type.

3. Configure campaign parameters such as audience, trigger conditions, and delivery preferences.

4. Under the **What** section, click the **API** icon.

5. From the dropdown, select the **Linked Content** configuration you created earlier.

6. Map the email parameter to:

   ```
   {{ Profile.Email | default: "NULL" }}
   ```

7. In the **Title** or **Message** field, type `{{` to access Linked Content data.

8. Use **Liquid tags** to personalize the message based on Mail.so’s verification result:

```liquid
{% if Linked["Mail.so"].result == "deliverable" %}
Email verified successfully.
{% else %}
Invalid email address provided. Please enter a valid email.
{% endif %}
```

> ⚠️ **Note:**
> 
> This logic customizes the push message depending on the email verification result returned by Mail.so.

9. Click **Preview and Test** to confirm the campaign behavior.
10. Once validated, click **Publish** to make the campaign live.

## Expected Outcome

When the campaign runs:

- **For valid emails:** Users receive a success message such as _“Email verified successfully.”_
- **For invalid emails:** Users receive a prompt such as _“Invalid email address provided. Please enter a valid email.”_

This flow ensures data accuracy and improves the overall user experience.

[Placeholder: Screenshots showing valid and invalid email notification examples]

## Conclusion

This integration allows CleverTap to validate user emails dynamically through Mail.so and tailor messaging accordingly.  
It strengthens data accuracy, enhances user engagement, and ensures a cleaner, more reliable contact database.

### 📘 **Final Category Placement**

**Category:** Integrations  
**Subcategory:** Email Validation  
**Title:** _Mail.so Email Validation Integration with CleverTap_