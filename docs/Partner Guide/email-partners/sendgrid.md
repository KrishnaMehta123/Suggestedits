---
title: SendGrid
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
CleverTap supports sending emails through SendGrid. 

# Integrate SendGrid with CleverTap

1. In the dashboard, navigate to Settings > Engage > Channels > Email. 
2. Click the + Provider button. The Provider credentials page appears.
3. Select SendGrid from the provider list.
4. Provide a nickname for your integration.
5. Enter the SendGrid API key. For more information on generating the key, see [Creating an API key in SendGrid](https://sendgrid.com/docs/ui/account-and-settings/api-keys/#creating-an-api-key).
   > 🚧 Note
   >
   > As of December 2020, SendGrid only requires an API key for authentication. Username and password are no longer needed.
   >
   > For any clarifications, contact your SendGrid Account Executive or SendGrid Support.
6. From Address – This value is used as the sender's email address. Most people will not open an email unless they recognize the sender.
7. Reply Address - This value is used as the reply address. You can receive replies to this address.
8. Save your settings.
9. Finally, click Send a test email and fill in your details to test the configuration details you entered. Has it arrived in your inbox? If not, see the troubleshooting steps below.

> 🚧 Note
>
> If you are using SendGrid credentials with SMTP integration, then enter **apikey** as username and \<API\_KEY\_VALUE> as password.

# Bounces, Rejections, Unsubscriptions, and Spam

When an email is classified as bounced, rejected, or when a user unsubscribes, or it is marked as spam, CleverTap needs to be notified so that no further deliveries to that mailbox are attempted. This is considered a good practice and helps improve your sender's reputation. Good sender reputation virtually guarantees better delivery rates.

To enable support for these, follow the steps:

1. Navigate to *Settings* > *Email* Settings and enable Event Notification.

2. Navigate to Settings from within Event Notification.

3. In the HTTP Post URL input box, add the Callback URL from the CleverTap dashboard from *Settings* > *Email* > *Provider* > *Sendgrid*.\[block:image]\{"images":\[\{"image":["https://files.readme.io/39730b0-SendGrid_Email_Provider.png",null,""],"align":"center","border":true}]}\[/block]

4. Check the following from the Select Options menu in SendGrid Dashboard– Dropped, Bounced, Unsubscribed From, and  Marked as Spam.

5. Save your settings.

<Image title="Enable event notifications for emails via SendGrid" alt={669} align="center" border={true} src="https://files.readme.io/c7c968d-Email_Sendgrid_Settings.png">
  Enable Event Notifications for Emails via SendGrid
</Image>

**Notes**

* When an email bounces, drops, or unsubscribes, CleverTap will mark the user’s email address as inactive.
* The count of email bounces is shown on the email report screen.

# Troubleshooting

Check your SPAM folder to see if the message has been classified as SPAM by your email provider.
