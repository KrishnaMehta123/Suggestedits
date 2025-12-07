---
title: Use Loyalty Wallets in Engagement Campaigns
excerpt: >-
  Learn how to engage users using the CT Points Credited event and drive repeat
  purchases or desired behaviors.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

CleverTap allows you to target users who have received loyalty points by creating a campaign based on the _CT Points Credited_ event. This event helps you personalize communication and encourage users to redeem their points, driving higher conversions and user retention.

## Engage with Wallet Points Rewarded Users

If you are an e-commerce brand that wants to remind users who earned points from a recent purchase or campaign but have not redeemed them yet. You can create a targeted campaign like this:

1. Go to _Campaigns_ from the CleverTap dashboard.
2. Click **+ Campaign** and select a messaging channel from the dropdown.
3. Click **Add an event** from the _Who_ section.
4. Select the **CT Points Credited** event and apply filters using the event properties.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/41803e646664d95abb96b12dd840ffdf55d0ad2fad546698d361ebad1c73b243-image.png",
        null,
        "Target Points Credited Users with a Campaign/Journey"
      ],
      "align": "center",
      "border": true,
      "caption": "Target Points Credited Users with a Campaign/Journey"
    }
  ]
}
[/block]


## CT Points Credited

Whenever a user's wallet is credited with points, either via a campaign, API, or manually, CleverTap triggers the _CT Points Credited_ event. This allows you to create follow-up messaging such as reminders, promotional nudges, or personalized incentives.

The event includes some System and Custom event properties, which help you to personalize campaigns or segment users. These properties can be leveraged in Liquid Tags to personalize messages, enabling dynamic content in your engagement campaigns.

For more information, refer to the CT Points Credited event under [System Events](doc:events#system-events).