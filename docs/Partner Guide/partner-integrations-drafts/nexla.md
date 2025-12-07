---
title: Nexla
excerpt: '@shreyans to conform the catagory'
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

[Nexla](https://www.nexla.com) is a unified data operations platform that enables teams to connect, transform, and monitor ready-to-use data across any system. Designed for analytics and AI workflows, Nexla simplifies complex data integrations using no-code and low-code tools.

With the CleverTap and Nexla integration, you can:

* Export campaign interaction events from CleverTap to data warehouses using *Data Warehouse Exports* or *Webhook campaigns*.
* Transform and forward enriched data from Nexla to CleverTap using *Amazon S3*, *SFTP Imports*, or *Nexla’s REST API*.

This integration enables real-time, high-quality data flow between CleverTap and your enterprise data stack, powering personalized engagement and advanced analytics.

# Prerequisites for Integration

Ensure the following before starting the integration:

* An active [Nexla](https://www.nexla.com) account
* Automated *Data Warehouse Exports* or *Webhook campaigns* configured in CleverTap
* Access to your *BigQuery* , or *Amazon S3* account

# Integrating Nexla with CleverTap

To integrate Nexla with CleverTap, perform the following five major steps:

1. [Export Data from CleverTap](doc:nexla#export-data-from-clevertap-to-your-data-warehouse)
2. [Add Data Source in Nexla](doc:nexla#add-data-source-in-nexla)
3. [Send Webhook Data from CleverTap to Nexla](doc:nexla#send-webhook-data-from-clevertap-to-nexla-optional) (Optional)
4. [Transform Data in Nexla](doc:nexla#transform-data-in-nexla)
5. [Import Data Back into CleverTap](doc:nexla#import-data-back-into-clevertap)

## Export Data from CleverTap to Your Data Warehouse

Use Data Warehouse Exports in CleverTap to send campaign interaction data to supported destinations such as:

* Google Cloud Storage
* Amazon S3 Exports

<Image alt="Create Export" align="center" width="75% " border={true} src="https://files.readme.io/d2bd87a881b08611cf192e3ce42e5875793ac33c1830a6eabfe5fdbd6f7cac3b-image.png">
  Create Export
</Image>

Once configured, Nexla can pull this data directly from the connected source. Refer to the [Data Warehouse Export Guide](doc:data-warehouse) for setup instructions.

## Add Data Source in Nexla

To configure your data source, perform the following steps:

1. Log in to the Nexla console.
2. Add the appropriate warehouse (such as BigQuery or Amazon S3).
3. Authenticate using your access credentials.
4. Once connected, Nexla will begin ingesting the exported CleverTap data.

Refer to the [Add a Data Source in Nexla](https://docs.nexla.com/user-guides/data-sources/how-to-add-a-data-source) for details.

## Send Webhook Data from CleverTap to Nexla (Optional)

You can optionally use Webhook campaigns in CleverTap to push event data to Nexla in real time:

* In CleverTap, create a Connector Campaign with Nexla’s webhook URL as the endpoint.
* Use this approach if you want immediate data delivery without waiting for exports.

To configure Webhooks, refer to [Send Webhooks from CleverTap](doc:create-message-webhook) and [Nexla Webhook Reference](https://docs.nexla.com/user-guides/connectors/webhook)

## Transform Data in Nexla

To apply custom logic or formatting before sending data to CleverTap, perform the following steps:

1. Locate the dataset in Nexla and click **Transform**.
2. Use the *Transform Builder* to:

   * Rename fields
   * Apply conditions or filters
   * Add computed fields or enrichments
3. Click **Save** to transform the dataset.

For more information, refer to [Using the Transform Builder](https://docs.nexla.com/user-guides/transformations)

## Import Data Back into CleverTap

You can send data from Nexla into CleverTap using two options:

1. [Nexla REST API Destination](doc:nexla#option-a-nexla-rest-api-destination)
2. [Using SFTP Imports](doc:nexla#option-b-using-sftp-imports)

### Option A: Nexla REST API Destination

* Configure [Nexla](https://docs.nexla.com/user-guides/connectors/rest-api/rest-api-generic#3-data-destination) to use [CleverTap’s Upload Users or Events API](https://developer.clevertap.com/docs/api-overview).
* Format the JSON payload to match the API’s requirements.
* Ensure the following headers are set:

```
Authorization: <Account ID + Passcode>
Content-Type: application/json
```

<Image alt="Edit Credentials" align="center" width="55% " border={true} src="https://files.readme.io/8e3197252c1565d94e0d79b56d15ba19467068d788e52ac40a4245dc9990cd94-image.png">
  Edit Credentials
</Image>

> ⚠️ Note
>
> Disable Nexla’s credential validation. Set header values manually using your CleverTap credentials.

### Option B: Using SFTP Imports

* Export the transformed dataset from Nexla to a supported destination (for example, SFTP).
* Configure CleverTap to import the data using its native import capability.

Refer to [SFTP Import Documentation](https://developer.clevertap.com/docs/imports-via-sftp)

<Image alt="SFTP Imports" align="center" width="55% " border={true} src="https://files.readme.io/63788bc898378ab2ed85fc3bbdd67d7e5ad990db37e0d1db7ea80dad09df3db7-image.png">
  SFTP Imports
</Image>

# Verify the Integration

Once your data flow is set up:

* Nexla monitors source and destination schema changes
* Errors are flagged and visible in the Nexla dashboard
* Any edits to the flow (such as sources, transformations, and destinations) are reflected automatically

This enables a fully automated, scalable, and error-resilient integration between Nexla and CleverTap.
