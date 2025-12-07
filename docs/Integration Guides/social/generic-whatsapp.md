---
title: Generic WhatsApp
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
# Overview
CleverTap has opened its platform for all WhatsApp providers by creating open APIs and standard callback formats. Now providers can integrate these APIs with their platform and get themselves added as a supported partner for the WhatsApp channel in the CleverTap dashboard. 
[block:callout]
{
  "type": "info",
  "body": "Customers can only use the providers available in the list of integrated partners provided below. If customers don't find the partner of their choice, they can share this documentation with their partner and ask the partner to integrate with CleverTap APIs for the WhatsApp channel.",
  "title": "Feature Availability"
}
[/block]
# List of Integrated Partners

[block:callout]
{
  "type": "info",
  "title": "Note",
  "body": "Providers interested in pursuing the partnership must complete the integration steps listed in this document and write to [partner-integrations@clevertap.com](mailto:partner-integrations@clevertap.com) and [integrations@clevertap.com](mailto:integrations@clevertap.com) to get your name added to this list."
}
[/block]
# Partner Acceptance Criteria
Any WhatsApp partner can integrate with our open APIs, but to get added to the list of integrated partners, they need to share the following with CleverTap:
  * Production API endpoint for sending Template and Freeform notifications via single endpoint
  * Production API credentials for two test accounts so the CleverTap team can test the integration.
  * Providers need to provide dashboard access where the CleverTap team can create the templates or share approved templates to test the campaign flow.
  * Providers need to add CleverTap's callback URL in the test accounts so that CleverTap can ensure that callbacks are received in the correct format.
  * Providers must publish a CleverTap integration guide in their user docs so that CleverTap can link it with the user document.
  * Partners must provide the contact details of their dedicated support and product team so that CleverTap can reach out to them in case of any issues.

#  Integration steps
Customers need to get endpoint and authentication details from BSP.
[block:callout]
{
  "type": "info",
  "body": "* **For customers**\nBSPs might have a dedicated endpoint(different from their standard endpoint) for CleverTap integration, so you need to explicitly mention to your provider that you need the API details for CleverTap integration.\n\n* **For BSPs:**\nBSPs must provide API endpoints and credentials that have been tested and work with Clever CleverTap platform.",
  "title": "Custom Endpoint"
}
[/block]
To get started with generic integration, BSP integrating with CleverTap must share the API endpoint and authentication details with customers. BSPs must ensure that they provide the endpoint that can process the payload being sent by CleverTap. After the customers have API details handy, proceed as follows:

1. Navigate to *Settings* > *Channels* > *WhatsApp* and select **Other(Generic)** from the *Provider* dropdown list. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9e5acb0-WA_generic_1.png",
        "WA generic 1.png",
        1604,
        1532,
        "#f4f6f9"
      ]
    }
  ]
}
[/block]
2. Enter the API endpoint and auth details to save the endpoint.
[block:callout]
{
  "type": "info",
  "body": "CleverTap sends the following sample payload to validate the credentials before saving the provider details. BSPs need to provide a “200 OK“ response along with the following response if API credentials are correct",
  "title": "Provider Verification"
}
[/block]
**Expected API Response** 
[block:code]
{
  "codes": [
    {
      "code": "{\n    \"status\": \"success\"\n}",
      "language": "json"
    }
  ]
}
[/block]
**Sample Credential Validation Payload** 
[block:code]
{
  "codes": [
    {
      "code": "{\n    \"payloadVersion\": 0.1,\n    \"wabaNumber\": $$WABAnumber,\n    \"to\": \"+919870369294\",\n    \"isTemplate\": true,\n    \"template\": {\n      \"namespace\": \"whatsapp:hsm:technology:generic:verify\",\n      \"languageCode\": \"en\"\n    },\n    \"components\": [\n      {\n        \"type\": \"body\",\n        \"body\": {\n          \"text\": \"1 code: 2.Valid for 3 minutes.\",\n          \"parameters\": [\n            {\n              \"type\": \"text\",\n              \"text\": \"1\"\n            },\n            {\n              \"type\": \"text\",\n              \"text\": \"2\"\n            },\n            {\n              \"type\": \"text\",\n              \"text\": \"3\"\n            }\n          ]\n        }\n      }\n    ],\n    \"msgId\": \"0|0|0|0\"\n  }",
      "language": "json"
    }
  ]
}
[/block]
3. Customers need to copy both delivery report callbacks and IMO callback URLs and get these callbacks configured with the WhatsApp provider. Providers need to send the callbacks in the format specified later in this document. Any format, other than our expected callback, will not be accepted. This results in campaign stats not being populated and incoming messages not showing up in the CleverTap dashboard.

