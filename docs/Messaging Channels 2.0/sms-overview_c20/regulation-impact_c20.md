---
title: Regulation Impact
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: >-
    Refer to the page listed below to learn more about the following SMS
    section:
  pages:
    - type: link
      title: FAQs
      url: https://docs.clevertap.com/docs/sms-faqs_c20
---
[block:api-header]
{
  "title": "Overview"
}
[/block]
The Telecom Regulatory Authority of India (TRAI) requires distributed ledger technology (DLT) registration for all the service providers for bulk SMS services in India. Starting on February 1, 2021, it is mandatory to send messages to customers via a pre-approved template. For more information regarding DLT registration, refer to [SMS Regulations](doc:sms-regulations). 

#What This Means to Our Clients
This requires the following changes from your side when you create an SMS campaign on the CleverTap dashboard. 
[block:callout]
{
  "type": "danger",
  "title": "Template IDs",
  "body": "For the SMS campaigns targeted to Indian mobile numbers and having MSG-91 as the service provider, a template ID always needs to be added. For other service providers, a template ID may or may not be required. We recommend checking with your service provider."
}
[/block]
##Future Campaigns
Future campaigns are the campaigns that have started after February 1, 2021.

When you create campaigns after the mandated date, you must use a pre-approved template. In the campaign setup where you choose a service provider, we now provide an extra field to provide a template ID. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a8d7c22-SMS_temp_new.png",
        "SMS temp new.png",
        1702,
        960,
        "#efecf8"
      ],
      "border": true
    }
  ]
}
[/block]
This field is optional because it is only required for sending SMS messages to phone numbers in India. Check that you provide a matching template ID every time you create an SMS campaign for customers in India. 

For generic service providers, you can edit the settings to additionally set up a key-value pair as shown below:
  * Key: This indicates the name of the key for a template ID your service provider is expecting you to send. In the example shown below 'content_id' is the name of the key expected by the service provider.
  * Value: Specify $$TemplateId. You can enter the value of the template ID at the time of the campaign creation. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d89ec0d-Screenshot_2021-01-29_at_3.21.42_PM.png",
        "Screenshot 2021-01-29 at 3.21.42 PM.png",
        733,
        509,
        "#f9fafb"
      ],
      "border": true
    }
  ]
}
[/block]
For example, if the key name for a template ID is expected as content_id.

The Template ID that you have to use in the campaign, has to be entered in the *WHAT* section of the campaign. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/577d331-temp_id.png",
        "temp id.png",
        1720,
        832,
        "#efebf8"
      ],
      "border": true
    }
  ]
}
[/block]
The value that you will enter here is the one that is being accepted by your service provider for passing the Template ID. The Template ID parameter that you put in the endpoint URL.
Check with the service provider which key they accept for Template ID and accordingly add that key and then the Template ID value in the message section.


##Current Campaigns
Current campaigns are the campaigns that were started before February 1, 2021. 

###Campaigns
To receive all your running campaigns, perform the following steps:
1. From the dashboard, navigate to *Campaigns*.
2. Select the channel as *SMS* from the filter.
3. Select the status as *Running*, then click **Apply**. 


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7cc9d02-sms_filter.png",
        "sms filter.png",
        2878,
        1578,
        "#a1a0a3"
      ],
      "border": true
    }
  ]
}
[/block]
4. Click on the **Subscribe to Reports** link.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d73379a-subscribe_to_reports.png",
        "subscribe to reports.png",
        2824,
        866,
        "#e6e8ef"
      ]
    }
  ]
}
[/block]
5. Once the *Campaign Summary Emails* window displays, enter a report name.
6. Select *Campaign overview*.
7. Click **Send Report**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/35dad38-4_Fill_out_report.png",
        "4 Fill out report.png",
        565,
        813,
        "#f8f9fb"
      ]
    }
  ]
}
[/block]
You will then receive a report via email with all the running SMS campaigns and their relevant campaign IDs.  

###Journeys
To receive all your running journeys, perform the following steps:
1. From the dashboard, navigate to *Journeys*.
2. Select the status as *Running* from the filter, then click **Apply**. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/58cda56-filter_journeys.png",
        "filter journeys.png",
        460,
        1558,
        "#f4f3f6"
      ],
      "border": true,
      "sizing": "smart"
    }
  ]
}
[/block]
3. Select the desired campaign and click the **Email report** link.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ea0a4d0-email_reports_1.png",
        "email reports 1.png",
        2736,
        728,
        "#f8f8fa"
      ],
      "border": true
    }
  ]
}
[/block]
4. Once the *Email report* window displays, enter a report name.
6. Select *Nodewise* for the report type.
7. Click **Email report**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2a02134-er.png",
        "er.png",
        588,
        436,
        "#eeeef4"
      ],
      "border": true
    }
  ]
}
[/block]
You will then receive a report via email that you can filter by campaign channel as SMS to get a list of all SMS campaigns with their campaign IDs.

###Match IDs

After you have a list of all campaign IDs from the campaign and journey steps above, perform the following steps:
1. Match these IDs to the template IDs from the SMS service provider's dashboard.
2. Send this data to the CleverTap platform in the JSON format/JSON payload and hit our endpoint. 

####Base URLs
Use the appropriate URL depending on your location:
  * For customers on an EU stack: https://api.clevertap.com/1/update/templateIds.json 
  * For customers on an IN stack: https://in1.api.clevertap.com/1/update/templateIds.json

####HTTP POST Method 

The X-CleverTap-Account-Id and X-CleverTap-Passcode are used to authenticate the request. Please refer to the [authentication guide](doc:authentication) to view how to get their values.

The following headers are all required:
[block:parameters]
{
  "data": {
    "h-0": "Header",
    "h-1": "Description",
    "h-2": "Type",
    "h-3": "Example Value",
    "0-0": "X-CleverTap-Account-Id",
    "0-1": "Your CleverTap account ID.",
    "0-2": "String",
    "0-3": "\"X-CleverTap-Account-Id: ACCOUNT_ID\"",
    "1-0": "X-CleverTap-Passcode",
    "1-1": "Your CleverTap account passcode.",
    "1-3": "\"X-CleverTap-Passcode: PASSCODE\"",
    "1-2": "String",
    "2-0": "Content-Type",
    "2-1": "Request content-type is always set to application/JSON.",
    "2-2": "String",
    "2-3": "\"Content-Type: application/json\""
  },
  "cols": 4,
  "rows": 3
}
[/block]
The following is a sample JSON:
[block:code]
{
  "codes": [
    {
      "code": "[\n{\n\"campaign_id\" : 1563478922,  // campaign ID\n\"template_id\" : \"455633413\", // template ID\n},\n{\n\"campaign_id\" : 1563478922,  \n\"template _id\" : \"455633413\"\n}\n]",
      "language": "json"
    }
  ]
}
[/block]
Your CleverTap campaigns will now have the correct template IDs tagged to them.