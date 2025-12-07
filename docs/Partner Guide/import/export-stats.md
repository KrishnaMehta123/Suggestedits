---
title: Export Stats
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
Exporting data from CleverTap to a third-party raw data or analytics partner such as AWS or GCP enables businesses to leverage comprehensive insights and analytics. This integration supports robust data-driven decision-making, enhances campaign effectiveness, and optimizes user engagement strategies across various platforms.

# Pre requisites

To export data to these partners, the users must integrate the partners under _Settings > Partners_ and then select **Integrate**. Fill in the necessary configuration details like **Bucket Nickname, Bucket URL, Access Key, and Secret Key**.

# Creating an export

1. Navigate to _Settings > Partners_ and select **Exports**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ee4e9d3-Export_Stats_1.png",
        "",
        "Exports"
      ],
      "align": "center",
      "border": true,
      "caption": "Exports"
    }
  ]
}
[/block]


2. Navigate to **Create Export**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9fcedce-Export_Stats_-_create_export.png",
        "",
        "Create Export"
      ],
      "align": "center",
      "border": true,
      "caption": "Create Export"
    }
  ]
}
[/block]


3. Select an integrated partner platform to which the data has to be exported. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/86961ab-Export_Stats_-_select_partner.png",
        "",
        "Integrated Partner Platforms"
      ],
      "align": "center",
      "border": true,
      "caption": "Integrated Partner Platforms"
    }
  ]
}
[/block]


4. The Partner Bucket Name will be auto-filled based on the information filled in during the integration process and in case of multiple buckets, select the relevant Partner Bucket from the drop-down.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/674d155-export_stats_-_partner_bucket.png",
        "",
        "Partner Bucket Name"
      ],
      "align": "center",
      "border": true,
      "caption": "Partner Bucket Name"
    }
  ]
}
[/block]


4. Select a Data Type based on the kind of data that needs to be exported.

- All Events: Export all events for the selected duration. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9a56187-export_stats_-_data_type.png",
        "",
        "Data Types"
      ],
      "align": "center",
      "border": true,
      "caption": "Data Types"
    }
  ]
}
[/block]


- Selected Events: Select the events from the drop-down and export specific data for the selected duration.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a965c82-export_stats_-_data_type_2.png",
        "",
        "Data Type - Selected Events"
      ],
      "align": "center",
      "border": true,
      "caption": "Data Type - Selected Events"
    }
  ]
}
[/block]


- All User Profiles: User profiles will not be available for export stats.

6. Set the priority in the order in which the users will be identified under Identifier \__Priority > Fallback priority order \_for identifiers_. User profiles can be identified by Identity, Email, and Phone Number. In case the identifier set as first priority is not available, the identity column in the export file will display the second priority identifier, and so on.

For Example, if the first priority is set to Identity, the second priority is set to Email, and the third priority is set to Phone Number, then in the user profile, if Identity is not available, the specific cell for the particular user in the Identity column will reflect Email, and if Email is not available, then the export will fetch the Phone Number.

> 📘 Fallback Priority Order
> 
> The default priority is set to identity in case no order of priority is set.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/14e18c7-2024-07-15_12-29-15_1.gif",
        "",
        "Fallback priority for identifiers"
      ],
      "align": "center",
      "border": true,
      "caption": "Fallback priority for identifiers"
    }
  ]
}
[/block]


7. Set the export frequency as **One Time** or **Recurring**. Data can be exported only up to the last 60 days.

- One Time: Select the to and from dates to export the data once. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a6110af-2024-07-15_12-35-20_1.gif",
        "",
        "One Time Export"
      ],
      "align": "center",
      "border": true,
      "caption": "One Time Export"
    }
  ]
}
[/block]


- Recurring: Schedule regular data exports at specified intervals every four hours. This automated process ensures that updated data is consistent. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/187f2fb-2024-07-15_12-40-36_1.gif",
        "",
        "Recurring Export"
      ],
      "align": "center",
      "border": true,
      "caption": "Recurring Export"
    }
  ]
}
[/block]


8. Select the export format as **CSV**, **Parquet**, **XML**, or **JSON**; if no format is selected, JSON is the default.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/10a748c-export_stats_-_format.png",
        "",
        "Export Format"
      ],
      "align": "center",
      "border": true,
      "caption": "Export Format"
    }
  ]
}
[/block]


8. Export as a string: 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3dbfb9d-2024-07-15_12-45-57_1.gif",
        "",
        "Export as a string"
      ],
      "align": "center",
      "border": true,
      "caption": "Export as a string"
    }
  ]
}
[/block]


