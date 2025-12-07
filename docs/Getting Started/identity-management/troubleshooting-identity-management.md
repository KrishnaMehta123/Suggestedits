---
title: Troubleshooting Identity Management - WIP
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Overview

This section will help you with troubleshooting identity management issues.

# Identity Lifecycle \<\<@harsh, do we need to mention this ?>>

\-- Identity Set\
Dropped History (true,false)\
ID ( value of identity )\
Source ( SDK, API)\
Type ( New User, Merged, Appended )\
\-- Identity Error\
ID ( value of identity )\
Source ( SDK, API)\
\-- Identity Reset\
ID ( value of identity )\
Source ( SDK, API)

# Identity Protection \<\<@harsh, do we need to mention this ?>>

![774](https://files.readme.io/ea711dc-Identity_Protection.png "Identity Protection.png")

# How to Validate Identity Management

![956](https://files.readme.io/748f314-1_audit.png "1 audit.png")

## Marketer Audit

If you don't have access to the tools, you can simply leverage the CleverTap dashboard to perform the same\
validation. Confirm with your tech team the identity that is being pushed to CleverTap on Login/Registration.\
It can be your database identity or an email address.\
Simply login/register into the app. Now using the identity/email you can search for the user profile in the CleverTap dashboard to validate the events/user properties being pushed.

![687](https://files.readme.io/035da46-5_Marketer_Audit1.png "5 Marketer Audit1.png")

It will load the User Profile.

![812](https://files.readme.io/9d98815-5_Marketer_Audit2.png "5 Marketer Audit2.png")

# Developer Audit

This will require a developer audit for Android & iOS and then a test from the CleverTap dashboard.

## Android

Add the following code snippet to your Application/Delegate class :

* Android - `CleverTapAPI.setDebugLevel(1277182231)`

### Android Debug Log

For Android, the logs will be visible in the Android Studio Logcat.\
After you run the application with the code snippet, the Logcat window of Android Studio will allow you to see all the events trigger in real-time.

![749](https://files.readme.io/0748f90-2_android1.png "2 android1.png")

To find the same profile in the CleverTap dashboard, you can simply fetch the "g"(CleverTap ID) value available in logs. Enter this CleverTap ID in the CleverTap dashboard under *Segment* > *Find People*.

![728](https://files.readme.io/b9dd683-2_android2.png "2 android2.png")

## iOS

Add the following code snippet to your Application/Delegate class:

* iOS - `CleverTap.setDebugLevel(1277182231)`

### iOS Debug Area Logs

![679](https://files.readme.io/31e10d3-3_iOS_Debug_Area_Logs.png "3 iOS Debug Area Logs.png")

## Audit from CT Dashboard

Go to Segments -> Find People and search for the ‘g’ value to find your Profile page.

![847](https://files.readme.io/8695c97-4_Steps_in_CT_Dashboard1.png "4 Steps in CT Dashboard1.png")

This will redirect you to a CleverTap profile wherein you will find the events and user properties

![620](https://files.readme.io/712fe9d-4_Steps_in_CT_Dashboard2.png "4 Steps in CT Dashboard2.png")
