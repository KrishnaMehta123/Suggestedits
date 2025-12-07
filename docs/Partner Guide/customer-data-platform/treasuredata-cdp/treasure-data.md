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

1. Open *TD Console* and log in to your Treasure Data account.

2. Select *Integrations Hub* from the top navigation menu.

3. Click **Catalog** to view available integrations from the *Integrations Hub*.

4. Search and select *CleverTap*  from the list.

<Image align="center" className="border" border={true} src="https://files.readme.io/60414a971ef64fc017a79e44dc64cd02cb87e74e96da0f26e7d72d307a2b3462-image.png" />

5. Click **Create Authentication** and enter the required credential information as follows:


| Field            | Description                                                                                                                                                                                                                                                                 |
| :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Account ID       | Access the CleverTap dashboard and locate the Project ID under *Settings* > *Project*.                                                                                                                                                                                      |
| Account Passcode | Access the CleverTap dashboard and locate the Passcode under *Settings* > *Project*. For more information, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).                                                        |
| Region           | Access the CleverTap dashboard and locate *Region* for the API endpoint you want to select under *Settings* > *Project*. To find the API endpoint for your region, refer to [API endpoints based on your data center region](https://developer.clevertap.com/docs/idc#api). |

6. Click **Continue**. You are prompted to enter a name for the authentication setup.
7. Enter a *Name* for the *Authentication* and click **Done**.

Once the setup is complete, save any changes and verify that the integration is successfully set up. For more information, refer to the [Treasure Data document](https://docs.treasuredata.com/articles/int/clevertap-export-integration/a/h2__1933218993).

## Configure a Query Result for Import

This section provides information about steps to import user profiles, events, and segments from Treasure Data to CleverTap. This involves running a data query and setting options for the format and destination of the results. This process enables users to easily transfer and share data with other systems or tools. 

The following are the steps to import data from the Treasure Data:

1. Go to *Data Workbench* > *Queries*.
2. Select **New Query** and define your SQL query.
3. Click **Export Results** to configure the data import and enter the required details.


<Image alt="Connector Configuration Parameters" align="center" border={true} src="https://files.readme.io/488f39b9d05a306dd35b1f45ab1b60f9b8cfabb2a5eedd2a87b0c959f22d9680-image.png" />  Connector Configuration Parameters
<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Parameter
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Target Data Entity
      </td>

      <td>
        Indicates the CleverTap Import Target Data Entity. Supported Values:  

        <ul>
          <li>User Profiles: Upload the data related to user profiles.</li>
          <li>User Events: Upload the data related to user events.</li>
          <li>User Audiences - Custom List: Upload custom list segment.</li>
        </ul>
        For more information about each Target Data Entity, refer to [Detailed Guide for Each Target Data Entity](https://docs.treasuredata.com/articles/#!int/clevertap-export-integration/a/h2_771907757).
      </td>
    </tr>

    <tr>
      <td>
        User Profiles Operation
      </td>

      <td>
        Indicates the operation related to importing user profiles. Select the list of values below:  

        <ul>
          <li>_Upload User Profiles_: Update user profile information such as gender, phone, etc.</li>
          <li>_Upload Device Tokens_: Add an existing device token to a CleverTap user profile.</li>
          <li>_Demerge User Profile_: Demerge a user profile.</li>
          <li>_Update Email/Phone Subscription_: Set a phone number or email status as subscribed or unsubscribed.</li>
          <li>_Disassociate A Phone Number_: Disconnect a phone number from a user profile.</li>
        </ul>
      </td>
    </tr>

    <tr>
      <td>
        Array Property Operation
      </td>

      <td>
        Required only if the *User Profiles Operation* is Upload User Profiles and the custom attribute value is .JSON array. It applies the CleverTap array operation: replace, append ($add), and remove ($remove). Supported operations: <ul><li>Replace</li> <li>Append</li><li> Remove</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        Name for Custom List Upload
      </td>

      <td>
        Required if the *Target Data Entity* is *User Audiences - Custom List*. This indicates the name of the segment in CleverTap.
      </td>
    </tr>

    <tr>
      <td>
        Custom List Upload User Email
      </td>

      <td>
        Required if the *Target Data Entity* is *User Audiences - Custom List*. The email must belong to the CleverTap admin role.
      </td>
    </tr>

    <tr>
      <td>
        Segment Operation Mode
      </td>

      <td>
        Supported values: <ul><li>Create New Segment (One-Time): This will create a new segment on the CleverTap. If the segment already exists, the job will fail.</li><li>Update Existing Segment (Scheduled): This will update the existing segment on the CleverTap.</li><li>The segment must exist in the CleverTap; otherwise, the job will fail. This option can be used for scheduled jobs.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        Thread Count Number
      </td>

      <td>
        Indicates the number of concurrent requests to the CleverTap server. The minimum is 1, the maximum is 10, and the default is 5. This parameter only applies to Target Data Entity: User Profiles and User Events.
      </td>
    </tr>

    <tr>
      <td>
        Skip on Invalid Record?
      </td>

      <td>
        Select if the job must skip the invalid record and continue to handle the next record. Otherwise, the job will stop if it encounters an invalid record.
      </td>
    </tr>
  </tbody>
</Table>
4. Select or create a [CleverTap authentication](doc:treasure-data#set-up-clevertap-on-treasure-data) and click **Done**.

## Activate a Segment from Audience Studio

You can also import segment data to CleverTap by creating an activation in the Audience Studio.

(@Parth: Is the above statement correct?)

1. Go to *Audience Studio* and select a *parent segment*.
2. Right-click the target segment and select *Create Activation*.
3. Enter and configure an activation name based on the above configuration parameters from the *Details* section.
4. Customize the activation output from the *Output Mapping* section.

<Image alt="Customize Activation Output from Output Mapping section" align="center" border={true} src="https://files.readme.io/9e5c4adbb62b4de6096d87699f0ee368c0d9b59ae652f0c21c6ade64706c6218-image.png" />  Customize Activation Output from Output Mapping section











* Attribute Columns
  * Toggle ON the **Export All Columns** to import all columns without making any changes.
  * Click **+ Add Columns** to add specific columns for the import. The *Output Column Name* pre-populates with the same *Source* column name. You can update the Output Column Name. Continue to select **+ Add Columns** to add new columns for your activation output.
* String Builder\
  Add string to create strings for export. Select from the following values:
  * String: Choose any value; use text to create a custom value.
  * Timestamp: The date and time of the export.
  * Segment Id: The segment ID number.
  * Segment Name: The segment name.
  * Audience Id: The parent segment number.

5. Set a *Schedule*.
   1. Define your schedule and include optional email notifications.
   2. Click **Create** to finalize the activation.