4. After the credentials are stored, customers can save the approved templates under the template section to start sending WhatsApp notifications in the approved template formats. 
[block:callout]
{
  "type": "info",
  "body": "CleverTap sends a sample payload according to the template being saved in the dashboard. BSPs need to validate the payload and return **200 OK response** if all the details are as per approved templates.",
  "title": "Template Verification"
}
[/block]
5. After the templates are saved, you can navigate to the *Campaigns* and start creating campaigns.

If the end-customers reply to notifications sent from CleverTap, incoming messages appear under the Conversation section of the dashboard. Businesses can reply to incoming messages by selecting the chat.

## API Endpoint
BSPs are requested to create an endpoint where CleverTap can send the notification payload for campaigns and free form messages. Customers should ask BSPs to share the API endpoint that can accept the CleverTap Payload to save the provider in CleverTap Dashboard.

## API Authentication 
The CleverTap's REST API supports basic authentication or custom headers for authentication. Partners must share these credentials with customers and customers will save these credentials with an endpoint.

# Send message API Specifications

CleverTap has categorized outbound message payloads into 2 categories. 
* Templates messages
* Freeform messages 

CleverTap sends either of the payloads depending on the type of message sent by the dashboard user. CleverTap sends key `isTemplate` to help BSPs understand whether this is templatized message or a freeform message.
[block:callout]
{
  "type": "info",
  "body": "CleverTap does not support different endpoints for different types of messages, so BSPs need to provide just one endpoint to process freeform and template messages.",
  "title": "Single Endpoint"
}
[/block]
## API Payload for Template Message
CleverTap sends this payload for sending the template message notification.
The outgoing template message payload can be broken down into the following three sections:
  * User & notification information
  * Template information that includes template name, namespace, template language, etc. 
  * Content information
[block:callout]
{
  "type": "info",
  "body": "The message payload is encoded into UTF-8 (Unicode Transformation Format) before being sent to the provider's endpoint. \n\nValues with $$ ($$To,$$BusinessWabaNumber) are dynamic values and change for each request.\n\nCleverTap does not support templates with contacts currently, so contact objects are not sent with payload.\n\nCleverTap does not support Name, Address, or URL key in location object.\n\n`msg_id` is a unique parameter for each message sent from CleverTap and must be present in callbacks sent by BSP to CleverTap.",
  "title": "Payload Essentials"
}
[/block]

