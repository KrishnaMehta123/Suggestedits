---
title: Journey Performance
excerpt: Understand the metrics used to track your Journey's performance.
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
Click *Journeys* from the left pane. The *Journey List* page appears. Select to open a Journey.  
The Journey ID is available on the top left of the Journey Stats page.
The *Journey Canvas* has three tabs:
- Overview - Shows your Journey configuration including the setup, nodes, and links between them.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ab9c712-Journey_Overview_tab.jpg",
        "Journey_Overview_tab.jpg",
        1031,
        437,
        "#f4f6f8"
      ],
      "border": true,
      "caption": ""
    }
  ]
}
[/block]
- Node Stats - Shows the following stats for each node 
  - Users that entered the node
  - Users that moved forward to the next step
  - Users waiting to enter the node
  - Users waiting to move forward
  - Users exiting because of a journey timeout
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/412b022-Journey_Node_Stats_Tab.jpg",
        "Journey_Node_Stats_Tab.jpg",
        785,
        574,
        "#f5f5f7"
      ],
      "caption": "",
      "border": true
    }
  ]
}
[/block]
- Journey Stats - Shows the stats for the Journey
  - Goal Met - Number of users who met the goal. For example, the number of users that achieved the goal of registering on the platform, if the journey goal is to increase user registrations. For more information on goals, refer to [Define Goals](doc:define-goals)
  - Journey Timeout -  If a Journey timeout is set in the Journey builder (entry criteria), these are all the users who timed out. For example, the number of qualified users who timed out of the journey. For more information, refer to [Select a Journey Timeout](https://docs.clevertap.com/docs/setup-journey#select-a-journey-timeout)
  - Node Timeout -   The qualifying window that is set for the node, after which the users will move on to the next node via the Node timeout connector. For more information refer to [User flow in Journeys](doc:user-flow-journeys) 
  - Completed -  If a goal is not set in the Journey builder, these are all the users who successfully reached the last node of the Journey. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/29e99b8-Journey_Stats_Tab.jpg",
        "Journey_Stats_Tab.jpg",
        1388,
        578,
        "#f7f7f9"
      ],
      "border": true,
      "caption": "",
      "sizing": "smart"
    }
  ]
}
[/block]