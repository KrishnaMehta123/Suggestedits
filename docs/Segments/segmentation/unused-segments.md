---
title: Manage Unused Segments
excerpt: >-
  Learn how to manage unused segments by hiding them from your active view
  without permanently deleting them.
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

Manage unused segments to keep your workspace organized and efficient. This feature identifies segments no longer actively used and marks them as *Inactive*, so you can easily distinguish them from active ones.

Inactive segments remain available for review, reuse, or deletion, helping you focus on the segments that matter most to your campaigns and analytics.

This guide explains how segments become inactive, how to view and manage them, and how inactivity affects your account.

## Feature Purpose and Benefits

Over time, your account may accumulate unused segments that clutter your workspace and slow navigation. Managing unused segments helps you focus on segments that drive active campaigns.

By automatically identifying unused segments, this feature helps you to do the following:

* Clearly view which segments are active and which are unused.
* Review old segments to decide whether to reuse or delete them.
* Keep your segment list organized and clutter-free.

Inactive segments remain available for reference, and you can reactivate them at any time. The status of the segment does not affect active campaigns or reports.

## Identify When a Segment Becomes Inactive

Understanding when a segment becomes inactive helps you manage and maintain your data effectively. A segment is marked as inactive under the following conditions:

* It is not used in any live Campaign or Journey.
* It is no longer recalculated or refreshed for active use cases.

Even if a segment’s rules continue to support historical reports such as Funnels or Cohorts, it becomes inactive when it is no longer linked to any active Campaign or Journey.

Inactive segments are not deleted automatically. You can review, reuse, or delete them at any time from the segment list.

## Access Inactive Segments

Inactive segments are visible directly on the *Segments* list page.

You can identify them using the *Status* column, which shows whether each segment is Active or Inactive.

To filter inactive segments:

1. Go to the *Segments* page.
2. Enable the *Status* column (if not visible).
3. Apply the filter *Status > Inactive* to list all inactive segments.

Inactive segments are searchable and sortable, similar to any other segment, allowing quick access without cluttering your default view.

<Image alt="Unused Segments Marked Inactive" align="center" border={true} src="https://files.readme.io/a0e1cfc538439eb21edc7875e232df7f6a12e44a16f762e64d82ad08ab34d572-image.png">
  Unused Segments Marked Inactive
</Image>

## Compare Active and Inactive Segments

You can use the following table to understand how segment status affects its behavior and available actions.

| Segment Type          | Status   | Used in Analytics        | Used in Campaigns or Journeys | Actions Available     |
| --------------------- | -------- | ------------------------ | ----------------------------- | --------------------- |
| Actively Used Segment | Active   | Yes                      | Yes                           | Clone, Delete         |
| Unused Segment        | Inactive | Yes (for reporting only) | No                            | Clone, Delete, Resume |

When you resume or reuse an inactive segment, it becomes **Active** again.

## Behavior of Inactive Segments

Once a segment becomes inactive, it stays accessible but stops participating in active processes. Here’s how inactive segments behave in your workspace:

* Inactive segments remain visible in the list and can be filtered by status.
* You can resume them anytime.
* When resumed, the system recalculates the segment and marks it Active.
* Inactive segments do not affect reports or historical data.

Since inactive segments remain available until you delete them, you can keep, reuse, or remove them without impacting live campaigns.

> 📘 Note
>
> Inactive segments stop updating or recalculating until they are reactivated.

## Manage Inactive Segments

You can manage inactive segments from the *Segments* page. You can perform the following actions individually or in bulk:

<Table>
  <thead>
    <tr>
      <th>
        Action
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Clone**
      </td>

      <td>
        Create a duplicate of the segment for modification or reuse.
      </td>
    </tr>

    <tr>
      <td>
        **Resume**
      </td>

      <td>
        Reactivate the segment to make it active again for Campaigns or Journeys.  

        \{@Sanskriti- Does reactivating a segment requires user action (for example, selecting “Resume computation”) or if it occurs automatically when reused in a campaign?}
      </td>
    </tr>

    <tr>
      <td>
        **Delete**
      </td>

      <td>
        Permanently remove the segment if it's no longer needed.
      </td>
    </tr>
  </tbody>
</Table>

The following image shows the Resume computation option:

<Image alt="Manage Inactive Segments" align="center" border={true} src="https://files.readme.io/4db8b8c2f05d039cb4ca97b019a26300dbe55b430db28c1518d92b562bbeb241-image.png">
  Manage Inactive Segments
</Image>

To reactivate a segment, select *Resume computation*. Once resumed, the segment's data is recalculated and becomes active.

<Image alt="Resume Computation for Segments" align="center" border={true} src="https://files.readme.io/1adfe6f549ffa9a6514713b4cc1f67b5391827a6acee13a3df73752deddc5e74-image.png">
  Resume Computation for Segments
</Image>

# FAQs

This section covers common questions to help you manage segments effectively.

### What qualifies a segment as inactive?

A segment becomes inactive when it's no longer linked to any live campaign or journey. Although its rule logic may still support viewing historical data in reports such as Funnels or Cohorts, it is considered inactive for engagement purposes.

### Can I reuse inactive segments?

Yes. You can reuse any inactive segment. When you resume or use the segment in a new Campaign or Journey, it becomes active again, and the system recomputes which users currently qualify for that segment according to its rule conditions.

### How do I view inactive segments?

Inactive segments appear on the main Segments list. Use the *Status* column to check each segment's state or filter by *Status > Inactive* to view only unused ones.

### Can I delete inactive segments?

Yes. You can safely delete inactive segments to declutter your workspace. This action does not impact your analytics or previously collected data.

### Does marking a segment inactive affect reports?

No. Inactive segments do not affect any existing reports or analytics. Your historical data remains available even if a segment becomes inactive.
