---
title: Journey Concepts
excerpt: >-
  Understand how to define Journey constituents like nodes, links, and sleep
  time.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Journey Components

A Journey is configured using a combination of 

- [Nodes](https://docs.clevertap.com/docs/journey-components#journey-nodes-nodes)
- [Connections](https://docs.clevertap.com/docs/journey-components#journey-connections)

## Journey Nodes

Nodes are different entry and exit points for user navigation. The user navigates from a milestone to the intended one through different nodes, depending on the route they take. For example, you want the user to register and purchase a product on your platform after installing the app. When the user registers on your platform after app installation, a journey to purchase a product activates. However, if the user does not register on your platform even after app installation, you can activate a journey that nudges them to register on the platform. Nodes make it possible to automatically detect the route that the user takes, in order to steer them to the next relevant node.

A Journey is a combination of _Segment_ nodes and _Engagement_ nodes. You can connect _Segment_ nodes and _Engagement_ nodes to each other to create powerful automation.  
When compared with Campaigns, the _Segment_ nodes define the audience, and _Engagement_ nodes define the target. 

### Segment Nodes

_Segment_ nodes are various points in a journey to qualify users based on certain events.  
The events may be either entry or navigation points based on the user's action/inaction.  
In case of users not qualifying for a _Segment_, they may either be waiting for qualification or exit the journey, if entered.  
For example, on a successful login creation after installing the app, the user qualifies for a _registered_ event. In cases where the user does not create a login, they do not qualify, and based on the journey parameters, they either wait to enter the node or exit the journey.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/df13128-Segments_Journey_Components.png",
        "Various segment nodes in Journeys",
        203
      ],
      "align": "center",
      "border": true,
      "caption": "Segment Nodes"
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
    "0-2": "Qualify users as soon as they do _app install_.",
    "1-0": "Inaction",
    "1-1": "Segment users who did the first/initial event, but did not do the second event within a specified time interval.",
    "1-2": "Qualify users who _added to cart_, but did not purchase within five mins.",
    "2-0": "Past Behavior",
    "2-1": "Segment users who performed one event AND did not perform another in the past _n_ days.",
    "2-2": "Qualify users who performed _Video Watched_ AND did not do _Subscription Paid_ in the last 30 days.",
    "3-0": "Date Time",
    "3-1": "Segment users based on a _date time_ property value like flight time, due date, travel time, and so on.",
    "3-2": "Qualify users who have their credit card due date in the upcoming week.",
    "4-0": "Journey Trigger",
    "4-1": "**Use this node only in the entry criteria**.  \nSegment users based on a different user journey node.",
    "4-2": "Qualify users in current journey when they enter _X_ node of another journey.  \nFor instance, all users who have received nudges based on _Video Watched_ and _Subscription not paid_ enter the current journey that offers discount codes for subscribing.̧",
    "5-0": "Custom list",
    "5-1": "**Use this node only in the entry criteria**.  \nUpload custom list of users for entry to the Journey.",
    "5-2": "Qualify users based on an uploaded list from your Retail Point of Sale (POS).",
    "6-0": "Page Visit",
    "6-1": "**Web based segment**.  \nSegment users as soon as they visit a specific page.",
    "6-2": "Qualify users as soon as they visit a specific page.",
    "7-0": "Referrer Entry",
    "7-1": "**Web based segment**.  \nSegment users based on a referring website or campaign.",
    "7-2": "Qualify users as soon as they enter your website based on a referring website or campaign.",
    "8-0": "Page Count",
    "8-1": "**Web based segment**.  \nSegment users based on the number of pages visited by them.",
    "8-2": "Qualify users as soon as they visit _X_ pages."
  },
  "cols": 3,
  "rows": 9,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


#### Node Timeout for PBS and Action Segment

Let's understand how Node Timeout works in the Past Behaviour and Action segments. Consider the following scenario where the user performs event A but does not complete event B within 1 minute:

**If node timeout is not defined**: 

- the users who qualify for the next node move forward via the Yes path immediately.
- the non-qualified users move forward via the No path. 

**If node timeout is defined:**

- the users who qualify for the next node move forward via the Yes path immediately.
- the users who did not complete the action within the defined node timeout period will be evaluated every 1-hour timeframe.
- the users' movement via node timeout to subsequent nodes will always be **\<=1** hour as the time depends on when the user falls within the 1-hour timeframe.

