---
title: Generic WhatsApp (COPY) Concurrency WIP
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
# Overview

CleverTap has now made its WhatsApp API and standard callback formats public to global communities of WhatsApp service providers. Now, BSPs & customers do not need to depend on CleverTap to build the native WhatsApp integration. Instead, BSPs or customers can use these APIs and build the integration independently.

> 📘 For CleverTap Customers
>
> This feature is helpful to customers in the following ways:
>
> 1. Customers can build middleware between CleverTap & BSP and create their own endpoint to start using WhatsApp functionality in CleverTap with the BSP of their choice. 
> 2. Customers can ask their BSPs to build the CleverTap integration. This will allow customers to use that provider with CleverTap without any development.

> 📘 For WhatsApp BSPs
>
> Providers interested in pursuing the partnership must complete the integration steps listed in this document and write to [integrations@clevertap.com](mailto:integrations@clevertap.com) to get their name added to this list.

# Partner Acceptance Criteria

Any WhatsApp partner can integrate with our open APIs, but to get added to the list of integrated partners, they need to share the following with CleverTap:

* Production API endpoint for sending Template and Freeform notifications via single endpoint.
* Production API credentials for two test accounts so the CleverTap team can test the integration.
* Providers need to provide dashboard access where the CleverTap team can create the templates or share approved templates to test the campaign flow.
* Providers need to add CleverTap's callback URL in the test accounts so that CleverTap can ensure that callbacks are received in the correct format.
* Providers must publish a CleverTap integration guide in their user docs so that CleverTap can link it with the user document.
* Partners must provide the contact details of their dedicated support and product team so that CleverTap can reach out to them in case of any issues.

## Supported Business Service Providers

CleverTap supports WhatsApp integration with the following business service providers:

