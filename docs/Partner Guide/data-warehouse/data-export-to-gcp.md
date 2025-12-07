---
title: Google Cloud Platform (GCP)
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
# Overview

The GCP Export feature enables you to bulk export your CleverTap event or profile data to a GCP bucket. You can export your CleverTap data to analyze it with Business Intelligence (BI) tools or store it in your data warehouse for future analysis.

> 📘 Note
> 
> For more information and enable this feature for your account, contact your account manager at CleverTap.

# Integrate GCP with CleverTap

The integration involves the following steps:

1. [Create a Service Account for your Project](doc:data-export-to-gcp#create-a-service-account-for-your-project).
2. [Create a Bucket](doc:data-export-to-gcp#create-a-bucket).
3. [Configure CleverTap Dashboard](doc:data-export-to-gcp#configure-clevertap-dashboard).

## Create a Service Account for your Project

To create a service account:

1. Log in to your GCP account and select the project where you want to export your CleverTap data. Create a new project if you do not have a project.
2. From the left panel, select _IAM_ and then navigate to _Admin_ > _Service Accounts_. 
3. Create a new _Service Account_ linked to the selected project and enter the Service account name and description, respectively.  
   This is the account that you will use to _authenticate_ and _authorize_ CleverTap to upload exports to your GCP project.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fb49ce9-Screenshot_2020-04-06_at_3.57.40_PM.png",
        "Enter Service Account Details and click Create",
        2880
      ],
      "align": "center",
      "border": true,
      "caption": "Create a New Service Account"
    }
  ]
}
[/block]


2. Navigate to _Permissions_ > _Storage Admin and continue_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b14f47c-Screenshot_2020-04-06_at_3.58.36_PM.png",
        "Navigate to Storage Admin from Google Cloud",
        2880
      ],
      "align": "center",
      "border": true,
      "caption": "Navigate to Storage Admin"
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
        "Create a key and select JSON format for Service Account",
        2880
      ],
      "align": "center",
      "border": true,
      "caption": "Create Key"
    }
  ]
}
[/block]


## Create a Bucket

Create a bucket that will hold the export files from CleverTap. To do so:

1. From the left panel, navigate to _Storage_ and click **Create Bucket**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8d026fe-Screenshot_2020-04-06_at_4.12.33_PM.png",
        "Navigate to Storage Browser from Google Cloud dashboard",
        2280
      ],
      "align": "center",
      "border": true,
      "caption": "Navigate to Storage Browser from GCP Dashboard"
    }
  ]
}
[/block]


On clicking, _Create a bucket_ page opens.

2. _Name your bucket_ and fill in the other details as per your requirements.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c696063-Screenshot_2020-04-06_at_4.14.53_PM.png",
        "Enter your bucket details and create a bucket",
        2880
      ],
      "align": "center",
      "border": true,
      "caption": "Enter your Bucket Details and Create a Bucket"
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
        "Bucket created successfully on Google Cloud",
        2880
      ],
      "align": "center",
      "border": true,
      "caption": "Bucket Created Successfully"
    }
  ]
}
[/block]


## Configure CleverTap Dashboard

Add the Service account credentials (created in [Step 1](doc:data-export-to-gcp#create-a-service-account-for-your-project) and bucket name to CleverTap. To configure the dashboard:

1. Navigate to _Settings_ > _Partners_ > _Partner List_ from the CleverTap dashboard. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fa31f48-PartnersList.jpg",
        "Navigating to Partner page from the CleverTap dashboard",
        2848
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Navigating to Partners"
    }
  ]
}
[/block]


2. Hover on the _Google Cloud_ icon and click **Integrate**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/11536fe-IntegrateGCP.jpg",
        "Hover on the Google Cloud icon and click Integrate",
        2400
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Integrate Google Cloud"
    }
  ]
}
[/block]


The _Integrate analytics partner - Google Cloud_ window opens on the right side of the screen.

3. Click **+ Google Cloud Bucket** to add a bucket. You can also add multiple buckets from this popup.
4. Enter the following details and click **Save Credentials**:

