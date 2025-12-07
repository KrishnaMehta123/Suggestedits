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

1. Log in to your Microsoft Azure account and select *Storage Accounts* from the left menu.  
2. Click **+ Create** to create a new storage account. 

<Image alt="Select Storage Account from Left Manu" align="center" border={true} src="https://files.readme.io/214a3e7-Select_Storage_Account_from_the_left_menu.gif">
  Select Storage Account from Left Manu
</Image>

3. Enter the *Storage account name*, and do not modify the default settings.

<Image alt="Enter Storage Account Name" align="center" width="65% " border={true} src="https://files.readme.io/9304d54-Enter_Storage_Account_Name.png">
  Enter Storage Account Name
</Image>

4. Click **Review** and click **Create**. The following screen displays once the storage account is created:

<Image alt="Storage Account Created Successfully" align="center" width="65% " border={true} src="https://files.readme.io/102207f-Storage_Account_created_successfully.png">
  Storage Account Created Successfully
</Image>

The storage account you created now appears under the *Storage accounts* page.

## Create a Blob Service Container

To create a Blob Service Container:

1. Navigate to the *Blobs* menu under the *Blob Service* section of your storage account. 
2. Create **+ Container** to create a Blob Service Container within the storage account you created in the previous section.

<Image alt="Create a Blob Storage Container" align="center" width="80% " border={true} src="https://files.readme.io/9763f96-Create_Blob_Service_Container.gif">
  Create a Blob Storage Container
</Image>

3. Enter the *Name* of your Blob Service Container, and do not modify the other default settings.
4. Click **Create**.

<Image align="center" className="border" width="30% " border={true} src="https://files.readme.io/9e9032e-New_Container_popup.png" />

## Generate a SAS Token

