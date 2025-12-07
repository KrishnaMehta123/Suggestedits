---
title: Teams in Campaigns
excerpt: Learn how to use the Teams feature for campaigns.
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

The [Teams](https://staging.docs.user.clevertap.net/docs/teams-feature-setup-guide) feature in CleverTap introduces scoped access to campaigns, ensuring that users only view, create, manage, and publish campaigns that belong to their assigned teams. This enforces cleaner ownership, stricter governance, and prevents cross-team content visibility.

This document outlines how Teams affect campaign creation, editing, approval workflows, segment usage, and visibility across the dashboard.

# Access and Roles

Teams work in conjunction with Roles to define both **permissions** and **scope**.

| Role Type      | Campaign Access                                 |
| -------------- | ----------------------------------------------- |
| Admin          | Access to all campaigns across all teams        |
| Creator        | Can create/edit campaigns within assigned teams |
| Member         | Can view campaigns only in their team           |
| Approval Agent | Can approve campaigns in their team             |
| Custom Roles   | Scoped to teams and configured with permissions |

> 📘 Note
>
> Admins are always members of all teams and cannot be removed.

# Creating and Managing Campaigns

### Viewing Campaigns on the Campaigns Listing Page

On the Campaigns listing page, a *Team* column is included to indicate the team under which each campaign is created.

* Users only see campaigns that belong to the teams they are assigned to.
* Admins see all campaigns across all teams.
* If a user attempts to directly access a campaign (for example, via shared URL) outside their team scope, they will encounter a "permission denied" error and be blocked from viewing it.

<Image alt="Teams in Campaign Listing" align="center" border={true} src="https://files.readme.io/85c7d4a2d63eb0af415f725054200340ab2f662123298c247903c6c52196849d-Teams_in_Campaign.png">
  Teams in Campaign Listing
</Image>

You can also filter the campaigns based on teams.

<Image alt="Filter Campaigns" align="center" src="https://files.readme.io/c77317893a075995d007dac9af93bc9932cac00f75d38bd95dc69cc844268259-Filter_by_Teams.png">
  Filter Campaigns
</Image>

This view ensures that campaign visibility aligns with the access rules defined through Teams.

### Team Selection During Creation

When a user initiates a new campaign, the team assignment step determines where that campaign will reside and who will be able to access it:

* If the user is assigned to only one team, the team is automatically selected and locked. The user cannot change it.
* If the user is part of multiple teams, a dropdown is shown with a list of teams they belong to. The first team (based on join order) is preselected, but users can change it to any other team they are part of.
* Admins can create campaigns under any team, as they are implicitly part of all teams.

<Image alt="Team Selection" align="center" border={true} src="https://files.readme.io/0b50e3c7e5aebc2ce087f3e3d164384b253849da097fc7a28b9cbf02590d36f1-Select_Team.png">
  Team Selection
</Image>

This selection ensures that the campaign is created with appropriate access boundaries right from the start.

### Changing a Campaign’s Team

After a campaign is created, its team assignment is locked in most states. The only exception is when the campaign is still in *Draft*.

* In Draft state, users can update the assigned team if needed. 
* Once the campaign moves into Running, Scheduled, Completed, or Archived states, the team cannot be changed.
* In case users try to change the team while the selected segments or dependencies don’t exist in the new team, validation errors will appear and users can reselect those inputs.

<Image alt="Changing a Campaign’s Team in Draft State" align="center" border={true} src="https://files.readme.io/2896a9b0810df8b7e7f9ad20b4a8d8066a6021dd5d32a506c273c6b904fcd6d3-Edit_Teams.png">
  Changing a Campaign’s Team in Draft State
</Image>

This limitation ensures that the campaign content remains consistent after launch.

# Segment Usage in Campaigns

* During campaign creation, only segments from the **selected team** are available in the "Who" section.
* Include/Exclude queries also show segments from the current team only.

> 🚧 Segments cannot be shared across teams.
>
> If you change the team while the campaign is still in draft, previously selected segments may not be valid and trigger errors. You must reselect appropriate segments for the new team.

# Campaign Approvals and Teams

When **Maker-Checker** is enabled, campaign approval requests go to:

* **All Admins** regardless of team.
* **Team-specific approvers**, which are users with campaign approval permissions within the selected team.

For example, there are two teams, Team A and Team B. Both teams have an approver. In such cases, refer to the following scenarios:

| User Type         | User’s Team | Campaign Created In | Approval Request Sent | Notes                                       |
| :---------------- | :---------- | :------------------ | :-------------------- | :------------------------------------------ |
| Admin             | All Teams   | Team A              | Yes                   | Admins always receive all approval requests |
| Admin             | All Teams   | Team B              | Yes                   | Admins always receive all approval requests |
| Approver          | Team A      | Team A              | Yes                   | Approver is in the same team as campaign    |
| Approver          | Team A      | Team B              | No                    | Approver is in a different team             |
| Approver          | Team B      | Team A              | No                    | Approver is in a different team             |
| Non-approver user | Team A or B | Team A or B         | No                    | No approval permission                      |

> 📘 Note
>
> If no approvers exist in the campaign's team, Admins can handle the approval workflow without operational blockage.

# Default Team Behavior

When Teams is first enabled:

* All existing campaigns are assigned to the **Default Team** irrespective of their states.
* Any campaign created without selecting a team defaults here.
* Campaigns in the Default Team are visible only to users who belong to it, or Admins.

# FAQs

### Can a campaign be moved to another team after publishing?

No. Team reassignment is allowed only in draft state.

### What happens if a user is removed from a team?

If a user is removed from a team, they lose access to all campaigns belonging to that team.

### Can segments from one team be used in another team’s campaign?

No. Segment usage is restricted to the team selected during campaign creation.

This document is part of Teams governance. For setup details, refer to [Teams Setup](link) and for segment-specific rules, refer to [Teams in Segmentation](link).