* [Nexmo](https://docs.clevertap.com/docs/nexmo-whatsapp)
* [Gupshup](https://docs.clevertap.com/docs/gupshup)
* [Exotel](https://docs.clevertap.com/docs/exotel-whatsapp)
* [Yellow.AI](https://docs.clevertap.com/docs/yellowai)
* [Haptik](https://docs.clevertap.com/docs/haptik)
* [Kaleyra](https://docs.clevertap.com/docs/kaleyra)

# Integration steps

Customers need to get endpoint and authentication details from BSP.

> 📘 Custom Endpoint
>
> * **For customers**\
>   BSPs might have a dedicated endpoint (different from their standard endpoint) for CleverTap integration. Given this, you need to get the API details for CleverTap integration from your provider.
>
> * **For BSPs:**\
>   BSPs must provide API endpoints and tested credentials that work with the CleverTap platform.

To get started with generic integration, BSP integrating with CleverTap must share the API endpoint and authentication details with customers. BSPs must ensure that they provide the endpoint that can process the payload being sent by CleverTap. After the customers have API details handy, proceed as follows:

1. Navigate to *Settings* > *Channels* > *WhatsApp* and select **Other(Generic)** from the *Provider* dropdown list. 

<Image title="Configure Generic Provider Setup" alt={1604} align="center" border={true} src="https://files.readme.io/9e5acb0-WA_generic_1.png">
  Generic Provider Setup
</Image>

2. Enter the API endpoint and auth details to save the endpoint.

> 📘 Provider Verification
>
> CleverTap sends a sample payload to validate the credentials before saving the provider details. BSPs need to provide a “200 OK“ response along with the response if API credentials are correct.

**Expected API Response** 

```json
{
    "status": "success"
}
```

**Sample Credential Validation Payload** 

```json
{
    "payloadVersion": 0.1,
    "wabaNumber": $$WABAnumber,
    "to": "+919870369294",
    "isTemplate": true,
    "template": {
      "namespace": "whatsapp:hsm:technology:generic:verify",
      "languageCode": "en"
    },
    "components": [
      {
        "type": "body",
        "body": {
          "text": "1 code: 2.Valid for 3 minutes.",
          "parameters": [
            {
              "type": "text",
              "text": "1"
            },
            {
              "type": "text",
              "text": "2"
            },
            {
              "type": "text",
              "text": "3"
            }
          ]
        }
      }
    ],
    "msgId": "0|0|0|0"
  }
```

3. Customers need to copy both delivery report callbacks and IMO callback URLs and get these callbacks configured with the WhatsApp provider. Providers need to send the callbacks in the format specified later in this document. Any format, other than our expected callback, will not be accepted. This may result in campaign stats not being populated and incoming messages not showing up in the CleverTap dashboard.

4. After the credentials are stored, customers can save the approved templates under the template section to start sending WhatsApp notifications in the approved template formats. 

> 📘 Template Verification
>
> CleverTap sends a sample payload according to the template being saved in the dashboard. BSPs need to validate the payload and return **200 OK response** if all the details are as per approved templates.

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

> 📘 Single Endpoint
>
> CleverTap does not support different endpoints for different types of messages, so BSPs need to provide just one endpoint to process freeform and template messages.

## API Payload for Template Message

CleverTap sends this payload for sending the template message notification.\
The outgoing template message payload can be broken down into the following three sections:

* User & notification information
* Template information that includes template name, namespace, template language, etc. 
* Content information

> 📘 Payload Essentials
>
> The message payload is encoded into UTF-8 (Unicode Transformation Format) before being sent to the provider's endpoint. 
>
> Values with $$ ($$To,$$BusinessWabaNumber) are dynamic values and change for each request.
>
> CleverTap does not support templates with contacts currently, so contact objects are not sent with payload.
>
> CleverTap does not support Name, Address, or URL key in location object.
>
> `msg_id` is a unique parameter for each message sent from CleverTap and must be present in callbacks sent by BSP to CleverTap.

```json Template Message Payload
{
    "payloadVersion": $$payloadVersion,
    "to": "$$to", // suppport numbers with + and without +(eg. 91 and +91)
    "wabaNumber": "$$businessWabaNumber",
    "isTemplate": true,
    "msgId": "i|campaignID|batchID|j|campaign_variant", // upto 60 characters
    "template": {
        "namespace": "$$templateNamespace",
        "languageCode": "$$BSPsr-language-and-locale-code"
    },
    "components": [
        //There will be either just one header object or no header object present in the payload depending on the template being used. 
        { // optional media header
            "type": "header",
            "header": {
                "type": "text",
                "text": {
                    "text": "$headertext",
                    "parameters": [
                        {
                            "type": "text",
                            "text": "$$PlaceholderText1"
                        }
                    ]
                }
            }
        },
        { // optional media header
            "type": "header",
            "header": {
                "type": "video",
                "video": {
                    "mediaURL": "$$mediaUrl"
                }
            }
        },
      
          { // optional media header
            "type": "header",
            "header": {
                "type": "image",
                "image": {
                    "mediaURL": "$$mediaUrl"
                }
            }
        },
        { // optional document header
            "type": "header",
            "header": {
                "type": "file",
                "file": {
                    "mediaURL": "$$mediaUrl",
                    "filename": "$$filename"
                }
            }
        },
        { // optional location header
            "type": "header",
            "header": {
                "type": "location",
                "location": {
                    "longitude": "$$longitude",
                    "latitude": "$$longitude"
                }
            }
        },
        {
            "type": "body",
            "body": {
                "text": "$$Body",
                "parameters": [
                    {
                        "type": "text",
                        "text": "$$PlaceholderText1"
                    },
                    {
                        "type": "text",
                        "text": "$$PlaceholderText2"
                    }
                ]
            }
        },
        {// optional.. will be present in payload if templates have a footer text
            "type": "footer",
            "footer": "$$footertext"
        },
        {// Dynamic URL CTA (optional)
            "type": "button",
            "index": $$buttonPosition,
            "subType": "dynamicUrl",
            "buttonText": "$$cta_text",
            "parameters": [
                {
                    "type": "text",
                    "text": "$$suffixURL"
                }
            ]
        },
        {//static URL CTA (optional)
            "type": "button",
            "index": $$Buttonposition,
            "buttonText": "cta_text",
            "subType": "staticUrl",
            "parameters": [
                {
                    "type": "text",
                    "text": "$$ButtonURL"
                }
            ]
        },
        {// quick reply buttons (optional)
            "type": "button",
            "index": $$buttonPosition,
            "subType": "quickReply",
            "buttonText": "$$cta_text",
            "parameters": [
                {
                    "type": "payload",
                    "payload": "$$buttonPayload"
                }
            ]
        },
        {// call phone CTA (optional)
            "type": "button",
            "index": $$buttonPosition,
            "subType": "callPhone",
            "buttonText": "$$cta_text",
            "parameters": [
                {
                    "type": "text",
                    "text": "$$phonenumber"
                }
            ]
        }
    ]
}
```

### Postman Collection

[https://www.getpostman.com/collections/5c34a2e3ffd06b7c6492](https://www.getpostman.com/collections/5c34a2e3ffd06b7c6492) 

### Payload key-value description

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Key name
      </th>

      <th>
        Description
      </th>

      <th>
        Sample values
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        payloadVersion
      </td>

      <td>
        A version of the payload being sent.
      </td>

      <td>
        0.1
      </td>
    </tr>

    <tr>
      <td>
        to
      </td>

      <td>
        Targeted user’s phone number.
      </td>

      <td>
        9199XXXXXXXX/ +9199XXXXXXXX
      </td>
    </tr>

    <tr>
      <td>
        wabaNumber
      </td>

      <td>
        Business’s WABA number (from number).
      </td>

      <td>
        9189XXXXXXXX
      </td>
    </tr>

    <tr>
      <td>
        isTemplate
      </td>

      <td>
        Used to highlight whether the payload being sent is for templates or freeform.
      </td>

      <td>
        true/false (Boolean)
      </td>
    </tr>

    <tr>
      <td>
        msgId
      </td>

      <td>
        Unique identifier for a message sent and expected to be present in DLR status callback payloads.
      </td>

      <td>
        25596363|1639561857|20220227|25596363
      </td>
    </tr>

    <tr>
      <td>
        template.namespace
      </td>

      <td>
        Template name/namespace.
      </td>

      <td>
        Namespace/name
      </td>
    </tr>

    <tr>
      <td>
        template.languageCode
      </td>

      <td>
        Template language code as defined by Facebook in\
        [Message Templates - WhatsApp Business On-Premises API - Documentation - Facebook for Developers](https://developers.facebook.com/docs/whatsapp/api/messages/message-templates/#supported-languages).
      </td>

      <td>
        en(uk)
      </td>
    </tr>

    <tr>
      <td>
        components.type
      </td>

      <td>
        Type of component object.
      </td>

      <td>
        header/body/buttons
      </td>
    </tr>

    <tr>
      <td>
        Components.header.type
      </td>

      <td>
        Type of header object.
      </td>

      <td>
        text/audio/image/video/file/location
      </td>
    </tr>

    <tr>
      <td>
        Components.header.text.text
      </td>

      <td>
        Header text.
      </td>

      <td>
        “This is header text”
      </td>
    </tr>

    <tr>
      <td>
        Components.header.text.parameters[X].text
      </td>

      <td>
        Personalization variables sent as an array of objects.
      </td>

      <td>
        "john"
      </td>
    </tr>

    <tr>
      <td>
        Components.header.audio.mediaURL
      </td>

      <td>
        Media URL of the audio file.
      </td>

      <td>
        [www.example.com/audio.mp3](http://www.example.com/audio.mp3)
      </td>
    </tr>

    <tr>
      <td>
        Components.header.file.filename
      </td>

      <td>
        Title of the file.
      </td>

      <td>
        “sample\_document.pdf”
      </td>
    </tr>

    <tr>
      <td>
        Components.header.video.mediaURL  | Type= header
      </td>

      <td>
        Media URL of the video file.
      </td>

      <td>
        [www.example.com/video.mp4](http://www.example.com/video.mp4)
      </td>
    </tr>

    <tr>
      <td>
        Components.header.location.lattitude
      </td>

      <td>
        Latitude of the location shared.
      </td>

      <td>
        2.457476548
      </td>
    </tr>

    <tr>
      <td>
        Components.parameters.location.longitude
      </td>

      <td>
        Longitude of the location shared.
      </td>

      <td>
        1.565867657
      </td>
    </tr>

    <tr>
      <td>
        Components.body
      </td>

      <td>
        Message body.
      </td>

      <td>
        “This is message body”
      </td>
    </tr>

    <tr>
      <td>
        Components.body.parameters[x].text
      </td>

      <td>
        Personalization variables sent as an array of objects
      </td>

      <td>
        "john"
      </td>
    </tr>

    <tr>
      <td>
        Components.index |type = buttons
      </td>

      <td>
        Position of the buttons.
      </td>

      <td>
        0/1/2
      </td>
    </tr>

    <tr>
      <td>
        Components.subtype |type = buttons
      </td>

      <td>
        Type of button.
      </td>

      <td>
        static\_url/ Quickreply/call\_phone/dynamic\_url
      </td>
    </tr>

    <tr>
      <td>
        Components.parameters.text |type = buttons
      </td>

      <td>
        URL suffix for dynamic URL CTA.
      </td>

      <td>
        /home
      </td>
    </tr>

    <tr>
      <td>
        Components.parameters.payload |type = buttons
      </td>

      <td>
        Quick reply button identifier. Same value needs to be returned with incoming message callback URL if someone clicks on the button.
      </td>

      <td>
        “25596363|click“
      </td>
    </tr>

    <tr>
      <td>
        Components.buttonText
      </td>

      <td>
        Button text.
      </td>

      <td>
        “visit home page“
      </td>
    </tr>

    <tr>
      <td>
        Components.footer
      </td>

      <td>
        Footer text.
      </td>

      <td>
        “This is footer”
      </td>
    </tr>
  </tbody>
</Table>

### Payload Samples for Template Message

```json Text Template with Footer
{
"payloadVersion":0.1,
"to": "919999999999",
"wabaNumber": "91999999XXXX",
"isTemplate": true,
"msgId": "25596363|1639561857|20220227|25596363",
"template": {
             "namespace": "Namespace:sample",
             "languageCode":"en(uk)"
                         
                         },
"components": [

{
 "type": "body",
 "body": {
 "text":"This is sample body",
  "parameters": [
               {
                  "type": "text",
                   "text": "Sample"
               }
           ]}},
  {
  "type": "footer",
  "footertext":"this is footer"
        
       }
]}
```
```json Image Template with  Dynamic URL CTA buttons
{
    "payloadVersion": 0.1,
    "to": "919999999999",
    "wabaNumber": "919999999999",
    "isTemplate": true,
    "msgId": "i|campaignID|batchID|j",
    "template": {
        "namespace": "Namespace:sample",
        "languageCode": "en"
    },
    "components": [
        {
            "type": "header",
            "header": {
                "type": "image",
                "image": {
                    "mediaURL": "httpa://www.example.com/image.png"
                }
            }
        },
        {
            "type": "body",
            "body": {
                "text": "This is sample body",
                "parameters": [
                    {
                        "type": "text",
                        "text": "sample"
                    }
                ]
            }
        },
        {
            "type": "button",
            "index": 0,
            "subType": "dynamicUrl",
            "buttonText": "Sample CTA TEXT",
            "parameters": [
                {
                    "type": "text",
                    "text": "https://www.example.com"
                }
            ]
        }
    ]
}
```

## API Payload for Freeform Message

CleverTap will send this payload for sending the Freeform message notification.\
Freeform message API payload has the user information about the targetted users, media URLs, and text. 

> 📘 Payload Essentials
>
> * Values with $$ (for example $$To,$$BusinessWabaNumber) are dynamic values and change for each request.
>
>   * Dynamic Reply Button, interactive lists, and product catalog, contacts, and locations are not currently supported in the CleverTap platform. This is why these objects are not mentioned in the payload.
>
>   * CleverTap does not support Name, Address, or URL key in location object.
>
>   * `msg_id` is a unique parameter for each message sent from CleverTap and must be present in callbacks sent by BSP to CleverTap.

```json Freeform Message Payload
{
    "payloadVersion": $$payloadversion,
    "to": "$$To",
    "wabaNumber": "$$BusinessWabaNumber",
    "msgId": "i|campaignID|batchID|j",
    "type": "text/audio/file/image/location/video",
    "isTemplate": false,
    //Optional 
    "audio": {
        "mediaURL": "$$mediaUrl"
    },
    //OR
    "file": {
        "mediaURL": "$$mediaUrl",
        "caption": "$$body",
        "filename": "$$filename"
    },
    //OR
    "image": {
        "mediaURL": "$$mediaUrl",
        "caption": "$$body"
    },
    //OR
    "text": {
        "body": "$$Body"
    },
    //OR
    "video": {
        "mediaURL": "$$mediaUrl",
        "caption": "$$body"
    }
}
```

### Payload Description

| Key name         | Description                                                                              | Sample values                                                       |
| :--------------- | :--------------------------------------------------------------------------------------- | :------------------------------------------------------------------ |
| to               | Targeted user’s phone number                                                             | 9199XXXXXXXX                                                        |
| "payloadversion" | Version of the payload being sent to CleverTap                                           | 0.1                                                                 |
| wabaNumber       | Business’s WABA number                                                                   | 9189XXXXXXXX                                                        |
| isTemplate       | Used to highlight the whether the payload being sent is for templates or freeform        | true/false                                                          |
| msgId            | Unique identifier for message being sent and expected to be present in callback payloads | 25596363\\|1639561857\\|20220227\\|25596363                         |
| audio.mediaURL   | Media URL of the file                                                                    | [www.example.com/audio.mp3](http://www.example.com/audio.mp3)       |
| file.mediaURL    | Media URL of the file                                                                    | [www.example.com/document.pdf](http://www.example.com/document.pdf) |
| file.caption     | Message body                                                                             | “This is message body”                                              |
| file.filename    | Title of the file                                                                        | “sample\_document.pdf”                                              |
| image.mediaURL   | Media URL of the file                                                                    | [www.example.com/image.png](http://www.example.com/image.png)       |
| image.caption    | Message body                                                                             | “This is message body”                                              |
| video.mediaURL   | Media URL of the file                                                                    | [www.example.com/video.mp4](http://www.example.com/video.mp4)       |
| video.caption    | Message body                                                                             | “This is message body”                                              |

### Payload Samples For Freeform Message Template

```json Message Template with Audio
{
"payloadVersion":0.1,
"to": "919999999999",
“msg_id”:"25596363|1639561857|20220227|25596363",
"wabaNumber": "91999999XXXX",
"type": "audio",
"isTemplate": false,
"audio": {
        "mediaURL": "www.example.com/audio.mp3"
        }
        }
```
```json Message Template with Image
{
"payloadVersion":0.1,
"to": "919999999999",
"wabaNumber": "91999999XXXX",
“msg_id”:"25596363|1639561857|20220227|25596363",
"type": "image",
"isTemplate": false,
"image": {"mediaURL": "www.example.com/image.png","caption": "This is body"} }
```
```json Message with documents
{
"payloadVersion":0.1,
"to": "919999999999",
"wabaNumber": "91999999XXXX",
“msg_id”:"25596363|1639561857|20220227|25596363",
"type": "file",
"isTemplate": false,
"file": {
          "mediaURL": "www.example.com/document.pdf",
           "caption": "This is body",
          "filename": "sample.pdf"
          } }
```

# Expected API Response

CleverTap expects partners to return any of the following responses depending on whether the request was successful. CleverTap will read the response body if the API request status code is 200 OK, so notification processing-related errors and codes can be sent in the response body. Read below for expected error codes:

> 📘 Error Object
>
> The error object for the following error code needs to be specified only if there are errors in the send message API request:
>
> * 2000 → Invalid credentials
> * 2001 → Invalid template parameters
> * 2002 → Invalid phone number
> * 2003 → Phone number not subscribed 
> * 2004 → Other

### HTTPS Code: 200 Successful API call

```json
{ 
  "status": "success | failure",
}
```

### HTTPS Code: 200

```json
{ 
  "status": "failure",
   "error" : {
              "code" : 2000,
              "message" : "Invalid Credentials"
              }
}
```

### HTTPS Code: 500

```json
{
"status": "failure",
"error" : {
"message" : "Unable to process the request"
          }
}
```

### HTTPS Code: 429

```json
{ "message" : "Too many requests to process"}
```

### HTTPS Code: 403

```json
{ "message" : "Bad Request"}
```

# WhatsApp Callbacks

CleverTap automatically creates unique callback URLs for each customer. These callback URLs are available under the *Provider* setup section. BSPs are expected to add these callbacks at their end and forward the incoming messages to CleverTap’s callback URL in the specified format. CleverTap creates separate callback URLs for message status and incoming messages. Both these callbacks are needed to be configured at the BSP's end.

## Callback Authentication

CleverTap creates unique callback URLs for each customer and does not need any authentication. CleverTap accepts the callbacks if the callbacks are sent in the expected format.

## Incoming Message Callbacks

BSPs need to add  CleverTap's incoming message callback URL at their end and forward the incoming message in the following format.

```json Incoming message callback payload
{
    "payloadVersion": "$$payloadversion",
    "from": "$$phone",
    "wabaNumber": "$$BusinessWabaNumber",
    "timestamp": "$$receivedTS",
    "type": "text/location/image/video/voice/file/button",
    //Optional(Needs to be sent if user replies to previously sent message)
    "context": {
        "id": "$$msg_ID"
    },
    //Optional (will be needed if message received is text)
    "text": {
        "body": "$$incomingMessage"
    },
    //Optional (will be needed if message received is loaction)
    "location": {
        "address": "$$address",
        "latitude": "$$latitude",
        "longitude": "$$latitude",
        "name": "$$addressTitle",
        "url": "$$addressUrls"
    },
    //Optional (will be needed if message received is image)
    "image": {
        "mediaURL": "$$mediaUrl",
        "mimeType": "$$mediaMimeType", // image/jpeg
        "caption": "$$incomingmessage"
    },
    //Optional (will be needed if message received is file)
    "file": {
        "mediaURL": "$$mediaUrl",
        "mimeType": "$$mediaMimeType",
        "caption": "$$incomingmessage"
    },
    //Optional (will be needed if message received is audio)
    "audio": {
        "mediaURL": "$$mediaUrl",
        "mimeType": "$$mediaMimeType"
    },
    //Optional (will be needed if message received is video)
    "video": {
        "mediaURL": "$$mediaUrl",
        "mimeType": "$$mediaMimeType",
        "caption": "$$incomingmessage"
    },
    //Optional (will be needed if the message received is video)
    "button": {
        "payload": "$$buttonPayload", // same as outgoing  message
        "text": "$$buttonText"
    }
}
```

### Payload Description

| Key name           | Description                                                | Sample values                                                 |
| :----------------- | :--------------------------------------------------------- | :------------------------------------------------------------ |
| from               | Source number for incoming message                         | “9199XXXXXXXX”                                                |
| payloadversion     | version of the callback payload being sent to CleverTap    | “0.1“                                                         |
| wabaNumber         | Destination business WABA number to which message was sent | “9199XXXXXXXX”                                                |
| timestamp          | Timestamp when the message was sent                        | “1647441774”                                                  |
| type               | Type of incoming message                                   | “text/audio/video/image”                                      |
| context.id         | `Msg_id` of the message to which the user has responded    | 25596363\\|1639561857\\|20220227\\|25596363                   |
| text.body          | Text received from end user                                | “Hey, This is message”                                        |
| location.lattitude | Latitude of the location shared                            | 2.457476548                                                   |
| location.Longitude | Longitude of the location shared                           | 1.565867657                                                   |
| location.name      | Name of the location shared                                | Joe’s House                                                   |
| location.address   | Address of the location shared                             | 102, Parker street, USA                                       |
| location.url       | Address URL                                                | [www.example.com](http://www.example.com)                     |
| image.mediaURL     | Media File URL                                             | [www.example.com/image.png](http://www.example.com/image.png) |
| image.mimetype     | Media file mime type                                       | .png/.jpeg                                                    |
| image.caption      | Image caption                                              | “This is caption”                                             |
| file.mediaURL      | Media File URL                                             | [www.example.com/file.pdf](http://www.example.com/file.pdf)   |
| file.mimetype      | Media file mime type                                       | .pdf                                                          |
| file.caption       | Image caption                                              | “This is caption”                                             |
| audio.mediaURL     | Media File URL                                             | [www.example.com/audio.mp3](http://www.example.com/audio.mp3) |
| video.mimetype     | Media file mime type                                       | .mp3                                                          |
| video.mediaURL     | Media File URL                                             | [www.example.com/image.png](http://www.example.com/image.png) |
| video.mimetype     | Media file mime type                                       | .mp4                                                          |
| video.caption      | Image caption                                              | “This is caption”                                             |

## Sample Payload

```json Incoming message with Document
{
              "payloadVersion":"0.1",
              "from": "919999999999",
              "wabaNumber": "9199999998888",
              "timestamp": "1647441774",
              "type": "file",
              "context": {
              "id": "25596363|1639561857|20220227|25596363"
              },
"document": {
            "mediaURL": "www.example.com/document.pdf",
             "caption": "This is body",
             "mimeType": ".pdf"
          } 
}
```
```json Incoming message with location
{
"payloadversion":"0.1",
"from": "919999999999",
"wabaNumber": "9199999998888",
"timestamp": "1647441774",
"type": "location",
"context": {
              "id": "25596363|1639561857|20220227|25596363"
              },
"location": {
            "address": "107, baker street",
            "latitude": "2.457476548",
            "longitude": "2.457476548",
            "name": "Johns office", //optional
            "url": "www.johnsoffice.com" // optional
            }
}
```

## Message Status Callbacks

BSPs need to add  CleverTap's message status callback URL at their end and forward the message statuses in the following format. CleverTap uses these callbacks to populate the campaign statistics.

```json Message Status Callback
{
    "payloadVersion": "$$paypoadVersion",
    "statuses": [
        {
            "msgId": "$$customMessageID",
            "status": "sent/delivered/read/failed",
            "timestamp": "$$timestamp", //Event timestamp
            "error": {
                "code": "$$errorcode",
                "title": "$$errordescription"
            }
        },
        {
            //Support multiple status callbacks in a single request
        }
    ]
}
```

### Payload Description

| Key name                | Description                                                                              | Sample values                                       |
| :---------------------- | :--------------------------------------------------------------------------------------- | :-------------------------------------------------- |
| payloadversion          | Version of the payload being sent to CleverTap                                           | 0.1                                                 |
| statuses[X].status      | Notification status                                                                      | “sent/delivered/read/failed”                        |
| statuses[X].timestamp   | Timestamp of the event                                                                   | “1647441774”                                        |
| statuses[X].msgId       | Unique identifier for message being sent and expected to be present in callback payloads | 25596363\\|1639561857\\|20220227\\|25596363         |
| statuses[X].error.code  | Failure Error code                                                                       | 1001                                                |
| statuses[X].error.title | Description of error                                                                     | Message specified does not match with any template. |

## Sample Payload

```json Successful Delivery Payload
{
"payloadVersion":"0.1",
"statuses": [{
               "msgId": "25596363|1639561857|20220227|25596363", // same as outbound message ID
               "status": "delivered",
               "timestamp": "1647441774", //Event timestamp
               }]
               }
```
```json Failure Delivery Payload
{"paytloadVersion":"0.1",
"statuses": [{
               "msgId": "25596363|1639561857|20220227|25596363",
               "status": "failed",
               "timestamp": "1647441774", //Event timestamp
               "error": {
               "code": 1004,
               "title": "Invalid phone number."
               }}]

}
```

# Callback Error Codes

> 🚧 Callback Error Codes
>
> Listed below are the expected callback error codes:
>
> * 1000 → Invalid credentials
> * 1001  → Invalid template parameters
> * 1002 → Invalid phone number
> * 1003 → The phone number is no longer active
> * 1004 → Too many send requests to phone numbers
> * 1005 → The phone number is temporarily unavailable or not in the provider network
> * 1006 → Phone number is blacklisted
> * 1007 → User device can’t receive the message
> * 1008 → This message is sent outside of the WhatsApp chat window
> * 1009 →  Other

# Creating/Uploading User Base

You can upload a CSV file to upload a set of internal users by going to *Settings* > *CSV uploads*. The following is the sample CSV format for uploading user data.

| Identity                                                    | Name     | Email | Phone                    | Gender | MSG-WhatsApp | Upload Name   |
| :---------------------------------------------------------- | :------- | :---- | :----------------------- | :----- | :----------- | :------------ |
| [deepak+345@cleverTap.com](mailto:deepak+345@cleverTap.com) | John Doe |       | +919&#x39;**\***&#x34;20 | M      | TRUE         | Sample Upload |

# Accepted Message Formats

CleverTap currently has limitations on the types of WhatsApp messages supported on the dashboard. We are working on adding support for the new message types as soon as possible but for the time being, only the following message types are supported.

**Freeform Messages**\
This message type supports the following format:

* Simple text
* Audio
* Video
* Images
* Document

**Template messages**\
The elements of the Template message include a header, footer, simple text, and buttons.\
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
