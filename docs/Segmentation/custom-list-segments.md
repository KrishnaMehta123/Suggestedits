---
title: Custom List Segments
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
  pages:
    - type: link
      title: Use an API to upload custom list segments
      url: https://developer.clevertap.com/docs/custom-list-endpoints
    - type: link
      title: Use Custom list as an entry point in Journeys
      url: https://docs.clevertap.com/docs/journeys#section-journey-components
---
# Introduction

Custom List Segments are custom segments that you can create based on your requirements and analytics. These can be users with the required interests, demographics, and so on. You can use these segments to re-engage your users without having to apply the same conditions or filters again. 

## Examples

A custom list segment can be handy in many scenarios. Typical use cases can be any of the following and more:

* A retail business running SMS campaigns:\
  As a retail business, you may be generating user lists at your point of sale across different cities. You can upload city-based segments and run personalized campaigns to re-engage these users. 

* Engagement integrated with your segmentation engine:\
  You may have a segmentation engine or a data science engine that has created a user set to engage with a specific message. In this case, you can use custom list segments to seamlessly create segments from your custom lists and schedule engagement for them. 

* Real-time sync for engagement with your in-house segments:\
  For example, an app streaming a football match can have millions of users. However, let us assume that the target audience is 10,000 users. The next match is even more interesting and you are expecting a surge in the number of users. You have a list of 15,000 users handy that you can use to run the campaign. You create a segment on this list and run a campaign immediately.  

# Create a Custom List Segment

You can create a custom list segment by uploading user lists via the dashboard or API. 

> 📘 File Size
>
> You can upload a maximum file size of 50 MB from the dashboard. The maximum file size allowed from an API upload is 5GB.

## File Format

Only CSV file format is supported for upload. Also, the list of the users for your segment must follow a specific format. You can upload the profiles with identity type as GUID or CleverTap ID (g) or the identity (i). 

The format of the CSV file is as follows:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Type
      </th>

      <th>
        Identity
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        g
      </td>

      <td>
        a1e2723cba7c4518bea8ef95b036ac83
      </td>
    </tr>

    <tr>
      <td>
        i
      </td>

      <td>
        identity
      </td>
    </tr>
  </tbody>
</Table>

The type and identity columns are mandatory for successfully uploading a custom list segment.  


> 🚧 User Profiles
>
> A Custom List Segment can only contain user profiles that are on the CleverTap dashboard. It does not create any new profiles or update the attributes for the existing user profiles.

## Create from Dashboard

1. Navigate to *Segments* > *Segments*. 
2. Click **+ Segment**. 
3. Click **Custom list segments**. 

<Image title="Custom List Segment.png" alt={2836} className="border" border={true} src="https://files.readme.io/83855ee-Custom_List_Segment.png" />

The **Create new** page is displayed.\
3\. Enter the *Segment name*.\
4\. Click **Browse** and select the CSV file to be uploaded.

<Image title="Create new page.png" alt={1714} className="border" border={true} src="https://files.readme.io/7791d47-Create_new_page.png" />

> 📘 Sample custom list CSV
>
> It is recommended to download the Sample custom list CSV file and format your custom list information as per the downloaded sample file.

4. Click **Save Segment**.\
   You will receive an email with the details after the file is processed. 

<Image title="Segments_Custom_list_email_successful.png" alt={1109} className="border" border={true} src="https://files.readme.io/772be36-Segments_Custom_list_email_successful.png" />

The uploaded segment is now available for use. 

## Create from API

You can create a custom list segment from API. For detailed steps, refer to [Custom list API](https://developer.clevertap.com/docs/custom-list-endpoints).

## Replace via Dashboard

You can replace a custom list segment from the dashboard. However, if the segment is currently in use for engagement through a Campaign or Journey, then you must stop the Campaign or Journey before replacing the segment. 

To replace a segment:

1. Click the ellipsis for segment action from the Segments dashboard. 

<Image title="Segments_Custom_lists_replace.png" alt={1222} className="border" border={true} src="https://files.readme.io/efc2bc5-Segments_Custom_lists_replace.png" />

2. Click the replace icon <img src="https://files.readme.io/f7a63da-icon_replace.png" height="30px" width="30px" />
3. Click the Re-upload user list and select the CSV file.  
4. Upload the CSV file.
5. Name the file and save it. Wait for it to be processed. 
6. You will receive an email with the details after the file is processed. 

The uploaded segment is now available for use. 

## Troubleshoot Upload

### **File size exceeds 50 MB**

This error occurs when the file size exceeds 50 MB.
<Image title="File size exceeds.png" alt={1552} className="border" border={true} src="https://files.readme.io/ad225fc-File_size_exceeds.png" />

If the file size is more than 50 MB, it can be uploaded via [Custom list API](https://developer.clevertap.com/docs/custom-list-endpoints).

### **Error uploading the file**

You can see the following message when trying to upload the file.

<Image title="File Upload error.png" alt={1107} className="border" border={true} src="https://files.readme.io/a043cdf-File_Upload_error.png" />

If the file is not uploaded correctly, you can upload it again. 

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Segment issue
      </th>

      <th>
        Resolution
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        File upload failed
      </td>

      <td>
        The segment could not be created from the uploaded file. Fix the errors and re-upload the file.
      </td>
    </tr>

    <tr>
      <td>
        File re-upload failed
      </td>

      <td>
        The segment could not be refreshed with the latest file. The segment will be available with the last successful update. Refer to the [View Segment Details](https://docs.clevertap.com/docs/custom-list-segments#section-segment-details) page for the last updated file.
      </td>
    </tr>
  </tbody>
</Table>

> 📘 Segment processing
>
> The custom list segment is available for use only after the process of creating or updating is complete.

## Segment details

The segment details can be viewed from the Segment dashboard. 

![1246](https://files.readme.io/736e185-Segments_Custom_lists_view_report.png "Segments_Custom_lists_view_report.png")

The segment details page shows all the available information for the segment such as:

* Trend - If the users have increased or decreased over time. 
* Campaigns and Journeys - The number of campaigns and Journeys currently using the custom list segment. 
* Segment size and reachability - The total number of users in the segment and their reachability across various engagement channels. 
* Sample Users - These are samples from your list. You can open any of them to check their details. 

> 📘 Tip
>
> Hover over sample users to find the <img src="https://files.readme.io/f28fc62-icon_download.png" height="30px" width="30px" /> download icon.\
> Click this button to download all the users in your segment.
<Image title="Segments_Custom_lists_report.png" alt={1193} className="border" border={true} src="https://files.readme.io/81840d5-Segments_Custom_lists_report.png" />

# Use Custom List Segment

You can use the custom list segment from the *Who* section when creating a campaign. All the custom list segments are listed under the Custom list segment tab. 

![1067](https://files.readme.io/f11a255-segments_custom_lists_WHO.png "segments_custom_lists_WHO.png")