| Field               | Description                                                                                                                                                                       |
| :------------------ | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Bucket nickname     | Enter the nickname for your bucket.                                                                                                                                               |
| Service Account Key | Enter the contents of the downloaded Service Account Key JSON file (obtained in [Step 1](doc:data-export-to-gcp#create-a-service-account-for-your-project)) into the Service Key. |
| Bucket name         | Add the name of the bucket as given in the project.                                                                                                                               |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1e6eb6a-SaveBucket.jpg",
        "Enter Google Cloud bucket details and click Integrate",
        2358
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Enter Google Cloud Bucket Details"
    }
  ]
}
[/block]


> 🚧 Error When Saving Credential
> 
> 1. Check if the bucket name is the same as in GCP. Bucket names need to be an exact match.
> 2. Generate the Service Account key again, copy and paste the new key into the _Service Account Key_ field on the _Integrate analytics partner - Google Cloud_ window.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b4b5b46-Screenshot_2020-04-06_at_4.44.59_PM.png",
        "Service Account Key generated",
        2540
      ],
      "align": "center",
      "caption": "Service Account Key"
    }
  ]
}
[/block]


After successful integration, the _Export_ tag displays against _Google Cloud_ on the _Partner List_ page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/81d7927-image.png",
        null,
        "Successful Google Cloud Integration"
      ],
      "align": "center",
      "border": true,
      "caption": "Successful Google Cloud Integration"
    }
  ]
}
[/block]


<br />

# Create a New Data Export

To create a new data export:

> 📘 Private Beta: Recurring Export for User Profiles
> 
> Previously, handling large amounts of data and frequent updates led to duplication and higher storage needs. The new method uses scheduled transfers to manage resources more effectively and ease system load. We start with a full data export to set a complete base. Then, we only transfer updates or new data. This means that the profile exports will include less data than usual, considering only incremental updates will be exported. This reduces duplication and saves storage space, making data management more efficient.
> 
> Currently, this feature is in Private Beta. To enable this feature for your account, contact your Customer Success Manager.

1. Navigate to **Settings** > **Partners** > **Exports** from the CleverTap dashboard.
2. Click **Create Export** and select **Google Cloud**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a64c840-CreateGCPExport.jpg",
        "Click + Export and select Google Cloud from the Partner dropdown",
        2376
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Create Export"
    }
  ]
}
[/block]


The **Export to Google Cloud** window displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b251131-GCPExport.jpg",
        "Enter export details and click Export",
        2452
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Enter Export Details"
    }
  ]
}
[/block]


3. Configure the following settings:

   - **Partner Bucket name**: Name of the partner bucket. You can choose the required partner bucket from the drop-down list. 

   - **DATA TYPE & IDENTIFIER PRIORITY**: Select the events from the available options to export. 
     - _All events_: Export data for all events that have been defined, that is, system and custom events.
     - _Select events_: Exports only specific events.
     - _All user properties_: Exports all your user profile data.

   - **Fallback priority order for identifiers**: You can prioritize user identities when exporting data. If you have selected multiple identities in the _User Identity_ section, you can assign priorities 1, 2, and 3 to Email, Identity, and Phone Number. Users can then be identified based on these assigned priorities.  
     **NOTE**:  This feature applies only to _All events_ and _All user properties_ type.

   - **FREQUENCY**: Select the frequency of export.  
     - **One time**: A single export for the selected export type. You can export data up to the last 60 days. You create an export for a specific day, date range, previous month, current month, and more.  
     - **Recurring**: Set up a recurring export to export all the new events or user profiles captured in the last window. You can export as frequently as every 4 hours and up to once every 24 hours.
     - **Dates to export data**: The export starts at 12:00 a.m. on the specified date by default.

   - **Format**: Select from the following export formats: JSON, XML, CSV, and Parquet. For more information, refer to [Export Format](doc:data-export-to-gcp#export-format).

   - **Export Data**: If you choose **As string**, the data is sent as a string. If you do not select the box, data is sent in its original format.

> 🚧 Stop Recurring Profile Export to do One Time Export
> 
> Before running a one-time profile export, you must stop any scheduled recurring profile export.

4. Click **Export**. On clicking, the popup closes, and the _Google export has initiated_ message displays at the top of the _Exports_ page. CleverTap processes the export, and you can now see the newly created export for Google Cloud. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5392674-GCPInitiated.jpg",
        "Google Export has initiated message displays at the top",
        2392
      ],
      "align": "center",
      "border": true,
      "caption": "Google Export Initiated"
    }
  ]
}
[/block]


