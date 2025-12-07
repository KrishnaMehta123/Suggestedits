---
title: Microsoft Azure
excerpt: Understand how to export data from CleverTap dashboard to Microsoft Azure.
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

[Microsoft Azure](https://azure.microsoft.com/en-in/), a Microsoft cloud computing platform, offers access to, management of, and development of applications and services through global data centers. The Microsoft Azure data export feature provides the capability to bulk export your CleverTap event data to Azure Blob Storage. You can use this for analysis in BI tools or storage in your data warehouse for analysis in the future.

# Setup

The following are the two major steps involved in enabling this feature for your account:

1. Create a Microsoft Azure Storage Account.
2. Create a Blob Service Container.
3. Generate a SAS Token.
4. Configure Microsoft Azure Blob Container details on the CleverTap Dashboard.

## Create a Microsoft Azure Storage Account

To create a Microsoft Azure Storage Account:

1. Log in to your Microsoft Azure account and select _Storage Accounts_ from the left menu.  
2. Click **+ Create** to create a new storage account. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/214a3e7-Select_Storage_Account_from_the_left_menu.gif",
        null,
        "Select Storage Account from Left Manu"
      ],
      "align": "center",
      "border": true,
      "caption": "Select Storage Account from Left Manu"
    }
  ]
}
[/block]


3. Enter the _Storage account name_, and do not modify the default settings.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9304d54-Enter_Storage_Account_Name.png",
        null,
        "Enter Storage Account Name"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Enter Storage Account Name"
    }
  ]
}
[/block]


4. Click **Review** and click **Create**. The following screen displays once the storage account is created:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/102207f-Storage_Account_created_successfully.png",
        null,
        "Storage Account Created Successfully"
      ],
      "align": "center",
      "sizing": "65% ",
      "border": true,
      "caption": "Storage Account Created Successfully"
    }
  ]
}
[/block]


The storage account you created now appears under the _Storage accounts_ page.

## Create a Blob Service Container

To create a Blob Service Container:

1. Navigate to the _Blobs_ menu under the _Blob Service_ section of your storage account. 
2. Create **+ Container** to create a Blob Service Container within the storage account you created in the previous section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9763f96-Create_Blob_Service_Container.gif",
        null,
        "Create a Blob Storage Container"
      ],
      "align": "center",
      "sizing": "80% ",
      "border": true,
      "caption": "Create a Blob Storage Container"
    }
  ]
}
[/block]


3. Enter the _Name_ of your Blob Service Container, and do not modify the other default settings.
4. Click **Create**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9e9032e-New_Container_popup.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "30% ",
      "border": true
    }
  ]
}
[/block]


## Generate a SAS Token

A Shared Access Signature (SAS) Token is a Uniform Resource Identifier (URI) that provides limited access to an Azure Storage container. It is used when you want to authorize access to storage account assets within a defined time frame while keeping your storage account key confidential. For more information about SAS, refer to [Delegate access by using a SAS Token](https://learn.microsoft.com/en-gb/rest/api/storageservices/delegate-access-with-shared-access-signature).

To generate a SAS Token:

1. Select the _Container_ and click the ![](https://files.readme.io/a593067-Ellipses_icon.png) icon.
2. Select _Generate SAS_ from the dropdown list. The _Generate SAS_ window opens on the right side of the screen.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6e76239-Generate_SAS_Token.png",
        null,
        "Generate SAS Popup"
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Generate SAS Popup"
    }
  ]
}
[/block]


3. Enter the following details:

