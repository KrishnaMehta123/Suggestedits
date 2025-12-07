---
title: Setup_PE_2
excerpt: >-
  Learn about the setup required on the CleverTap dashboard for receiving events
  data from the [segment.io](https://segment.io/) dashboard
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
To export event data to the [segment.io](https://segment.io/) dashboard via the *Campaigns* page, we need to connect the segment.io account to the CleverTap dashboard. To do so:
1. Log in to your CleverTap account.
2. Navigate to *Settings* > *Partners*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/deb5cd8-Navigate_to_Partners_page.png",
        "Navigate to Partners page.png",
        2854,
        1100,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]
3. Hover on the *Segment* icon and click **Integrate**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c775761-Click_Integrate.png",
        "Click Integrate.png",
        2396,
        1100,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]
On clicking, *Integrate raw data partner - Segment* popup opens on the right side of the screen.
4. Enter the following details and click **Integrate**:
[block:parameters]
{
  "data": {
    "h-0": "Field",
    "h-1": "Description",
    "0-0": "Partner Nickname",
    "0-1": "Enter the nickname for the partnership.",
    "1-0": "Write Key",
    "1-1": "A unique identifier for each source. It helps Segment identify which source is sending the data and which destinations should receive that data.\nFor more information, refer to [Locate your Write Key](https://segment.com/docs/connections/find-writekey/)."
  },
  "cols": 2,
  "rows": 2
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8dc099d-Integrate_raw_data_partner_-_Segment.png",
        "Integrate raw data partner - Segment.png",
        2402,
        1290,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]
After the integration is successful, the *Integrated* tag displays against Segment on the *Partner List* page.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cbc5d0f-Integrated_tag.png",
        "Integrated tag.png",
        2396,
        1100,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]