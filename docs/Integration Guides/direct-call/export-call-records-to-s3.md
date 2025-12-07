---
title: Export Call Records to S3 Bucket
excerpt: Export your Direct Call recorded voice files to your Amazon S3 bucket
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
# Overview
CleverTap exports the Direct Call voice files directly to your Amazon S3 bucket instead of storing them in the database.
[block:callout]
{
  "type": "info",
  "body": "* CleverTap exports the voice files in .wav format.\n* We recommend you create a fresh bucket of voice files for ease of access.",
  "title": "Direct Call Voice Files"
}
[/block]
# Prerequisites
If you have not already integrated your S3 account on the CleverTap dashboard, the **Integrate S3 account** hyperlink displays just below the *API Key* and *Account ID*.  
For more information, refer to [AWS S3 Export Guide](https://docs.clevertap.com/docs/aws-s3-export). After the integration is successful, click **Refresh** from the *VoIP* page to proceed further with the export.

# Getting Started
To export the Direct Call voice files to your S3 bucket:

1. Navigate to *Settings* > *Direct Call* > *Integration* from the CleverTap dashboard.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/813c92f-Navigation_to_S3.png",
        "Navigation to S3.png",
        736,
        431,
        "#e9ebf1"
      ],
      "border": true
    }
  ]
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1340d3a-Integrate_S3_account.png",
        "Integrate S3 account.png",
        813,
        498,
        "#e9e9ef"
      ],
      "border": true
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
        "https://files.readme.io/bfa962b-Turn_On.png",
        "Turn On.png",
        661,
        166,
        "#f9f9fb"
      ],
      "border": true
    }
  ]
}
[/block]
3. Select your *Amazon S3 Bucket* from the dropdown and click **Confirm Your Bucket**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a3b0f91-Confirm_your_bucket.png",
        "Confirm your bucket.png",
        660,
        316,
        "#f8f9fc"
      ],
      "border": true
    }
  ]
}
[/block]
4. Click **Confirm** to confirm your bucket selection.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8d49eb3-Confirm_S3.png",
        "Confirm S3.png",
        657,
        322,
        "#767779"
      ],
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "warning",
  "title": "Changing a Bucket",
  "body": "After you save a bucket, you can only change it by reaching out to your contact person at CleverTap."
}
[/block]
Turn the toggle OFF and click **Stop export** to stop the export. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f59b449-Stop_export.png",
        "Stop export.png",
        813,
        455,
        "#68686b"
      ],
      "border": true
    }
  ]
}
[/block]
CleverTap sends an alert to your registered email for every setting change made on the dashboard.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/383aaf1-Alert_email.png",
        "Alert email.png",
        383,
        331,
        "#e5e6e8"
      ],
      "border": true
    }
  ]
}
[/block]