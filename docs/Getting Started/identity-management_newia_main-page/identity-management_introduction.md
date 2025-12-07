---
title: Identity Management Overview
excerpt: >-
  Understand the concept of identity, identity management, and its significance
  in CleverTap
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

All the user data is always stored against a user profile. When a user profile is created, several attributes are assigned to a profile to identify or reference the user uniquely. These attributes or a combination of more than one of these attributes, termed as primary key, can be used to identify the user uniquely.

# Identity Management

The CleverTap user profile stores all the events performed by the user in the application. CleverTap uses different identifiers to attribute these events and their properties to the user profile. To know more about events and properties, see [Events](doc:events). Identity management is defining your user information uniquely on the CleverTap dashboard by providing each user with a unique identifier.

By uniquely identifying users, marketing teams can maintain unique user profiles even if the user uses multiple devices or when multiple users use the same device.

## Maintain Identities

The following are some of the key points to maintain identities: 

* Maintain a holistic view of users and their activities on multiple devices.
* Maintain distinct user profiles for users who use the same device.
* Target intended users using Campaign/Journeys, user-level personalization, and recommendations.

# Types of Identifiers

The following types of identifiers are captured for user profiles on the CleverTap dashboard:

* CleverTap ID
* Identity
* Email ID
* Phone Number 

<Image title="User_Identity_Profile.png" alt={1989} className="border" border={true} src="https://files.readme.io/5eff36b-User_Identity_Profile.png" />

## CleverTap ID

CleverTap ID (CT ID) is a device level identifier.\
You can create your own unique identifiers for end-user devices using the custom CleverTap ID capability. For more information, refer to [Set CleverTap ID](https://developer.clevertap.com/docs/set-clevertap-id#section-rules-for-setting-the-clever-tap-id).

You can have a device identifier across all your systems without maintaining a mapping of the device ID across different systems. To know more about generating GDPR compliant and non-GDPR complaint CTID, refer to [Create a User Profile](https://docs.clevertap.com/suggested-edits/61fa3020837baa004af3da84?previewing=true#create-a-user-profile).\
A GDPR compliant ID will be prefixed by **, for example** g45sder2r.

## Identity\*\*

While users can update email and/or phone numbers on some apps or websites, there must be a unique identifier that always remains unchangeable. 

Identity is a unique ID that you define for your application to identify your user uniquely. The selection of the primary key depends on the nature of the business.

Using email or phone numbers is not useful if your app allows users to update their email or phone number.

Use *Identity* to identify the user uniquely. CleverTap provides the capability to use any unique ID on your systems as an identifier on the CleverTap dashboard. Some of the common examples are `customerID`, `userID`, `registrationID`, `databaseID`, and so on.

## Email ID

In today's digital world, an email ID is a preferred way of identifying users. The email must be unique to be set as an identity. For example, a user can use an email ID as a unique identifier for subscription-based services such as online grocery or music streaming applications.

## Phone number

Businesses can now use mobile phone numbers as a valid form of identity because of the accessibility of smartphones and the applications installed on them.  Users can sign up for any product on their mobile application and have a great onboarding experience. 

For example, fintech services use mobile phone numbers as a unique identifier for quicker login and signup.
