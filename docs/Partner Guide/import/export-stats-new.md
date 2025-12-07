---
title: Export Stats (New)
excerpt: >-
  Learn how to seamlessly export data from CleverTap to third-party platforms
  for enhanced analytics and insights.
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

Exporting data from CleverTap to third-party platforms like AWS or GCP enables businesses to gain deeper insights and analytics. This integration supports data-driven decisions, enhances campaign performance, and optimizes user engagement strategies.

# Prerequisites

To enable data export, navigate to _Settings > Partners_, select _Connections_, and provide the necessary configurations, including **Bucket Nickname, Bucket URL, Access Key, **and **Secret Key.**

# Create Export

Create Export allows you to configure data transfer to third-party platforms. To create an export on the CleverTap dashboard, follow these steps:

1. Navigate to _Settings > Partners_ and select _Exports_center_.
2. Select _Create Export_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f72cc0d793f71505ca07c57536d642bb2602a615dd4d6ebedf2406c044fb2ea0-image.png",
        null,
        "Create Export"
      ],
      "align": "center",
      "border": true,
      "caption": "Create Export"
    }
  ]
}
[/block]


3. Select an integrated partner platform for the data export.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7c1d0c3fb1409b6207f7df352c7ccd239312cc9176e249312f727a74c5ab38d8-image.png",
        null,
        "Integrated Partner Platforms"
      ],
      "align": "center",
      "border": true,
      "caption": "Integrated Partner Platforms"
    }
  ]
}
[/block]


4. The **Partner Bucket Name** is auto-filled based on the details provided during integration. Select the relevant one from the drop-down menu if there are multiple buckets.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/240817de68b5b32c4ff4ade4491c3ad32c15afaf0d1895e22a0f917265f69a8c-image.png",
        null,
        "Partner Bucket Name"
      ],
      "align": "center",
      "border": true,
      "caption": "Partner Bucket Name"
    }
  ]
}
[/block]


5. Select Export Data Type based on the data that needs to be exported.

- **All Events:** This exports data for all defined events, including System and Custom events.
- **Select Events: **This exports specific events you want to export.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/671dbeaf8adb1649517986d5118b6e08e3548f059dd9f99388dc76ffd868b9bb-image.png",
        null,
        "Data Type - Selected Events"
      ],
      "align": "center",
      "border": true,
      "caption": "Data Type - Selected Events"
    }
  ]
}
[/block]


- **All User Profiles:** This exports all your user profile data.

6. Set the priority order for identifying users under _Identifier Priority > Fallback Priority Order for Identifiers_. User profiles can be identified using _Identity_ and _Phone_ (only two priority identifiers can be set). If the first priority identifier is unavailable, the system will use the second priority identifier in the exported data.

**Example:**  
If the first priority is set to _Identity_ and the second priority is set to _Phone_, but a user's _Identity_ is unavailable, the _Identity_ column in the export file will display the _Phone_ number instead.

> ℹ️ Fallback priority order for identifiers
> 
> The default priority is set to _Identity_ in case no order of priority is set.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ad58b6aa35c08099ec52a5a77d6dfd17d1e1e27c363f83c1d28d43385ace0ac6-2024-12-11_20-22-44_1.gif",
        null,
        "Fallback priority for identifiers"
      ],
      "align": "center",
      "border": true,
      "caption": "Fallback priority for identifiers"
    }
  ]
}
[/block]


7. Set the export _FREQUENCY_  to either **One Time** or **Recurring**, with data export available only for the last 60 days:

- **One Time:**

  - This option allows you to export data for a specific time range.
  - Select the start date and end date using the date picker.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a5dfad3920e695d2f444905bd7b238eabbc40dbbceac5d9b5ad5c057e7a8b788-2024-12-11_20-55-38_1.gif",
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


- **Recurring:**
  - This feature enables scheduled, automated exports at regular intervals.
  - The recurrence intervals can be set from 4 to 24 hours, ensuring data is updated and exported consistently.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b27ba8fe7b10ff09d1fefc02aaed5aa554c30888db91d1f29f2e02d86b66923b-2024-12-11_21-00-00_1.gif",
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


8. Select from the export formats **CSV**, **Parquet**, **XML**, or **JSON**. If none is selected, **JSON** is the default format.
9. Export Data Type: Select either _As string_ or _CleverTap ID_ or both options.
10. After selecting, click the _Export_ button to initiate the export process.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/daa8b6726db9def06c864a264e32f5ce3b6b7d5cc0ae71ab96a0cb2e0bb9b00a-image.png",
        null,
        "Export"
      ],
      "align": "center",
      "border": true,
      "caption": "Export"
    }
  ]
}
[/block]


