---
title: Analyzing Discrepencies in Device Related Event Data (KB Article)
excerpt: ''
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

CleverTap's user counting mechanisms behave differently when segmenting users from Campaigns vs Events pages. This difference occurs when you segment people based on device-related data such as OS, SDK, and App Version. This article helps you understand why user count discrepancies exist between Segmentation in Campaigns and Events in CleverTap.

## Segmenting via Campaigns

When segmentating via the Campaign's _Who_ section, CleverTap employs a user-centric approach to counting users. This means that CleverTap ensures that users who qualify for segmentation across different criteria are not counted twice. For example, if a segmentation rule targets the users who performed the _App Launched_ event with the property _iOS version equals 1 and 2 in the last 30 days_, a user who uses both iOS versions within the specified timeframe is counted only once.

## Segmenting via Events

The _Events_ page employs an event-centric approach to user counting. It means that each occurrence of a specific event is considered independently. Consequently, if the same user performs the _App Launched_ event with different iOS versions (for example, _IOS=1_ and _IOS=2_),  these events be counted twice as we have the _App Launched_ event both with _IOS=1_ and _IOS=2_.

> 📘 Reason for the Changed Behavior
> 
> These discrepancies in behavior are visible during granular filtering or segmentation by technographic data, when you extensively use the  _filtering_ and/or _splitting by_ functionality. These disparities are not common but exist in edge-case scenarios that manifest when you perform a detailed analysis of device-related attributes.