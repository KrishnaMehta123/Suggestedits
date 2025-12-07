---
title: Google Cloud Platform (GCP)_PE_2
excerpt: Analytics Partner
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
[block:callout]
{
  "type": "info",
  "title": "What's New",
  "body": "CleverTap now supports adding multiple Google Cloud buckets and exporting data to respective buckets on the Google Cloud Platform (GCP)."
}
[/block]
# Overview 
The GCP Export feature enables you to bulk export your CleverTap event or profile data to a GCP bucket. You can export your CleverTap data to analyze it with Business Intelligence (BI) tools or store it in your data warehouse for future analysis.
[block:callout]
{
  "type": "info",
  "body": "For more information and enable this feature for your account, contact your account manager at CleverTap.",
  "title": "Note"
}
[/block]
# Integrate GCP with CleverTap
The integration involves the following steps:
1. [Create a Service Account for your Project](doc:google-cloud-platform-gcp_pe_2#create-a-service-account-for-your-project).
2. [Create A Bucket](doc:google-cloud-platform-gcp_pe_2#create-a-bucket).
3. [Configure CleverTap Dashboard](doc:google-cloud-platform-gcp_pe_2#configure-clevertap-dashboard).

## Create a Service Account for your Project
To create a service account:
1. Log in to your GCP account and select the project where you want to export your CleverTap data. Create a new project if you do not have a project.
2. From the left panel, select *IAM* and then navigate to *Admin* > *Service Accounts*. 
3. Create a new *Service Account* linked to the selected project and enter the Service account name and description, respectively.
This is the account that you will use to *authenticate* and *authorise* CleverTap to upload exports to your GCP project.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fb49ce9-Screenshot_2020-04-06_at_3.57.40_PM.png",
        "Screenshot 2020-04-06 at 3.57.40 PM.png",
        2880,
        1488,
        "#e7ebf2"
      ],
      "border": true
    }
  ]
}
[/block]
2. Navigate to *Permissions* > *Storage Admin and continue*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b14f47c-Screenshot_2020-04-06_at_3.58.36_PM.png",
        "Screenshot 2020-04-06 at 3.58.36 PM.png",
        2880,
        1488,
        "#ebeef3"
      ],
      "border": true
    }
  ]
}
[/block]
3. Click **+ Create Key** and select JSON for the Service account.
The JSON key downloads to your machine automatically. Save this key because you will have to upload the key to the CleverTap dashboard later.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e5bc98b-Screenshot_2020-04-06_at_4.04.32_PM.png",
        "Screenshot 2020-04-06 at 4.04.32 PM.png",
        2880,
        1488,
        "#c3c4c8"
      ],
      "border": true
    }
  ]
}
[/block]
## Create a Bucket 
Create a bucket that will hold the export files from CleverTap. To do so:
1. From the left panel, navigate to *Storage* and click **Create Bucket**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8d026fe-Screenshot_2020-04-06_at_4.12.33_PM.png",
        "Screenshot 2020-04-06 at 4.12.33 PM.png",
        2280,
        1262,
        "#e8ecf4"
      ],
      "border": true
    }
  ]
}
[/block]
On clicking, *Create a bucket* page opens.
2. *Name your bucket* and fill in the other details as per your requirements.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c696063-Screenshot_2020-04-06_at_4.14.53_PM.png",
        "Screenshot 2020-04-06 at 4.14.53 PM.png",
        2880,
        1262,
        "#e8ecf4"
      ],
      "border": true
    }
  ]
}
[/block]
3. Click **Create**. Following is an image for a successfully created bucket:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fd5d73b-Screenshot_2020-04-06_at_4.16.03_PM.png",
        "Screenshot 2020-04-06 at 4.16.03 PM.png",
        2880,
        1262,
        "#e9eef6"
      ],
      "border": true
    }
  ]
}
[/block]
## Configure CleverTap Dashboard
Add the Service account credentials (created in [Step 1](doc:google-cloud-platform-gcp_pe_2#create-a-service-account-for-your-project) and bucket name to CleverTap. To configure the dashboard:
1. Navigate to *Settings* > *Partners* from the CleverTap dashboard. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/168472b-Navigating_to_Partner_page.png",
        "Navigating to Partner page.png",
        2848,
        1196,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]
2. Hover on the *Google Cloud* icon and click **Integrate**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4abcfd4-Click_Integrate.png",
        "Click Integrate.png",
        2400,
        1196,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]
