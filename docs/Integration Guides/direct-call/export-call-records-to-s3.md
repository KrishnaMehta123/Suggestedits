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

> 📘 Direct Call Voice Files
>
> * CleverTap exports the voice files in .wav format.
> * We recommend you create a fresh bucket of voice files for ease of access.

# Prerequisites

If you have not already integrated your S3 account on the CleverTap dashboard, the **Integrate S3 account** hyperlink displays just below the *API Key* and *Account ID*.\
For more information, refer to [AWS S3 Export Guide](https://docs.clevertap.com/docs/aws-s3-export). After the integration is successful, click **Refresh** from the *VoIP* page to proceed further with the export.

# Getting Started

To export the Direct Call voice files to your S3 bucket:

1. Navigate to *Settings* > *Direct Call* > *Integration* from the CleverTap dashboard.

<Image title="Navigation to S3.png" alt={736} className="border" border={true} src="https://files.readme.io/813c92f-Navigation_to_S3.png" />

<Image title="Integrate S3 account.png" alt={813} className="border" border={true} src="https://files.readme.io/1340d3a-Integrate_S3_account.png" />

2. Turn the toggle **ON** to export recorded calls to the Amazon S3 bucket.

<Image title="Turn On.png" alt={661} className="border" border={true} src="https://files.readme.io/bfa962b-Turn_On.png" />

3. Select your *Amazon S3 Bucket* from the dropdown and click **Confirm Your Bucket**.

<Image title="Confirm your bucket.png" alt={660} className="border" border={true} src="https://files.readme.io/a3b0f91-Confirm_your_bucket.png" />

4. Click **Confirm** to confirm your bucket selection.

<Image title="Confirm S3.png" alt={657} className="border" border={true} src="https://files.readme.io/8d49eb3-Confirm_S3.png" />

> 🚧 Changing a Bucket
>
> After you save a bucket, you can only change it by reaching out to your contact person at CleverTap.

Turn the toggle OFF and click **Stop export** to stop the export. 

<Image title="Stop export.png" alt={813} className="border" border={true} src="https://files.readme.io/f59b449-Stop_export.png" />

CleverTap sends an alert to your registered email for every setting change made on the dashboard.

<Image title="Alert email.png" alt={383} className="border" border={true} src="https://files.readme.io/383aaf1-Alert_email.png" />