[block:code]
{
  "codes": [
    {
      "code": "{\n    \"payloadVersion\": $$payloadVersion,\n    \"to\": \"$$to\", // suppport numbers with + and without +(eg. 91 and +91)\n    \"wabaNumber\": \"$$businessWabaNumber\",\n    \"isTemplate\": true,\n    \"msgId\": \"i|campaignID|batchID|j|campaign_variant\", // upto 60 characters\n    \"template\": {\n        \"namespace\": \"$$templateNamespace\",\n        \"languageCode\": \"$$BSPsr-language-and-locale-code\"\n    },\n    \"components\": [\n        //There will be either just one header object or no header object present in the payload depending on the template being saved/used. \n        { // optional media header\n            \"type\": \"header\",\n            \"header\": {\n                \"type\": \"text\",\n                \"text\": {\n                    \"text\": \"$headertext\",\n                    \"parameters\": [\n                        {\n                            \"type\": \"text\",\n                            \"text\": \"$$PlaceholderText1\"\n                        }\n                    ]\n                }\n            }\n        },\n        { // optional media header\n            \"type\": \"header\",\n            \"header\": {\n                \"type\": \"image/video\",\n                \"image/video\": {\n                    \"mediaURL\": \"$$mediaUrl\"\n                }\n            }\n        },\n        { // optional document header\n            \"type\": \"header\",\n            \"header\": {\n                \"type\": \"file\",\n                \"file\": {\n                    \"mediaURL\": \"$$mediaUrl\",\n                    \"filename\": \"$$filename\"\n                }\n            }\n        },\n        { // optional location header\n            \"type\": \"header\",\n            \"header\": {\n                \"type\": \"location\",\n                \"location\": {\n                    \"longitude\": \"$$longitude\",\n                    \"latitude\": \"$$longitude\"\n                }\n            }\n        },\n        {\n            \"type\": \"body\",\n            \"body\": {\n                \"text\": \"$$Body\",\n                \"parameters\": [\n                    {\n                        \"type\": \"text\",\n                        \"text\": \"$$PlaceholderText1\"\n                    },\n                    {\n                        \"type\": \"text\",\n                        \"text\": \"$$PlaceholderText2\"\n                    }\n                ]\n            }\n        },\n        {// optional.. will be present in payload if templates have a footer text\n            \"type\": \"footer\",\n            \"footer\": \"$$footertext\"\n        },\n        {// Dynamic URL CTA (optional)\n            \"type\": \"button\",\n            \"index\": $$buttonPosition,\n            \"subType\": \"dynamicUrl\",\n            \"buttonText\": \"$$cta_text\",\n            \"parameters\": [\n                {\n                    \"type\": \"text\",\n                    \"text\": \"$$suffixURL\"\n                }\n            ]\n        },\n        {//static URL CTA (optional)\n            \"type\": \"button\",\n            \"index\": $$Buttonposition,\n            \"buttonText\": \"cta_text\",\n            \"subType\": \"staticUrl\",\n            \"parameters\": [\n                {\n                    \"type\": \"text\",\n                    \"text\": \"$$ButtonURL\"\n                }\n            ]\n        },\n        {// quick reply buttons (optional)\n            \"type\": \"button\",\n            \"index\": $$buttonPosition,\n            \"subType\": \"quickReply\",\n            \"buttonText\": \"$$cta_text\",\n            \"parameters\": [\n                {\n                    \"type\": \"payload\",\n                    \"payload\": \"$$buttonPayload\"\n                }\n            ]\n        },\n        {// call phone CTA (optional)\n            \"type\": \"button\",\n            \"index\": $$buttonPosition,\n            \"subType\": \"callPhone\",\n            \"buttonText\": \"$$cta_text\",\n            \"parameters\": [\n                {\n                    \"type\": \"text\",\n                    \"text\": \"$$phonenumber\"\n                }\n            ]\n        }\n    ]\n}",
      "language": "json",
      "name": "Template Message Payload"
    }
  ]
}
[/block]
### Postman Collection
https://www.getpostman.com/collections/5c34a2e3ffd06b7c6492 
### Payload key-value description
[block:parameters]
{
  "data": {
    "h-0": "Key name",
    "h-1": "Description",
    "h-2": "Sample values",
    "h-3": "Sample values",
    "0-0": "payloadVersion",
    "0-1": "A version of the payload being sent",
    "0-2": "0.1",
    "1-0": "to",
    "1-1": "Targeted user’s phone number",
    "1-2": "9199XXXXXXXX/ +9199XXXXXXXX",
    "2-0": "wabaNumber",
    "2-1": "Business’s WABA number (from number)",
    "2-2": "9189XXXXXXXX",
    "3-0": "isTemplate",
    "3-1": "Used to highlight the whether the payload being sent is for templates or freeform",
    "3-2": "true/false (Boolean)",
    "4-0": "msgId",
    "4-1": "Unique identifier for a message sent and expected to be present in DLR status callback payloads",
    "4-2": "25596363|1639561857|20220227|25596363",
    "5-0": "template.namespace",
    "5-1": "Template name/namespace.",
    "5-2": "Namespace/name",
    "6-0": "template.languageCode",
    "6-1": "Template language code as defined by Facebook in the below doc.\n[Message Templates - WhatsApp Business On-Premises API - Documentation - Facebook for Developers ](https://developers.facebook.com/docs/whatsapp/api/messages/message-templates/#supported-languages",
    "6-2": "en(uk)",
    "7-0": "components.type",
    "7-1": "Type of component object",
    "7-2": "header/body/buttons",
    "8-0": "Components.header.type",
    "8-1": "Type of header object",
    "8-2": "text/audio/image/video/file/location",
    "9-0": "Components.header.text.text",
    "9-1": "Header text",
    "9-2": "“This is header text”",
    "10-0": "Components.header.text.parameters[X].text",
    "10-1": "Personalization variables sent as an array of objects",
    "10-2": "\"john\"",
    "11-0": "Components.header.audio.mediaURL",
    "11-1": "Media URL of the file",
    "11-2": "www.example.com/audio.mp3",
    "12-0": "Components.header.file.filename",
    "12-1": "Title of the file",
    "12-2": "“sample_document.pdf”",
    "13-0": "Components.header.video.mediaURL  | Type= header",
    "13-1": "Media URL of the file",
    "13-2": "www.example.com/video.mp4",
    "14-0": "Components.header.location.lattitude",
    "14-1": "Latitude of the location shared",
    "14-2": "2.457476548",
    "15-0": "Components.parameters.location.longitude",
    "15-1": "Longitude of the location shared",
    "15-2": "1.565867657",
    "16-0": "Components.body",
    "16-1": "Message body",
    "16-2": "“This is message body”",
    "17-0": "Components.body.parameters[x].text",
    "17-1": "Personalization variables sent as an array of objects",
    "17-2": "\"john\"",
    "18-0": "Components.index |type = buttons",
    "18-1": "Position of the buttons",
    "18-2": "0/1/2",
    "19-0": "Components.subtype |type = buttons",
    "19-1": "Type of button",
    "19-2": "static_url/ Quickreply/call_phone/dynamic_url",
    "20-0": "Components.parameters.text |type = buttons",
    "20-1": "Url suffix for dynamic URL CTA",
    "20-2": "/home",
    "21-0": "Components.parameterss.payload |type = buttons",
    "21-1": "Quick reply button identifier. Same value needs to be returned with incoming message callback URL if someone clicks on the button.",
    "21-2": "“25596363|click“",
    "22-0": "Components.buttonText",
    "22-1": "Button text",
    "22-2": "“visit home page“",
    "23-0": "Components.footer",
    "23-1": "Footer text",
    "23-2": "“This is footer”"
  },
  "cols": 3,
  "rows": 24
}
[/block]
### Payload Samples for Template Message 
[block:code]
{
  "codes": [
    {
      "code": "{\n\"payloadVersion\":0.1,\n\"to\": \"919999999999\",\n\"wabaNumber\": \"91999999XXXX\",\n\"isTemplate\": true,\n\"msgId\": \"25596363|1639561857|20220227|25596363\",\n\"template\": {\n             \"namespace\": \"Namespace:sample\",\n             \"languageCode\":\"en(uk)\"\n                         \n                         },\n\"components\": [\n\n{\n \"type\": \"body\",\n \"body\": {\n \"text\":\"This is sample body\",\n  \"parameters\": [\n               {\n                  \"type\": \"text\",\n                   \"text\": \"Sample\"\n               }\n           ]}},\n  {\n  \"type\": \"footer\",\n  \"footertext\":\"this is footer\"\n        \n       }\n]}",
      "language": "json",
      "name": "Text Template with Footer"
    },
    {
      "code": "{\n    \"payloadVersion\": 0.1,\n    \"to\": \"919999999999\",\n    \"wabaNumber\": \"919999999999\",\n    \"isTemplate\": true,\n    \"msgId\": \"i|campaignID|batchID|j\",\n    \"template\": {\n        \"namespace\": \"Namespace:sample\",\n        \"languageCode\": \"en\"\n    },\n    \"components\": [\n        {\n            \"type\": \"header\",\n            \"header\": {\n                \"type\": \"image\",\n                \"image\": {\n                    \"mediaURL\": \"httpa://www.example.com/image.png\"\n                }\n            }\n        },\n        {\n            \"type\": \"body\",\n            \"body\": {\n                \"text\": \"This is sample body\",\n                \"parameters\": [\n                    {\n                        \"type\": \"text\",\n                        \"text\": \"sample\"\n                    }\n                ]\n            }\n        },\n        {\n            \"type\": \"button\",\n            \"index\": 0,\n            \"subType\": \"dynamicUrl\",\n            \"buttonText\": \"Sample CTA TEXT\",\n            \"parameters\": [\n                {\n                    \"type\": \"text\",\n                    \"text\": \"https://www.example.com\"\n                }\n            ]\n        }\n    ]\n}",
      "language": "json",
      "name": "Image Template with  Dynamic URL CTA buttons"
    }
  ]
}
[/block]
##  API Payload for Freeform Message
CleverTap will send this payload for sending the Freeform message notification.
Freeform message API payload has the user information about the targetted users, media URLs, and text. 
[block:callout]
{
  "type": "info",
  "body": "* Values with $$ (for example $$To,$$BusinessWabaNumber) are dynamic values and change for each request.\n \n  * Dynamic Reply Button, interactive lists, and product catalog, contacts, and locations are not currently supported in the CleverTap platform. This is why these objects are not mentioned in the payload.\n  \n  * CleverTap does not support Name, Address, or URL key in location object.\n \n  * `msg_id` is a unique parameter for each message sent from CleverTap and must be present in callbacks sent by BSP to CleverTap.",
  "title": "Payload Essentials"
}
[/block]