To confirm that your event data was successfully exported, select _Storage_ from the left panel of Google Cloud. Navigate to the _Bucket details_ page and search with the `requestid` (available under the Exports page of the CleverTap dashboard). All the exported files are displayed. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2dd4777-Screenshot_2020-04-06_at_8.23.50_PM.png",
        "New Google Cloud export displays on Export page",
        2862
      ],
      "align": "center",
      "border": true,
      "caption": "New Google Export Displays on Google Cloud"
    }
  ]
}
[/block]


# Stop Export

You can also stop the export that you have created. Hover over the export. Click the **Stop**  ![Stop export](https://files.readme.io/203208a-StopExport.jpg) button for the export request you want to stop.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6a8df33-StopGCPButton.jpg",
        null,
        "Stop Segment Export"
      ],
      "align": "center",
      "border": true,
      "caption": "Stop Google Cloud Export"
    }
  ]
}
[/block]


You are navigated back to the _Exports_ page, and the _Segment data export stopped_ message displays at the top. The status for the data export now displays as **STOPPED**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/41d5b4d-GCPStopped.jpg",
        null,
        "Segment Export Stopped"
      ],
      "align": "center",
      "border": true,
      "caption": "Google Cloud Export Stopped"
    }
  ]
}
[/block]


# Edit an Export

You might need to modify an export to meet specific business requirements or while waiting for the next run. This section describes editing a Live Data Streaming and Recurring export in the **RUNNING** and **PENDING** (awaiting next run) state. 

> 📘 Points to Remember
> 
> - In case of running exports, the new changes will apply to the next run.
> - You cannot edit a One-time export, regardless its status (RUNNING, PENDING, DONE, or STOPPED).
> - You cannot change the export from User Profile to Event and vice-versa.
> - You cannot modify exports marked as **DONE** or **STOPPED**.
> - Export changes for Live DataStreaming take 10-15 minutes to take effect.

To edit an export: 

1. On the CleverTap dashboard, go to **Partners** > **Exports**.
2. Hover over the required export. The **View**, **Edit**, and the **Stop** buttons appear.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5826e7a-EditGCP.jpg",
        null,
        "Click the Edit Export Icon"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Click the Edit Export Icon"
    }
  ]
}
[/block]


3. Click the **Edit** button. The **Export to Google Cloud** section appears.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b489522-EditGCPExport.jpg",
        null,
        "Edit the Export"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Edit the Export"
    }
  ]
}
[/block]


4. Edit the export details and click **Update export**.

# Filter Exports

This section describes the different ways you can filter exports.

## Filter by Export Details

To filter by export details: 

1. Click the **Filter** button at the top right corner. 
2. You can filter exports by **Partner**, **Type**, **Format**, **Status**, or **Frequency**. 
3. To clear the filter, click **Reset all**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6499e90-FilterButton.jpg",
        "",
        "Filter Exports"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Filter Exports"
    }
  ]
}
[/block]


## Filter Exports by Date Range

You can also filter the exports based on the export date. 

To filter exports by export date range:

1. Click the **Filter** button at the top right corner. 
2. Click the **Exported on** button.  
   The **Calendar** widget appears. 

   [block:image]{"images":[{"image":["https://files.readme.io/0cf145e-CalendarWidget.jpg","",""],"align":"center","sizing":"80% ","border":true}]}[/block]
3. Choose the custom date range and click **Apply**.  
   The exports are filtered accordingly.

## Filter Exports by Pagination

To choose how many export items you view per page:

1. Use the **Items per page** drop-down at the bottom of the **Exports** page.
2. Select one of the following options: 10, 20, 30, or 40. By default, the **Exports** page shows 20 exports.

