---
title: Import Existing Shopify Data into CleverTap
excerpt: Learn more about importing existing Shopify data into CleverTap.
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

CleverTap's Historical Data Import feature helps synchronize existing Shopify user and transaction data by allowing you to upload all your historical data directly to CleverTap.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/168b91fb5bc61e6b3694c0576351543a680b886f74698f3fa7735c18c968826a-historical_.png",
        "",
        "Historical Data Import"
      ],
      "align": "center",
      "border": true,
      "caption": "Historical Data Import"
    }
  ]
}
[/block]


You can upload the following types of data:

- **Profile Data**: Includes user information such as name, email, phone number, and so on. This is mapped as Profile Properties on the CleverTap dashboard. Refer to the [sample profile data file](https://docs.google.com/spreadsheets/d/11e16DkoSHT_zeYgaa2E_hJjHVO9U4VSzoR4nXb_xXAY/edit?usp=sharing).
- **Purchase Data**: Includes transaction data such as order data. This is mapped as Charged Event on the CleverTap dashboard. Refer to the [sample purchase data file](https://docs.google.com/spreadsheets/d/1gyycrJlx6NgaftxJMJpKXig3mI8fYSTFz9Honp9Ltzs/edit?usp=sharing).

To upload your Shopify website data on CleverTap, follow the steps below:

1. Download a CSV file from your Shopify dashboard. This file can either be a **Profile CSV** with user data or a **Charged Event CSV**  with transaction data.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f64dcd8c88237e5388b979d14e2d5cb8bb93985d7261e40d43661766b6c9539b-Shopify_Admin_Panel.png",
        "",
        "Shopify Dashboard"
      ],
      "align": "center",
      "border": true,
      "caption": "Shopify Dashboard"
    }
  ]
}
[/block]


2. To upload the CSV file to CleverTap, go to _Settings_ > _Project_ and click **Shopify**.  
3. Select the upload option: **Profiles** or **Charged Events**. The system starts processing the uploaded file immediately.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9601297b3d90c605de105f3841df3c2bf91147152d447faacb905c89e6cb0e63-Historical_data_import.png",
        "",
        "Historical Data Import"
      ],
      "align": "center",
      "border": true,
      "caption": "Historical Data Import"
    }
  ]
}
[/block]


4. Track the status of your upload at any time. Statuses include:

- **Pending**: The file has been received and is waiting to be processed.
- **Processing**: The system is validating and ingesting the data.
- **Importing**: The data is actively being ingested and merged into your CleverTap project.
- **Merged**: All rows are processed and added to your CleverTap project.
- **Merged with Errors**: The file is processed and merged, but some rows contain issues. You can check the error details, fix the data, and re-upload the CSV.
- **Failed**: The upload has failed due to formatting or validation issues. 
- **Paused**: Processing has been paused manually, or there may be a system interruption.

5. After processing, you will receive an email with a CSV file attached only for rows that encountered errors. This file includes an additional column indicating the reason for failure. In case of errors, fix the failed rows and re-upload only the affected rows. Multiple uploads are supported if required.

Once your data is merged, you can create campaigns, run analytics, and fully utilize the CleverTap platform. Profiles and events can be found in your CleverTap dashboard for further engagement. 

> 📘 Note
> 
> - Events containing any error columns will be silently ignored and dropped.
> - Ensure every user record has at least one valid identity field. The value must be under **1024 characters**. If this condition is not met, the following error will occur: `Identity value cannot be null or set at least one of identity / fbId / gpId / objectId under 1024 chars to identify the user`. 
> - The maximum file size for historical backfill uploads is 5 GB.
> - The following four columns are mandatory for a Charged file upload:
>   - Name
>   - Email
>   - Id
>   - Phone
> - Profile and Purchase data must be uploaded as two separate files.
> - If your mobile number is used as an identity, always search it in the CSV using the full international format. For example: `+91XXXXXXXXXX`.