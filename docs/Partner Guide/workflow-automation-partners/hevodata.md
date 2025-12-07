---
title: HevoData
excerpt: Workflow Automation
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

[HevoData](https://hevodata.com/) is a no-code data pipeline platform that enables businesses to integrate data from multiple sources into cloud data warehouses like Snowflake, BigQuery, and Redshift. 

By integrating CleverTap with HevoData, businesses can automate the transfer of customer engagement data to central repositories, enabling real-time analytics, personalized marketing, and data-driven decision-making. For example, with this integration, you can:

- Customer Behavior Analytics: Track and analyze user interactions from CleverTap in a data warehouse for insights into customer journeys and engagement trends.
- Personalized Marketing Campaigns: Leverage centralized data to build highly targeted and automated marketing strategies.
- Real-time Decision-Making: Sync real-time event data for faster response to customer behaviors.

# Prerequisites for Integration

The following are the prerequisites for HevoData integration:

- Ensure you have access to an active HevoData account with permission to create pipelines.
- Ensure you have a destination Data Warehouse or Database set up and accessible in HevoData account.
- Ensure you have a CleverTap account with valid **Account ID**, **Passcode**,**Region** and **Events CSV** file (contains event names for ingestion).

> 🚧 Support For Integration
> 
> This integration is managed and continuously improved by HevoData. The CleverTap and HevoData integration has undergone stringent testing to ensure seamless functionality. For any questions or issues, contact [HevoData](https://hevodata.com/contact/) for support and resolution.

# Integrate HevoData with CleverTap

Consider this as an example where you are a growth analyst at an e-commerce company using CleverTap to track user interactions such as app launches, product views, and purchases. To analyze this data effectively, you need to centralize it in Snowflake for insights into user behavior trends, retention metrics, and personalized marketing campaigns. By integrating CleverTap with HevoData, you can automate data ingestion into Snowflake, eliminating manual exports and ensuring real-time data availability.

This process involves the following three major steps:

1. [Set Up a Pipeline in HevoData.](doc:hevodata#set-up-a-pipeline-in-hevodata)
2. [Add CleverTap as a Source on HevoData.](doc:hevodata#add-clevertap-as-a-source-on-hevodata)
3. [Configure Data Pipelines](doc:hevodata#configure-data-pipelines)

## Set Up a Pipeline in HevoData.

Create a pipeline to transfer data from CleverTap to your destination (for example, Snowflake, BigQuery, or Redshift). This pipeline automates data ingestion and ensures a continuous flow of customer engagement data. Follow these steps to set it up:

1. Navigate to the left side panel and click on **Pipelines** in HevoData.
2. Click on **+ Create Pipeline** to create new pipeline.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4ebdeb7f8823cedbdb01382dcba1b58bc5b1c552a7771d5cc2effd64e208d421-image.png",
        null,
        "Set Up a Pipeline in HevoData"
      ],
      "align": "center",
      "border": true,
      "caption": "Set Up a Pipeline in HevoData"
    }
  ]
}
[/block]


## Add CleverTap as a Source on HevoData.

Connect your CleverTap account to HevoData by providing authentication details such as the Project ID, Passcode, and Region. Upload the Events CSV file to specify the data to be transferred. To do so, follow these steps:

1. In the source search box, type _CleverTap_ and select it.
2. Enter the following details:

| Field                       | Description                                                                                                                                                                                                                              |
| :-------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Pipeline Name               | Provide a unique name for your pipeline (max 255 characters).                                                                                                                                                                            |
| Project ID                  | Locate the Project ID under _Settings_ > _Project_ from the CleverTap dashboard.                                                                                                                                                         |
| Project Passcode            | Locate the Passcode under _Settings_ > _Project_ from the CleverTap dashboard. For more information, refer to [Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).                           |
| Region                      | Locate _Region_ for the API endpoint you want to select under _Settings_ > _Project_. To find the API endpoint for your region, refer to [API endpoints based on your data center region](https://developer.clevertap.com/docs/idc#api). |
| Events File (In CSV format) | Upload the CSV file containing CleverTap event names. Refer to [Download Schema Data from Dashboard for downloading the event files.](doc:schema#download-schema-data-from-dashboard)                                                    |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/60733e1e875cbc22bc3f8a9647993f7f77b980e57cbbb8fe37186b041942371e-image.png",
        null,
        "Add CleverTap as a Source"
      ],
      "align": "center",
      "border": true,
      "caption": "Add CleverTap as a Source"
    }
  ]
}
[/block]


3. Click **TEST & CONTINUE** to validate the connection.

## Configure Data Pipelines

