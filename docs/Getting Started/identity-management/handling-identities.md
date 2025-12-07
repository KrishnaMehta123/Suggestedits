---
title: Configure Identities
excerpt: Understand how to select the best approach to manage Identities.
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

You control how to identify and track your users. The CleverTap dashboard helps you set up the user profile identification based on your requirements. To configure user profiles from the dashboard, go to Settings > User Identity. The User Identity page appears.

Clarity on the approach to identifying and tracking the profiles is a prerequisite. Before you start, check that you have the following information:

* Decide on a method to identify users who are logged in.
* Determine how CleverTap should handle the identified profiles.
* Decide on using ADID or IDFA as device identifiers.

 Having this information beforehand will help you decide how to manage your users' identities.

# Identify logged-in users

The system automatically assigns a device-level ID (CleverTap ID) to logged-in users.  Using additional identifiers for logged-in users can help identify the users better and unify user data from different sessions. If a user logs into multiple devices, CleverTap maps all these devices and the relevant data to the same identity. To identify logged-in users, you can use the following identifier options from the dashboard:

* Email ID
* Mobile number
* Identity

For more information on types of identifiers, refer to [Types of Identifiers](https://staging.docs.user.clevertap.net/docs/identity-management-overview#types-of-identifiers).

<Image title="Identity_Identity logged in Users.png" alt={884} align="center" border={true} src="https://files.readme.io/25bc2e0-Identity_Identity_logged_in_Users.png" /> Identify Logged-in Users











> 📘 Preferred Identifer
>
> We recommend selecting the Email ID to identify users.

# Declare Identification Method

You have the option to customize your app's behavior for managing identified users by using the identifying methods provided by CleverTap. With these methods, you can set up your app to merge multiple identifiers upon login or create unique identifiers for the user. We recommend that you do not merge identifiers on the same device. 

<Image title="How Do You Want CleverTap to Handle Identified Profiles.png" alt="Select Identity Method" align="center" border={true} src="https://files.readme.io/54af1bb-How_Do_You_Want_CleverTap_to_Handle_Identified_Profiles.png" /> Select Identity Method











## Do Not Merge Identifiers on the Same Device
We recommend this approach for setting up identity management in CleverTap to avoid merging multiple users on the same device.  By selecting this option, you indicate to CleverTap that even if different users sign up or log in to the same device, CleverTap must store their user data on separate profiles. 

This method is ideal for scenarios where different users may log in to a single device, such as multiple users on the same OTT platform. It helps categorize user data more accurately and efficiently attribute user actions.

To declare the method, perform the following steps from the CleverTap dashboard:

1. Go to *Settings* > *User Identity* .
2. Under the *How do you want CleverTap to handle identified profiles?* section, select *Do not merge identifiers on the same device*.

## Allowing Multiple Identities to Merge on the Same Device

We *do not* recommend this approach for setting up identity management in CleverTap. By selecting this option, you indicate to CleverTap that you wish to store all user data under the original user profile, regardless of how many users use the device. Some businesses utilize this feature to consolidate data from multiple users.

If you have enabled the `ProfilePush` method,  select the "Allow multiple identities to merge on the same device" option. Verify that you have indeed used the `ProfilePush` method during the SDK integration. This method should only be used if your business requires tracking all users who log in through a single device under a single profile.

To declare the method, perform the following steps from the CleverTap dashboard:

1. From the dashboard, navigate to *Settings* > *User Identity*.
2. Under the section *How do you want CleverTap to handle identified profiles?*, select  *Allow multiple identities to merge on the same device*.

# Declare Device Identifiers

Google Play services provide a unique, user-defined ID for advertising, known as the Advertising ID (ADID). Similarly, Apple assigns a unique code to each iPhone, called the Identifier for Advertisers (IDFA), which allows third parties to track users for ad targeting. You must inform CleverTap whether you will be using ADID, IDFA, or a custom device identifier.

<Image title="Do You Want to Use ADID and IDFA as Device Identifiers.png" alt="Use Device Identifiers" align="center" border={true} src="https://files.readme.io/f1e3b52-Do_You_Want_to_Use_ADID_and_IDFA_as_Device_Identifiers.png" />  Use Device Identifiers
## Use ADID and IDFA as Device Identifiers

The CleverTap SDK can capture the Google Ad ID (GAID) and IDFV if defined during integration. However, due to current GDPR policies, using GAID and IDFA to track user data is prohibited. If your app needs to comply with GDPR policies, it's not recommended to use GAID or IDFA as device identifiers.

If GDPR policies do not govern your use case and region, you may use GAID to gather user information. When using GAID to create a CleverTap ID or Profile, it will appear as "\_\_g&lt;google ad id without special characters&gt;" on the CleverTap dashboard. For iOS, if you use a GAID, the CleverTap ID displays as "-g&lt;IDFA&gt;" on the dashboard.

To comply with Apple's latest privacy policies, the newest version of the CleverTap iOS SDK no longer collects IDFA or other device IDs such as IMEI. Instead, starting from SDK version 3.9, it uses IDFV to track anonymous users. Apple provides a distinct alphanumeric label for all apps created by the same publisher or vendor, known as the Identifier for Vendors (IDFV). For example, suppose a user downloads four apps from the same vendor on a single device. In that case, the IDFV is the same for all four apps and is accessible to the app publisher or vendor. The CleverTap ID based on the IDFV is shown under *Other Data* and displayed in the format *-v&lt;IDFV&gt;* on the CleverTap dashboard.

## Use a Custom Device Identifier

By default, the CleverTap Android SDK does not use the Google Ad ID to generate CleverTap IDs. In this case, you can set your custom identifiers or allow CleverTap ID to handle the ID creation for user profiles.

If the app is required to be GDPR compliant or you do not want to use the Google AdID, you can use the "\_\_&lt;Random Alphanumeric String&gt;" notation to generate the CleverTap ID. 

When creating the CleverTap ID using the custom identifier, the format is the following: 

* "\_\_h&lt;unique id&gt;" for Android
* "-h&lt;unique id&gt;" for iOS

For more information on using a custom device identifier, refer to [Set CleverTap ID](https://developer.clevertap.com/docs/set-clevertap-id#section-rules-for-setting-the-clever-tap-id)).