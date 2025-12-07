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
[block:api-header]
{
  "title": "Overview"
}
[/block]
The user needs an invitation and an appropriate access level to access the CleverTap dashboard. The account admin can perform different operations, such as adding a new user, assigning the role to a user, editing the user's current role, etc. from the *Settings* > *Users* page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f1e63cd-Users_page_navigation.png",
        "Users page navigation.png",
        1644,
        1126,
        "#e8e9f0"
      ],
      "border": true
    }
  ]
}
[/block]
After the new user is added, the dashboard allows an admin to view the following information about all the users added to the project: Name, Role, Email, User Status, Last Login, and Passcode-Status.

# Operations
The account admin can perform different user management operations from the CleverTap dashboard. Each of these operations is described briefly in the following sections.

## Add/Invite Users
To add/invite a new user to the CleverTap dashboard:
1. Navigate to *Settings* > *Users* from the CleverTap dashboard. 
2. Click **+ User**. On clicking, the *Invite users* window displays on the right side.
3. Enter the email address and assign the role. For more information about different roles in the CleverTap dashboard, refer to [Role-Based Access Control](doc:role-based-access-control).
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dffdeb2-Invite_a_new_user_.png",
        "Invite a new user .png",
        2374,
        1304,
        "#d3d4d7"
      ],
      "border": true
    }
  ]
}
[/block]
You can also invite multiple users at one time by clicking **+ User** from the *Invite User* window. You can invite a maximum of 50 users at one time.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/497da55-Invite_multiple_users_to_the_dashboard.png",
        "Invite multiple users to the dashboard.png",
        2374,
        1314,
        "#d2d2d5"
      ]
    }
  ]
}
[/block]
4. Click **Invite**. The message *X users successfully invited* displays if the invites are successfully sent to the users, where 'X' indicates the number of users you invited to the dashboard.
(@Saurav: After sending the invite, is the user immediately listed under the Users page?)
[block:callout]
{
  "type": "info",
  "title": "Download Users List",
  "body": "You can download the list of all the users by clicking **Download User** from the *Users* page."
}
[/block]

## Edit a Role
You can also edit the role of the user in the future. To do so, click the ![Ellipses](https://files.readme.io/2717d2a-ellipses_icon.png) against the required user and select *Edit Role* from the list.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/36add3c-Edit_Role.png",
        "Edit Role.png",
        2372,
        1202,
        "#f7f7f9"
      ],
      "border": true
    }
  ]
}
[/block]
For more information about role management, refer to [Role-Based Access Control](doc:role-based-access-control_invite-user-update).

## Revoke Access
Revoking user access invalidates the existing passcode for the user, and the user can no longer make API calls using their passcode. To do so, click the ![Ellipses](https://files.readme.io/2717d2a-ellipses_icon.png) against the required user and select *Revoke access* from the list.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3b4881c-revoke-access.png",
        "revoke-access.png",
        2372,
        1202,
        "#f7f7f9"
      ],
      "border": true
    }
  ]
}
[/block]
Click **Revoke** when prompted to confirm the action.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/114faaa-Revoke_access_.png",
        "Revoke access ?.png",
        576,
        292,
        "#f7f0f1"
      ],
      "border": true,
      "sizing": "80"
    }
  ]
}
[/block]

## Reset Passcode
Reset Passcode generates a fresh new passcode for the user. Post resetting, the user must incorporate this passcode for the APIs. To do so, click the ![Ellipses](https://files.readme.io/2717d2a-ellipses_icon.png) icon against the required user and select *Reset passcode* from the list.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a489c9d-reset-passcode.png",
        "reset-passcode.png",
        2372,
        1202,
        "#f7f7f9"
      ],
      "border": true
    }
  ]
}
[/block]
Click **Reset Passcode** when prompted to confirm your action.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e6ad6f4-reset_passcode.png",
        "reset passcode?.png",
        578,
        294,
        "#f7eced"
      ],
      "border": true,
      "sizing": "80"
    }
  ]
}
[/block]

## Grant User Passcode
Granting a user passcode helps authenticate the user when making API calls. To grant a passcode, click the ![Ellipsis](https://files.readme.io/2717d2a-ellipses_icon.png) icon against the required user and select *Grant passcode* from the list. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/571a716-grant-passcode.png",
        "grant-passcode.png",
        2372,
        1202,
        "#f7f7f9"
      ],
      "border": true
    }
  ]
}
[/block]
Select the tenure for which you want to grant passcode and then click **Grant** to confirm your action.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8e5cc88-grant-passcode.png",
        "grant-passcode?.png",
        726,
        390,
        "#f4f6f9"
      ],
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]
For more information about API authentication in CleverTap, refer to [Authentication](https://developer.clevertap.com/docs/authentication).