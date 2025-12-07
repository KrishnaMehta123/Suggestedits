---
title: 'Webhook: Troubleshooting and FAQs'
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
# FAQS

## Q. What is a Webhook Dispatched Failed error?

The _Webhook Dispatched Failed_ error occurs when the CleverTap server does not receive a "200 OK" response. A "200 OK" response is an acknowledgment from the REST API server that the API request was received successfully. 

This error can occur in either of the following three scenarios:

- CleverTap sends the payload to your endpoint, but you do not receive a "200 OK" response after retrying three times after a wait of 15 seconds.  
- CleverTap sends the payload, but your endpoint health is down.
- You may receive the payload at your endpoint but not send a "200 OK" response to the CleverTap server within the timeout frame of 3 seconds. CleverTap displays a _Webhook Dispatched Failed_ error in this case.

As a best practice, we recommend queueing the payload at your end and providing us with a "200 OK" in response.

## Q. What is a Webhook Dispatched Failed error?

The _Webhook Dispatched Failed_ error occurs when the CleverTap server does not receive a "200 OK" response. A "200 OK" response is an acknowledgment from the REST API server that the API request was received successfully. 

This error can occur in either of the three scenarios:

- When CleverTap sends the payload to your endpoint and we do not receive a "200 OK" response after retrying three times after a wait of 15 seconds. 
- When CleverTap sends the payload and your endpoint health is down.
- When you may receive the payload at your endpoint but not send a "200 OK" response to CleverTap server within the timeout frame of 3 seconds. CleverTap displays a _Webhook Dispatched Failed_ error in this case.

As a best practice, we recommend queueing the payload at your end and providing us a "200 OK" in response.