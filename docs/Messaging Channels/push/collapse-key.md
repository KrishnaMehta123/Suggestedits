---
title: Collapse Key
excerpt: >-
  Understand how to use the collapse notification key to update push
  notifications on Android devices.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Overview

A collapse notification key or collapse key is used to update push notifications on Android devices.

> 📘 Android Only
>
> The collapse key feature is only specific to Android devices.

This feature is used to update a notification that is rendered and available in the notification tray. While setting up the campaigns, check that the same key is used in similar campaigns. For example, a Score Update notification if the key used is *score-update*. All following campaigns that would be used to update earlier notifications must have the same key.

> 📘 New Notification
>
> A new notification will be rendered if the earlier notification was dismissed and not present on the device notification tray.

<Image title="Collapse Key.png" alt={989} border={true} src="https://files.readme.io/73ae9f0-Collapse_Key.png">
  Collapse Key
</Image>

# Use Case

Following is the order in which a notification can be replaced:

Push notification 1 (general notification) > Notification 2 (promo code or coupon) > Notification 2 with a higher validity. 

Coupon code to avail free snacks with orders above $20 at 5:00 PM > Promotional code valid for one hour can be sent at 7:00 PM > Replace it with a thank you notification for ordering and status tracking notification.
