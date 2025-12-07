---
title: Custom Dashboards_CD Enhancements
excerpt: ''
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

CleverTap provides a set of default dashboards, such as the [Today View](doc:today-view), which you can use to analyze user activity in your application. _Custom Dashboards_ is a feature in CleverTap that allows you to create and customize your board. 

Each custom dashboard you create is composed of cards, which are widgets you can pin to the board to track the metrics of your interest. You can pin cards that track [events](doc:events), [funnels](doc:funnels), [segments](doc:segments), [trends](doc:trends), and [cohorts](doc:cohorts).

For example, if you want to create a custom dashboard to analyze _Charged_ events over the past 30 days, you can add a line graph card to view the number of _Charged_ events and a bar graph to view the distribution between App Launched and Charged.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/330f13a-Custom_Dashboard_-_Overview.png",
        "Custom Dashboard - Overview.png",
        2370
      ],
      "border": true
    }
  ]
}
[/block]

After you build your custom dashboard, you can pin an item to a custom board and can also share the board with other people in your organization.  
Custom dashboards can have the following features: Boards, Cards, and Workflows.

# Boards

This section provides information about different user operations on the boards. Users can view a list of all boards created by them and the public boards available for users in their organization. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0b2c839-List_of_Boards.png",
        "List of Boards.png",
        2380
      ],
      "border": true
    }
  ]
}
[/block]

## Operations

Select the board from the _All Boards_ page. You can perform the following actions on a particular board:

- ### Sort
  You can sort the boards by the date on which the board was created and the person who created the board.  
  You can do so by clicking the ![Arrow](https://files.readme.io/ea0d68c-Arrow_icon.png) icon present under _Created by_ and _Created on_ columns.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f99cf25-Sort_Boards.png",
        "Sort Boards.png",
        2378
      ],
      "border": true
    }
  ]
}
[/block]

- ### Search
  You can search the boards by board name or creator email. You can do so by entering the search criteria under the Search text box.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7a31a9a-Search_boards.png",
        "Search boards.png",
        2378
      ],
      "border": true
    }
  ]
}
[/block]

- ### Mark As Favorite
  To mark a particular board as a favorite:

1. Select the board from the _Boards_ > _All boards_ page.
2. Click **Mark As Favorite** present at the top of the page. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e061901-Mark_As_Favorite.png",
        "Mark As Favorite.png",
        2370
      ],
      "border": true
    }
  ]
}
[/block]

The message _Board marked as favorite successfully!_ displays at the top of the board page.

- ### Change Date Range
  You can view the data for the different periods by changing the date range of all cards on the board.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/19635f0-Change_Date_Range.gif",
        "Change Date Range.gif",
        1188
      ],
      "border": true
    }
  ]
}
[/block]

- ### Refresh
  You can refresh the dashboard to view the most recent information by clicking **Refresh** present at the top of the page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9ee1da4-Refresh.png",
        "Refresh.png",
        2370
      ],
      "border": true
    }
  ]
}
[/block]

- ### Share

  CleverTap provides restricted dashboard access so that the owner of a dashboard can control the members who can view and contribute to the insights captured on the dashboard. The dashboard owner can add and remove members from the access list and can control access levels.

    To share a dashboard, perform the following steps:

1. Create your custom dashboard.
2. Click **Share**. The _Share Board_ popup displays with restricted permissions by default. Use the search box to view and add users to this board.

> 🚧 Share Board
> 
> The _Share_ option is only visible to the board's creator after they create the board.

3. Select a user and click **Send**. An email is sent to the user with a link to the board.  
   Select as many users as needed before clicking **Send** to add multiple users.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/98a8931-Share_Board_-_Select_User.png",
        "Share Board - Select User.png",
        560
      ],
      "border": true
    }
  ]
}
[/block]

> 📘 Change Default Board Permissions
> 
> You can change the default permissions by clicking the _Change_ link on the Share Board and selecting the appropriate permission.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8f0e9f4-Share_Board_-_Change_Default_Permission.png",
        "Share Board - Change Default Permission.png",
        561
      ],
      "border": true
    }
  ]
}
[/block]

- ### Clone
  This option is used when you want to track almost the metrics with minor changes. You can clone the board by clicking **More** and then selecting **Clone** from the list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b5a34d1-Clone_Board.gif",
        "Clone Board.gif",
        1186
      ],
      "border": true
    }
  ]
}
[/block]

- ### Edit
  You can rename the board by clicking **More** and then selecting **Edit** from the list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b0170ce-Edit_Board.gif",
        "Edit Board.gif",
        1188
      ],
      "border": true
    }
  ]
}
[/block]

- ### Delete
  You can delete the boards you created by clicking **More** and then selecting **Delete** from the list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8faea74-Delete_Board.gif",
        "Delete Board.gif",
        1186
      ],
      "border": true
    }
  ]
}
[/block]

- ### Edit User Permissions
  You can also edit the user's permissions to either Viewer (view-only access), Editor (view and edit access), or remove the user access user completely. To do so:

1. Click **Share** and select the permission from the list next to the user name.
2. Select _Viewer_ or _Editor_. You can remove the user access by selecting _Remove_.
3. Click **Save**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e9a9c2d-Edit_User_Permission.gif",
        "Edit User Permission.gif",
        1194
      ],
      "border": true
    }
  ]
}
[/block]

## Board Limits

The following table describes a list of board limits:

