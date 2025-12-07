---
title: Identifying Users
excerpt: >-
  Understand how user profiles are created in the CleverTap dashboard and how
  different identifiers are used to identify the users
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
#Overview

CleverTap uses the following parameters to identify any user uniquely:
* CleverTap ID
* Identity
* Email ID
* Phone Number

For more information about these parameters, refer to [Types of Identifiers](https://docs.clevertap.com/docs/identity-management_newia_wip#types-of-identifiers).

All the user activities are tracked against the `CleverTap ID` until a user signs up or logs in. On signup or login, the identity is passed from your application/website to CleverTap. This identity can be an email, a mobile phone number, or any other unique identifier. A mapping between the CleverTap ID and this identity ensures that the registered user's profile is merged with that of the user's anonymous profile. This merged profile is now called *Addressable Profile*.

For more information about different CleverTap user profiles, refer to [User Profiles](doc:user-profiles).


#  Profile Creation
There are different ways of creating a user profile on the CleverTap dashboard such as via an SDK, CSV Upload, and SFTP.  
## Profile Creation with SDK
This section provides information about creating a user profile via an SDK. 
The CleverTap SDK must be integrated to create a user profile on the CleverTap dashboard.
After integrating the SDK, the platform creates a user profile for each person who launches the application or visits the website. 

The following figure shows the workflow of user profile creation in the CleverTap dashboard.

Need a better workflow here. <<@sunil to get from marketing>>
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e3c8842-image4.png",
        "image4.png",
        1999,
        691,
        "#f0f1f1"
      ]
    }
  ]
}
[/block]
The above figure shows that the SDK gets initialized when the user launches the application after integrating the CleverTap SDK. 

The anonymous user profile is created with `CleverTap ID` in the following way: 

**For Android Users**
  * If the app is not GDPR compliant, an anonymous user profile is created with the Google Ad ID as the CleverTap ID. The `CleverTap ID` displays as `__g<google ad id>`. 
  * If the app is GDPR compliant, an anonymous user profile is created with `__<Random Alphanumeric String>` as the `CleverTap ID`.
 * You also have the option to [set up a custom CleverTap ID](https://developer.clevertap.com/docs/set-clevertap-id). An anonymous user profile is created with `__h<unique id>` as the CleverTap ID.

**For iOS Users** 
  * If the app is not GDPR compliant, an anonymous user profile is created with IDFA. The `CleverTap ID` displays as `-g<IDFA>`.
  * If the app is GDPR compliant, an anonymous user profile is created with `-v<App Vendor ID>` as the `CleverTap ID`.
* You also have the option to set up a custom `CleverTap ID`. An anonymous user profile is created with `-h<unique id>` as the `CleverTap ID`.

## Profile Creation with Other Modes

You can also create profiles using
  * [SFTP](https://developer.clevertap.com/docs/imports-via-sftp) - Use SFTP to import data including profile data.
  * [Data Import tool](https://developer.clevertap.com/docs/data-imports) - Import profile data from various sources including third parties.
  * [APIs](https://developer.clevertap.com/docs/user-profile-object) - Import profile data using APIs.


# Best Practices to Choose User Identity
Depending on your business, the best practice is to identify your logged-in users by using a primary key that you already use in your database as an `Identity` on CleverTap.
[block:callout]
{
  "type": "success",
  "body": "Each business may want to choose a different primary key as a unique identity, such as:\n* An over-the-top (OTT) platform can use an email\n* A payment gateway can use a phone number",
  "title": "Common Use Case Examples with a Primary Key"
}
[/block]
Creating an internal user ID is also a recommended best practice. A good way to implement identity creation on login is to embed the `onUserLogin` method provided by the CleverTap SDK. For more information, refer to [Maintaining Multiple User Profiles on the Same Device](https://developer.clevertap.com/docs/concepts-user-profiles#section-maintaining-multiple-user-profiles-on-the-same-device).