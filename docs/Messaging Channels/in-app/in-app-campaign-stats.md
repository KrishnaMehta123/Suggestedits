---
title: In-App Stats
excerpt: Measure the performance of your In-App campaign.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# View In-App Campaign Stats

You can use the [Campaign Filters](https://docs.clevertap.com/docs/intro-to-campaigns) to find your campaigns. Once the campaign is live, you can view its stats by selecting an _In-App_ campaign from the _Campaigns_ page on the CleverTap dashboard. Click to view its deliveries, clicks, and conversions. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/41f0509930c6042557c64f170c1e40373a5cc024fdc33510cb59c09f8829635f-Filter_Campaigns.png",
        "Select In-App Stats",
        1012
      ],
      "align": "center",
      "border": true,
      "caption": "Filter by Channel"
    }
  ]
}
[/block]


Click to open the selected campaign. The campaign stats page displays.

## Key Metrics

On the stats page you can track the following metrics:

- Viewed: The total number of devices that receive the notification. 
- Clicks: Number of clicks on the notification. Calculated as (Clicks/Viewed) \* 100.
- CTR: The clickthrough rate of the campaign. It is measured by (Click/Viewed) \* 100.
- Converted users: Percentage of users who viewed the campaign and completed the conversion goal event. (Converted users/Unique Views \* 100). 
- Control group: The number of users considered in the control group for the campaign.

# Message Trend

Shows the daily, weekly, and monthly trends for campaign messages. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fc4bb2c6907c94213c94ce5d3ee57df36c53bb309514c81f8b9a8c66c4b96d11-In-app_Message_trend.png",
        "Daily, Weekly, and Monthly Trends",
        1350
      ],
      "align": "center",
      "border": true,
      "caption": "Daily Message Trend"
    }
  ]
}
[/block]


# Conversion Performance Overview

## Conversion Performance

It shows Conversion performance, Revenue performance, Users conversion funnel, and Influenced conversion funnel.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e860139ed884795e65b014457dd986cd455d43d6badb2fcab1c3d7aa46a0c68c-In-app-_Conversion_and_Revenue.png",
        null,
        "Conversion Performance and Revenue Numbers shown In the Table"
      ],
      "align": "center",
      "sizing": "75% ",
      "border": true,
      "caption": "Conversion Performance and Revenue Numbers shown In the Table"
    }
  ]
}
[/block]


For A/B Test, Split Delivery, and Message on User Property campaigns, you can view stats for each variant under User conversion funnel.

## Revenue Performance

Revenue generated from the campaign.

## Users Conversion Funnel

Allows you to view conversion by OS. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/01111e1-in-app_stats_users_conversion_funnel.png",
        "Conversion by OS",
        1319
      ],
      "align": "center",
      "border": true,
      "caption": "Users Conversion Funnel"
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

Click the _View details of users who clicked_ linked on the _Split of Clicks_ tab. The event analytics is displayed.  Click the _People_ tab to view user details.