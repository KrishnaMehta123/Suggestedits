---
title: Copy
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

Unused Segment Management helps you keep your segments organized and your workspace efficient by identifying no longer actively used segments. These unused segments are marked as **Inactive**, making it easier to distinguish them from the currently used segments.

Inactive segments remain available for review, reuse, or deletion, allowing the system to prioritize active segments. This ensures your segment list stays clutter-free and focuses on segments relevant to your ongoing campaigns and analytics.

This guide explains how segments are classified as inactive, how you can access and manage them, and how inactive segments affect your account.

## Why This Feature Exists

Over time, accounts may accumulate many segments, some of which are no longer actively used. These inactive segments can make finding and managing the ones that matter most is harder (SA: grammatical error).  By automatically identifying and grouping unused segments, this feature helps you:

- Gain better visibility into which segments are in use and which are idle
- Review segments that may no longer be needed
- Easily reuse or remove old segments without disrupting ongoing setups
- Keep your workspace organized and easier to navigate

Inactive segments do not interfere with active campaigns or analytics but remain accessible whenever needed.

## How Segments Are Marked Inactive

A segment is marked **Inactive** when it meets the following conditions:

- It is not actively referenced in any live campaign, journey, test list, or message (SA: referencing is technical for customers, what is test list or message?)
- Its rule logic may still support passive features like analytics reports (Funnels, Cohorts) (SA: didn't understand this)

Inactive segments are not automatically removed from your account. They remain available for reuse, review, or deletion. You can view them by applying a filter on the segment list.

## Accessing Inactive Segments

The main _Segments_ page does not display inactive segments by default (This is wrong, inactive segments are displayed on the list page, however customer can't differentiate between active and inactive segments from the list page), prioritizing active segments for easier navigation. However, you can view inactive segments by enabling the **Status** column and applying filters to explore segments that are not currently in use.

Inactive segments are fully searchable and sortable like any other segment, ensuring you can find them when needed without cluttering the default view.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a0e1cfc538439eb21edc7875e232df7f6a12e44a16f762e64d82ad08ab34d572-image.png",
        null,
        "Unused Segments Marked Inactive"
      ],
      "align": "center",
      "border": true,
      "caption": "Unused Segments Marked Inactive"
    }
  ]
}
[/block]


## Segment Status: Active vs Inactive

| Segment Type          | Status   | Used in Analytics                     | Used in Campaigns or Journeys | Actions Available      |
| --------------------- | -------- | ------------------------------------- | ----------------------------- | ---------------------- |
| Actively Used Segment | Active   | Yes                                   | Yes                           | Clone, Delete, Archive |
| Unused Segment        | Inactive | Yes (rule only) (what does this mean) | No                            | Clone, Delete, Resume  |

Inactive segments remain accessible without interfering with your active setups. When a segment is resumed or reused, it becomes active again and participates in computations when triggered.

## How Inactive Segments Work

- They are grouped separately and hidden from the default view until filtered.
- They remain searchable, sortable, and available for reuse.
- They are marked active when resumed or reused.
- Computation for resumed segments is triggered as needed.
- Their presence does not affect reports or historical data.

## Managing Inactive Segments

While this feature does not require constant action, it helps you review and manage unused segments effectively. From the _Segments_ screen, you can:

| Action | Description                                                         |
| ------ | ------------------------------------------------------------------- |
| Clone  | Create a copy of the segment without affecting the original         |
| Resume | Reactivate the segment for use in campaigns or journeys when needed |
| Delete | Permanently remove the segment if it is no longer required          |

These actions help you keep the segment list tidy and ensure only relevant segments are visible in your day-to-day workflow.

You can perform these actions individually or in bulk.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4db8b8c2f05d039cb4ca97b019a26300dbe55b430db28c1518d92b562bbeb241-image.png",
        null,
        "Manage Inactive Segments"
      ],
      "align": "center",
      "border": true,
      "caption": "Manage Inactive Segments"
    }
  ]
}
[/block]


Segments can be resumed for computation using the option **Resume computation**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1adfe6f549ffa9a6514713b4cc1f67b5391827a6acee13a3df73752deddc5e74-image.png",
        null,
        "Resume Computation for Segments"
      ],
      "align": "center",
      "border": true,
      "caption": "Resume Computation for Segments"
    }
  ]
}
[/block]


# FAQs

### What qualifies a segment as inactive?

A segment is considered inactive when it is no longer referenced in any live setup like campaigns or journeys, although its rule logic may still support analytics features like Funnels or Cohorts. (SA:This is not clear)

### Can I reuse inactive segments?

Yes. Inactive segments remain available for use. Once you resume or reuse a segment, it is marked active and participates in computations when triggered. (SA: what does when triggered means)

### How do I view inactive segments?

Inactive segments are accessible by applying filters in the _Segments_ list. The default view prioritizes active segments, but you can easily include inactive segments by enabling the **Status** column and selecting the appropriate filter. (SA: this is incorrect)

### What is the difference between inactive and archived segments? (SA: we dont have any thing called as "Archived" segments)

- **Inactive** segments are automatically marked based on usage patterns but remain accessible and visible when filtered.
- **Archived** segments are manually removed from the active list and can be restored when needed. 

### Can I delete inactive segments?

Yes. You can review and delete segments that are no longer required. This helps in maintaining a clean and efficient segment list.

### Does marking a segment inactive affect reports?

No. Inactive segments do not impact existing reports or analytics data.