Define the data flow settings by selecting the events to replicate, select a destination, setting up ingestion frequency, and activating the pipeline. This step ensures seamless and scheduled data synchronization. To do so, follow these steps:

1. In the _Select Objects_ section, choose the user events you want to replicate.
   - By default, all objects are selected.
   - Uncheck any events you do not want to include.
2. Click **CONTINUE** once the required objects are selected.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e7a513f0b6dd58aaedf1f51db90b979d0885bcb7a04bba8c5782a4d2604f416f-image.png",
        null,
        "Select Objects"
      ],
      "align": "center",
      "border": true,
      "caption": "Select Objects"
    }
  ]
}
[/block]


3. Select an existing destination in the _Configure Destination_ section or click **+ ADD DESTINATION** to configure a new one.
   - You can search for a destination using the search bar.
   - For this example, we use [Snowflake](https://docs.hevodata.com/destinations/data-warehouses/snowflake/?utm_source=docs_sidebar).
   - Refer to the [Destinations](https://docs.hevodata.com/destinations/) for specific destination setup instructions.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5fca44b5303e0fc3574ed999f0816bebb67ae6dc2eb6368ec928c8f15098f963-image.png",
        null,
        "Configure Destination"
      ],
      "align": "center",
      "border": true,
      "caption": "Configure Destination"
    }
  ]
}
[/block]


4. _Configure Destination _ setup involves setting up how data is structured and transferred to the destination. It includes:
   1. _Destination Table Prefix_: Add a prefix for tables (optional). A prefix can help you identify the tables loaded by a specific Pipeline. Hevo appends an underscore (\_) to the prefix.
   2. _Auto Mapping_: Enable or disable automatic schema mapping for the pipeline.
   3. _Pipeline Ingestion Schedule_: Set the ingestion frequency for all objects in the pipeline.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4bc21b5813ff6a7ff66ad6c850df8f938fe277f690a61a1fdbc27e93c623b34f-image.png",
        null,
        "Configure Destination"
      ],
      "align": "center",
      "border": true,
      "caption": "Configure Destination"
    }
  ]
}
[/block]


5. Click **CONTINUE** to activate the pipeline, then verify that data appears in _Snowflake_ or your chosen data warehouse.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/864827544f882bb530b1b6c4c0932c2ee3118864abd2c5110d4465a49c2a978b-image.png",
        null,
        "Verify data in Snowflake"
      ],
      "align": "center",
      "border": true,
      "caption": "Verify data in Snowflake"
    }
  ]
}
[/block]


# Key Points to Remember

Keep these essential details in mind when working with data replication.

## Data Replication Details

HevoData fetches event records from CleverTap at scheduled intervals. The ingestion frequency depends on the HevoData version you are using.

| **Release Version** | **Default Frequency** | **Minimum Frequency** | **Maximum Frequency** | **Custom Frequency (Hrs)** |
| ------------------- | --------------------- | --------------------- | --------------------- | -------------------------- |
| Before 2.21         | 30 minutes            | 5 minutes             | 24 hours              | 1-24                       |
| After 2.21          | 6 hours               | 30 minutes            | 24 hours              | 1-24                       |

### Key Considerations

- Custom frequencies must be set in whole hours (For example, 1, 2, and 3  hours, but not 1.5 or 1.75 ).
- HevoData retrieves event data using CleverTap’s [Get Events API](https://developer.clevertap.com/docs/get-events-api).
- Historical Data: In the first run of the Pipeline, Hevo ingests the data of the past 30 days for the Events object in your CleverTap account.
- Incremental Data: Once the historical load is complete, data is ingested as per the [ingestion frequency](https://docs.hevodata.com/data-ingestion/ingestion-and-loading-frequency/#ingestion-frequency) in Full Load or Incremental mode, as applicable.

This ensures timely and accurate data replication, allowing businesses to analyze real-time customer interactions efficiently.

## Limitations

- Event Size Restriction: Events larger than **128 MB** are not ingested by Hevo.
- Data Discrepancy Prevention: Ensure each row in the source is under **100 MB** to avoid ingestion failures.

> 📘 Additional Note:
> 
> CleverTap’s Get Events API returns duplicate data for some Events. Read [Schema and Primary Keys](https://docs.hevodata.com/sources/analytics/clevertap-source/#schema-and-primary-keys) to understand how Hevo handles this.
> 
> You can also fetch data from CleverTap in real-time using a Pipeline with a [Webhook Type Source](https://docs.hevodata.com/sources/sdk-&-streaming/webhook/) in Hevo and use [CleverTap webhooks](https://developer.clevertap.com/docs/webhooks) with it.