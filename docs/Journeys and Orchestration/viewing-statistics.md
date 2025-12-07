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

* **Goal Met**: If a goal is set in the Journey builder, these are all users who met the goal. 
* **Journey Timeout** : If a Journey timeout is set in the Journey builder (entry criteria), these are all the users who timed out.
* **Node Timeout** : The qualifying window that is set for the node, after which the users will move on to the next node via the Node timeout connector.
* **Completed**: If a goal is not set in the Journey builder, these are all the users who successfully reached the last node of the Journey.

# Overview

Click *Engage* > *Journeys* from the left side menu. The *Journey List\_page appears. Search for a journey and then click to open a Journey. The \_Journey Canvas* has three tabs:

* **Overview Tab**: Displays your Journey components and connections.

<Image title="Overview of Journey" alt={2718} align="center" width="90% " border={true} src="https://files.readme.io/4ddff52-Journeys_Overview.png">
  Journey Overview
</Image>

* [Node Stats Tab](https://staging.docs.user.clevertap.net/docs/node-stats-1#node-stats): Displays stats for each Node.

<Image title="View node stats" alt={2718} align="center" width="90% " border={true} src="https://files.readme.io/e31e40e-Node_Stats.png">
  Node Stats
</Image>

* [Engagement Stats Tab](https://staging.docs.user.clevertap.net/docs/engagement-stats#overview): Displays stats for the Engagement.

  <Image alt="Engagement Stats" align="center" width="97% " border={true} src="https://files.readme.io/32d91d7d36a9cbef15aded10c76f974a9a645b58e59f36614ce3366a00b21657-new_new_new_.png">
    Engagement Stats
  </Image>
* [Journey Stats Tab](https://staging.docs.user.clevertap.net/docs/journey-stats-1#journey-stats): Displays stats for the Journey.

<Image title="View Journey stats" alt={2718} align="center" width="92% " border={true} src="https://files.readme.io/c8e8bce-Jounrey_Stats.png">
  Journey Stats
</Image>

# Frequently asked questions

Q. Why do my users not qualify?\
A. Check if your user matches all the entry-level segments in the initial node.\
If it is an action, check if the event is from API. If yes, then check if you are passing the event in real-time or in batches. Passing the event with backdated timestamp will not qualify users in a live-action.

Q. What are last nodes?\
A. These are the nodes that do not have an output path. These nodes are present in Journeys without goals. 

Q. What happens to my users if my Journey does not have a goal?\
A. If you do not set a goal, the users from the last node exit the Journey. Their Journey is considered complete when they reach the last node. 

Q. Where can I see the users who are waiting because of delay or sleep defined between two nodes?\
A. You will see them on the following node under 'Waiting users'. 

Q. What are *Unreachable* profiles?\
A. *Unreachable* profiles are profiles that do not have any identity, email, phone, or token (web/ push).

Q. What happens to Unreachable profiles if they reach the last engagement node?\
A. If Journey Goal is set up, *Unreachable* profiles move to *Waiting users* > *Before Node* stats.\
If Journey Goal is not set up, *Unreachable* profiles exit the journey.

Q. Why is the number of users on nodes not matching or adding up?\
A. The count of users depends on the selected date range. If the original date range of the Journey does not match the date range in your search, then the numbers will differ from the original. 

Q. How do I verify the number of users entering a specific node?\
A. The number of users moving forward from a node will always match the number of users who are entering the following nodes.

Q. Why do my stats at the last node do not match?\
A. In the Journeys created before Dec 27, 2019, You might see a mismatch of user counts or a drop in users. This is because earlier we used to have a dummy *wait* step after the last node, where users will move and wait for the goal to be met. In the new Journeys (created post-Dec 27, 2019), the dummy step no longer exists and there is no mismatch. 

Q. What is this intermediate stat on node stat?\
A. If you draw the same connector, such as 'Yes',  multiple times from a node and connect it to multiple Segment nodes, the users will move after the first action.  The stats for these Waiting users are displayed as an intermediate node on the connector.  

<Image title="Journeys stats for multiple Yes build" alt={785} align="center" border={true} src="https://files.readme.io/e0d470f-Journeys_multiple_Yes_Build.png">
  Intermediate Node - Build
</Image>

<Image title="Journeys stats for intermediate node" alt={1080} align="center" border={true} src="https://files.readme.io/960c1b8-Journeys_Multile_Yes_Node_stats.png">
  Intermediate Node - Stats
</Image>

Q. How will I see the stats for the Phantom node?\
A.  A Phantom node appears only when a *Viewed* or *Clicked* connector is drawn from an Engage node. The originating node will display the Sent count and the Phantom node will display the Clicked or Viewed count. For more information on Phantom nodes, see [Users waiting at Engage nodes](https://docs.clevertap.com/docs/journeys#section-users-waiting-at-segment-node).

<Image title="Journeys stats for Phantom node" alt={1162} align="center" border={true} src="https://files.readme.io/af5a2ea-Journeys_Pseudo_Node.png">
  Phantom Node - Build
</Image>

<Image title="Journeys stats for Phantom node" alt={839} align="center" border={true} src="https://files.readme.io/8fac40f-Journeys_Pseudo_Node_Stats.png">
  Phantom Node - Stats
</Image>