The *Integrate analytics partner - Google Cloud* window opens on the right side of the screen.
3. Click **+ Google Cloud Bucket** to add a bucket. You can also add multiple buckets from this popup.
4. Enter the following details and click **Save Credentials**:
[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "0-0": "Bucket nickname",
    "1-0": "Service Account Key",
    "2-0": "Bucket name",
    "0-1": "Enter the nickname for your bucket.",
    "1-1": "Enter the contents of the downloaded Service Account Key JSON file (obtained in [Step 1](doc:google-cloud-platform-gcp_pe_2#create-a-service-account-for-your-project)) into the Service Key.",
    "2-1": "Add the name of the bucket as given in the project."
  },
  "cols": 2,
  "rows": 3
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/068bba9-Integrate_analytics_partner_-_GCP.png",
        "Integrate analytics partner - GCP.png",
        2358,
        1304,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "warning",
  "title": "Error When Saving Credential",
  "body": "1. Check if the bucket name is the same as in GCP. Bucket names need to be an exact match.\n2. Generate the Service Account key again, copy and paste the new key into the *Service Account Key* field on the *Integrate analytics partner - Google Cloud* window."
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b4b5b46-Screenshot_2020-04-06_at_4.44.59_PM.png",
        "Screenshot 2020-04-06 at 4.44.59 PM.png",
        2540,
        848,
        "#f8edeb"
      ],
      "caption": "Service Account Key"
    }
  ]
}
[/block]
After successful integration, the *Integrated* tag displays against *Google Cloud* on the *Partner List* page.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/15326b9-Integrated_tag.png",
        "Integrated tag.png",
        2372,
        1196,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]
# Create a New Data Export
To create a new data export:
1. Navigate to *Settings* > *Partners* > *Exports* from the CleverTap dashboard.
2. Click **+ Export** and select *Google Cloud* from the partners dropdown.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2c8be9b-Select_GCP_from_the_Partner_List.png",
        "Select GCP from the Partner List.png",
        2376,
        1192,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]
The *Export to Google Cloud* window displays on the right side of the screen.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1876397-Export_to_Google_Cloud_popup.png",
        "Export to Google Cloud popup.png",
        2452,
        1328,
        "#babbbe"
      ]
    }
  ]
}
[/block]
3. Configure the following settings:
     * **Type**: Select the events from the available options to export. 
       * *All user events*: Export data for all events that have been defined, that is, system and custom events.
       * *Select Events*: Exports only specific events.
       * *All user properties*: Exports all your user profile data.

     * **Frequency**: Select the frequency of export.  
        * *Once only*: A single export for the selected export type. You can export data up to the last 60 days. You create an export for a specific day, date range, previous month, current month, and more.  
       * *Recurring*: Set up a recurring export to export all the new events or user profiles captured in the last window. You can export as frequently as every 4 hours and up to once every 24 hours.
     * **Format**: Select from the following export formats: JSON, XML, CSV, and Parquet. For more information, refer to [Export Format](doc:google-cloud-platform-gcp_pe_2#export-format).
[block:callout]
{
  "type": "warning",
  "body": "Before running a one-time profile export, you must stop any scheduled recurring profile export.",
  "title": "Stop Recurring Profile Export to do One Time Export"
}
[/block]
4. Click **Export**. On clicking, the popup closes, and the *Google export has initiated* message displays at the top of the *Exports* page. CleverTap processes the export, and you can now see the newly-created export for Google Cloud.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/401ba16-Pending_Status.png",
        "Pending Status.png",
        2392,
        1240,
        "#f7f6f8"
      ],
      "border": true
    }
  ]
}
[/block]
To confirm that your event data was successfully exported, select *Storage* from the left panel of Google Cloud. Navigate to the *Bucket details* page and search with the `requestid` (available under the Exports page of CleverTap dashboard). All the exported files are displayed. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2dd4777-Screenshot_2020-04-06_at_8.23.50_PM.png",
        "Screenshot 2020-04-06 at 8.23.50 PM.png",
        2862,
        1240,
        "#ecf0f8"
      ],
      "border": true
    }
  ]
}
[/block]
# Export Format
This section provides information about the file format and the name format of the files being exported to the Google Cloud bucket.

