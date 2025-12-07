---
title: Segment
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
## Introduction

Segment is a Customer Data Infrastructure (CDI) service provider, that provides a service that simplifies collecting and using data from the users of your digital properties (websites, apps, etc). With Segment, you can collect, transform, send, and archive your first-party customer data.

CleverTap has built an integration with Segment, where we provide

1. Integrated SDK 
2. API integration
3. Export to Segment

## API integration

Passing your Segment data into CleverTap can be achieved by API integration.  
Details about this integration are provided [here](https://segment.com/docs/connections/destinations/catalog/clevertap/#identify) 

> 🚧 Transformation of User and Event Properties when using Segment HTTP API
> 
> Segment transforms user property and event property names when passing data to partners like CleverTap in the following scenario.
> 
> 1. Send data to Segment from your servers using the [Segments HTTP API](https://segment.com/docs/connections/sources/catalog/libraries/server/http-api/), if this data is.
> 2. Send data to CleverTap using the [Server Side CleverTap destination](https://segment.com/docs/connections/destinations/catalog/clevertap/#server-side)
> 3. In this case, all event and user property names will be converted from '_sentence case_' to '_snake_case_'  
>    Example :  
>    Data passed from sever -> Segment
> 
> - "Industry Of Traits":" Hello World"  
>   Data passed from Segment -> CleverTap
> - "industry_of_traits": "Hello World"
> 
> If the same data is being passed from multiple destinations to CleverTap, this will lead to the creation of 2 keys for every event and user property. We recommend using CleverTap's own API's to ensure data integrity.  
> More information on the CleverTap API's  [here](https://developer.clevertap.com/docs/api-overview)

## Export to Segment

CleverTap also provides a way in which you can export your data into your Segment account  
Below are the steps to achieve it

## 1. Connect your Segment Account

To be able to send data from CleverTap into Segment, you will need to provide the credentials of your Segment account. This can be done by going into _Settings_ > _Partners_ > _Segment_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5ea9f35-Screenshot_2020-01-13_at_8.06.36_PM.png",
        "Enter Segment project details for connecting the Segment account",
        2428
      ],
      "align": "center",
      "border": true,
      "caption": "Enter Segment Project Details"
    }
  ]
}
[/block]

Enter the Segment write key in the field provided and save the credentials

## 2. Initiate export

You can initiate an export from CleverTap into Segment by navigating to the Campaigns page. Click **+ Campaigns** and select _Segment_ from the channel list. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bc567cd-Screenshot_2020-01-13_at_8.08.13_PM.png",
        "Selecting Segment from the Messaging Channels to create Segment export",
        2264
      ],
      "align": "center",
      "border": true,
      "caption": "Selecting Segment from the Messaging Channels"
    }
  ]
}
[/block]

You can create either a Past Behavior Segment export or an Action export.

You can use all the capabilities of the campaign like scheduling it for later, recurring, etc. to leverage the power of sending you CleverTap data into Segment



# FAQs

### Q. Do CleverTap data exports allow special characters?

A. Yes, CleverTap data exports allow the following special characters:

- CleverTap's export system supports Unicode (UTF-8)  character encoding. It facilitates the accurate representation of text in various languages and scripts. For example, Indian regional languages, Arabic, Korean, Russian, Japanese, Chinese, Spanish, Greek, Indonesian, etc.
- It replaces the following characters with a hyphen to avoid issues in output file generation:
  - Whitespace
  - Tab
  - Slash
  - null (\\0)
- Control characters are replaced with ?. For more information, refer to [Control Character](https://en.wikipedia.org/wiki/Control_character). 
- Supports emoji characters; however, some emojis (UTF-16) may not render properly.