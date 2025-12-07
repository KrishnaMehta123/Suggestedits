---
title: Troubleshooting and FAQs
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
[block:api-header]
{
  "title": "Overview"
}
[/block]
This section provides some FAQs, troubleshooting help for your email setup, tips to raise your reputation from poor to good, and IP and domain monitoring. 

#FAQs
## Q. Why does linked content not work in the email builder?
Linked content does not work in the email builder because it is in text format. Linked content is only supported in custom HTML.

## Q. Does the recommendation feature work in the email builder?
No.

## Q. What are the IPs that are used to send out the emails?
To get the IPs, perform the following steps:
1. From the dashboard, navigate to *Settings* > *Channels* > *Mobile Push*.
[block:callout]
{
  "type": "info",
  "body": "The IPs are the same for webhooks, SMS, and emails.",
  "title": "Same IPs"
}
[/block]


# Troubleshooting 


## 1. I received the error message: "Please set the email credentials." How do I fix it?
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e527565-Screen_Shot_2018-07-15_at_8.40.27_PM.png",
        "Screen Shot 2018-07-15 at 8.40.27 PM.png",
        519,
        256,
        "#f3f4f6"
      ],
      "border": true
    }
  ]
}
[/block]
This error message means you have not integrated your email provider with CleverTap. You can do this by following [this guide](doc:email-partners).

## 1. Raise your reputation from poor to good
Monitoring your domain health is an ongoing process that requires consistent nurturing. Your sending reputation is a decisive factor when it comes to the delivery of your emails. By complying with permission policies and best practices and carefully monitoring your email list performance, you will be well-positioned to develop and maintain a robust sending reputation.

Take the steps below to improve your domain and IP reputation.

## 2. Prime your IP for success
The job of ISP filters is to defend against spam emails. How do you tell these filters that your IP is valid and trustworthy? Start any email campaign by sending small batches of emails. Send these messages to email addresses that you know are engaged. As these emails are received and opened by engaged users, your IP will build trust with the ISP. Slowly increase the number of emails until you scale to your peak volume.

## 3. Create a new subdomain 
We do not recommend everyone to create a new subdomain, but you may wish to create one if possible. Over time, users will come to trust the subdomain, which is an added benefit. The purpose is that this subdomain will allow for domain-specific monitoring of your IP reputation and succeed against some domain-based certification filters.

To add a new subdomain in SendGrid, perform the following steps:
1. Log in to your SendGrid account and navigate to the *Settings* section.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/46f1e01-1_Settings.png",
        "1 Settings.png",
        182,
        207,
        "#f0f6f4"
      ],
      "border": true
    }
  ]
}
[/block]
2. Click **Sender Authentication**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/06c6adc-2_Sender_Authentication.png",
        "2 Sender Authentication.png",
        180,
        360,
        "#f6f7f9"
      ],
      "border": true
    }
  ]
}
[/block]
3. Click **Authenticate Your Domain** under *Domain Authentication*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/242cfc9-3_Authenticate_Your_Domain.png",
        "3 Authenticate Your Domain.png",
        424,
        328,
        "#f6f7f8"
      ],
      "border": true
    }
  ]
}
[/block]
4. Select the name of your DNS host provider.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2ce2a25-4_name_of_your_DNS_host_provider.png",
        "4 name of your DNS host provider.png",
        873,
        513,
        "#f7f8f9"
      ],
      "border": true
    }
  ]
}
[/block]
5. In the second option on the same page, choose if you want the link branding or not and click **Next**.
6. Fill in the name of the domain/subdomain from which you wish to send your email campaigns. 
7. Select the *Use automated security* option in the *Advanced Settings* section and click **Next**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b395e61-5_Next.png",
        "5 Next.png",
        502,
        524,
        "#f4f6f8"
      ],
      "border": true
    }
  ]
}
[/block]
8. The next screen will provide you the records which will be required to be updated on the DNS settings page of your domain host name provider.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3928608-6_records.png",
        "6 records.png",
        1106,
        484,
        "#fbfbfc"
      ],
      "border": true
    }
  ]
}
[/block]
9. Once the provided records have been updated on the DNS settings page, click on the checkbox in the bottom right corner along with the option *I've added these records* and click **Verify**.

This step will verify that the correct records are added to the domain DNS. Once the verification is complete, the added domain is listed on the *Sender Authentication* page and is ready for use. If the verification fails, check if the records have been added to the DNS correctly and repeat the previous verification steps.