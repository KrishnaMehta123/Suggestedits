---
title: Catalogs (wip)
excerpt: Learn how to use Catalogs for sending personalized campaigns
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Overview

A Catalog enables you to personalize campaigns with dynamic information (such as product prices or inventory levels) in your messages. Using a catalog, you can send automated campaigns powered with personalized product recommendations based on your user's location. For example, you can send distinct and personalized web series recommendations for users residing in the USA and India.

# Download a Sample Catalog

Sample catalog files (.CSV files) help you get started with creating your catalog. There are two types of Catalogs:

* Product Catalog
* Product Location Catalog

The following image represents a sample product catalog:

<Image title="Sample Product Catalog" alt="An image that shows the columns listed under Sample Product Catalog" align="center" className="border" border={true} src="https://files.readme.io/c047967-Sample_Product_Catalog.png" />

In a product location catalog, the identity represents the location ID. The following image represents a sample product location catalog:

<Image title="Sample_Product_Location_Catalog.png" alt={750} align="center" width="80%" border={true} src="https://files.readme.io/f6de8be-product_location_catalog.png">
  Sample Product Location Catalog
</Image>

To download a sample catalog, perform the following steps:

1. Navigate to *Settings* > *Catalogs*. 
2. Click the **Sample Product Location csv** or **Sample Product csv** link.

<Image title="Download Sample CSV" alt="Click Sample Product Location Catalog csv and Sample Product Catalog csv links to download the respective sample CSV files from the Catalogs page" align="center" border={true} src="https://files.readme.io/b4286e6-csv_catalog.png">
  Download Sample CSVs
</Image>

> 🚧 Mandatory Fields
>
> The following are the mandatory fields for each catalog type:
>
> * Product location: *identity*, *latitude*, and *longitude*.
> * Product: *Identity*, *Name*, and *ImageURL*.

# Create a New Catalog

To create a new catalog, perform the following steps:

1. Navigate to *Settings* > *Catalogs*. 
2. Click **+ Catalog**.
3. Select *Product* or *Product Location*.

<Image title="Create a New Catalog" alt="Click Plus Catalog button from the Catalogs page to create a new catalog" align="center" border={true} src="https://files.readme.io/c406e0e-Create_a_New_Catalog.png">
  Create a New Catalog
</Image>

4. Click **Browse** to search and upload a new catalog. The catalog file must be in a CSV format.

<Image title="Browse for product location catalog" alt="A prompt displays from where you can browse to the product location catalog file on your system" align="center" border={true} src="https://files.readme.io/70a32f1-Browse_for_product_location_catalog.png">
  Browse to the catalog CSV file location from your system
</Image>

> 📘 Upload Limit
>
> You can insert up to 10,000 rows from the dashboard; however, you can insert up to 5 million rows from our API. For more information, refer to [Catalog API](https://developer.clevertap.com/docs/catalog-api-endpoints).

5. Enter the Catalog name after the *Catalog preview* displays.
6. Click **Upload**.

<Image title="Upload Catalog" alt="Catalog Preview prompt opens from where you can click the Upload button to upload your catalog" align="center" border={true} src="https://files.readme.io/476ff67-Upload_Catalog.png">
  Click Upload to upload the catalog
</Image>

7. Click **Save Catalog**. 

<Image title="Save Catalog" alt="A prompt displays from where you can click Save button to save the uploaded catalog" align="center" width="smart" border={true} src="https://files.readme.io/b870255-Save_Catalog.png">
  Click Save Catalog to save the catalog
</Image>

The new catalog is now displayed on the *Catalogs* page. 

<Image title="New Catalog Displays" alt="You are navigated back to Catalogs page where you can see the newly-uploaded catalog" align="center" border={true} src="https://files.readme.io/9f81181-New_Catalog_Displays.png">
  New catalog displays on the Catalogs page
</Image>

> 🚧 Key Points to Consider
>
> * The catalog file must be in a CSV format.
>
> * You can add a maximum of 20 columns in a catalog.
>
> * **Product Catalog**
>   * You can upload a maximum of five catalogs.
>   * Each catalog can have up to five million rows.
>
> * **Product Location Catalog**
>   * You can upload a maximum of five catalogs.
>   * Each catalog can have up to one million rows.
>
> * You can upload the catalog with columns having accent marks and emojis, but you cannot view these characters at the time of catalog send-time personalization or downloading the catalog.

# Map Catalog Columns

After uploading the catalog, you must map the catalog column with the associated event and property on CleverTap (for example, map the *Name* field of the catalog to the event property *Product Name* of the event *Product Viewed*).

1. Navigate to *Settings* > *Catalogs* and select the uploaded catalog. 
2. From the map catalog section, select the catalog columns to map. 

The following is the sample mapping of the Product Location Catalog where the identity column from the catalog must be mapped to any other column in any product catalog:

<Image title="Select Product Location Catalog columns to map" alt="A prompt displays from where you need to click Map to map the columns of your uploaded Product Location Catalog" align="center" border={true} src="https://files.readme.io/ccbc79b-Select_Product_Location_Catalog_columns_to_map.png">
  Select Product Location Catalog columns to map
</Image>

> 📘 Required Location Column in a Product Catalog
>
> Include a location field in the product catalog to align with the identity column in the product location catalog, allowing for multiple mappings.

The following is the sample mapping for the Product Catalog:

<Image title="Select_Product_Catalog_columns_to_map" alt="A prompt displays from where you need to click Map to map the columns of your uploaded Product Catalog" align="center" border={true} src="https://files.readme.io/872cfac-Select_Product_Catalog_columns_to_map.png">
  Select Product Catalog columns to map
</Image>

> 📘 Key Points to Consider for Product Catalog
>
> * You can map multiple catalog columns to a CleverTap event property.
> * A mapped event property can only belong to the same event.

3. Click **Save Catalog** after the mapping is complete. 

> 📘 Catalog Column Mapping
>
> When mapping catalog columns, both user and event properties are always interpreted as String values, regardless of the provided data type.

# Catalog Best Practices

When uploading a catalog, consider the following best practices: some items are mandatory, and others are recommendations.

## Mandatory Practices

The following are some of the mandatory practices when working with Catalogs on the CleverTap dashboard:

* The first row in the file must contain the header fields separated by commas. The subsequent rows are fields with your individual catalog items in them, also separated by commas. Each row identifies one item in your catalog.

* There can be a total of 20 columns in your catalog. The following are some tangible benefits of adding a large number of custom fields when uploading your record:
  * Every field in the catalog can be used for sending personalized messages to your users. 
  * Also, every field could be used to create recommendations for a filtered set of items in your catalog. For example, you could have a field that identifies the things that are the *flavor of the season*. 
  * You could create a recommendation to serve only the *flavor of the season* from the catalog. You could also exclude items that are not best suited to be recommended to a wider audience (for example, rated content).

* The images added within the *ImageURL* field must adhere to the following guidelines to render correctly:
  * [Aspect Ratio for In-App Campaigns](https://docs.clevertap.com/docs/in-app-editor#guidelines-for-template-aspect-ratio-and-file-size).
  * Others: The aspect ratio of images must be 16: 9 or 1:1, depending on your campaign requirement.

## Recommended Practices

The following are recommended practices:

* You can add custom fields in addition to the mandatory fields. 
* It is highly recommended that you keep your catalog updated to ensure that:
  * The [recommendations](doc:recommendations) are accurate and useful to users. Also, it is important to avoid showing recommendations for items that have expired or are currently out of stock.
  * The [Catalog Data Ingestion](doc:catalog-data-ingestion) is accurate.
