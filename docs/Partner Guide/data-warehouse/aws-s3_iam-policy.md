---
title: AWS S3_IAM Policy
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

The data export feature provides the capability to bulk export your CleverTap event data to your AWS S3 bucket. You can use this for analysis in BI tools or storage in your data warehouse for analysis in the future.

> 📘 Feature Availability
>
> This capability is a part of the *CleverTap for Enterprises* plan. To activate this for your account, contact your sales account manager.

# Setup

The following are the two major steps involved in enabling this feature for your account:

1. [Create an AWS S3 Bucket](doc:aws-s3_iam-policy#create-an-aws-s3-bucket).
2. Configure Buckets details on CleverTap Dashboard using one of the following methods:
   * [Using Access Key](doc:aws-s3_iam-policy#using-iam-policy)
   * [Using IAM Policy](doc:aws-s3_iam-policy#using-access-key)

## Create an AWS S3 Bucket

To create an AWS S3 bucket:

1. Log in to your AWS account, then search for *S3* in the AWS services box. 
2. Select *S3* from the search results. 

<Image title="Selecting S3 from the list.png" alt={891} className="border" border={true} src="https://files.readme.io/bb8d83c-Selecting_S3_from_the_list.png" />

   On clicking, the *Bucket* page displays.

3. Click **+ Create bucket**. On clicking, the *Create bucket* page displays:

<Image title="Bucket page.png" alt={2876} className="border" border={true} src="https://files.readme.io/111a267-Bucket_page.png" />

4. Enter a bucket name, region, logging, versioning, and encryption preferences. 

<Image title="Create bucket page.png" alt={1628} className="border" width="80%" border={true} src="https://files.readme.io/407acf4-Create_bucket_page.png" />

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
  </tbody>
</Table>

5. Click **Create bucket**. On successful bucket creation, the following message displays in the snackbar at the top:

<Image title="Successful bucket creation.png" alt={2770} className="border" border={true} src="https://files.readme.io/681e832-Successful_bucket_creation.png" />

The bucket you just created now shows up on your S3 console. We recommend you note down the name of your new bucket, as you will need it for the next step.

## Configure S3 Bucket Details on CleverTap Dashboard

### Using IAM Policy

The following are the two major steps to perform this task:\
i. [Copy IAM Policy from the CleverTap dashboard](doc:aws-s3_iam-policy#copy-iam-policy-from-the-clevertap-dashboard)\
ii. [Add IAM Policy to S3 Bucket from AWS console](doc:aws-s3_iam-policy#add-iam-policy-to-s3-bucket-on-aws-console). 

#### Copy IAM Policy from the CleverTap Dashboard

To copy the IAM policy from the CleverTap dashboard:

1. Navigate to *Settings* > *Partners* and click **View Details** against Amazon S3. The *Integrate analytics partner - Amazon S3* window displays on the right side of the screen.

<Image title="Integrate Analytics Partner - AWS S3.png" alt={1500} className="border" width="80%" border={true} src="https://files.readme.io/27118b6-Integrate_Analytics_Partner_-_AWS_S3.png" />

2. Click **+ Amazon S3 Bucket** to create a new bucket.
3. Enter the *Bucket name*. 
4. Select *IAM (Identity and Access Management) Policy* option under *Configure with* section.

<Image title="Select IAM Policy option.png" alt={1446} className="border" width="80%" border={true} src="https://files.readme.io/475094f-Select_IAM_Policy_option.png" />

4. Click the ![Copy](https://files.readme.io/2bd537e-Copy_icon.png) icon to copy the policy to the clipboard and keep this window open for saving these details later.

#### Add IAM Policy to S3 Bucket on AWS Console

To add IAM policy to the S3 bucket:

1. Select the bucket from the Bucket page of the AWS console.
2. Select the *Permissions* tab.
3. Click **Edit** under the *Bucket policy* section and enter the policy that you copied in Step *4* of [Copy IAM Policy from the CleverTap dashboard](doc:aws-s3_iam-policy#copy-iam-policy-from-the-clevertap-dashboard):

<Image title="Add IAM policy to S3  Bucket.png" alt={2052} className="border" width="80%" border={true} src="https://files.readme.io/438b0da-Add_IAM_policy_to_S3_Bucket.png" />

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
5. Go back to the same window opened in *Step 4* of [Copy IAM Policy From CleverTap Dashboard](doc:aws-s3_iam-policy#copy-iam-policy-from-the-clevertap-dashboard) and click **Save Credentials**.\
   Amazon S3 bucket is now configured on both the AWS S3 console and CleverTap dashboard. 

### Using Access Key

The following are the two major steps to perform this task:\
i. [Create an API Key for Your S3 Bucket](doc:aws-s3_iam-policy#create-an-api-key-for-your-s3-bucket).\
ii. [Add Your S3 Bucket Details to CleverTap](doc:aws-s3_iam-policy#add-your-s3-bucket-details-to-clevertap-1).

#### Create an API Key for Your S3 Bucket

This section demonstrates the creation of an AWS API key with write access to the bucket we created in the above step. CleverTap uses this API key to export data to your S3 bucket.

1. Click on your account name on the top right of the AWS console.
2. Click **Security Credentials**.

<Image title="Security credentials.png" alt={388} className="border" width="smart" border={true} src="https://files.readme.io/152163f-Security_credentials.png" />

3. Select *Users* from the left navigation and click **Add user**.

<Image title="Click Add users.png" alt={2878} className="border" border={true} src="https://files.readme.io/8b81e57-Click_Add_users.png" />

On clicking, the *Add user* page displays.\
4\. Enter the *User name* and select the *Programmatic access* checkbox.\
5\. Click **Next:Permissions**.

<Image title="Add user.png" alt={2878} className="border" border={true} src="https://files.readme.io/7840a59-Add_user.png" />

On clicking, *Set permissions* page displays.\
6\. Click **Create group** under *Add user to group* tab.

<Image title="Create_group.png" alt={2872} className="border" border={true} src="https://files.readme.io/592634b-Create_group.png" />

On clicking, *Create group* page displays.

<Image title="Create group page.png" alt={2482} className="border" border={true} src="https://files.readme.io/5cfd145-Create_group_page.png" />

7. Click **Create policy**. On clicking, *Create policy* page opens in a new tab.
8. Select the **JSON** tab and then paste the JSON code given below in the box. 
9. Replace `clevertap-example` in the JSON code with the name of the S3 bucket you created in the above step.\
   The permissions defined in this policy allow CleverTap to get information about your bucket and upload files to it.

> 📘 AWS API Access Policies
>
> *IP Whitelisting* is not supported with S3 exports. For more information about AWS API access policies, refer to [this post](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies_examples_s3_rw-bucket-console.html) from the AWS blog.

<Image title="Replace JSON code.png" alt={2874} className="border" border={true} src="https://files.readme.io/bc21bb7-Replace_JSON_code.png" />

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

<Image title="Create policy.png" alt={2648} className="border" border={true} src="https://files.readme.io/f81305a-Create_policy.png" />

On successful policy creation, the following message displays in the snackbar at the top:

<Image title="Policy created successfully.png" alt={2870} className="border" border={true} src="https://files.readme.io/cc7b89a-Policy_created_successfully.png" />

12. Go back to the *Create group* page (opened in *Step 6*), search for the policy you just created, and assign it to the new group by selecting the checkbox.
13. Click **Create group**. On clicking, the *Add user* page displays.

<Image title="Search policy.png" alt={2486} className="border" border={true} src="https://files.readme.io/c28e813-Search_policy.png" />

14. Click **Next: Tags** and then click **Next: Review**.

<Image title="Click_Next_Tags.png" alt={2012} className="border" border={true} src="https://files.readme.io/15f1ead-Click_Next_Tags.png" />

15. Click **Create user**. 

<Image title="Create user.png" alt={1980} className="border" border={true} src="https://files.readme.io/d88007d-Create_user.png" />

On successful user creation, the following page displays. You will see your *Access key ID* and the *Secret access key*. 

<Image title="Access key and secret access key.png" alt={2878} className="border" border={true} src="https://files.readme.io/d3b1def-Access_key_and_secret_access_key.png" />

These credentials allow CleverTap to upload files to your S3 bucket. We recommend you note down these values as you will require them for the next step. Otherwise, you can also click **Download .csv** to save these details for future use.

#### Add Your S3 Bucket Details to CleverTap

To add your S3 bucket details to Clevertap, perform the following steps:

1. Navigate to *Settings* > *Partners* and click **View Details** against Amazon S3. The *Integrate analytics partner - Amazon S3* window displays on the right side of the screen.

<Image title="Integrate Analytics Partner - AWS S3.png" alt={1500} className="border" border={true} src="https://files.readme.io/6ab03f2-Integrate_Analytics_Partner_-_AWS_S3.png" />

2. Click **+ Amazon S3 Bucket** to create a new bucket. The *Integrate Amazon S3 Bucket* window opens on the right side of the screen. 
3. Enter the *Bucket nickname* and *Bucket URL*. 
4. Select the *User details* option under *Configure with* section.
5. Enter your *Access key ID* and the *Secret access key* obtained earlier and click **Save Credentials**.

<Image title="Select User details option.png" alt={1494} className="border" border={true} src="https://files.readme.io/5f44e48-Select_User_details_option.png" />

# Create a New Data Export

To create a new data export, perform the following steps:

1. Navigate to *Settings* > *Partners* > *Exports*.
2. Click **+ Export** and select *Amazon S3* from the Partners dropdown.

<Image title="Select Amazon S3 ftom the partner list.png" alt={2426} className="border" border={true} src="https://files.readme.io/18b7cf9-Select_Amazon_S3_ftom_the_partner_list.png" />

On clicking, the *Export to Amazon S3* popup displays on the right side of the screen.

<Image title="Export to Amazon S3 popup.png" alt={1008} className="border" width="80%" border={true} src="https://files.readme.io/9256a21-Export_to_Amazon_S3_popup.png" />

3. Configure the following settings:
   * **Type**: Select the events to export from the available options. For more information, refer to [Export Details](doc:aws-s3_iam-policy#export-details).
   * **Frequency**: Select from one of the following options:
     * *Once only*: A single export for the selected export type. You can export data up to the last **60 days**. You create an export for a specific day, date range, previous month, current month, and more. 
     * *Recurring*: Set up a recurring export that exports all the new events captured in the last window. You can export data as frequently as every 4 hours and up to once every 24 hours.

4. Click **Create export**. On clicking, the popup closes and the following message displays at the top of the *Exports* page:

<Image title="Amazon S3 export initiated.png" alt={2362} className="border" border={true} src="https://files.readme.io/743e38d-Amazon_S3_export_initiated.png" />

CleverTap processes the export, and you can now see the newly created export for AWS S3.

<Image title="Exports page.png" alt={2426} className="border" border={true} src="https://files.readme.io/9a9a189-Exports_page.png" />

The status for each export is displayed as *Pending* as soon as the export is created. The status changes to *Running* after the processing starts. And, it changes to *Done* when the export is complete.

> 📘 Stop Export
>
> You can also stop the export that you have created. To do so, click the ![Stop export](https://files.readme.io/22bc9e8-Stop_icon)\
>  icon for the export request you want to stop, and then click **Stop** to confirm your action.

5. Confirm if your event data was successfully exported. To do so:\
   a. Log in to your AWS account and navigate to the *S3* console.\
   b. Search your *Bucket* from the *Buckets* page and then click the bucket name.\
   c. Copy the *Request ID* from the activity log and search with that ID. You should see your respective file there. 

<Image title="Search for export files.png" alt={2842} className="border" border={true} src="https://files.readme.io/217fe0e-Search_for_export_files.png" />

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

The example below shows the file name format for data exports:

* **Export request ID**: The export request ID is generated when you create a request in the CleverTap dashboard.
* **Timestamp of export run**: The timestamp is when the export was run.
* **Event name**: The event name is an event type that is included in the file.
* **File index**: We chunk the data across multiple files for larger exports. The file index notes what file number in the file series it is. We have limited file sizes to 100 MB chunks to make them more consumable.
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

Parquet has a timestamp, eventName, and eventProperties for each event. 

> 📘 Parquet File Format
>
> Parquet is an open-source file format for Hadoop. Parquet stores nested data structures in a flat columnar format.

# FAQs

### What permission is required for CleverTap to export data to your AWS S3 bucket?

Ans. CleverTap needs write permission to be able to export data to your AWS S3 bucket, as shown in the following figure:

<Image title="Select IAM Policy option.png" alt={1446} className="border" width="80%" border={true} src="https://files.readme.io/7bed273-Select_IAM_Policy_option.png" />

### What should I do if I already have an existing IAM policy for my AWS S3 bucket?

Ans. Ensure that you modify the current IAM policy to provide CleverTap with write access to export data to your AWS S3 bucket.
