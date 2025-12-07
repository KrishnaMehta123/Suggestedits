---
title: Events_clone with WZRK ID_WIP
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
# Overview

Events track what individual actions users perform in your app or website. Some examples of events include a user launching an app, viewing a product, listening to a song, sharing a photo, making a purchase, or favoriting an item.

By tracking events in your app, you can better understand what users are doing. In CleverTap, you can analyze these events in many different ways, such as getting aggregating metrics of a specific event or measuring how a specific event type trends over time. You can also engage with your users based on these events by creating campaigns in CleverTap that are triggered by them. 

<Image title="events1.png" alt={898} className="border" border={true} src="https://files.readme.io/40b874a-events1.png" />

**Event Categories**

There are two categories of events in CleverTap: System Events and Custom Events. 

System Events are events recorded automatically after you integrate our SDK. Custom Events are events you define and track with our SDK or API.

**Event Properties**

Events have details that describe the action taking place called properties. 

For example, while recording the “Product viewed” event, you could also store event properties like product name, category, and price. Recording event properties will help you answer questions like which category of products are more popular and help you segment users based on which categories or price points they’ve viewed.

# System Events

System Events are events recorded automatically after you integrate our SDK. 

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Event Type
      </th>

      <th>
        Description
      </th>

      <th>
        How Event is Tracked
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        App Installed
      </td>

      <td>
        This event is recorded when a user installs your application.
      </td>

      <td>
        The event is raised when the user launches the app for the first time. 

        There are three cases when this event will be recorded multiple times for a single user. The first case is when a user installs your app, uninstalls it, and then reinstalls it. The second case is when clear your app's memory. The third case is when a user installs your app on multiple devices.
      </td>
    </tr>

    <tr>
      <td>
        App Launched
      </td>

      <td>
        This event is recorded every time a user launches your application.
      </td>

      <td>
        There are two cases when this event will recorded. The first case is a fresh app launch, which is when an app is launched from a killed state. The second case is when a app is brought to the foreground after 20 minutes of inactivity in the background.
      </td>
    </tr>

    <tr>
      <td>
        App Uninstalled
      </td>

      <td>
        This event is recorded when a user uninstalls your application.
      </td>

      <td>
        This event is tracked by sending silent push notifications, which are type of notification that is not rendered on a user’s device. We send silent push notifications to your entire install base once every 24 hours to track uninstalls. For more information, please see [App Uninstall](https://clevertap.com/blog/track-app-uninstalls-effectively/).
      </td>
    </tr>

    <tr>
      <td>
        UTM Visited
      </td>

      <td>
        This event is tracked when user clicks on a link from a marketing campaign that has a UTM parameter defined on it. This event is also tracked when a CleverTap-integrated attribution platform, such as Branch or Apsalar, sends this information to CleverTap.
      </td>

      <td>
        The UTM Visited event is recorded for your marketing campaigns from external sources, such as Google Adwords or AdRoll.
      </td>
    </tr>

    <tr>
      <td>
        Notification Sent
      </td>

      <td>
        This event is tracked when a campaign message is sent to a user. This event is always recorded, even if the user does not open or click on the message. This event is recorded for email, mobile push, SMS, web push, and Facebook Audience campaigns. The Notification Sent event is available on the Event dashboard but it is not displayed on the User Profile.
      </td>

      <td>
        The event is tracked when the notification is successfully sent from CleverTap to the communication channel you select for your campaign.
      </td>
    </tr>

    <tr>
      <td>
        Notification Viewed
      </td>

      <td>
        This event is tracked when a user views an email, in-app notification, or a web notification sent from CleverTap.
      </td>

      <td>
        The CleverTap SDK recognizes when a notification sent via CleverTap is viewed by a user.

        Notification Viewed is available for Email, Web Push, InApp, Web Popup and App Inbox.
      </td>
    </tr>

    <tr>
      <td>
        Notification Clicked
      </td>

      <td>
        This event is tracked only when a user clicks on a campaign sent via CleverTap. You can track or create a Notification Clicked event for every UTM Visited event that is tracked by CleverTap and not any other provider. There is no separate event storage required for the Notification Clicked event because it is derived from the UTM Visited event.
      </td>

      <td>
        Recorded when a user clicks on a mobile push, in-app, email, web-popup or web push message sent via the CleverTap dashboard, or through the campaign API. 

        The Android Push notifications containing deep links to third-party apps are not tracked.
      </td>
    </tr>

    <tr>
      <td>
        Push Impressions
      </td>

      <td>
        This event is tracked when a Push notification sent from CleverTap is delivered on a user’s device. The funnels on the Push campaign statistics page reflects the count for this event.
      </td>

      <td>
        After the toggle for Push Impressions is turned on/setup from settings, the CleverTap SDK starts recording an event whenever a Push notification sent via CleverTap is delivered to the user’s device.
      </td>
    </tr>

    <tr>
      <td>
        App Version Changed
      </td>

      <td>
        This event is raised when a user’s current app version is different from the user’s previous app version.
      </td>

      <td>
        This event is tracked when the "CT App version" system property differs from one "App Launched" event to another.
      </td>
    </tr>

    <tr>
      <td>
        Notification Replied
      </td>

      <td>
        This event is recorded when a user replies to a WhatsApp message.
      </td>

      <td>
        This event is raised when the brand receives a reply from the user.
      </td>
    </tr>

    <tr>
      <td>
        Reply Sent
      </td>

      <td>
        This event is recorded when an agent (CleverTap user) replies to a message from the end user.
      </td>

      <td>
        This event is raised against the user profile of the end user.
      </td>
    </tr>

    <tr>
      <td>
        State Transitioned
      </td>

      <td>
        This event is recorded for lifecycle optimizer when a user transitions from one stage to another.
      </td>

      <td>
        This event is raised whenever a user transitions from one state to another or from unmapped to one of the states in the lifecycle optimization framework. It is meant for internal usage at CleverTap and therefore unavailable for querying.
      </td>
    </tr>

    <tr>
      <td>
        Session Concluded
      </td>

      <td>
        This event is recorded to mark the end of a session. Session Tracking must be enabled for the event to be tracked.
      </td>

      <td>
        This event is raised when there is 20 minutes of inactivity after an event is raised for a user.
      </td>
    </tr>
  </tbody>
</Table>

# Debug Events

Debug Events are events recorded automatically after you integrate our SDK. These events are raised at certain lifecycle stages in your integration and helps you track and manage your integration\
These events are available on any profile page and Find People page by adding a parameter to the url '*?showDebugEvents=true*'

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Event Name
      </th>

      <th>
        Description
      </th>

      <th>
        When is it raised
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Identity Set
      </td>

      <td>
        This DEBUG event is raised when a new user is identified on a customer’s app or an identified user pushes another identity.
      </td>

      <td>
        This event monitors the status and data points that are important for the identification and engagement of users. This event is for monitoring and debugging only.
      </td>
    </tr>

    <tr>
      <td>
        Identity Reset
      </td>

      <td>
        This DEBUG event is raised when a profile is de-merged (after de-merge a new profile for every device is created and identities are dropped) either from dashboard (“reset identities” click on profile page) or through the Demerge Profile API.
      </td>

      <td>
        It monitors the reset of identities and handles unnecessary merges. This event is used for monitoring and debugging only.
      </td>
    </tr>

    <tr>
      <td>
        Identity Error
      </td>

      <td>
        This DEBUG event is raised when an existing identity is associated incorrectly with another identity. The former identity is now declared as invalid for the latter's profile.
      </td>

      <td>
        This event is for monitoring and debugging when identity merges are invalid
      </td>
    </tr>

    <tr>
      <td>
        Reachable By
      </td>

      <td>
        This DEBUG event is raised when a user becomes reachable by a communication channel, such as SMS, Email, Mobile Push, or there are changes to the existing communication channel.
      </td>

      <td>
        Tracked for a profile when

        * Push token is added/changed.
        * Email ID is added/changed
        * Phone number is added/changed.
      </td>
    </tr>
  </tbody>
</Table>

# Custom Events

Custom Events are events you define and track with our SDK or API. For more information, please visit our [developer documentation](https://developer.clevertap.com/v1.0/docs/concepts-events).

# Event Metadata Recorded Automatically

For every event that’s recorded, CleverTap records the following standard metadata:

* Information about the user who performed the event.
* Date and time when the event was recorded.
* The number of screens viewed by the user before performing the action.
* The referring site and the source of the user visit if it was from an external source.

Additionally, CleverTap keeps the user profiles updated with the latest:

* Geographic information like their city, region, country, and latitude/longitude (if available).
* Browser or device make, model, etc. used to access the website or app.

# System Properties

CleverTap tracks the following system properties automatically from the mobile SDK. All the system properties are prefixed by ‘CT’, indicating that they are provided by CleverTap. 

The following properties are tracked automatically on all events:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        System Property
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        CT App version
      </td>

      <td>
        This is the current version of your application installed on the user device.
      </td>
    </tr>

    <tr>
      <td>
        CT Latitude
      </td>

      <td>
        The user location identified by the latitude.
      </td>
    </tr>

    <tr>
      <td>
        CT Longitude
      </td>

      <td>
        The user location identified by the longitude.
      </td>
    </tr>

    <tr>
      <td>
        CT Source
      </td>

      <td>
        The source of the event.\
        For example, the event may originate from a Mobile SDK or an API.

        All possible values:

        * Mobile (Mobile SDK)
        * MobileWeb (Web SDK)
        * Web (Web SDK)
        * API
        * segment
        * appsflyer
        * apsalar
        * branch
        * tune
        * System (For events generated by CleverTap)
      </td>
    </tr>
  </tbody>
</Table>

The following properties are available on the App Launched event:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        System Property
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        CT App version
      </td>

      <td>
        This is the current version of your application installed on the user device.
      </td>
    </tr>

    <tr>
      <td>
        CT Latitude
      </td>

      <td>
        The user location identified by the latitude.
      </td>
    </tr>

    <tr>
      <td>
        CT Longitude
      </td>

      <td>
        The user location identified by the longitude.
      </td>
    </tr>

    <tr>
      <td>
        CT OS Version
      </td>

      <td>
        The Operating system of the device.\
        For example,  1.0.0
      </td>
    </tr>

    <tr>
      <td>
        CT SDK Version
      </td>

      <td>
        The CleverTap SDK version. For example, 30501
      </td>
    </tr>

    <tr>
      <td>
        CT Network Carrier
      </td>

      <td>
        The network carrier of the device.\
        For example, AT\&T, Vodafone.
      </td>
    </tr>

    <tr>
      <td>
        CT Network Type
      </td>

      <td>
        The network type of the device\
        For example, 4g
      </td>
    </tr>

    <tr>
      <td>
        CT Connected To WiFi
      </td>

      <td>
        Indicates if the device is connected to the Wi-FI.
      </td>
    </tr>

    <tr>
      <td>
        CT Bluetooth Version
      </td>

      <td>
        The Bluetooth version of the device
      </td>
    </tr>

    <tr>
      <td>
        CT Bluetooth Enabled
      </td>

      <td>
        Indicates if  Bluetooth is enabled on the device.
      </td>
    </tr>

    <tr>
      <td>
        CT Source
      </td>

      <td>
        The source of the event.\
        For example, the event may originate from a Mobile SDK or an API.

        All possible values:

        * Mobile (Mobile SDK)
        * MobileWeb (Web SDK)
        * Web (Web SDK)
        * API
        * segment
        * appsflyer
        * apsalar
        * branch
        * tune
        * System (For events generated by CleverTap)
      </td>
    </tr>
  </tbody>
</Table>

> 📘 Latitude and Longitude
>
> The system properties 'latitude' and 'longitude' are captured and sent from the SDK only if the user gives consent on your app.

## Notification Viewed event 

The following properties are available on the Notification Viewed event:

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        System Property
      </th>

      <th>
        Description
      </th>

      <th>
        Raise event if
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        wzrk\_id
      </td>

      <td>
        Open rate tracking ID (can be empty or it might not be present).
      </td>

      <td>
        This event is tracked when a user views an email, in-app notification, or a web notification sent from CleverTap.
      </td>
    </tr>

    <tr>
      <td>
        wzrk\_pivot
      </td>

      <td>
        Variant of the A/B test
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Campaign type
      </td>

      <td>
        CT campaign type (push,Web,Webhook,)
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Campaign id
      </td>

      <td>
        CT campaign id
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_acct\_id
      </td>

      <td>
        CT account id
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_cid
      </td>

      <td>
        Channel ID
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_pid
      </td>

      <td>
        Campaign ID
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_rnv
      </td>

      <td>
        If present and not empty, it will raise notification viewed event
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_ttl
      </td>

      <td>
        time to live
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_bc
      </td>

      <td>
        Batch count
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_bp
      </td>

      <td>
        Image URL
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_ck
      </td>

      <td>
        Collapse key (the actual key which you have provided)
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_dl
      </td>

      <td>
        deeplink
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_pn
      </td>

      <td>
        If present, this notification is sent from CleverTap.
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_sound
      </td>

      <td>
        Custom sound to play or not boolean value.
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_collapsible
      </td>

      <td>
        Collapse key (the actual key which you have provided) \{@ankita same as wzrk\_ck ? what is the difference?}
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        CT App Version
      </td>

      <td>
        CT version
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        CT Source
      </td>

      <td>
        Mobile Phone or Desktop
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        CT Latitude
      </td>

      <td>
        last known latitude captured by CT (on APP launch)
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        CT Longitude
      </td>

      <td>
        Last known longitude captured by CT (on APP launch)
      </td>

      <td>

      </td>
    </tr>
  </tbody>
</Table>

## Notification sent

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        System Property
      </th>

      <th>
        Description
      </th>

      <th>
        Raised event if
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Campaign Id
      </td>

      <td>
        campaign id
      </td>

      <td>
        This event is tracked when a campaign message is sent to a user. This event is always recorded, even if the user does not open or click on the message. This event is recorded for email, mobile push, SMS, web push, and Facebook Audience campaigns. The Notification Sent event is available on the Event dashboard but it is not displayed on the User Profile.
      </td>
    </tr>

    <tr>
      <td>
        Campaign type
      </td>

      <td>
        type of campaign - push, email, etc
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Labels
      </td>

      <td>
        labels added to campaign
      </td>

      <td>

      </td>
    </tr>
  </tbody>
</Table>

## Notification clicked

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        System Property
      </th>

      <th>
        Description
      </th>

      <th>
        Raised event if
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        wzrk\_acct\_id
      </td>

      <td>
        account id
      </td>

      <td>
        This event is tracked only when a user clicks on a campaign sent via CleverTap.
      </td>
    </tr>

    <tr>
      <td>
        wzrk\_bc
      </td>

      <td>
        badge count
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_bi
      </td>

      <td>
        badge icon
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_c2a
      </td>

      <td>
        call to action (c2a) buttons
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_cid
      </td>

      <td>
        channel id
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_ck
      </td>

      <td>
        Collapse key (the actual key which you have provided)
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_clr
      </td>

      <td>
        If present and not empty, it contains the Hex value of the colour to be applied on the small icon (and app name for Android versions below Pie)
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_cts
      </td>

      <td>
        Clicked Timestamp
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_collapsible
      </td>

      <td>
        if collapse key is added
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_dl
      </td>

      <td>
        deep link
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_nms
      </td>

      <td>
        notification message summary
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_pid
      </td>

      <td>
        Internal Push notification id
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_pivot
      </td>

      <td>
        Variant of the A/B test
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_pn
      </td>

      <td>
        If present, this notification is sent from CleverTap.
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_rnv
      </td>

      <td>
        Flag to raise notification viewed event
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_sound
      </td>

      <td>
        custom sound (true/flase)
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_st
      </td>

      <td>
        notification subtext
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        wzrk\_ttl
      </td>

      <td>
        time to live
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Campaign id
      </td>

      <td>
        campaign id
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        CT App Version
      </td>

      <td>
        app version
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        CT Source
      </td>

      <td>
        Mobile or Web
      </td>

      <td>

      </td>
    </tr>
  </tbody>
</Table>

## Push Impression

This event is raised when a push notification is delivered/rendered on the device.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        System Property
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        CT App Version
      </td>

      <td>
        app version
      </td>
    </tr>

    <tr>
      <td>
        CT Source
      </td>

      <td>
        Mobile or Web
      </td>
    </tr>

    <tr>
      <td>
        Campaign type
      </td>

      <td>
        email/push
      </td>
    </tr>

    <tr>
      <td>
        wzrk\_acct\_id
      </td>

      <td>
        account id
      </td>
    </tr>

    <tr>
      <td>
        wzrk\_bc
      </td>

      <td>
        badge count
      </td>
    </tr>

    <tr>
      <td>
        wzrk\_bi
      </td>

      <td>
        badge icon
      </td>
    </tr>

    <tr>
      <td>
        wzrk\_cid
      </td>

      <td>
        channel id
      </td>
    </tr>

    <tr>
      <td>
        wzrk\_dl
      </td>

      <td>
        deep link
      </td>
    </tr>

    <tr>
      <td>
        wzrk\_id
      </td>

      <td>
        campaign id
      </td>
    </tr>

    <tr>
      <td>
        wzrk\_pid
      </td>

      <td>
        Internal Push notification id
      </td>
    </tr>

    <tr>
      <td>
        wzrk\_pivot
      </td>

      <td>
        Variant of the A/B test
      </td>
    </tr>

    <tr>
      <td>
        wzrk\_pn
      </td>

      <td>
        If present, this notification is sent from CleverTap.
      </td>
    </tr>

    <tr>
      <td>
        wzrk\_rnv
      </td>

      <td>
        Flag to raise notification viewed event
      </td>
    </tr>

    <tr>
      <td>
        wzrk\_sound
      </td>

      <td>
        custom sound (true/flase)
      </td>
    </tr>

    <tr>
      <td>
        wzrk\_ttl
      </td>

      <td>
        time to live
      </td>
    </tr>
  </tbody>
</Table>

## App Installed

This event is recorded when a user installs your application.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        System Property
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        CT App Version
      </td>

      <td>
        app version
      </td>
    </tr>

    <tr>
      <td>
        CT Source
      </td>

      <td>
        Mobile or Web
      </td>
    </tr>
  </tbody>
</Table>

## App Uninstalled

\{@ankita need info here}

| System Property | Description |
| :-------------- | :---------- |
|                 |             |

## Identity Set

This DEBUG event is raised when a new user is identified on a customer’s app or an identified user pushes another identity.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        System Property
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        ID
      </td>

      <td>
        user identity
      </td>
    </tr>

    <tr>
      <td>
        Type
      </td>

      <td>
        new or existing user
      </td>
    </tr>

    <tr>
      <td>
        Source
      </td>

      <td>
        API/ SDK
      </td>
    </tr>

    <tr>
      <td>
        Dropped History
      </td>

      <td>
        if history is dropped
      </td>
    </tr>
  </tbody>
</Table>

## Identity Reset

This DEBUG event is raised when a profile is de-merged (after de-merge a new profile for every device is created and identities are dropped) either from dashboard (“reset identities” click on profile page) or through the Demerge Profile API.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        System Property
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Dropped History
      </td>

      <td>
        if history is dropped
      </td>
    </tr>

    <tr>
      <td>
        Source
      </td>

      <td>
        API/ SDK
      </td>
    </tr>
  </tbody>
</Table>

## Identity Error

This DEBUG event is raised when an existing identity is associated incorrectly with another identity. The former identity is now declared as invalid for the latter's profile.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        System Property
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        ID
      </td>

      <td>
        user identity
      </td>
    </tr>

    <tr>
      <td>
        Source
      </td>

      <td>
        API/ SDK
      </td>
    </tr>
  </tbody>
</Table>

## Reachable By

This DEBUG event is raised when a user becomes reachable by a communication channel, such as SMS, Email, Mobile Push, or there are changes to the existing communication channel.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        System Property
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        type
      </td>

      <td>
        channel type where reachable - Email or push
      </td>
    </tr>

    <tr>
      <td>
        value
      </td>

      <td>
        email of the user if reachable via email and push token if reachable via Mobile Push
      </td>
    </tr>
  </tbody>
</Table>

## App Version Change

This event is raised when a user’s current app version is different from the user’s previous app version.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        System Property
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        CT App Version
      </td>

      <td>
        current app version
      </td>
    </tr>

    <tr>
      <td>
        CT Previous App Version
      </td>

      <td>
        previous app version
      </td>
    </tr>

    <tr>
      <td>
        CT Source
      </td>

      <td>
        mobile
      </td>
    </tr>
  </tbody>
</Table>

## Webhook Delivered

This event is raised when a webhook is delivered.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        System Property
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        CT Source
      </td>

      <td>
        system
      </td>
    </tr>

    <tr>
      <td>
        Campaign id
      </td>

      <td>
        campaign id
      </td>
    </tr>
  </tbody>
</Table>

## UTM Visited

This event is tracked when user clicks on a link from a marketing campaign that has a UTM parameter defined on it. This event is also tracked when a CleverTap-integrated attribution platform, such as Branch or Apsalar, sends this information to CleverTap.

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        System Property
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        install
      </td>

      <td>
        if this is an install
      </td>
    </tr>

    <tr>
      <td>
        provider
      </td>

      <td>
        attribution provider integrated with
      </td>
    </tr>
  </tbody>
</Table>
