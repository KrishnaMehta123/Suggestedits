---
title: AWS S3 Export
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

The data export feature can export your CleverTap event data to your AWS S3 bucket in bulk. You can use this for analysis in Business Intelligence (BI) tools or storage in your data warehouse for analysis in the future.
[block:callout]
{
  "type": "info",
  "body": "This capability is a part of the *CleverTap for Enterprises* plan. To activate this for your account, contact your sales account manager.",
  "title": "Feature Availability"
}
[/block]
# Setup
This section includes information about the setup steps involved to enable this feature for your account. 
1. [Create an AWS S3 Bucket](doc:aws-s3-export#create-an-aws-s3-bucket)
2. [Create an API Key for Your S3 Bucket](docs:aws-s3-export#create-an-api-key-for-your-s3-bucket)
3. [Add Your S3 Bucket Details to CleverTap](doc:aws-s3-export#add-your-s3-bucket-details-to-clevertap)

## Create an AWS S3 Bucket
To create an AWS S3 bucket:

1. Log in to your AWS account, then search for *S3* in the AWS services box. 
2. Select *S3* from the search results. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/68c90b5-Selecting_S3_from_the_list.png",
        "Selecting S3 from the list.png",
        891,
        566,
        "#eaecee"
      ],
      "border": true
    }
  ]
}
[/block]
    On clicking, the *Bucket* page displays.

3. Click **+ Create bucket**. On clicking, the *Create bucket* page displays:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fe98c60-Bucket_page.png",
        "Bucket page.png",
        2876,
        1132,
        "#d1e2ec"
      ],
      "border": true
    }
  ]
}
[/block]
4. Enter a bucket name, region, logging, versioning, and encryption preferences. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0bbda49-Create_bucket_page.png",
        "Create bucket page.png",
        1628,
        4452,
        "#f2f4f5"
      ],
      "border": true,
      "sizing": "80"
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "body": "For this integration, you need not modify the default settings; however, you must check your internal organization's policies to verify if you need to modify any of these settings.",
  "title": "Recommendation for Setup"
}
[/block]

Based on your CleverTap account settings, we host your data in Europe (EU), the United States (US), Singapore (SG), or India (IN). To identify the region of your account and the corresponding region that you must select when configuring the bucket settings, refer to the following table:
[block:parameters]
{
  "data": {
    "h-0": "CleverTap Dashboard URL",
    "h-1": "Region",
    "h-2": "AWS S3 Bucket Region",
    "0-0": "[https://eu1.dashboard.clevertap.com/login.html](https://eu1.dashboard.clevertap.com/login.html#/)",
    "0-1": "EU",
    "1-0": "[https://in1.dashboard.clevertap.com/login.html](https://in1.dashboard.clevertap.com/login.html#/)",
    "1-1": "India",
    "2-0": "[https://us1.dashboard.clevertap.com/login.html](https://us1.dashboard.clevertap.com/login.html#/)",
    "2-1": "US",
    "3-0": "[https://sg1.dashboard.clevertap.com/login.html](https://sg1.dashboard.clevertap.com/login.html#/)",
    "3-1": "Singapore",
    "4-1": "South Korea",
    "0-2": "EU (Ireland) eu-west-1",
    "2-2": "US West (Oregon) us-west-2",
    "1-2": "Asia Pacific (Mumbai) ap-south-1",
    "3-2": "Asia Pacific (Singapore) \nap-southeast-1",
    "4-0": "[https://sk1.dashboard.clevertap.com/login.html](https://sk1.dashboard.clevertap.com/login.html#/)",
    "4-2": "Asia Pacific (Seoul) \nap-northeast-2"
  },
  "cols": 3,
  "rows": 5
}
[/block]
5. Click **Create bucket**. On successful bucket creation, the following message displays in the snackbar at the top:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/66633bb-Successful_bucket_creation.png",
        "Successful bucket creation.png",
        2770,
        1194,
        "#d5e3dc"
      ],
      "border": true
    }
  ]
}
[/block]
The bucket you just created now shows up on your S3 console. We recommend you note down the name of your new bucket as you will need it for the next step.

## Create an API Key for Your S3 Bucket
This section demonstrates the creation of an AWS API key that has write access to the bucket we created in the above step. CleverTap uses this API key to export data to your S3 bucket.

