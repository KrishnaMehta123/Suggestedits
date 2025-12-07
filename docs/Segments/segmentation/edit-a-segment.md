---
title: Edit a Segment
excerpt: >-
  Learn how to edit Segments in CleverTap to quickly update and apply segment
  changes across Campaigns and Journeys.
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

The Segment Edits feature allows users to modify existing Past Behaviour Segments (PBS) directly within the CleverTap dashboard. This capability enhances operational efficiency by allowing edits to be made once and reflected across all associated entities, such as Campaigns, Journeys, and Product experiences, without the need to recreate or clone segments.

> 📘 **Note**
> 
> Editing is currently supported only for Past Behaviour Segments (PBS).

## Purpose

This feature introduces segment modification support to simplify segment management across multiple use cases.

Segment Edits aims to:

- Reduce operational overhead for marketing teams.
- Ensure consistency across campaigns and journeys using shared PBS segments.
- Minimize errors caused by cloning or duplicating segment definitions.

# Edit a Segment

Editing a segment enables you to refine existing audience definitions without having to start from scratch. You can use this option when you want to adjust targeting rules, update filters, or align segment criteria with new campaign goals, all while preserving linked dependencies and historical context.

1. Navigate to the _Segments_ page of the CleverTap dashboard.
2. Locate your desired Past Behaviour Segment in the list view or open its _Details_ page.
3. Click the three-dot menu beside the segment name.
4. Select **Edit** from the dropdown menu.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0c53e068d95ef7c05957356de2fa4c5a52d724ea40aad650c2a6ded310ec07a9-image.png",
        null,
        "Edit a Segment"
      ],
      "align": "center",
      "border": true,
      "caption": "Edit a Segment"
    }
  ]
}
[/block]


When you click **Edit**, CleverTap confirms that all the Campaigns, Journeys, and Product experiences that reference the segment are updated. This ensures users understand how editing a Segment impacts its dependent entities.

### Steps to Edit

1. Review the dependency list shown in the confirmation modal.

   - Each dependent campaign or journey is listed.
2. Choose one of the following actions:

   - **Edit Segment:** Proceed with editing the segment definition.
   - **Clone Segment:** Create a new version to avoid affecting existing dependencies.
3. Modify any of the following:

   - Include/Exclude conditions
   - Events
   - User properties
4. Click **Save Edits**.
5. Confirm your changes in the confirmation window.
6. Click **Confirm and Save**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4ed57c86375365de78083e58e8158457cb40512b096843be43b9a38b43471022-image.png",
        null,
        "Edit Segment Confirmation"
      ],
      "align": "center",
      "border": true,
      "caption": "Edit Segment Confirmation"
    }
  ]
}
[/block]


### Segment Trend and Insights

- Trend cards display historical data until the next computation cycle updates the values.
- The updated counts and analytics appear in the next scheduled run.
- Insights columns are updated in real time as per the new definition.

> 🚧 Important
> 
> Ensure that segments used in Campaigns or Journeys are referenced segments if you want edits to take effect.

Only users belonging to the same team as the segment owner can edit that segment.  
This ensures that segment edits respect existing access control policies.

# Use Case

A marketer uses a Past Behaviour Segment called _High-Value App Users_ in multiple Campaigns and Journeys. After new engagement rules are introduced, the marketer edits the segment to include users who have completed three or more transactions.

**Result**  
All Campaigns and Journeys using this PBS segment automatically adopt the updated rule set during the next segment computation cycle.

# FAQs

The following are the common FAQs:

### Can I edit Live or other segment types?

No. Editing is currently limited to Past Behaviour Segments (PBS).

### Will my Campaign metrics change immediately after editing a segment?

No. The updated segment definition is visible immediately, but data recalculations occur in the next computation cycle.

### What happens if I clone a segment instead of editing it?

The clone creates a new independent segment. Campaigns referencing the old segment remain unaffected.