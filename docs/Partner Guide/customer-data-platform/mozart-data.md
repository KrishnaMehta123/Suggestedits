---
title: Mozart Data
excerpt: Data Warehouse
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

[Mozart Data](https://www.mozartdata.com) offers a modern data stack that simplifies data consolidation, transformation, and readiness for analytics. When integrated with CleverTap, Mozart Data enables a two-way data sync via Snowflake, allowing for scalable behavioral analysis and personalized engagement.

With this integration, you can:

- Import enriched or external data from Mozart into CleverTap via Snowflake.
- Run business intelligence (BI) tools on Snowflake to uncover actionable insights.

# Prerequisites

Ensure the following before starting the integration:

- You have an active Mozart Data account.
- Snowflake Exports are enabled in your CleverTap account.
- You have access credentials to your Snowflake data warehouse.

# Integrate CleverTap with Mozart Data

To integrate CleverTap with Mozart Data, follow these three main steps to prepare, schedule, and import user profile data into CleverTap:

1. [Create Source and Destination Connectors in Mozart](doc:mozart-data#create-source-and-destination-connectors-in-mozart)
2. [Create a Transform in Mozart](doc:mozart-data#create-a-transform-in-mozart)
3. [Create a Snowflake Import in CleverTap](doc:mozart-data#create-a-snowflake-import-in-clevertap)

## Create Source and Destination Connectors in Mozart

Set up Mozart to connect your data sources and Snowflake. To do so, perform the following steps:

1. Go to _Connectors_, select the data source type in the Mozart dashboard. Out of the available options in Mozart Data or upload a CSV file to Mozart Data.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0e27f60ab8136a730e58cded6a2cffaf9c898bb98d7bc2c46aff13b5a501b656-image.png",
        null,
        "Add Connector"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Add Connector"
    }
  ]
}
[/block]


2. Select the type of _Integration_ you want to add. Search by typing in the search bar. Then click on the connector icon. For this use case, we will select _Snowflake_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/443c5a7f546c2b8ae0d579cf928ffbc0922e2c9d9dd32162ab8e3796f03f822a-image.png",
        null,
        "Type of Integration"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Type of Integration"
    }
  ]
}
[/block]


2. Create a **Snowflake destination connector**.
   1. This will redirect you to Fivetran to authenticate your Snowflake account.
   2. Enter your credentials and click **Save & Test**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d6816ad7423fb25ac89fbb297c8a10809c4fde21676a371141e0b8c3233aa200-image.png",
        null,
        "Snowflake destination connector"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Snowflake destination connector"
    }
  ]
}
[/block]


For information, refer to [Mozart Data Connectors](https://help.mozartdata.com/docs/connectors).

This completes the initial connection between the source and Snowflake.

## Create a Transform in Mozart

Use transforms in Mozart to clean and prepare your data for import. To do so, perform the following steps:

1. Go to the **Warehouse** tab.
2. Click **Create Transform**, enter all the needed details, and click **Create**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/36c99c172910f258c565e61b8af39b032f6c38cb7bc7d7c7cb2bba31712e44fe-image.png",
        null,
        "Create Transform"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Create Transform"
    }
  ]
}
[/block]


3. Add the data you want to fetch from the source you have connected using a SQL query. For this example, we have uploaded a CSV file. Ensure your source also contains a field for `timestamps` /  `Updated at timestamp`.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1f63f4003ad36bcc9c2c88fcad2caf277d3a9dc3bf51a974ea36cbb7d4a875a2-image.png",
        null,
        "Filter the data from the source"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Filter the data from the source"
    }
  ]
}
[/block]


4. Click **Save** and **Run**.
5. Go to the _Runs_ tab to verify that the query executes properly.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1f63f4003ad36bcc9c2c88fcad2caf277d3a9dc3bf51a974ea36cbb7d4a875a2-image.png",
        null,
        "Verify The Query"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Verify The Query"
    }
  ]
}
[/block]


This step prepares your data for loading into Snowflake on a schedule.

## Create a Snowflake Import in CleverTap

Set up CleverTap to import Mozart-prepped user data from Snowflake. To do so, perform the following steps:

1. Go to _Settings_ > _Partners_ > _Connections_ in your CleverTap dashboard.
2. Click **Snowflake**, fill in your credentials, and click **Save**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/aa58040ff97292abfebc6f262f6fe1747000ab00a0246d366a45a5c17bec598f-image.png",
        null,
        "Create a Snowflake Import in CleverTap"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Create a Snowflake Import in CleverTap"
    }
  ]
}
[/block]


3. Go to _Settings_ > _Imports_ and click **Create Import**.
4. Select **Snowflake** as the source.
5. Configure the import:

   - Use **Table Preview** if the data resides in the `PUBLIC` schema.
   - Use a **Custom SQL Query** for non-public schemas.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/187dbb2498af45ce2712c8a6d60cac88bf0c0e1f875edb0aa2de955a8d1e73a4-image.png",
        null,
        "Configure the import"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Configure Import"
    }
  ]
}
[/block]


6. Map the fields, select the data according to your requirements, and click **Test data**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b8e6fb7b17684a03c83049209b001c189fcdb3bfa0e526b7cde723a8e56fc3b8-image.png",
        null,
        "Map Fields"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Map Fields"
    }
  ]
}
[/block]


7. Schedule and run the import to see the data flow into your CleverTap account.
8. Verify the imported data by navigating to the Segments page from the CleverTap dashboard.

   [block:image]{"images":[{"image":["https://files.readme.io/9c67c4f82a5c59a2cb9a04f9953453e665e9a85a2a9bf2a2831573155e387974-image.png",null,"Verify Imported Data"],"align":"center","sizing":"75% ","border":true,"caption":"Verify Imported Data"}]}[/block]

Once the import is successful, the enriched user data from Mozart will be available in CleverTap, ready to power segmentation, campaign targeting, and personalized engagement journeys.