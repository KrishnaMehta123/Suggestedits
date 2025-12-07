---
title: App Inbox Stats
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
  pages:
    - type: link
      title: App Inbox Troubleshooting
      url: https://docs.clevertap.com/docs/troubleshooting-app-inbox
---
# View App Inbox Stats

You can use the [Campaign Filters](doc:filters) to find your campaigns.  Once the campaign is live, you can view its stats by selecting an *App Inbox* campaign from the *Campaigns* page on the CleverTap dashboard. Click to view its deliveries, clicks, and conversions. 

<Image title="push_filter_campaigns.png" alt={1012} className="border" border={true} src="https://files.readme.io/93047d6-push_filter_campaigns.png" />

Click to open the selected campaign. The campaign stats page displays.

You can track the following stats:

* Sent: Total number of notifications delivered to the user device.
* Viewed: The total number of devices that receive the notification. Calculated as (Viewed/Sent) \* 100
* Clicks: Number of clicks on the notification. Calculated as (Clicks/Sent) \* 100.
* CTR: The clickthrough rate of the campaign. It is measured by (Click/Viewed) \* 100.
* Converted users: The percentage of total users that converted after receiving the campaign. 
* Errors: Number of errors for the campaign. These errors can be both technical errors such as FCM related errors or non-technical errors such as messages frequency exceeded. \<\<@dk, does in-app also show errors ?>>
* Control group: The number of users considered in the control group for the campaign.

<Image title="app_inbox_stats_Hero.png" alt={2640} className="border" border={true} src="https://files.readme.io/c9c792a-app_inbox_stats_Hero.png" />

## Message Trend

Shows the daily, weekly, and monthly trends for campaign messages. 

<Image title="app_inbox_stats_performance_trend.png" alt={2652} className="border" border={true} src="https://files.readme.io/77c2c8e-app_inbox_stats_performance_trend.png" />

## Conversion Performance

Shows the Conversion performance, Revenue performance, Users conversion funnel, and Influenced conversion funnel. 

<Image title="app_inbox_stats_conversion_performance_Revenue_performance.png" alt={2628} className="border" border={true} src="https://files.readme.io/ea10bcb-app_inbox_stats_conversion_performance_Revenue_performance.png" />

## Revenue Performance

Shows the incremental and boost revenue due to the campaign. 

### Users conversion funnel

Allows you to view conversion by OS. 

<Image title="app_inbox_stats_user_conversion_funnel.png" alt={2674} className="border" border={true} src="https://files.readme.io/26075d2-app_inbox_stats_user_conversion_funnel.png" />

#### User Details

Click the *View details of users who clicked the notification. The event analytics is displayed.  Click the* People\* tab to view user details. 

## Errors

Shows [Campaign Errors](doc:campaign-errors).
