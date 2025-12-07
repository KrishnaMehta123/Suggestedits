---
title: Journey components
excerpt: >-
  Understand how to define Journey constituents like nodes, links, and sleep
  time
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
  pages:
    - type: link
      title: Building a Journey
      url: https://docs.clevertap.com/docs/construct-a-journey_c20
---
# Overview

A Journey is configured using a combination of 

* [Nodes](https://docs.clevertap.com/docs/journey-components_c20#journey-nodes-nodes)
* [Connections](https://docs.clevertap.com/docs/journey-components_c20#journey-connections)

## Journey Nodes ![Nodes](https://files.readme.io/18ff72b-Segment_Node_icon.png)

Nodes are different entry and exit points for user navigation.\
The user navigates from a milestone to the intended one through different nodes, depending on the route they take.\
For example, you want the user to register and purchase a product on your platform after installing the app. When the user registers on your platform after app installation, a journey to purchase a product activates. However, if the user does not register on your platform even after app installation, you can activate a journey that nudges them to register on the platform.\
Nodes make it possible to automatically detect the route that the user takes, in order to steer them to the next relevant node.

A Journey is a combination of *Segment* nodes and *Engagement* nodes. You can connect *Segment* nodes and *Engagement* nodes to each other to create powerful automation.\
When compared with Campaigns, the *Segment* nodes define the audience, and *Engagement* nodes define the target. 

### Segment nodes

*Segment* nodes are various points in a journey to qualify users based on certain events.\
The events may be either entry or navigation points based on the user's action/inaction.\
In case of users not qualifying for a *Segment*, they may either be waiting for qualification or exit the journey, if entered.\
For example, on a successful login creation after installing the app, the user qualifies for a *registered* event. In cases where the user does not create a login, they do not qualify, and based on the journey parameters, they either wait to enter the node or exit the journey.

<Image title="Segments_Journey_Components.png" alt={203} className="border" border={true} src="https://files.readme.io/df13128-Segments_Journey_Components.png" />

#### Types of Segment Nodes

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Segment Node
      </th>

      <th>
        Description
      </th>

      <th>
        Example
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Action
      </td>

      <td>
        Qualification to this node occurs as soon as the user performs the said event.
      </td>

      <td>
        Qualify users as soon as they do *app install*.
      </td>
    </tr>

    <tr>
      <td>
        Inaction
      </td>

      <td>
        Segment users who did the first/initial event, but did not do the second event within a specified time interval.
      </td>

      <td>
        Qualify users who *added to cart*, but did not purchase within five mins.
      </td>
    </tr>

    <tr>
      <td>
        Past Behavior
      </td>

      <td>
        Segment users who performed one event AND did not perform another in the past *n* days.
      </td>

      <td>
        Qualify users who performed *Video Watched* AND did not do *Subscription Paid* in the last 30 days.
      </td>
    </tr>

    <tr>
      <td>
        Date Time
      </td>

      <td>
        Segment users based on a *date time* property value like flight time, due date, travel time, and so on.
      </td>

      <td>
        Qualify users who have their credit card due date in the upcoming week.
      </td>
    </tr>

    <tr>
      <td>
        Journey Trigger
      </td>

      <td>
        * \*Use this node only in the entry criteria\*\*.\
          Segment users based on a different user journey node.
      </td>

      <td>
        Qualify users in current journey when they enter *X* node of another journey.\
        For instance, all users who have received nudges based on *Video Watched* and *Subscription not paid* enter the current journey that offers discount codes for subscribing.̧
      </td>
    </tr>

    <tr>
      <td>
        Custom list
      </td>

      <td>
        * \*Use this node only in the entry criteria\*\*.\
          Upload custom list of users for entry to the Journey.
      </td>

      <td>
        Qualify users based on an uploaded list from your Retail Point of Sale (POS).
      </td>
    </tr>

    <tr>
      <td>
        Page Visit
      </td>

      <td>
        * \*Web based segment\*\*.\
          Segment users as soon as they visit a specific page.
      </td>

      <td>
        Qualify users as soon as they visit a specific page.
      </td>
    </tr>

    <tr>
      <td>
        Referrer Entry
      </td>

      <td>
        * \*Web based segment\*\*.\
          Segment users based on a referring website or campaign.
      </td>

      <td>
        Qualify users as soon as they enter your website based on a referring website or campaign.
      </td>
    </tr>

    <tr>
      <td>
        Page Count
      </td>

      <td>
        * \*Web based segment\*\*.\
          Segment users based on the number of pages visited by them.
      </td>

      <td>
        Qualify users as soon as they visit *X* pages.
      </td>
    </tr>
  </tbody>
</Table>

### Engagement Nodes

*Engagement* nodes are interaction points in a user journey that determine the channel and its message contents. The interaction points are users engaging with nudges/notifications sent to them. Users that do not interact with engagements do not qualify.\
For example, you can qualify users when they click a link in an email to indicate interaction. This enables further engagement to prompt certain user actions.

<Image title="Engagement_Journey_Components.png" alt={192} className="border" border={true} src="https://files.readme.io/b123263-Engagement_Journey_Components.png" />

#### Types of Engagement nodes

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Engagement Node
      </th>

      <th>
        Description
      </th>

      <th>
        Node Actions
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Push
      </td>

      <td>
        Send push notifications that display in the users' notification tray or the notification inbox.
      </td>

      <td>
        * Sent
        * Failed
        * Clicked
        * Unreachable 
      </td>
    </tr>

    <tr>
      <td>
        SMS
      </td>

      <td>
        Send text messages to your app or website users even outside of the app.
      </td>

      <td>
        * Sent
          * Failed
          * Unreachable
      </td>
    </tr>

    <tr>
      <td>
        Email
      </td>

      <td>
        Send emails to your app or website users
      </td>

      <td>
        * Sent
        * Failed
        * Viewed
        * Clicked
        * Unreachable 
      </td>
    </tr>

    <tr>
      <td>
        Webhook
      </td>

      <td>
        Receive push notifications on app server when monitored events happen.
      </td>

      <td>
        * Sent
      </td>
    </tr>

    <tr>
      <td>
        Web Push
      </td>

      <td>
        Send browser-based messages  to your website users even outside of your website.
      </td>

      <td>
        * Sent
          * Failed
          * Viewed
          * Clicked
          * Unreachable
      </td>
    </tr>

    <tr>
      <td>
        Web Pop-up
      </td>

      <td>
        Display pop-up messages on desktop or mobile websites.
      </td>

      <td>
        * Sent
          * Viewed
          * Clicked
      </td>
    </tr>

    <tr>
      <td>
        Whatsapp
      </td>

      <td>
        Send Whatsapp messages to your app or website users even outside of the app.

        To know more, refer [Engagement Nodes - Whatsapp](doc:engagement-nodes-whatsapp)
      </td>

      <td>
        * Sent
        * Failed
        * Delivered
        * Unreachable 
      </td>
    </tr>

    <tr>
      <td>
        Exit Intent
      </td>

      <td>
        Display pop-up messages before users leave your website
      </td>

      <td>
        * Sent
        * Viewed
        * Clicked 
      </td>
    </tr>

    <tr>
      <td>
        In-app
      </td>

      <td>
        Display pop-up messages while a user is in the app.
      </td>

      <td>
        * Viewed
          * Clicked
      </td>
    </tr>

    <tr>
      <td>
        Inbox
      </td>

      <td>
        Send messages that remain accessible after they’re received in the app.
      </td>

      <td>
        * Sent
        * Viewed
        * Clicked 
      </td>
    </tr>

    <tr>
      <td>
        Facebook
      </td>

      <td>
        Send messages to users outside of your app or website, via ads on Facebook.
      </td>

      <td>
        * Sent
        * Failed
        * Unreachable 
      </td>
    </tr>

    <tr>
      <td>
        Google
      </td>

      <td>
        Send messages to users outside of your app or website, via ads on Google apps.
      </td>

      <td>
        * Sent
        * Failed
        * Unreachable 
      </td>
    </tr>

    <tr>
      <td>
        Amazon event bridge
      </td>

      <td>
        Interact with Amazon EventBridge(if integrated) to send user action-based notifications.
      </td>

      <td>
        Sent
      </td>
    </tr>

    <tr>
      <td>
        Segment
      </td>

      <td>
        Interact with Segment(if integrated) to personalize engagements based on user actions.
      </td>

      <td>
        Sent
      </td>
    </tr>

    <tr>
      <td>
        mParticle
      </td>

      <td>
        Interact with mParticle(if integrated) to collect user data for rich engagements.
      </td>

      <td>
        Sent
      </td>
    </tr>
  </tbody>
</Table>

### Controller Nodes

*Controller* Nodes are points in a user journey that perform certain actions. For example, you may exit a user from a journey on completion of an *Email Engagement*.

<Image title="Controller_Journey_Components.png" alt={188} className="border" border={true} src="https://files.readme.io/840aead-Controller_Journey_Components.png" />

#### Types of Controller Nodes

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Controller Node
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Force exit
      </td>

      <td>
        Exit a user from a journey.
      </td>
    </tr>

    <tr>
      <td>
        User profile update
      </td>

      <td>
        Update a system or custom user property.
      </td>
    </tr>

    <tr>
      <td>
        A/B Test
      </td>

      <td>
        Define different paths for the user to take.
      </td>
    </tr>
  </tbody>
</Table>

## Journey Connections

You can connect your journey nodes through *links* and specify a *sleep time* before an action. 

### Journey Links

Journey links are routing rules between different nodes. Based on user behavior or action, you can create a connection between a node and link it to distinct nodes.\
For example, when you send push notifications to nudge buying for a segment of new users within the past year but have not purchased anything in the past month, you create a link between the segment node *Past behavior* and the engagement node *Push*.

<Image title="Link_Sleep_Time.png" alt={596} className="border" border={true} src="https://files.readme.io/ddd50bf-Link_Sleep_Time.png" />

### Sleep Time

Sleep Time enables you to specify whether to do the specified action immediately or after a gap. You may define the gap in minutes, hours or days.\
In the above example, you may choose to send the nudge either immediately, as soon as the user qualifies, or wait for a few days before nudging the user.\
Click the **hourglass** ![\*\*hourglass\*\*](https://files.readme.io/edc6717-Hourglass.png) to modify the sleep time. By default, there's no sleep time.

<Image title="Sleep_Time_Journey_Components.png" alt={449} className="border" border={true} src="https://files.readme.io/1c0073a-Sleep_Time_Journey_Components.png" />