1. Click on your account name on the top right of the AWS console.
2. Click **Security Credentials**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/152163f-Security_credentials.png",
        "Security credentials.png",
        388,
        438,
        "#313742"
      ],
      "border": true,
      "sizing": "smart"
    }
  ]
}
[/block]
3. Select *Users* from the left navigation and click **Add user**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8b81e57-Click_Add_users.png",
        "Click Add users.png",
        2878,
        1196,
        "#e2e9f1"
      ],
      "border": true
    }
  ]
}
[/block]
On clicking, the *Add user* page displays.
4. Enter the *User name* and select the *Programmatic access* checkbox.
5. Click **Next:Permissions**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2cb0126-Add_user.png",
        "Add user.png",
        2878,
        1274,
        "#ececed"
      ],
      "border": true
    }
  ]
}
[/block]
On clicking, *Set permissions* page displays.
6. Click **Create group** under *Add user to group* tab.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c008773-Create_group.png",
        "Create group.png",
        2872,
        1760,
        "#f7f8f9"
      ],
      "border": true
    }
  ]
}
[/block]
On clicking, *Create group* page displays.
7. Click **Create policy**. On clicking, *Create policy* page opens in a new tab.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2803f68-Create_group_page.png",
        "Create group page.png",
        2482,
        1501,
        "#f0f1f1"
      ],
      "border": true
    }
  ]
}
[/block]
8. Select the **JSON** tab and then paste the JSON code given below in the box. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7622dac-Replace_JSON_code.png",
        "Replace JSON code.png",
        2874,
        1238,
        "#f9f9fa"
      ]
    }
  ]
}
[/block]

[block:code]
{
  "codes": [
    {
      "code": "{\n    \"Version\": \"2012-10-17\",\n    \"Statement\": [\n        {\n            \"Effect\": \"Allow\",\n            \"Action\": [\n                \"s3:ListBucket\"\n            ],\n            \"Resource\": [\n                \"arn:aws:s3:::clevertap-example\"\n            ]\n        },\n        {\n            \"Effect\": \"Allow\",\n            \"Action\": [\n                \"s3:PutObject\"\n            ],\n            \"Resource\": [\n                \"arn:aws:s3:::clevertap-example/*\"\n            ]\n        }\n    ]\n}",
      "language": "json"
    }
  ]
}
[/block]
9. Replace `clevertap-example` in the JSON code with the name of the S3 bucket you created in the above step. 
The permissions defined in this policy allow CleverTap to get information about your bucket and upload files to it.
[block:callout]
{
  "type": "info",
  "body": "*IP Whitelisting* is not supported with S3 exports. For more information about AWS API access policies, refer to [this post](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_examples_s3_rw-bucket-console.html) from the AWS blog.",
  "title": "AWS API Access Policies"
}
[/block]
10. Click **Next: Tags**  and then click **Next: Review**. On clicking, the *Create policy* page opens.
11. Enter the policy *Name* and click **Create policy**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3c47940-Create_policy.png",
        "Create policy.png",
        2648,
        1588,
        "#f7f7f8"
      ],
      "border": true
    }
  ]
}
[/block]
On successful policy creation, the following message displays in the snackbar at the top:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cc7b89a-Policy_created_successfully.png",
        "Policy created successfully.png",
        2870,
        1198,
        "#d0e1e3"
      ],
      "border": true
    }
  ]
}
[/block]
12. Go back to the *Create group* page (opened in step 6), search for the policy you just created, and assign it to the new group by selecting the checkbox next to it.
13. Click **Create group**. On clicking, the *Add user* page displays.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a81e456-Search_policy.png",
        "Search policy.png",
        2486,
        1198,
        "#f1f1f2"
      ],
      "border": true
    }
  ]
}
[/block]
14. Click **Next: Tags** and then click **Next: Review**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6bbcf91-Click_Next_Tags.png",
        "Click Next Tags.png",
        2012,
        1824,
        "#f5f7f7"
      ],
      "border": true
    }
  ]
}
[/block]
15. Click **Create user**. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d88007d-Create_user.png",
        "Create user.png",
        1980,
        1208,
        "#f8f8f8"
      ],
      "border": true
    }
  ]
}
[/block]
On successful user creation, the following page displays. You will see your *Access key ID* and the *Secret access key*. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d3b1def-Access_key_and_secret_access_key.png",
        "Access key and secret access key.png",
        2878,
        1200,
        "#f7f8f6"
      ],
      "border": true
    }
  ]
}
[/block]
These credentials allow CleverTap to upload files to your S3 bucket. We recommend you note down these values as you will require them for the next step. Otherwise, you can also click **Download .csv** to save these details for future use.

## Add Your S3 Bucket Details to CleverTap
To add your S3 bucket details to Clevertap, perform the following steps:

1. Log in to your CleverTap account.
2. Navigate to *Settings* > *Partners* > *Exports*. 
3. Click the **AWS Amazon** icon and select *S3* from the *AWS Connections* dropdown.
4. Enter your bucket name from the *Create an AWS S3 Bucket* section above. 
5. Enter your *Access key ID* and the *Secret access key* obtained earlier.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/94cbd71-Exports_page.png",
        "Exports page.png",
        2270,
        1288,
        "#fafafb"
      ],
      "border": true
    }
  ]
}
[/block]
# Create a New Data Export
To create a new data export, perform the following steps:

1. Navigate to *Settings* > *Partners* > *Exports* > *Activity Log*.
2. Click **+ Create Export**. 


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/438f569-Create_Export_page.png",
        "Create Export page.png",
        1209,
        639,
        "#f5f6f7"
      ],
      "border": true
    }
  ]
}
[/block]

On clicking, *Create an export* popup will display.

