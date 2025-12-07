---
title: Journey Performance
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
# Concepts

You will need to know some key terms to understand the Journey stats.

- **Goal Met**: If a goal is set in the Journey builder, these are all users who met the goal. 
- ** Journey Timeout**: If a Journey timeout is set in the Journey builder (entry criteria), these are all the users who timed out.
- ** Node Timeout**: The qualifying window that is set for the node, after which the users will move on to the next node via the Node timeout connector.
- **Completed**: If a goal is not set in the Journey builder, these are all the users who successfully reached the last node of the Journey.

# Overview

Click _Engage_ > _Journeys_ from the left side menu. The _Journey List \_page appears. Search for a journey and then click to open a Journey. The \_Journey Canvas_ has four tabs:

- **Overview Tab**: Displays your Journey components and connections.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2084cba7569ebe28e57fe577d3a40583dfe29e1791e0cfac4ebbb738f05e1cef-Journey_Overview.png",
        null,
        "Journey Overview"
      ],
      "align": "center",
      "border": true,
      "caption": "Journey Overview"
    }
  ]
}
[/block]


- [Node Stats Tab](doc:node-stats-1): Displays stats for each Node.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/09514a56bd3dd3f6a6ab02828a90afaba271a09c7c53e42976f322539160eb42-Journey_Node_Stats.png",
        "View node stats",
        2718
      ],
      "align": "center",
      "sizing": "100% ",
      "border": true,
      "caption": "Node Stats"
    }
  ]
}
[/block]


- [Engagement Stats Tab](doc:engagement-stats): Displays stats for the Engagement.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8ccea81f0a5cde597cf9a57c1fcc7e05843eb9d8481f7ea0952c8138dfd1ee0a-Journey_Enagagement_Stats.png",
        null,
        "Engagement Stats"
      ],
      "align": "center",
      "border": true,
      "caption": "Engagement Stats"
    }
  ]
}
[/block]


- [Journey Stats Tab](doc:journey-stats-1): Displays stats for the Journey.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9b5c4909500e5f4a3f3fba73c035f49a8d049c1e22ceb8864cab4fa57d240718-Journey_Stats.png",
        "View Journey stats",
        2718
      ],
      "align": "center",
      "sizing": "100% ",
      "border": true,
      "caption": "Journey Stats"
    }
  ]
}
[/block]


# Frequently asked questions

### Why do my users not qualify?

Check if your user matches all the entry-level segments in the initial node.  
If it is an action, check if the event is from API. If yes, then check if you are passing the event in real-time or in batches. Passing the event with a backdated timestamp will not qualify users in a live-action.

### What are the last nodes?

These are the nodes without an output path, which are present in Journeys without goals. 

### What happens to my users if my Journey does not have a goal?

If you do not set a goal, the users from the last node exit the Journey. Their Journey is considered complete when they reach the last node. 

### Where can I see the users who are waiting because of delay or sleep defined between two nodes?

You will see them on the following node under 'Waiting users'. 

### What are _Unreachable_ profiles?

_Unreachable_ profiles are profiles that do not have any identity, email, phone, or token (web/ push).

### What happens to Unreachable profiles if they reach the last engagement node?

If the Journey Goal is set up, _Unreachable_ profiles move to _Waiting users_ > _Before Node_ stats.  
If the Journey Goal is not set up, _Unreachable_ profiles exit the journey.

### Why is the number of users on nodes not matching or adding up?

The count of users depends on the selected date range. If the original date range of the Journey does not match the date range in your search, then the numbers will differ from the original. 

### How do I verify the number of users entering a specific node?

The number of users moving forward from a node will always match the number of users who are entering the following nodes.

### Why do my stats at the last node not match?

In the Journeys created before Dec 27, 2019, You might see a mismatch of user counts or a drop in users. This is because earlier we used to have a dummy _wait_ step after the last node, where users will move and wait for the goal to be met. In the new Journeys (created post-Dec 27, 2019), the dummy step no longer exists, and there is no mismatch. 

### What is this intermediate stat on node stat?

If you draw the same connector, such as 'Yes',  multiple times from a node and connect it to multiple Segment nodes, the users will move after the first action.  The stats for these Waiting users are displayed as an intermediate node on the connector.  

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e0d470f-Journeys_multiple_Yes_Build.png",
        "Journeys stats for multiple Yes build",
        785
      ],
      "align": "center",
      "border": true,
      "caption": "Intermediate Node - Build"
    }
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/960c1b8-Journeys_Multile_Yes_Node_stats.png",
        "Journeys stats for intermediate node",
        1080
      ],
      "align": "center",
      "border": true,
      "caption": "Intermediate Node - Stats"
    }
  ]
}
[/block]


### How will I see the stats for the Phantom node?

A Phantom node appears only when a _Viewed_ or _Clicked_ connector is drawn from an Engage node. The originating node will display the Sent count, and the Phantom node will display the Clicked or Viewed count. For more information on Phantom nodes, refer to [Users waiting at Engage nodes](https://docs.clevertap.com/docs/journeys#section-users-waiting-at-segment-node).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/af5a2ea-Journeys_Pseudo_Node.png",
        "Journeys stats for Phantom node",
        1162
      ],
      "align": "center",
      "border": true,
      "caption": "Phantom Node - Build"
    }
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8fac40f-Journeys_Pseudo_Node_Stats.png",
        "Journeys stats for Phantom node",
        839
      ],
      "align": "center",
      "border": true,
      "caption": "Phantom Node - Stats"
    }
  ]
}
[/block]