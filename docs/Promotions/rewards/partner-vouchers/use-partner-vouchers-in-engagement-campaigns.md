---
title: Use Partner Vouchers in Engagement Campaigns
excerpt: >-
  Learn how to engage users using the CT Partner Voucher Rewarded event and
  drive conversions.
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

CleverTap allows you to target users who have received a voucher by creating a campaign based on the *CT Partner Voucher Rewarded* event. This event helps personalize communication and drive users toward completing a desired action, such as making a purchase or redeeming an offer.

# Engage with Voucher Assigned Users

If you are a food delivery app that wants to increase redemption rates on the app. Let's say you want to remind users who received a discount voucher but have not redeemed it yet. You can set up a campaign as follows:

1. Go to *Campaigns* from the CleverTap dashboard.
2. Click **+ Campaign** and select a messaging channel from the *Messaging Channels* dropdown.
3. Click **Add an event** from the *Who* section.
4. Select the *CT Partner Voucher Rewarded* event and the required *Event Property*.

<Image alt="Target Partner Voucher Rewarded Users with a Campaign/Journey" align="center" border={true} src="https://files.readme.io/ec0bf334c94c2f624a6efed751bf2db208975e7bfe799b3352f4074a891b6bfe-image.png">
  Target Partner Voucher Rewarded Users with a Campaign/Journey
</Image>

<br />

For more information about creating a campaign, refer to the *Create Message* document of the respective messaging channel.

# CT Partner Voucher Rewarded

After a voucher is assigned to a user, CleverTap triggers the *CT Partner Voucher Rewarded* event. This event enables you to engage users by creating targeted campaigns based on voucher-related actions.

The event includes some System and Custom event properties, which help you track and personalize user engagement strategies. These properties can be leveraged in Liquid Tags to personalize messages, enabling dynamic content in your engagement campaigns.

For more information, refer to the CT Partner Voucher Rewarded event under [System Events](doc:events#system-events).
