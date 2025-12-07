---
title: Advanced Frequency Cap for Native Display (Paytm-specific)
excerpt: >-
  Learn how Advanced Frequency Capping helps control message frequency to
  deliver a balanced and non-intrusive user experience.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Overview

CleverTap’s Frequency Capping (FCAPS) ensures that users receive relevant and timely messages without being overwhelmed by communication. This helps improve user experience, prevent message fatigue, and maintain campaign effectiveness.

For Paytm, this feature is enhanced with Advanced Frequency Cap settings that go beyond standard limits. It provides granular control by allowing capping at daily, weekly, and monthly levels ensuring that broader quotas such as 100 messages/month are not exhausted within just a few days.

This implementation is currently exclusive to Paytm and applies specifically to Native Display campaigns.

Unlike standard frequency capping, Paytm’s implementation supports:

- Priority-driven campaign selection
- Trigger-based eligibility checks
- On-device FCAP evaluation for real-time decision-making
- Campaign recency resolution when priorities are equal

## Key Concepts

| Term                   | Description                                                                                                  |
| ---------------------- | ------------------------------------------------------------------------------------------------------------ |
| Frequency Cap          | The maximum number of times a user can receive a campaign within a defined time window (for example, 3/day). |
| Advanced Frequency Cap | Multi-level limit set across Month, Week, and Day to ensure fair distribution of messages over time.         |
| Priority               | Determines campaign precedence. Lower number = higher priority.                                              |
| Contextual Trigger     | A real-time event (for example, App Launch, Transaction Complete) that prompts campaign evaluation.          |
| Eligible Campaign      | A Native Display campaign that matches the trigger, hasn’t exhausted its FCAP, and is currently live.        |

## Advanced Frequency Cap Explained

The Advanced Frequency Cap helps ensure consistent pacing of user messages throughout the month by setting layered delivery limits across time windows:

- **Monthly Cap**: Sets the maximum number of messages a user can receive in a month.
- **Weekly Cap**: Restricts how many messages are delivered per week (within the monthly total).
- **Daily Cap**: Adds a cap to how many messages are sent per day (within the weekly and monthly limits).

These limits work in tandem, the most restrictive one applies first. If a user hits the daily cap, no further messages are shown that day, even if weekly or monthly caps are still available.

### Example Configuration

| Condition | Limit              |
| --------- | ------------------ |
| WHERE     | 100 messages/month |
| AND       | 55 messages/week   |
| AND       | 10 messages/day    |

This setup ensures the following:

- Users receive a 
  - maximum of 10 messages per day
  - maximum of 55 messages per week
  - maximum of 100 messages in a month

This prevents message exhaustion by ensuring message limits are spread over time, rather than being exhausted early.

#### Campaign Priority Settings

In addition to message caps, campaigns are assigned a priority (Low, Medium, High), which helps resolve conflicts when multiple campaigns are eligible. Priority is evaluated only after trigger and FCAP eligibility are validated.  
The following gif shows how to set your Advanced FCAP from the CleverTap dashboard for your campaigns:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5e8ec05002af3f6bad880b75b55598efd71a791f3b9791dde2a701cf559a0397-2025-07-21_17-16-05_1.gif",
        "",
        ""
      ],
      "align": "center",
      "border": true,
      "caption": "Setting up Advanced FCAP"
    }
  ]
}
[/block]


## Campaign Selection Logic (Paytm SDK)

When a contextual trigger fires (for example, App Launch), the SDK performs the following steps:

1. **Fetch eligible campaigns**:

   - Must be live Native Display campaigns
   - Must be tied to the current trigger
   - Must not have exhausted their FCAP (daily/weekly/monthly)

2. **Evaluate based on priority**:

   - Select the campaign with the lowest priority number
   - If multiple campaigns share the same priority:

     - Pick the one with the most recent update timestamp

3. **Display the selected campaign** and update FCAP usage on device.

## Example Scenario

The following campaigns are eligible for the **App Launch** trigger:

| Campaign Name  | Priority | Cap   | Views so far | Last Updated  |
| -------------- | -------- | ----- | ------------ | ------------- |
| Diwali Offer   | 2        | 3/day | 1            | 10 July, 2025 |
| Wallet Promo   | 1        | 1/day | 1            | 08 July, 2025 |
| Cashback Tease | 1        | 1/day | 0            | 09 July, 2025 |

**Resolution:**

- _Wallet Promo_ is disqualified (daily cap already hit).
- _Diwali Offer_ and _Cashback Tease_ are eligible.
- _Cashback Tease_ is chosen because it has:

  - Higher priority (1 vs 2)
  - Available daily cap
  - More recent update (vs Wallet Promo)

## Limitations

- Not supported for Push, Email, WhatsApp, or SMS campaigns.
- Rolling time window–based frequency capping is not available.
- Trigger and FCAP logic is custom to Paytm’s SDK and not part of CleverTap's standard SDK behavior.