# Export Format

This section provides information about the file format and the name format of the files being exported to the Google Cloud bucket.

## File Name Format

- **File Name Format for Event Export**  
   The example below shows the file name format for event export:
  - _Export request ID_: Indicates the export request ID generated when you create a request in the CleverTap dashboard.
  - _Timestamp of the export run_: Indicates when the export was run.
  - _Event name_: Indicates the event type that is included in the file.
  - _File index_: We chunk the data across multiple files for larger exports. We limit file sizes to 100 MB chunks to make them more consumable. The file index indicates the file number in the file series. 
  - _Database ID_: Indicates the database ID of the CleverTap from where the file was exported. 
  - _File format_: Indicates the format of the file exported to the GCP bucket.  

```text
<export request id>-<timestamp of the export run>-<event name>-<yyyymmdd>-<file index>-<database-id>.json
```

- **File Name Format for User Profile Export**:  
   The example below shows the file name format for user profile export:
  - _Account ID_: Indicates the integer value for your CleverTap project ID. 
  - _Request ID_: Indicates the export request ID generated when you create a request in the CleverTap dashboard.
  - _Timestamp of the export run_: Indicates when the export was run.
  - _Database ID_: Indicates the database ID of the CleverTap from where the file was exported. 
  - _File format_: Indicates the format of the file exported to the GCP bucket.

```text
<account id>-<request id>-<timestamp of the export run>-<database-id>-<file format>.gz
```

## File Data Format

Export files are split by event names and date range for the specified event. 

### JSON

The first line of the file contains the event name. After the first line, each line is JSON describing the timestamp, object id, and event properties.

```json
{
	"profile": {
		"identity": "dqsndckfk234"
	},
	"ts": 20171109000015,
	"eventProps": {
		"ct_connected_to_wifi": "false",
		"ct_bluetooth_version": "ble",
		"ct_bluetooth_enabled": "false",
		"ct_sdk_version": 30107,
		"ct_latitude": -6.1975594,
		"ct_longitude": 106.52913,
		"ct_os_version": "5.1.1",
		"ct_app_version": "2.30.1",
		"ct_network_carrier": "3",
		"ct_network_type": "4G"
	}
}
```

### CSV

CSV files are comma-delimited and have each event in separate rows.

![](https://files.readme.io/fdc7b42-CSV.png "CSV.png")

### XML

XML files have the _timeStamp_, and _eventName_, followed by _eventProperties_.

```text
<Event>
    <ts>20200220130735</ts>
    <eventName>Export Custom Event</eventName>
    <profile>
        <all_identities>exportProfile+81@clevertap.com</all_identities>
        <platform>Web</platform>
        <email>exportProfile+81@clevertap.com</email>
    </profile>
    <deviceInfo>
        <browser>Others</browser>
    </deviceInfo>
    <eventProps>
        <entry>
            <key>CT Source</key>
            <value>API</value>
        </entry>
        <entry>
            <key>Category</key>
            <value>Mens Watch</value>
        </entry>
        <entry>
            <key>Product name</key>
            <value>Casio Chronograph Watch</value>
        </entry>
        <entry>
            <key>Price</key>
            <value>59.99</value>
        </entry>
        <entry>
            <key>Currency</key>
            <value>USD</value>
        </entry>
    </eventProps>
</Event>
```

### Parquet

Parquet has a timestamp, eventName, and eventProperties for each event. 

> 📘 Parquet File Format
> 
> - Parquet is an open-source file format for Hadoop. Parquet stores nested data structures in a flat columnar format.
> - Currently, exports in Parquet format are compressed as **.parquet.gzip**. Contact the customer support if you wish to get the file as .parquet i.e. without any additional compression.

## Prioritize User Identity for Exports

The export file includes an identity column with the user's Identity, Phone Number, or Email values. These values are set based on the identities configured in the CleverTap dashboard under the _Settings_ > _User Identity_ page. This feature lets you prioritize the identifier you want to export in the identity column. 

Let us understand how the prioritization works based on the identities selected in the _User Identity_ page:

- If you select only _Identity_, export includes the identity value. The export file's identity column is empty if it is unavailable.  
  ![](https://files.readme.io/aad1f81-image.png)
- If you select multiple identifiers, you must set the priorities on the _Export_ page. For instance, you set Priority 1 to _Identity_ and Priority 2 to _Email ID_. When exporting data, the export prioritizes the Identity value for the identity column. If it is absent, the Email ID is exported under the identity column of the export file. If both are missing, the column remains empty.  
  ![](https://files.readme.io/52ae818-UserIdentity.jpg)

> 📘 Key Points to Remember
> 
> - If you change the identity later, the export works according to the set priority. To prioritize the modified identities, edit your export.
> - This feature applies only to the following export types: _All events_ and _All user profiles_.
> - For the old running export, this configuration or prirotization is not applicable. You can add the prioritization by editing the running exports.

To prioritize user identity for exports: 

1. Go to **Partners** > **Exports**. 
2. Hover over the required GCP export. Click the **Edit** button.
3. Under **Fallback priority order for identifiers**, set up the priority 1, 2, and 3 for the required identities from the drop-down list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/195d8df-GCPPriority.jpg",
        "Enter export details and click Export",
        1008
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Edit Export Priority"
    }
  ]
}
[/block]


