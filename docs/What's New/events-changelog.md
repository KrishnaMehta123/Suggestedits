---
title: Events Changelog
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
Welcome to the Events changelog document for CleverTap. This changelog provides insights about the system event updates in CleverTap, ensuring you use CleverTap effectively and monitor your metrics with greater accuracy.

We are dedicated to empowering businesses with advanced mobile marketing and analytics capabilities and delivering continuous improvements to meet our users' evolving needs. Stay tuned as we update this changelog regularly, informing our customers about any changes to existing system events or the introduction of new ones.

<br />

# October

<br />

<Table align={["left","left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Change Release Date
      </th>

      <th>
        Event Name
      </th>

      <th>
        Property Name
      </th>

      <th>
        Update Type
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        October 11th, 2024
      </td>

      <td>
        Notification Failed
      </td>

      <td>

      </td>

      <td>
        Others
      </td>

      <td>
        Now, this event also captures the errors that occur in email campaigns.  

        * \*Note\*\*: This event is currently in Private Beta. Contact your account manager to enable this event.
      </td>
    </tr>
  </tbody>
</Table>

# June

<Table align={["left","left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Change Release Date
      </th>

      <th>
        Event Name
      </th>

      <th>
        Property Name
      </th>

      <th>
        Update Type
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        June 19th, 2024
      </td>

      <td>
        Notification Failed
      </td>

      <td>

      </td>

      <td>
        Event Added
      </td>

      <td>
        This event captures the errors that occurred in the campaign.  

        This event is currently in private beta and can be enabled upon request. Contact your account manager if you need access to this event.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>
        Campaign ID
      </td>

      <td>

      </td>

      <td>
        The property helps identify the specific campaign associated with the error.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>
        Campaign Type
      </td>

      <td>

      </td>

      <td>
        The property indicates the type of campaign (e.g., WhatsApp, SMS, Email).
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>
        Error
      </td>

      <td>

      </td>

      <td>
        The property describes the title of the error observed in the campaign.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>
        Label
      </td>

      <td>

      </td>

      <td>
        The property denotes the specific label associated with the error.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>
        Variant
      </td>

      <td>

      </td>

      <td>
        The property helps identify the errors for a specific campaign variant in the case of A/B, split delivery, or multi-variant campaigns.
      </td>
    </tr>
  </tbody>
</Table>

# May

<Table align={["left","left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Change Release Date
      </th>

      <th>
        Event Name
      </th>

      <th>
        Property Name
      </th>

      <th>
        Update Type
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        May 15, 2024
      </td>

      <td>
        Push Unregistered
      </td>

      <td>

      </td>

      <td>
        Properties Added
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>
        Source
      </td>

      <td>

      </td>

      <td>
        The property can have any one of the following values:  

        <ul><li> **CT_Push**: Indicating that the event is raised via silent Push. In this case, FCM returns a [404 Unregistered error](https://firebase.google.com/docs/reference/fcm/rest/v1/ErrorCode) for stale tokens from devices that have not connected to FCM for 270 days or for users who have uninstalled the app. </li> <li> **CT_SDK**: Indicating that the event is raised via OnUserLogin() method.</li> <li> **CT_Target**: Indicating that the event is raised via campaigns or journeys. </li></ul>
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>
        Token Value
      </td>

      <td>

      </td>

      <td>
        The property contains the actual value of the token.
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>
        Token Type
      </td>

      <td>

      </td>

      <td>
        The property indicates the type of token and can have any one of the following values:  

        <ul><li> FCM </li> <li> Baidu </li> <li> Huawei </li></ul>
      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>
        targetId
      </td>

      <td>

      </td>

      <td>
        The property denotes the ID of the campaign or journey.
      </td>
    </tr>
  </tbody>
</Table>

# April

<Table align={["left","left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Change Release Date
      </th>

      <th>
        Event Name
      </th>

      <th>
        Property Name
      </th>

      <th>
        Update Type
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        April 2, 2024
      </td>

      <td>
        Notification Clicked
      </td>

      <td>

      </td>

      <td>
        Property Added
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>

      </td>

      <td>

      </td>

      <td>
        button\_id
      </td>

      <td>

      </td>

      <td>
        The property is visible for the event if the *Notification Clicked* event is tracked for button clicks associated with the new Image Interstitial template. Therefore, the customers adopting this template will see this new property.  

        For more information, refer to [In-App Image Interstitial Template](doc:in-app-editor#image-interstitial).
      </td>
    </tr>
  </tbody>
</Table>
