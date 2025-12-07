---
title: Mandrill
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
CleverTap supports sending emails through Mandrill.

# Step 1: Integrating Mandrill into CleverTap
  * In the dashboard, navigate to Settings and click on Integrate Email.
  * Select Mandrill.
  * In the Host text box, fill the host value as smtp.mandrillapp.com.
  * In the Port text box, fill Port value as 587.
  * Fill in the Username value as your Mandrill username.
  * The Password is any valid Mandrill API key.
  * From Address – this value is used as the sender's email address. Most people will not open an email unless they recognize the sender.
  * Save your settings.
  * Finally, click Send a test email and fill in your details to test the configuration details you entered. Has it arrived in your inbox? If not, see the troubleshooting steps below. 

# Step 2: Bounces, Rejections, and Unsubscriptions

When an email is classified as bounced, rejected or when a user unsubscribes, CleverTap needs to be notified so that no further deliveries to that mailbox are attempted. This is considered a good practice and helps improve your sender reputation. Good sender reputation virtually guarantees better delivery rates.
  * In the dashboard, navigate to Go to Settings and click the Webhooks tab.
  * Click on the +Add a Webhook button.
  * As shown in the image below, check the following: Message is Bounced, Message is Rejected, Message Recipient Unsubscribes, and Message is Soft-Bounced.
  * In the Post to URL input box, add the Callback URL as shown in your CleverTap account. You will get from CleverTap Settings -> Email settings page.
  * Save your settings.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2efc6ef-Campaign_Email_Mandrill_Setup.png",
        "Campaign_Email_Mandrill_Setup.png",
        1357,
        723,
        "#f0f1eb"
      ],
      "border": true
    }
  ]
}
[/block]
* In the Mandrill dashboard, navigate to Go to Settings and click the Sending defaults tab.
* As shown in the image below, check the following: Add Unsubscribe Footer
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/39ea47c-mandril.png",
        "mandril.png",
        449,
        260,
        "#edeff1"
      ]
    }
  ]
}
[/block]
# Step 3: Troubleshooting
  * Check whether Mandrill API key used is not restricted by IP address.
  * Check that your Mandrill API key is active.
  * Check your SPAM folder to see if the message has been classified as SPAM by your email provider.