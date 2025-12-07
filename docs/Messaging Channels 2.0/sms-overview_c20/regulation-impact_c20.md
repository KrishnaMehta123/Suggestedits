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
## Overview

The Telecom Regulatory Authority of India (TRAI) requires distributed ledger technology (DLT) registration for all the service providers for bulk SMS services in India. Starting on February 1, 2021, it is mandatory to send messages to customers via a pre-approved template. For more information regarding DLT registration, refer to [SMS Regulations](doc:sms-regulations). 

# What This Means to Our Clients

This requires the following changes from your side when you create an SMS campaign on the CleverTap dashboard. 

> ❗️ Template IDs
>
> For the SMS campaigns targeted to Indian mobile numbers and having MSG-91 as the service provider, a template ID always needs to be added. For other service providers, a template ID may or may not be required. We recommend checking with your service provider.

## Future Campaigns

Future campaigns are the campaigns that have started after February 1, 2021.

When you create campaigns after the mandated date, you must use a pre-approved template. In the campaign setup where you choose a service provider, we now provide an extra field to provide a template ID. 

<Image title="SMS temp new.png" alt={1702} className="border" border={true} src="https://files.readme.io/a8d7c22-SMS_temp_new.png" />

This field is optional because it is only required for sending SMS messages to phone numbers in India. Check that you provide a matching template ID every time you create an SMS campaign for customers in India. 

For generic service providers, you can edit the settings to additionally set up a key-value pair as shown below:

* Key: This indicates the name of the key for a template ID your service provider is expecting you to send. In the example shown below 'content\_id' is the name of the key expected by the service provider.
* Value: Specify $$TemplateId. You can enter the value of the template ID at the time of the campaign creation. 

<Image title="Screenshot 2021-01-29 at 3.21.42 PM.png" alt={733} className="border" border={true} src="https://files.readme.io/d89ec0d-Screenshot_2021-01-29_at_3.21.42_PM.png" />

For example, if the key name for a template ID is expected as content\_id.

The Template ID that you have to use in the campaign, has to be entered in the *WHAT* section of the campaign. 

<Image title="temp id.png" alt={1720} className="border" border={true} src="https://files.readme.io/577d331-temp_id.png" />

The value that you will enter here is the one that is being accepted by your service provider for passing the Template ID. The Template ID parameter that you put in the endpoint URL.\
Check with the service provider which key they accept for Template ID and accordingly add that key and then the Template ID value in the message section.

## Current Campaigns

Current campaigns are the campaigns that were started before February 1, 2021. 

### Campaigns

To receive all your running campaigns, perform the following steps:

1. From the dashboard, navigate to *Campaigns*.
2. Select the channel as *SMS* from the filter.
3. Select the status as *Running*, then click **Apply**. 

<Image title="sms filter.png" alt={2878} className="border" border={true} src="https://files.readme.io/7cc9d02-sms_filter.png" />

4. Click on the **Subscribe to Reports** link.

![2824](https://files.readme.io/d73379a-subscribe_to_reports.png "subscribe to reports.png")

5. Once the *Campaign Summary Emails* window displays, enter a report name.
6. Select *Campaign overview*.
7. Click **Send Report**.

![565](https://files.readme.io/35dad38-4_Fill_out_report.png "4 Fill out report.png")

You will then receive a report via email with all the running SMS campaigns and their relevant campaign IDs.  

### Journeys

To receive all your running journeys, perform the following steps:

1. From the dashboard, navigate to *Journeys*.
2. Select the status as *Running* from the filter, then click **Apply**. 

<Image title="filter journeys.png" alt={460} className="border" width="smart" border={true} src="https://files.readme.io/58cda56-filter_journeys.png" />

3. Select the desired campaign and click the **Email report** link.

<Image title="email reports 1.png" alt={2736} className="border" border={true} src="https://files.readme.io/ea0a4d0-email_reports_1.png" />

4. Once the *Email report* window displays, enter a report name.
5. Select *Nodewise* for the report type.
6. Click **Email report**.

<Image title="er.png" alt={588} className="border" border={true} src="https://files.readme.io/2a02134-er.png" />

You will then receive a report via email that you can filter by campaign channel as SMS to get a list of all SMS campaigns with their campaign IDs.

### Match IDs

After you have a list of all campaign IDs from the campaign and journey steps above, perform the following steps:

1. Match these IDs to the template IDs from the SMS service provider's dashboard.
2. Send this data to the CleverTap platform in the JSON format/JSON payload and hit our endpoint. 

#### Base URLs

Use the appropriate URL depending on your location:

* For customers on an EU stack: [https://api.clevertap.com/1/update/templateIds.json](https://api.clevertap.com/1/update/templateIds.json) 
* For customers on an IN stack: [https://in1.api.clevertap.com/1/update/templateIds.json](https://in1.api.clevertap.com/1/update/templateIds.json)

#### HTTP POST Method 

The X-CleverTap-Account-Id and X-CleverTap-Passcode are used to authenticate the request. Please refer to the [authentication guide](doc:authentication) to view how to get their values.

The following headers are all required:

<Table align={["left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Header
      </th>

      <th>
        Description
      </th>

      <th>
        Type
      </th>

      <th>
        Example Value
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        X-CleverTap-Account-Id
      </td>

      <td>
        Your CleverTap account ID.
      </td>

      <td>
        String
      </td>

      <td>
        "X-CleverTap-Account-Id: ACCOUNT\_ID"
      </td>
    </tr>

    <tr>
      <td>
        X-CleverTap-Passcode
      </td>

      <td>
        Your CleverTap account passcode.
      </td>

      <td>
        String
      </td>

      <td>
        "X-CleverTap-Passcode: PASSCODE"
      </td>
    </tr>

    <tr>
      <td>
        Content-Type
      </td>

      <td>
        Request content-type is always set to application/JSON.
      </td>

      <td>
        String
      </td>

      <td>
        "Content-Type: application/json"
      </td>
    </tr>
  </tbody>
</Table>

The following is a sample JSON:

```json
[
{
"campaign_id" : 1563478922,  // campaign ID
"template_id" : "455633413", // template ID
},
{
"campaign_id" : 1563478922,  
"template _id" : "455633413"
}
]
```

Your CleverTap campaigns will now have the correct template IDs tagged to them.
