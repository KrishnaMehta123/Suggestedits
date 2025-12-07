---
title: Role-Based Access Control Beta - Remove
excerpt: Learn how to grant access on a granular level to your users.
deprecated: true
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Overview

As a part of our commitment to account security, CleverTap offers Role-Based Access Control (RBAC) for account administrators to enable different levels of access for dashboard users.

> 📘 RBAC for Product Experiences
> 
> Role-based access control (RBAC) is now supported for _Product Experiences_. For more information, refer to [Product Experiences](doc:product-experiences).

## Invite Users

The user needs an invitation and an appropriate access level to access the CleverTap dashboard. For more information about inviting users to the dashboard, refer to [Manage Users](doc:manage-users#invite-users).

# Types of Roles

Roles in CleverTap can be broadly categorized as System Roles and Custom Roles. Each of these roles has been discussed in detail in the following sections.

## System Roles

CleverTap provides four standard system roles for every account. These roles cannot be cloned, deleted, or edited.

- **Admin**: Full and unlimited access to the account.

  - Assign new users as Admin, Creator, Member, or custom roles.
  - Revoke access of an existing user.
  - Create campaigns.
  - Stop and archive campaigns.
  - Approve or reject campaigns created by users in the Creator role.
  - View analytics.
  - Download user profiles.
  - Download reports.
  - Add and update billing details.
  - Read & Modify Schema of Event & Profile Properties
  - Manage Security Features viz. IP Whitelisting, 2FA & Campaign Approval Workflow

- **Creator**: Create, edit, schedule, and stop any type of engagement such as campaigns, journeys, and product experiences.

  - Create engagements.
  - Stop and delete engagements.
  - View analytics.
  - Download reports.
  - A Creator cannot revoke user access or view billing information. 

- **Member**: View analytics and reports in the account.

  - Read-only access.
  - View analytics, including campaign performance.

- **Approver**: Approve campaigns created by users in the creator role.

> 📘 Note
> 
> The Approver role can only be accessed when the [Campaign Approval Workflow](https://docs.clevertap.com/docs/campaign-approval-workflow) feature is turned on.

- Assign new users as Creator, Member, or Custom Roles.
- Create campaigns.
- Stop and archive campaigns.
- Approve or reject campaigns created by users in the Creator role.
- View analytics.
- Download user profiles.
- Download reports.

## Custom Roles

To create a custom role, perform the following steps:

1. Navigate to _Settings_ > _Roles_ from the dashboard.  
2. Click **Create Role**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7f28c0d0d7362316f3fc1e4b40a178020819dfbd8712e722951ff087098aad04-image.png",
        null,
        "Create a New Role"
      ],
      "align": "center",
      "border": true,
      "caption": "Create a New Role"
    }
  ]
}
[/block]


3. The _Add Role_ page appears {@charul, the page copy should say "Create Role" or "Create Custom Role", not Add Role}. Select the required permissions for _Component access_  tab and click **Next**. You can specify whether the users have complete or partial access to Campaigns and Journeys limits.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9ccffbca1a8656fba72e75ef909df668da21f154ce0d36c9113642264b8410a0-image.png",
        null,
        "Provide Component Access"
      ],
      "align": "center",
      "border": true,
      "caption": "Provide Component Access"
    }
  ]
}
[/block]


4. From the Engagement Permissions tab, provide write access for the role if required. All users have read access, meaning they can view the current limits. The default value is always set to _enabled_. To learn more about access rights, refer to [Access for Advanced Custom Roles](doc:role-based-access-control-beta). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/02c537260c91f03778694a835af735d38b97d75edc4e56a877fdf76151ed178d-image.png",
        null,
        "Engagement Permissions"
      ],
      "align": "center",
      "border": true,
      "caption": "Engagement Permissions"
    }
  ]
}
[/block]


5. The _ Data Access _ tab allows you to define access for the selected users. You can provide access to all users or filter by user properties and segments. This tab also allows you to mask _Personally identifiable information_ and _Events_.  After selecting the required users, click **Next**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3b5cee660e3bb60cffc4fb2a425ac51c9af6ddd5f942a41bf30ffd743ba10a40-image.png",
        null,
        "Specify Data Access"
      ],
      "align": "center",
      "border": true,
      "caption": "Specify Data Access"
    }
  ]
}
[/block]


