---
title: Advanced Identity Management
excerpt: Learn how CleverTap uniquely identifies user profiles in different scenarios
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
## Overview

After becoming familiar with the basics of identity management, this section provides information about uniquely identifying user profiles on the CleverTap dashboard in different scenarios.

# Merge a Profile \<\<@harsh is it required now that we already have [Assign Identities](doc:assign-identities) ? >>

CleverTap merges the profile when the same user logs in from different devices.

> 👍 Example: Multiple Devices, One User
>
> Consider the scenario where a user logs in to their favorite TV streaming app via their mobile phone in the morning and then logs in to the same app via the tablet in the evening. In this case, the profile gets merged.

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Device ID
      </th>

      <th>
        User ID
      </th>

      <th>
        CleverTap ID
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        A (TV)
      </td>

      <td>
        John
      </td>

      <td>
        1
      </td>
    </tr>

    <tr>
      <td>
        B (Tablet)
      </td>

      <td>
        John
      </td>

      <td>
        1
      </td>
    </tr>
  </tbody>
</Table>

Here, the device IDs have a lower priority than user IDs.

# Append a Profile [Assign Identities](doc:assign-identities)

CleverTap appends the profile when two different *identities* are pushed for the same CleverTap ID.

> 👍 Example: One Device, Multiple Users
>
> Consider a scenario where two different users log in to a food delivery app using the same device. To keep these users separate, the profile is appended.

For example, Bob performs the first event on the device and CleverTap assigns the CleverTap ID 6. An Anonymous user performs another event from the same device. Bob may have logged out but the event is assigned to Bob because he was the last known user. Now a new user Adam logs in and performs a third event from the same device. This event is assigned a CleverTap ID 7 because Adam is a different user. Again, an anonymous user performs the next two events. CleverTap assigns them a CleverTap ID 7 as the last known user was Adam. The events are associated with Adam.

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Device ID
      </th>

      <th>
        User ID
      </th>

      <th>
        CleverTap ID
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        E
      </td>

      <td>
        Bob
      </td>

      <td>
        6
      </td>
    </tr>

    <tr>
      <td>
        E
      </td>

      <td>
        null
      </td>

      <td>
        6
      </td>
    </tr>

    <tr>
      <td>
        E
      </td>

      <td>
        Adam
      </td>

      <td>
        7
      </td>
    </tr>

    <tr>
      <td>
        E
      </td>

      <td>
        null
      </td>

      <td>
        7
      </td>
    </tr>

    <tr>
      <td>
        E
      </td>

      <td>
        null
      </td>

      <td>
        7
      </td>
    </tr>
  </tbody>
</Table>

# Demerge Identities&#x9;

Demerging is the segregation of two different unique identities from one CleverTap ID, which can be done in two ways. Demerging happens when you have a bad merge profile. 

## Method 1: Reset Identities from the Dashboard

Identity reset is recommended when there is a need to demerge a badly merged profile.

Before the identity reset, note down all the CleverTap IDs and identities associated with the profile. Then, to reset an identity, perform the following steps:

### Reset Identities

1. From the dashboard, navigate to *Segments* > *Find People*.
2. Search your user by identity or scroll down and click on the appropriate profile once you have identified it.
3. Click **Reset Identities**.

This option contains a number associated with it indicating the number of identities associated with that profile.

\<\<@harsh, need a new screenshot here>>

