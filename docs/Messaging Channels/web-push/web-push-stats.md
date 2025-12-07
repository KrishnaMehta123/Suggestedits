---
title: Web Push Stats
excerpt: >-
  Understand all the statistical information available for your Web Push
  campaign
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Viewing Web Push Campaign Stats

Once the campaign has been published, you can view the statistics from the dashboard. Click on **Campaigns** > select the specific campaign from the campaign list. A Stats page opens up where you can view the total Views, Clicks, Conversions, CTR, and Conversion Performance.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cefa7ba-web_push_stats_final.png",
        "Trends and Stats",
        2768
      ],
      "align": "center",
      "border": true,
      "caption": "Web Push Campaign Stats"
    }
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ca4dc9cb6c0f6ec7e0c4c6cffa7b592e484c274073d2a12180aef09804b02a90-image.png",
        null,
        null
      ],
      "align": "center",
      "border": true,
      "caption": "Web Push Conversion Performance Stats"
    }
  ]
}
[/block]


<br />

- **Sent**: Represents the count of total Web Push notifications sent to the end-users.
- **Views**: Represents the number of times a Web Push notification is viewed.
- **Clicks**: Represents the number of times users have clicked on the Web Push notification.
- **CTR**:  Represents the ratio of Clicks to Views. (CTR = Clicks/Views \* 100).
- **Trend charts**: Represents trends of _Sent_, _Viewed_, and _Clicked_ events for this campaign over a specific period of time (for example daily, weekly, monthly).

# FAQs

### What are the timeouts and retry limits for Web Push Notifications?

The following are the timeout and retry limits for web push notifications:

| Channel | Timeout (ConnectionRequest)                  | Retry Limits |
| :------ | :------------------------------------------- | :----------- |
| Chrome  | 10 Seconds                                   | 6            |
| Firefox | 10 Seconds                                   | 3            |
| KaiOS   | 10 Seconds                                   | 3            |
| Safari  | 10 Seconds (Read and Connect), 30 Sec (Read) | 3            |

For more information, refer to the [Channel-Specific Timeouts and Retries](doc:platform-considerations#channel-specific-timeouts-and-retries).