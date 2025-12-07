---
title: Partner Vouchers (COPY)
excerpt: >-
  Learn how Partner Vouchers simplify voucher management for enabling seamless
  promotions and user rewards.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

Businesses often collaborate with brand partners to offer incentives, such as discounts or exclusive offers, to drive user engagement, increase retention, and boost conversions. The Partner Vouchers reward module allows you to upload, manage, and distribute vouchers received from your partners to your app or website users.

Vouchers can be uploaded for a partner along with their metadata, such as code name, description, and expiry date. (@Bajrang: are these the only details uploaded??) The Uploaded vouchers can then be mapped to a Promo Campaign to distribute a unique voucher to your users based on the intended actions defined in the Campaign.

When a user receives a voucher, the Promo engine triggers an event called *CT Partner Voucher Rewarded* with its event metadata. Based on this event, you can create a live-action engagement campaign, and the event metadata can be used to send a personalized message using Liquid tags to the user upon receiving the reward.

# Features

The following are the features of Partner Vouchers:

* **Voucher List Management**: Upload, manage, and distribute voucher codes.
* **Status Tracking**: Track the current state of voucher lists (Active, Expired, Paused, Archived).
* **Campaign Mapping**: Map uploaded voucher lists to one or multiple campaigns and track the campaign linkage in the voucher list page. \{@Krishna: Can we rephrase this as, "Map voucher lists to one or multiple Promo Campaigns. Each campaign can define specific conditions for voucher distribution. You can also track which campaigns are linked to a voucher list directly from the voucher list page."?}
* **Voucher Utilization Tracking**: Track the number of codes issued against the total number of codes uploaded for each voucher list.
* **Top-up Codes**: Top up the voucher list with a new set of codes when used codes exceed a threshold limit.

# Voucher Workflow

A business using CleverTap partners with various brands to offer discount vouchers as part of its promotional campaigns. The business receives vouchers from these partnered brands, uploads them to the CleverTap platform, and then distributes them to eligible users based on predefined campaign conditions. Customers who meet the campaign criteria receive a unique voucher code and redeem it on the partnered brand platform.

Alternatively, if the business has an internal coupon engine to manage voucher redemption directly, it can upload internally generated vouchers to CleverTap for distribution. In this case, customers redeem the vouchers on the business's platform instead of an external partner's.

This setup ensures seamless voucher management, whether sourced externally from partners or internally from the business systems.

# Voucher Distribution: Key Participants

Voucher distribution and redemption involve multiple participants, each playing a crucial role. The following table outlines each participant and their role in the voucher distribution and redemption workflow:

| Participants                      | Responsibility                                                                                                                                                                                                                                 |
| --------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Business (CleverTap Customer)** | Defines campaign eligibility criteria and distributes voucher codes through CleverTap. If partnering with brands, the business receives voucher codes from them. If using an internal coupon engine, it manages voucher redemption internally. |
| **Brand Partners**                | Supplies voucher codes to a business for distribution, if applicable. Customers redeem these vouchers on the brand platform.                                                                                                                   |
| **CleverTap**                     | Enables businesses to upload, manage, and distribute vouchers through the Partner Vouchers feature. It ensures vouchers are assigned to eligible users based on campaign conditions and tracks their usage.                                    |
| **Customer (End User)**           | Performs the required campaign actions to earn a voucher, then redeems it either on the partnered brand’s platform (if applicable) or the business’s platform if it manages redemptions internally.                                            |

# Access Vouchers List

View and manage all your voucher lists in one place. The *Voucher Lists* page provides key details about each list, helping you track their status, usage, and associated campaigns. To access the *Voucher Lists* page:

1. Go to *Promotions* from the CleverTap dashboard.
2. Click **Rewards** and select **Partner Vouchers** from the dropdown menu.

<Image alt="Voucher Lists" align="center" border={true} src="https://files.readme.io/b55c1ccbffd44f05f9ab7a67f24171c5aa6097fff121e15eba98d013160fed01-Voucher_Lists_Page.png">
  Voucher Lists
</Image>

The **Voucher Lists** page provides a comprehensive overview of all voucher lists with the following columns:

