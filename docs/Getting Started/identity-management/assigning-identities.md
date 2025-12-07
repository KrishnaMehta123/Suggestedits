---
title: Identify Users
excerpt: Understand how CleverTap attributes actions to users.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
When a user interacts with an app or website integrated with CleverTap, a [user profile](https://docs.clevertap.com/docs/user-profiles) is created with a unique CleverTap ID. Once the CleverTap ID is assigned, you can add more identifiers based on your implementation to identify individual users. CleverTap allows adding  [multiple types of identifiers](https://docs.clevertap.com/docs/identity-management-overview#types-of-identifiers) to uniquely identify a user profile. Let's explore different situations to identify unique users.

## Anonymous Users

Anonymous users have only a CleverTap ID on their profiles. Here are some scenarios illustrating the mapping of Device IDs, User IDs, and CleverTap IDs.

| Device        | CleverTap ID | User ID |
| :------------ | :----------- | :------ |
| iPhone        | 1            | null    |
| Desktop       | 2            | null    |
| Android phone | 3            | null    |

In the table, there are three unique users.

The first event was performed on an iPhone. Since this device had no previous record, CleverTap assigned it a new CleverTap ID of 1.

The second event came from a Desktop. Because there was no previous record of this device, CleverTap assigned it a new CleverTap ID of 2.

The third event came from an Android phone and was assigned a CleverTap ID 3.

Based on the devices, these are three different anonymous users. 

## Anonymous Users After Login

<br />

When a user logs in after an anonymous user on the same device, all the previous events are associated with the identified user.

Consider the table below where an identified user uses the device after an anonymous user:

| Device | CleverTap ID | User ID                                  |
| :----- | :----------- | :--------------------------------------- |
| iPhone | 4            | null                                     |
| iPhone | 4            | [smith@email.com](mailto:jane@email.com) |

After a user logs in, the profile with the CleverTap ID 4 is updated with an additional identifier, that is, the User ID [smith@email.com.](mailto:jane@email.com) Now, Mr. Smith is an identified user. All future events on this device will be mapped with our identified user, Mr. Smith, with the user ID [smith@email.com.](mailto:jane@email.com).

## Common User ID on Multiple Devices

The following image shows how user profiles are identified on multiple devices:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/81af898-image.png",
        null,
        "Common user on multiple devices - merging profiles"
      ],
      "align": "center",
      "border": true,
      "caption": "Profile merge after identification"
    }
  ]
}
[/block]


Refer to the table below to understand how CleverTap assigns IDs to users logging in to the app. 

| Devices     | CleverTap ID | User ID                                   |
| :---------- | :----------- | :---------------------------------------- |
| iPhone      | 8            | [smith@email.com](mailto:smith@email.com) |
| iPad        | 9            | null                                      |
| iPad+iPhone | 8+9          | [smith@email.com](mailto:smith@email.com) |

When a user installs the app on an iPhone, CleverTap creates a user profile and assigns it a CleverTap ID 8. At this point, the User ID is unavailable and, therefore, null. Once the user logs in, a User ID is assigned, such as [smith@email.com.](mailto:smith@email.com.) This action identifies the profile.

In another scenario, if Mr. Smith installs the same app on an iPad, Clevertap creates a new profile with a CleverTap ID of 9, and the User ID remains null. However, when Mr. Smith logs in to the iPad using his email ID [smith@email.com](mailto:smith@email.com), CleverTap recognizes that this user is already identified with CleverTap ID 8 on the iPhone. As a result, both the profiles are merged, resulting in a user profile with one User ID ([smith@email.com](mailto:smith@email.com)) and two CleverTap IDs (8 and 9).

## Multiple Users on the Same Device

If multiple users log in to the same device, they get the same CleverTap ID. As a result, CleverTap combines these user profiles. If you want to track these users separately, you must use the 'Onuserlogin' method. Let's take a closer look at how these users are identified and tracked.

| Device | CleverTap ID | User ID                                  |
| :----- | :----------- | :--------------------------------------- |
| iPad   | 6            | [bob@email.com](mailto:bob@email.com)    |
| iPad   | 6            | null                                     |
| iPad   | 7            | [smith@email.com](mailto:adam@email.com) |

Bob and Mr. Smith are friends who share the same iPad. They each have their own login credentials for an OTT app, making them unique users for CleverTap.

Bob was the first to login to the app and was assigned CleverTap ID 6. After using the app, Bob logged out from the iPad.

Then, Mr. Smith started using the iPad. Since it was unclear if a new user had started using the device, all the activities performed on the iPad were associated with Bob's profile as he was the last known user, identified by CleverTap ID 6.

Now, Mr. Smith logged into the app and started using the app. As soon as Mr. Smith logs in, the [OnUserLogin](https://developer.clevertap.com/docs/user-profiles-ios#create-a-user-profile-when-user-logs-in-on-user-login-method) method creates a separate CleverTap ID for Mr. Smith, that is CleverTap ID 7, with the identifier [smith@email.com.](mailto:smith@email.com.) All the events performed by Mr. Smith are mapped to the new profile, that is CleverTap ID 7. All the events performed before the login are mapped to the previous profile, that is, Bob (CleverTap ID 6).