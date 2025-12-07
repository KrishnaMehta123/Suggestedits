---
title: 'SMS: Troubleshooting and FAQs'
excerpt: >-
  Refer to our frequently asked questions and troubleshoot any issues with your
  SMS campaign.
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

This section covers FAQs related to the SMS messaging channel.

#FAQs

##Q. How to unsubscribe a user from receiving SMS promotions?
The [Subscribe API](https://developer.clevertap.com/docs/subscribe-api) allows you to subscribe or unsubscribe a phone number. This is important so that you do not accidentally send an SMS to a phone number unless they have explicitly opted for it. 

##Q. What is a *Profile not reachable* error?
The *Profile not reachable* error occurs when the qualified device is not reachable via the selected communication channel.

In the case of SMS, this error occurs if the profile does not have a phone number or the user has unsubscribed from SMS communication.

##Q. What is a *Duplicate Profile for the channel* error?
This error indicates two different profiles have the same credentials, such as a phone number, a push token, and an email (based on the communication channel). The engagement is sent to the first profile, and this error is sent to the second profile.

##Q. Why some emojis and characters do not appear in my SMS body?
To resolve this issue, ensure your service provider supports sending special characters or emojis in an SMS.

##Q. What is the character limit for SMS?
The limit for a standard SMS is 140 to 160 characters, after which the remainder of the message is sent as a new SMS.

#SMS Error

An SMS error is a common campaign error that occurs while scheduling the SMS campaign. If the SMS service provider’s endpoint is unavailable, the SMS error appears. It applies to generic integrations and MSG91 (SMS provider).

The SMS error shows the following message: 

*Error java.net.SocketTimeoutException: Read timed out for message*. It is referred to as the *SocketTimeoutException* error.

This SMS error occurs when CleverTap sends the SMS payload to the SMS provider’s endpoint, but there is no acknowledgment within 15 seconds. The SMS error appears under the *Technical Errors* category. You can view the errors within the campaign reports under the *Error* section. 


[block:callout]
{
  "type": "info",
  "body": "The issue generally means a socket timeout exception. Sometimes, it can also mean a connection request exception.",
  "title": "Note"
}
[/block]

For other integrated vendors, we have the following equivalent errors: 
* Exotel server error
* Twilio server error
* Gupshup server error
* Netcore service error
* Nexmo SMS error