---
title: Analysing User Ratings in Analytics
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
### Tracking Events

Whenever a user submits the feedback form, the **Rating Submitted** event is triggered. This event includes properties such as *User Rating, Input Type, Comment*.
Refer to the table below for a better understanding of the event properties.

[block:parameters]
{
  "data": {
    "h-0": "Event Name",
    "h-1": "Properties",
    "h-2": "Data Type",
    "h-3": "Sample Value",
    "h-4": "Comments",
    "0-0": "Rating Submitted",
    "0-1": "User Rating",
    "1-1": "Input Type",
    "2-1": "Comment",
    "3-1": "Campaign Id",
    "0-2": "Number",
    "1-2": "String",
    "2-2": "String",
    "3-2": "String",
    "0-3": "3",
    "1-3": "Rating/NPS",
    "2-3": "Awesome product",
    "3-3": "17654",
    "2-4": "512 characters limit"
  },
  "cols": 5,
  "rows": 4
}
[/block]
The event details can then be tracked from the Analytics dashboard.

## Analysis of Data Captured using Ratings Template

1. When a user submits a rating by clicking on Submit button on the Web popup, a Rating Submitted event is triggered.
2. This event is available across the CleverTap platform. It helps in creating targeted segments for users to engage them on various channels based on their rating feedback. 
3. This event can also be used in Analytics for the analysis of data captured through the **Ratings** campaigns. 

Listed below are the steps to perform analysis for some of the key metrics:

1. To view the *Trend* for the number of ratings submitted and Frequency histogram:
  * Go to *Analytics > Events*. 
  * From the event dropdown, search for *Rating Submitted* event and click on **View details**.
  * Under the *Trends & Properties* tab, one can view the trend for the number of ratings submitted on a Daily, Weekly, and Monthly basis.
  * Select Event property as *Ratings* to get a histogram view of the rating scale.

2. To analyze the Average Rating trends
  * Go to *Analytics > Trends*
  * Select the *Rating Submitted event* > *+Summarize by* “User Rating” property and click on **View Trend**
  * Navigate to the *Properties* tab and select *Average of property value* from the *View* dropdown. 
  * You can also analyze the trend of Average Rating on a Daily, Weekly, and Monthly basis.
[block:callout]
{
  "type": "info",
  "title": "Pinning Reports to Dashboards",
  "body": "One can also pin the reports or specific trend charts to a custom dashboard using the pin icon available at the extreme right for monitoring the data at regular intervals."
}
[/block]