<Table>
  <thead>
    <tr>
      <th>
        **Column Name**
      </th>

      <th>
        **Description**
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **List ID**
      </td>

      <td>
        A unique identifier for each voucher list. Click the ID to view detailed information about the list.
      </td>
    </tr>

    <tr>
      <td>
        **Partner**
      </td>

      <td>
        Displays the name of the voucher provider associated with the list.
      </td>
    </tr>

    <tr>
      <td>
        **List Tag**
      </td>

      <td>
        A unique identifier representing the voucher codes within the list. List Tag is used along with Provider Name to generate a unique List ID.
      </td>
    </tr>

    <tr>
      <td>
        **Updated On**
      </td>

      <td>
        The date and time of the most recent modification.
      </td>
    </tr>

    <tr>
      <td>
        **Status**
      </td>

      <td>
        <p>Indicates the current state of the voucher list. The following are the statuses:</p><ul><li>Active (Green)</li><li>Expired (Red)</li><li>Paused (Orange)</li><li>Archived (Gray)</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        **Linked Promo Campaigns**
      </td>

      <td>
        The number of campaigns using this voucher list.
      </td>
    </tr>

    <tr>
      <td>
        **Codes Uploaded**
      </td>

      <td>
        The total number of voucher codes uploaded.
      </td>
    </tr>

    <tr>
      <td>
        **Codes Distributed**
      </td>

      <td>
        The number of voucher codes issued to users.
      </td>
    </tr>
  </tbody>
</Table>

## Voucher List Status and Actions

A voucher list status determines its availability and the actions you can perform. Managing these statuses ensures smooth integration and organization of vouchers in promotional campaigns.  

The table below outlines each voucher list status, its description, and the actions you can perform:  

| Status       | Description                                                              | Allowed Actions                       |
| ------------ | ------------------------------------------------------------------------ | ------------------------------------- |
| **Active**   | Voucher list is available for use in promotional campaigns.              | Pause, Edit, Upload Codes, Archive    |
| **Paused**   | Voucher list is temporarily inactive, and campaigns cannot use codes.    | Activate, Edit, Upload Codes, Archive |
| **Expired**  | Voucher list has passed its expiration date and cannot be used.          | Edit, Archive                         |
| **Archived** | Voucher list is permanently deactivated and retained for record-keeping. | No further actions allowed            |

### Managing Voucher Lists

