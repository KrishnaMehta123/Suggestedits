---
title: WhatsApp Stats
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
[block:api-header]
{
  "title": "Campaign Stats in WhatsApp"
}
[/block]
To view the statistics of your campaign, select the campaign from the campaign list page.

You can track the status of your messages sent under the following heads:
  * Sent: Messages sent from CleverTap.
  * Delivered: Messages delivered to the user's WhatsApp app.
  * Viewed: Messages that the users have viewed. 
  * Control Group: Users who were excluded from the WhatsApp campaign because they belong to the control group.
  * Replied: The total number of replies sent by the users in response to the most recent campaign they respond to.
  * Errors: Errors occurred while sending the messages to the user.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/be3fbf4-Whatsapp_Stats.png",
        "Whatsapp Stats.png",
        2856,
        2968,
        "#f3f4f8"
      ],
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "warning",
  "title": "Notification Clicked Not Supported",
  "body": "In case of Whatsapp, CleverTap receives data points (like Sent, Delivered, Viewed, etc.) from Whatsapp as callbacks. However, WhatsApp does not support callbacks for Clicks. Therefore, the Notification Clicked event cannot be tracked and viewed under the *Overall Stats* tab."
}
[/block]