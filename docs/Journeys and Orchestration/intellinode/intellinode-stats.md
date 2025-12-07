---
title: IntelliNODE Stats
excerpt: Understand how to view IntelliNODE Stats
deprecated: false
hidden: false
metadata:
  title: ''
  description: This page is documented for Splitter Node
  robots: index
next:
  description: ''
---
# Overview

The Stats for an IntelliNODE provide a summary of results collected for each path. This helps understand the goal conversions for the paths to decide the user distributions better. 

# View Node Stats

1. Click the required journey from the _All Journeys_ page. 
2. Click **Node Stats**. The stats page opens to show the journey nodes.
3. Select the date range to show stats for the journey. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9477aaa71df86d418e67dbd006f0fc514918418d2309ea03eb03ba9cd1ae1124-View_IntelliNODE_Node_Stats_for_a_Journey.png",
        "View IntelliNODE node stats for a Journey",
        2212
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "View IntelliNODE Node Stats for a Journey"
    }
  ]
}
[/block]


## View IntelliNODE Stats

Click the IntelliNODE on the Node Stats page to view detailed stats for each experiment. Scroll down to view the detailed stats. This page displays the following information:

- [Goal Conversion Across Paths](https://docs.clevertap.com/docs/intellinode-stats#goal-conversion-across-paths)
- [Winning Path Selection](https://docs.clevertap.com/docs/intellinode-stats#declare-winning-path)
- [Change Log](https://docs.clevertap.com/docs/intellinode-stats#view-change-log)
- [Goal Conversion (#) Across Paths Chart](https://docs.clevertap.com/docs/intellinode-stats#goal-conversion--across-paths)
- [User Distribution (%) Across Paths Chart](https://docs.clevertap.com/docs/intellinode-stats#user-distribution--across-paths)

## Goal Conversion Across Paths

You can view the goal conversion results for all paths in absolute numbers or percentages.  The values are cumulative from the date the journey was first run till the date selected on the canvas. The following details are displayed on the _Stats_ page:

- Paths: Lists all the paths drawn from the IntelliNODE. There can be up to 7 paths. 
- Users Entered: Shows all the users that entered the path. 
- Goal: Shows how many people performed the IntelliNODE goal event for each path. You can set up to 3 goals for an IntelliNODE. 
- Total Conversions: Displays the summation of all the defined goals, that is, _Goal 1 + Goal 2 + Goal 3 = Total Conversions._

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e9b4c952d2f00b58f05278ae16317650d96896d8f6c7a3d567b336440efb4a6b-Goal_Conversions_Across_Paths.png",
        "View IntelliNODE goal conversion results for all paths",
        1532
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "View IntelliNODE Goal Stats"
    }
  ]
}
[/block]


### Declare Winning Path

For Automated IntelliNODEs, you can select the preferred path and declare a winner. After a winner a declared, the experiment stops, but the journey continues to run. In the future run of the journeys, all the qualified users will move forward on the winning path.  IntelliNODE does not send any users to the non-winning paths. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/423aefc9a22fd9ed13a6b4f8cafc6962b8538366fa3acd524d458a8512ad8ba8-Declare_Winning_Path.png",
        "Select a preferred path and declare winning IntelliNODE path",
        1490
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Declare Winning IntelliNODE Path"
    }
  ]
}
[/block]


### View Change Log

You can view all the changes made to the path by clicking **View Change Log**. 

- Changelog for automated journeys: All the changes to the path are listed on this page.
- Changelog for manual journeys: The latest ten changes to the path are listed on this page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4fe9225-Intellinode_user_distribution_edit_log.png",
        "View user distribution changelog for manual and automated journeys",
        1568
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "IntelliNODE Change Log"
    }
  ]
}
[/block]


## Goal Conversion (%) Across Paths

Select the IntelliNODE goal from the list. This trend line graph shows the goal conversion % across the path for the selected IntelliNODE goal. The values on this chart are cumulative, that is, the values for each day indicate the users converted from the start of the journey to the end date selected from the canvas. 

Click on the legends at the bottom of the trend (indicated by colored squares) to hide or unhide a trend line for the selected path.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/30d8cef-IntelliNODE_goal_conversion_trend.png",
        "IntelliNODE goal conversion across path",
        1532
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "IntelliNODE Goal Conversion Across Path"
    }
  ]
}
[/block]


## User Distribution (%) Across Paths

You can view the distribution of users across paths on a daily, weekly, or monthly basis.

Select the date range for the user distribution. The trend line graph displays the selected date range. The date range could be daily, weekly, or monthly.  
This trend line shows % trend of user distribution across different paths. 

This graph will stabilize over time as more users enter the journey. For example, if only one user qualifies for the journey and is sent along a path, then the user distribution for that path will be 100 %.  However, there is greater clarity when the sample size is larger.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4f2f7ab-IntelliNODE_user_distribution_trend.png",
        "IntelliNODE user distribution across paths",
        1532
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "User Distribution Across Paths"
    }
  ]
}
[/block]