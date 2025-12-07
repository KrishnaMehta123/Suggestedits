---
title: 'Email: Troubleshooting and FAQs'
excerpt: >-
  Refer to our frequently asked questions and troubleshoot any issues with your
  Email campaign.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Overview

This section provides FAQs, troubleshooting help for your email setup, tips to raise your reputation from poor to good, and IP and domain monitoring. 

#FAQs
## Q. Does linked content work in the email builder?
Yes. To know more, refer to [Linked Content](doc:personalize-message-email#linked-content).

## Q. Does the recommendation feature work in the email builder?
Yes. To know more, refer to [Email Recommendations](doc:create-campaigns-using-recommendations#email-campaigns-with-recommendations).

## Q. What IPs does CleverTap use to send out emails?
To view the IPs:
1. Navigate to *Settings* > *Channels* > *Email* from the dashboard. 
2. In the *Providers* tab, refer to the *Additional security* note at the top highlighting the IPs.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/213bdfe-Providers.png",
        "Providers.png",
        1422,
        788,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]




[block:callout]
{
  "type": "info",
  "body": "These IPs are common for webhooks, SMS, and emails.",
  "title": "Common IPs"
}
[/block]

## Q. Why is my unsubscribe count lower than expected?
This is because the unsubscribe count is updated when a user unsubscribes from email communications overall and not to only specific subscription group(s). You can check the dashboard for users unsubscribed from specific subscription groups by searching for them on the [Find People](doc:find-people) page. Search for users by the *Channel Unsubscribed* event and filter by event property *Group*. 

##Q. How do you handle unsubscribes and bounce for callbacks, such as Mandrill or SendGrid?
CleverTap must be notified for any email classified as bounced, rejected, spam, or unsubscriptions by the user so that we do not attempt any further deliveries to their mailboxes.

For more information, refer to [SendGrid Bounces, Rejections, and Unsubscriptions](doc:sendgrid#section-step-2-bounces-rejections-and-unsubscriptions) and [Mandrill Bounces, Rejections, and Unsubscriptions](doc:mandrill#handle-bounce-rejection-spam-and-unsubscriptions).

A service provider tracks any user unsubscribes using the unsubscription link in your email. The service provider then sends this information to CleverTap through the callback URL. 

The communication preference for users is marked as false (MSG_Email=False). 
Hard-bounced and unsubscribed users both fall under unsubscription. Follow the steps below to find the number of users who have unsubscribed via email:

1. Navigate to *Segments* > *Find People*. 
2. From the *Display* common properties, select *Reachability* > *Unsubscribed* > *Yes*.

##Q. How do you annotate an email?
Email annotations in the *Promotions* tab bring email messages to life with images, deals, expiration dates, and more. The email annotation can be performed in the drag-and-drop email editor and also in the custom HTML email editor.

Use the <meta> tag in the drag-and-drop editor to annotate an email. Following is the sample code that can be used in the HTML block of the drag-and-drop editor:



[block:code]
{
  "codes": [
    {
      "code": "<p>\n<div itemscope itemtype=\"http://schema.org/Organization\">\n\n<meta itemprop=\"logo\" content=\"https://www.gstatic.com/images/branding/product/1x/googleg_48dp.png\" />\n\n</div>\n\n<div itemscope itemtype=\"http://schema.org/DiscountOffer\">\n\n<meta itemprop=\"description\" content=\"40% off\" />\n\n<meta itemprop=\"discountCode\" content=\"DISCOUNTCODE\" />\n\n<meta itemprop=\"availabilityStarts\" content=\"2020-03-20T08:00:00-07:00\" />\n\n<meta itemprop=\"availabilityEnds\" content=\"2020-03-21T23:59:59-07:00\" />\n\n</div>\n\n<div itemscope itemtype=\"http://schema.org/PromotionCard\">\n\n<meta itemprop=\"image\" content=\"https://gmail-ads-markup-test.sandbox.google.com/sample.png\" />\n\n</div> This is metadata in HTML block of drag and drop editor</p>\n",
      "language": "html"
    }
  ]
}
[/block]

For custom HTML implementation, refer to [Get started: How to annotate your email](https://developers.google.com/gmail/promotab/overview) in the Google documentation. The *Promotions* tab capability works in custom HTML with both inline microdata and the script tag.

When you test this feature, check the following:

* The target audience email addresses are not GSuite emails.
* The availability start date must be far apart from the end date. If the values of the start date and end date are closer to the current date, then the mail is most likely to appear in the *Top Picks* of the *Promotions* tab.

##Q. How do you add custom fonts in email?
You need the CleverTap custom HTML builder for your email campaigns.

You can add custom fonts to emails by adding a link tag to the header of your email HTML. It means the font must be hosted somewhere on the internet. Following is an example:


[block:code]
{
  "codes": [
    {
      "code": "<html>\n<head>\n    <link href=\"https://fonts.googleapis.com/css?family=Roboto\" rel=\"stylesheet\" type=\"text/css\" />\n</head>\n<body>\n<h1 style=\"font-family:'Roboto'\">Test text</h1>\n</body>\n</html>\n",
      "language": "html"
    }
  ]
}
[/block]

Custom fonts may not be supported by all email clients. If you are adding a custom font to emails, you may also want to specify fallback fonts. This ensures the latter font is picked up if the first font is unavailable. 

Following is an example:


[block:code]
{
  "codes": [
    {
      "code": "<h1 style=\"font-family: Lato, 'Lucida Grande', Tahoma, Sans-Serif;\">Welcome</h1>\n\n",
      "language": "html"
    }
  ]
}
[/block]


##Q. What does the *Do not stack on mobile devices* mean?  
Do not stack on mobile devices alerts you that it will disable the resizing and repositioning of the content per the device screen width. 

**With Stacking on Mobile**




[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8ed477f-campaigns_email_Stack_images.png",
        "campaigns_email_Stack_images.png",
        1080,
        1683,
        "#ecedee"
      ],
      "sizing": "full",
      "border": true
    }
  ]
}
[/block]

