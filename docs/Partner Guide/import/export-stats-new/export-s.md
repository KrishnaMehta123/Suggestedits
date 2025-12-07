---
title: View Export Stats With Use Case
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

Learn how to navigate and analyze export data, apply filters, and view detailed breakdowns of events and counts in CleverTap's Export Center.

# Access the Export Center

1. Navigate to _Settings > Partners_ and select _Export Center_.
2. Select the export to review from the list by scrolling or using the search bar.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4e25bd5c518a09a75426d8aa08648fdd73000e6ceb929847e94f464d36f436d0-image.png",
        null,
        "Stats Dashboard"
      ],
      "align": "center",
      "border": true,
      "caption": "Stats Dashboard"
    }
  ]
}
[/block]


3. **Apply Filters**

- Use the _Filter_ option to refine exports based on Partner, Type, Format, Status, Frequency, and Exported On (Date).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9246c7eb2388a162541946ca4d91b2ee3c84fd2494054dc4ab1e4bcbedffa59a-2024-12-12_00-10-02_1.gif",
        null,
        "Filters"
      ],
      "align": "center",
      "border": true,
      "caption": "Export Filters"
    }
  ]
}
[/block]


# Frequency: Data Export Options

CleverTap’s export features enable marketers and analysts to seamlessly retrieve event data, ensuring timely insights for campaign optimization and business analysis. Choose between two types of export options based on specific requirements: **[One-Time Export](https://staging.docs.user.clevertap.net/docs/export-s#one-time-export)** and **[Recurring Export](https://staging.docs.user.clevertap.net/docs/export-s#recurring-export)**.

## One-Time Export

The One-Time Export feature enables users to retrieve event data for a specific date range or week and displays data on a day-wise basis.

### Use Case:

A marketer analyzing campaign performance for a specific date or week can determine which campaigns generated the most engagement by exporting event data, such as the number of notifications sent or UTM visits.

### Key Details:

- Select One-Time export when creating the bucket to configure this option.
- Data can be exported for specific dates, such as a single day or an entire week.
- Use the date picker to define the export's start and end dates.
- The export will show data segmented by each day within the selected range.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a49d7cd42b7a2f9b21f93e265c4f4b381ed24506be2db105da9c1dc140f435ef-image.png",
        null,
        "One Time Export"
      ],
      "align": "center",
      "border": true,
      "caption": "One Time Export"
    }
  ]
}
[/block]


## Recurring Export

The Recurring Export feature enables users to automate event data retrieval at regular intervals.

### Use Case:

An analyst monitoring daily sales performance for a subscription-based SaaS product ensures their reporting dashboard remains updated by automating data exports to run every 8 hours.

### Key Details:

- Select _Recurring export_ when creating the bucket to configure this option.
- Scheduled, automated exports can be set to occur at regular intervals.
- Recurrence intervals can range from 4 to 24 hours, ensuring data remains up-to-date.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ad1af78e656f5fec82e58a65368207a1f0ca6656f462d0b2f7c38278957d193a-image.png",
        null,
        "Recurring Export"
      ],
      "align": "center",
      "border": true,
      "caption": "Recurring Export"
    }
  ]
}
[/block]


# View Stats

The View Stats section serves as a unified hub for analyzing exported data. Whether users rely on **[One-Time Export](https://staging.docs.user.clevertap.net/docs/export-s#one-time-export) **or **[Recurring Export](https://staging.docs.user.clevertap.net/docs/export-s#recurring-export)**, this section helps track, filter, and gain insights into data effortlessly.

- Select the desired export to open the Export Page.
- Navigate to the Stats section to analyze data.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8feea376516c73341ed66012340e8d3c32f7685a2343f54af77464bb1e1206f4-image.png",
        null,
        "Stats"
      ],
      "align": "center",
      "border": true,
      "caption": "Stats"
    }
  ]
}
[/block]


# Stats Overview

The type of export determines how stats are displayed:

- **For [One-Time Export](https://staging.docs.user.clevertap.net/docs/export-s#one-time-export):**
  - View the **Export Date** for each export.
  - Analyze the **Total Count** of events exported for specific dates.
- **For [Recurring Export](https://staging.docs.user.clevertap.net/docs/export-s#recurring-export):**
  - View data by **Time Intervals** to analyze event counts within specific recurring periods.

Expand any entry to delve deeper into specific Event Types and their counts for selected dates or intervals.

> 📘 Backdated Events
> 
> If events are missed during an export, the system adds the missed count to the next export. For example, if 28 out of 30 "Added to Cart" events are exported, the remaining 2 will be included in the subsequent export, ensuring data accuracy.

# Filtering Options

Filters narrow down data to focus on relevant aspects. Different filters are available depending on the type of export:

- **For [One-Time Export](https://staging.docs.user.clevertap.net/docs/export-s#one-time-export)**
  - **Filter by Dates**: Select a date range from the start of the export. Analyze data for specific date range with Event type.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1de39d0cd939c031896700cabb8cc951271cc576cf8a59b6c23fb4883f38b39a-2024-12-13_17-16-15_1.gif",
        null,
        "Event And Date Filtering"
      ],
      "align": "center",
      "border": true,
      "caption": "Filter for Event and Date "
    }
  ]
}
[/block]


- **For [Recurring Export](https://staging.docs.user.clevertap.net/docs/export-s#recurring-export)**
  - **Time Interval Filters**: Focus on specific time intervals by selecting them. View corresponding event counts for the chosen periods.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/89bc1b418bb91793580e8cdd918597529fe570225a997c3127112b195c72d27b-2024-12-13_17-02-08_1.gif",
        null,
        "Filters for Time Interval"
      ],
      "align": "center",
      "border": true,
      "caption": "Filters for Time Interval"
    }
  ]
}
[/block]


> 📘 Blue Numbers in Time Intervals
> 
> Blue numbers show the number of data points in each interval. For example, for the time interval 12:00 -08:00, a blue "6" indicates 6 data points within this range.

# Detailed Insights

For in-depth data exploration, use the Detailed Insights feature:

- Select an **Event Type** to view its details.
- Analyze the **Total Count** for specific time intervals, identifying trends and event distribution.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7a938d8bccb28240fc34d07be8a2bd81eb6c435ac0f80c00578a2371ac06cd31-image.png",
        null,
        "Event's distribution"
      ],
      "align": "center",
      "border": true,
      "caption": "Event's distribution"
    }
  ]
}
[/block]


> 📘 Data Storage
> 
> CleverTap stores export data for 30 days for both [One Time Export](https://staging.docs.user.clevertap.net/docs/export-s#one-time-export) and [Recurring Exports](https://staging.docs.user.clevertap.net/docs/export-s#recurring-export).