---
title: Orphan Profiles_Delete
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
We can see that some users have events that are shown in the grey background.
This basically means that these users have done these events before they identified themselves( Identity being pushed to CleverTap). These events are called anonymous events. (As mentioned earlier, This related to Blacklisting events).
Allow me to explain how a user is identified in CleverTap. This is on account of the way data is stored for your account. It is stored across multiple databases (shards) for faster execution of queries and faster TAT.
The blacklisting of profiles seems to be affecting users who are already identified on CleverTap, i.e their identity already exists and then they log in from a new device.
Let me explain the concept of anonymous events in detail:
Let's assume the existing profile is on Database 1. i.e., the earlier existing profile with the given identity.
Now, the user is attempting to log in again on a new device. In this case, since the device is new and the user is still anonymous we create an anonymous profile (given the number of databases, the probability that this user is on a different database is high). The database number is decided on the basis of our internal algorithm wrt the CleverTap ID of the device.
Once the user login to the new device, the profile is then updated with the identity, and since the identity already exists on the account - we merge the profiles.
In such a scenario - all anonymous events performed by this user when he was anonymous on device 2 then the events are blacklisted.
As the new profile is present on a different database the profile is blacklisted but is given in the Find People or the events dashboard when we try to execute the query.


Data types supported for events:

CleverTap supports only primitive java data types (String, Integer, Float, Boolean, List, Mixed), so if you are using a list/array etc, that instance will be dropped (the properties where the data type is incorrect)

Charged is a special event, where the data can be passed in an array.

---------------------

#Overview

A good retention strategy needs to identify unique accurately measures and analyze engagement. Identifying unique users may require some work on the part of the campaign manager.  Your users may choose to log in and out, browse anonymously, or use multiple devices. All these events can happen in isolation or in combination. 

CleverTap uses a combination of Device IDs, User IDs, and CleverTap IDs (CT IDs) to track unique users. 

# Identify Users

CleverTap uses a system of three different IDs to track users: Device ID, User ID, and CleverTap ID.

* Device ID: It can be either the IDFV or a random alphanumeric string for the device ID. This string is stored locally in the browser's cookie or the mobile device. For web-based applications, CleverTap generates a random UUID. It will stay unless a user clears their browser cookies and/ or is browsing in private mode. 

* User ID: You can configure this user profile identifier.  Most apps use a phone number or email address to track their users. A user ID must be unique and permanent. If somewhere down the line if the User ID changes for a user , then the user is regarded as another user. 

Do not assign a user ID to anonymous users. These users can be merged later with their identified profiles. 

To set a user ID, use the onUserLogin method described in our SDK documentation.
Amplitude ID: After gathering the device and user IDs, Amplitude generates the Amplitude ID and associates it with the user and device IDs it has already collected for this user. Amplitude only needs one or the other to generate an Amplitude ID; however, the user ID is preferred, as multiple unique users could share the same device.

This section explains in detail how Amplitude generates an Amplitude ID in different scenarios.




 analytics need Tracking users can require some work.  

What are Orphan Profiles
Identification IDs

How are Orphan Profiles Created
OnUser Login Method
Profile Push Method
Merge User Profiles