![1999](https://files.readme.io/382378e-Reset_identities.png "Reset_identities.png")

Through this identity reset, you create separate user profiles for each of the CleverTap IDs (devices) and none of the profiles will have any email or identity associated with it. All the events from the merged profiles are also logged under the user profile with CleverTap ID (device) from which the events were logged.

Basically, this operation will create 10 separate profiles and none of them will have any of the identities (neither email, nor identity). All the identities will be reset or removed making these 10 profiles as the anonymous profiles.

For more information, refer to [Maintaining Multiple User Profiles on the Same Device](https://developer.clevertap.com/docs/concepts-user-profiles#section-maintaining-multiple-user-profiles-on-the-same-device).

### Merge Profiles by Uploading the Identity

Upload one of the identities, such as the profile email or identity to all these synonymous profiles using the API or CSV upload. This operation will merge these 10 profiles with the profile. This operation will merge the profiles and you can see all the events under the same profile.

For more details on how to upload a profile via API and CSV upload, refer to [Upload User Profiles API]\
([https://developer.clevertap.com/docs/upload-user-profiles-api](https://developer.clevertap.com/docs/upload-user-profiles-api)) and [CSV Upload](https://docs.clevertap.com/docs/csv-upload#notes) respectively.

## Method 2: Reset Identities using CleverTap Demerge API

Before using the demerge API, perform the following:

1. Ensure the onUserLogin is being used for login functions across all platforms.
2. Identify the profiles where the identity or email is not set.
3. Demerge these profiles in bulk using demerge API.

To reset an identity using the demerge API, use the following URL: [https://api.clevertap.com/1/demerge/profiles.json](https://api.clevertap.com/1/demerge/profiles.json)

Following is a sample payload:

`{
"identities": ["sahil.jugiani18@gmail.com","sahilnewid010@gmail.com","sahil2@gmail.com","sahil@clevertap.com"] }`

Identities object has to be a list. A maximum of 100 identities in one request is allowed.

> 📘 Process Notices
>
> The process only runs between 4 am to 7 am during the account's timezone. A request can take up to a day to process it. In the case of millions of requests, it can take a few days since the processing stops after 7 am.

Once the profile is demerged, all the device IDs associated with the profile will have their own profiles without any identities. Once the user logs in from the device, the identity will be assigned to the respective device ID and the data will start flowing as expected.

For more information, refer to [Demerge User Profile API](https://developer.clevertap.com/docs/demerge-user-profile-api).

# Delete a Profile (GDPR Mandate) &#x9;

When a customer wants to erase user data from the dashboard, they can use the delete API which takes about 48 hours to complete the profile deletion from the database. For more information, refer to [Delete User Profile API](https://developer.clevertap.com/docs/delete-user-profile-api).

Multiple reasons to delete the user profile, include:

* Bad merge
* Internal user
* Security or business reasons 

If the deleted user comes back again, we will treat them as a new user. 

For more information on GDRP, refer to [Right to Erase](https://docs.clevertap.com/docs/gdpr#right-to-erase).

# Identity Errors&#x9;

An identity error is a debug event that is raised when an existing identity is associated incorrectly with another identity. The former identity is now declared as invalid for the latter's profile. This event is raised during monitoring and debugging when identity merges are invalid.

For more information, refer to [Debug Events](https://docs.clevertap.com/docs/events#debug-events).

## Bad Merge

When two different identities that are supposed to be for two different profiles get associated with the single profile, we call it a bad merge.

When a bad merge happens, we raise an event called identity error into the user's profile. This event is typically raised when an existing identity is associated incorrectly with another identity. This may sometimes occur particularly in test cases and test profiles due to repeated uninstall/re-installs.

In the case of a profile push, if you try to push another identity for the same profile, in this case, the profile will be badly merged. An immediate solution would be to reset these profiles and begin testing on the devices again.

To avoid any kind of merge, we recommend that the `onUserLogin` function should be called on every login or sign-up. For more information, refer to [Maintaining Multiple User Profiles on the Same Device](https://developer.clevertap.com/docs/concepts-user-profiles#section-maintaining-multiple-user-profiles-on-the-same-device).

> 👍 Bad Merge Example
>
> User A has [abc@gmail.com](mailto:abc@gmail.com) and user B has [xyz@gmail.com.](mailto:xyz@gmail.com.) 
>
> If both users used the same device and their profiles on CleverTap were merged, it is known as a bad merge. All the events done by user A or user B would be considered in one single profile.

### Avoid Bad Merge

* Check that the mapping of users in the application is correct and the correct data is sent to CleverTap. 
* Maintain consistency in assigning a new identity.

## Ghost Profile \<\<@harsh, should we mention this is customer facing docs?>>

Currently, we allow every CleverTap profile to have a maximum of 50 devices (that is, 50 CleverTap IDs). 

Consider a user gets a 51st CleverTap ID and the client sends the same identity on the 51st device which was sent on the first 50. We will not merge the 51st ID into the parent profile (profile with 50 CTIDs) to avoid data corruption in the account because a user cannot have more than 50 devices. The 51st profile internally is called a ghost profile since we accept the profile/events but do not save the identity for the 51st profile.
