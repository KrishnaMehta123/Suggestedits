---
title: Trends Beta Backup Page
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

CleverTap's Trends feature provides advanced tools for analyzing and visualizing data, offering a comprehensive understanding of user behavior. The key functions include the following:

* *Selection Capabilities*: Users can choose event-level data, event properties, and user properties and specify analysis periods for deeper insights.
* *Advanced Filtering and Segmentation*: Robust filtering options and the ability to segment data for a targeted analysis.
* *Visualization Tools*: Trends can be visualized using various metrics, such as trendlines, conversion metrics, anomaly detection, and retention metrics.

These capabilities give users a powerful way to optimize platform usage and enable them to make informed decisions to drive business outcomes.

Using the *Trends* dashboard, users can:

* Plot and analyze trends of event occurrences.
* Compare trends of multiple events to uncover patterns.
* Examine trends across different event property values.
* Compare event trends by user properties.
* Summarize trends using event properties.
* Compare trends across multiple segments.

# Getting Started

The Trends dashboard enables you to visualize data by segmenting events based on event properties and user-defined segments. You can further refine these segments by splitting them based on user properties.

Results can be displayed in various formats, such as trendlines, pie charts, and more, and can be viewed over different time periods, including days, or months. You also have the option to download the resulting visualizations or pin the analysis to a board for continuous updates.

> 📘 Event and Segment Limit
>
> You can select up to five events and five segments for analysis.

<Image alt="Trend Analysis" align="center" border={true} src="https://files.readme.io/79923bce74d05b0178c3541a856d3dc7bc7315b9d7ea2b06e75e5fb0e7668587-image.png">
  Trend Analysis
</Image>

# View a Trend

To set up a trend analysis, select the event you would want to analyze. You can also restrict your analysis further to a specific property of that event.

To view a trend:

1. Go to *Analytics* > *Trends* and select an event to analyze from the *EVENTS* section to view a trend. For example, you want to analyze all the users who launched the app.
2. Click **View Analysis**. 

<Image alt="View a Trend" align="center" border={true} src="https://files.readme.io/f07eb1911a1e56da4f0f3fbe668a21f313b57abfd37ce778851a4fd5beeb5c0c-View_Trends_Main.jpg">
  View a Trend
</Image>

The trend results are displayed. Hovering over the trendline shows the percentage increase or decrease for the selected time frame and other event information. 

You can change the view period of the trend on a daily or monthly basis:

<Image alt="Viewing period" align="center" border={true} src="https://files.readme.io/4430a0dfe39b74984c3aa6b32c7e07ac3f23831f4c38b5838a148f3755d33ea6-image.png">
  Viewing period
</Image>

* *Daily*: The trend and data points are plotted on a daily basis. 
* *Monthly*: The trend and data points are plotted on a daily basis.

## Event Count

To measure the event count:

1. Go to *Analytics* > *Trends* and select an event to analyze and view a trend. 
2. From the *MEASURE* section, select any one of the following:
   * *Total Events*: This measure displays the sum of events in the specified period. If an event is performed multiple times, each occurrence is accounted for separately in the total count. For example, if user A performs an event in Day 1 and again in Day 2, the *Total Events* count will be cumulative, showing 2 for those two days combined.
   * *Unique Users*: This measure displays the trend for the number of unique users who performed the chosen events in the selected period. The *Unique Users* column in the table shows the unique users that have performed the event, property, and segment combination in the entire period selected from the date picker. For example, if user A has done the event on Day 1 and Day 2, the user is counted once each day. However, user  A is counted only once in the *Unique User* column.
3. Click **View Analysis**.

### View Event Count

To view the event count, hover over any trendline.  For example, the number of *App Launched* events that occurred in the selected period. (This is repeated information - we have already stated earlier - hovering on the data point gives this information.)

<Image title="View Trends Stats Event Count" alt="Event Count in Trend" align="center" border={true} src="https://files.readme.io/70480afa9d9015cab6214c0125afc565dce5e92374cb17b13880b8da5cc70079-View_Trends_Main.jpg">
  Trend Event Count
