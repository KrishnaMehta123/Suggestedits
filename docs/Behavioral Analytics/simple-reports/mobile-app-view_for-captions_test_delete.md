---
title: Mobile App View_for captions_test_delete
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

The *Mobile App* dashboard shows various metrics related to app usage, user retention, engagement, and conversion across mobile platforms.

Navigate to *Boards* > *Mobile App*.

 * *Daily Active Users*, *Weekly Active Users*, and *Monthly Active Users* represent users who have launched your application at least once during the respective *Daily*, *Weekly*, and *Monthly* time period.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d331003-DAUMAUWAU.png",
        "DAU,MAU,WAU.png",
        747,
        213,
        "#000000"
      ],
      "border": true,
      "sizing": "80",
      "caption": "DAU, WAU, and MAU"
    }
  ]
}
[/block]
The *Quick View* shows:

## Active Users
1. Select the required segment under *For Segments*.
2. Select the date range.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/33f145e-Date_Range.png",
        "Date_Range.png",
        2420,
        718,
        "#f9f9fb"
      ],
      "sizing": "original",
      "border": true,
      "caption": "Date Range for Segment"
    }
  ]
}
[/block]
This shows: 
  * *Total users*- Total number of users who launched the mobile app in the selected time period.
  * *Average users*- Displays data based on the **Time Interval** selection, shown in![One](https://files.readme.io/07d4443-one.png) below.
    *  For *Daily* time interval, it shows the average daily users for the selected date range.
    *  For *Weekly* and *Monthly* intervals, it shows the number of users who launched the mobile app in the last 7 days and 30 days, respectively, of the selected date range. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/26fa986-Active_Users.png",
        "Active_Users.png",
        2418,
        1046,
        "#f8f8fa"
      ],
      "border": true,
      "sizing": "original",
      "caption": "App Launch Trend"
    }
  ]
}
[/block]
 ## Conversions
This shows the total number of users who have performed the conversion event ( set under “Settings > Schema > Events > Conversion event ) within the selected time period.
It also displays data based on the **Time Interval** selection, shown in![One](https://files.readme.io/07d4443-one.png) above.
For *Daily* time interval, it shows the average daily conversion for the selected date range.
For *Weekly* and *Monthly* intervals, it shows the total number of converted users in the last 7 days and 30 days, respectively, of the selected date range.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/11d7c44-Conversions.png",
        "Conversions.png",
        2340,
        864,
        "#f9fafa"
      ],
      "border": true,
      "sizing": "original",
      "caption": "Conversion Trend"
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "Note",
  "body": "The number of users is displayed as NA (Not Applicable) if the selected date range is less than a week or a month and the interval filter is set as weekly or monthly, respectively.\nIf the selected date range is less than a week with the time interval as “weekly”, then both “Last 7 days’ users” and “Last 30 days’ users” will not be applicable and is displayed as NA."
}
[/block]
## Distribution by App Version
This shows the distribution of users by the version of the App being used. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0ea452f-Dist_app_version.png",
        "Dist_app_version.png",
        1169,
        393,
        "#f7f8fd"
      ],
      "border": true,
      "sizing": "original",
      "caption": "User Distribution by App Version"
    }
  ]
}
[/block]
## User Retention And Conversion
This shows detailed metrics on *1, 3, and 7-day *Retention*, *Engagement* and *Conversion* percentages, reflecting the percentage of new users who return to your application, meaningfully engage with your application, and convert into paying (or another conversion metric you choose) users, respectively, during the first 1, 3 and 7 days after first use.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f978b4e-User_rention.png",
        "User_rention.png",
        1173,
        261,
        "#fafafb"
      ],
      "sizing": "original",
      "border": true,
      "caption": "Retention and Conversion by Date Range"
    }
  ]
}
[/block]
For detailed analysis, click *More*  

## App Launched vs Conversions
This displays a comparison of users who have launched the app vs users performing the conversion event.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/84adb06-AppL-VsC.png",
        "AppL-VsC.png",
        1211,
        488,
        "#fafbfc"
      ],
      "sizing": "original",
      "border": true,
      "caption": "App Launch vs Actual Conversion"
    }
  ]
}
[/block]
## Usage and Revenue Trends
This shows you the following metrics based on selection.
  * *Daily Paying Users*/*Daily Active Users (DPU/DAU(%)*) and *Daily Paying Users*/*Monthly Active Users (DPU/MAU(%)*) epresent users for whom you have raised the *Charged* event (or users qualifying as per the conversion event) at least once during the relevant time period.
  * *Average Revenue Per Daily Active User (ARPDAU)* which gives a sense of revenue earned on a daily basis per user from your application.
  * *Average Revenue Per Daily Paying User (ARPDPU)* which gives a sense of average daily revenue from a paying user in your application.
  * *Daily Active Users*/*Monthly Active Users(DAU/MAU(%)*), also known as *Sticky Quotient*, which represents the percentage of your monthly active users who visit your application daily (i.e., how many of your active users are very active users).
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7ae1d75-Usage_Revenue.png",
        "Usage_Revenue.png",
        1194,
        387,
        "#fbfbfd"
      ],
      "sizing": "original",
      "border": true,
      "caption": "Usage and Revenue Trend"
    }
  ]
}
[/block]