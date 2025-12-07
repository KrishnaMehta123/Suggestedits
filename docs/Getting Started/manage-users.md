---
title: Manage Users
excerpt: Understand how you can invite and manage users on the CleverTap dashboard
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

The user needs an invitation and an appropriate access level to access the CleverTap dashboard. The account admin can perform different operations, such as adding a new user, assigning the role to a user, editing the user's current role, etc. from the _Settings_ > _Users_ page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4d81f09-Users.png",
        "Users Page Navigation",
        "A dashboard image of User Settings page which gives an overview of added users and their access type"
      ],
      "align": "center",
      "sizing": "800px",
      "border": true,
      "caption": "User Settings"
    }
  ]
}
[/block]


After the new user is added, the dashboard allows an admin to view the following information about all the users added to the project: Name, Role, Email, User Status, Last Login, and Passcode-Status.

# Operations

The account admin can perform different user management operations from the CleverTap dashboard. Each of these operations is described briefly in the following sections.

## Invite Users

To invite a new user to the CleverTap dashboard:

1. Navigate to _Settings_ > _Users_ from the CleverTap dashboard. 
2. Click **+ User**. On clicking, the _Invite users_ window displays on the right side.
3. Enter the email address and assign the role. For more information about different roles in the CleverTap dashboard, refer to [Role-Based Access Control](doc:role-based-access-control).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bfb01eb-MU2.png",
        "Invite a New User",
        "A dashboard image showing how to invite a new user. Enter the email and select the role type that you want to assign"
      ],
      "align": "center",
      "border": true,
      "caption": "Invite Users"
    }
  ]
}
[/block]


> 📘 Assign Multiple Roles to a User
> 
> You can assign multiple roles to a user if needed. If you assign two system roles to the user, the role with higher precedence is assigned to the user.

> 📘 Invite Multiple Users at Once
> 
> You can invite multiple users (up to 50) at once by clicking **+ User** from the _Invite User_ window.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c6339c4-invite_users1.png",
        "Invite Multiple Users to Dashboard",
        "A dashboard image showing how to invite multiple users at once to the project"
      ],
      "align": "center",
      "border": true,
      "caption": "Invite Multiple Users at Once"
    }
  ]
}
[/block]


4. Click **Invite** to extend invitations to the email IDs added.

## Download User List

You can download the list of all the users by clicking **Download as CSV** from the _Users_ page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f01b3b7-csv.png",
        "Download User List",
        "A dashboard image showing the option to download user list as CSV"
      ],
      "align": "center",
      "border": true,
      "caption": "Download User List as CSV"
    }
  ]
}
[/block]


## Edit a Role

You can also edit the role of the user in the future. To do so, click the ![Ellipses](https://files.readme.io/2717d2a-ellipses_icon.png) against the required user and select _Edit Role_ from the list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7233579-Edit_Role_Access.png",
        "Edit a Role",
        "A dashboard image showing the option to Edit Role of a user"
      ],
      "align": "center",
      "border": true,
      "caption": "Edit Role"
    }
  ]
}
[/block]


For more information about role management, refer to [Role-Based Access Control](doc:role-based-access-control).

### Bulk Action For Managing Multiple User Roles

You can assign or unassign roles for multiple users at once. To do so: 

1. Navigate to _Settings_ > _Users_
2. Select the set of users for whom you want to assign or unassign the roles
3. Click the Hat ![](https://files.readme.io/22ed0b8-image.png)icon.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5b995f0-assign_unassign.png",
        "",
        "Manager Multiple User Roles in Bulk"
      ],
      "align": "center",
      "border": true,
      "caption": "Manage Multiple User Roles in Bulk"
    }
  ]
}
[/block]


4. After the _ Edit Roles_ window opens, enter the roles you wish to assign to your users in the _Assign roles_ field.    Similarly, enter the roles you wish to unassign for your users in the _Unassign roles_ field. 
5. After making the required changes, click **Continue**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/24fb83d-assign_roles.png",
        "",
        "Save Bulk Actions"
      ],
      "align": "center",
      "border": true,
      "caption": "Save Bulk Actions"
    }
  ]
}
[/block]


6. Review the bulk changes in user roles and click **Save**.

## Revoke Access

Revoking user access implies that the user no longer has access to the dashboard. To do so, click the ![Ellipses](https://files.readme.io/2717d2a-ellipses_icon.png) against the required user and select _Revoke User Access_ from the list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3a5c201-revoke_acess.png",
        "Revoke Access",
        "A dashboard image showing the option to Revoke User Access of a user"
      ],
      "align": "center",
      "border": true,
      "caption": "Revoke User Access"
    }
  ]
}
[/block]


## Grant User Passcode

Every CleverTap API call requires a passcode to authenticate the API calls. Granting a user passcode helps authenticate the user when making API calls. To grant a passcode, click the ![Ellipsis](https://files.readme.io/2717d2a-ellipses_icon.png) icon against the required user and select _Grant Passcode_ from the list. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/88fa387-_grant.png",
        "Grant Passcode",
        "A dashboard image showing the option to Grant Passcode to a user"
      ],
      "align": "center",
      "border": true,
      "caption": "Grant Passcode"
    }
  ]
}
[/block]


Select the tenure for which you want to grant the passcode and then click **Grant** to confirm your action.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8e5cc88-grant-passcode.png",
        "Grant Passcode",
        "A pop-up asking to select the Passcode Time for the user"
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Select Passcode Time"
    }
  ]
}
[/block]


For more information about API authentication in CleverTap, refer to [Authentication](https://developer.clevertap.com/docs/authentication).

## Reset Passcode

Reset Passcode generates a fresh new passcode for the user. Post resetting, the user must incorporate this passcode for the APIs. To reset the passcode, click the ![Ellipses](https://files.readme.io/2717d2a-ellipses_icon.png) icon against the required user and select _Reset Passcode_ from the list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ca50b70-reset.png",
        "Reset Passcode",
        "A dashboard image showing the option to Reset the Passcode of a user"
      ],
      "align": "center",
      "border": true,
      "caption": "Reset Passcode"
    }
  ]
}
[/block]


# FAQ

### Q. How to recover Admin access and assign it to a new user if the original Admin account is deactivated?

A. If your organization’s sole admin account has been deactivated and you no longer have access to it, you can still recover admin access and assign new admin privileges by following these steps:

1. Contact your organization’s IT administrator or domain owner to temporarily reactivate and grant access to the email account of the Project's admin.

2. Once the account is reactivated, use the _Forgot Password_ option on the CleverTap login page to reset the password for that admin user account.

3. After resetting the password, log in to the account and assign admin access to an existing user within your Project or invite a new user with Admin access. This new admin will then have access to the CleverTap dashboard for that project.

4. (Optional) [Revoke](doc:manage-users#revoke-access) the former admin's access from the dashboard project.

To prevent similar issues in the future, CleverTap recommends assigning admin roles to at least two users. This ensures that if one admin leaves or becomes unavailable, the other can still manage the project and perform necessary administrative tasks.