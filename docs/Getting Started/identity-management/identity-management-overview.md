---
title: Identity Management Overview - WIP
excerpt: >-
  Understand the concept of identity, identity management, and its significance
  in CleverTap
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

A user profile in CleverTap provides a comprehensive overview of all user data, including demographics, location, actions, and engagements. When a user profile is created, it is assigned several attributes to identify or reference the user individually or in combination. CleverTap assigns each user with a unique ID to identify users even if they use multiple devices or the same device.

User identities are important for the following reasons:

* Mapping user activities and profile attributes to specific profiles.
* Targeting intended users through Campaigns or Journeys, user-level personalization, and recommendations.

# Types of Identifiers

CleverTap captures the following types of identifiers to identify users:

* CleverTap ID
* Identity 
* Email ID
* Phone Number

<Image alt="Sample Profile With Identifiers" align="center" border={true} src="https://files.readme.io/4c742cb-identity_management_sample_profile.jpg">
  Sample User Profile with Identifiers
</Image>

## CleverTap ID

CleverTap generates a device-level identifier called CleverTap ID (CT ID). You can have a common device identifier for the user across all systems without maintaining a mapping of the device ID. You can also create unique identifiers for end-user devices using a custom CleverTap ID. For more information about setting up a custom CleverTap ID, refer to [Set CleverTap ID](https://developer.clevertap.com/docs/set-clevertap-id#section-rules-for-setting-the-clever-tap-id).

> 📘 GDPR-compliant ID
>
> A GDPR-compliant ID is prefixed by **, For example,\_** g45sder2r\_. To know more about generating GDPR-compliant and non-GDPR complaint CTID, refer to [Create a User Profile](https://developer.clevertap.com/docs/sdk-changes-for-gdpr-compliance).

## Identity

Identity is an ID that you can define in your internal system (database) to uniquely identify users. CleverTap allows you to use any unique ID on your systems as an identifier on the CleverTap dashboard, such as `customerID`, `userID`, `registrationID`, `databaseID`, and so on. The selection of this unique ID in your database depends on the nature of the business. For example, a banking application can have its own unique ID for a user, such as *john1234*. 

## Email ID

In today's digital world, an email ID is a preferred way of identifying users. The email that is used as an identity must be unique. For example, customers can use an email ID as a unique identifier for subscription-based services such as online grocery or music streaming applications.

## Phone Number

Businesses can now use mobile phone numbers as a valid form of identity because of the accessibility of smartphones and the applications installed on them. Users can sign up for any product from their mobile application and have a great onboarding experience. 

For example, Fintech services use mobile phone numbers as a unique identifier for quicker login and signup.