[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "0-0": "Signing method",
    "0-1": "Select **Account key** from the Signing method list. The Signing method provides secure delegated access to resources in your storage account. For more information, refer to [Types of shared access signatures](https://learn.microsoft.com/en-us/azure/storage/common/storage-sas-overview#account-sas).",
    "1-0": "Signing key",
    "1-1": "Select any one key from the following options: <li> Key 1 </li> <li> Key 2 </li>.",
    "2-0": "Stored access policy",
    "2-1": "Select the _Stored access policy_ you want to define for your storage. When defining a policy, you need to define the following: start time, expiry time, and permissions for the signature. To export data from CleverTap to Microsoft Azure, you need Read and Write permissions for the container.  \n  \nWhen defined on a container, it grants permissions to the container itself or to the blobs that it contains. For more information, refer to [Define a stored access policy](https://learn.microsoft.com/en-us/rest/api/storageservices/define-stored-access-policy).",
    "3-0": "Permissions",
    "3-1": "This is a mandatory field. Select the permission for the request made with the service SAS. To export data from CleverTap to Microsoft Azure, you need Read and Write permissions for the container. If you have already assigned the required permissions to your stored access policy, the same permissions will be assigned to the request made with the service SAS. For more information, refer to [Account SAS Permissions by Operation](https://learn.microsoft.com/en-gb/rest/api/storageservices/create-account-sas#account-sas-permissions-by-operation).",
    "4-0": "Start and expiry date/time",
    "4-1": "Indicates the start and end date/time during which the blob SAS is valid. CleverTap recommends setting the expiration time to the maximum duration available. This is because you cannot export any data to the container if the expiration date has passed. For more information, refer to [Configure a SAS Expiration Policy](https://learn.microsoft.com/en-us/azure/storage/common/sas-expiration-policy?tabs=azure-portal#how-to-configure-a-sas-expiration-policy).",
    "5-0": "Allowed IP address",
    "5-1": "CleverTap recommends not adding any IP address range in this field. It indicates that Microsoft will accept export requests only from the IP address or range of IP addresses defined under this field. If you still want to add the IP address(es), you must whitelist the IP addresses listed under [CleverTap IP Ranges](https://developer.clevertap.com/docs/clevertap-ip-ranges).",
    "6-0": "Allowed protocols",
    "6-1": "Allowing requests over HTTPS only is recommended. This field indicates the protocols permitted for a request made with the service SAS."
  },
  "cols": 2,
  "rows": 7,
  "align": [
    "left",
    "left"
  ]
}
[/block]


4. Click **Generate SAS token and URL**.

Copy the generated SAS token and URL, as you cannot access it later.

## Configure Microsoft Azure Blob Container on CleverTap Dashboard

To add your Microsoft Azure Blob Container to Clevertap:

1. Navigate to _Settings_ > _Partners_ and click **Integrate** against Mircosoft Azure. The _Integrate analytics partner - Microsoft Azure_ window displays on the right side of the screen.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/372d7a1-MSAzure.jpg",
        null,
        "Integrate analytics partner - Microsoft Azure"
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Integrate analytics partner - Microsoft Azure"
    }
  ]
}
[/block]


2. Click **+ Microsoft Azure** to create a new bucket. The _Integrate Microsoft Azure Bucket_ window opens on the right side of the screen. 
3. Enter the _Bucket Nickname_. 
4. Select the _Azure Blob Storage Endpoint_.
   - Default: Enter the Blob Storage Account name. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bb30e87-Default_Blob_Storage_Endpoint.png",
        null,
        "Default Blob Storage Account on Microsoft Azure Portal"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Default Blob Storage Account on Microsoft Azure Portal"
    }
  ]
}
[/block]


- Custom: Add a custom domain mapped to your Azure Blob Storage Endpoint. For more information about defining a custom endpoint, refer to [Map a Custom Domain](https://learn.microsoft.com/en-gb/azure/storage/blobs/storage-custom-domain-name?tabs=azure-portal#map-a-custom-domain).

2. Enter the container name that stores data on Azure and the SAS token we obtained in Step 4 of the Generate a SAS Token section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a27cb22-image.png",
        null,
        "Integrate Microsoft Azure Bucket"
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Integrate Microsoft Azure Bucket"
    }
  ]
}
[/block]


<br />

# Create export

To begin, you first create a new export from the CleverTap dashboard. This step connects your CleverTap account with a partner destination and sets the context for the configuration that follows.

1. Navigate to _Settings_ → _Partners_ and click **Create Export**. 

   [block:image]{"images":[{"image":["https://files.readme.io/6d308e01cc3dc940760f1c76ee5cecffda32a57b8db946c62d3e125af9c15d75-export_center_profile_1.png","","Create Export"],"align":"center","border":true,"caption":"Create Export"}]}[/block]
