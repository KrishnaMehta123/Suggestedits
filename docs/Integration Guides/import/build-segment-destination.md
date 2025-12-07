---
title: Segment Destination (Action)
excerpt: >-
  Understand how the destination action framework controls Segment to send the
  events data it receives from the sources
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

The Destination Action framework lets you see and control how Segment sends the event data it receives from your sources to action-based destinations. In other words, it helps to create the following:

* Subscriptions, set of conditions that act as triggers to send data to the destination 
* Data mappings to format that data for the destination platform

After setting up the destination (action), Segment monitors the data that matches the conditions you create (called "triggers") for the subscription. When the conditions are met, explicit mapping transforms the incoming data to an output format that your destination can use.

# Advantages of Segment Destination (Action)

The following are the advantages of setting up Segment Destination:

* Upload User Profile
* Delete User Profile

# Set up Segment Destination (Action)

To set up Segment Destination (Action):

1. From the Segment web app, click **Catalog** and then click **Destinations**.
2. Select *Destinations Actions* under Categories from the left navigation.

<Image title="Navigation.png" alt={2848} className="border" border={true} src="https://files.readme.io/5f75f8e-Navigation.png" />

3. Click *CleverTap (Actions)*.
4. Click **Configure Actions CleverTap**.

<Image title="Click Configure CleverTap Action.png" alt={2418} className="border" border={true} src="https://files.readme.io/18e73b7-Click_Configure_CleverTap_Action.png" />

5. Select an existing *Source* to connect to CleverTap (Actions).
6. Enter the following project details to authorize the connection: 
   * Project ID
   * Passcode
   * Region

  These details are obtained by navigating to the *Settings* > *Project* page of the CleverTap dashboard.\
  To identify the region of your account, check the URL of your CleverTap account.

<Image title="CT Project Details.png" alt={1660} className="border" border={true} src="https://files.readme.io/0f85927-CT_Project_Details.png" />

   Refer to the following table to identify the region for your account:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        CleverTap Dashboard URL
      </th>

      <th>
        Region
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        [https://eu1.dashboard.clevertap.com/login.html#/](https://eu1.dashboard.clevertap.com/login.html#/)
      </td>

      <td>
        EU
      </td>
    </tr>

    <tr>
      <td>
        [https://in1.dashboard.clevertap.com/login.html#/](https://in1.dashboard.clevertap.com/login.html#/)
      </td>

      <td>
        India
      </td>
    </tr>

    <tr>
      <td>
        [https://us1.dashboard.clevertap.com/login.html#/](https://us1.dashboard.clevertap.com/login.html#/)
      </td>

      <td>
        US
      </td>
    </tr>

    <tr>
      <td>
        [https://sg1.dashboard.clevertap.com/login.html#/](https://sg1.dashboard.clevertap.com/login.html#/)
      </td>

      <td>
        Singapore
      </td>
    </tr>
  </tbody>
</Table>

7. Select *Quick Setup* to start with pre-populated subscriptions, or *Customized Setup* to configure each action from scratch. 
8. Click **Configure Actions**.

# Available Presets

CleverTap (Actions) has the following presets:

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Preset Name
      </th>

      <th>
        Trigger
      </th>

      <th>
        Default Action
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        User Upload
      </td>

      <td>
        Event type = "identify"
      </td>

      <td>
        Uploads User Profile to CleverTap dashboard
      </td>
    </tr>

    <tr>
      <td>
        User Delete
      </td>

      <td>
        Event event = "delete user"
      </td>

      <td>
        Deletes user profile
      </td>
    </tr>
  </tbody>
</Table>

# Available Actions

Combine supported triggers with the following CleverTap-supported actions:

## User Upload

Create a profile on the CleverTap dashboard or update it if it exists.

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Type
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Identity
      </td>

      <td>
        string
      </td>

      <td>
        * This field is mandatory.
        * It is used to recognize a unique user. 
        * It can be the user’s email, a phone number, or any other identifier that you are using to tag your users.
      </td>
    </tr>

    <tr>
      <td>
        Created At
      </td>

      <td>
        ts
      </td>

      <td>
        * This field is optional.
        * It denotes the date and time when the user profile was created.
        * Defaults to the current timestamp, if omitted.
        * For more information about converting this timestamp to Unix timestamps, refer to [Conversion Timestamps](https://docs.clevertap.com/docs/build-segment-destination#conversion-timestamps).
      </td>
    </tr>

    <tr>
      <td>
        Person Attributes
      </td>

      <td>
        object
      </td>

      <td>
        * This field is mandatory.
        * It consists of user profile properties. 
        * It is passed as key/value pairs.
        * properties[“Phone”] must be formatted as +[country code][phone number].
      </td>
    </tr>
  </tbody>
</Table>

## Delete User

Deletes the user profile on the CleverTap dashboard.

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Type
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Identity
      </td>

      <td>
        string
      </td>

      <td>
        * This field is mandatory.
        * It is used to recognize a unique user. 
        * It can be the user’s email, a phone number, or any other identifier that you are using to tag your users.
      </td>
    </tr>
  </tbody>
</Table>

# Conversion Timestamps

When mapping actions, you will see a *Convert Timestamps* setting. When enabled, it converts attributes containing ISO-8601 timestamps to Unix timestamps.

For example, if you send an event with a timestamp of 2006-01-02T18:04:07Z. It is converted to 1136253847. If the timestamp is not in ISO-8601 format, it is not converted. This avoids converting attributes such as phone numbers or IDs.
