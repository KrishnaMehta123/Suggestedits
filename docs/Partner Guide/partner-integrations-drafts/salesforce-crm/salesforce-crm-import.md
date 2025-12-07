---
title: Salesforce Import
excerpt: >-
  Learn how to import Salesforce data into CleverTap to enrich user profiles,
  trigger CRM-based campaigns, and enable advanced segmentation.
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

Connecting your Salesforce account allows you to sync standard objects, such as Leads, Contacts, Opportunities, and Events, into CleverTap to enrich user profiles, enable segmentation, and power analytics. The integration supports real-time and historical imports, allowing you to bring CRM data into CleverTap for more personalized and data-driven engagement.

Supported data types include:

- **Profiles**: Contact, Lead, Account, Opportunity
- **Events**: Case, Campaign, Task, Campaign Member, Event, Service Appointment
- **Sales Data**: Quote, Contract, Order, Product, Opportunity Product, Asset, Price Book

This integration enables Salesforce to act as a data source for the CleverTap platform. Once connected, organizations can use imported data to:

- **Unify Customer Profiles**: Bring in Salesforce records such as contacts, leads, accounts, or opportunities as profile data in CleverTap.
- **Trigger Campaigns from CRM Events**: Use status changes and CRM events, such as task creation, opportunity updates, or case resolutions, as triggers for CleverTap Journeys and messaging.
- **Segment Based on Historical CRM Data**: Backfill historical Salesforce records to enable precise segmentation and reporting in CleverTap.

# Use Cases

The Salesforce–CleverTap integration supports a wide range of marketing, sales, and engagement scenarios. Below are some common ways teams can leverage the integration:

- **Import Leads and Contacts**: Sync lead and contact data into CleverTap to build enriched profiles for segmentation and targeting.
- **Bring in Opportunity and Account Records**: Use structured deal and customer data from Salesforce to create meaningful lifecycle campaigns in CleverTap.
- **Log Events such as Case Updates or Task Completion**: Track CRM activities such as ticket resolutions, calls, or meeting completions as events in CleverTap.
- **Backfill Historical Records**: Populate CleverTap with historical CRM data to inform engagement strategies and analytics from day one.

# Prerequisites for Integration

Before initiating the integration between Salesforce and CleverTap, ensure that both platforms are properly configured. Salesforce access is required for source data, and CleverTap credentials are required for authentication and ingestion.

## CleverTap Requirements

To configure the integration, retrieve the following details from your CleverTap dashboard:

| Field            | Description                                                                                                                                                                                                               |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Account ID**   | You can find the Project ID under _Settings_ > _Project_ in the CleverTap dashboard.                                                                                                                                      |
| **API Passcode** | You can find the Password under _Settings_ > _Project_ in the CleverTap dashboard. For more information, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).        |
| **Region**       | You can determine your account's data center under _Settings_ > _Project_. To select the appropriate endpoint for integration, refer to the [API endpoints by region](https://developer.clevertap.com/docs/api-endpoint). |

- - [block:image]{"images":[{"image":["https://files.readme.io/33e977b0e8ae75a9da88d8734de53a4ebfc71b1f35964e3d33185c5af775b8f7-Clevertap_project_details.png","","Project details - CleverTap"],"align":"center","border":true,"caption":"CleverTap Project Details"}]}[/block]

## Salesforce Requirements

To allow Salesforce to act as a data source, ensure the following system-level and permission-based prerequisites are met:

