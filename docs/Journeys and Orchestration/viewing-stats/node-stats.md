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

The Node Stats tab shows you the stats for each node. You can account for all users who entered the Journey and their current state.\
The ID mentioned at the node is the sequence number of the node.\
Each step is indicated by an ID on the top right corner of the pertinent node.

Click the **Node Stats** tab. Select the *date range* from the calendar. The following shows how to check the statistics for each of the node types:

## Entry Node

This is the first node in the Journey. There can be only one *Entry* node.  An *Entry* node can only be a *Segment* node. 

<Image title="Journeys_node_Entry.png" alt={317} width="smart" src="https://files.readme.io/f7aca14-Journeys_node_Entry.png">
  Entry node
</Image>

| Stat            | Description                                                                                                                                                                                                                                                                        |
| :-------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Qualified       | The total number of users who qualified for the journey. This stat is available only on the entry node.                                                                                                                                                                            |
| Entered Journey | The users who have entered a Journey via node connectors, such as Yes or No.                                                                                                                                                                                                       |
| Control Group   | The number of users who were marked for the control group. A control group is a set of users who do not receive any marketing campaigns. You can measure the effectiveness of your initiatives by comparing this group with the target group of users who received your campaigns. |

## Segment Nodes

<Image title="Journeys_node_Segment.png" alt={316} src="https://files.readme.io/5a1ed63-Journeys_node_Segment.png">
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
        <p>The users waiting at a node to qualify. The users may wait for either of the 2 reasons: </p><ol><li>Delay from a previous node</li><li>Waiting to perform an action</li></ol>
      </td>
    </tr>

    <tr>
      <td>
        Goal Met
      </td>

      <td>
        These are the users who have performed the intended goal, such as viewing a movie or purchasing a product.
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

<Image title="Journeys_nodes_Engage.png" alt={315} src="https://files.readme.io/e443e68-Journeys_nodes_Engage.png">
  Engage node
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
        <p>Moved Forward</p>
      </td>

      <td>
        <p>The users who have moved forward via node connectors, such as Sent, Viewed, Clicked, Failed, and Unreachable.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>Waiting users</p>
      </td>

      <td>
        <p>These users may wait for either of the 2 reasons: </p><ol><li>Before Node: Delay from a previous node</li><li>At Node: The outcome for these users is not defined. For example, if the 'Failed' connector is not connected, the users in this state will be counted in ‘At node.’</li></ol>
      </td>
    </tr>

    <tr>
      <td>
        Goal Met
      </td>

      <td>
        These are the users who have performed the intended goal, such as viewing a movie or purchasing a product.
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

> 📘 Campaign Reports
>
> You can view the [Campaign Reports](doc:campaign-reports) from the Engage node. Click the **Engage** node to open the campaign report.

## Force Exit Node

This node stat shows only the number of force exits.

<Image title="Journeys_node_Force_exit.png" alt={310} src="https://files.readme.io/200599b-Journeys_node_Force_exit.png">
  Force exit node
</Image>
