---
title: Identification Methods
excerpt: >-
  Understand how multiple user profiles are maintained and how the user profile
  properties can be updated in the CleverTap dashboard
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
[block:api-header]
{
  "title": "Overview"
}
[/block]
CleverTap automatically creates a user profile for every person visiting your website or using the application. At first, the user profile starts as anonymous and becomes addressable when the user logs in for the first time. However, there are scenarios where multiple users log in from the same device. In this case, the challenge is to track and attribute user activities against the correct user profile. In addition to this, there are scenarios where you want to add more user properties to the identified profiles.

CleverTap uses the following two methods to enrich user profiles: 
  * [OnUserLogin](doc:enrich-user-profiles#onuserlogin)
  * [ProfilePush](doc:enrich-user-profiles#profilepush)	

#OnUserLogin
Always ask your app developer to ensure that the `OnUserLogin` method is active on the application SDK. `OnUserLogin` is a CleverTap method to differentiate multiple users on the same device, such as the user's name or email. When a new user logs in to your app from the same device, the `OnUserLogin` method ensures that the new user is tracked separately.
[block:callout]
{
  "type": "success",
  "body": "Consider a scenario where user A logs in from a single device and then logs out of the device. Now, user B logs on to the same device. Here, `OnUserLogin` helps you to track events performed by the users A and B separately.",
  "title": "Different Users on Same Device Example"
}
[/block]
##When do I Use OnUserLogin?
When creating an account or logging into your application, you must use `OnUserLogin` if you want to maintain a separate profile for each user that logs on to the device. `OnUserLogin` switches between identified app users on the same device and track them. 

For more information, refer to [Maintaining Multiple User Profiles on the Same Device] (https://developer.clevertap.com/docs/concepts-user-profiles#section-maintaining-multiple-user-profiles-on-the-same-device) and [Web SDK Quick Start Guide - Identify Users](https://developer.clevertap.com/docs/web-quickstart-guide#section-identify-users).

##Example
The following example shows an onboarding app screen from which different users could log in or register using their user ID or Facebook IDs.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/aac1cdd-onuserlogin_example.png",
        "onuserlogin example.png",
        374,
        553,
        "#c8c3c6"
      ],
      "border": true
    }
  ]
}
[/block]
#ProfilePush
ProfilePush is the CleverTap method of updating the user properties. It is used to push the user information to CleverTap. For instance, when you want to update the user information from silver to gold status.
[block:callout]
{
  "type": "success",
  "title": "User Information Update Example",
  "body": "Consider a scenario where user A upgrades the subscription from a free account to a paid version. Here, ProfilePush helps to update the subscription status in the user property."
}
[/block]

## When do I use ProfilePush?
Ask your developers to activate the `ProfilePush` method only when you want to update user profiles. Whenever you want to update users' information, you should use `ProfilePush` to add more user properties to the identified profiles. 

For more information, refer to [Maintaining Multiple User Profiles on the Same Device] (https://developer.clevertap.com/docs/concepts-user-profiles#section-maintaining-multiple-user-profiles-on-the-same-device).

[block:callout]
{
  "type": "warning",
  "title": "Do not use Profile Push",
  "body": "The `OnUserLogin` method can handle the unique profile creation (Email ID) effectively and automatically. Do not use the ProfilePush method to update a user's unique identity on CleverTap."
}
[/block]
##Example
The following is an example showing an app screen from which users can update their accounts. <@harsh need a better screen here>
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8429278-65b954f-profilepush_example_-_revised.png",
        "65b954f-profilepush_example - revised.png",
        314,
        535,
        "#eaeaea"
      ]
    }
  ]
}
[/block]
For more information about profile creation, refer to [Identity Generation](doc:identity-generation_newia_wip).