## File Name Format 
The example below shows the file name format for data exports.
  * **Export request ID**: The export request ID is generated when you create a request in the CleverTap dashboard.
  * **Timestamp of export run**: This is the timestamp when the export was run.
  * **Event name**: The event name is an event type included in the file.
  * **File index**: For larger exports, we chunk the data across multiple files. We have limited file sizes to 100 MB chunks to make them more consumable. The file index notes the file series number to arrange the export data.
  * **Database ID**: The database ID of the CleverTap from where the file was exported.
  * **File format**: The format of the file exported to the S3 bucket.
[block:code]
{
  "codes": [
    {
      "code": "<export request id>-<timestamp of the export run>-<event name>-<yyyymmdd>-<file index>-<database-id>.json",
      "language": "text"
    }
  ]
}
[/block]
## File Data Format
Export files are split by event names and date range for the specified event. 

### JSON
The first line of the file contains the event name. After the first line, each line is JSON describing the timestamp, object id, and event properties.
[block:code]
{
  "codes": [
    {
      "code": "{\n\t\"profile\": {\n\t\t\"identity\": \"dqsndckfk234\"\n\t},\n\t\"ts\": 20171109000015,\n\t\"eventProps\": {\n\t\t\"ct_connected_to_wifi\": \"false\",\n\t\t\"ct_bluetooth_version\": \"ble\",\n\t\t\"ct_bluetooth_enabled\": \"false\",\n\t\t\"ct_sdk_version\": 30107,\n\t\t\"ct_latitude\": -6.1975594,\n\t\t\"ct_longitude\": 106.52913,\n\t\t\"ct_os_version\": \"5.1.1\",\n\t\t\"ct_app_version\": \"2.30.1\",\n\t\t\"ct_network_carrier\": \"3\",\n\t\t\"ct_network_type\": \"4G\"\n\t}\n}",
      "language": "json"
    }
  ]
}
[/block]
### CSV
CSV files are comma-delimited and have each event in separate rows.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fdc7b42-CSV.png",
        "CSV.png",
        2032,
        798,
        "#eeefef"
      ]
    }
  ]
}
[/block]
### XML
XML files have the *timeStamp*, and *eventName*, followed by *eventProperties*.
[block:code]
{
  "codes": [
    {
      "code": "<Event>\n    <ts>20200220130735</ts>\n    <eventName>Export Custom Event</eventName>\n    <profile>\n        <all_identities>exportProfile+81@clevertap.com</all_identities>\n        <platform>Web</platform>\n        <email>exportProfile+81@clevertap.com</email>\n    </profile>\n    <deviceInfo>\n        <browser>Others</browser>\n    </deviceInfo>\n    <eventProps>\n        <entry>\n            <key>CT Source</key>\n            <value>API</value>\n        </entry>\n        <entry>\n            <key>Category</key>\n            <value>Mens Watch</value>\n        </entry>\n        <entry>\n            <key>Product name</key>\n            <value>Casio Chronograph Watch</value>\n        </entry>\n        <entry>\n            <key>Price</key>\n            <value>59.99</value>\n        </entry>\n        <entry>\n            <key>Currency</key>\n            <value>USD</value>\n        </entry>\n    </eventProps>\n</Event>",
      "language": "text"
    }
  ]
}
[/block]
### Parquet
Parquet has a timestamp, eventName, and eventProperties for each event.
[block:callout]
{
  "type": "info",
  "body": "Parquet is an open-source file format for Hadoop. Parquet stores nested data structures in a flat columnar format.",
  "title": "Parquet File Format"
}
[/block]