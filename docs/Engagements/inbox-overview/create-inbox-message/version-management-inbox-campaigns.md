---
title: Version Management
excerpt: >-
  Learn to use CleverTap's Version Management feature for creating, editing, and
  publishing Inbox campaigns effortlessly.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
In the fast-paced world of customer engagement, clarity, and control are essential. That is where CleverTap's Version History feature steps in. It is a go-to tool for tracking every critical update to the campaign message.

With Version History, you gain clear visibility into what changes have been made to your engagement strategies. Wondering how? The feature allows you to track edits to the _What_ section of campaigns even after publishing them.  After you publish the campaign for the first time, each edit and subsequent publish action creates a new campaign version. This allows you to maintain your campaign history while implementing necessary updates.

 You can view the version history of a particular campaign from the _Overview_ tab. Each new version is assigned a sequential version number (for example, v.1, v.2, v.3).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/84b57003fbdc954f2d9626331f28e64c77093da0657304661fd149b3621970e3-image.png",
        null,
        "Version History for Email Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Version History for Inbox Campaign"
    }
  ]
}
[/block]


Each version contains the following details:

- Version number
- Email address of the person who published the changes
- Timestamp when the version is published

# Key Benefits

The following are some of the benefits of implementing CleverTap's Version Management feature:

- **Reuse Content**: Marketers run promotional campaigns to drive sales and engagement. With a diverse customer base and ever-changing market dynamics, they need a solution that allows for dynamic content changes while retaining the ability to reuse successful campaign elements. The CleverTap's Version Management feature comes to the rescue in this case.
- **Maintain Regulatory Compliance**: If you are a FinTech organization, you can modify campaign content in accordance with regulatory requirements while maintaining a comprehensive version history for compliance purposes. The archived version history serves as auditable documentation for regulatory audits, tracking the evolution of campaign content and compliance disclosures over time.

# How Does it Work?

This section provides information about how CleverTap manages different versions of a particular campaign, highlighting how each edit and subsequent publish action generates a new version of a campaign while retaining previous versions for reference. 

Consider a scenario where a campaign is initially created and set up. When you publish the campaign for the first time, it becomes the Base Version, marked as the current version. Next time, when you edit the _What_ section of this campaign and publish the changes, a new version, Version 1, is created. Now, Version 1 becomes the current version. Similarly, a new version is created when you make changes and publish the campaign again. The most recent published version always becomes the current version (see the following illustration).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bf8cc61-Version_Management_Graphics.png",
        "",
        "Version Management in CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Version Management in CleverTap"
    }
  ]
}
[/block]


**Key Points**:

- **Incremental Versioning**: Each publish action creates a new version, with versions numbered incrementally (Version 1, Version 2, and so on).
- **Current Version**: The most recently published version is always the current version.
- **Preservation of Older Versions**: Previous versions are retained for reference and can be revisited if needed. CleverTap preserves a maximum of 50 versions for a particular campaign. If more than 50 versions are created, only the most recent 50 versions are displayed in the version dropdown, with older versions being overridden.

Using this feature, you can ensure that any changes to a campaign are systematically recorded. This allows for easy tracking and managing the campaign's evolution and provides a clear history of all modifications.

> 📘 Role-Based Access Control in Version Management
> 
> Role-Based Access Control (RBAC) is currently not supported for Version Management.

# Manage Versions

You can create or clone a version, ensuring seamless campaign optimization.

## Create a Version

To create a version:

1. Click the campaign you want to edit from the _Campaigns_ page.
2. Go to the _Overview_ tab. The current campaign version opens.
3. Click the ![Edit](https://files.readme.io/bba69a0-Edit_icon.png) icon to create a new campaign version from the current one. You can also select from the list of versions and edit the selected campaign. The edited version becomes the new version. 
4. Modify the campaign message and click **Publish**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/23b887378463cd2a60a865a9a68e1296f88f39fb9c8259d37c44b786b2d40db8-create_a_version.gif",
        null,
        "Create a new version"
      ],
      "align": "center",
      "border": true,
      "caption": "Create a new version"
    }
  ]
}
[/block]




> 📘 Note
> 
> A new version is created if you did not make any edits between opening and publishing a particular version.

After you publish the campaign, a new version appears in the version dropdown on the _Overview_ page.

## Clone a Version

You can only clone the current campaign version:

1. Click the campaign you want to edit from the _Campaigns_ page. The current campaign version opens.
2. Go to the _Overview_ tab and click the ![](https://files.readme.io/46b1c04-Clone_icon_-_version_management.png)icon to create a new campaign version.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/657e844549ce99422ad997baea47058370d05082e80374052f847038fc13c6b0-image.png",
        null,
        "Clone a version"
      ],
      "align": "center",
      "border": true,
      "caption": "Clone a version"
    }
  ]
}
[/block]


3. Modify the campaign message and click **Publish**.