[block:code]
{
  "codes": [
    {
      "code": "{\n    \"payloadVersion\": $$payloadversion,\n    \"to\": \"$$To\",\n    \"wabaNumber\": \"$$BusinessWabaNumber\",\n    \"msgId\": \"i|campaignID|batchID|j\",\n    \"type\": \"text/audio/file/image/location/video\",\n    \"isTemplate\": false,\n    //Optional \n    \"audio\": {\n        \"mediaURL\": \"$$mediaUrl\"\n    },\n    //OR\n    \"file\": {\n        \"mediaURL\": \"$$mediaUrl\",\n        \"caption\": \"$$body\",\n        \"filename\": \"$$filename\"\n    },\n    //OR\n    \"image\": {\n        \"mediaURL\": \"$$mediaUrl\",\n        \"caption\": \"$$body\"\n    },\n    //OR\n    \"text\": {\n        \"body\": \"$$Body\"\n    },\n    //OR\n    \"video\": {\n        \"mediaURL\": \"$$mediaUrl\",\n        \"caption\": \"$$body\"\n    }\n}",
      "language": "json",
      "name": "Freeform Message Payload"
    }
  ]
}
[/block]
### Payload Description
[block:parameters]
{
  "data": {
    "h-0": "Key name",
    "h-1": "Description",
    "h-2": "Sample values",
    "0-0": "to",
    "0-1": "Targeted user’s phone number",
    "0-2": "9199XXXXXXXX",
    "1-0": "\"payloadversion\"",
    "1-1": "Version of the payload being sent to CleverTap",
    "1-2": "0.1",
    "2-0": "wabaNumber",
    "2-1": "Business’s WABA number",
    "2-2": "9189XXXXXXXX",
    "3-0": "isTemplate",
    "3-1": "Used to highlight the whether the payload being sent is for templates or freeform",
    "3-2": "true/false",
    "4-0": "msgId",
    "4-1": "Unique identifier for message being sent and expected to be present in callback payloads",
    "4-2": "25596363|1639561857|20220227|25596363",
    "5-0": "audio.mediaURL",
    "5-1": "Media URL of the file",
    "5-2": "www.example.com/audio.mp3",
    "6-0": "file.mediaURL",
    "6-1": "Media URL of the file",
    "6-2": "www.example.com/document.pdf",
    "7-0": "file.caption",
    "7-1": "Message body",
    "7-2": "“This is message body”",
    "8-0": "file.filename",
    "8-1": "Title of the file",
    "8-2": "“sample_document.pdf”",
    "9-0": "image.mediaURL",
    "9-1": "Media URL of the file",
    "9-2": "www.example.com/image.png",
    "10-0": "image.caption",
    "10-1": "Message body",
    "10-2": "“This is message body”",
    "11-0": "video.mediaURL",
    "11-1": "Media URL of the file",
    "11-2": "www.example.com/video.mp4",
    "12-0": "video.caption",
    "12-1": "Message body",
    "12-2": "“This is message body”"
  },
  "cols": 3,
  "rows": 13
}
[/block]
### Payload Samples For Freeform Message Template 
[block:code]
{
  "codes": [
    {
      "code": "{\n\"payloadVersion\":0.1,\n\"to\": \"919999999999\",\n“msg_id”:\"25596363|1639561857|20220227|25596363\",\n\"wabaNumber\": \"91999999XXXX\",\n\"type\": \"audio\",\n\"isTemplate\": false,\n\"audio\": {\n        \"mediaURL\": \"www.example.com/audio.mp3\"\n        }\n        }",
      "language": "json",
      "name": "Message Template with Audio"
    },
    {
      "code": "{\n\"payloadVersion\":0.1,\n\"to\": \"919999999999\",\n\"wabaNumber\": \"91999999XXXX\",\n“msg_id”:\"25596363|1639561857|20220227|25596363\",\n\"type\": \"image\",\n\"isTemplate\": false,\n\"image\": {\"mediaURL\": \"www.example.com/image.png\",\"caption\": \"This is body\"} }",
      "language": "json",
      "name": "Message Template with Image"
    },
    {
      "code": "{\n\"payloadVersion\":0.1,\n\"to\": \"919999999999\",\n\"wabaNumber\": \"91999999XXXX\",\n“msg_id”:\"25596363|1639561857|20220227|25596363\",\n\"type\": \"file\",\n\"isTemplate\": false,\n\"file\": {\n          \"mediaURL\": \"www.example.com/document.pdf\",\n           \"caption\": \"This is body\",\n          \"filename\": \"sample.pdf\"\n          } }",
      "language": "json",
      "name": "Message with documents"
    }
  ]
}
[/block]