2. In _Export Setup_, under _Data type_, select **Profiles**. Click **Next**. 

   [block:image]{"images":[{"image":["https://files.readme.io/5c7972185b625c21e9b8e3dd538630e7c917584f95c90cccca70fb876021f7fa-data_type_profiles_.png","","Data Type - Profiles"],"align":"center","sizing":"65% ","border":true,"caption":"Data Type - Profiles"}]}[/block]
3. Under _Partner_, select where you want to send the export and Click **Start**. Selecting a partner affects the first field you’ll see in _Storage & file details_: it appears as _Storage bucket_ for Amazon S3 and Google Cloud, and as _Storage blob_ for Microsoft Azure.

   - **Amazon S3**
   - **Google Cloud**
   - **Microsoft Azure** 

     [block:image]{"images":[{"image":["https://files.readme.io/353438c2d86d5c956db69fb1e54c319b25ace89c7951fe05772d9768e3692f2c-partner_export_profile.png","","Select Partner"],"align":"center","sizing":"65% ","border":true,"caption":"Select Partner"}]}[/block]

# Legacy Export

The **Export to Microsoft Azure** popup displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8256d08-AzureExport.jpg",
        null,
        "Enter Export Details"
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
   - **DATA TYPE & IDENTIFIER PRIORITY**: Select the events from the available options to export. For more information, refer to [Export Details](doc:data-export-to-aws-s3#export-details).
     - **Fallback priority orders for identifiers**: When exporting data, you can prioritize user identities. If you have selected multiple identities in the _User Identity_ section, you can assign priorities 1, 2, and 3 to Email, Identity, and Phone Number. Users can then be identified based on these assigned priorities.  
       **NOTE**:  This feature applies only to _All events_ and _All user properties_ type.
   - **FREQUENCY**: Select from one of the following options:
     - **One time**: A single export for the selected export type. You can export data up to the last **60 days**. You create an export for a specific day, date range, previous month, current month, and more. 
     - **Recurring**: Set up a recurring export that exports all the new events captured in the last window. You can export data as frequently as every 4 hours and up to once every 24 hours.
     - **Dates to export data**: The export starts at 12:00 a.m. on the specified date by default.
   - **FORMAT**: Select from the following export formats: JSON, XML, CSV, and Parquet. For more information, refer to [Export Format](https://staging.docs.user.clevertap.net/docs/microsoft-azure-export#export-format-1).
   - **Export Data**: Enable _As string_ to export data in string format.

4. Click **Export**. On clicking, the popup closes, and the following message displays at the top of the _Exports_ page:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b3a84b7-AzureExportInitiated.jpg",
        null,
        "Microsoft Azure Export Initiated"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Microsoft Azure Export Initiated"
    }
  ]
}
[/block]


CleverTap processes the export, and you can now see the newly created export for Microsoft Azure.

The status for each export is displayed as _Pending_ as soon as the export is created. The status changes to _Running_ after the processing starts. And it changes to _Done_ when the export is complete.

> 📘 Stop Export
> 
> You can also stop the export that you have created. To do so, click the  ![](https://files.readme.io/203208a-StopExport.jpg) icon for the export request you want to stop, and then click **Stop** to confirm your action.

5. Confirm if your event data was successfully exported. To do so:  
   a. Log in to your Microsoft Azure account and select the Storage account under Resources.  
   b. Click the _Blob service_ link under the _Properties_ tab.  
   c. Select the _Container_ where you exported the data.  
   d. (Optional) Click the **Switch to Acces Key** link if you encounter any authorization error after selecting the _Container_. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7c9e1a4-New_Export_Displays_on_Microsoft_Azure_Dashboard.gif",
        null,
        "New Export Displays on Microsoft Azure Dashboard"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "New Export Displays on Microsoft Azure Dashboard"
    }
  ]
}
[/block]


# Export Details

## Export Type

- **All user events**: This exports data for all events that have been defined, which include _System_ and _Custom_ events. 
- **Select events**: This exports specific events you want to export. 
- **All user profiles**: This exports all your user profile data.

## Export Frequency

- **One time**: Single export for the export type selected. You can export data up to the last 60 days. 
- **Recurring**: Set up a recurring export that exports all the new events/user profiles captured in the last window. You can export as frequently as every 4 hours and up to once every 24 hours. 

