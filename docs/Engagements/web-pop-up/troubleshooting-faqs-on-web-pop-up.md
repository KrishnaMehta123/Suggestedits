---
title: 'Web Pop-up: Troubleshooting and FAQs'
excerpt: >-
  In this document, you can explore concise troubleshooting tips and FAQs for
  Web Pop-up Notifications. You can click on each heading to expand sections for
  detailed information.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# FAQs

### Can web pop-ups work on mobile web browsers?

Yes, web pop-ups work on mobile web browsers.

### What is a Webhook Dispatched Failed error?

The *Webhook Dispatched Failed* error occurs when the CleverTap server does not receive a "200 OK" response. A "200 OK" response is an acknowledgment from the REST API server that the API request was received successfully. 

This error can occur in either of the three scenarios:

* When CleverTap sends the payload to your endpoint and we do not receive a "200 OK" response after retrying three times after a wait of 15 seconds. 
* When CleverTap sends the payload and your endpoint health is down.
* When you may receive the payload at your endpoint but not send a "200 OK" response to CleverTap server within the timeout frame of 3 seconds. CleverTap displays a *Webhook Dispatched Failed* error in this case.

As a best practice, we recommend queueing the payload at your end and providing us a "200 OK" in response.

### Does the Web pop-up campaign render an API event?

Web Pop-ups will only render for events raised from the Web SDK. Web Pop-ups are not supported for events raised through API.