8. Select **Export**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9ed3194-export_stats_-_export.png",
        "",
        "Export"
      ],
      "align": "center",
      "border": true,
      "caption": "Export"
    }
  ]
}
[/block]


8. On the dashboard, the status of the export will be Pending, and once the export starts based on the type of export - One Time or Recurring, the status will change to Done, Running, or Stopped.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/114cba9-export_stats_-_status.png",
        "",
        "Status"
      ],
      "align": "center",
      "border": true,
      "caption": "Status"
    }
  ]
}
[/block]


# Dashboard

## Set up

1. Navigate to the Stats Dashboard, click on ![](https://files.readme.io/1ede62e-export_stats_-_view_icon.png) and then select **Setup**. You can edit your export by selecting** Edit**. This page will provide comprehensive details about the export, including: 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b7c7844-export_stats_-_edit.png",
        "",
        ""
      ],
      "align": "center",
      "border": true,
      "caption": "Setup and Edit"
    }
  ]
}
[/block]


1. <br />
   1. **Partner Bucket Name**: This refers to the nickname assigned to the partner during the export creation process. This is an editable field. 
   2. **Data Type**: Specifies the category of data to be exported, including All Events or Selected Events. This is an editable field. Export Stats for User Profiles is not available. Therefore, the Data Type cannot be changed from Events to User Profiles.
   3. **Fallback Priority for Identifiers**: User profiles can be identified by Identity, Email, and Phone Number. This is an editable field; more identifiers can be added as a fallback if only one has been selected.
   4. **Frequency**: Indicates whether the export is set to occur One Time or Recurring. The frequency of the Recurring export is editable. 
   5. **Format**: Indicates the file format for exporting the stats, such as CSV, JSON, Parquet, or XML. This is an editable field.
2. Navigate to the Stats Dashboard, and click on Stop Export, to stop the generation of exports from the next cycle. 

## Stats

1. Navigate to the Stats Dashboard, select ![](https://files.readme.io/2ed6cec-export_stats_-_view_icon.png) , and select **Stats**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5ee4c59-export_stats_-_view_stats.png",
        "",
        ""
      ],
      "align": "center",
      "border": true,
      "caption": "View Export"
    }
  ]
}
[/block]


### One Time Export

1. The dashboard will show export data based on dates when data was available for export. For example, if a user sets up a One-Time export covering the last 60 days but no data was available for the first two days, the dashboard will only display dates when data was available and exported. 
2. When you click on a date, a panel on the right will display a list of all the events, along with the total count of the number of times the event was performed and a sum total of the counts of all events.
3. Navigate to **Filter** to filter by dates. Select any range of dates from the start of the export to the current day and **Apply** filter.

### Recurring Export

1. The dashboard will show export data based on dates when data was available for export. An export file for each date with stats will be displayed. 
2. Select the date and each date will display the events for which the export was created. 
3. Next to the event: 
   1. A total count of the number of times the event has been performed for the specified time frequency will be shown next to each timestamp.
   2. The total number of time stamps available for that particular event will be displayed.

<!----->

3. Select an event to expand and view its timestamps. For instance, with a recurring export set every 4 hours, timestamps such as 4:00, 8:00, 12:00, 16:00, 20:00, and 00:00 in 24-hour format will be displayed for the selected date. It will show the total number of times the event occurred at each timestamp/frequency, as well as a total count for how many times the selected event occurred throughout the day. If no events have been performed for a particular time stamp, the total count will be 0. 
4. Once you select the event, the right panel will display a filter containing timestamps based on the frequency chosen for export. For example, a recurring export set for every 4 hours will have filters for timestamps like 4:00, 8:00, 12:00, 16:00, 20:00, and 00:00 in 24-hour format for the selected date. If the event occurs 3 times at 8:00, the filter will only show 8:00 with the total count of the number of times the event has been performed i.e., 3, or it will display a count of 0 against each timestamp where the event did not occur. (@nishu please confirm). 

> 📘 Back Dated Events
> 
> If any events are missed or not included during an export run, such as when the 4:00 stats show 30 'Added to Cart' events but the export displays only 28, the missed events (in this case, 2) will be added to the total count in the next export. Therefore, for the 8:00 stats with originally 15 occurrences of 'Added to Cart' events, the displayed count will be 15 + 2, totalling 17.

5. Navigate to **Filter** to filter by dates and Event Type. 
   1. Filter by Dates: Select any date range from the start of the export to the current day and **Apply** filter.
   2. Filter by Events Type: Choose from a list of events using a search bar to find specific events. You can select multiple events and **Apply** filter.

> 📘 Data Storage
> 
> CleverTap will only store data for 30 days for both Recurring and One Time exports. In the case of a 60-day One Time export, the most recent 30-day export data will be available.