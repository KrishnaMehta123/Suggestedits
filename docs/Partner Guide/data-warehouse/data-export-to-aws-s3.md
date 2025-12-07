---
title: AWS S3 Export
excerpt: Understand how to export data from CleverTap dashboard to AWS S3.
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

The data export feature provides the capability to bulk export your CleverTap event data to your AWS S3 bucket. You can use this for analysis in BI tools or storage in your data warehouse for analysis in the future.

> 📘 Feature Availability
>
> This capability is a part of the *CleverTap for Enterprises* plan. To activate this for your account, contact your sales account manager.

# Setup

The following are the two major steps involved in enabling this feature for your account:

1. [Create an AWS S3 Bucket](doc:data-export-to-aws-s3#create-an-aws-s3-bucket).
2. Configure Buckets details on the CleverTap Dashboard using one of the following methods:
   * [Using Access Key](doc:data-export-to-aws-s3#using-access-key)
   * [Using IAM Policy](doc:data-export-to-aws-s3#using-iam-policy)

## Create an AWS S3 Bucket

To create an AWS S3 bucket:

1. Log in to your AWS account, then search for *S3* in the AWS services box. 
2. Select *S3* from the search results. 

<Image title="Select S3 from AWS account" alt={891} align="center" border={true} src="https://files.readme.io/bb8d83c-Selecting_S3_from_the_list.png">
  Select S3 from AWS Account 
</Image>

   On clicking, the *Bucket* page displays.

3. Click **Create bucket**. On clicking, the *Create bucket* page displays:

<Image title="Click Create bucket from Buckets page" alt={2876} align="center" border={true} src="https://files.readme.io/111a267-Bucket_page.png">
  Click Create Bucket
</Image>

4. Enter a bucket name, region, logging, versioning, and encryption preferences. 

<Image title="Enter General Configuration for S3 bucket and click Create bucket" alt={1628} align="center" width="80%" border={true} src="https://files.readme.io/407acf4-Create_bucket_page.png">
  Configure S3 Bucket Settings and Click Create Bucket 
</Image>

> 📘 Recommendation for Setup
>
> For this integration, you need not modify the default settings; however, you must check your internal organization's policies to verify if you need to modify any of these settings.

Based on your CleverTap account settings, we host your data in Europe (EU), the United States (US), Singapore (SG), or India (IN). To identify the region of your account and the corresponding region that you must select when configuring the bucket settings, refer to the following table:

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        CleverTap Dashboard URL
      </th>

      <th>
        Region
      </th>

      <th>
        AWS S3 Bucket Region
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        [https://eu1.dashboard.clevertap.com/login.html](https://eu1.dashboard.clevertap.com/login.html#/)
      </td>

      <td>
        EU
      </td>

      <td>
        EU (Ireland) eu-west-1
      </td>
    </tr>

    <tr>
      <td>
        [https://in1.dashboard.clevertap.com/login.html](https://in1.dashboard.clevertap.com/login.html#/)
      </td>

      <td>
        India
      </td>

      <td>
        Asia Pacific (Mumbai) ap-south-1
      </td>
    </tr>

    <tr>
      <td>
        [https://us1.dashboard.clevertap.com/login.html](https://us1.dashboard.clevertap.com/login.html#/)
      </td>

      <td>
        US
      </td>

      <td>
        US West (Oregon) us-west-2
      </td>
    </tr>

    <tr>
      <td>
        [https://sg1.dashboard.clevertap.com/login.html](https://sg1.dashboard.clevertap.com/login.html#/)
      </td>

      <td>
        Singapore
      </td>

      <td>
        Asia Pacific (Singapore)\
        ap-southeast-1
      </td>
    </tr>

    <tr>
      <td>
        [https://sk1.dashboard.clevertap.com/login.html](https://sk1.dashboard.clevertap.com/login.html#/)
      </td>

      <td>
        South Korea
      </td>

      <td>
        Asia Pacific (Seoul)\\nap-northeast-2
      </td>
    </tr>
  </tbody>
</Table>

> 📘 Set Up AWS Bucket Region
>
> When setting up the AWS bucket region for your AWS account, ensure that the AWS bucket region matches your CleverTap account region. To identify the region of your CleverTap account, refer to the above table. 
>
> Also, you can set up the CleverTap account region only once during registration.

5. Click **Create bucket**. On successful bucket creation, the following message displays in the snack bar at the top:

<Image title="S3 Bucket created successfully message displays at the top" alt={2770} align="center" border={true} src="https://files.readme.io/681e832-Successful_bucket_creation.png">
  S3 Bucket Created Successfully
</Image>

The bucket you just created now shows up on your S3 console. We recommend you note down the name of your new bucket, as you will need it for the next step.

## Configure S3 Bucket Details on CleverTap Dashboard

### Using IAM Policy

The following are the two major steps to perform this task:\
i. [Copy IAM Policy from the CleverTap dashboard](doc:data-export-to-aws-s3#copy-iam-policy-from-the-clevertap-dashboard)\
ii. [Add IAM Policy to S3 Bucket from AWS console](doc:data-export-to-aws-s3#add-iam-policy-to-s3-bucket-on-aws-console). 

#### Copy IAM Policy from the CleverTap Dashboard

To copy the IAM policy from the CleverTap dashboard:

1. Navigate to *Settings* > *Partners* and click **View Details** against Amazon S3. The *Integrate analytics partner - Amazon S3* window displays on the right side of the screen.

<Image title="Click View Details against Amazon S3 from Partner page" alt={1500} align="center" width="80%" border={true} src="https://files.readme.io/27118b6-Integrate_Analytics_Partner_-_AWS_S3.png">
  Click View Details against Amazon S3 from Partner Page
</Image>

2. Click **+ Amazon S3 Bucket** to create a new bucket.
3. Enter the *Bucket name*. 
4. Select *IAM (Identity and Access Management) Policy* option under *Configure with* section.

<Image title="Enter Bucket URL and select IAM Policy option" alt={1446} align="center" width="80%" border={true} src="https://files.readme.io/475094f-Select_IAM_Policy_option.png">
  Configure S3 Bucket with IAM Policy
</Image>

5. Click the ![Copy](https://files.readme.io/2bd537e-Copy_icon.png) icon to copy the policy to the clipboard and keep this window open for saving these details later.

#### Add IAM Policy to S3 Bucket on AWS Console

To add IAM policy to the S3 bucket:

1. Select the bucket from the Bucket page of the AWS console.
2. Select the *Permissions* tab.
3. Click **Edit** under the *Bucket policy* section and enter the policy that you copied in Step *4* of [Copy IAM Policy from the CleverTap dashboard](doc:data-export-to-aws-s3#copy-iam-policy-from-the-clevertap-dashboard):

<Image title="Click Edit to edit S3 bucket policy" alt={2052} align="center" width="80%" border={true} src="https://files.readme.io/438b0da-Add_IAM_policy_to_S3_Bucket.png">
  Edit S3 Bucket Policy
</Image>

```json IAM Policy
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:iam::062484260092:root"
            },
            "Action": "s3:PutObject*",
            "Resource": "arn:aws:s3:::bucket-name/*"
        },
        {
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:iam::062484260092:root"
            },
            "Action": "s3:PutObject*",
            "Resource": "arn:aws:s3:::bucket-name"
        }
    ]
}
```

> 🚧 IMPORTANT
>
> Ensure that you replace all the occurrences of `bucket-name` in the above JSON payload with your actual bucket name.

4. Click **Save Changes** to save the policy.
5. Go back to the same window opened in *Step 4* of [Copy IAM Policy From CleverTap Dashboard](doc:data-export-to-aws-s3#copy-iam-policy-from-the-clevertap-dashboard) and click **Save Credentials**.\
   Amazon S3 bucket is now configured on both the AWS S3 console and CleverTap dashboard. 

### Using Access Key

The following are the two major steps to perform this task:\
i. [Create an API Key for Your S3 Bucket](doc:data-export-to-aws-s3#create-an-api-key-for-your-s3-bucket).\
ii. [Add Your S3 Bucket Details to CleverTap](doc:data-export-to-aws-s3#add-your-s3-bucket-details-to-clevertap).

#### Create an API Key for Your S3 Bucket

This section demonstrates the creation of an AWS API key with write access to the bucket we created in the above step. CleverTap uses this API key to export data to your S3 bucket.

1. Click on your account name on the top right of the AWS console.
2. Select *Security credentials*.

<Image title="Select Security credentials option" alt={388} align="center" width="smart" border={true} src="https://files.readme.io/152163f-Security_credentials.png">
  Select Security credentials
</Image>

3. Select *Users* from the left navigation and click **Add user**.

<Image title="Click Add users from the User page" alt={2878} align="center" border={true} src="https://files.readme.io/8b81e57-Click_Add_users.png">
  Add Users
</Image>

On clicking, the *Add user* page displays.

4. Enter the *User name* and select the *Programmatic access* checkbox.
5. Click **Next:Permissions**.

<Image title="Enter the User name, select AWS credential type and click Next: Permissions" alt={2878} align="center" border={true} src="https://files.readme.io/7840a59-Add_user.png">
  Select AWS Access Type and Click Next: Permissions
</Image>

On clicking, *Set permissions* page displays.

6. Click **Create group** under *Add user to group* tab.

<Image title="Click Create group under Add user to group tab" alt={2872} align="center" border={true} src="https://files.readme.io/592634b-Create_group.png">
  Add User to Group
</Image>

On clicking, *Create group* page displays.

<Image title="Assign policy to group" alt={2482} align="center" border={true} src="https://files.readme.io/5cfd145-Create_group_page.png">
  Assign Policy to Group
</Image>

7. Click **Create policy**. On clicking, *Create policy* page opens in a new tab.
8. Select the **JSON** tab and then paste the JSON code given below in the box. 
9. Replace `clevertap-example` in the JSON code with the name of the S3 bucket you created in the above step.\
   The permissions defined in this policy allow CleverTap to get information about your bucket and upload files to it.

> 📘 AWS API Access Policies
>
> *IP Whitelisting* is not supported with S3 exports. For more information about AWS API access policies, refer to [this post](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_examples_s3_rw-bucket-console.html) from the AWS blog.

<Image title="Bucket policy in JSON format" alt={2874} align="center" border={true} src="https://files.readme.io/bc21bb7-Replace_JSON_code.png">
  Bucket Policy in JSON Format
</Image>

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3:ListBucket"
            ],
            "Resource": [
                "arn:aws:s3:::clevertap-example"
            ]
        },
        {
            "Effect": "Allow",
            "Action": [
                "s3:PutObject"
            ],
            "Resource": [
                "arn:aws:s3:::clevertap-example/*"
            ]
        }
    ]
}
```

10. Click **Next: Tags**  and then click **Next: Review**. On clicking, the *Create policy* page opens.
11. Enter the policy *Name* and click **Create policy**.

<Image title="Enter policy name and click Create policy" alt={2648} align="center" border={true} src="https://files.readme.io/f81305a-Create_policy.png">
  Enter Policy Name and Click Create policy
</Image>

On successful policy creation, the following message displays in the snack bar at the top:

<Image title="Policy created successfully message displays at the top" alt={2870} align="center" border={true} src="https://files.readme.io/cc7b89a-Policy_created_successfully.png">
  Bucket  Policy Created Successfully
</Image>

12. Go back to the *Create group* page (opened in *Step 6*), search for the policy you just created, and assign it to the new group by selecting the checkbox.
13. Click **Create group**. On clicking, the *Add user* page displays.

<Image title="SSelect Policy and Click Create Group" alt={2486} align="center" border={true} src="https://files.readme.io/c28e813-Search_policy.png">
  Select Policy and Click Create Group
</Image>

14. Click **Next: Tags** and then click **Next: Review**.

<Image title="Click Next: Tags.png" alt={2012} align="center" border={true} src="https://files.readme.io/15f1ead-Click_Next_Tags.png">
  Click Next: Tags
</Image>

15. Click **Create user**. 

<Image title="Click Create user" alt={1980} align="center" border={true} src="https://files.readme.io/d88007d-Create_user.png">
  Click Create user
</Image>

On successful user creation, the following page displays. You will see your *Access key ID* and the *Secret access key*. 

<Image title="Copy or download Access key ID and Secret access key" alt={2878} align="center" border={true} src="https://files.readme.io/d3b1def-Access_key_and_secret_access_key.png">
  Copy or Download User Security Credentials
</Image>

These credentials allow CleverTap to upload files to your S3 bucket. We recommend you note down these values as you will require them for the next step. Otherwise, you can also click **Download .csv** to save these details for future use.

#### Add Your S3 Bucket Details to CleverTap

To add your S3 bucket details to Clevertap, perform the following steps:

1. Navigate to *Settings* > *Partners* and click **View Details** against Amazon S3. The *Integrate analytics partner - Amazon S3* window displays on the right side of the screen.

<Image title="Integrate Analytics Partner - AWS S3.png" alt={1500} align="center" border={true} src="https://files.readme.io/6ab03f2-Integrate_Analytics_Partner_-_AWS_S3.png">
  Click View Details against Amazon S3 from Partners Page
</Image>

2. Click **+ Amazon S3 Bucket** to create a new bucket. The *Integrate Amazon S3 Bucket* window opens on the right side of the screen. 
3. Enter the *Bucket nickname* and *Bucket URL*. 
4. Select the *User details* option under *Configure with* section.
5. Enter your *Access key ID* and the *Secret access key* obtained earlier and click **Save Credentials**.

<Image title="Select User details and enter the user security credentials" alt={1494} align="center" border={true} src="https://files.readme.io/5f44e48-Select_User_details_option.png">
  Enter User Security Credentials and Click Save Credentials 
</Image>

# Create a New Data Export

To create a new data export:

> 📘 Private Beta: Recurring Export for User Profiles
>
> Previously, handling large amounts of data and frequent updates led to duplication and higher storage needs. The new method uses scheduled transfers to manage resources more effectively and ease system load. We start with a full data export to set a complete base. Then, we only transfer updates or new data. This means that the profile exports will include less data than usual, considering only incremental updates will be exported. This reduces duplication and saves storage space, making data management more efficient.
>
> Currently, this feature is in Private Beta. To enable this feature for your account, contact your Customer Success Manager.

1. Navigate to **Settings** > **Partners** > **Exports**.
2. Click **Create Export** and select **Amazon S3**.

<Image title="Select Amazon S3 from the partner list" alt={2426} align="center" width="90% " border={true} src="https://files.readme.io/a562833-CreateS3Export.jpg">
  Create Export
</Image>

The **Export to Amazon S3** pop-up displays.

<Image title="Enter export details and click Export" alt={1008} align="center" width="90% " border={true} src="https://files.readme.io/13a408d-CreateAmazonS3Export.jpg">
  Enter Export Details
</Image>

3. Configure the following settings:
   * **Partner Bucket name**:  Name of the partner bucket. Choose the required partner bucket name from the drop-down. 
   * **DATA TYPE & IDENTIFIER PRIORITY**: Select the events from the available options to export. For more information, refer to [Export Details](doc:data-export-to-aws-s3#export-details).
     * **Fallback Priority order for identities**: Select priority for user identities when exporting data. User Identifiers will be exported based on selected priority. For more information, refer to the [Prioritize User Identity for Exports](https://staging.docs.user.clevertap.net/docs/data-export-to-aws-s3#prioritize-user-identity-for-exports) section. 
   * **FREQUENCY**: Select from one of the following options:
     * **One time**: A single export for the selected export type. You can export data up to the last **60 days**. You create an export for a specific day, date range, previous month, current month, and more.
     * **Recurring**: Set up a recurring export that exports all the new events captured in the last window. You can export data as frequently as every 4 hours and up to once every 24 hours.
     * **Dates to export data**: The export starts at 12:00 a.m. on the specified date by default.
   * **FORMAT**: Select from the following export formats: JSON, XML, CSV, and Parquet. For more information, refer to [Export Format](https://staging.docs.user.clevertap.net/docs/data-export-to-aws-s3#export-format-1).
     * **Export Data**: If you choose **As string**, the data is sent as a string. If you do not select the box, data is sent in its original format.

4. Click **Export**. On clicking, the popup closes, and the following message displays at the top of the *Exports* page: 

<Image title="Amazon S3 export initiated message displays at the top.png" alt={2362} align="center" border={true} src="https://files.readme.io/b7d314e-S3ExportInitiated.jpg">
  Amazon S3 Export Initiated
</Image>

CleverTap processes the export, and you can now see the newly created export for AWS S3.

<Image title="New Amazon S3 export displays on Exports page" alt={2426} align="center" border={true} src="https://files.readme.io/04e088a-S3ExportPending.jpg">
  New Amazon S3 Export Displays on Exports Page
</Image>

The status for each export is displayed as **PENDING** as soon as the export is created. The status changes to **RUNNING** after the processing starts. And it changes to **DONE** when the export is complete.

> 📘 Stop Export
>
> You can also stop the export that you have created. To do so, click the  ![Stop export](https://files.readme.io/203208a-StopExport.jpg) Stop Export\
>  icon for the export request you want to stop, and then click **Stop** to confirm your action.

5. Confirm if your event data was successfully exported. To do so:\
   a. Log in to your AWS account and navigate to the *S3* console.\
   b. Search your *Bucket* from the *Buckets* page and then click the bucket name.\
   c. Copy the *Request ID* from the activity log and search with that ID. You should see your respective file there. 

<Image title="Search for new Amazon S3 export on Amazon S3 Dashboard" alt={2842} align="center" border={true} src="https://files.readme.io/217fe0e-Search_for_export_files.png">
  New Amazon S3 Export Displays on Amazon S3 Dashboard
</Image>

# Stop Export

You can also stop the export that you have created. Hover over the required export. The **View**, **Edit**, and **Stop** buttons appear. Click the **Stop**  ![Stop export](https://files.readme.io/203208a-StopExport.jpg) button for the export request you want to stop.

<Image alt="Stop Amplitude Export" align="center" width="90% " border={true} src="https://files.readme.io/057c29d-StopAWSS3.jpg">
  Stop Amazon S3 Export
</Image>

The **Stop export?** window appears. Click **Stop** to confirm your action. 

<Image align="center" className="border" width="60% " border={true} src="https://files.readme.io/f941b8e-StopS3Button.jpg" />

You now return to the *Exports* page, and the *Amazon S3 data export stopped* message displays at the top. The status of the export is displayed as **STOPPED**.

<Image alt="Amplitude Export Stopped" align="center" width="90% " border={true} src="https://files.readme.io/31783ec-StoppedS3.jpg">
  Amazon S3 Export Stopped
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

1. On the CleverTap dashboard, go to *Partners* > *Exports*.
2. Hover over the export. The **View**, **Edit**, and the **Stop** buttons appear. 

<Image alt="Click the Edit Export Icon" align="center" width="90% " border={true} src="https://files.readme.io/e048c7d-EditAWSS3.jpg">
  Click the Edit Export Icon
</Image>

3. Click the **Edit** button. The **Export to Amazon S3** section appears.

<Image alt="Edit the Export" align="center" width="90% " border={true} src="https://files.readme.io/a79ec21-ExportToAmazonS3.jpg">
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

You can also filter the exports based on the export date. 

To filter exports by export date range:

1. Click the **Filter** button at the top right corner. 
2. Click the **Exported on** button.\
   The **Calendar** widget appears. 

   <Image align="center" className="border" width="80% " border={true} src="https://files.readme.io/0cf145e-CalendarWidget.jpg" />
3. Choose the custom date range and click **Apply**.\
   The exports are filtered accordingly.

## Filter Exports by Pagination

To choose how many export items you view per page:

1. Use the **Items per page** drop-down at the bottom of the **Exports** page.
2. Options include 10, 20, 30, or 40. By default, the **Exports** page shows 20 exports.

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
> * Currently, exports in Parquet format are compressed as **.parquet.gzip**. Contact the Customer Support Team to obtain **.parquet** files, that is, files without any additinal compression.

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
2. Hover over the required AWS S3 export. Click the **Edit** button.
3. Under **Fallback priority order for identifiers**, set up the priority 1, 2, and 3 for the required identities from the drop-down list.

<Image title="Enter export details and click Export" alt={1008} align="center" width="90% " border={true} src="https://files.readme.io/47d17d5-AWS3Priority.jpg">
  Edit Export Priority
</Image>

4. Click **Update export**.

# FAQs

### Q. What permission is required for CleverTap to export data to your AWS S3 bucket?

A. CleverTap needs write permission to be able to export data to your AWS S3 bucket, as shown in the following figure:

<Image title="IAM Policy to provide CleverTap with write access" alt={1446} align="center" width="80%" border={true} src="https://files.readme.io/7bed273-Select_IAM_Policy_option.png">
  IAM Policy to Provide CleverTap with Write Access
</Image>

### Q. What should I do if I already have an existing IAM policy for the AWS S3 bucket?

A. Ensure that you modify the current IAM policy to provide CleverTap with write access to export data to your AWS S3 bucket.

### Q. Do CleverTap data exports allow special characters?

A. Yes, CleverTap data exports allow the following special characters:

* CleverTap's export system supports Unicode (UTF-8)  character encoding. It facilitates the accurate representation of text in various languages and scripts. For example, Indian regional languages, Arabic, Korean, Russian, Japanese, Chinese, Spanish, Greek, Indonesian, etc.
* It replaces the following characters with a hyphen to avoid issues in output file generation:
  * Whitespace
  * Tab
  * Slash
  * null (\\0)
* Control characters are replaced with ?. For more information, refer to [Control Character](https://en.wikipedia.org/wiki/Control_character). 
* Supports emoji characters; however, some emojis (UTF-16) may not render properly.

### Q. What customer-related errors can stop exports, and how are customers notified when interruptions occur?

A. Export processes can stop due to customer-related errors. For example, invalid/expired credentials or a missing partner bucket. CleverTap emails customers about the issue to ensure timely resolution. 

Here are the customer-related errors that can stop an AWS S3 export: 

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Error Code
      </th>

      <th>
        Error Message
      </th>

      <th>
        Cause and Resolution
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        403
      </td>

      <td>
        Invalid AWS credentials
      </td>

      <td>
        AWS credentials are expired or deleted. You must create a new Access key ID and Secret access key. For more information, refer to [Create an API Key for your S3 Bucket](https://staging.docs.user.clevertap.net/docs/data-export-to-aws-s3#create-an-api-key-for-your-s3-bucket).
      </td>
    </tr>

    <tr>
      <td>
        403
      </td>

      <td>
        All access to this object has been disabled
      </td>

      <td>
        Here are the possible causes:  

        <li>IAM policy is removed from the S3 bucket. For more information, refer to [Add IAM Policy to S3 Bucket on AWS Console](https://docs.clevertap.com/docs/data-export-to-aws-s3#add-iam-policy-to-s3-bucket-on-aws-console).</li><li>IAM policy is not configured. Check the policy or reconfigure the credentials. For more information, refer to [IAM Policy](https://staging.docs.user.clevertap.net/docs/data-export-to-aws-s3#using-iam-policy).</li>
      </td>
    </tr>

    <tr>
      <td>
        404
      </td>

      <td>
        The specified S3 bucket does not exist
      </td>

      <td>
        S3 bucket is deleted. You must create a new S3 bucket and update the credentials in CleverTap. For more information, refer to [Create an AWS S3 Bucket](https://staging.docs.user.clevertap.net/docs/data-export-to-aws-s3#create-an-aws-s3-bucket).
      </td>
    </tr>
  </tbody>
</Table>

Exports are checked every hour for failures. If an error occurs, CleverTap sends three emails to the export creator within a span of three days. Emails 1 and 2 include the error details and a link to fix it. It warns that the export will stop if the problem is not fixed within three days. Email 3 notifies the creator that CleverTap has stopped the export.

### Q. How can I export data from CleverTap?

A. You can export the data from CleverTap using one of the three methods below:

* **S3 Export (AWS)**: You can export your event and profile data in the AWS S3 bucket using CleverTap Data Exports. For more information on using our data export, refer to [Data Export to AWS S3](doc:data-export-to-aws-s3).

* **Export via API**: You can export your events and user data with our APIs. For more information, refer to [API Overview](https://developer.clevertap.com/docs/api-overview).

* **Find People**: You can download the profile data directly from the CleverTap dashboard through the *Find People* page with the following steps:

  1. Navigate to *Segments* > *Find People*.
  2. Define the criteria you want to export, then click **View Details**.
  3. Click the download icon below *Total users* to initiate the export.

### Q: How does recurring export work?

A: In recurring export, the user profile data is transferred on a scheduled basis. For example, every 4 hours.  

The entire user profile data (e.g., 300 GB) is sent on day one. Only updates or additions to the user profile are exported from day two onwards. For example, only 50 GB of incremental data is sent on day two.  

This incremental data export occurs when:

* New profiles are created.

* User properties or communication preferences are updated.
