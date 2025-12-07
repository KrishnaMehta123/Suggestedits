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

The ID mentioned at the node is the sequence number of the node.\
Each step is indicated by an ID on the top right corner of the pertinent node.

Click the **Node Stats** tab. Select the date range from the calendar. The following section show how to check the statistics for each of the node types:

## Entry Node

This is the first node in the Journey. There can be only one Entry node. An Entry node can only be a Segment node.

<Image alt="Entry Node" align="center" border={true} src="https://files.readme.io/53a486bcfdb0d168359b16576f77015010e37eff2d252b2d9c8a9ccbb45dedb6-image.png">
  Entry Node
</Image>

| Stat            | Description                                                                                                                                                                                                                                                                        |
| :-------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Qualified       | The total number of users who qualified for the journey. This stat is available only on the entry node.                                                                                                                                                                            |
| Entered Journey | The users who have entered a Journey via node connectors, such as Yes or No.                                                                                                                                                                                                       |
| Control Group   | The number of users who were marked for the control group. A control group is a set of users who do not receive any marketing campaigns. You can measure the effectiveness of your initiatives by comparing this group with the target group of users who received your campaigns. |

## Segment Nodes

<Image title="Segment node for Journeys" alt={316} align="center" border={true} src="https://files.readme.io/5a1ed63-Journeys_node_Segment.png">
  Segment node
</Image>

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        <p>Stat</p>
      </th>

      <th>
        <p>Description</p>
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>Entered Node</p>
      </td>

      <td>
        <p>The total number of users who entered the node. It includes the sum of all the users from Moved forward, Waiting users, Goal Met, and Journey timeout.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Moved forward</p>
      </td>

      <td>
        <p>The users who have moved forward via node connectors, such as Yes, No, or Node Timeout.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Waiting users</p>
      </td>

      <td>
        <p>The users waiting at a node to qualify. The users may wait for either of two reasons: </p><ul><li>Delay from a previous node</li><li>Waiting to perform an action</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Goal Met</p>
      </td>

      <td>
        <p>These users have performed the intended goal, such as viewing a movie or purchasing a product.</p><ul><li><em>Before Node</em><br />Indicates that the user achieved the goal while waiting on the delay path but did not get a message from the next node.</li><li><em>At Node</em><ul><li>Indicates that the user is on the node</li><li>If the 'Failed' connector is not connected, the users in this state are counted as <em>At Node.</em></li></ul></li></ul>
      </td>
    </tr>

    <tr>
      <td>
        Journey timeout exits
      </td>

      <td>
        These are the users who exited the Journey after the time duration set for the Journey, that is, Journey Timeout is complete.
      </td>
    </tr>
  </tbody>
</Table>

## Engage Nodes

Simply put, *Engage* nodes are campaigns. You can see the stats of each campaign from the *Node Stats* tab. Click the **Engage** node from the *Nodes Stats* tab to see the campaign statistics. 

<Image title="Engage nodes for Journeys" alt={315} align="center" border={true} src="https://files.readme.io/e443e68-Journeys_nodes_Engage.png">
  Engage Node
</Image>

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        <p>

        Stat

        </p>
      </th>

      <th>
        <p>

        Description

        </p>
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>Entered Node</p>
      </td>

      <td>
        The total number of users who entered the node. It includes the sum of all the users from Moved forward, Waiting users, Goal Met, and Journey timeout.
      </td>
    </tr>

    <tr>
      <td>
        <p>Moved Forward</p>
      </td>

      <td>
        Users who have moved forward via node connectors, such as Sent, Viewed, Clicked, Failed, and Unreachable.\
        Unreachable’ profiles are profiles that do not have any identity, email, phone, or token (web/ push).
      </td>
    </tr>

    <tr>
      <td>
        <p>Waiting users</p>
      </td>

      <td>
        <p>These users may wait for either of two reasons: </p><ul><li><em>Before Node</em><ul><li>Delay from a previous node.</li><li>Unreachable profiles if an Unreachable path is not drawn. </li></ul></li><li><em>At Node</em><br />The outcome for these users is not defined. For example, if the 'Failed' connector is not connected, the users in this state will be counted in the <em>At node.</em></li></ul>
      </td>
    </tr>

    <tr>
      <td>
        <p>Goal Met</p>
      </td>

      <td>
        <p>These users have performed the intended goal, such as viewing a movie or purchasing a product.</p><ul><li><em>Before Node</em><br />Indicates that the user achieved the goal while waiting on the delay path but did not get a message from the next node.</li><li><em>At Node</em><ul><li>Indicates that the user is on the node</li><li>If the <em>Failed</em> connector is not connected, the users in this state are counted in the <em>At node.</em></li></ul></li></ul>
      </td>
    </tr>

    <tr>
      <td>
        Journey timeout exits
      </td>

      <td>
        These are the users who exited the Journey after the time duration set for the Journey, that is, Journey Timeout is complete.
      </td>
    </tr>
  </tbody>
</Table>

> 📘 Campaign Stats
>
> You can view the campaign-level stats for every node. Click the **Engage** node to open the campaign-level stats.

> 📘 Unique Users Converted
>
> If a user enters the journey and performs the conversation event twice, only one conversation event for that unique user is counted.

## Force Exit Node

This node stat shows only the number of force exits.

<Image title="Force exit node for Journeys" alt={310} align="center" border={true} src="https://files.readme.io/200599b-Journeys_node_Force_exit.png">
  Force Exit Node
</Image>
