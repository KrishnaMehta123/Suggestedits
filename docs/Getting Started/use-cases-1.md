---
title: Use Cases_NewIA_WIP_NOT REQUIRED
excerpt: Explore use cases related to identity management
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
[block:api-header]
{
  "title": "Overview"
}
[/block]
To contextualize the concept of identity management, this section covers four use cases showcasing different scenarios.

#Use Case #1: No Identity Is Assigned
If your product does not assign an identity, the CleverTap ID is generated when the SDK is initialized for
the first time. 

In the following example, the first event came from device A and since there was no
record of this device, we assigned it a new CleverTap ID 1.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b51af39-Use_Case_1.png",
        "Use Case 1.png",
        728,
        279,
        "#faf0e9"
      ]
    }
  ]
}
[/block]
#Use Case #2: Identity Is Assigned after Anonymous Events
If your product assigns an identity, then we assume any events logged anonymously prior to an identity.
 
In the following example, the first two events are logged anonymously on device A which get assigned a
CleverTap ID of 1. The third event is the first event to have an identity on device A and therefore, is
assigned to the same CleverTap ID as the anonymous events. We can then say that user John did all
three events. There is one unique user in this set.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/07d0b20-Use_Case_2.png",
        "Use Case 2.png",
        733,
        149,
        "#fae7da"
      ]
    }
  ]
}
[/block]


#Use Case #3: Same Identity on Multiple Devices
For an e-commerce website, a user is navigating on both a mobile app and a website. When the user uses a common identity across multiple devices, CleverTap tracks the user in a single profile and provides a 360-degree view.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d815b1a-Use_Case_3.png",
        "Use Case 3.png",
        723,
        220,
        "#f8ece4"
      ]
    }
  ]
}
[/block]
#Use Case #4: Multiple Identities on the Same Device

CleverTap can maintain two separate profiles for users who are accessing the product from the same
 device. The onUserLogin API allows you to help accomplish the same.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/59777cb-Use_Case_4.png",
        "Use Case 4.png",
        723,
        224,
        "#f7ebe3"
      ]
    }
  ]
}
[/block]