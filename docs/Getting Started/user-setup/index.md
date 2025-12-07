---
title: User Setup
excerpt: Understand how you can add and manage users from the CleverTap dashboard
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

The user needs an invitation and an appropriate access level to access the CleverTap dashboard. The account admin can perform different operations, such as adding a new user, assigning the role to a user, editing the user's current role, etc. from the *Settings* > *Users* page.

<Image title="Users page navigation.png" alt={1644} className="border" border={true} src="https://files.readme.io/f1e63cd-Users_page_navigation.png" />

After the new user is added, the dashboard allows an admin to view the following information about all the users added to the project: Name, Role, Email, User Status, Last Login, and Passcode-Status.

# Operations

The account admin can perform different user management operations from the CleverTap dashboard. Each of these operations is described briefly in the following sections.

## Add/Invite Users

To add/invite a new user to the CleverTap dashboard:

1. Navigate to *Settings* > *Users* from the CleverTap dashboard. 
2. Click **+ User**. On clicking, the *Invite users* window displays on the right side.
3. Enter the email address and assign the role. For more information about different roles in the CleverTap dashboard, refer to [Role-Based Access Control](doc:role-based-access-control).

<Image title="Invite a new user .png" alt={2374} className="border" border={true} src="https://files.readme.io/dffdeb2-Invite_a_new_user_.png" />

You can also invite multiple users at one time by clicking **+ User** from the *Invite User* window. You can invite a maximum of 50 users at one time.

![2374](https://files.readme.io/497da55-Invite_multiple_users_to_the_dashboard.png "Invite multiple users to the dashboard.png")

4. Click **Invite**. The message *X users successfully invited* displays if the invites are successfully sent to the users, where 'X' indicates the number of users you invited to the dashboard.\
   (@Saurav: After sending the invite, is the user immediately listed under the Users page?)

> 📘 Download Users List
>
> You can download the list of all the users by clicking **Download User** from the *Users* page.

## Edit a Role

You can also edit the role of the user in the future. To do so, click the ![Ellipses](https://files.readme.io/2717d2a-ellipses_icon.png) against the required user and select *Edit Role* from the list.

<Image title="Edit Role.png" alt={2372} className="border" border={true} src="https://files.readme.io/36add3c-Edit_Role.png" />

For more information about role management, refer to [Role-Based Access Control](doc:role-based-access-control_invite-user-update).

## Revoke Access

Revoking user access invalidates the existing passcode for the user, and the user can no longer make API calls using their passcode. To do so, click the ![Ellipses](https://files.readme.io/2717d2a-ellipses_icon.png) against the required user and select *Revoke access* from the list.

<Image title="revoke-access.png" alt={2372} className="border" border={true} src="https://files.readme.io/3b4881c-revoke-access.png" />

Click **Revoke** when prompted to confirm the action.

<Image title="Revoke access ?.png" alt={576} className="border" width="80%" border={true} src="https://files.readme.io/114faaa-Revoke_access_.png" />

## Reset Passcode

Reset Passcode generates a fresh new passcode for the user. Post resetting, the user must incorporate this passcode for the APIs. To do so, click the ![Ellipses](https://files.readme.io/2717d2a-ellipses_icon.png) icon against the required user and select *Reset passcode* from the list.

<Image title="reset-passcode.png" alt={2372} className="border" border={true} src="https://files.readme.io/a489c9d-reset-passcode.png" />

Click **Reset Passcode** when prompted to confirm your action.

<Image title="reset passcode?.png" alt={578} className="border" width="80%" border={true} src="https://files.readme.io/e6ad6f4-reset_passcode.png" />

## Grant User Passcode

Granting a user passcode helps authenticate the user when making API calls. To grant a passcode, click the ![Ellipsis](https://files.readme.io/2717d2a-ellipses_icon.png) icon against the required user and select *Grant passcode* from the list. 

<Image title="grant-passcode.png" alt={2372} className="border" border={true} src="https://files.readme.io/571a716-grant-passcode.png" />

Select the tenure for which you want to grant passcode and then click **Grant** to confirm your action.

<Image title="grant-passcode?.png" alt={726} className="border" width="80%" border={true} src="https://files.readme.io/8e5cc88-grant-passcode.png" />

For more information about API authentication in CleverTap, refer to [Authentication](https://developer.clevertap.com/docs/authentication).
