---
title: Node Stats
excerpt: View stats for each Journey node.
deprecated: false
hidden: true
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

Click the **Node Stats** tab. Select the _date range_ from the calendar. The following shows how to check the statistics for each of the node types:

## Entry Node

This is the first node in the Journey. There can be only one _Entry_ node.  An _Entry_ node can only be a _Segment_ node. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f7aca14-Journeys_node_Entry.png",
        "Journeys_node_Entry.png",
        317
      ],
      "sizing": "smart",
      "caption": "Entry node"
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
        "Journeys_node_Segment.png",
        316
      ],
      "caption": "Segment node"
    }
  ]
}
[/block]

| <p>Stat</p>           | <p>Description</p>                                                                                                                                                               |
| :-------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Entered Node</p>   | <p>The total number of users who entered the node. It includes the sum of all the users from Moved forward, Waiting users, Goal Met, and Journey timeout.</p>                    |
| <p>Moved forward</p>  | <p>The users who have moved forward via node connectors, such as Yes, No, or Node Timeout.</p>                                                                                   |
| <p>Waiting users</p>  | <p>The users waiting at a node to qualify. The users may wait for either of the 2 reasons: </p><ol><li>Delay from a previous node</li><li>Waiting to perform an action</li></ol> |
| Goal Met              | These are the users who have performed the intended goal, such as viewing a movie or purchasing a product.                                                                       |
| Journey timeout exits | These are the users who exited the Journey after the time duration set for the Journey, that is, Journey Timeout is complete.                                                    |

## Engage Nodes

Simply put, _Engage_ nodes are campaigns. You can see the stats of each campaign from the _Node Stats_ tab. Click the **Engage** node from the _Nodes Stats_ tab to see the campaign statistics. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e443e68-Journeys_nodes_Engage.png",
        "Journeys_nodes_Engage.png",
        315
      ],
      "caption": "Engage node"
    }
  ]
}
[/block]

| <p>Stat</p>           | <p>Description</p>                                                                                                                                                                                                                                                                             |
| :-------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Entered Node</p>   | <p>The total number of users who entered the node. It includes the sum of all the users from Moved forward, Waiting users, Goal Met, and Journey timeout.</p>                                                                                                                                  |
| <p>Moved Forward</p>  | <p>The users who have moved forward via node connectors, such as Sent, Viewed, Clicked, Failed, and Unreachable.</p>                                                                                                                                                                           |
| <p>Waiting users</p>  | <p>These users may wait for either of the 2 reasons: </p><ol><li>Before Node: Delay from a previous node</li><li>At Node: The outcome for these users is not defined. For example, if the 'Failed' connector is not connected, the users in this state will be counted in ‘At node.’</li></ol> |
| Goal Met              | These are the users who have performed the intended goal, such as viewing a movie or purchasing a product.                                                                                                                                                                                     |
| Journey timeout exits | These are the users who exited the Journey after the time duration set for the Journey, that is, Journey Timeout is complete.                                                                                                                                                                  |

> 📘 Campaign Reports
> 
> You can view the [Campaign Reports](doc:campaign-reports) from the Engage node. Click the **Engage** node to open the campaign report.

## Force Exit Node

This node stat shows only the number of force exits.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/200599b-Journeys_node_Force_exit.png",
        "Journeys_node_Force_exit.png",
        310
      ],
      "caption": "Force exit node"
    }
  ]
}
[/block]