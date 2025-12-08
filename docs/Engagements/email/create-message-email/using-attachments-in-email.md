---
title: Using Attachments in Email
excerpt: >-
  Learn how to attach one or more files as part of the CleverTap email
  campaigns.
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

CleverTap allows you to attach files directly to your email campaigns and journeys. This helps marketers share downloadable content such as brochures, onboarding kits, and so on without redirecting users to external URLs.

Here are some of the common cases:

* **Onboarding Kits**: Include welcome guides or product setup PDFs for new users.
* **Policy or Legal Documents**: Share terms and conditions, compliance forms, or updated policy documents.
* **Event Resources**: Send event passes, itineraries, and so on.
* **Customer Support**: Share product manuals, troubleshooting guides, or return forms.
* **Educational Resources**: Deliver course materials, certificates, or lesson plans to learners.

> 📘 Private Beta
>
> The Email Attachments feature is currently released in Private Beta. The feature is currently available for **SendGrid** and **Infobip** (with Advanced Email Add-on) providers. For early access, contact Customer Success Manager.

# Supported File Types and Limits

CleverTap supports uploading images and PDFs using flexible upload methods to help you include documents or media in your emails. Before uploading attachments, make sure your files meet the supported format and size limits outlined below:

<Table>
  <thead>
    <tr>
      <th>
        Attribute
      </th>

      <th>
        Value
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Supported file extensions
      </td>

      <td>
        `.pdf`, `.doc`, `.docx`, .`ics`, `.jpg`, `.png`, and `.jpeg`
      </td>
    </tr>

    <tr>
      <td>
        Max number of files
      </td>

      <td>
        Up to 10 attachments per email
      </td>
    </tr>

    <tr>
      <td>
        Max file size
      </td>

      <td>
        * 2 MB per PDF
        * 2MB per document
        * 1 MB per image
      </td>
    </tr>
  </tbody>
</Table>

# Add Attachments to Email

You can add attachments to your email directly from the **Content Manager**, **What** section of the campaign builder, or **Email engagement node** of the journey builder.

From the campaign creation setup, select **Attachments** from the _What_ section, select one of the following options, and click **Attach**:

* **File URL**: Paste a publicly accessible HTTPS URL pointing to the file. Also, provide a friendly display name for the file, such as `Monthly Report.pdf`.  After uploading, you can rename the file by hovering over the uploaded attachment and clicking the ![](https://files.readme.io/42a29cd4fe23c9ab89b9e3f19c62f7896517787823c9b86827530e2ee9266a0b-Rename_icon.png) icon. The display name provided here (for example, _Monthly Report.pdf_) is visible to the end user in their inbox. Attachments are **not stored in CMS automatically** when uploaded via this option.

  <Image align="center" alt="Attach Files via Files URL" border={true} caption="Attach Files via Files URL" src="https://files.readme.io/73237a564349e698f1717dfecff2fdfb8ee7bee27d6e3fdc32b8bfd1f7c8557f-Attach_FIles_via_URL.gif" />
* **Device Storage**: Click to open your file browser and select the file you want to upload. Attachments are **not stored in CMS automatically** when uploaded via this option.  

  <br />

  <Image align="center" alt="Attach Files via Device Storage" border={true} caption="Attach Files via Device Storage" src="https://files.readme.io/fb71219a6004ddb399ce79bd6582106269af7a31314eecf4058e6b18294083ab-Attach_File_via_Device_Storage.gif" />
* **Content Manager**: Click **Browse** to attach previously uploaded assets to the email campaign.  


  The attached files, along with their file names and types, are displayed in the _Preview_ section on the right. The files are validated for size, extension, and name during this time. You can **rename** a file uploaded by clicking the ![](https://files.readme.io/b79e2947976e8baefc1fba973c0a391d91528b5b933eb4e3a4eb7190ed62be37-Rename_icon.png) icon next to the file name and entering a display-friendly name. The display name provided here is visible to the end user in their inbox. You can remove any file by clicking the ![](https://files.readme.io/77cb7f4c433c6442788e32e4d6ec56906e305942d35b0c7c5e7f9f4a4c8949ad-70a339a-delete_all_icon.jpg) icon next to the uploaded file.

<Callout icon="📘" theme="info">
  **Max Overall Email Size**

  To avoid message delivery failure, ensure the total email size, including attachments, stays within the limits set by your Email Service Provider (ESP):

  * SendGrid: 30MB
  * Infobip: 24MB

  You can validate by sending a test campaign to your internal audience before publishing the campaign.
</Callout>

Once you have attached your files, add all the _Sender Details_. If you add CC/BCC recipients under _Sender Details_, they receive the same attachments as the primary recipient.

> 📘 Private Beta
>
> Adding CC/BCC recipients to email campaign is currently in Private Beta. For more information, refer to [CC/BCC](doc:create-message-email#ccbcc).

# Errors

If an error occurs due to an issue with the attached file while sending the campaign, the email is not delivered. A soft bounce is recorded and listed under the _Errors_ tab on the campaign _Stats_ page. However, the **recipient is not unsubscribed** from future emails. Additionally, the **Notification Failed** event is also triggered for the user, with the event property _Error_ set to _Attachment errors_.

<Image align="center" alt="Email Attachment Errors" border={true} caption="Email Attachment Errors" src="https://files.readme.io/6fb0e04c57b85a2861be36ee9cc5313fff2dbfc31d29c506d71a566ca296e227-Email_Attachment_Errors_Stats.png" />
