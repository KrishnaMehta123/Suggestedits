---
title: SMS as a Channel
excerpt: ''
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

CleverTap allows you to send SMS messages using either its Native SMS service or by connecting your own SMS provider. Both options support global delivery, regulatory compliance, and analytics, giving you complete flexibility in how you manage and measure your campaigns.

## SMS Integration Modes

You can choose between two setup options based on whether your SMS provider is already integrated with CleverTap.

| Method      | Description                                   | Navigation                                |
| ----------- | --------------------------------------------- | ----------------------------------------- |
| SMS Direct  | Pre-integrated and fully managed by CleverTap | _Settings > Channels > SMS > SMS Direct_  |
| SMS Connect | Connect your own provider via API credentials | _Settings > Channels > SMS > SMS Connect_ |

## Common Use Cases

The table below highlights popular SMS use cases implemented through CleverTap.

| Use Case                       | Objective                                 | Implementation                                              |
| ------------------------------ | ----------------------------------------- | ----------------------------------------------------------- |
| Order & Shipping Notifications | Keep users informed of order status       | Triggered by events such as `order_placed`, `order_shipped` |
| Abandoned Cart Recovery        | Recover revenue from incomplete purchases | Triggered by inactivity; personalized offers and links      |
| Flash Sales & Promotions       | Create urgency for time-limited offers    | Blast campaigns to segmented users with short URLs          |
| Appointment Reminders          | Reduce no-shows and missed deliveries     | Scheduled reminders with confirmation options via reply     |
| Feedback & NPS Surveys         | Collect customer feedback                 | Survey via SMS after events like `order_delivered`          |
| Subscription Renewal Alerts    | Reduce churn from missed renewals         | Date-based SMS one week and one day before expiration       |
| Emergency Alerts               | Communicate urgent service disruptions    | Manual or system-triggered; supports escalation logic       |