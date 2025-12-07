---
title: Webhooks
excerpt: Monitor specific events.
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
      title: Setup Webhooks
      url: https://docs.clevertap.com/docs/webhooks-overview_c20
    - type: link
      title: Create Webhooks
      url: https://docs.clevertap.com/docs/create-message-webhook_c20
    - type: link
      title: Personalize Webhooks
      url: https://docs.clevertap.com/docs/personalize-message-webhooks_c20
    - type: link
      title: Webhook Stats
      url: https://docs.clevertap.com/docs/webhooks-stats_c20
---
# Overview

CleverTap webhooks enable you to pass user information basis on specific business workflows to any third-party endpoint. 

For example, when a high-value transaction is abandoned on your e-commerce website, you can send details about the abandoned products and user details via a webhook campaign to your operations center.

There are six categories of webhooks that you can create. The table below describes each of those categories.

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Type
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
        Single action
      </td>

      <td>
        User performed an action.
      </td>

      <td>
        User launched the app.
      </td>
    </tr>

    <tr>
      <td>
        Actions
      </td>

      <td>
        User performed multiple actions.
      </td>

      <td>
        User launched the app and viewed a notification.
      </td>
    </tr>

    <tr>
      <td>
        Inaction within time
      </td>

      <td>
        User performed an action, but does not perform another action within a certain time.
      </td>

      <td>
        User has not launched the app in three days.
      </td>
    </tr>

    <tr>
      <td>
        Inaction
      </td>

      <td>
        Users performed an action, but did not perform another action.
      </td>

      <td>
        User launched the app, but did not view a notification.
      </td>
    </tr>

    <tr>
      <td>
        Date time property
      </td>

      <td>
        Period of time after a date time property on a user event.
      </td>

      <td>
        User purchased an item and three days have passed.
      </td>
    </tr>

    <tr>
      <td>
        Actions with user properties
      </td>

      <td>
        Performed an action or not, filtered by their demographic properties.
      </td>

      <td>
        User purchased an item and lives in Canada.
      </td>
    </tr>
  </tbody>
</Table>