11. The export's status on the dashboard will be Pending. Once the export starts, based on the Frequency **One time** or **Recurring**type, the status will change to **DONE**, **PENDING**, or **STOPPED**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ccbdf1d35006804356211f45088aa9cdc5a753b398aa8341e0fb7485252eb000-image.png",
        null,
        "Status"
      ],
      "align": "center",
      "border": true,
      "caption": "Status"
    }
  ]
}
[/block]


# View Export Stats

1. Navigate to _Settings > Partners_ and select _Export_center_.
2. Select the **Export** you want to review from the list by scrolling through or searching for specific entries.

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


3. Navigate to _Filter_ to filter by **PARTNER**, **TYPE**,**FORMAT**, **STATUS**, **FREQUENCY**, and **EXPORTED ON** (Date).

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


4. Select the desired export, and the Export Page will open. Navigate to the _Stats_ section on this page.

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


5. **Stats** section displays export data summarized by **Export Date** and **Total Count**.

- Each export data entry can be expanded to view a breakdown of the event types and their corresponding total counts for that specific date

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e80f2a2b1842242bfc907a10b2016a902260a423bb7e92f716120668ecceb1e0-image.png",
        null,
        "View Stats"
      ],
      "align": "center",
      "border": true,
      "caption": "View Stats"
    }
  ]
}
[/block]


> 📘 Back Dated Events
> 
> If events are missed during an export, the missed count will be added in the next export. For example, if 28 out of 30 'Added to Cart' events are exported, the remaining 2 will be added to the next export. This ensures accurate data in subsequent exports.

6. **Filtering Options**
   - **Filter by Dates**: Select a date range from the start of the export to the current day and apply the filter.
   - **Filter by Event Type**: Select specific events from the list using a search bar. You can choose multiple events and apply the filter.

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
      "caption": "Event and Date Filtering"
    }
  ]
}
[/block]


7. Select an event type to view its details. The total count for a particular time interval can be viewed, giving detailed insights into the event's distribution over different time ranges.

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


8. Use the _Filter_ option to apply filters for specific time intervals to view the corresponding event counts.

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


> 📘 Data Storage
> 
> CleverTap will only store data for 30 days for both Recurring and One Time exports. In the case of a 60-day One Time export, the most recent 30-day export data will be available.

# Edit Export

Edit Export allows you to modify the settings of an existing export, such as selecting a partner, choosing the data type, updating identifiers, adjusting the frequency, and changing the file format.

1. Navigate to the Stats Dashboard and click **Edit** to modify the export settings.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/efb1431e10d03536271b8a6501dfeffd2b8ab880cc9a97c59f0cee1a5f408bcd-image.png",
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


2. The Export settings page provides details about the export, which can be modified, including:

| **Setting**                           | **Description**                                                                                           |
| ------------------------------------- | --------------------------------------------------------------------------------------------------------- |
| **Partner Bucket Name**               | Select a partner from the drop-down if it's not the default option.                                       |
| **Data Type**                         | Choose a category. You can edit only "All Events" or "Selected Events". User profiles cannot be modified. |
| **Fallback Priority for Identifiers** | Edit identifiers such as Identity and Phone Number.                                                       |
| **Frequency**                         | You cannot change the frequency (One-Time or Recurring); you can only modify the export time or date.     |
| **Format**                            | Change the export file format to CSV, JSON, Parquet, or XML.                                              |
| **Export Data**                       | Modify the selection by choosing or removing As strings or CleverTap ID to export.                        |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e729036cb608e14782f66c806146013baca76a61ea8de6e5b41fd74ff1090556-image.png",
        null,
        "Export Details"
      ],
      "align": "center",
      "border": true,
      "caption": "Export Details"
    }
  ]
}
[/block]


# Stop Export

Allows users to cancel or halt an ongoing export process, preventing further data from being exported.

1. Go to the Stats Dashboard and click **Stop Export** to halt future exports. A confirmation box will appear, prompting you to confirm the action.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c38ae12c33beac818afae11c5af14ac184d36ae73c9dab07791f60190c6d74ea-image.png",
        null,
        "Stop Export"
      ],
      "align": "center",
      "border": true,
      "caption": "Stop Export"
    }
  ]
}
[/block]