9. The Overview tab displays permissions assigned to the new role. You can also click the **Previous** button to change any permissions. Specify the name and click **Create **to add the new role. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/36a2944dc79224c17011e70217c2cd1ca86db0bb09e845f85cca93cb94d7a95f-image.png",
        null,
        "Role Overview"
      ],
      "align": "center",
      "border": true,
      "caption": "Role Overview"
    }
  ]
}
[/block]


<br />

# Define Access for Custom Roles

## Define Access for Basic Custom Roles

When inviting a new user, the administrators can assign a custom role to the user. Administrators can also create a new custom role or clone an existing custom role.

Set up a role by defining two things:

1. Component - Select the component for which you want to grant access.
2. Access levels:

- Read Access - Only allowed to view the feature (for example, campaign stats). For example, a particular entity is accessible to you with Read Access. You can open it and see what is present, but you can not modify anything in the entity or download any data.
- Write Access - Allowed read and write access (for example, changing throttle limits). 

## Define Access for Advanced Custom Roles

Custom roles can be mapped to user groups for advanced role-based access control. You can give various users access to different datasets and restrict access to the data you don't want them to view on the CleverTap dashboard. Administrators can also restrict data access to new custom roles based on selected user properties, such as geographies. Users assigned to these roles are limited to only the  read/write data available to the particular role. 

> 👍 Advanced Custom Role Example
> 
> You can grant access to a role _US Campaign Manager_ where the role has write access to campaigns for only users in the United States. This role cannot create campaigns for users in other geographies.

1. Assign permissions for component access and define which components are available to the user role. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d204fbd24eaf8dac03f00be6ccdade09bc1843ca048dd8b54256626762e1845d-image.png",
        null,
        "Component Access Permissions"
      ],
      "align": "center",
      "border": true,
      "caption": "Component Access Permissions"
    }
  ]
}
[/block]


3. Assign permissions for data access and define the user property data accessible by the user role.  (Optional) Mask [personally identifiable information](role-based-access-control#mask-personally-identifiable-information) or [events](role-based-access-control#mask-events).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2f9a3d0fca0a25fce0bed68574cfd0545abf6cfc9333149a8c64dc1c8933fb27-image.png",
        null,
        "Map User Properties"
      ],
      "align": "center",
      "border": true,
      "caption": "Map User Properties"
    }
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c3e0e17570fb82b12d54efecc0c2b4f24af9c40aa7f41b1e68c17474b20c9c8e-image.png",
        null,
        "Overview of Data Access"
      ],
      "align": "center",
      "caption": "Overview of Data Access"
    }
  ]
}
[/block]


<br />

# Segment Access

Segment access management in roles allows you to better manage your security, compliance, and data management. If you have dashboard users who are responsible for all marketing activities in specific sub-regions, you can grant access to only that segment of users who are from the sub-region.

> 👍 Segment Access Example
> 
> You have operations in Spain, Germany, England, Greece, and Italy and each region is managed by a regional manager. You can create a role for each of these regions where access to end-user data is restricted by their geography. In this way, each regional manager will have access to only end-users only from their region.

> 📘 Note
> 
> By picking the user property that the role is granted access to, you are restricting access to all data on CleverTap. Even if the role is viewing 'All Users' data, it is default limited to the access restriction for that role. You cannot assign more than one segment role per user.

# Operations on Custom Roles

You can edit, clone, or delete custom roles. Hover over the role and select the appropriate icon. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bbc503426c5f5508969bfd86cb7bf2fb77244764e89cc88e4ff9ded187ffb1aa-image.png",
        null,
        "Role Operations"
      ],
      "align": "center",
      "border": true,
      "caption": "Role Operations"
    }
  ]
}
[/block]


> 🚧 Deleting a Role
> 
> When a custom role is deleted, all users with this role assignment will be re-assigned as _Member_ by default.

## Access Rules and Handling Conflicts

Permissions and access can be set while creating a custom role. The following order of preference applies.

