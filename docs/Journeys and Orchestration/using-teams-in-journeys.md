---
title: Using Teams in Journeys
excerpt: >-
  Learn how the new Teams feature helps you create, manage, and access Journeys
  in a more organized and secure way, tailored to your department or a group.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

You can organize and control access to Journeys using Teams in CleverTap. This means each business department or working group can manage their own Journeys separately, so only team members belonging to the specific team can view, edit, or approve the campaigns it is responsible for. This helps avoid accidental changes and keeps work focused within the right teams.

This document explains how the Teams feature in CleverTap affects the way users create, manage, and collaborate on journeys.

# Access and Roles

Teams work with Roles to define both **what users can do** (permissions) and **what they can access** (team-scoped entities).

[block:parameters]
{
  "data": {
    "h-0": "**Role Type**",
    "h-1": "**Access Description**",
    "0-0": "**Admin**",
    "0-1": "They have full access to all Campaigns, Journeys, and Segments across all teams in the project.  \n  \n**Note**: Admins are always members of all teams and cannot be removed.",
    "1-0": "**Creator**",
    "1-1": "They can create and edit Campaigns, Journeys, and Segments within their assigned teams.",
    "2-0": "**Member**",
    "2-1": "They can view Campaigns, Journeys, and Segments created within their teams.",
    "3-0": "**Approver**",
    "3-1": "They can approve campaigns created by users on their team if they have approval permissions.",
    "4-0": "**Custom Roles**",
    "4-1": "Access is limited to the user’s teams and governed by their configured permissions. For example, a Team Marketing Manager can publish journeys for Team A, but cannot access anything under Team B."
  },
  "cols": 2,
  "rows": 5,
  "align": [
    null,
    null
  ]
}
[/block]


# View Journeys on Listing Page

The _Team_ column on the Journeys listing page displays the team associated with each journey.

![](<>)

- You can view only the journeys that belong to the teams you are assigned to.
- Admin users can view all journeys across all teams.
- If you try to access a Journey via a shared link belonging to a different team, you will see a _Permission Denied_ error.

You can also **filter** and **sort** the Journey list by Team. The _Created By_ filter continues to display the journey creator, even if they are no longer part of the team.

# Assign Journey to Team

When a user initiates a new journey, the team assignment step determines where that journey will reside and who will be able to access it:

- If the user is assigned to only one team, that team is automatically selected and locked, and the user cannot change it once the journey is published, even in edit.
- If the user is part of multiple teams, a dropdown shows a list of the teams they belong to. The first team (based on join order) is preselected, but users can change it to any other team they are part of.
- Admins can create journeys under any team, as they are implicitly part of all teams.
- When you clone a journey, the team assignment cannot be changed. The cloned journey automatically inherits the same team as the original.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2e669108e0f3cedcccf06d29b84e82787bb035ae1ffd1f4e6f14f0118000c61a-Assign_Journey_to_a_Team.png",
        "",
        "Assign Journey to a Team"
      ],
      "align": "center",
      "border": true,
      "caption": "Assign Journey to a Team"
    }
  ]
}
[/block]


This selection ensures that the journey is created with appropriate access rights.

> 📘 Default Team
> 
> When Teams is first enabled:
> 
> - All existing campaigns are assigned to the **Default Team** irrespective of their states.
> - Any journey created without selecting a team is assigned to Default Team.
> - Journeys in the Default Team are visible only to users who belong to it or Admins.

# Change Team for Journey

You can only change the assigned team if the Journey is still in **Draft** state. If the Journey is in **Running**, **Scheduled**, **Completed**, **Paused**, or **Archived** state, the team **cannot** be changed. If the newly assigned team does not have access to selected segments or triggers, validation errors are displayed. You must update the journey by selecting segments and dependencies that belong to the newly assigned team.

# Segmentation in Journeys

When defining the audience in the _Who_ section or configuring any node that uses segments, such as goals, conditional splits, or IntelliNODEs:

- Only segments created within the **same team** as the Journey are available.
- This also applies to **Include/Exclude** segments.

When using another journey as a trigger, only journeys belonging to the selected team are available.

> 🚧 Sharing Segments Across Teams
> 
> If you change the team for a draft Journey, previously selected segments from a different team become invalid and must be replaced.

# FAQs

Here are answers to common questions about using Teams with Journeys.

### Can a journey be moved to another team after publishing?

No. The team reassignment is allowed only in the _Draft_ state.

### What happens if a user is removed from a team?

If a user is removed from a team, they lose access to all engagements belonging to that team.

### Can segments from one team be used in another team’s campaign?

No. Segment usage is restricted to the team selected during campaign creation. For setup details, refer to [Teams Setup](link) and for segment-specific rules, refer to [Teams in Segmentation](link).