---
title: Uninstall Events Sources (KB Article)
excerpt: >-
  Learn about different sources of uninstall events and its effect on Live
  Behavior campaigns.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

This article guides on configuring Live Behavior campaigns based on uninstall events. It also explains why the uninstall events with the source `CT_PUSH` do not trigger Live Behavior campaigns.

# Issue

A client has reported an issue with their SMS campaign, where users are not qualifying for the campaign even though they meet the criteria. This article addresses the specific issue where users did not qualify for campaigns where the source of uninstall events was `CT_PUSH`.

# Resolution

Understanding the source of uninstall events is crucial when configuring Live Behavior campaigns in CleverTap. Uninstall events can have the following two sources:

* Uninstall Events with Source as `CT_PUSH`
* Uninstall Events with Source as `REALTIME_FIREBASE`

The uninstall events with the source `CT_PUSH` are primarily used for tracking purposes and are not considered qualifying events for live behavior campaigns. Therefore, if the live behavior campaign's qualification event is set to *Uninstall events with source as CT\_PUSH*, users do not qualify for the campaign. The `CT_PUSH` does not work for the qualification because uninstall events with `CT_PUSH` are generated when CleverTap attempts to send a silent push to all eligible users. For the users who do not receive it, CleverTap assumes that they have uninstalled the app and raises an uninstall event. This usually happens once a day, and it does not coincide with the time the customer actually uninstalled. On the other side, the `REALTIME_FIREBASE` is real-time, as the name suggests. Therefore, it is more appropriate to trigger a campaign based on this source.

If you encounter issues where users are not qualifying for campaigns, ensure that the qualification event is set to *Uninstall events with source as REALTIME\_FIREBASE* to capture real-time uninstalls correctly.
