---
title: Assigning Identities
excerpt: Understand how CleverTap assigns Identities to users
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
We will explore some common scenarios that occur when identifying unique users.

## Unidentified User
If the user is not identified, a CleverTap ID is assigned when the user performs an action from a device for the first time. 

[block:parameters]
{
  "data": {
    "h-0": "Device ID",
    "h-1": "User ID",
    "h-2": "CleverTap ID",
    "0-0": "X",
    "0-1": "null",
    "0-2": "1",
    "1-0": "Y",
    "2-0": "Y",
    "3-0": "Z",
    "4-0": "X",
    "5-0": "Z",
    "1-1": "null",
    "2-1": "null",
    "3-1": "null",
    "4-1": "null",
    "5-1": "null",
    "1-2": "2",
    "2-2": "2",
    "3-2": "3",
    "4-2": "1",
    "5-2": "3"
  },
  "cols": 3,
  "rows": 6
}
[/block]
There are three unique users in this table.

Here, the first event was performed on device X. Because there was no previous record of this device, CleverTap assigned it a new CleverTap ID of 1.

The second event came from device Y. Because there was no previous record of this device,  CleverTap assigned it a new CleverTap ID of 2.

The third event also came from device Y, and because CleverTap already had a record of this device, it was assigned a CleverTap ID of 2. The same logic applies to device Z. 

## Identified User after anonymous events

For an identified user, CleverTap assumes that all previous events logged anonymously on that device belong to this identified user.

[block:parameters]
{
  "data": {
    "h-0": "Device ID",
    "h-1": "User ID",
    "h-2": "CleverTap ID",
    "0-0": "A",
    "1-0": "A",
    "2-0": "A",
    "0-1": "null",
    "0-2": "4",
    "1-1": "null",
    "1-2": "4",
    "2-1": "Jane",
    "2-2": "4"
  },
  "cols": 3,
  "rows": 3
}
[/block]
There is one unique user in this table.

The first two events are logged anonymously on device A and are assigned a CleverTap ID of 4. The third event is the first event received from device A that includes a logged-in user. CleverTap assigns this user the same CleverTap ID as the previous anonymous events. We can now assume that the identified user, Jane performed all three events. 

##  Common User ID on Multiple device IDs with no anonymous events

The device IDs have a lower priority than user IDs.
[block:parameters]
{
  "data": {
    "h-0": "Device ID",
    "h-1": "User ID",
    "h-2": "CleverTap ID",
    "0-0": "B",
    "1-0": "C",
    "0-1": "John",
    "0-2": "5",
    "1-1": "John",
    "1-2": "5"
  },
  "cols": 3,
  "rows": 2
}
[/block]

CleverTap assigned a CleverTap ID of 5 to a logged-in user *John*, who performed an event on device B. Thereafter, CleverTap assigns the same CleverTap ID of 5 to John whenever he logs into any device. 

## Multiple user IDs on the same device

If an event is performed from an identified device (a device with at least one user login), then CleverTap associates this event with the previously identified user. 
[block:parameters]
{
  "data": {
    "h-0": "Device ID",
    "h-1": "User ID",
    "h-2": "CleverTap ID",
    "0-0": "E",
    "1-0": "E",
    "2-0": "E",
    "3-0": "E",
    "4-0": "E",
    "0-1": "Bob",
    "2-1": "Adam",
    "1-1": "null",
    "3-1": "null",
    "4-1": "null",
    "0-2": "6",
    "1-2": "6",
    "2-2": "7",
    "3-2": "7",
    "4-2": "7"
  },
  "cols": 3,
  "rows": 5
}
[/block]
Bob and Adam are two unique users in this table. 

Bob performed the first event on the device and CleverTap assigned him a CleverTap ID of 6. Somebody performed another event anonymously from the same device. Bob may have logged out but the event was assigned to Bob because he was the last known user. 

Now a logged-in user Adam performs a third event from the same device. This event is assigned a CleverTap ID of 7 because Adam is a different user. 

The next two events are performed anonymously; CleverTap assigns them a CleverTap ID of 7. Because the last known user was Adam, the events are associated with Adam. 

To log out users and log events as anonymous, you must set the User ID to null and regenerate a new device ID. <<@harsh, is it actually OnuserLogin method? >>>


## Same user ID on multiple devices, with anonymous events

[block:parameters]
{
  "data": {
    "h-0": "Device ID",
    "h-1": "User ID",
    "h-2": "CleverTap ID",
    "0-0": "P",
    "1-0": "Q",
    "2-0": "Q",
    "3-0": "Q",
    "0-1": "Smith",
    "2-1": "Smith",
    "1-1": "null",
    "3-1": "null",
    "0-2": "8",
    "1-2": "9",
    "2-2": "8",
    "3-2": "8"
  },
  "cols": 3,
  "rows": 4
}
[/block]
In this example, Smith performs an event on device P and is assigned a CleverTap ID of 8.

Next, an anonymous user logs an event on device Q and is assigned a CleverTap ID of 9 because no user is associated with the device.

Then Smith logs on the application from the same device, that is, device Q. This event has a CleverTap ID of 8 because Smith was already assigned this ID.

Again, an event is logged anonymously on device Q. This event is assigned a CleverTap ID of 8 because the last known user was Smith on this device. 

The anonymous events on device Q have two different CleverTap IDs, even though there's only one user ID associated with the device. This means that both the CleverTap IDs 8 and 9 refer to the same user: Smith. CleverTap will automatically recognize and merge these IDs so that only one user is calculated. This merge can only occur because the event with CleverTap ID 9 does not have a User ID. <<<@harsh, does this cover our shard scenario? Is this our orphan profile ?>>

#Orphan profiles	
When identified users visit your app or website from another device or browser, CleverTap creates new profiles for these users. For example, once they identify with their identities on the app or website through login, CleverTap merges the newly created profile with the already present user profile, and all the events that were recorded on the new profile before the user identification are orphan profiles. 

For more information, refer to [Upload Past User Profiles](https://docs.clevertap.com/docs/upload-past-user-profiles#already-identified-user).

##Impact on Analytics and Campaigns
To avoid any impact on analytics and your campaigns, during integration, ensure that the identities are pushed to CleverTap as soon as they are available on the platform and leverage CleverTap IDs instead of *Identity*, if possible.