</Image>

The stats available are:

* Total events: Sum of events in the selected period.
* Daily change: The change in percentage from the previous time period, that is, day, or month.

# Pin or Download Trends

Pinning a trend to a board helps you continuously monitor changes to your KPIs. You can select a specific time period, such as the past three months, to view and track your selected events over time. 

To pin a trend to a board:

1. **Plot a Trend**\
   First, plot the trend for the event(s) you wish to track.
2. **Export the Trend Analytics**\
   Click the download icon to export the trend analytics. You can export the visual representation as a PNG or PDF file, while the data table can be exported as a CSV file.
3. Click **Add to Board** to pin the trend to a board.

<Image alt="Download or pin the Trend" align="center" border={true} src="https://files.readme.io/b5b4d39bf134251453092e3481fd1e0c35371a76c2d0d56918115cd0901d5732-image.png">
  Download or Pin the Board
</Image>

The trend is added to the board.\
\{@sunil to add zoomed out version of the pinned board}

<Image alt="Pinned Trend" align="center" border={true} src="https://files.readme.io/97a2aad557c6d76aad69ff025f0de98566f8e1616ee2dc1de64f33dd65fe7f81-image.png">
  Pinned Board
</Image>

You can decide on the visualization for the plotted trend. You can view the trends as:

* Number: A quick snapshot of your KPIs. This visualization is useful for pinning your KPIs to a board and regularly tracking them.
* Line - This visualization is useful when comparing multiple trends. This is the default visualization. 
* Bar: This visualization is useful for trend split and viewing relative differences.

# Compare Trends for Events

You can compare trends for multiple events. For example, you can understand the correlation between two events, such as App Launched and Notification Viewed.

To view a trend, perform the following steps:

1. Go to *Analytics* > *Trends* and select an event to analyze and view a trend. You can also filter your analysis further by the event property. 
2. Click **Add Event** to add another event for comparison. 
3. Click **View Analysis**. 

<Image title="Select Trend Options and Click View Trend" alt="Compare Trends for different events" align="center" width="100%" border={true} src="https://files.readme.io/9123233f0a9485ce41f62ece0f3a3f26421a450f9da8233d9bf4933d4c16384d-Compare_Trends.jpg">
  Compare Trends
</Image>

## Filter by Event Property

When selecting an event for analysis, you can restrict the search criteria by filtering based on the specific event properties. All subsequent analyses are performed using these filtered event properties, while other properties of the selected event are excluded. 

 To filter a trend by event property:

1. Go to *Analytics* > *Trends* and select an event to analyze from the *EVENTS* section and view a trend. For example, you want to analyze only those users who viewed In-App notifications. 
2. Click **+ Filter** to filter by an event property, that is, In-app. 
3. Click **View Analysis**.

The resulting trend filters users who viewed notifications from an in-app notification. It does not include users who viewed other types of notifications, such as Email or Web. Any further analysis of this event will focus exclusively on users who viewed notifications from the In-App campaign. 

<Image alt="Filter Event by Property" align="center" border={true} src="https://files.readme.io/0ae068a6ae0702833c24dff297308064596016dc0cd218f9416d585b4b4028ff-Trends_filter_by_event.jpg">
  Filter Event by Property
</Image>

## Split by Event Property

You can split the analysis of your event based on specific event properties. For example, consider the `Charged` event, which indicates a user has made a purchase. You can split this event by its underlying properties, such as `Payment Mode` and `Amount`. This divides your single `Charged` trend line into multiple lines, with each trend line representing the value of a different event property. This allows you to visualize the payment method preferred by your users.

To split a trend by event property: 

1. Go to *Analytics* > *Trends* and select an event to analyze and view a trend. For example, `Charged`. 
2. Click **+ Split by** to divide the trend by the event properties, such as `payment method`.
3. Click **View Analysis**. 

<Image alt="Compare trends by event properties" align="center" border={true} src="https://files.readme.io/d5b72c9af7314d6543c2acc901717ba58a02e2d1c194ce415390b80799b7ee36-image.png">
  Compare trends by event properties
