---
title: Node stats
excerpt: View stats for each Journey node.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
#Node Stats
The Node Stats tab shows you the stats for each node. You can account for all users who entered the Journey and their current state.
The ID mentioned at the node is the sequence number of the node.
Each step is indicated by an ID on the top right corner of the pertinent node.

Click the **Node Stats** tab. Select the *date range* from the calendar. The following shows how to check the statistics for each of the node types:

##Entry Node
This is the first node in the Journey. There can be only one *Entry* node.  An *Entry* node can only be a *Segment* node. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f7aca14-Journeys_node_Entry.png",
        "Journeys_node_Entry.png",
        317,
        250,
        "#e5e8ee"
      ],
      "border": false,
      "caption": "Entry node",
      "sizing": "smart"
    }
  ]
}
[/block]

[block:parameters]
{
  "data": {
    "h-0": "Stat",
    "h-1": "Description",
    "0-0": "Qualified",
    "0-1": "The total number of users who qualified for the journey. This stat is available only on the entry node.",
    "1-0": "Entered Journey",
    "1-1": "The users who have entered a Journey via node connectors, such as Yes or No.",
    "2-0": "Control Group",
    "2-1": "The number of users who were marked for the control group. \n\nA control group is a set of users who do not receive any marketing campaigns. You can measure the effectiveness of your initiatives by comparing this group with the target group of users who received your campaigns."
  },
  "cols": 2,
  "rows": 3
}
[/block]
##Segment Nodes
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5a1ed63-Journeys_node_Segment.png",
        "Journeys_node_Segment.png",
        316,
        302,
        "#eceaeb"
      ],
      "caption": "Segment node"
    }
  ]
}
[/block]

[block:parameters]
{
  "data": {
    "h-0": "Stat",
    "h-1": "Description",
    "0-0": "Entered Node",
    "0-1": "The total number of users who entered the node. It includes the sum of all the users from Moved forward, Waiting users, Goal Met, and Journey timeout.",
    "1-0": "Moved forward",
    "2-0": "Waiting users",
    "3-0": "Goal Met",
    "4-0": "Journey timeout exits",
    "2-1": "The users waiting at a node to qualify. The users may wait for either of the 2 reasons: \n1. Delay from a previous node\n2. Waiting to perform an action",
    "1-1": "The users who have moved forward via node connectors, such as Yes, No, or Node Timeout.",
    "4-1": "These are the users who exited the Journey after the time duration set for the Journey, that is, Journey Timeout is complete.",
    "3-1": "These are the users who have performed the intended goal, such as viewing a movie or purchasing a product."
  },
  "cols": 2,
  "rows": 5
}
[/block]
##Engage Nodes
Simply put, *Engage* nodes are campaigns. You can see the stats of each campaign from the *Node Stats* tab. Click the **Engage** node from the *Nodes Stats* tab to see the campaign statistics. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e443e68-Journeys_nodes_Engage.png",
        "Journeys_nodes_Engage.png",
        315,
        327,
        "#e8ecee"
      ],
      "caption": "Engage node"
    }
  ]
}
[/block]

[block:parameters]
{
  "data": {
    "h-0": "Stat",
    "h-1": "Description",
    "2-0": "Waiting users",
    "2-1": "These users may wait for either of the 2 reasons: \n1.  Before Node: Delay from a previous node\n2. At Node: The outcome for these users is not defined. For example, if the 'Failed' connector is not connected, the users in this state will be counted in ‘At node.’",
    "1-0": "Moved Forward",
    "1-1": "The users who have moved forward via node connectors, such as Sent, Viewed, Clicked, Failed, and Unreachable.",
    "3-0": "Goal Met",
    "3-1": "These are the users who have performed the intended goal, such as viewing a movie or purchasing a product.",
    "4-0": "Journey timeout exits",
    "4-1": "These are the users who exited the Journey after the time duration set for the Journey, that is, Journey Timeout is complete.",
    "0-0": "Entered Node",
    "0-1": "The total number of users who entered the node. It includes the sum of all the users from Moved forward, Waiting users, Goal Met, and Journey timeout."
  },
  "cols": 2,
  "rows": 5
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "Campaign Reports",
  "body": "You can view the [Campaign Reports](doc:campaign-reports) from the Engage node. Click the **Engage** node to open the campaign report."
}
[/block]
##Force Exit Node
This node stat shows only the number of force exits.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/200599b-Journeys_node_Force_exit.png",
        "Journeys_node_Force_exit.png",
        310,
        132,
        "#dad5db"
      ],
      "caption": "Force exit node"
    }
  ]
}
[/block]