3. Define the following settings and click **Create export**:
* *Select an export partner*: Select AWS S3 from the dropdown list.
* Export details: Select the following appropriate export-related options: the type of export (user profile or events), export frequency, and export format. For more information, refer to [Export Details](doc:aws-s3-export#export-details).
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/370dd04-Create_an_export_popup.png",
        "Create an export popup.png",
        1098,
        1346,
        "#f8f9fb"
      ],
      "border": true,
      "sizing": "smart"
    }
  ]
}
[/block]
# Export Details

## Export Type 
* **All user events**: This exports data for all events that have been defined, which include *System* and *Custom* events. 
* **Select events**: This exports specific events you want to export. 
* **All user profiles**: This exports all your user profile data.

## Export Frequency
* **One time**: Single export for the export type selected. You can export data up to the last 60 days. 
* **Recurring**: Set up a recurring export that exports all the new events/user profiles captured in the last window. You can export as frequently as every 4 hours and up to once every 24 hours. 

## Export Format
* JSON
* XML
* CSV
* Parquet
[block:callout]
{
  "type": "info",
  "body": "If there is a scheduled recurring profile export, you must stop it to run a one-time profile export.",
  "title": "Exception for One-time Profile Export"
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b1aed72-Data_Export_to_AWS_S3_-_Choose_Export.png",
        "Data Export to AWS S3 - Choose Export.png",
        634,
        542,
        "#ccced2"
      ],
      "border": true,
      "sizing": "80"
    }
  ]
}
[/block]
CleverTap will now process the export. You can refresh the *Activity Log* page to see the current status of the export. After the export is complete, the status for that export is displayed as *Done*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1653bb8-Export_Status.png",
        "Export Status.png",
        1209,
        639,
        "#f5f6f7"
      ],
      "border": true
    }
  ]
}
[/block]
To confirm your event data was successfully exported:
1. Log in to your AWS account and navigate to the *S3* console. 
2. Search your *Bucket* from the *Buckets* page and then click the bucket name. 
3. Copy the *Request ID* from the activity log and search with that ID. You should see your respective file there. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fc7efeb-Search_for_export_files.png",
        "Search for export files.png",
        2842,
        1190,
        "#f2f4f5"
      ],
      "border": true
    }
  ]
}
[/block]
For more information, refer to the following section.

# Export Format
This section provides information about file format and name format of the files being exported to the S3 bucket.

## File Name Format 
The example below shows the file name format for data exports:
  * **Export request ID**: The export request ID is generated when you create a request in the CleverTap dashboard.
  * **Timestamp of export run**: The timestamp is when the export was run.
  * **Event name**: The event name is an event type that is included in the file.
  * **File index**: For larger exports, we chunk the data across multiple files. The file index notes what file number in the file series it is. We have limited file sizes to 100 MB chunks to make them more consumable.
  * **Database ID**: The database ID of the CleverTap from where the file was exported. 
  * **File format**: The format of the file exported to the S3 bucket. 
[block:code]
{
  "codes": [
    {
      "code": "<export request id>-<timestamp of the export run>-<event name>-<yyyymmdd>-<file index>-<database-id>.<file format>.gz",
      "language": "text"
    }
  ]
}
[/block]
## File Data Format
Files are split by event names for event exports and each file will have all event data for the given period for the event.

### JSON
The first line of the file contains the event name. After the first line, each line in JSON describes the timestamp, object id, and event properties.
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
        "https://files.readme.io/aa71f9f-Screenshot_2020-02-28_at_12.53.22_PM.png",
        "Screenshot 2020-02-28 at 12.53.22 PM.png",
        2032,
        798,
        "#eeefef"
      ]
    }
  ]
}
[/block]
### XML
XML have the timeStamp, eventName, followed by eventProperties.
[block:code]
{
  "codes": [
    {
      "code": "<Event>\n    <ts>20200220130735</ts>\n    <eventName>Export Custom Event</eventName>\n    <profile>\n        <all_identities>exportProfile+81@clevertap.com</all_identities>\n        <platform>Web</platform>\n        <email>exportProfile+81@clevertap.com</email>\n    </profile>\n    <deviceInfo>\n        <browser>Others</browser>\n    </deviceInfo>\n    <eventProps>\n        <entry>\n            <key>CT Source</key>\n            <value>API</value>\n        </entry>\n        <entry>\n            <key>Category</key>\n            <value>Mens Watch</value>\n        </entry>\n        <entry>\n            <key>Product name</key>\n            <value>Casio Chronograph Watch</value>\n        </entry>\n        <entry>\n            <key>Price</key>\n            <value>59.99</value>\n        </entry>\n        <entry>\n            <key>Currency</key>\n            <value>USD</value>\n        </entry>\n    </eventProps>\n</Event>",
      "language": "typescript"
    }
  ]
}
[/block]
### Parquet
Parquet have timestamp, eventName, and eventProperties for each event. 
[block:callout]
{
  "type": "info",
  "body": "Parquet is an open source file format for Hadoop. Parquet stores nested data structures in a flat columnar format.",
  "title": "Parquet File Format"
}
[/block]