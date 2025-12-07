---
title: App Inbox Stats
excerpt: Measure the performance of your App Inbox campaign.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# View App Inbox Stats

You can use the [Campaign Filters](https://docs.clevertap.com/docs/intro-to-campaigns) to find your campaigns.  Once the campaign is live, you can view its stats by selecting an _App Inbox_ campaign from the _Campaigns_ page on the CleverTap dashboard. Click to view its deliveries, clicks, and conversions. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c8c97c1c9a9551d6375bc14c1f8bbf7d93052098f2a3cca19ef67915850eaae2-Filter_By_Channels.png",
        "Filter campaigns by App-Inbox Channel",
        1012
      ],
      "align": "center",
      "border": true,
      "caption": "Filter Campaigns by App Inbox Channel"
    }
  ]
}
[/block]


Click to open the selected campaign. The campaign stats page displays.

You can track the following stats:

- Sent: A total number of notifications sent to the user device.
- Viewed: A total number of devices that receive the notification. Calculated as (Viewed/Sent) \* 100
- Clicks: Number of clicks on the notification. Calculated as (Clicks/Sent) \* 100.
- CTR: The clickthrough rate of the campaign. It is measured by (Click/Viewed) \* 100.
- Converted users: The percentage of total users that converted after receiving the campaign. 
- Errors: Number of errors for the campaign. These errors can be technical errors such as FCM-related or non-technical errors such as messages frequency exceeded. 
- Control group: The number of users considered in the control group for the campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c9c792a-app_inbox_stats_Hero.png",
        "View App Inbox Statistics",
        2640
      ],
      "align": "center",
      "border": true,
      "caption": "App Inbox Statistics"
    }
  ]
}
[/block]


# Message Trend

Shows the daily, weekly, and monthly trends for campaign messages. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/77c2c8e-app_inbox_stats_performance_trend.png",
        "View App Inbox Campaign Message Trends",
        2652
      ],
      "align": "center",
      "border": true,
      "caption": "Message Trends"
    }
  ]
}
[/block]


# Conversion Performance Overview

## Conversion Performance

Shows the Conversion performance, Revenue performance, Users conversion funnel, and Influenced conversion funnel.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ea10bcb-app_inbox_stats_conversion_performance_Revenue_performance.png",
        "View campaign conversion performance",
        2628
      ],
      "align": "center",
      "border": true,
      "caption": "Conversion and Revenue Performance"
    }
  ]
}
[/block]


For A/B Test, Split Delivery, and Message on User Property campaigns, you can view stats for each variant under User conversion funnel.

## Revenue Performance

Shows the incremental and boost revenue due to the campaign. 

## Users conversion funnel

Allows you to view conversion by OS. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/26075d2-app_inbox_stats_user_conversion_funnel.png",
        "View the overall conversion funnel",
        2674
      ],
      "align": "center",
      "border": true,
      "caption": "Conversion Funnel View"
    }
  ]
}
[/block]


<br />

> 📘 Key Points to Remember
> 
> The Conversion Performance number for _All Variants_ may be equal to or less than the combined Conversion Performance number for each individual variant. For example, if the Conversion Performance number for All Variants is 10500, with Variant A at 5575 and Variant B at 5053, the total for Variants A and B combined is 10628, exceeding the total for _All Variants_.
> 
> This scenario can occur due to the following reasons:
> 
> - For Live campaigns, different variants are delivered to various devices, identified by different GUIDs for the same user. Consequently, the Conversion Performance number for All Variants might not match the sum of the Conversion Performance numbers for each variant. For instance, a user may receive Variant A before uninstalling the app and then receive Variant B after reinstalling it until their identity is established.
> - For Recurring campaigns (user property campaigns), the user can qualify more than once when and receive different message copy each time. For example, the user upgrades to a new plan. In this case, the message copy received by the user before and after upgrading the _Membership type_ can be different.
> 
> In both the cases, the same user is counted twice, once for Variant A and once for Variant B. However, when calculating the Conversion Performance number for _All Variants_, each user is counted only once.

## User Details

Click the _View_ details of users who clicked the notification. The event analytics is displayed.  Click the _People_ tab to view user details. 

# Errors

You can view campaign errors from the _Stats_ > _Errors_ tab.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5408869852c4e8d35614097614753dc0414fa7d1a59ebdac7cfdfd86174e2567-image.png",
        null,
        null
      ],
      "align": "center",
      "border": true,
      "caption": "Errors Tab"
    }
  ]
}
[/block]