</Image>

The trend for each event property is displayed. 

All the split event properties are listed at the bottom of the right pane. You can perform the following actions:

* Use the search box to find specific event properties.
* Select or deselect event properties from the trend by selecting the corresponding boxes.
* Sort the event properties from highest to lowest values, or vice versa, by clicking the arrows.

> 📘 Maximum Split
>
> You can split an event by up to two event properties at a time.

# Compare Trends for Segments

You can compare your event trend across different user segments. For example, you could compare the App Uninstalled event trend across segments, such as *Loyal Customers,* *Champion Users*, and *Match Day Players*. The differences in the segment trends could reveal variations in user behavior, providing invaluable insights. For instance, if a significant number of Booster Abandoners are uninstalling the app, it may indicate a need for alternative engagement strategies rather than simply offering them game boosters.

To compare trends across segments, perform the following steps: 

1. Go to *Analytics* > *Trends* and select an event to analyze and view a trend. You can also filter your analysis further by the event property.
2. Click **Add Segment** from the *SEGMENT* section.
3. Select a segment from the list or create an ad-hoc segment. For more information, refer to [Segments](doc:segments).
4. Click **View Analysis**. 

<Image alt="Compare Trends Across Segments" align="center" border={true} src="https://files.readme.io/372d2522452f6264308263ee5c232a65feca2aef22f238c82cb8e5c4433993ba-image.png">
  Compare Trends Across Segments
</Image>

The results are displayed. 

> 📘 Comparison Considerations
>
> When comparing, consider the following:
>
> * You can compare a saved or an ad-hoc segment. 
> * You can compare a maximum of five segments.
> * You cannot simultaneously split the trend by user property and compare the trend by segments.

## Split by User Property

You can analyze a trend based on the specific user properties. For example, consider the event `Charged`, which indicates that the user has started watching content. Here, you can split this trend based on the underlying user property, such as `Customer_Type`.

This splits your single `Charged` trend line into multiple trend lines, such that each trend line references the user property value. For example, the user property `Customer_Type` is split by user property values such as *Platinum*, *Silver*, and so on. 

To split a trend by user property, perform the following steps: 

1. Go to *Analytics* > *Trends* and select an event to analyze and view a trend.
2. Select the user property from the *Split by user* property list under the *SEGMENT* section
3. Click **View Analysis**. 

<Image alt="Split Segment by User Property" align="center" border={true} src="https://files.readme.io/1729dee2d0d09682ba1fcef09cfdad337364111ec2c738a9271690c1cb046d75-image.png">
  Split Segment by User Property
</Image>

The trend for each user property displays.  All the split user properties are listed at the bottom. You can do the following:

* Search through the listed user properties using the search box.
* Select or clear the user properties from the trend by selecting the specific checkbox.
* Sort the user properties from highest to lowest value and vice versa using the arrows. 

> 📘 Maximum Split
>
> You can split by a maximum of two user properties. Split by properties is not available when comparing two or more segments.

## Adhoc Segments

You can use available user segments or create ad-hoc segments in run time when performing a trend analysis. 

To create adhoc segments, follow these steps:

1. From the SEGMENT section, click the edit icon. 

<Image alt="Create Adhoc Segment" align="center" width="40% " border={true} src="https://files.readme.io/3eb2702d462e999b6155fa3b76bce5ff4dd9efb5e9265c676f5ef8bb7d452046-image.png">
  Create Adhoc Segment
</Image>

2. Click the Add Rule button to add a condition or click [Add Rule Group](https://docs.clevertap.com/docs/segmentation-rules) to add multiple conditions. 

<Image alt="Add Rules" align="center" width="70% " border={true} src="https://files.readme.io/0f6c55c2577f3d86d157776fcb521eff4938a783049e90261cd57c621105ee11-image.png">
  Add Rules
</Image>

For information about using segmentation, refer to [Segmentation](https://docs.clevertap.com/docs/segmentation).
