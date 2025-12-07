---
title: Analysing User Ratings in Analytics (WIP)
excerpt: Understand how you can analyze user ratings for accurate data analysis
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Tracking Events

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

1. When a user submits a rating by clicking the Submit button on the Web popup, a *Rating Submitted* event is triggered.
2. This event is available across the CleverTap platform. It helps in creating targeted segments for users to engage them on various channels based on their rating feedback. 
3. This event can also be used in Analytics for the analysis of data captured through the **Ratings** campaigns. 

Listed below are the steps to perform analysis for some of the key metrics:

### View Ratings Trend

To view the *Trend* for the number of ratings submitted and Frequency histogram:
   i. Navigate to *Analytics > Events*. 
   ii. From the event dropdown, search for *Rating Submitted* event and click on **View details**.
   iii. Under the *Trends & Properties* tab, one can view the trend for the number of ratings submitted on a Daily, Weekly, and Monthly basis.
  iv. Select Event property as *Ratings* to get a histogram view of the rating scale.

### Analyze Average Rating Trends

To analyze the Average Rating trends:
  i. Navigate to *Analytics > Trends*
  ii. Select the *Rating Submitted event* > *+Summarize by* “User Rating” property and click on **View Trend**
  iii. Navigate to the *Properties* tab and select *Average of property value* from the *View* dropdown. 
  iv. You can also analyze the trend of Average Rating on a Daily, Weekly, and Monthly basis.
[block:callout]
{
  "type": "info",
  "title": "Pinning Reports to Dashboards",
  "body": "One can also pin the reports or specific trend charts to a custom dashboard using the pin icon available at the extreme right for monitoring the data at regular intervals."
}
[/block]
### Analyze Comments

To view and analyze the Comments received:

   i. Navigate to *Analytics* > *Events* 
   ii. Select the *Rating Submitted event*
   iii. To filter the data at a campaign level, add the *Campaign id* filter as show below:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/edf2849-campaign_id.png",
        "campaign id.png",
        2544,
        988,
        "#000000"
      ],
      "caption": "Rating Submitted Data",
      "border": true
    }
  ]
}
[/block]
iv. Click *View details*. 
v. Navigate to *Trend & Properties* 
vi. From the Event property dropdown, select *Comment*
vii. Select the grid view to view all the comments received in tabular format.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/466a94a-comments_received.png",
        "comments received.png",
        2164,
        574,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]
viii. To download the comments, Click **Export as CSV** button available below the grid icon.