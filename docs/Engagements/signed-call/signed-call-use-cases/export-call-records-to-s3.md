---
title: Export Call Records to S3
excerpt: >-
  Learn how to export your Signed Call™ recorded voice files to your Amazon S3
  bucket.
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

CleverTap exports the Signed Call™ recorded voice files directly to your Amazon S3 bucket instead of storing them in the database.

> 📘 Signed Call Voice Files
> 
> - CleverTap exports the voice files in **.wav** format.
> - We recommend you create a fresh bucket of voice files for ease of access.

# Prerequisites

Ensure you integrate your S3 account on the CleverTap dashboard.  
To set up your S3 account, refer to [AWS S3 Export Guide](https://docs.clevertap.com/docs/aws-s3-export). 

> 📘 Signed Call S3 Configuration
> 
> Currently, Signed Call only supports S3 bucket configuration via Bucket Access Key and Secret key. S3 configuration through IAM is not currently supported, but it's in the pipeline and will be integrated soon.

After successful integration, click **Refresh** from the _Signed Call_ page to proceed with the export.

# Setup Signed Call Export with CleverTap

To set up the export of Signed Call voice files to your S3 bucket:

1. Navigate to _Settings_ > _Signed Call_ > _Integration_ from the CleverTap dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6321450-SC1.png",
        "Navigation to S3.png",
        736
      ],
      "align": "center",
      "sizing": "95% ",
      "border": true,
      "caption": "Amazon S3 Integration"
    }
  ]
}
[/block]


2. Turn the toggle **ON** to export recorded calls to the Amazon S3 bucket.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f644b3d-SC2.png",
        "",
        "Export Toggle "
      ],
      "align": "center",
      "sizing": "95% ",
      "border": true,
      "caption": "Export Toggle "
    }
  ]
}
[/block]


3. Select your _Amazon S3 Bucket_ from the dropdown and click **Confirm Your Bucket**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8413b73-SC3.png",
        "Confirm your bucket.png",
        660
      ],
      "align": "center",
      "sizing": "95% ",
      "border": true,
      "caption": "Amazon S3 Bucket "
    }
  ]
}
[/block]


4. Click **Confirm** to confirm your bucket selection.

> 🚧 Changing a Bucket
> 
> After you save a bucket, you can only change it by raising a request on [signedcall@clevertap.com](mailto:signedcall@clevertap.com)

> 📘 Stopping the Export
> 
> Turn the toggle **OFF** and click **Stop export** to stop the export.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ac96a65-SC4.png",
        "Stop export.png",
        813
      ],
      "align": "center",
      "border": true,
      "caption": "Stop Export"
    }
  ]
}
[/block]


CleverTap sends an alert to your registered email for any changes made to the dashboard settings.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1c28b7f-SC5.png",
        "Alert email.png",
        383
      ],
      "align": "center",
      "sizing": "450px",
      "border": true
    }
  ]
}
[/block]