A Shared Access Signature (SAS) Token is a Uniform Resource Identifier (URI) that provides limited access to an Azure Storage container. It is used when you want to authorize access to storage account assets within a defined time frame while keeping your storage account key confidential. For more information about SAS, refer to [Delegate access by using a SAS Token](https://learn.microsoft.com/en-gb/rest/api/storageservices/delegate-access-with-shared-access-signature).

To generate a SAS Token:

1. Select the *Container* and click the ![](https://files.readme.io/a593067-Ellipses_icon.png) icon.
2. Select *Generate SAS* from the dropdown list. The *Generate SAS* window opens on the right side of the screen.

<Image alt="Generate SAS Popup" align="center" width="60% " border={true} src="https://files.readme.io/6e76239-Generate_SAS_Token.png">
  Generate SAS Popup
</Image>

3. Enter the following details:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Signing method
      </td>

      <td>
        Select **Account key** from the Signing method list. The Signing method provides secure delegated access to resources in your storage account. For more information, refer to [Types of shared access signatures](https://learn.microsoft.com/en-us/azure/storage/common/storage-sas-overview#account-sas).
      </td>
    </tr>

    <tr>
      <td>
        Signing key
      </td>

      <td>
        Select any one key from the following options: <li> Key 1 </li> <li> Key 2 </li>.
      </td>
    </tr>

    <tr>
      <td>
        Stored access policy
      </td>

      <td>
        Select the *Stored access policy* you want to define for your storage. When defining a policy, you need to define the following: start time, expiry time, and permissions for the signature. To export data from CleverTap to Microsoft Azure, you need Read and Write permissions for the container.  

        When defined on a container, it grants permissions to the container itself or to the blobs that it contains. For more information, refer to [Define a stored access policy](https://learn.microsoft.com/en-us/rest/api/storageservices/define-stored-access-policy).
      </td>
    </tr>

    <tr>
      <td>
        Permissions
      </td>

      <td>
        This is a mandatory field. Select the permission for the request made with the service SAS. To export data from CleverTap to Microsoft Azure, you need Read and Write permissions for the container. If you have already assigned the required permissions to your stored access policy, the same permissions will be assigned to the request made with the service SAS. For more information, refer to [Account SAS Permissions by Operation](https://learn.microsoft.com/en-gb/rest/api/storageservices/create-account-sas#account-sas-permissions-by-operation).
      </td>
    </tr>

    <tr>
      <td>
        Start and expiry date/time
      </td>

      <td>
        Indicates the start and end date/time during which the blob SAS is valid. CleverTap recommends setting the expiration time to the maximum duration available. This is because you cannot export any data to the container if the expiration date has passed. For more information, refer to [Configure a SAS Expiration Policy](https://learn.microsoft.com/en-us/azure/storage/common/sas-expiration-policy?tabs=azure-portal#how-to-configure-a-sas-expiration-policy).
      </td>
    </tr>

    <tr>
      <td>
        Allowed IP address
      </td>

      <td>
        CleverTap recommends not adding any IP address range in this field. It indicates that Microsoft will accept export requests only from the IP address or range of IP addresses defined under this field. If you still want to add the IP address(es), you must whitelist the IP addresses listed under [CleverTap IP Ranges](https://developer.clevertap.com/docs/clevertap-ip-ranges).
      </td>
    </tr>

    <tr>
      <td>
        Allowed protocols
      </td>

      <td>
        Allowing requests over HTTPS only is recommended. This field indicates the protocols permitted for a request made with the service SAS.
      </td>
    </tr>
  </tbody>
</Table>

4. Click **Generate SAS token and URL**.

Copy the generated SAS token and URL, as you cannot access it later.

## Configure Microsoft Azure Blob Container on CleverTap Dashboard

To add your Microsoft Azure Blob Container to Clevertap:

1. Navigate to *Settings* > *Partners* and click **Integrate** against Mircosoft Azure. The *Integrate analytics partner - Microsoft Azure* window displays on the right side of the screen.

<Image alt="Integrate analytics partner - Microsoft Azure" align="center" width="60% " border={true} src="https://files.readme.io/372d7a1-MSAzure.jpg">
  Integrate analytics partner - Microsoft Azure
</Image>

2. Click **+ Microsoft Azure** to create a new bucket. The *Integrate Microsoft Azure Bucket* window opens on the right side of the screen. 
3. Enter the *Bucket Nickname*. 
4. Select the *Azure Blob Storage Endpoint*.
   * Default: Enter the Blob Storage Account name. 

<Image alt="Default Blob Storage Account on Microsoft Azure Portal" align="center" width="75% " border={true} src="https://files.readme.io/bb30e87-Default_Blob_Storage_Endpoint.png">
  Default Blob Storage Account on Microsoft Azure Portal
</Image>

* Custom: Add a custom domain mapped to your Azure Blob Storage Endpoint. For more information about defining a custom endpoint, refer to [Map a Custom Domain](https://learn.microsoft.com/en-gb/azure/storage/blobs/storage-custom-domain-name?tabs=azure-portal#map-a-custom-domain).

2. Enter the container name that stores data on Azure and the SAS token we obtained in Step 4 of the Generate a SAS Token section.

<Image alt="Integrate Microsoft Azure Bucket" align="center" width="60% " border={true} src="https://files.readme.io/a27cb22-image.png">
  Integrate Microsoft Azure Bucket
</Image>

# Create a New Data Export

To create a new data export, perform the following steps:

> 📘 Private Beta: Recurring Export for User Profiles
>
> Previously, handling large amounts of data and frequent updates led to duplication and higher storage needs. The new method uses scheduled transfers to manage resources more effectively and ease system load. We start with a full data export to set a complete base. Then, we only transfer updates or new data. This means that the profile exports will include less data than usual, considering only incremental updates will be exported. This reduces duplication and saves storage space, making data management more efficient.
>
> Currently, this feature is in Private Beta. To enable this feature for your account, contact your Customer Success Manager.

1. Navigate to **Settings** > **Partners** > **Exports**.
2. Click **Create Export** and select **Microsoft Azure**.

<Image alt="Create Export" align="center" width="90% " border={true} src="https://files.readme.io/d037cd2-CreateAzureExport.jpg">
  Create Export
</Image>

The **Export to Microsoft Azure** popup displays.

<Image alt="Enter Export Details" align="center" width="90% " border={true} src="https://files.readme.io/8256d08-AzureExport.jpg">
  Enter Export Details
</Image>

3. Configure the following settings:
   * **Partner Bucket name**: Name of the partner bucket. You can choose the required partner bucket from the drop-down list. 
   * **DATA TYPE & IDENTIFIER PRIORITY**: Select the events from the available options to export. For more information, refer to [Export Details](doc:data-export-to-aws-s3#export-details).
     * **Fallback priority orders for identifiers**: When exporting data, you can prioritize user identities. If you have selected multiple identities in the *User Identity* section, you can assign priorities 1, 2, and 3 to Email, Identity, and Phone Number. Users can then be identified based on these assigned priorities.\
       **NOTE**:  This feature applies only to *All events* and *All user properties* type.
   * **FREQUENCY**: Select from one of the following options:
     * **One time**: A single export for the selected export type. You can export data up to the last **60 days**. You create an export for a specific day, date range, previous month, current month, and more. 
     * **Recurring**: Set up a recurring export that exports all the new events captured in the last window. You can export data as frequently as every 4 hours and up to once every 24 hours.
     * **Dates to export data**: The export starts at 12:00 a.m. on the specified date by default.
   * **FORMAT**: Select from the following export formats: JSON, XML, CSV, and Parquet. For more information, refer to [Export Format](https://staging.docs.user.clevertap.net/docs/microsoft-azure-export#export-format-1).
   * **Export Data**: Enable *As string* to export data in string format.

4. Click **Export**. On clicking, the popup closes, and the following message displays at the top of the *Exports* page:

<Image alt="Microsoft Azure Export Initiated" align="center" width="90% " border={true} src="https://files.readme.io/b3a84b7-AzureExportInitiated.jpg">
  Microsoft Azure Export Initiated
</Image>

CleverTap processes the export, and you can now see the newly created export for Microsoft Azure.

The status for each export is displayed as *Pending* as soon as the export is created. The status changes to *Running* after the processing starts. And it changes to *Done* when the export is complete.

> 📘 Stop Export
>
> You can also stop the export that you have created. To do so, click the  ![Stop export](https://files.readme.io/203208a-StopExport.jpg) icon for the export request you want to stop, and then click **Stop** to confirm your action.

5. Confirm if your event data was successfully exported. To do so:\
   a. Log in to your Microsoft Azure account and select the Storage account under Resources.\
   b. Click the *Blob service* link under the *Properties* tab.\
   c. Select the *Container* where you exported the data.\
   d. (Optional) Click the **Switch to Acces Key** link if you encounter any authorization error after selecting the *Container*. 

<Image alt="New Export Displays on Microsoft Azure Dashboard" align="center" width="90% " border={true} src="https://files.readme.io/7c9e1a4-New_Export_Displays_on_Microsoft_Azure_Dashboard.gif">
  New Export Displays on Microsoft Azure Dashboard
</Image>

# Stop Export

You can also stop the export that you have created. Hover over the export. Click the **Stop** ![Stop export](https://files.readme.io/203208a-StopExport.jpg) button for the export request you want to stop.

<Image alt="Stop Amplitude Export" align="center" width="90% " border={true} src="https://files.readme.io/146b6e5-StopAzure.jpg">
  Stop Microsoft Azure Export
</Image>

The **Stop export?** window appears. Click **Stop** to confirm your action. 

<Image align="center" className="border" width="60% " border={true} src="https://files.readme.io/0ac7c40-image.png" />

You now return to the **Exports** page, and the *Microsoft Azure data export stopped* message displays at the top. The status of the export is displayed as *Stopped*.

<Image alt="Amplitude Export Stopped" align="center" width="90% " border={true} src="https://files.readme.io/c87565a-AzureStopped.jpg">
  Microsoft Azure Export Stopped
</Image>

# Edit an Export

You might need to modify an export to meet specific business requirements or while waiting for the next run. This section describes editing a Live Data Streaming and Recurring export in the **RUNNING** and **PENDING** (awaiting next run) state. 

> 📘 Points to Remember
>
> * In case of running exports, the new changes will apply to the next run.
> * You cannot edit a One-time export, regardless its status (RUNNING, PENDING, DONE, or STOPPED).
> * You cannot change the export from User Profile to Event and vice-versa.
> * You cannot modify exports marked as **DONE** or **STOPPED**.
> * Export changes for Live DataStreaming take 10-15 minutes to take effect.

To edit an export: 

1. On the CleverTap dashboard, go to **Partners** > **Exports**.
2. Hover over the required export. The **View**, **Edit**, and the **Stop** buttons appear.

<Image alt="Click the Edit Export Icon" align="center" width="90% " border={true} src="https://files.readme.io/aa99fa9-EditAzure.jpg">
  Click the Edit Export Icon
</Image>

3. Click the **Edit** button. The **Export to Segment** section appears.

<Image alt="Edit the Export" align="center" width="90% " border={true} src="https://files.readme.io/7557c24-EditExportAzure.jpg">
  Edit the Export
</Image>

4. Edit the export details and click **Update export**.

# Filter Exports

This section describes the different ways you can filter exports.

## Filter by Export Details

To filter by export details: 

1. Click the **Filter** button at the top right corner. 
2. You can filter exports by **Partner**, **Type**, **Format**, **Status**, or **Frequency**. 
3. To clear the filter, click **Reset all**.

<Image alt="Filter Exports" align="center" width="90% " border={true} src="https://files.readme.io/6499e90-FilterButton.jpg">
  Filter Exports
</Image>

## Filter Exports by Date Range

To filter exports by export date range:

1. Click the **Filter** button at the top right corner. 
2. Click the **Exported on** button.\
   The **Calendar** widget appears. 

<Image alt="Calendar Widget" align="center" width="90% " border={true} src="https://files.readme.io/74ce34b-Amplitude_Exports_-_Calendar_Widget.png">
  Calendar Widget
</Image>

3. Choose the custom date range and click **Apply**.\
   The exports are filtered accordingly.

## Filter Exports by Pagination

To choose how many export items you view per page:

1. Use the **Items per page** drop-down at the bottom of the **Exports** page.
2. Select one of the following options: 10, 20, 30, or 40. By default, the **Exports** page shows 20 exports.

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

For more information, refer to the following section.

# Export Format

This section provides information about the file format and the name format of the files exported to the S3 bucket.

## File Name Format

* **File Name Format for Event Export**\
   The example below shows the file name format for event export:
  * *Export request ID*: Indicates the export request ID generated when you create a request in the CleverTap dashboard.
  * *Timestamp of export run*: Indicates when the export was run.
  * *Event name*: Indicates the event type that is included in the file.
  * *File index*: We chunk the data across multiple files for larger exports. We limit file sizes to 100 MB chunks to make them more consumable. The file index indicates the file number in the file series. 
  * *Database ID*: Indicates the database ID of the CleverTap from where the file was exported. 
  * *File format*: Indicates the format of the file exported to the S3 bucket.  

```text
<export request id>-<timestamp of the export run>-<event name>-<yyyymmdd>-<file index>-<database-id>.json
```

* **File Name Format for User Profile Export**:\
   The example below shows the file name format for user profile export:
  * *Account ID*: Indicates the integer value for your CleverTap project ID. 
  * *Request ID*: Indicates the export request ID generated when you create a request in the CleverTap dashboard.
  * *Timestamp of export run*: Indicates when the export was run.
  * *Database ID*: Indicates the database ID of the CleverTap from where the file was exported. 
  * *File format*: Indicates the format of the file exported to the S3 bucket.

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

<Image title="Sample CSV File" alt={2032} align="center" src="https://files.readme.io/aa71f9f-Screenshot_2020-02-28_at_12.53.22_PM.png">
  Sample CSV File
</Image>

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
> * Parquet is an open-source file format for Hadoop. Parquet stores nested data structures in a flat columnar format.
> * Currently, exports in Parquet format are compressed as .parquet.gzip. Contact the customer support if you wish to get the file as .parquet i.e. without any additional compression.

## Prioritize User Identity for Exports

The export file includes an identity column with the user's Identity, Phone Number, or Email values. These values are set based on the identities configured in the CleverTap dashboard under the *Settings* > *User Identity* page. This feature lets you prioritize the identifier you want to export in the identity column. 

Let us understand how the prioritization works based on the identities selected in the *User Identity* page:

* If you select only *Identity*, export includes the identity value. The export file's identity column is empty if it is unavailable.\
  ![](https://files.readme.io/aad1f81-image.png)
* If you select multiple identifiers, you must set the priorities on the *Export* page. For instance, you set Priority 1 to *Identity* and Priority 2 to *Email ID*. When exporting data, the export prioritizes the Identity value for the identity column. If it is absent, the Email ID is exported under the identity column of the export file. If both are missing, the column remains empty.\
  ![](https://files.readme.io/52ae818-UserIdentity.jpg)

> 📘 Key Points to Remember
>
> * If you change the identity later, the export works according to the set priority. To prioritize the modified identities, edit your export.
> * This feature applies only to the following export types: *All events* and *All user profiles*.
> * For the old running export, this configuration or prirotization is not applicable. You can add the prioritization by editing the running exports.

To prioritize user identity for exports: 

1. Go to **Partners** > **Exports**. 
2. Hover over the required Microsoft Azure export. Click the **Edit** button.
3. Under **Fallback priority order for identifiers**, set up the priority 1, 2, and 3 for the required identities from the drop-down list.

<Image title="Enter export details and click Export" alt={1008} align="center" width="90% " border={true} src="https://files.readme.io/3411a5b-AzurePriority.jpg">
  Edit Export Priority
</Image>

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
