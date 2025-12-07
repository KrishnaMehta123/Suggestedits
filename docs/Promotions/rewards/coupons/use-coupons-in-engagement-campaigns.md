---
title: Use Coupons in Engagement Campaigns
excerpt: >-
  Learn how to engage users using the CT Coupon Rewarded event and drive
  redemptions or specific user actions.
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

CleverTap enables you to target users who have been rewarded with coupons by creating an engagement campaign based on the _CT Coupon Rewarded_ event. This event helps you personalize communication and encourages users to redeem their coupons, leading to improved conversions and enhanced customer loyalty.

## Engage with Coupon Rewarded Users

If you are an e-commerce brand that has distributed coupons to users after a special promotion, you can nudge those who have not redeemed them yet. Here's how to set up such a campaign:

1. Go to _Campaigns_ in the CleverTap dashboard.
2. Click **+ Campaign** and choose a messaging channel.
3. Click **Add an event** from the _Who_ section.
4. Select the _CT Coupon Rewarded_ event and apply relevant filters using the event properties.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b9cd58cc7945a1dac059d8688dec6d23c69577af140a06c548e272218c2a58f2-image.png",
        null,
        "Target Coupon Rewarded Users with a Campaign/Journey"
      ],
      "align": "center",
      "border": true,
      "caption": "Target Coupon Rewarded Users with a Campaign/Journey"
    }
  ]
}
[/block]


## CT Coupon Rewarded

Whenever a user's account is rewarded with a coupon, whether via a promo campaign or API, CleverTap triggers the _CT Coupon Rewarded_ event. This allows you to send timely follow-up messages, promotional nudges, or personalized reminders to drive coupon usage.

The event includes some System and Custom properties to help personalize campaigns or create meaningful segments. These properties can be used with **Liquid Tags** to personalize your message content, enabling dynamic and tailored user engagement in your campaigns.

For more information, refer to the CT Coupon Rewarded event under [System Events](doc:events#system-events).