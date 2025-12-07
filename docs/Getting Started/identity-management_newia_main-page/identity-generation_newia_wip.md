---
title: Identity Generation_NewIA_WIP_NOT required
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
## Overview

This section covers how our identity generation flows work with Android and iOS taking into account whether the identity generation needs to be GDPR compliant or not.

# Android

The following explains the different Android scenarios when generating an identity with Android.&#x9;

## GDPR

When the user identity needs to be GDPR compliant, we create a random CleverTap ID (CTID), such as: `__<Random Alphanumeric String>`

The following shows the identity generation flow:

1. User installs the app.
2. User launches the app.
3. Check if your customer needs to be GDPR compliant.
4. If they must be GDPR compliant, a random number is generated as a CTID.
5. User registers or logs in.
6. If it is the same user, then an identity is created. `OnUserLogin` is applied.
7. If the user logs out, they are redirected to the login page.
8. If the user uninstalls the app, they are redirected to the app install page.

![502](https://files.readme.io/52ccce5-Android_GDPR_Compliant_Flow.png "Android (GDPR Compliant Flow).png")

## Non-GDPR

When the user identity does not need to be GDPR compliant, use Google Ad ID to create an ID. The following is an example: `__g<google ad id>`

The following shows the identity generation flow:

1. User installs the app.
2. User launches the app.
3. Check if your customer needs to be GDPR compliant.
4. If they do not need to be GDPR compliant, Google Ad ID is appended with a ‘\_\_g’ prefix.
5. User registers or logs in.
6. If it is a new user, then a random number is generated as a CTID.
7. The identity is set.
8. If the user logs out, they are redirected to the login page.

![483](https://files.readme.io/a3bc97f-Android_Non-GDPR_Compliant.png "Android (Non-GDPR Compliant).png")

## Custom CleverTap ID

Customers can set their own CleverTap ID which looks like: `__h<your unique id i.e ABC>`

> 📘 SET Custom ID Consideration
>
> In SET Custom ID, ct\_id remains constant throughout the digital life of the profile. 
>
> If the customer cannot recall the ct\_id from their server for the user, then a new ct\_id will be assigned and a new profile will be created on CleverTap.

# iOS&#x9;

The following explains the different iOS scenarios when generating an identity with iOS.&#x9;

## GDPR

When the user identity needs to be GDPR compliant, we create a CTID on the basis of an identifier for vendor (IDFV) or a random CTID depending on the scenarios. 

For IDFV, it looks like this: `-v<alphanumeric value>` and for a random CTID, it looks like -1234.

The following shows the identity generation flow:

1. User installs the app.
2. User launches the app.
3. Check if your customer needs to be GDPR compliant.
4. If they must be GDPR compliant, a CTID using IDFV gets generated with the prefix ‘-v’.
5. User registers or logs in.
6. If it is the same user, then an identity is created. OnUserLogin is applied. If it is a new user, then a random number is generated as a CTID.
7. If the user logs out, they are redirected to the login page.
8. If the user uninstalls the app, they are redirected to the app install page.

![518](https://files.readme.io/fd6e14d-iOS_GDPR_Compliant.png "iOS (GDPR Compliant).png")

## Non-GDPR

When the user identity does not need to be GDPR compliant, we create a CTID on the basis of an identifier for advertising (IDFA) which looks like: `-g<IDFA/IDFV>`

The following shows the identity generation flow:

1. User installs the app.
2. User launches the app.
3. An anonymous profile with a CTID ‘-g’ gets generated.
4. User 1 logs in using the OnUserLogin method.
5. User 1 gets a CTID as ‘-gxxxx’.
6. Events start getting pushed to user 1's CleverTap account.
7. User 1 logs out.
8. User 2 logs in using the OnUserLogin method.
9. Is the email address the same? It is verified using cache.
10. If the email address is the same, all the events are recorded in the CTID of User 1. If the email address is different, user 2 gets a CTID as ‘-vxxx’.
11. Events start getting pushed to user 2's CleverTap account.
12. User 2 logs out.
13. User 3 logs in using the OnUserLogin method. 
14. Is the email address the same? It is verified using cache.
15. If it is the same, it will check with which user it matches with between 1 or 2.  
16. If the email address is different, user 3 gets a CTID as ‘-xxx’.
17. Events start getting pushed to user 3's CleverTap account.
18. User 3 logs out.
19. User 4 logs in using the OnUserLogin method. 
20. Is the email address the same? It is verified using cache.
21. If it is the same, it will check with which user it matches with between 1, 2, or 3.  
22. If the email address is different, user 4 gets a CTID as ‘-xxx’.
23. User 4 uninstalls the app and gets redirected to the app install page.

![658](https://files.readme.io/65b76f3-iOS_Non-GDPR_Compliant.png "iOS (Non-GDPR Compliant).png")

## Custom CleverTap ID

Customers can set their own CleverTap ID which looks like: `-h<your unique id i.e ABC>`

# Recommendation

It is recommended to use the OnUserLogin method whenever the users sign up or log in to your app. At any log-in possibility, the OnUserLogin works.

Contrary to that, ProfilePush works the best when you want to update the user properties of a logged-in user.