To update a voucher list, click the ![](https://files.readme.io/bb833f57ad2428831fdc23f4a1bf488039206ddbf9bdd8083d13148e887e17cf-Ellipsis_Promo.png) icon next to the list. The available options depend on the current status of the list.  

| Action           | Effect                                                            |
| ---------------- | ----------------------------------------------------------------- |
| **Pause**        | Temporarily disables an active voucher list.                      |
| **Upload Codes** | Adds more voucher codes to an existing list.                      |
| **Edit**         | Modifies details such as list name, description, and expiry date. |
| **Activate**     | Reactivates a paused voucher list.                                |
| **Archive**      | Permanently deactivates a list, preventing further modifications. |

## Uploads

Once a voucher file is uploaded, the system processes and validates the codes and records the upload logs against each voucher list. The *Upload* tab logs details of uploaded voucher files, helping you track and manage the upload process. 

To view the upload history of a voucher file, click the **List ID** of the desired voucher list, then click the *Uploads* tab.

<Image alt="View Uploads" align="center" border={true} src="https://files.readme.io/b5be60febe7a6c8d3a4e898129653f3b4b8fdfb32e9f0104cee692872fe7fa7f-Uploads_History_Tab.gif">
  View Uploads
</Image>

Each entry has the following fields:

<Table>
  <thead>
    <tr>
      <th>
        Column Name
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Timestamp**
      </td>

      <td>
        The date and time when the voucher file was uploaded.
      </td>
    </tr>

    <tr>
      <td>
        **Status**
      </td>

      <td>
        <p>Indicates the current state of the upload process. The possible statuses are:</p><ul><li>**Completed**: The upload was successful, and all valid voucher codes have been processed.</li><li>**In Progress**: The system is still processing the uploaded file.</li><li>**Failed**: The upload encountered errors, and no codes were processed.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        **Uploaded By**
      </td>

      <td>
        Displays the email ID of the user who uploaded the voucher file.
      </td>
    </tr>

    <tr>
      <td>
        **File Name**
      </td>

      <td>
        Name of the uploaded file.
      </td>
    </tr>

    <tr>
      <td>
        **Codes (Uploaded/Total)**
      </td>

      <td>
        Number of voucher codes successfully uploaded compared to the total codes in the file.
      </td>
    </tr>

    <tr>
      <td>
        **Errors**
      </td>

      <td>
        Displays any issues encountered during upload, such as duplicate codes or an invalid file format. It also indicates the total number of errors found in the uploaded file.
      </td>
    </tr>
  </tbody>
</Table>

You can download the uploaded voucher file from the *Uploads* page for reference or troubleshooting.

<Image alt="Download Uploaded Vouchers File" align="center" border={true} src="https://files.readme.io/705175fec85decd3d94309734cc68c0a717eaf9c758cc1fd7740efa60a77a34b-Download_Voucher_File.png">
  Download Uploaded Vouchers File
</Image>

### Upload Errors

If an error occurs during upload, for example, duplicate codes or invalid format, download the *Error File* from the *Uploads* tab. This file contains error codes and corresponding error messages. Correct the errors and re-upload the corrected file using the *Upload Codes* flow against the same voucher list.

> 📘 Upload Codes
>
> If your voucher list is running low on codes, you can add more voucher codes without creating a new list. The *Upload Codes* option let's you do this which ensures uninterrupted voucher distribution in your campaigns.
>
> * You can upload additional voucher codes to an existing voucher list at any time.  
> * The system validates the new codes to prevent duplicates within the same list.  
> * The newly added codes are available for distribution once the upload is complete.

# Upload New Vouchers

You can create a voucher list to upload new voucher codes to CleverTap. To upload new vouchers, follow these steps:

1. Go to *Promotions* from the CleverTap dashboard.
2. Click **Rewards** and select **Partner Vouchers** from the dropdown menu.
3. Click the **New Voucher List** button in the top-right corner.
4. Add the following details:
   1. **Partner**: Enter the name of the voucher provider. The partner name helps categorize and track voucher sources. If the Partner is not listed, click **Add New** to create a new entry.
      1. **Accepted format**: Any value you enter is accepted. However, the system enforces case sensitivity and does not allow duplicate partner names. For example, `clevertap` and `CLEVERTAP` are treated as separate partners in Promo.
   2. **List Tag**: Define a short identifier for the codes. The List Tag uniquely identifies the uploaded voucher list within CleverTap.
      1. **Accepted format**: It must be unique within a given Partner. The system stores its value in lowercase. Special characters are permitted, but spaces are not allowed.
   3. **List Name**: This is the name of the voucher list used for communication campaigns. It does not describe individual voucher codes but serves as an identifier for the list.
   4. **List Description**: This field defines the usage conditions of the voucher codes uploaded in a voucher list.
   5. **Files**: Upload a CSV file containing the voucher codes. Ensure the file follows the guidelines:
      1. The file format must be .CSV
      2. Each row must contain a unique voucher code.
      3. Maximum file size must not exceed 50MB.
      4. Add voucher codes in a single column without comma-separated values. If multiple columns are added, the system rejects the file.
   6. **List Expiry**: Set an expiration date for the voucher list. Once the date expires, CleverTap stops distributing vouchers from this list. However, you can still extend the expiration date if needed. 
5. Click **Save**.

<Image alt="Voucher List Setup" align="center" border={true} src="https://files.readme.io/200d13a916693d097cdb3fd7a5667fbdc20fd3a39dcf3f2ea25c957b3e082209-Create_Voucher_List.png">
  Voucher List Setup
</Image>

# Duplicate Code Rules

the TheCleverTap system enforces strict duplicate checks while uploading voucher codes to ensure data integrity. The duplicate check logic is based on the combination of *List Tag* and *Partner* across all *Active* voucher lists (lists that are not archived).

The following are the rules to check the duplication of codes:

* A voucher code cannot be uploaded again within the same voucher list (with the same List Tag and Partner).
* A voucher code cannot be uploaded to another list if the same List Tag and Partner combination already contains that code in any active voucher list.
* A voucher code can be uploaded under the same List Tag but with a different Partner since redemptions occur on a separate platform.
* Once a voucher list is archived, its codes are no longer checked for duplication, allowing the same codes to be uploaded again.

## Example Scenarios

The following table illustrates different scenarios of voucher code duplication across lists. The **Available Codes** column represents the existing codes in active voucher lists, helping you verify duplication before uploading new codes.

| List Name | Partner   | List Tag              | Available Codes       | Codes Uploaded        | Duplication Allowed?                                |
| --------- | --------- | --------------------- | --------------------- | --------------------- | --------------------------------------------------- |
| List A    | Partner A | List Tag A            | -                     | `Code1, Code2, Code3` | Allowed (First-time upload)                         |
| List B    | Partner A | List Tag B            | `Code1, Code4, Code5` | `Code1, Code4, Code5` | Allowed (Different List Tag under the same Partner) |
| List C    | Partner B | List Tag A            | `Code1, Code2, Code3` | `Code1, Code2, Code3` | Allowed (Different Partner, different redemptions)  |
| List D    | Partner A | List Tag A            | `Code1, Code2, Code3` | `Code1, Code2, Code3` | Not Allowed (Same Partner and List Tag)             |
| List E    | Partner A | List Tag A (Archived) | `Code1, Code2, Code3` | `Code1, Code2, Code3` | Allowed because List A is archived                  |

## Managing Duplicate Voucher Codes Across Partners

Consider a scenario where Customer X runs a New Year sale campaign and collaborates with multiple partners to distribute discount vouchers. Each partner, such as Partner A and Partner B, operates independently, managing their own set of voucher codes.

Since each partner controls their own redemption platform, CleverTap enforces duplication checks within the same partner but allows the same code across different partners.

### Allowed Scenario

Referring to the example table, let's say Customer X uploads `Code1` under different partners:

* `Code1` is uploaded under **Partner A** (similar to List A).
* `Code1` is uploaded under **Partner B** (similar to List C).

This is allowed because Partner A and Partner B operate independently, ensuring no redemption conflicts.

### Not Allowed Scenario

Now, consider Customer X trying to upload `Code1` again under **Partner A**:

* `Code1` was already uploaded under Partner A (similar to List A).
* Customer X attempts to upload `Code1` again under Partner A in another active list (similar to List D).

This is not allowed because Partner A already has an active voucher list containing `Code1`. CleverTap blocks duplicate codes within the same partner across active lists to prevent duplication and ensure consistency.

However, if List A is archived, Customer X can re-upload `Code1` under a new list (similar to List E).

# Triggering Partner Voucher Rewarded Event

After a voucher is assigned to a user, CleverTap triggers the *Partner Voucher Rewarded* event, which includes key properties such as:

* `campaignID`
* `codeDescription`
* `codeProvider`
* `codeSnippetName`
* `source`
* `voucherCode`
* `voucherListID`

You can drive engagement by sending a communication campaign using the *Partner Voucher Rewarded* event. These properties can be leveraged in Liquid Tags to personalized messages, enabling dynamic content in push notifications, emails, or SMS.

## Engage with Voucher Assigned Users

To target users who have received a voucher:

1. Go to *Campaigns* from the CleverTap dashboard.
2. Click **+ Campaign** and select a messaging channel from the *Messaging Channels* dropdown.
3. Click **Add an event** from the *Who* section.
4. Select the *Partner Voucher Rewarded* event and the required *Event Property*.

<Image alt="Target Users with a Campaign/Journey" align="center" border={true} src="https://files.readme.io/caf5147da03def348122c8efcd3d085d43af1f932de05043eca578f1336702d9-image.png">
  Target Users with a Campaign/Journey
</Image>

To learn how to create a campaign, refer to [Create Message](doc:create-message-push#create-a-new-push-campaign).

# Best Practices

To ensure smooth voucher list management and avoid disruptions in campaigns, follow these best practices:

* **Upload Unique Voucher Codes**: Ensure that all voucher codes in a list are unique to prevent duplication errors and maintain accuracy.
* **Monitor Status Regularly**: Keep track of the voucher list status to ensure it remains active for ongoing campaigns.
* **Maintain Unique List Tag**: Use meaningful and distinct identifiers for better organization and easy reference.
* **Keep Codes Updated**: Regularly upload new voucher codes to prevent depletion and ensure continuous availability.

# Troubleshooting

You may encounter issues with voucher lists. In case you do, the following are some common problems and their solutions:

* **Unable to Activate Voucher List**: Check if the expiration date is in the future. You can not reactivate an expired voucher list without extending its validity.
* **Error Uploading Codes**:
  * Ensure the file format is *.CSV*.
  * Check that all voucher codes are correctly formatted and do not contain invalid characters.  
  * Verify that the file contains only one column with voucher codes and no comma-separated values.  
* **Missing Campaign Linkage**: If a voucher list is not linked to a campaign, review the campaign settings to ensure proper mapping.

# FAQs

Find answers to the following common questions about managing partner vouchers:

### What is the maximum number of codes I can upload to a voucher list?

You can upload up to one million codes per voucher list.

### Can I edit a voucher list after it is created?

Yes, you can update the List Name, List Description, and List Expiry.

### What happens if a voucher list expires?

Once expired, you can not use a voucher list in campaigns. However, you can still extend the expiry date.

### How can I track issued codes?

The *Codes Issued* column provides real-time data on the number of voucher codes distributed to users.

### Can I delete a voucher list linked to an active campaign?

No, a voucher list must be unlinked from all campaigns before it can be deleted.
