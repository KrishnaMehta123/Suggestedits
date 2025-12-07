---
title: Treasure Data
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

> 📘 Public Beta
>
> This feature is released in Public Beta. For more information about this feature, contact your Success Manager or [CleverTap support.](https://clevertap.com/contact-us/)

A Customer Data Platform (CDP) like [Treasure Data](https://www.treasuredata.com/) streamlines data transfer between systems. It enables customers to consolidate data from one source and push it to multiple destinations, such as CleverTap and other attribution partners, without requiring manual integration of each system.

The CleverTap integration with Treasure Data allows for seamless data synchronization, enabling businesses to efficiently manage customer profiles and enhance targeted marketing efforts across platforms.

If you have any issues with this integration, write to [Treasure Data support](https://support.treasuredata.com/hc/en-us/requests)

> 📘 Cloud Mode Integration
>
> This Cloud mode integration facilitates efficient data synchronization between Treasure Data and CleverTap. If you require a Device mode integration for more granular control or specific use cases, contact Treasure Data [support](https://support.treasuredata.com/hc/en-us/requests) for assistance.

# Integrating Imports from Treasure Data to CleverTap

1. Setup CleverTap on TreasureData
2. Configure a Query Result for Export
3. User Profiles Import from Treasure Data
4. Events Data Import from Treasure Data
5. Custom List Segment Import from Treasure Data

# # Setup CleverTap on TreasureData

To configure CleverTap on Treasure Data, follow these steps:

1. **Open TD Console**: Log in to your Treasure Data account.

2. **Navigate to Integrations Hub**: Go to the top navigation menu and select "Integrations Hub."

3. **Select Catalog**: In the Integrations Hub, click on "Catalog" to view available integrations.

4. **Search for CleverTap**: Use the search bar to find "CleverTap" and select it from the list.

<Image align="center" src="https://files.readme.io/edc181838d62f0d5e89ebf86d99b1aef023911bf1a5e6562966dd56ee70e3cda-Screenshot_2024-09-27_at_4.10.19_PM.png" />

5. **Create Authentication**: Click on "Create Authentication."
6. **Provide Credential Information**: Fill in the required credential information as specified in your integration documentation. This usually includes:

* **Account ID**: Access the CleverTap dashboard and locate the Project ID under Settings > Project.
* **Account Passcode**: Access the CleverTap dashboard and locate the Passcode under Settings > Project. To know more refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).
* **Region**: Access the CleverTap dashboard and locate Region for the API endpoint you want to select under Settings > Project. To find the API endpoint for your region, refer to [API endpoints based on your data centre region](https://developer.clevertap.com/docs/idc#api).

7. **Continue**: After entering the credentials, select "Continue."
8. **Enter a Name for the Authentication**: Provide a descriptive name for the authentication setup, then click "Done."
9. **Complete Configuration**: Once you've completed this, make sure to save any changes and verify that the integration is successfully set up.

For more information, refer to this [TreasureData document](https://docs.treasuredata.com/articles/int/clevertap-export-integration/a/h2__1933218993).

# CleverTap Data Import from Treasure Data

This document outlines the steps to import user profiles, events, and segments from Treasure Data to CleverTap.

## Data Query

A data query is a request to retrieve specific information from a database, often written in SQL. It defines criteria to select and filter data, allowing users to analyze or manipulate the information.

### Configure a Query Result for Export

In Treasure Data, configuring a query result for export involves running a data query and setting options for the format and destination of the results. This process enables users to transfer and share data with other systems or tools easily. To configure a query result for export on the Treasure Data dashboard, refer to the documentation here: [Configure a Query Result for Export](https://docs.treasuredata.com/display/public/PD/Exporting+Query+Results).

1. **Navigate**: Go to **Data Workbench > Queries**.
2. **Create Query**: Select **New Query** and define your SQL query.
3. **Export Results**: Click on **Export Results** and choose or create a CleverTap authentication.
4. **Select Done**.

### Connector Configuration Parameters

This section outlines the key parameters required to configure the connector for data import. 

### Target Data Entity

* **User Profiles**: Import user profile data.
* **User Events**: Import user event data.
* **User Audiences - Custom List**: Import a custom list segment.

# User Profiles Import from Treasure Data

Select one of the following operations for importing user profiles. Refer to this document to [know more](https://docs.treasuredata.com/articles/int/clevertap-export-integration/a/h2_1587868635).

* **Upload User Profiles**: Update user profile information.
* **Upload Device Tokens**: Add existing device tokens.
* **Demerge User Profile**: Separate merged profiles.
* **Update Email/Phone Subscription**: Manage subscription statuses.
* **Disassociate a Phone Number**: Disconnect a phone number.

## Additional Options

You can customize the import process with the following options:

* **Array Property Operation**: Choose to replace, append, or remove.
* **Name for Custom List Upload**: Required for custom lists. [Know more](https://docs.treasuredata.com/articles/int/clevertap-export-integration/a/fieldcolumn-level-specifications)
* **Segment Operation Mode**: Create or update segments.
* **Thread Count Number**: Set concurrent requests (1-10, default 5).
* **Skip on Invalid Record**: Check to skip invalid records.

## Query Specifications

This section outlines the criteria for structuring your queries for user profile imports.

### General Requirements

1. **Required Columns**: Include at least one of the`identity` or `objectId`.
2. **Column Rules**: No special characters, max 120 characters, and values must not exceed 512 characters.

### User Profiles Operations

1. **Upload User Profiles**: Include required fields like `identity` or `objectId`.
2. **Upload Device Tokens**: Include `objectId`, `id`, and `type`.
3. **Demerge User Profile**: Required field: `identity`.
4. **Update Email/Phone Subscription**: Required fields: `type`, `value`, `status`.
5. **Disassociate a Phone Number**: Required: `value` (E.164 format).

For more information 

# Events Data Import from Treasure Data

This section describes the process of importing user event data from Treasure Data into CleverTap.

## I. Building the Export Query

To successfully import user event data into CleverTap, your query must adhere to the following specifications for both default and custom fields.

### 1. Export Query Specifications

Ensure your query meets the following criteria:

| Specification                   | Description                                                                                                 |
| ------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| **Required Columns**            | At least one of the following must be present: `identity` or `objectid`. The `evtName` column is mandatory. |
| **Null Value Columns**          | Columns with null values will be ignored.                                                                   |
| **Column Naming Rules**         | Column names must not include: &, $, ", ,, %, >, \<, !. They must not exceed 120 characters.                |
| **Maximum Column Value Length** | Values for both default and custom fields must not exceed 512 characters.                                   |
| **Duplicated Columns**          | Duplicated columns are not allowed.                                                                         |

### 2. Field/Column-Level Specifications

Review the following specifications for field and column requirements:

#### Default Field Columns

| Field/Column/Alias     | Description                                | Required                          | Data Type                               | Additional Specifications                                                              |
| ---------------------- | ------------------------------------------ | --------------------------------- | --------------------------------------- | -------------------------------------------------------------------------------------- |
| `identity`             | User identity field                        | Yes, if `objectid` is not present | Scalar types (string, integer, boolean) |                                                                                        |
| `objectid`             | User identity field                        | Yes, if `identity` is not present | Scalar types (string, integer, boolean) |                                                                                        |
| `ts`                   | Event timestamp                            | No                                | Integer/Long                            | Must match Unix timestamp format (see details below).                                  |
| `evtName`              | Event name                                 | Yes                               | String                                  |                                                                                        |
| `Items[index].KeyName` | List of products/items for “Charged Event” | No                                | Array of Objects                        | Must follow the pattern: `Items[x].field_name`. For example: `Items[0].Category`, etc. |

**Event Timestamp Options**:

1. **Integer Type**: Use as-is if already in Unix format.
2. **Timestamp Cast**: Use SQL to cast to Unix time format (e.g., `SELECT CAST(timestamp_field AS TIMESTAMP) AS ts`).
3. **ISO-8601 Format**: Must end with "Z" for UTC (e.g., `SELECT "2020-08-01T00:00:00Z" AS ts`).

#### Example for Items:

```json
"evtData": {   
    "Items": [
        {
            "Category": "books",
            "Book name": "The Millionaire Next Door",
            "Quantity": 1
        }
    ]
}
```

#### Custom Field Columns

| Column Type        | Description                                                       | Mapping                                           | Additional Specifications                                                                                              |
| ------------------ | ----------------------------------------------------------------- | ------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| Non-default Fields | Columns not listed as default fields are treated as custom fields | Mapped as key/value pairs in the `evtData` object | Date-time columns must be cast as timestamps or ISO-8601 strings. Refer to the Upload User Profiles guide for details. |

## II. Connector Configuration

This section outlines the necessary configuration settings for importing event data into CleverTap.

### Configuration Options

| Configuration Option   | Value       | Description                            |
| ---------------------- | ----------- | -------------------------------------- |
| **Target Data Entity** | User Events | Set to “User Events” for this feature. |

# Custom List Segment Import from Treasure Data

This section outlines the process for creating a user segment by uploading a list of user identities to CleverTap from Treasure Data. It includes detailed instructions for building the export query and configuring the connector.

## I. Building the Export Query

Your export query must adhere to specific data specifications to successfully create a segment.

### 1. Export Query Specifications

| Specification          | Description                                                      |
| ---------------------- | ---------------------------------------------------------------- |
| **Required Columns**   | The query result must include the `type` and `identity` columns. |
| **Null Value Columns** | Columns with null values will be ignored.                        |
| **Ignored Columns**    | Any columns that are not required will be ignored.               |

### 2. Field/Column-Level Specifications

| Field      | Description          | Required | Data Type         | Additional Specifications      |
| ---------- | -------------------- | -------- | ----------------- | ------------------------------ |
| `type`     | User identity type   | Yes      | String            | Values can only be `g` or `i`. |
| `identity` | User identity values | Yes      | String or Integer |                                |

## II. Connector Configuration

This section details the configuration required to import custom list segments into CleverTap.

### Configuration Options

| Configuration Option              | Value                                        | Description                                                                                                |
| --------------------------------- | -------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| **Target Data Entity**            | User Audiences - Custom List                 | Set to “User Audiences - Custom List” for this feature.                                                    |
| **Name for Custom List Upload**   | [Custom List Segment Name]                   | Specify the segment name in the CleverTap dashboard UI.                                                    |
| **Custom List Upload User Email** | [User Email]                                 | Enter the email of a CleverTap user with an Admin Role; otherwise, the job will fail.                      |
| **Segment Operation Mode**        | Create New Segment / Update Existing Segment | Choose “Create New Segment” for a one-time job or “Update Existing Segment” to modify an existing segment. |

### Activating a Segment from Audience Studio

1. Navigate to **Audience Studio**.
2. Select a **parent segment**.
3. Right-click on the target segment and select **Create Activation**.
4. In the **Details panel**, enter and configure an activation name based on the above configuration parameters.
5. **Output Mapping**: Customize the activation output.

### Attribute Columns

* **Export All Columns**: Choose this to export all columns without changes.
* **Add Specific Columns**: Select `+ Add Columns` to include specific columns, updating the Output Column Name as needed.

### String Builder

* **Add String**: Create custom strings for export using options like:
  * **String**: Choose any value.
  * **Timestamp**: The date and time of the export.
  * **Segment Id**: The segment ID number.
  * **Segment Name**: The segment name.
  * **Audience Id**: The parent segment number.

### Setting a Schedule

* Define your schedule and include optional email notifications.
* Select **Create** to finalize the activation.
