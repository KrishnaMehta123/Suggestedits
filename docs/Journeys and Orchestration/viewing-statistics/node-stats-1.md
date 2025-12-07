---
title: Node Stats
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Node Stats

The Node Stats tab shows you the stats for each node. You can account for all users who entered the Journey and their current state.

The ID mentioned at the node is the sequence number of the node.  
Each step is indicated by an ID on the top right corner of the pertinent node.

Click the **Node Stats** tab. Select the date range from the calendar. The following section show how to check the statistics for each of the node types:

## Entry Node

This is the first node in the Journey. There can be only one Entry node. An Entry node can only be a Segment node.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/53a486bcfdb0d168359b16576f77015010e37eff2d252b2d9c8a9ccbb45dedb6-image.png",
        null,
        "Entry Node"
      ],
      "align": "center",
      "border": true,
      "caption": "Entry Node"
    }
  ]
}
[/block]


| Stat            | Description                                                                                                                                                                                                                                                                        |
| :-------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Qualified       | The total number of users who qualified for the journey. This stat is available only on the entry node.                                                                                                                                                                            |
| Entered Journey | The users who have entered a Journey via node connectors, such as Yes or No.                                                                                                                                                                                                       |
| Control Group   | The number of users who were marked for the control group. A control group is a set of users who do not receive any marketing campaigns. You can measure the effectiveness of your initiatives by comparing this group with the target group of users who received your campaigns. |

## Segment Nodes

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5a1ed63-Journeys_node_Segment.png",
        "Segment node for Journeys",
        316
      ],
      "align": "center",
      "border": true,
      "caption": "Segment node"
    }
  ]
}
[/block]


| <p>Stat</p>           | <p>Description</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| :-------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Entered Node</p>   | <p>The total number of users who entered the node. It includes the sum of all the users from Moved forward, Waiting users, Goal Met, and Journey timeout.</p>                                                                                                                                                                                                                                                                                                        |
| <p>Moved forward</p>  | <p>The users who have moved forward via node connectors, such as Yes, No, or Node Timeout.</p>                                                                                                                                                                                                                                                                                                                                                                       |
| <p>Waiting users</p>  | <p>The users waiting at a node to qualify. The users may wait for either of two reasons: </p><ul><li>Delay from a previous node</li><li>Waiting to perform an action</li></ul>                                                                                                                                                                                                                                                                                       |
| <p>Goal Met</p>       | <p>These users have performed the intended goal, such as viewing a movie or purchasing a product.</p><ul><li><em>Before Node</em><br>Indicates that the user achieved the goal while waiting on the delay path but did not get a message from the next node.</li><li><em>At Node</em><ul><li>Indicates that the user is on the node</li><li>If the 'Failed' connector is not connected, the users in this state are counted as <em>At Node.</em></li></ul></li></ul> |
| Journey timeout exits | These are the users who exited the Journey after the time duration set for the Journey, that is, Journey Timeout is complete.                                                                                                                                                                                                                                                                                                                                        |

## Engage Nodes

Simply put, _Engage_ nodes are campaigns. You can see the stats of each campaign from the _Node Stats_ tab. Click the **Engage** node from the _Nodes Stats_ tab to see the campaign statistics. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e443e68-Journeys_nodes_Engage.png",
        "Engage nodes for Journeys",
        315
      ],
      "align": "center",
      "border": true,
      "caption": "Engage Node"
    }
  ]
}
[/block]


[block:parameters]
{
  "data": {
    "h-0": "<p>Stat</p>",
    "h-1": "<p>Description</p>",
    "0-0": "<p>Entered Node</p>",
    "0-1": "The total number of users who entered the node. It includes the sum of all the users from Moved forward, Waiting users, Goal Met, and Journey timeout.",
    "1-0": "<p>Moved Forward</p>",
    "1-1": "Users who have moved forward via node connectors, such as Sent, Viewed, Clicked, Failed, and Unreachable.  \nUnreachable’ profiles are profiles that do not have any identity, email, phone, or token (web/ push).",
    "2-0": "<p>Waiting users</p>",
    "2-1": "<p>These users may wait for either of two reasons: </p><ul><li><em>Before Node</em><ul><li>Delay from a previous node.</li><li>Unreachable profiles if an Unreachable path is not drawn. </li></ul></li><li><em>At Node</em><br>The outcome for these users is not defined. For example, if the 'Failed' connector is not connected, the users in this state will be counted in the <em>At node.</em></li></ul>",
    "3-0": "<p>Goal Met</p>",
    "3-1": "<p>These users have performed the intended goal, such as viewing a movie or purchasing a product.</p><ul><li><em>Before Node</em><br>Indicates that the user achieved the goal while waiting on the delay path but did not get a message from the next node.</li><li><em>At Node</em><ul><li>Indicates that the user is on the node</li><li>If the <em>Failed</em> connector is not connected, the users in this state are counted in the <em>At node.</em></li></ul></li></ul>",
    "4-0": "Journey timeout exits",
    "4-1": "These are the users who exited the Journey after the time duration set for the Journey, that is, Journey Timeout is complete."
  },
  "cols": 2,
  "rows": 5,
  "align": [
    "left",
    "left"
  ]
}
[/block]


> 📘 Campaign Stats
> 
> You can view the campaign-level stats for every node. Click the **Engage** node to open the campaign-level stats.

> 📘 Unique Users Converted
> 
> If a user enters the journey and performs the conversation event twice, only one conversation event for that unique user is counted.

## Force Exit Node

This node stat shows only the number of force exits.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/200599b-Journeys_node_Force_exit.png",
        "Force exit node for Journeys",
        310
      ],
      "align": "center",
      "border": true,
      "caption": "Force Exit Node"
    }
  ]
}
[/block]