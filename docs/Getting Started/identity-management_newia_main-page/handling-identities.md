---
title: Handling Identities
excerpt: Select the approach to manage Identities.
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

You can handle the identified profiles per your requirements on the CleverTap dashboard.\
Open the *User Identity* page from *Settings* > *Identity*.  

Answer the following questions based on your requirements:

* How do you want to identify logged-in users?
* How do you want CleverTap to handle identified profiles?
* Do you want to use ADID and IDFA as device identifiers?

# How do you want to identify logged-in users?

Select how to identify users. We recommend that you use the user email ID to identify users.

You can also use any of the other identifiers, such as [Mobile number] or [Identity]. 

![884](https://files.readme.io/25bc2e0-Identity_Identity_logged_in_Users.png "Identity_Identity logged in Users.png")

## How do you want CleverTap to handle identified profiles?

![932](https://files.readme.io/54af1bb-How_Do_You_Want_CleverTap_to_Handle_Identified_Profiles.png "How Do You Want CleverTap to Handle Identified Profiles.png")

## Do Not Merge Identifiers on the Same Sevice 

This method is recommended to set up identity management on CleverTap. This option invokes the `OnUserLogin` method. It ensures that even if multiple users perform the signup or login operation on the same device, their individual user data is stored on separate user profiles. 

This is the ideal and recommended scenario as it ensures the correct isolation of user data and helps in tracking events more efficiently. 

To configure this setting, perform the following steps:

1. From the dashboard, navigate to *Settings* > *User Identity*.
2. Under *How do you want CleverTap to handle identified profiles?* section, select *Do not merge identifiers on the same device*. 

### Allow Multiple Identities to Merge on the Same Device 

If your business only requires a singular profile to track all the multiple users logging in through the same device, then this method of user identity management can be used.

To implement this method, the `ProfilePush method` is used in invoked with any signup or login method. This ensures that even if multiple users perform the signup or login operation on the same device, their individual user data would be stored on the same user profile which was created using the first user’s operations.


This is not an ideal and recommended scenario as it restricts multiple individual users to have individual profiles. This type of use case should be implemented in scenarios such as a booking desk application registering all the users onto a singular desk profile. 

To configure this setting, perform the following steps:

1. From the dashboard, navigate to *Settings* > *User Identity*.
2. Under *How do you want CleverTap to handle identified profiles?*, select *Allow multiple identities to merge on the same device*. 

# Do You Want to Use AdID and IDFA as Device Identifiers?

The Advertising ID (AdID) is a unique, user-resettable ID for advertising provided by Google Play services. Similarly, Identifier for Advertisers (IDFA) is a unique code that Apple assigns to each iPhone for third parties to track users for ad targeting.

![766](https://files.readme.io/f1e3b52-Do_You_Want_to_Use_ADID_and_IDFA_as_Device_Identifiers.png "Do You Want to Use ADID and IDFA as Device Identifiers.png")

## Yes, I Will Use AdID and IDFA as Device Identifiers

Conforming to the latest privacy policies designed by Apple, the latest CleverTap iOS SDK does not capture IDFA or other device IDs, such as IMEI. The Identifier for Vendors (IDFV) is used to create a CleverTap ID which is disclosed under *Other Data*.

The Google AdID and IDFV can be captured by the CleverTap SDK during integration. 

The current GDPR policies do not allow using the Google AdID and the IDFA for tracking user data. So if your app conforms with the GDPR policies, it is not recommended to use the Google AdID or the IDFA as device identifiers.

If your use case and region are not governed by the GDPR policies, you can use the Google AdID to capture the user info.

When you use the Google Ad ID for creating a Clevertap ID/Profile, they display as: \_\_g&lt;google ad id without special characters&gt;. For iOS, this displays as: `-g<IDFA>`

## No, I Will Use a Custom Device Identifier

By default, the CleverTap Android SDK will not use the Google Ad ID to generate CleverTap IDs. In this case, you can set your own custom identifiers or let the CleverTap ID handle the ID creation to create user profiles.

If the app is required to be GDPR compliant or if you do not want to use the Google AdID, you can use the \_\_&lt;Random Alphanumeric String&gt; notation to generate the CleverTap ID. 

When creating the CleverTap ID using the custom identifier, the following format is:
* \_\_h&lt;unique id&gt; for Android. 
* -h&lt;unique id&gt; for iOS.

## I Want to Use IDFV

The Identifier for Vendors (IDFV) is a code assigned to all apps by one developer and is shared across all apps by that developer on your device. The IDFV value is the same for apps from the same developer running on the same iOS-enabled device. This displays as: -`v&lt;IDFV&gt;`

The CleverTap iOS SDK does not track IDFA. CleverTap’s iOS SDK uses IDFV to track anonymous users from SDK version 3.9 above.

You can use IDFV to collect data of users from CleverTap SDK versions 3.9 and above.