| <p>Plan Type</p>                        | <p>Limits</p>                                                                                                                                                                                                                    |
| :-------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Paid Plans (Enterprise/Business)</p> | <ul><li>Each user can create up to 100 boards.</li><li>Users can pin up to 20 cards per board.</li><li>Users can share the board within the organization.</li><li>Users can pin up to 5 boards on the left navigation.</li></ul> |

# Cards

This section provides information about different user operations on the card. Select the board to view all the included cards. 

## Operations

You can perform the following actions on a particular card:

- ### Pin a Card
  Users can pin Event details, Segments, Funnels, Cohorts, or Trends to a particular card. Consider the example of pinning a card that shows information about a particular segment. To do so:

1. Navigate to _Segment_ > _Segments_.
2. Select a segment.
3. Click the ![Pin](https://files.readme.io/32ed498-Pin_icon.png) icon to pin the report to an existing or new board.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/80633fb-Cards_1_-_pin_a_card.png",
        "Cards 1 - pin a card.png",
        693
      ],
      "border": true
    }
  ]
}
[/block]

4. Enter the _Card name_ and select the board where you want to pin this card.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/64f62cf-Pin_a_segment_to_Custom_Board.png",
        "Pin a segment to Custom Board.png",
        2236
      ],
      "sizing": "smart",
      "border": true
    }
  ]
}
[/block]

> 📘 Other Analytics Features
> 
> The following steps can also be performed for _Events_, _Funnels_, _Segments_, _Find People_, and _Trends_.

- ### Rename a Card
  You can change the card's name when you hover over any card on a board. To do so, 

1. Click the ![Edit](https://files.readme.io/2ac4bf2-Edit_icon.png) icon and enter the new name.
2. Click the ![Checkmark](https://files.readme.io/34d30a8-Checkmark_icon.png) icon to save the changes.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/89651f5-Rename_a_card.gif",
        "Rename a card.gif",
        1186
      ],
      "border": true
    }
  ]
}
[/block]

- ### Refresh
  You can view the most recent data for a card by clicking the ![Refresh](https://files.readme.io/b76c705-Refresh_icon.png) icon.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d8dd771-Refresh_a_card.gif",
        "Refresh a card.gif",
        1186
      ],
      "border": true
    }
  ]
}
[/block]

- ### Delete
  You can delete the card by clicking the ![Trash](https://files.readme.io/7b0992e-Trash_icon.png) icon.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b1ad24f-Delete_a_card.gif",
        "Delete a card.gif",
        1186
      ],
      "border": true
    }
  ]
}
[/block]

> 📘 Delete Cards Access
> 
> Only the creator of the board or the administrators can delete cards on public boards.

- ### Resize
  You can resize the card by clicking the ![Resize](https://files.readme.io/ad1e01b-Resize_icon.png) icon.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d9ad652-Resize_a_card.gif",
        "Resize a card.gif",
        1186
      ],
      "border": true
    }
  ]
}
[/block]

- ### Move
  You can reorder the sequence of cards by clicking the ![Move](https://files.readme.io/9d21ac7-Move_icon.png) icon.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/763c6ef-Move_a_card.gif",
        "Move a card.gif",
        1186
      ],
      "border": true
    }
  ]
}
[/block]

> 📘 Note
> 
> The steps listed in the above section can also be followed to pin any chart that provides the Pin to board(s) option.

# Build Your First Custom Dashboard

This section covers how to build a custom dashboard. Consider the example where you want to number of users who performed Charged event for the last month.

You can do so by:

1. [Creating a custom dashboard](doc:custom-dashboards_cd-enhancements#create-a-new-board). 
2. [Pinning the card for required metrics](doc:custom-dashboards_cd-enhancements#pin-a-card-1). 

## Create a New Board

To create a board:

1. From the left navigation menu, click **Boards**.
2. Click **+ Board** to create a new board.
3. Enter your board name and click **Create**.

## Pin a Card

When you create your new board, you start with an empty board. To track the metrics mentioned above:

1. Click any of the sections within the empty board. For example, select _Trends_ to track the users who charged last month. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f8ed409-Dashboard_1_-_Pin_a_card.png",
        "Dashboard 1 - Pin a card.png",
        524
      ],
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]

2. Select _Charged_ event and select the required _Date Range_ from the _Events_ page.
3. Click ![Pin](https://files.readme.io/32ed498-Pin_icon.png) icon . 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/55558a1-Pin_a_Trend.png",
        "Pin a Trend.png",
        2372
      ],
      "border": true
    }
  ]
}
[/block]

4. Enter the _Card name_ and select an existing board or create a new board by selecting _Pin to a new board_. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ebb5624-Pin_event_to_dashboard.png",
        "Pin event to dashboard.png",
        1134
      ],
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]

5. Click **Pin** to view the metrics on the custom dashboard whenever required.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/234b3c5-Pin_your_First_Card.png",
        "Pin your First Card.png",
        2370
      ],
      "border": true
    }
  ]
}
[/block]

# Access Control

The action that a user can perform on the dashboard may vary depending on the type of their access, as shown in the following table:

|                                                | Administrator | Creator/Approver | Members                         |
| :--------------------------------------------- | :------------ | :--------------- | :------------------------------ |
| Create a board                                 | Yes           | Yes              | Yes, can create a private board |
| Delete their board                             | Yes           | Yes              | Yes                             |
| Pin a card to their board                      | Yes           | Yes              | Yes                             |
| Pin a card to any public board                 | Yes           | Yes              | No                              |
| Delete a pinned card from their board          | Yes           | No               | No                              |
| Delete any pinned cards from any public boards | Yes           | No               | No                              |