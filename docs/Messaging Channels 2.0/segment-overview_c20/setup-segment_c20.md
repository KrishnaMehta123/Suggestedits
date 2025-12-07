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

<Image title="Segment unconnected.png" alt={1674} className="border" border={true} src="https://files.readme.io/b87d01a-Segment_unconnected.png" />

3. Click the **Segment** icon under the *Unconnected partners* section. The *Segment* page is displayed.
4. Enter the Segment details.

<Image title="Segment details.png" alt={2328} className="border" border={true} src="https://files.readme.io/3a78bbb-Segment_details.png" />

Segment : Write Key: The write key is a unique identifier for each source. It lets Segment know which source is sending the data and which destinations should receive that data.\
For more information, refer to [Locate your Write Key](https://segment.com/docs/connections/find-writekey/).

5. Click **Save credentials**. On clicking, the message "Credentials Saved" is displayed.

<Image title="Save Credentials.png" alt={2344} className="border" border={true} src="https://files.readme.io/02293d2-Save_Credentials.png" />

6. Click **Ok** to navigate back to the Exports page. Segment is now displayed under Connected partners when you navigate to *Settings* > *Partners* > *Exports*.

<Image title="Segment connected.png" alt={1392} className="border" border={true} src="https://files.readme.io/793543f-Segment_connected.png" />
