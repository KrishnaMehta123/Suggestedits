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

* **If the email is valid:** The user continues the process seamlessly.
* **If the email is invalid:** An in-app or push message prompts the user to correct the email address.

This ensures that only valid, deliverable addresses are added to your system, improving campaign performance and data integrity.

# Prerequisites for Integration

The following are the prerequisites for this integration:

* Access to your Mail.so dashboard and Mail.so API key.
* Access to your CleverTap Dashboard with rights to create and manage Linked Content and Campaigns.

# Integrate Mail.so with CleverTap

This section explains how to connect Mail.so with CleverTap using Linked Content. Once configured, CleverTap can call Mail.so’s verification API to validate user email addresses dynamically whenever a campaign is triggered.

The process includes three key configurations:

1. [Obtain the Mail.so API Key]()
2. [Configure Linked Content]()
3. [Configure Campaign in CleverTap]()

## Obtain the Mail.so API Key

To enable communication between CleverTap and Mail.so, you need a Mail.so API key. This key authenticates CleverTap’s requests to Mail.so and ensures secure data exchange. To do so, perform the following steps:

1. Log in to your Mail.so Dashboard.
2. Go to _API_ from the top navigation panel.
3. Copy the _API Key_ displayed in this section.
4. Keep it secure; it will be used in the Linked Content configuration step.

<Image align="center" alt="Mail.so API Key page" border={true} caption="Mail.so API Key page" src="https://files.readme.io/dd0453010af50fa59c5291e92bc27f5a9c21879684b76e2a4114c1f94f199ec1-image.png" width="65% " />

For additional details, refer to the [Mail.so API Documentation](https://mail.so/docs).

## Configure Linked Content

Once the API key is ready, create a _Linked Content_ configuration in CleverTap. Linked Content allows CleverTap to fetch live data from Mail.so’s verification API whenever a campaign runs.

To configure Linked Content:

1. Go to _Settings_ > _Setup_ > _Linked Content_ from the CleverTap dashboard.

2. Click **+ Linked Content** and enter the following:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Value
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Name**
      </td>

      <td>
        Provide a name for the Linked Content. For example: `Mail.so Email Validation`
      </td>
    </tr>

    <tr>
      <td>
        **Request Type**
      </td>

      <td>
        Select `GET` method.
      </td>
    </tr>

    <tr>
      <td>
        **Endpoint URL**
      </td>

      <td>
        Enter the following endpoint URL: `https://api.mails.so/v1/validate?email={{email}}`

        * The `{{email}}` parameter dynamically retrieves the user’s email from CleverTap.
        * The endpoint validates that email in real time through Mail.so’s API.
      </td>
    </tr>

    <tr>
      <td>
        **Headers**
      </td>

      <td>
        Add key-value pair as:  
        Key: `x-mails-api-key`  
        Value: `<YOUR_API_KEY>`
      </td>
    </tr>
  </tbody>
</Table>

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

<Image align="center" alt="Linked Content Setup" border={true} caption="Linked Content Setup" src="https://files.readme.io/d36834cdf3040ca49a7d0ebab85629522e18cddf38c6367926657441afd91c58-image.png" width="75% " />

4. Click **Autofill Objects with Response** to map the data automatically.

<Image align="center" alt="Autofill Objects with Response" border={true} caption="Autofill Objects with Response" src="https://files.readme.io/a2234f9f6d4912a49e4c8daf056d1f2d341fe341afcb94bdb9ce881b43486e49-image.png" width="45% " />

5. Click **Test and Save** to complete your Linked Content configuration.

<Image align="center" alt="Test and Save" border={true} caption="Test and Save" src="https://files.readme.io/82403b215a4d6080c96d54ad01528db3f022816e401409c63af03d0dd4a97616-f3c8d36cb3a3c519913e7ce1264832eb7b72bfda7d84994768ac5441f5834d8c-image.png" width="55% " />

## Configure the Campaign in CleverTap

With Linked Content set up, you can now use it inside a campaign. This example demonstrates how to incorporate Mail.so verification results into a _Push Notification campaign_ in CleverTap.

1. Go to the _Campaigns_ page, click **+ Campaign**, and select _Push Notification_ from the list of messaging channels.
2. Define the campaign’s target segment, qualification criteria, and delivery schedule.
3. Click **Go to Editor** under the _What_ section.  
   1. Click **Personalization** in the top-right corner.
   2. Select the Linked Content configured in [Configure Linked Content](doc:mailso#configure-linked-content).
   3. Map the email parameter to:

```
{{ Profile.Email | default: "NULL" }}
```

This mapping ensures that CleverTap passes the user’s email to Mail.so for verification each time the campaign is triggered.

<Image align="center" alt="Personalization Setup" border={true} caption="Personalization Setup" src="https://files.readme.io/42dd7cfd83c1fb92de1cc7414dbe3e2b1f3aba3ba6ab21ded6062bedb81d5d60-image.png" />

4. Use [Liquid tags](doc:personalize-message-all#liquid-tags) to personalize your message based on email validity. For example:

```liquid
{% assign emailStatus = linkedcontent.result %}
{% if emailStatus == "deliverable" %}
  The email address you provided is valid and deliverable.
{% else %}
  The email address you entered is invalid or undeliverable. Please check and try again.
{% endif %}
```

This logic dynamically displays different messages depending on the verification result returned by Mail.so.

> 📘 Note
>
> When using _Linked Content_ responses, extract only the specific fields needed for display to maintain clarity and prevent unnecessary data exposure.

<Image align="center" alt="Linked Content" border={true} caption="Linked Content" src="https://files.readme.io/2b6a55dbbd951c9989440e468890a00f3e2ac99e6c0df2174b044ae7393a0213-image.png" width="75% " />

5. Click **Preview and Test** to verify that the response values from Mail.so appear as expected.
6. Once confirmed, click **Publish** to activate the campaign.

When triggered:

* If the email address is **not valid**, the user receives a notification indicating the issue.

<Image align="center" alt="Push Notification - Invalid Email" border={true} caption="Push Notification - Invalid Email" src="https://files.readme.io/ac39b0aff3968bb9f30dac2af4700aefcce173bbc9ee7c231c40f5b15a707942-image.png" width="35% " />

* If the email address is **valid**, a confirmation message is sent.

<Image align="center" alt="Push Notification - Valid Email" border={true} caption="Push Notification - Valid Email" src="https://files.readme.io/81491d54f1ca1249709b3b8a43f750fd25ab8c6fea9b1aee43d52d58a7b85395-image.png" width="35% " />

This integration allows CleverTap to validate user emails dynamically through Mail.so and tailor messaging accordingly. It strengthens data accuracy, enhances user engagement, and ensures a cleaner, more reliable contact database.
