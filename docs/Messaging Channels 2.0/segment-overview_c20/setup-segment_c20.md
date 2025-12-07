---
title: Setup
excerpt: >-
  Understand how to set up Segment for sending event data to the Segment
  dashboard
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: >-
    Refer to the pages listed below to learn more about the following Segment
    sections:
  pages:
    - type: link
      title: Create Message
      url: https://docs.clevertap.com/docs/create-message-segment_c20
    - type: link
      title: Personalize Message
      url: https://docs.clevertap.com/docs/personalize-message-segment_c20
    - type: link
      title: Segment Campaign Stats
      url: https://docs.clevertap.com/docs/segment-campaign-stats_c20
---
To export event data to the Segment dashboard via the *Campaigns* page, we need to connect the Segment account to the CleverTap dashboard. To do so:
1. Log in to your CleverTap account.
2. Navigate to *Settings* > *Partners* > *Exports*. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b87d01a-Segment_unconnected.png",
        "Segment unconnected.png",
        1674,
        1032,
        "#e9ebf1"
      ],
      "border": true
    }
  ]
}
[/block]
3. Click the **Segment** icon under the *Unconnected partners* section. The *Segment* page is displayed.
4. Enter the Segment details.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3a78bbb-Segment_details.png",
        "Segment details.png",
        2328,
        632,
        "#fafbfc"
      ],
      "border": true
    }
  ]
}
[/block]
Segment : Write Key: The write key is a unique identifier for each source. It lets Segment know which source is sending the data and which destinations should receive that data.
For more information, refer to [Locate your Write Key](https://segment.com/docs/connections/find-writekey/).

5. Click **Save credentials**. On clicking, the message "Credentials Saved" is displayed.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/02293d2-Save_Credentials.png",
        "Save Credentials.png",
        2344,
        826,
        "#acadb0"
      ],
      "border": true
    }
  ]
}
[/block]
6. Click **Ok** to navigate back to the Exports page. Segment is now displayed under Connected partners when you navigate to *Settings* > *Partners* > *Exports*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/793543f-Segment_connected.png",
        "Segment connected.png",
        1392,
        792,
        "#f9f9fa"
      ],
      "border": true
    }
  ]
}
[/block]