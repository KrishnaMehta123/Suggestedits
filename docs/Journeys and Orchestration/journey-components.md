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
- [Nodes](https://docs.clevertap.com/docs/journey-components_c20#journey-nodes-nodes)
- [Connections](https://docs.clevertap.com/docs/journey-components_c20#journey-connections)

## Journey Nodes ![Nodes](https://files.readme.io/18ff72b-Segment_Node_icon.png)
Nodes are different entry and exit points for user navigation.
The user navigates from a milestone to the intended one through different nodes, depending on the route they take.
For example, you want the user to register and purchase a product on your platform after installing the app. When the user registers on your platform after app installation, a journey to purchase a product activates. However, if the user does not register on your platform even after app installation, you can activate a journey that nudges them to register on the platform. 
Nodes make it possible to automatically detect the route that the user takes, in order to steer them to the next relevant node.

A Journey is a combination of *Segment* nodes and *Engagement* nodes. You can connect *Segment* nodes and *Engagement* nodes to each other to create powerful automation.
When compared with Campaigns, the *Segment* nodes define the audience, and *Engagement* nodes define the target. 

### Segment nodes 
*Segment* nodes are various points in a journey to qualify users based on certain events. 
The events may be either entry or navigation points based on the user's action/inaction. 
In case of users not qualifying for a *Segment*, they may either be waiting for qualification or exit the journey, if entered. 
For example, on a successful login creation after installing the app, the user qualifies for a *registered* event. In cases where the user does not create a login, they do not qualify, and based on the journey parameters, they either wait to enter the node or exit the journey.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/df13128-Segments_Journey_Components.png",
        "Segments_Journey_Components.png",
        203,
        330,
        "#f9f7f7"
      ],
      "border": true
    }
  ]
}
[/block]
#### Types of Segment Nodes
[block:parameters]
{
  "data": {
    "h-0": "Segment Node",
    "h-1": "Description",
    "h-2": "Example",
    "0-0": "Action",
    "0-1": "Qualification to this node occurs as soon as the user performs the said event.",
    "0-2": "Qualify users as soon as they do *app install*.",
    "1-0": "Inaction",
    "2-0": "Past Behavior",
    "3-0": "Date Time",
    "4-0": "Journey Trigger",
    "4-1": "**Use this node only in the entry criteria**.\nSegment users based on a different user journey node.",
    "4-2": "Qualify users in current journey when they enter *X* node of another journey. \nFor instance, all users who have received nudges based on *Video Watched* and *Subscription not paid* enter the current journey that offers discount codes for subscribing.̧",
    "6-0": "Page Visit",
    "7-0": "Referrer Entry",
    "8-0": "Page Count",
    "1-1": "Segment users who did the first/initial event, but did not do the second event within a specified time interval.",
    "1-2": "Qualify users who *added to cart*, but did not purchase within five mins.",
    "2-1": "Segment users who performed one event AND did not perform another in the past *n* days.",
    "2-2": "Qualify users who performed *Video Watched* AND did not do *Subscription Paid* in the last 30 days.",
    "3-1": "Segment users based on a *date time* property value like flight time, due date, travel time, and so on.",
    "3-2": "Qualify users who have their credit card due date in the upcoming week.",
    "6-1": "**Web based segment**.\nSegment users as soon as they visit a specific page.",
    "7-1": "**Web based segment**.\nSegment users based on a referring website or campaign.",
    "8-1": "**Web based segment**.\nSegment users based on the number of pages visited by them.",
    "6-2": "Qualify users as soon as they visit a specific page.",
    "7-2": "Qualify users as soon as they enter your website based on a referring website or campaign.",
    "8-2": "Qualify users as soon as they visit *X* pages.",
    "5-0": "Custom list",
    "5-1": "**Use this node only in the entry criteria**.\nUpload custom list of users for entry to the Journey.",
    "5-2": "Qualify users based on an uploaded list from your Retail Point of Sale (POS)."
  },
  "cols": 3,
  "rows": 9
}
[/block]
### Engagement Nodes
*Engagement* nodes are interaction points in a user journey that determine the channel and its message contents. The interaction points are users engaging with nudges/notifications sent to them. Users that do not interact with engagements do not qualify.  
For example, you can qualify users when they click a link in an email to indicate interaction. This enables further engagement to prompt certain user actions.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b123263-Engagement_Journey_Components.png",
        "Engagement_Journey_Components.png",
        192,
        461,
        "#f9fbfb"
      ],
      "border": true
    }
  ]
}
[/block]
#### Types of Engagement nodes
[block:parameters]
{
  "data": {
    "h-0": "Engagement Node",
    "h-1": "Description",
    "h-2": "Node Actions",
    "0-0": "Push",
    "1-0": "SMS",
    "2-0": "Email",
    "3-0": "Webhook",
    "4-0": "Web Push",
    "5-0": "Web Pop-up",
    "7-0": "Exit Intent",
    "8-0": "In-app",
    "9-0": "Inbox",
    "10-0": "Facebook",
    "11-0": "Google",
    "12-0": "Amazon event bridge",
    "13-0": "Segment",
    "14-0": "mParticle",
    "0-1": "Send push notifications that display in the users' notification tray or the notification inbox.",
    "0-2": "  * Sent\n  * Failed\n  * Clicked\n  * Unreachable ",
    "1-1": "Send text messages to your app or website users even outside of the app.",
    "1-2": "* Sent\n  * Failed\n  * Unreachable",
    "2-1": "Send emails to your app or website users",
    "2-2": "  * Sent\n  * Failed\n  * Viewed\n  * Clicked\n  * Unreachable ",
    "3-1": "Receive push notifications on app server when monitored events happen.",
    "3-2": "* Sent",
    "4-1": "Send browser-based messages  to your website users even outside of your website.",
    "4-2": "* Sent\n  * Failed\n  * Viewed\n  * Clicked\n  * Unreachable",
    "5-1": "Display pop-up messages on desktop or mobile websites.",
    "7-1": "Display pop-up messages before users leave your website",
    "8-1": "Display pop-up messages while a user is in the app.",
    "9-1": "Send messages that remain accessible after they’re received in the app.",
    "10-1": "Send messages to users outside of your app or website, via ads on Facebook.",
    "11-1": "Send messages to users outside of your app or website, via ads on Google apps.",
    "12-1": "Interact with Amazon EventBridge(if integrated) to send user action-based notifications.",
    "13-1": "Interact with Segment(if integrated) to personalize engagements based on user actions.",
    "14-1": "Interact with mParticle(if integrated) to collect user data for rich engagements.",
    "5-2": "* Sent\n  * Viewed\n  * Clicked",
    "6-0": "Whatsapp",
    "6-1": "Send Whatsapp messages to your app or website users even outside of the app.\n\nTo know more, refer [Engagement Nodes - Whatsapp](doc:engagement-nodes-whatsapp)",
    "6-2": "  * Sent\n  * Failed\n  * Delivered\n  * Unreachable ",
    "7-2": "  * Sent\n  * Viewed\n  * Clicked ",
    "8-2": "* Viewed\n  * Clicked",
    "9-2": "  * Sent\n  * Viewed\n  * Clicked ",
    "10-2": "  * Sent\n  * Failed\n  * Unreachable ",
    "11-2": "  * Sent\n  * Failed\n  * Unreachable ",
    "12-2": "Sent\n ",
    "13-2": "Sent",
    "14-2": "Sent"
  },
  "cols": 3,
  "rows": 15
}
[/block]
### Controller Nodes
*Controller* Nodes are points in a user journey that perform certain actions. For example, you may exit a user from a journey on completion of an *Email Engagement*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/840aead-Controller_Journey_Components.png",
        "Controller_Journey_Components.png",
        188,
        147,
        "#fafafa"
      ],
      "border": true
    }
  ]
}
[/block]
####Types of Controller Nodes
[block:parameters]
{
  "data": {
    "h-0": "Controller Node",
    "h-1": "Description",
    "h-2": "Description",
    "0-0": "Force exit",
    "1-0": "User profile update",
    "2-0": "A/B Test",
    "0-1": "Exit a user from a journey.",
    "1-1": "Update a system or custom user property.",
    "2-1": "Define different paths for the user to take."
  },
  "cols": 2,
  "rows": 3
}
[/block]
## Journey Connections
You can connect your journey nodes through *links* and specify a *sleep time* before an action. 

###Journey Links
Journey links are routing rules between different nodes. Based on user behavior or action, you can create a connection between a node and link it to distinct nodes. 
For example, when you send push notifications to nudge buying for a segment of new users within the past year but have not purchased anything in the past month, you create a link between the segment node *Past behavior* and the engagement node *Push*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ddd50bf-Link_Sleep_Time.png",
        "Link_Sleep_Time.png",
        596,
        216,
        "#ede2de"
      ],
      "border": true
    }
  ]
}
[/block]
###Sleep Time
Sleep Time enables you to specify whether to do the specified action immediately or after a gap. You may define the gap in minutes, hours or days.
In the above example, you may choose to send the nudge either immediately, as soon as the user qualifies, or wait for a few days before nudging the user.
Click the **hourglass** ![**hourglass**](https://files.readme.io/edc6717-Hourglass.png) to modify the sleep time. By default, there's no sleep time.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1c0073a-Sleep_Time_Journey_Components.png",
        "Sleep_Time_Journey_Components.png",
        449,
        496,
        "#f2f3fa"
      ],
      "border": true
    }
  ]
}
[/block]