**Without Stacking on Mobile**




[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/de9274d-campaigns_email_Not_Stack_images.png",
        "campaigns_email_Not_Stack_images.png",
        1080,
        1120,
        "#e2e4e5"
      ],
      "border": true,
      "sizing": "full"
    }
  ]
}
[/block]


##Q. How do you add a GIF file in an email?
You can add a GIF file using the content field image or custom HTML by following the steps below:

1. Select the *New Email with drag and drop* template. 
2. From the *Content* tab, click **Image**. 
3. Drag and drop the image icon in the email body. 
3. Click **Browse**.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/76f72c9-New_final_GIF_file_Browse.png",
        "New final GIF file Browse.png",
        1322,
        544,
        "#fafafb"
      ],
      "caption": ""
    }
  ]
}
[/block]

4. Click **Upload** and select your GIF file.
5. In the *File manager*, find your GIF file and click **Insert**.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e6d322e-New_file_GIF_file_Upload.png",
        "New file GIF file Upload.png",
        1318,
        547,
        "#eeedf3"
      ]
    }
  ]
}
[/block]




[block:callout]
{
  "type": "info",
  "title": "Note",
  "body": "* Images/GIFs must be less than 5 MB; however, we recommend the media must be less than 1 MB for optimal results. The media may not load in the user's inbox because all your users may not have a high-speed internet connection.\n* The media formats supported are JPEG, GIF, and MP4."
}
[/block]

##Q. Can I integrate an email provider that is not listed in documents?
Yes, you can use Generic SMTP to integrate any email provider of your choice. For more information, refer to [Generic SMTP](https://docs.clevertap.com/docs/generic-smtp).

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

## 2. Raise your reputation from poor to good
Monitoring your domain health is an ongoing process that requires consistent nurturing. Your sending reputation is a decisive factor when it comes to the delivery of your emails. By complying with permission policies and best practices and carefully monitoring your email list performance, you will be well-positioned to develop and maintain a robust sending reputation.

Take the steps below to improve your domain and IP reputation.

## 3. Prime your IP for success
The job of ISP filters is to defend against spam emails. How do you tell these filters that your IP is valid and trustworthy? Start any email campaign by sending small batches of emails. Send these messages to email addresses that you know are engaged. As these emails are received and opened by engaged users, your IP will build trust with the ISP. Slowly increase the number of emails until you scale to your peak volume.

## 4. Create a new subdomain 
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