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

> 📘 Feature Availability
>
> This capability is a part of the *CleverTap for Enterprises* plan. To activate this for your account, contact your sales account manager.

# Setup

This section includes information about the setup steps involved to enable this feature for your account. 

1. [Create an AWS S3 Bucket](doc:aws-s3-export#create-an-aws-s3-bucket)
2. [Create an API Key for Your S3 Bucket](docs:aws-s3-export#create-an-api-key-for-your-s3-bucket)
3. [Add Your S3 Bucket Details to CleverTap](doc:aws-s3-export#add-your-s3-bucket-details-to-clevertap)

## Create an AWS S3 Bucket

To create an AWS S3 bucket:

1. Log in to your AWS account, then search for *S3* in the AWS services box. 
2. Select *S3* from the search results. 

<Image title="Selecting S3 from the list.png" alt={891} className="border" border={true} src="https://files.readme.io/68c90b5-Selecting_S3_from_the_list.png" />

```
On clicking, the *Bucket* page displays.
```

3. Click **+ Create bucket**. On clicking, the *Create bucket* page displays:

<Image title="Bucket page.png" alt={2876} className="border" border={true} src="https://files.readme.io/fe98c60-Bucket_page.png" />

4. Enter a bucket name, region, logging, versioning, and encryption preferences. 

<Image title="Create bucket page.png" alt={1628} className="border" width="80%" border={true} src="https://files.readme.io/0bbda49-Create_bucket_page.png" />

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
        Asia Pacific (Seoul)\
        ap-northeast-2
      </td>
    </tr>
  </tbody>
</Table>

5. Click **Create bucket**. On successful bucket creation, the following message displays in the snackbar at the top:

<Image title="Successful bucket creation.png" alt={2770} className="border" border={true} src="https://files.readme.io/66633bb-Successful_bucket_creation.png" />

The bucket you just created now shows up on your S3 console. We recommend you note down the name of your new bucket as you will need it for the next step.

## Create an API Key for Your S3 Bucket

This section demonstrates the creation of an AWS API key that has write access to the bucket we created in the above step. CleverTap uses this API key to export data to your S3 bucket.

1. Click on your account name on the top right of the AWS console.
2. Click **Security Credentials**.

<Image title="Security credentials.png" alt={388} className="border" width="smart" border={true} src="https://files.readme.io/152163f-Security_credentials.png" />

3. Select *Users* from the left navigation and click **Add user**.

<Image title="Click Add users.png" alt={2878} className="border" border={true} src="https://files.readme.io/8b81e57-Click_Add_users.png" />

On clicking, the *Add user* page displays.\
4\. Enter the *User name* and select the *Programmatic access* checkbox.\
5\. Click **Next:Permissions**.

<Image title="Add user.png" alt={2878} className="border" border={true} src="https://files.readme.io/2cb0126-Add_user.png" />

On clicking, *Set permissions* page displays.\
6\. Click **Create group** under *Add user to group* tab.

<Image title="Create group.png" alt={2872} className="border" border={true} src="https://files.readme.io/c008773-Create_group.png" />

On clicking, *Create group* page displays.\
7\. Click **Create policy**. On clicking, *Create policy* page opens in a new tab.

<Image title="Create group page.png" alt={2482} className="border" border={true} src="https://files.readme.io/2803f68-Create_group_page.png" />

8. Select the **JSON** tab and then paste the JSON code given below in the box. 

![2874](https://files.readme.io/7622dac-Replace_JSON_code.png "Replace JSON code.png")

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

9. Replace `clevertap-example` in the JSON code with the name of the S3 bucket you created in the above step.\
   The permissions defined in this policy allow CleverTap to get information about your bucket and upload files to it.

> 📘 AWS API Access Policies
>
> *IP Whitelisting* is not supported with S3 exports. For more information about AWS API access policies, refer to [this post](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_examples_s3_rw-bucket-console.html) from the AWS blog.

10. Click **Next: Tags**  and then click **Next: Review**. On clicking, the *Create policy* page opens.
11. Enter the policy *Name* and click **Create policy**.

<Image title="Create policy.png" alt={2648} className="border" border={true} src="https://files.readme.io/3c47940-Create_policy.png" />

On successful policy creation, the following message displays in the snackbar at the top:

<Image title="Policy created successfully.png" alt={2870} className="border" border={true} src="https://files.readme.io/cc7b89a-Policy_created_successfully.png" />

12. Go back to the *Create group* page (opened in step 6), search for the policy you just created, and assign it to the new group by selecting the checkbox next to it.
13. Click **Create group**. On clicking, the *Add user* page displays.

<Image title="Search policy.png" alt={2486} className="border" border={true} src="https://files.readme.io/a81e456-Search_policy.png" />

14. Click **Next: Tags** and then click **Next: Review**.

<Image title="Click Next Tags.png" alt={2012} className="border" border={true} src="https://files.readme.io/6bbcf91-Click_Next_Tags.png" />

15. Click **Create user**. 

<Image title="Create user.png" alt={1980} className="border" border={true} src="https://files.readme.io/d88007d-Create_user.png" />

On successful user creation, the following page displays. You will see your *Access key ID* and the *Secret access key*. 

<Image title="Access key and secret access key.png" alt={2878} className="border" border={true} src="https://files.readme.io/d3b1def-Access_key_and_secret_access_key.png" />

These credentials allow CleverTap to upload files to your S3 bucket. We recommend you note down these values as you will require them for the next step. Otherwise, you can also click **Download .csv** to save these details for future use.

## Add Your S3 Bucket Details to CleverTap

To add your S3 bucket details to Clevertap, perform the following steps:

1. Log in to your CleverTap account.
2. Navigate to *Settings* > *Partners* > *Exports*. 
3. Click the **AWS Amazon** icon and select *S3* from the *AWS Connections* dropdown.
4. Enter your bucket name from the *Create an AWS S3 Bucket* section above. 
5. Enter your *Access key ID* and the *Secret access key* obtained earlier.

<Image title="Exports page.png" alt={2270} className="border" border={true} src="https://files.readme.io/94cbd71-Exports_page.png" />

# Create a New Data Export

To create a new data export, perform the following steps:

1. Navigate to *Settings* > *Partners* > *Exports* > *Activity Log*.
2. Click **+ Create Export**. 

<Image title="Create Export page.png" alt={1209} className="border" border={true} src="https://files.readme.io/438f569-Create_Export_page.png" />

On clicking, *Create an export* popup will display.

3. Define the following settings and click **Create export**:

* *Select an export partner*: Select AWS S3 from the dropdown list.
* Export details: Select the following appropriate export-related options: the type of export (user profile or events), export frequency, and export format. For more information, refer to [Export Details](doc:aws-s3-export#export-details).

<Image title="Create an export popup.png" alt={1098} className="border" width="smart" border={true} src="https://files.readme.io/370dd04-Create_an_export_popup.png" />

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

> 📘 Exception for One-time Profile Export
>
> If there is a scheduled recurring profile export, you must stop it to run a one-time profile export.

<Image title="Data Export to AWS S3 - Choose Export.png" alt={634} className="border" width="80%" border={true} src="https://files.readme.io/b1aed72-Data_Export_to_AWS_S3_-_Choose_Export.png" />

CleverTap will now process the export. You can refresh the *Activity Log* page to see the current status of the export. After the export is complete, the status for that export is displayed as *Done*.

<Image title="Export Status.png" alt={1209} className="border" border={true} src="https://files.readme.io/1653bb8-Export_Status.png" />

To confirm your event data was successfully exported:

1. Log in to your AWS account and navigate to the *S3* console. 
2. Search your *Bucket* from the *Buckets* page and then click the bucket name. 
3. Copy the *Request ID* from the activity log and search with that ID. You should see your respective file there. 

<Image title="Search for export files.png" alt={2842} className="border" border={true} src="https://files.readme.io/fc7efeb-Search_for_export_files.png" />

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

```text
<export request id>-<timestamp of the export run>-<event name>-<yyyymmdd>-<file index>-<database-id>.<file format>.gz
```

## File Data Format

Files are split by event names for event exports and each file will have all event data for the given period for the event.

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

![2032](https://files.readme.io/aa71f9f-Screenshot_2020-02-28_at_12.53.22_PM.png "Screenshot 2020-02-28 at 12.53.22 PM.png")

### XML

XML have the timeStamp, eventName, followed by eventProperties.

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

Parquet have timestamp, eventName, and eventProperties for each event. 

> 📘 Parquet File Format
>
> Parquet is an open source file format for Hadoop. Parquet stores nested data structures in a flat columnar format.
