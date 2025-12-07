---
title: In-App Campaign Stats
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
      title: In-App Troubleshooting & FAQs
      url: https://docs.clevertap.com/docs/troubleshooting-faqs-inapp
---
# View In-App Campaign Stats
You can use the [Campaign Filters](doc:filters) to find your campaigns. Once the campaign is live, you can view its stats by selecting an *In-App* campaign from the *Campaigns* page on the CleverTap dashboard. Click to view its deliveries, clicks, and conversions. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9480b41-push_filter_campaigns.png",
        "push_filter_campaigns.png",
        1012,
        627,
        "#acadb1"
      ],
      "border": true
    }
  ]
}
[/block]
Click to open the selected campaign. The campaign stats page displays.


You can track the following stats:

* Viewed: The total number of devices that receive the notification. 
* Clicks: Number of clicks on the notification. Calculated as (Clicks/Viewed) * 100.
 * CTR: The clickthrough rate of the campaign. It is measured by (Click/Viewed) * 100.
* Converted users: The number of users that converted after receiving the campaign. 
* Errors: Number of errors for the campaign. These errors can be both technical errors such as FCM related errors or non-technical errors such as messages frequency exceeded. <<@dk, does in-app also show errors ?>>
* Control group: The number of users considered in the control group for the campaign.



# Message Trend

Shows the daily, weekly, and monthly trends for campaign messages. 


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/170b832-in-app_stats_message_trend.png",
        "in-app_stats_message_trend.png",
        1350,
        597,
        "#fcfbfc"
      ],
      "border": true
    }
  ]
}
[/block]
### Conversion Performance

Shows the Conversion performance, Revenue performance, Users conversion funnel, and Influenced conversion funnel. 

### Revenue Performance 
Revenue generated from the campaign.

### Users conversion funnel

Allows you to view conversion by OS. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/01111e1-in-app_stats_users_conversion_funnel.png",
        "in-app_stats_users_conversion_funnel.png",
        1319,
        748,
        "#f0f2fc"
      ],
      "border": true
    }
  ]
}
[/block]
### User Details

Click the *View details of users who clicked* linked on the *Split of Clicks* tab. The event analytics is displayed.  Click the *People* tab to view user details. 

### Errors
Shows [Campaign Errors](doc:campaign-errors).