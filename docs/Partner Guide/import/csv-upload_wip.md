---
title: CSV Upload_WIP
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
With the CSV upload feature, you can create new [user profiles](doc:user-profiles) in CleverTap in bulk by uploading a CSV file with a list of user profiles. You can also use this feature to add or update information for existing user profiles.

> 📘 CSV Upload Permissions
>
> Only [Admins, Creators, and Approvers](doc:managing-dashboard-access) can use the CSV upload feature.

# Upload a CSV File

To upload a CSV file to the CleverTap dashboard: 

1. Log in to your CleverTap account and click *Settings* > *Engage* > *CSV uploads*.
2. Click **Import new profiles from CSV**.

<Image title="Click Import.png" alt={1198} className="border" border={true} src="https://files.readme.io/4851bca-Click_Import.png" />

3. Select the CSV file from your computer, preview it, and click **Upload**.

<Image title="Preview CSV.png" alt={816} className="border" border={true} src="https://files.readme.io/453c793-Preview_CSV.png" />

4. Enter the *CSV import name* and click **Upload**. 

<Image title="CSV_Upload_Sample_file_preview_Name.png" alt={962} className="border" border={true} src="https://files.readme.io/a4dc642-CSV_Upload_Sample_file_preview_Name.png" />

The CSV upload is processed in near real-time. After the CSV upload is done processing, the status for that upload changes to *Completed*.

<Image title="CSV_Upload_Main_Final.png" alt={1198} className="border" border={true} src="https://files.readme.io/88b4bae-CSV_Upload_Main_Final.png" />

# Key Points to Remember

## CSV Upload Details

* If a new user profile is uploaded, a new user profile is created on the account.
* If an existing user profile is uploaded, the old user profile is updated with new values.
* If a new user profile property is added, a property is created on the user profile.
* You can upload multiple CSV files simultaneously, even when existing files are currently processing.
* Customers can preview up to 15 rows of the file before uploading.
* The phone number must have only digits. For example, 01 123 111 0123. It must not contain any string values.
* After the upload is completed, the following information for the upload is displayed: 
  * Name: Displays the CSV import name.
  * Uploaded on: Displays the date on which the CSV file was uploaded. 
  * Uploaded by: Displays the email ID of the person who uploaded the file.
  * Status of upload: Displays the status of CSV File upload. The following are the two possible statuses of the upload: In Progress and Completed.
  * No. of Errors: Displays the count of rows that were not uploaded due to an error.
  * No. of Records: Displays the count of records that were uploaded successfully. 

## CSV File Format

* To view the expected CSV format, download the [sample CSV file](https://s3-eu-west-1.amazonaws.com/eu1-dashboard-uploads3bucket-j4m0n5829hvh/csv-upload/sample-upload-csv.csv).
* The upload will not be allowed if the file is not a CSV file or does not comply with CSV standards.
* [identity](doc:user-profiles) is a mandatory column in the CSV. However, if you want to make profile updates using the CleverTap ID, you can use the `objectId` in place of identity.

> 🚧 Note
>
> * Ensure that the `identity` key is always in lower case.
> * You can upload a CSV with a file size of up to 50MB.

The following is the sample format for the CSV file using `objectId`:

<Image title="CSV File with ObjectID.png" alt={1587} className="border" border={true} src="https://files.readme.io/bcf5586-CSV_File_with_ObjectID.png" />

The following is the sample format for the CSV file using `identity`:

<Image title="sample_upload_CSV.png" alt={1510} className="border" border={true} src="https://files.readme.io/2e166c6-sample_upload_CSV.png" />

## Date Format

* CleverTap supports uploading date information in the following formats: 
  * dd/MM/yyyy HH:mm:ss
  * MM/dd/yyyy HH:mm:ss
  * yyyy/dd/MM HH:mm:ss
  * yyyy/MM/dd HH:mm:ss
  * dd MMM yyyy HH:mm:ss
  * Unix time\
    All other formats will be treated as a String.

* Time defaults to 12:00:00 if hh:mm:ss is not added.

* 24-hour date format is supported.

* If you are uploading a date, the header must mention the name of the property followed by the date format in angular brackets. Ensure to use the exact case as the format is case-sensitive. 

> 👍 Date Format Example
>
> A purchase date example: \<dd/MM/yyyy HH:mm:ss>.