### Engagement Nodes

_Engagement_ nodes are interaction points in a user journey that determine the channel and its message contents. The interaction points are users engaging with nudges/notifications sent to them. Users that do not interact with engagements do not qualify.  
For example, you can qualify users when they click a link in an email to indicate interaction. This enables further engagement to prompt certain user actions.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/de9c6a32f3c1859a555eee62f5f9db03f87518731adb3cd2ad553ed8006ecfc9-Engagement_Nodes.png",
        "Various engagement nodes in Journeys",
        406
      ],
      "align": "center",
      "sizing": "smart",
      "border": true,
      "caption": "Engagement Nodes"
    }
  ]
}
[/block]


#### Types of Engagement Nodes

| Engagement Node     | Description                                                                                                                                                                                                                                                             | Node Actions                                                                                    |
| :------------------ | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------- |
| Push                | Send push notifications that display in the users' notification tray or the notification inbox.                                                                                                                                                                         | <ul> <li>Sent</li> <li>Failed</li> <li>Clicked</li> <li>Unreachable </li> </ul>                 |
| SMS                 | Send text messages to your app or website users even outside of the app.                                                                                                                                                                                                | <ul> <li>Sent</li> <li>Failed</li> <li>Unreachable</li> </ul>                                   |
| Email               | Send emails to your app or website users                                                                                                                                                                                                                                | <ul> <li>Sent</li> <li>Failed</li> <li>Viewed</li> <li>Clicked</li> <li>Unreachable </li> </ul> |
| Webhook             | Webhooks serve many purposes. It includes receiving push notifications on the app server and tracking events in a system. Chatbots and virtual assistants use it to connect with external services. It enables them to exchange data when responding to user inquiries. | <ul> <li>Sent</li> </ul>                                                                        |
| Web Push            | Send browser-based messages to your website users even outside of your website.                                                                                                                                                                                         | <ul> <li>Sent</li> <li>Failed</li> <li>Viewed</li> <li>Clicked</li> <li>Unreachable</li> </ul>  |
| Web Pop-up          | Display pop-up messages on desktop or mobile websites.                                                                                                                                                                                                                  | <ul> <li>Sent</li> <li>Viewed</li> <li>Clicked</li> </ul>                                       |
| WhatsApp            | Send WhatsApp messages to your app or website users even outside of the app. To know more, refer to [Engagement Nodes - WhatsApp](doc:engagement-nodes-whatsapp)                                                                                                        | <ul> <li>Sent</li> <li>Failed</li> <li>Delivered</li> <li>Unreachable </li> </ul>               |
| Exit Intent         | Display pop-up messages before users leave your website                                                                                                                                                                                                                 | <ul> <li>Sent</li> <li>Viewed</li> <li>Clicked</li> </ul>                                       |
| In-app              | Display pop-up messages while a user is in the app. An In-App renders as soon as the user performs an event.                                                                                                                                                            | <ul> <li>Viewed</li> <li>Clicked</li> </ul>                                                     |
| Web Native Display  | Display content on your website without interrupting the user journey.                                                                                                                                                                                                  | <ul> <li>Viewed</li> <li>Clicked</li> </ul>                                                     |
| Inbox               | Send messages that remain accessible after they’re received in the app.                                                                                                                                                                                                 | <ul> <li>Sent</li> <li>Viewed</li> <li>Clicked </li> </ul>                                      |
| Facebook            | Send messages to users outside of your app or website via ads on Facebook.                                                                                                                                                                                              | <ul> <li>Sent</li> <li>Failed</li> <li>Unreachable </li> </ul>                                  |
| Google              | Send messages to users outside your app or website via ads on Google apps.                                                                                                                                                                                              | <ul> <li>Sent</li> <li>Failed</li> <li>Unreachable </li> </ul>                                  |
| Amazon event bridge | Interact with Amazon EventBridge(if integrated) to send user action-based notifications.                                                                                                                                                                                | Sent                                                                                            |
| Segment             | Interact with Segment(if integrated) to personalize engagements based on user actions.                                                                                                                                                                                  | Sent                                                                                            |
| mParticle           | Interact with mParticle(if integrated) to collect user data for rich engagements.                                                                                                                                                                                       | Sent                                                                                            |

