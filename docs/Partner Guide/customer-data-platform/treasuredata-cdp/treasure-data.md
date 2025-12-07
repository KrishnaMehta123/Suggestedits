---
title: Treasure Data
excerpt: Customer Data Platform
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

> 📘 Public Beta
> 
> This feature is released in Public Beta. For more information about this feature or any queries, contact [Treasure Data Support](mailto:support@treasure-data.com).

 [Treasure Data](https://www.treasuredata.com/), a Customer Data Platform (CDP), streamlines data transfer between systems. It enables businesses to consolidate data from one source and push it to multiple destinations, such as CleverTap, without requiring manual integration of each system.

The CleverTap and Treasure Data integration allows seamless data synchronization, enabling businesses to efficiently manage customer profiles and enhance targeted marketing efforts across platforms. If you have any issues with this integration, write to [Treasure Data support](https://support.treasuredata.com/hc/en-us/requests). 

> 📘 Cloud Mode Integration
> 
> This integration uses Cloud-mode integration, which facilitates efficient data synchronization between Treasure Data and CleverTap. If you require a Device-mode integration for more granular control or specific use cases, contact Treasure Data.

# Integrate Treasure Data with CleverTap

The integration process involves the following steps:

1. [Set Up CleverTap on Treasure Data](doc:treasure-data#set-up-clevertap-on-treasure-data)
2. [Configure a Query Result for Import](doc:treasure-data#configure-a-query-result-for-import)
3. [Activate a Segment from Audience Studio](doc:treasure-data#activate-a-segment-from-audience-studio)

## Set Up CleverTap on Treasure Data

To configure CleverTap on Treasure Data:

1. Open _TD Console_ and log in to your Treasure Data account.

2. Select _Integrations Hub_ from the top navigation menu.

3. Click **Catalog** to view available integrations from the _Integrations Hub_.

4. Search and select _CleverTap_  from the list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/60414a971ef64fc017a79e44dc64cd02cb87e74e96da0f26e7d72d307a2b3462-image.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


5. Click **Create Authentication** and enter the required credential information as follows:

| Field            | Description                                                                                                                                                                                                                                                                 |
| :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Account ID       | Access the CleverTap dashboard and locate the Project ID under _Settings_ > _Project_.                                                                                                                                                                                      |
| Account Passcode | Access the CleverTap dashboard and locate the Passcode under _Settings_ > _Project_. For more information, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).                                                        |
| Region           | Access the CleverTap dashboard and locate _Region_ for the API endpoint you want to select under _Settings_ > _Project_. To find the API endpoint for your region, refer to [API endpoints based on your data center region](https://developer.clevertap.com/docs/idc#api). |

6. Click **Continue**. You are prompted to enter a name for the authentication setup.
7. Enter a _Name_ for the _Authentication_ and click **Done**.

Once the setup is complete, save any changes and verify that the integration is successfully set up. For more information, refer to the [Treasure Data document](https://docs.treasuredata.com/articles/int/clevertap-export-integration/a/h2__1933218993).

## Configure a Query Result for Import

This section provides information about steps to import user profiles, events, and segments from Treasure Data to CleverTap. This involves running a data query and setting options for the format and destination of the results. This process enables users to easily transfer and share data with other systems or tools. 

The following are the steps to import data from the Treasure Data:

1. Go to _Data Workbench_ > _Queries_.
2. Select **New Query** and define your SQL query.
3. Click **Export Results** to configure the data import and enter the required details.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/488f39b9d05a306dd35b1f45ab1b60f9b8cfabb2a5eedd2a87b0c959f22d9680-image.png",
        null,
        "Connector Configuration Parameters"
      ],
      "align": "center",
      "border": true,
      "caption": "Connector Configuration Parameters"
    }
  ]
}
[/block]


[block:parameters]
{
  "data": {
    "h-0": "Parameter",
    "h-1": "Description",
    "0-0": "Target Data Entity",
    "0-1": "Indicates the CleverTap Import Target Data Entity. Supported Values:  \n  \n<ul> <li>User Profiles: Upload the data related to user profiles.</li><li> User Events: Upload the data related to user events.</li><li>User Audiences - Custom List: Upload custom list segment.</li>/<ul>For more information about each Target Data Entity, refer to [Detailed Guide for Each Target Data Entity](https://docs.treasuredata.com/articles/#!int/clevertap-export-integration/a/h2_771907757).",
    "1-0": "User Profiles Operation",
    "1-1": "Indicates the operation related to importing user profiles. Select the list of values below:  \n  \n<ul> <li>_Upload User Profiles_: Update user profile information such as gender, phone, etc.</li><li> _Upload Device Tokens_: Add an existing device token to a CleverTap user profile.</li><li>\n_Demege User Profile_: Demerge a user profile. </li> <li>_Update Email/Phone Subscription_: Set a phone number or email status as subscribed or unsubscribed.</li> <li>_Disassociate A Phone Number_: Disconnect a phone number from a user profile.</li></ul>",
    "2-0": "Array Property Operation",
    "2-1": "Required only if the _User Profiles Operation_ is Upload User Profiles and the custom attribute value is .JSON array. It applies the CleverTap array operation: replace, append ($add), and remove ($remove). Supported operations: <ul><li>Replace</li> <li>Append</li><li> Remove</li></ul>",
    "3-0": "Name for Custom List Upload",
    "3-1": "Required if the _Target Data Entity_ is _User Audiences - Custom List_. This indicates the name of the segment in CleverTap.",
    "4-0": "Custom List Upload User Email",
    "4-1": "Required if the _Target Data Entity_ is _User Audiences - Custom List_. The email must belong to the CleverTap admin role.",
    "5-0": "Segment Operation Mode",
    "5-1": "Supported values: <ul><li>Create New Segment (One-Time): This will create a new segment on the CleverTap. If the segment already exists, the job will fail.</li><li>Update Existing Segment (Scheduled): This will update the existing segment on the CleverTap.</li><li>The segment must exist in the CleverTap; otherwise, the job will fail. This option can be used for scheduled jobs.</li></ul>",
    "6-0": "Thread Count Number",
    "6-1": "Indicates the number of concurrent requests to the CleverTap server. The minimum is 1, the maximum is 10, and the default is 5. This parameter only applies to Target Data Entity: User Profiles and User Events.",
    "7-0": "Skip on Invalid Record?",
    "7-1": "Select if the job must skip the invalid record and continue to handle the next record. Otherwise, the job will stop if it encounters an invalid record."
  },
  "cols": 2,
  "rows": 8,
  "align": [
    "left",
    "left"
  ]
}
[/block]


4. Select or create a [CleverTap authentication](doc:treasure-data#set-up-clevertap-on-treasure-data) and click **Done**.

## Activate a Segment from Audience Studio

You can also import segment data to CleverTap by creating an activation in the Audience Studio.

(@Parth: Is the above statement correct?)

1. Go to _Audience Studio_ and select a _parent segment_.
2. Right-click the target segment and select _Create Activation_.
3. Enter and configure an activation name based on the above configuration parameters from the _Details_ section.
4. Customize the activation output from the _Output Mapping_ section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9e5c4adbb62b4de6096d87699f0ee368c0d9b59ae652f0c21c6ade64706c6218-image.png",
        null,
        "Customize Activation Output from Output Mapping section"
      ],
      "align": "center",
      "border": true,
      "caption": "Customize Activation Output from Output Mapping section"
    }
  ]
}
[/block]


- Attribute Columns
  - Toggle ON the **Export All Columns** to import all columns without making any changes.
  - Click **+ Add Columns** to add specific columns for the import. The _Output Column Name_ pre-populates with the same _Source_ column name. You can update the Output Column Name. Continue to select **+ Add Columns** to add new columns for your activation output.
- String Builder  
  Add string to create strings for export. Select from the following values:
  - String: Choose any value; use text to create a custom value.
  - Timestamp: The date and time of the export.
  - Segment Id: The segment ID number.
  - Segment Name: The segment name.
  - Audience Id: The parent segment number.

5. Set a _Schedule_.
   1. Define your schedule and include optional email notifications.
   2. Click **Create** to finalize the activation.