---
title: Version Management
excerpt: >-
  Understand how CleverTap's Version Management feature allows marketers to
  create, edit, and publish campaigns effortlessly.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Version Management in CleverTap allows you to edit the _What_ section of campaigns even after publishing them.  After you publish the campaign for the first time, each edit and subsequent publish action creates a new campaign version. This allows you to maintain your campaign history while implementing necessary updates.

This feature is currently enabled only for Email campaigns. You can view the version history of a particular campaign from the _Overview_ tab. Each new version is assigned a sequential version number (for example, v.1, v.2, v.3)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/458ed56-image.png",
        null,
        "Version History for Email Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Version History for Email Campaign"
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

Consider a scenario where a campaign is initially created and set up. When you publish the campaign for the first time, it becomes the Base Version, marked as the current version. Next time, when you edit the _What_ section of this campaign and publish the changes, a new version, Version 1, is created. Also, Version 1 also becomes the current version now. Similarly, when you make changes and publish the campaign again, a new version is created. And, the most recent published version becomes the current version always (see the following illustration).

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

- **Incremental Versioning**: Each publish action creates a new version, with versions numbered incrementally (Version 1, Version 2, etc.).
- **Current Version**: The most recently published version is always the current version.
- **Preservation of Older Versions**: Previous versions are retained for reference and can be revisited if needed. CleverTap preserves a maximum of 50 versions for a particular campaign. If more than 50 versions are created, only the most recent 50 versions are displayed in the version dropdown, with older versions being overridden.

Using this feature, you can ensure that any changes to a campaign are systematically recorded. This allows for easy tracking and management of the campaign's evolution and provides a clear history of all modifications.

> 📘 Role-Based Access Control in Version Management
> 
> Role-Based Access Control (RBAC) is currently not supported for Version Management.

# Manage Versions

You can create or clone a version, ensuring seamless campaign optimization.

## Create a Version

To create a version:

1. Click the campaign you want to edit from the _Campaigns_ page.
2. Go to the _Overview_ tab. The current campaign version opens.
3. Click the ![Edit](https://files.readme.io/bba69a0-Edit_icon.png) icon to create a new campaign version from the current one. You can also select from the list of versions and edit the selected campaign.
4. Modify the campaign message and click **Publish**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3f3f9c2-Create_a_Version.gif",
        "",
        ""
      ],
      "align": "center",
      "border": true
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
        "https://files.readme.io/6c59d02-Clone_a_Version.gif",
        "",
        "Clone a Version"
      ],
      "align": "center",
      "border": true,
      "caption": "Clone a Version"
    }
  ]
}
[/block]


3. Modify the campaign message and click **Publish**.