# Expected API Response
CleverTap expects partners to return any of the following responses depending on whether the request was successful. CleverTap will read the response body if the API request status code is 200 OK, so notification processing-related errors and codes can be sent in the response body.  Read below for expected error codes as CleverTapll (@jash: pls check if this should be CleverTap11).
[block:callout]
{
  "type": "info",
  "title": "Error Object",
  "body": "The error object for the following error code needs to be specified only if there are errors in the send message API request:\n\n* 2000 → Invalid credentials\n* 2001 → Invalid template parameters\n* 2002 → Invalid phone number\n* 2003 → Phone number not subscribed \n* 2004 → Other"
}
[/block]
### HTTPS Code: 200 | Successful API call
[block:code]
{
  "codes": [
    {
      "code": "{ \n  \"status\": \"success | failure\",\n}",
      "language": "json"
    }
  ]
}
[/block]
### HTTPS Code: 200 | error
[block:code]
{
  "codes": [
    {
      "code": "{ \n  \"status\": \"failure\",\n   \"error\" : {\n              \"code\" : 2000,\n              \"message\" : \"Invalid Credentials\"\n              }\n}",
      "language": "json"
    }
  ]
}
[/block]
### HTTPS Code: 500
[block:code]
{
  "codes": [
    {
      "code": "{\n\"status\": \"failure\",\n\"error\" : {\n\"message\" : \"Unable to process the request\"\n          }\n}",
      "language": "text"
    }
  ]
}
[/block]
### HTTPS Code: 429
[block:code]
{
  "codes": [
    {
      "code": "{ \"message\" : \"Too many requests to process\"}",
      "language": "json"
    }
  ]
}
[/block]
### HTTPS code: 403 
[block:code]
{
  "codes": [
    {
      "code": "{ \"message\" : \"Bad Request\"}",
      "language": "json"
    }
  ]
}
[/block]

