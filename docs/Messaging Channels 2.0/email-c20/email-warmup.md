---
title: Email Warmup _ WIP_Not to be released with campaign 2.0
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
# Email Warmup Process <<@sunil to move it out in a separate page>>
The email warmup process is done to ease the inboxing process and establish a positive sending reputation with internet service providers (ISPs). It is essential when you plan to use a new, dedicated IP address/domain where you plan to deploy large volumes of emails. This strategy sets you apart from spammers and lets ISPs know the type of mailing you are doing.

##IP Warming
IP warming is the practice of gradually increasing the volume of mail sent with a dedicated IP address according to a predetermined schedule. This gradual process helps establish a reputation with ISPs as legitimate email sender and improves your emails' deliverability.

[block:callout]
{
  "type": "info",
  "body": "We recommend that you have a list of contacts of more than 10,000 emails.",
  "title": "Recommended List of Contacts"
}
[/block]
During this warmup period, ISPs evaluate your email list health, sending behavior, email list health, and whether you provide relevant and valuable information to your recipients. The better the engagement, the better the ISPs will favor your IP. You can monitor and optimize your entire email campaign. Once you have built a good reputation during the warmup period, you can focus on your email strategy, the content, and the tracking results.
[block:callout]
{
  "type": "info",
  "body": "If you have set up your email service provider with SendGrid, their support team can help you with IP warming and monitor your domain as well as your IP quality.",
  "title": "SendGrid Support"
}
[/block]
##Populate Historical Data into CleverTap
From the initial days of deployment, you will want to upload all the active, engaged users from your previous email provider so that it helps you have a reasonable response rate, which in return helps to improve your sender reputation.

Export the following data from the previous email sender and upload it on your CleverTap dashboard:
  * Email opened users in the last 30/60/90/180 days respectively.
  * Email clicked users in the last 30/60/90/180 days respectively.
  * Suppression lists (unsubscribes, bounces, spam reports). 

For more information, refer to [CSV Upload](https://docs.clevertap.com/docs/csv-upload).

The following is a sample format for uploading the users into CleverTap via a CSV upload based on the previous user engagements. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8219ca0-Historical_data.png",
        "Historical data.png",
        512,
        384,
        "#d5dbca"
      ],
      "sizing": "smart",
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "warning",
  "body": "The emails must be under the *identity* column where:\n* The letter \"i\" has to be lowercase.\n*  *identity* always has to be the first column irrespective of their user properties.",
  "title": "CSV Requirements"
}
[/block]
After you upload the users based on the recency of the users, you can find these details during the email campaign creation in the *Who* step. 

For more information on creating an email campaign, refer to [Email](https://docs.clevertap.com/docs/email).

<< @PM: need a new UI screen >>

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/724be4c-Display_common_properties.png",
        "Display common properties.png",
        512,
        293,
        "#faf6f6"
      ]
    }
  ]
}
[/block]
The following is a sample format on how to upload the suppression list of users.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c2dde94-Sample_format.png",
        "Sample format.png",
        512,
        285,
        "#d8d9b5"
      ]
    }
  ]
}
[/block]
##Warmup Plan Steps
The following shows the steps broken down by days as per your warmup plan, where you should start sending emails to your highly engaged users.
  * Day 1: 100 users.
  * Day 2: 180 users. Don't send emails to the same users from day 1.
  * Day 3: 320 users. Don't send emails to the same users from days 1 and 2.
  * Day 4: 600 users. Don't send emails to the same users from days 1, 2, and 3.
  * Day 5: 1,000 users. Don't send emails to the same users from days 1, 2, 3, and 4.

Follow the same steps for the remaining days of your warmup plan. If the users are unique, we would only require one email template until your overall list is exhausted.

If you plan to send openers from these day sends <<@pm what does day sends mean? >>during the warmup plan, we always have to create new email content not to receive the same email again. <<@pm we meaning users ? or clevertap>>

Use this checklist for your warmup process for a smooth transition:
  * Check for all the links whether they are redirecting to the desired page.
  * Check for all the images whether they are rendering correctly or not.
  * Check for the unsubscribe link whether it is working or not.

##IP Warming Best Practices
Here are some IP warming best practices to consider:
  * Begin with the most active and engaged users (openers/clickers of the past 30, 60, and 90 days respectively).
  * Start by sending a lower volume of emails and then increase the volume each day as gradually as possible.
  * Check that your email list is clean and does not have old or unverified emails.
  * Ensure that your first content is highly engaging and maximizes the likelihood that users click, open, and engage with your email.
  * When the IP warming is complete, continue sending as consistently as possible.
  * Carefully monitor your sender's reputation while you conduct the IP warming process.