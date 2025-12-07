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
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5f75f8e-Navigation.png",
        "Navigation.png",
        2848,
        1608,
        "#d7d8df"
      ],
      "border": true
    }
  ]
}
[/block]
3. Click *CleverTap (Actions)*.
4. Click **Configure Actions CleverTap**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/18e73b7-Click_Configure_CleverTap_Action.png",
        "Click Configure CleverTap Action.png",
        2418,
        1262,
        "#f7f8fc"
      ],
      "border": true
    }
  ]
}
[/block]
5. Select an existing *Source* to connect to CleverTap (Actions).
6. Enter the following project details to authorize the connection: 
   * Project ID
   * Passcode
   * Region
  
  These details are obtained by navigating to the *Settings* > *Project* page of the CleverTap dashboard.
  To identify the region of your account, check the URL of your CleverTap account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0f85927-CT_Project_Details.png",
        "CT Project Details.png",
        1660,
        1086,
        "#e2e2e9"
      ],
      "border": true
    }
  ]
}
[/block]
   Refer to the following table to identify the region for your account:
[block:parameters]
{
  "data": {
    "h-0": "CleverTap Dashboard URL",
    "h-1": "Region",
    "0-0": "https://eu1.dashboard.clevertap.com/login.html#/",
    "0-1": "EU",
    "1-0": "https://in1.dashboard.clevertap.com/login.html#/",
    "1-1": "India",
    "2-1": "US",
    "3-1": "Singapore",
    "3-0": "https://sg1.dashboard.clevertap.com/login.html#/",
    "2-0": "https://us1.dashboard.clevertap.com/login.html#/"
  },
  "cols": 2,
  "rows": 4
}
[/block]
7. Select *Quick Setup* to start with pre-populated subscriptions, or *Customized Setup* to configure each action from scratch. 
8. Click **Configure Actions**.
 
# Available Presets
CleverTap (Actions) has the following presets:
[block:parameters]
{
  "data": {
    "h-0": "Preset Name",
    "h-1": "Trigger",
    "h-2": "Default Action",
    "0-0": "User Upload",
    "1-0": "User Delete",
    "0-1": "Event type = \"identify\"",
    "0-2": "Uploads User Profile to CleverTap dashboard",
    "1-1": "Event event = \"delete user\"",
    "1-2": "Deletes user profile"
  },
  "cols": 3,
  "rows": 2
}
[/block]
# Available Actions
Combine supported triggers with the following CleverTap-supported actions:

## User Upload
Create a profile on the CleverTap dashboard or update it if it exists.

[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Type",
    "0-0": "Identity",
    "h-2": "Description",
    "0-1": "string",
    "0-2": "* This field is mandatory.\n* It is used to recognize a unique user. \n* It can be the user’s email, a phone number, or any other identifier that you are using to tag your users.",
    "1-0": "Created At",
    "1-1": "ts",
    "1-2": "* This field is optional.\n* It denotes the date and time when the user profile was created.\n* Defaults to the current timestamp, if omitted.\n* For more information about converting this timestamp to Unix timestamps, refer to [Conversion Timestamps](https://docs.clevertap.com/docs/build-segment-destination#conversion-timestamps).",
    "2-0": "Person Attributes",
    "2-1": "object",
    "2-2": "* This field is mandatory.\n* It consists of user profile properties. \n* It is passed as key/value pairs.\n* properties[“Phone”] must be formatted as +[country code][phone number]."
  },
  "cols": 3,
  "rows": 3
}
[/block]
## Delete User
Deletes the user profile on the CleverTap dashboard.
[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Type",
    "h-2": "Description",
    "0-0": "Identity",
    "0-1": "string",
    "0-2": "* This field is mandatory.\n* It is used to recognize a unique user. \n* It can be the user’s email, a phone number, or any other identifier that you are using to tag your users."
  },
  "cols": 3,
  "rows": 1
}
[/block]
# Conversion Timestamps
When mapping actions, you will see a *Convert Timestamps* setting. When enabled, it converts attributes containing ISO-8601 timestamps to Unix timestamps.

For example, if you send an event with a timestamp of 2006-01-02T18:04:07Z. It is converted to 1136253847. If the timestamp is not in ISO-8601 format, it is not converted. This avoids converting attributes such as phone numbers or IDs.