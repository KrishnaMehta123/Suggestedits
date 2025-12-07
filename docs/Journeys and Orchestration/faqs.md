---
title: Journey FAQs
excerpt: Frequently asked Questions related to Journeys
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
## Frequently asked questions

Q. Why do my users not qualify?
A. If the entry node is an action node, but the events are coming from an API, then the users associated with these events do not qualify.

Q. What are last nodes?
A. These are the nodes that do not have an output path. These nodes are present in Journeys without goals. 

Q. What happens to my users if my Journey does not have a goal? 
A. If you do not set a goal, the users from the last node exit the Journey. Their Journey is considered complete when they reach the last node. 

Q. Where can I see the users who are waiting because of delay or sleep defined between two nodes? 
A. You will see them on the following node under 'Waiting users'. 

Q. Why is the number of users on nodes not matching or adding up? 
A. The count of the users depends on the selected date range. If the original date range of the Journey does not match with the date range in your search, then the numbers will differ from the original. 

Q. How do I verify the number of users entering a specific node?
A. The number of users moving forward from a node will always match the number of users who are entering the following nodes.

Q. Why my stats at last node are not matching? 
A. In the journeys created before Dec 27, 2019, You might see a mismatch of user counts or a drop in users. This is because earlier we used to have a dummy wait step post last node, where users will move and wait for goal to be met. In the new journeys (created post Dec 27, 2019), the dummy step no longer exists and this mismatch should not happen. 

Q. What is this intermediate stat on node stat?
A. If you draw the same connector, such as 'Yes',  multiple times from a node and connect it to multiple Segment nodes, the users will move after the first action.  The stats for these Waiting users are displayed as an intermediate node on the connector.  
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e0d470f-Journeys_multiple_Yes_Build.png",
        "Journeys_multiple_Yes_Build.png",
        785,
        430,
        "#f5f1f0"
      ],
      "border": true,
      "caption": "Intermediate node - Build"
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
        "Journeys_Multile_Yes_Node_stats.png",
        1080,
        553,
        "#faf9fa"
      ],
      "border": true,
      "caption": "Intermediate node - Stats"
    }
  ]
}
[/block]

Q. How will I see the stats for the Phantom node?
A.  A Phantom node appears only when a *Viewed* or *Clicked* connector is drawn from an Engage node. The originating node will display the Sent count and the Phantom node will display the Clicked or Viewed count. For more information on Phantom nodes, see [Users waiting at Engage nodes](https://docs.clevertap.com/docs/journeys#section-users-waiting-at-segment-node).


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/af5a2ea-Journeys_Pseudo_Node.png",
        "Journeys_Pseudo_Node.png",
        1162,
        243,
        "#f2f4f1"
      ],
      "caption": "Phantom node - Build"
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
        "Journeys_Pseudo_Node_Stats.png",
        839,
        223,
        "#f5f5f6"
      ],
      "caption": "Phantom node - Stats"
    }
  ]
}
[/block]
Q. What are the different journey types in the past behavior segment?
A. One Time Journey is the type of journey that runs only for one time at the start time of the journey. Here there is no option to re-enter for the users who have exited the journey through journey timeout, force exit, or Goal completed. New users will not be added after the journey ran its course on the start time.

Multiple Dates Journey is the type of journey that will run on the multiple dates selected by you. You get to select the journey end time as per your use case for the journey. In this type of journey, the users can re-enter if the option of Allow users to re-enter the journey is selected.

The recurring journey is the type of journey that will repeatedly run and allow entry to new users on the criteria selected by you under the Repeat section. The first run would be as soon as you publish the Journey. The next runs will be according to the selected criteria. The users once exited can re-enter the journey if the option of Allow users to re-enter the journey is selected.

https://docs.clevertap.com/docs/journeys#section-past-behavior-segments-journey-qualification