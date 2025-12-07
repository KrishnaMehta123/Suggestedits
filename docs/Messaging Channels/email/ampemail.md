---
title: AMP For Email_Delete
excerpt: Learn about the AMP feature available in Gmail.
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

AMP (Accelerated Mobile Pages) is a set of standards and open source web components introduced by Google, designed to improve the experience of mobile web browsing by making page load times nearly instantaneous.

[AMP for Email](https://amp.dev/about/email/) brings a subset of the AMP web components and standards to email, allowing a historically static medium to provide interactive, secure, and data-driven experiences.

For example, AMP emails can include forms, carousels, accordions, sidebars, timestamps, and responsive layouts, and the data included in these messages can update in real-time each time they're opened.

> 📘 NOTE
>
> Google created AMP and AMP for Email, but they are open source technologies supported by multiple email providers. For more information, see Email providers, browsers, and clients.

CleverTap supports AMP for Email, which allows you to send interactive, app-like messages that help users accomplish meaningful tasks right from their inboxes—no linking out to external web pages required.

> 🚧 AMP For Email

# When is AMP for Email useful?

AMP for Email has a wide variety of potential applications. For example, AMP emails can allow users to:

* Look at promotional content, flipping through a carousel of on-sale items
* Respond to a discussion thread by filling in a form and submitting it
* Vote on a poll
* Manage subscription preferences at a granular level
* View real-time information about order shipments, flights, events, purchases, etc. This information can update each time the email is opened.
* To get a feel for the types of experiences enabled by AMP for Email, take a look at the Gmail AMP for Email Playground.

# Email providers, browsers, and clients

According to the AMP for Email homepage([https://amp.dev/about/email/#:\~:text=Get%20Started-,Supported,-Email%20Clients](https://amp.dev/about/email/#:~:text=Get%20Started-,Supported,-Email%20Clients)), the following email services can receive and display AMP emails (however, for some of these services, support may be in early beta):

Gmail ([https://developers.google.com/gmail/ampemail/supported-platforms](https://developers.google.com/gmail/ampemail/supported-platforms))\
Mail.ru ([https://postmaster.mail.ru/amp/](https://postmaster.mail.ru/amp/))\
Yahoo mail ([https://senders.yahooinc.com/amp/](https://senders.yahooinc.com/amp/))

> 📘 IMPORTANT
>
> * As a spam prevention and security measure, these providers generally require you to register all email addresses from which you will send AMP email. Similarly, you may need to enable a mailbox setting before you can view AMP content.
> * Be sure to click the above links to read the latest information about the level of AMP for Email support provided by these email services, since it may vary over time.

# What about security?

AMP for Email has several built-in, security-enhancing features:

* Only a subset of AMP components can be used in AMP emails
* Ad components are not allowed
* Third-party features / scripts are not allowed

Additionally, email providers that support AMP generally have their own security requirements. For example, Gmail's Amp for Email Security Requirements([https://developers.google.com/gmail/ampemail/security-requirements](https://developers.google.com/gmail/ampemail/security-requirements)) specify that the email must, among other things, pass DKIM and SPF authentication.

# AMP for Email and CleverTap

To send an AMP email message from CleverTap:

1. Register your sending address with the email providers to which you'll be sending AMP emails. For example, to learn how to send AMP email messages to Gmail, read Tutorial: Configuring CleverTap to Send AMP Email to Gmail.

Design an AMP email message, using tools such as:

AMP for Email Playground ([https://playground.amp.dev/?runtime=amp4email](https://playground.amp.dev/?runtime=amp4email))\
AMP for Email Validator ([https://validator.ampproject.org/#htmlFormat=AMP4EMAIL](https://validator.ampproject.org/#htmlFormat=AMP4EMAIL))\
Gmail AMP for Email Playground ([https://amp.gmail.dev/playground/](https://amp.gmail.dev/playground/))

Use CleverTap to create and send an email campaign as usual. The template editor allows you to specify three types of content for your email:

Plain text content\
HTML content\
AMP for Email HTML

Users whose email provider and client or browser support AMP for Email will see the AMP email content, and other users will see the HTML or plain text content.

You can use CleverTap to track the results of your AMP email campaigns as normal.

# Further Reading

(YouTube) What's New in AMP for Email ([https://www.youtube.com/watch?v=R\_YQB6rLo\_M](https://www.youtube.com/watch?v=R_YQB6rLo_M))\
Tools([https://amp.dev/documentation/tools/?format=email](https://amp.dev/documentation/tools/?format=email)) to help you build AMP emails.

# Configuring CleverTap to Send AMP Email to Gmail

Before you can send AMP emails to Gmail (or Google Apps), you must register each of your sending addresses with Google. This security measure allows Google to verify that you aren't a spammer and that you can be trusted to send dynamic content.

To register a sending address with Gmail, follow the steps in Register With Google to Send Dynamic Emails. At a high level, you'll need to:

Understand and comply with Gmail's registration guidelines\
Send a production AMP email to Google\
Fill out a registration form

> 📘 IMPORTANNT
>
> To send AMP emails from CleverTap, you must use an ESP which supports AMP via SMTP link SendGrid or MailGun. If unsure, please connect with your ESP to check if AMP is supported via SMTP.

## 1. Review Google's Registration Guidlines

To start, review Gmail's Registration Guidelines, and make sure that you can comply with all the requirements.

In particular, note that AMP emails sent to Gmail must be authenticated with SPF, DKIM and DMARC, as mentioned in their Security Requirements. If you have not yet set up these authentications, talk to your CleverTap customer success manager.

## 2. Create, validate and test an AMP email