#### Node Actions

This section explains the status of the message delivery and the actions a user may perform on the engagement node. 

| Node Actions    | Description                                                                                                                                                                                                                |
| :-------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Sent**        | Indicates that the message is sent from CleverTap and has reached the recipient's device. In the case of a Webhook, the recipient is the system server.                                                                    |
| **Failed**      | Indicates that the sent message could not be delivered to its intended recipient due to specific errors. For example, third-party provider issues.                                                                         |
| **Unreachable** | Indicates that the sent message could not be delivered because the recipient's device or contact information is unavailable. For example, a push token or phone number does not exist.                                     |
| **Viewed**      | Indicates that the user viewed the message sent from CleverTap. For example, the user views an Email or In-App notification.                                                                                               |
| **Clicked**     | Indicates that the user clicked the message sent from CleverTap. For example, the user clicks a Push, In-App, Email, Web Popup, or Web Push message.                                                                       |
| **Delivered**   | In WhatsApp, _Sent_ indicates that the message is on its way to the user's device, and _Delivered_ indicates that the message has reached the recipient's device. If the user blocks you, the message does not reach them. |

### Controller Nodes

_Controller_ Nodes are points in a user journey that perform certain actions. For example, you may exit a user from a journey after completing an _Email Engagement_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f72c5b9cad2e508628cae0f6e07bc1e73860e3ddb90e31449c2f46fca14fe026-Journey_Controllers.png",
        null,
        "Journey Controllers"
      ],
      "align": "center",
      "sizing": "40% ",
      "border": true,
      "caption": "Journey Controllers"
    }
  ]
}
[/block]


#### Types of Controller Nodes

| Controller Node     | Description                                                             |
| :------------------ | :---------------------------------------------------------------------- |
| Force exit          | Exit a user from a journey.                                             |
| User profile update | Update a system or custom user property.                                |
| IntelliNODE         | Define and compare multiple journey variations within a single journey. |

## Journey Connections

You can connect your journey nodes through _links_ and specify a _sleep time_ before an action. 

### Journey Links

Journey links are routing rules between different nodes. Based on user behavior or action, you can create a connection between a node and link it to distinct nodes.  
For example, when you send push notifications to nudge buying for a segment of new users within the past year but have not purchased anything in the past month, you create a link between the segment node _Past behavior_ and the engagement node _Push_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ddd50bf-Link_Sleep_Time.png",
        "Journey links used to connect different nodes",
        596
      ],
      "align": "center",
      "border": true,
      "caption": "Journey Links"
    }
  ]
}
[/block]


### Sleep Time

When you choose a journey link and connect it to the engagement node, the **hourglass** ![\*\*hourglass\*\*](https://files.readme.io/edc6717-Hourglass.png) icon appears on the link. Click the **hourglass** ![\*\*hourglass\*\*](https://files.readme.io/edc6717-Hourglass.png) to modify the sleep time. By default, there's no sleep time.

Sleep Time enables you to specify whether to do the specified action immediately or after a gap. You may define the gap in minutes, hours or days.  
In the below figure, you may choose to send the nudge either immediately, as soon as the user qualifies, or wait for a few days before nudging the user.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1c0073a-Sleep_Time_Journey_Components.png",
        "Sleep time component in Journey",
        449
      ],
      "align": "center",
      "border": true,
      "caption": "Sleep Time"
    }
  ]
}
[/block]


> 📘 Note
> 
> The In-App renders as soon as the user performs an event. Hence, sleep time does not apply to In-App. However, to add a delay, add a segment node followed by the In-App node.

## Journey Procedures and Outcomes

The following table describes the journey procedures and outcomes involved in a Journey: 

| Procedures                         | Description                                                                                                                                                                                     |
| :--------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Publish the Journey**            | Makes your journey live.                                                                                                                                                                        |
| **Schedule the Journey**           | Activates the journey (users begin entering the journey) at a specified time—either now or at a later date.                                                                                     |
| **Initial Run of the Journey**     | The initial run of the journey occurs as soon as it is activated based on the scheduled date and time.                                                                                          |
| **Subsequent Run of the Journey ** | After the initial run, if the journey is set to recurring, subsequent runs occur at 12:00 a.m. the following day. Assuming the recurring day is set to T, the subsequent run occurs on T+1 day. |