4. Click **Update export**. 

# FAQs

### Q. How to secure the data exports from CleverTap to GCP?

A. You can whitelist IPs to ensure that CleverTap will only have access to push data to your GCP bucket. To get the list of IP whitelisting, refer to the [IP Whitelisting](https://docs.clevertap.com/docs/ip-whitelisting) documentation.

### Q. How to resolve a `403: retentionPolicyNotMet` error during data export to GCP?

A. A `403: retentionPolicyNotMet` error can occur when exporting data to GCP. It could be because of a locked retention policy. To resolve this error: 

1. Open the **GCP Console**.
2. Go to **Menu** > **Cloud Storage** > **Buckets**.
3. Select the required bucket.
4. Go to the **Protection** tab.
5. Check the **Retention policy (for compliance)** section. If any policy is active, the **Edit**, **Delete**, and **Lock** icons are enabled.
6. Click the **Delete** icon to delete the retention policy. If the Delete icon is not enabled, the retention policy is locked on the bucket. In this case, you have no option but to change the bucket to which CleverTap uploads export data.

### Q. Do CleverTap data exports allow special characters?

A. Yes, CleverTap data exports allow the following special characters:

- Supports Unicode (UTF-8)  character encoding. It facilitates the accurate representation of text in various languages and scripts. For example, Indian regional languages, Arabic, Korean, Russian, Japanese, Chinese, Spanish, Greek, Indonesian, etc.
- Replaces the following characters with a hyphen to avoid issues in output file generation: Whitespace, Tab, Slash, and null (\\0).
- Replaces control characters with ?. For more information, refer to [Control Character](https://en.wikipedia.org/wiki/Control_character). 
- Supports emoji characters; however, some emojis (UTF-16) may not render properly.

### Q. What customer-related errors can stop exports, and how are customers notified when interruptions occur?

A. Export processes can stop due to customer-related errors. For example, invalid/expired credentials or a missing partner bucket. CleverTap emails customers about the issue to ensure timely resolution. 

Here is the customer-related error that can stop a GCP export: 

| Error Code | Error Message                                        | Cause and Resolution                                                                                                                                                                                                                                                                    |
| :--------- | :--------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 403        | Credentials are incorrect, GCP account is forbidden. | Your Service Account Key has expired or is invalid. There could be various reasons why your key is incorrect. Recheck all the steps, and you can refer to [Integrate GCP with CleverTap](https://staging.docs.user.clevertap.net/docs/data-export-to-gcp#integrate-gcp-with-clevertap). |

Exports are checked every hour for failures. If an error occurs, CleverTap sends three emails to the export creator within a span of three days. Emails 1 and 2 include the error details and a link to fix it. It warns that the export will stop if the problem is not fixed within three days. Email 3 notifies the creator that CleverTap has stopped the export.