## Export Format

- JSON
- XML
- CSV
- Parquet

For more information, refer to the following section.

# Export Format

This section provides information about the file format and the name format of the files exported to the S3 bucket.

## File Name Format

- **File Name Format for Event Export**  
   The example below shows the file name format for event export:
  - _Export request ID_: Indicates the export request ID generated when you create a request in the CleverTap dashboard.
  - _Timestamp of export run_: Indicates when the export was run.
  - _Event name_: Indicates the event type that is included in the file.
  - _File index_: We chunk the data across multiple files for larger exports. We limit file sizes to 100 MB chunks to make them more consumable. The file index indicates the file number in the file series. 
  - _Database ID_: Indicates the database ID of the CleverTap from where the file was exported. 
  - _File format_: Indicates the format of the file exported to the S3 bucket.  

```text
<export request id>-<timestamp of the export run>-<event name>-<yyyymmdd>-<file index>-<database-id>.json
```

- **File Name Format for User Profile Export**:  
   The example below shows the file name format for user profile export:
  - _Account ID_: Indicates the integer value for your CleverTap project ID. 
  - _Request ID_: Indicates the export request ID generated when you create a request in the CleverTap dashboard.
  - _Timestamp of export run_: Indicates when the export was run.
  - _Database ID_: Indicates the database ID of the CleverTap from where the file was exported. 
  - _File format_: Indicates the format of the file exported to the S3 bucket.

```text
<account id>-<request id>-<timestamp of the export run>-<database-id>-<file format>.gz
```

## File Data Format

Files are split by event names for event exports, and each file will have all event data for the given period for the event.

### JSON

The first line of the file contains the event name. After the first line, each line in JSON describes the timestamp, object id, and event properties.

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

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/aa71f9f-Screenshot_2020-02-28_at_12.53.22_PM.png",
        "Sample CSV File",
        2032
      ],
      "align": "center",
      "caption": "Sample CSV File"
    }
  ]
}
[/block]


### XML

XML has the timeStamp, eventName, followed by eventProperties.

```typescript
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
> - Currently, exports in Parquet format are compressed as .parquet.gzip. Contact the customer support if you wish to get the file as .parquet i.e. without any additional compression.

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
2. Hover over the required Microsoft Azure export. Click the **Edit** button.
3. Under **Fallback priority order for identifiers**, set up the priority 1, 2, and 3 for the required identities from the drop-down list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3411a5b-AzurePriority.jpg",
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

# FAQ

### Q. How do you secure the data exports from CleverTap to Microsoft Azure?

A. You can whitelist IPs to ensure that CleverTap will only have access to push data to your Microsoft Azure bucket. To get the list of IP Whitelisting, refer to the [IP Whitelisting](https://docs.clevertap.com/docs/ip-whitelisting) documentation.

### Q. What customer-related errors can stop exports, and how are customers notified when interruptions occur?

A. Exports can stop due to customer-related errors. For example, invalid/expired credentials or a missing partner bucket. CleverTap emails customers about the issue to ensure timely resolution. 

Here are the customer-related errors that can stop Microsoft Azure export: 

| Error Code | Error Message                     | Cause and Resolution                                                                                                                                                                                                                                                                                       |
| :--------- | :-------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Unknown    | Azure SAS token is expired.       | You must create a new Azure SAS token and set it up in CleverTap. For more information, refer to [Generate a SAS Token](https://staging.docs.user.clevertap.net/docs/microsoft-azure-export#generate-a-sas-token).                                                                                         |
| Unknown    | Azure SAS token is not yet valid. | The Azure SAS token is valid on a future date. Ensure you generate a new Azure SAS token with the correct validity start date and set it up in CleverTap. For more information, refer to [Generate a SAS Token](https://staging.docs.user.clevertap.net/docs/microsoft-azure-export#generate-a-sas-token). |

Exports are checked every hour for failures. If an error occurs, CleverTap sends three emails to the export creator within a span of three days. Emails 1 and 2 include the error details and a link to fix it. It warns that the export will stop if the problem is not fixed within three days. Email 3 notifies the creator that CleverTap has stopped the export.