- A user can only be assigned system role(s) and custom role(s).
- **Permission Conflict on System Roles**: When a user is assigned multiple system roles, there is a permission conflict, and the role with the higher access level is enabled. For example, if a user is assigned both Admin and Creator roles, Admin access is enabled. Thus, a user cannot have multiple system roles enabled simultaneously.
- **Component Conflict on System Role & Custom Role**: When a user is assigned a system role and a custom role, there can be situations where one role has access to a component, and another role does not allow access to the same component. In this case, the permissions will be a union. For example, a user has two roles: “Creator” and “Custom B.” Role Creator has write access to Campaigns while role Custom B does not have access to Campaigns. In this scenario, the user will have write access to the Campaigns. 
- **Component Conflict on Custom Roles**: When a user is assigned multiple custom roles, there can be situations where one role has access to a component, and another role does not allow access to the same component. In this case, the permissions are restricted to the intersection of the roles. For example, a user has two roles: “Custom A” and “Custom B.” Role Custom A has write access to Campaigns while role Custom B does not have access to Campaigns. In this scenario, the user will not have write access to the Campaigns.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2ca1e03-Jash-Deepen-Document-v1.png",
        null,
        "Permission Clash For Custom Roles"
      ],
      "align": "center",
      "border": true,
      "caption": "Permission Conflict For Custom Roles"
    }
  ]
}
[/block]


## General rules of access

- Any write access automatically gives read access to the user.
- All users can have multiple custom roles; however, a user cannot have multiple system roles. 
- A user can have access to both system and custom roles at the same time. They can have one system role and unlimited custom roles. 
- System roles cannot be altered.

## Components of Access

Only the Admin role can alter and assign access to custom roles. 

| Component   | Subcomponents                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| :---------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Boards      | <ul> <li>Daily Boards</li> <li>Custom Boards</li> </ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Segments    | <ul> <li><strong>Manual segmentation</strong>: Segments, Find People</li> <li><strong>Automated segmentation</strong>: Goals, IBM, RFM</li> </ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Analytics   | <ul> <li><strong>Core Analytics</strong>: Events, Funnels, Cohorts, Trends, Attribution, Device Crossovers</li> <li><strong>Advanced Analytics</strong>: Pivots, Flows</li> </ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Engagement  | <ul> <li><strong> Campaigns</strong>: Campaigns, Clever Campaigns</li> <li><strong>Journeys</strong></li> <li><strong>Recommendation</strong></li> <li><strong>Catalogs</strong></li> </ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Real Impact | <ul> <li><strong>Control groups</strong>: Custom Control Group, System Control Group</li> <li><strong>Real Impact dashboard</strong></li> </ul>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Settings    | <ul> <li><strong>Billing</strong>: Billing, app usage, plans, invoices</li> <li><strong>Account Settings</strong>: Role Based Access Control, add new app, change account, timezone, privacy settings, uninstall</li> <li><strong>User Settings</strong>: Invite user, revoke access, account settings	</li> <li><strong>Event and User Properties</strong>	</li> <li><strong>CSV Uploads</strong>: Profile uploads and external user list	</li> <li><strong>My Profile And Password	</strong></li> <li><strong>Exports</strong>: Events and profile exports to amazon S3</li> <li><strong>Downloads</strong>: Download profiles</li> <li><strong>Email Reports</strong>: Campaign and Journey reports	</li> <li><strong>Campaign Integration and Settings</strong>: Push, Email, SMS, Web Push, FB, Google AdWords</li> <li><strong>Campaign Settings</strong>: Campaign limits, Best Time settings</li> </ul> |

## Mask Personally Identifiable Information and Events

There are two options available for masking data on user profiles:

### Mask Personally Identifiable Information

   This option allows you to mask data that describes personal information such as Email, Phone number, Location, Gender, User properties, and other sensitive data. You can mask the required Personally identifiable information from the _Settings_ > _Roles_  page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2f9a3d0fca0a25fce0bed68574cfd0545abf6cfc9333149a8c64dc1c8933fb27-image.png",
        null,
        "Enable Masking"
      ],
      "align": "center",
      "border": true,
      "caption": "Enable Masking"
    }
  ]
}
[/block]


  When the _Mask Personally Identifiable Information_ is enabled, the user Profile page appears as follows:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dda9129-mask_PII.png",
        null,
        "Masking Personally Identifiable Information "
      ],
      "align": "center",
      "border": true,
      "caption": "Masking Personally Identifiable Information "
    }
  ]
}
[/block]


### Mask Events

This option masks the data that shows the event activity of a user profile. You can mask the required Personally identifiable information from the _Settings_ > _Roles_  page.

   When _Mask Events_ is enabled, the user Profile page appears as follows:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/81c5045-Mask_Events.png",
        null,
        "Masking User Profile Events"
      ],
      "align": "center",
      "border": true,
      "caption": "Masking User Profile Events"
    }
  ]
}
[/block]