- A valid Salesforce account with API access enabled (Enterprise, Unlimited, or Performance edition).
- Required permissions to access object data such as [Leads](https://help.salesforce.com/s/articleView?id=sf.leads_def.htm), [Contacts](https://help.salesforce.com/s/articleView?id=sf.contacts_def.htm), [Accounts](https://help.salesforce.com/s/articleView?id=sf.accounts_def.htm), [Opportunities](https://help.salesforce.com/s/articleView?id=sf.opps_def.htm), [Cases](https://help.salesforce.com/s/articleView?id=sf.cases_def.htm), [Campaign](https://help.salesforce.com/s/articleView?id=sf.campaigns.htm), [Event](https://help.salesforce.com/s/articleView?id=sf.activity_def.htm), [Task](https://help.salesforce.com/s/articleView?id=sf.tasks_def.htm), [Campaign Member](https://help.salesforce.com/s/articleView?id=sf.campaign_members.htm), [Service Appointment](https://help.salesforce.com/s/articleView?id=sf.field_service_overview.htm), [Quote](https://help.salesforce.com/s/articleView?id=sf.quotes_def.htm), [Contract](https://help.salesforce.com/s/articleView?id=sf.contracts.htm), [Order](https://help.salesforce.com/s/articleView?id=sf.orders_def.htm), [Product](https://help.salesforce.com/s/articleView?id=sf.products_def.htm), [Price Book](https://help.salesforce.com/s/articleView?id=sf.products_pricebooks.htm), [Asset](https://help.salesforce.com/s/articleView?id=sf.assets_def.htm), and [Opportunity Product](https://help.salesforce.com/s/articleView?id=sf.products_opps.htm). 
- [API access](https://help.salesforce.com/s/articleView?id=sf.integrate_api_enable.htm) must be enabled for the user who authorizes the integration.

# Integrate Salesforce with CleverTap to Import Data

The following sections outline how to set up and use this integration step-by-step:

1. [Connect Salesforce to Your CleverTap Account](doc:salesforce-crm-import#connect-salesforce-to-your-clevertap-account)
2. [Import Profiles from Salesforce to CleverTap](doc:salesforce-crm-import#import-profiles-from-salesforce-to-clevertap) or  
   [Import Events from Salesforce to CleverTap](doc:salesforce-crm-import#import-events-from-salesforce-to-clevertap)

## Connect Salesforce to Your CleverTap Account

To begin syncing data from Salesforce to CleverTap, a secure connection must be established between the two platforms. This section outlines how to create that connection from within the Salesforce interface.

1. Select ![](https://files.readme.io/44a8fb78a662226f376cb2676d584f3306b1647be8a454f3c3fc07738c721478-Applauncher.png)and search for _CleverTap_, and select the app from the results. 

   [block:image]{"images":[{"image":["https://files.readme.io/e12006960e4988c50a37249d609adad8597f2d095352ba56e50f03f7d4284bf8-applauncher_ct.png","","App Launcher - Salesforce"],"align":"center","border":true,"caption":"App Launcher - Salesforce"}]}[/block]

2. Select the _CleverTap Settings_ tab and click **Add New Connection**. 

   [block:image]{"images":[{"image":["https://files.readme.io/37d3b1c5c3e3cc6ad4afe053b75e6ec1efb4fef9b4b73389d669a49daffa16ec-add_new_connection.png","","Add New Connection - Salesforce"],"align":"center","border":true,"caption":"Add New Connection - Salesforce"}]}[/block]

3. Enter the following integration details:

   - **Region**: Data center corresponding to the CleverTap instance (for example, `in1`, `us1`). This can be determined from the dashboard URL. To identify the region of your account, refer to [API endpoints](https://developer.clevertap.com/docs/api-endpoint).
   - **Connection Name**: Label to identify the integration instance (for example, _Salesforce Production_).
   - **Account ID**: Identifier for your CleverTap account. You can find this under the _Settings_ > _Project_ section of the CleverTap dashboard.
   - **API Passcode**: Found under _Settings_ > _Project_. For more information, refer to the [API Passcode Documentation](https://developer.clevertap.com/docs/authentication#create-account-passcode). 
     - [block:image]{"images":[{"image":["https://files.readme.io/fe96b79870c8cc442713d56f2ac75c22203fefba82eb9723d0cca15b2ea59196-New_connection.png","","Connection Details - Salesforce"],"align":"center","sizing":"65% ","border":true,"caption":"Enter Connection Details on Salesforce Dashboard "}]}[/block]

4. Click **Save**. The _Connections_ listing table displays the connection name, region, and account ID.

The _Actions_ column provides options to **Delete**, **Edit**, or **Map Field**, which allow administrators to manage the connection and configure data mapping. 

## Import Profiles from Salesforce to CleverTap

A sync must be configured from the Salesforce connection to bring user data, such as leads, contacts, or accounts, into CleverTap as unified profiles. The steps below describe how to map and import profile data. This example illustrates importing a Lead object into CleverTap to build enriched user profiles.

1. Select **Map Field** from the _Actions_ column for the corresponding connection. 

   [block:image]{"images":[{"image":["https://files.readme.io/64dee680b032188d1df21c96ac33f26c22a4034b0d0cc2715838eab4fc51275e-map_field.png","","Map field - Salesforce"],"align":"center","border":true,"caption":"Map field - Salesforce"}]}[/block]

2. Click **Add New Sync**. 

   [block:image]{"images":[{"image":["https://files.readme.io/0b49530a673f5c6d2d4310b59fb37369ebc8aaea87e8d10e8242f17529670ca6-Add_new_sync.png","","Add new sync - Salesforce"],"align":"center","border":true,"caption":"Add new sync - Salesforce"}]}[/block]

3. Enter the following configuration values and click **Next**.

   - **Sync Name**: A name for the sync job (for example, _Lead Profile Sync_).
   - **Sync Type**: This value is fixed as **Salesforce to CleverTap**.
   - **Source Entity**: The Salesforce object from which data will be imported. CleverTap supports the following objects: [Lead](https://help.salesforce.com/s/articleView?id=sf.leads_def.htm), [Contact](https://help.salesforce.com/s/articleView?id=sf.contacts_def.htm), [Account](https://help.salesforce.com/s/articleView?id=sf.accounts_def.htm), [Opportunity](https://help.salesforce.com/s/articleView?id=sf.opps_def.htm) , [Case](https://help.salesforce.com/s/articleView?id=sf.cases_def.htm), [Campaign](https://help.salesforce.com/s/articleView?id=sf.campaigns.htm), [Event](https://help.salesforce.com/s/articleView?id=sf.events.htm), [Task](https://help.salesforce.com/s/articleView?id=sf.tasks.htm), [Campaign Member](https://help.salesforce.com/s/articleView?id=sf.campaignmembers.htm), [Service Appointment](https://help.salesforce.com/s/articleView?id=sf.field_service_object_fields.htm&type=5), [Quote](https://help.salesforce.com/s/articleView?id=sf.quotes.htm), [Contract](https://help.salesforce.com/s/articleView?id=sf.contracts.htm), [Order](https://help.salesforce.com/s/articleView?id=sf.orders.htm), [Product](https://help.salesforce.com/s/articleView?id=sf.products.htm), [Price Book](https://help.salesforce.com/s/articleView?id=sf.products_pricebooks.htm), [Asset](https://help.salesforce.com/s/articleView?id=sf.assets.htm), and [Opportunity Product](https://help.salesforce.com/s/articleView?id=sf.products_opportunitylineitems.htm). In this example, select **Lead** as the source entity to sync lead records into CleverTap.
   - **Target Entity**: Select **Profile**.

     [block:image]{"images":[{"image":["https://files.readme.io/5c9573cfd197a12f8b98bd21151f7447dbb05ed06ffeeb608b2f677f635a6170-new_sync_config_-_Profile.png","","New Sync Configuration - Profile"],"align":"center","border":true,"caption":"Configure New Sync - Salesforce"}]}[/block]

4. Under the _Required Mapping_ section, map the **Customer ID** field.

- This field is mandatory and serves as the primary identifier for user profiles in CleverTap.
- It may be mapped to a relevant Salesforce field such as Lead ID, Master Record ID, Email, First Name, or Last Name.
- For example, mapping _Lead ID_ ensures each CleverTap profile is uniquely associated with a Salesforce lead. 
- For our Lead example, you can map `Lead.Id` to Customer ID and use a prefix such as `SF_Lead_{{Lead.Id}}` to prevent conflicts with other objects.
- Refer to the [Salesforce Object Reference](https://developer.salesforce.com/docs/atlas.en-us.object_reference.meta/object_reference/sforce_api_objects_concepts.htm) for details on identifier fields.

1. Under the _Additional Fields_ section, select **Add Field** to define optional mappings.

   - For instance, map: 
     - **Target Field**: `Email` → Source Field: `Lead.Email`
     - **Target Field**: `City` → Source Field: `Lead.City`
   - **Data Type**: The data format (for example, _String_, _Number_, _Date_), ensuring correct processing in CleverTap

2. Add mappings as necessary and click **Save** to complete the profile import setup. 

   [block:image]{"images":[{"image":["https://files.readme.io/a15a256e3dce66bad4e03536884d10ef1a2a311982cd22daa8420ad4c8ac6811-Filed_mapping_profile.png","","Mapping fields - Profile"],"align":"center","border":true,"caption":"Mapping Profile Fields on Salesforce Dashboard"}]}[/block]

## Import Events from Salesforce to CleverTap

Event syncs can be configured to capture behavioral data such as opportunity creation, status changes, or lifecycle events from Salesforce into CleverTap. The steps below guide you through mapping and importing Salesforce events into CleverTap.

1. Click **Map Field** from the _Actions_ column for the corresponding connection. 

   [block:image]{"images":[{"image":["https://files.readme.io/165ded573a6c63e67f868c965fa7fb276ec12716dbc735bcca502889db0d715a-map_field.png","","Map field - Salesforce"],"align":"center","border":true,"caption":"Map field - Salesforce"}]}[/block]

2. Click **Add New Sync** button. 

   [block:image]{"images":[{"image":["https://files.readme.io/969b0feb4caf4cc51f2ae36ce2ef63d14588ed539af4f5bcbe3e0a8f5c55fe02-Add_new_sync.png","","Add New Sync"],"align":"center","border":true,"caption":"Add New Sync on Salesforce Dashboard"}]}[/block]

3. Enter the following configuration values:

   - **Sync Name**: A name for the sync job (For example, _Lead Event Sync_).
   - **Sync Type**: This value is fixed as **Salesforce to CleverTap**. 
   - **Source Entity**: The Salesforce object from which data will be imported. CleverTap supports the following objects: [Lead](https://help.salesforce.com/s/articleView?id=sf.leads_def.htm), [Contact](https://help.salesforce.com/s/articleView?id=sf.contacts_def.htm), [Account](https://help.salesforce.com/s/articleView?id=sf.accounts_def.htm), [Opportunity](https://help.salesforce.com/s/articleView?id=sf.opps_def.htm) , [Case](https://help.salesforce.com/s/articleView?id=sf.cases_def.htm), [Campaign](https://help.salesforce.com/s/articleView?id=sf.campaigns.htm), [Event](https://help.salesforce.com/s/articleView?id=sf.events.htm), [Task](https://help.salesforce.com/s/articleView?id=sf.tasks.htm), [Campaign Member](https://help.salesforce.com/s/articleView?id=sf.campaignmembers.htm), [Service Appointment](https://help.salesforce.com/s/articleView?id=sf.field_service_object_fields.htm&type=5), [Quote](https://help.salesforce.com/s/articleView?id=sf.quotes.htm), [Contract](https://help.salesforce.com/s/articleView?id=sf.contracts.htm), [Order](https://help.salesforce.com/s/articleView?id=sf.orders.htm), [Product](https://help.salesforce.com/s/articleView?id=sf.products.htm), [Price Book](https://help.salesforce.com/s/articleView?id=sf.products_pricebooks.htm), [Asset](https://help.salesforce.com/s/articleView?id=sf.assets.htm), and [Opportunity Product](https://help.salesforce.com/s/articleView?id=sf.products_opportunitylineitems.htm). In this example, select **Lead** as the source entity to sync lead records into CleverTap.
   - **Target Entity**: Select **Event**

4. Select **Next**. 

   [block:image]{"images":[{"image":["https://files.readme.io/75b517bf4301abe6dff804ddf3f1dff765a8c16b00cdc7728d5129f58fcc052e-new_sync_config.png","","New Sync Configuration - Salesforce"],"align":"center","border":true,"caption":"New Event Sync Configuration"}]}[/block]

5. Under the _Required Mapping_ section, map the **Customer ID** and **Event Name** fields.

   - These fields are mandatory and serve as the primary identifiers for events in CleverTap.
   - **Customer ID** may be mapped to a relevant Salesforce field such as Lead ID, Master Record ID, Email, First Name, or Last Name. For example, if using a Lead as the source entity, map the Customer ID to the Lead ID field and prefix it (for example, `SF_Lead_{{Lead.Id}}`) to ensure uniqueness and consistent identity resolution.
   - **Event Name** may be a static value (for example, _Opportunity Created_) or dynamically mapped from a Salesforce field.
   - For more information on identifier fields, refer to the [Salesforce Object Reference](https://developer.salesforce.com/docs/atlas.en-us.object_reference.meta/object_reference/sforce_api_objects_concepts.htm) 

6. Under the _Additional Fields_ section, select **Add Field** to define optional mappings.

   - **Target Field**: The field in CleverTap where the event attribute will be stored
   - **Source Field**: The Salesforce field from which the data originates
   - **Data Type**: The data format (for example, _String_, _Number_, _Date_), ensuring correct processing in CleverTap

7. Add mappings as necessary and click **Save** to complete the event import setup. 

   [block:image]{"images":[{"image":["https://files.readme.io/a6a940e42434efb04faf2ec60daf6ad1876b0965b5c1f5158bab956f636878ae-Field_mapping_.png","","Mapping Fields - Salesforce"],"align":"center","border":true,"caption":"Field Mapping - Lead to Event"}]}[/block]

# Verify Imported Records in CleverTap

Once a record, such as a Lead, Contact, or Opportunity, is created in Salesforce, and the sync is active, the data should appear in CleverTap. The steps below outline how to confirm the successful import of these records. To create a new object in Salesforce (for example, Lead or Contact), refer to [Salesforce: Add Records](https://help.salesforce.com/s/articleView?id=sf.create_records.htm).

## On Salesforce Dashboard

To locate the source event and retrieve the record's identifier from Salesforce, perform the following steps

1. Select the _Events Log_ tab in the Salesforce dashboard and locate the event for the newly created record.
2. Click the ![](https://files.readme.io/75102dc9aae3047d66d82768c5c8bdf8171119b5f9e8155fc63ad1d171a68b3c-drop_down.png) icon and click **View Details**. 

   [block:image]{"images":[{"image":["https://files.readme.io/364c7ef042ab199c2444c0869e6fba2922f35d2c8508e2242381a38d7d0f09a8-verifying.png","","View Details - Salesforce"],"align":"center","border":true,"caption":"View Event Details on Salesforce Dashboard"}]}[/block]
3. Copy the record’s unique ID (for example, _Lead ID_, _Contact ID_, _Opportunity ID_). 

   [block:image]{"images":[{"image":["https://files.readme.io/9276821d362a652649e7dcfcec0df2d57c2f25fe83a4d6e804d7e01c13529100-verifying_salesforce.png","","Unique ID - Salesforce"],"align":"center","sizing":"65% ","border":true,"caption":"Unique ID - Salesforce"}]}[/block]

## On CleverTap dashboard

To verify if the record has been successfully imported into CleverTap, perform the following steps:

1. From the CleverTap dashboard, go to _Segments_ > _Find People_ > _By Identity_. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4d967022db53847260b616dfdd2251ffbfafa67fee3564349522ef8c79a52421-veryfying_ct_1.png",
        "",
        "Search profiles - CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Search Imported Profiles on CleverTap Dashboard"
    }
  ]
}
[/block]


2. Paste the copied ID into the identity input field.
3. Click **Find**. If the sync is successful, the corresponding CleverTap user profile will appear. 

   [block:image]{"images":[{"image":["https://files.readme.io/1dd47a86701d7d85b9aa31fea8f8fbd8b1f4783fe1117960679c2dac13923d43-verifying_ct_.png","","Imported Record - CleverTap"],"align":"center","border":true,"caption":"Imported Record - CleverTap"}]}[/block]

# FAQs

This section addresses frequently asked questions related to the Salesforce integration with CleverTap.

### What is historical data import in the Salesforce integration?

Historical import enables you to backfill previously captured Salesforce records into CleverTap. This ensures that all relevant CRM data is available for segmentation, analysis, and engagement within CleverTap, even for events or profiles created before the integration was set up.

### How can I trigger a historical data sync?

To trigger a historical sync:

1. Open the Salesforce dashboard and navigate to _CleverTap Settings_.
2. Under the _Integration Sync List_, locate the sync for which you want to import historical data.
3. Click the ![](https://files.readme.io/3588d6052ccec01069b828a02b6ed4d763eebfa97727c622e80c53c6ceabfe4b-drop_down.png) icon next to the sync name and select **Historical Sync**.

   1. [block:image]{"images":[{"image":["https://files.readme.io/9ed036c002ad06c340f17d846e8d33521df9f202cba621e7ff21db0c0b4ac453-Historical_Sync.png","","Historical Sync - Salesforce"],"align":"center","border":true,"caption":"Historical Sync - Salesforce"}]}[/block]

### Where does the historical data appear after sync?

Once the sync is complete:

- The imported data is logged in the _CleverTap Event Logs_ within Salesforce.
- It also becomes accessible in the CleverTap dashboard under _Segments → Find People_ for immediate use in segmentation, journeys, and analytics.

# Best Practices for Identity Mapping

To ensure accurate user attribution during data syncs, identity fields from Salesforce must map consistently to user profiles in CleverTap. This section outlines best practices, naming conventions, and edge case considerations for both profile and event imports.

## Identity Mapping for Profiles

When importing Salesforce objects as CleverTap profiles, the **Customer ID** acts as the unique identifier for each user. This field determines which profile the record will update or create in CleverTap.

The table below shows recommended identifiers for common Salesforce objects:

| Salesforce Object | Recommended Identifier |
| ----------------- | ---------------------- |
| Lead              | `SF_Lead`              |
| Contact           | `SF_Contact`           |
| Account           | `SF_Account`           |
| Opportunity       | `SF_Opportunity`       |

Use Salesforce’s **Record ID** (for example, `Lead.Id`, `Contact.Id`) as the source value. Prefix the ID with the object type (for example, `SF_Lead_{{Lead.Id}}`) to prevent identifier conflicts between different object types. This approach ensures uniqueness and improves profile traceability.

Avoid mapping identity to **non-unique or mutable fields** such as:

- `Email`
- `Phone Number`
- `First Name` or `Last Name`

These values can change, leading to duplicate or orphaned profiles.

## Identity Mapping for Events

When importing Salesforce objects as events into CleverTap, the **Customer ID** in the event payload must exactly match the identity of an existing user profile in CleverTap.

Use the same prefix strategy and identifier as used in profile imports. For example:

- Lead-related event → `SF_Lead_{{Lead.Id}}`
- Contact-related event → `SF_Contact_{{Contact.Id}}`

If you are importing **only events** and not corresponding profiles, ensure the identity value already exists in CleverTap. Otherwise, the event may be dropped or result in incomplete records. If an identity mismatch occurs, CleverTap cannot link the event to any user profile.

## General Guidelines

The following guidelines apply to all identity mappings—across both profile and event imports:

- **Prefixing IDs**: Always use a unique prefix (for example, `SF_Lead_`, `SF_Contact_`) to avoid collisions between different Salesforce object types.
- **Consistency across syncs**: Maintain a uniform identity convention for both profile and event syncs.
- **Dynamic mapping**: Use field expressions or dynamic token substitution where possible to avoid hardcoding values.
- **Initial validation**: Run a test sync to confirm identity consistency and correctness before scheduling a full import.
- **Documentation**: Internally document your identity strategy for ongoing reference by marketing, analytics, and CRM teams.