# WhatsApp Callbacks
CleverTap automatically creates unique callback URLs for each customer. These callback URLs are available under the *Provider* setup section. BSPs are expected to add these callbacks at their end and forward the incoming messages to CleverTap’s callback URL in the specified format. CleverTap creates separate callback URLs for message status and incoming messages. Both these callbacks are needed to be configured at the BSP's end.

## Callback Authentication
CleverTap creates unique callback URLs for each customer and does not need any authentication. CleverTap accepts the callbacks if the callbacks are sent in the expected format.

## Incoming Message Callbacks
BSPs need to add  CleverTap's incoming message callback URL at their end and forward the incoming message in the following format.
[block:code]
{
  "codes": [
    {
      "code": "{\n    \"payloadVersion\": \"$$payloadversion\",\n    \"from\": \"$$phone\",\n    \"wabaNumber\": \"$$BusinessWabaNumber\",\n    \"timestamp\": \"$$receivedTS\",\n    \"type\": \"text/location/image/video/voice/file/button\",\n    //Optional(Needs to be sent if user replies to previously sent message)\n    \"context\": {\n        \"id\": \"$$msg_ID\"\n    },\n    //Optional (will be needed if message received is text)\n    \"text\": {\n        \"body\": \"$$incomingMessage\"\n    },\n    //Optional (will be needed if message received is loaction)\n    \"location\": {\n        \"address\": \"$$address\",\n        \"latitude\": \"$$latitude\",\n        \"longitude\": \"$$latitude\",\n        \"name\": \"$$addressTitle\",\n        \"url\": \"$$addressUrls\"\n    },\n    //Optional (will be needed if message received is image)\n    \"image\": {\n        \"mediaURL\": \"$$mediaUrl\",\n        \"mimeType\": \"$$mediaMimeType\", // image/jpeg\n        \"caption\": \"$$incomingmessage\"\n    },\n    //Optional (will be needed if message received is file)\n    \"file\": {\n        \"mediaURL\": \"$$mediaUrl\",\n        \"mimeType\": \"$$mediaMimeType\",\n        \"caption\": \"$$incomingmessage\"\n    },\n    //Optional (will be needed if message received is audio)\n    \"audio\": {\n        \"mediaURL\": \"$$mediaUrl\",\n        \"mimeType\": \"$$mediaMimeType\"\n    },\n    //Optional (will be needed if message received is video)\n    \"video\": {\n        \"mediaURL\": \"$$mediaUrl\",\n        \"mimeType\": \"$$mediaMimeType\",\n        \"caption\": \"$$incomingmessage\"\n    },\n    //Optional (will be needed if the message received is video)\n    \"button\": {\n        \"payload\": \"$$buttonPayload\", // same as outgoing  message\n        \"text\": \"$$buttonText\"\n    }\n}",
      "language": "json",
      "name": "Incoming message callback payload"
    }
  ]
}
[/block]
### Payload Description
[block:parameters]
{
  "data": {
    "h-0": "Key name",
    "h-2": "Sample values",
    "h-1": "Description",
    "0-0": "from",
    "0-1": "Source number for incoming message",
    "0-2": "“9199XXXXXXXX”",
    "1-0": "payloadversion",
    "1-2": "“0.1“",
    "1-1": "version of the callback payload being sent to CleverTap",
    "2-0": "wabaNumber",
    "2-2": "“9199XXXXXXXX”",
    "2-1": "Destination business WABA number to which message was sent",
    "3-0": "timestamp",
    "3-2": "“1647441774”",
    "3-1": "Timestamp when the message was sent",
    "4-0": "type",
    "4-2": "“text/audio/video/image”",
    "4-1": "Type of incoming message",
    "5-0": "context.id",
    "5-2": "25596363|1639561857|20220227|25596363",
    "5-1": "`Msg_id` of the message to which the user has responded",
    "6-0": "text.body",
    "6-2": "“Hey, This is message”",
    "6-1": "Text received from end user",
    "7-0": "location.lattitude",
    "7-2": "2.457476548",
    "7-1": "Latitude of the location shared",
    "8-0": "location.Longitude",
    "8-2": "1.565867657",
    "8-1": "Longitude of the location shared",
    "9-0": "location.name",
    "9-2": "Joe’s House",
    "9-1": "Name of the location shared",
    "10-0": "location.address",
    "11-2": "www.example.com",
    "11-1": "Address URL",
    "11-0": "location.url",
    "10-2": "102, Parker street, USA",
    "10-1": "Address of the location shared",
    "12-0": "image.mediaURL",
    "12-1": "Media File URL",
    "12-2": "www.example.com/image.png",
    "13-0": "image.mimetype",
    "13-1": "Media file mime type",
    "13-2": ".png/.jpeg",
    "14-0": "image.caption",
    "14-1": "Image caption",
    "14-2": "“This is caption”",
    "15-0": "file.mediaURL",
    "15-1": "Media File URL",
    "15-2": "www.example.com/file.pdf",
    "16-0": "file.mimetype",
    "16-1": "Media file mime type",
    "17-0": "file.caption",
    "17-1": "Image caption",
    "17-2": "“This is caption”",
    "16-2": ".pdf",
    "18-0": "audio.mediaURL",
    "18-1": "Media File URL",
    "18-2": "www.example.com/audio.mp3",
    "19-0": "video.mimetype",
    "19-1": "Media file mime type",
    "19-2": ".mp3",
    "20-0": "video.mediaURL",
    "20-1": "Media File URL",
    "20-2": "www.example.com/image.png",
    "21-0": "video.mimetype",
    "21-1": "Media file mime type",
    "21-2": ".mp4",
    "22-0": "video.caption",
    "22-1": "Image caption",
    "22-2": "“This is caption”"
  },
  "cols": 3,
  "rows": 23
}
[/block]
## Sample Payload
[block:code]
{
  "codes": [
    {
      "code": "{\n              \"payloadVersion\":\"0.1\",\n              \"from\": \"919999999999\",\n              \"wabaNumber\": \"9199999998888\",\n              \"timestamp\": \"1647441774\",\n              \"type\": \"file\",\n              \"context\": {\n              \"id\": \"25596363|1639561857|20220227|25596363\"\n              },\n\"document\": {\n            \"mediaURL\": \"www.example.com/document.pdf\",\n             \"caption\": \"This is body\",\n             \"mimeType\": \".pdf\"\n          } \n}",
      "language": "json",
      "name": "Incoming message with Document"
    },
    {
      "code": "{\n\"payloadversion\":\"0.1\",\n\"from\": \"919999999999\",\n\"wabaNumber\": \"9199999998888\",\n\"timestamp\": \"1647441774\",\n\"type\": \"location\",\n\"context\": {\n              \"id\": \"25596363|1639561857|20220227|25596363\"\n              },\n\"location\": {\n            \"address\": \"107, baker street\",\n            \"latitude\": \"2.457476548\",\n            \"longitude\": \"2.457476548\",\n            \"name\": \"Johns office\", //optional\n            \"url\": \"www.johnsoffice.com\" // optional\n            }\n}\n",
      "language": "json",
      "name": "Incoming message with location"
    }
  ]
}
[/block]
## Message Status Callbacks
BSPs need to add  CleverTap's message status callback URL at their end and forward the message statuses in the following format. CleverTap uses these callbacks to populate the campaign statistics.
[block:code]
{
  "codes": [
    {
      "code": "{\n    \"paytloadVersion\": \"$$paypoadVersion\",\n    \"statuses\": [\n        {\n            \"msgId\": \"$$customMessageID\",\n            \"status\": \"sent/delivered/read/failed\",\n            \"timestamp\": \"$$timestamp\", //Event timestamp\n            \"error\": {\n                \"code\": \"$$errorcode\",\n                \"title\": \"$$errordescription\"\n            }\n        },\n        {\n            //Support multiple status callbacks in a single request\n        }\n    ]\n}",
      "language": "json",
      "name": "Message Status Callback"
    }
  ]
}
[/block]
### Payload Description
[block:parameters]
{
  "data": {
    "0-0": "payloadversion",
    "0-1": "Version of the payload being sent to CleverTap",
    "0-2": "0.1",
    "h-0": "Key name",
    "h-1": "Description",
    "h-2": "Sample values",
    "1-0": "statuses[X].status",
    "1-1": "Notification status",
    "1-2": "“sent/delivered/read/failed”",
    "2-0": "statuses[X].timestamp",
    "2-1": "Timestamp of the event",
    "2-2": "“1647441774”",
    "3-0": "statuses[X].msgId",
    "3-1": "Unique identifier for message being sent and expected to be present in callback payloads",
    "3-2": "25596363|1639561857|20220227|25596363",
    "4-0": "statuses[X].error.code",
    "4-1": "Failure Error code",
    "4-2": "1001",
    "5-0": "statuses[X].error.title",
    "5-1": "Description of error",
    "5-2": "Message specified does not match with any template."
  },
  "cols": 3,
  "rows": 6
}
[/block]
## Sample Payload
[block:code]
{
  "codes": [
    {
      "code": "{\n\"paytloadVersion\":\"0.1\",\n\"statuses\": [{\n               \"msgId\": \"25596363|1639561857|20220227|25596363\", // same as outbound message ID\n               \"status\": \"delivered\",\n               \"timestamp\": \"1647441774\", //Event timestamp\n               }]\n               }",
      "language": "json",
      "name": "Successful Delivery Payload"
    },
    {
      "code": "{\"paytloadVersion\":\"0.1\",\n\"statuses\": [{\n               \"msgId\": \"25596363|1639561857|20220227|25596363\",\n               \"status\": \"failed\",\n               \"timestamp\": \"1647441774\", //Event timestamp\n               \"error\": {\n               \"code\": 1004,\n               \"title\": \"Invalid phone number.\"\n               }}]\n\n}\n",
      "language": "json",
      "name": "Failure Delivery Payload"
    }
  ]
}
[/block]
# Callback Error Codes
[block:callout]
{
  "type": "warning",
  "title": "Callback Error Codes",
  "body": "Listed below are the expected callback error codes:\n\n* 1000 → Invalid credentials\n* 1001  → Invalid template parameters\n* 1002 → Invalid phone number\n* 1003 → The phone number is no longer active\n* 1004 → Too many send requests to phone numbers\n* 1005 → The phone number is temporarily unavailable or not in the provider network\n* 1006 → Phone number is blacklisted\n* 1007 → User device can’t receive the message\n* 1008 → This message is sent outside of the WhatsApp chat window\n* 1009 →  Other"
}
[/block]
# Creating/Uploading User Base
You can upload a CSV file to upload a set of internal users by going to *Settings* > *CSV uploads*. The following is the sample CSV format for uploading user data.
[block:parameters]
{
  "data": {
    "h-0": "Identity",
    "h-1": "Name",
    "h-2": "Email",
    "h-3": "Phone",
    "h-4": "Gender",
    "h-5": "MSG-WhatsApp",
    "h-6": "Upload Name",
    "0-0": "deepak+345@cleverTap.com",
    "0-3": "+9199*****420",
    "0-6": "Sample Upload",
    "0-5": "TRUE",
    "0-4": "M",
    "0-1": "John Doe"
  },
  "cols": 7,
  "rows": 1
}
[/block]
# Accepted Message Formats
CleverTap currently has limitations on the types of WhatsApp messages supported on the dashboard. We are working on adding support for the new message types as soon as possible but for the time being, only the following message types are supported.

**Freeform Messages**
This message type supports the following format:
  * Simple text
  * Audio
  * Video
  * Images
  * Document

**Template messages**
The elements of the Template message include a header, footer, simple text, and buttons.
The header section supports the following formats:

  * Text
  * Image
  * Videos
  * Locations
  * Audios
  * Documents

# FAQs

**Q. My WhatsApp provider has shared the API credentials with me. Can I save the provider in the CleverTap dashboard and start creating WhatsApp campaigns?**

**Ans:** Ensure that your WhatsApp service provider is there in the list of integrated partners. If yes, ensure that you are using the custom API endpoint that your partner has created for CleverTap integration.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/96d165f-image_18.png",
        "image (18).png",
        1288,
        976,
        "#f7f7f9"
      ],
      "border": true
    }
  ]
}
[/block]