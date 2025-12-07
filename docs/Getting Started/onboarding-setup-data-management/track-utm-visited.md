---
title: Track UTM Visited_BIL-2152
excerpt: Learn more about UTM Visited event tracking.
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

The _UTM Visited_ event is tracked when a user clicks on a link from a marketing campaign that has a UTM parameter defined on it. This event is also tracked when a CleverTap-integrated attribution platform, such as AppsFlyer or Branch, sends this information to CleverTap. This event is recorded for your marketing campaigns from external sources, such as Google Ads or Facebook.

## Enable UTM Visited Tracking

The traffic that UTM Visited event drives is mostly anonymous for the CleverTap platform and may result in an MAU spike. These anonymous users are often the dropped-off users for whom businesses do not have a use case to either track or engage with them. To avoid this MAU spike, CleverTap provides the functionality to enable or disable tracking of UTM Visited. 

> 📘 Deault Behavior
> 
> The UTM Visited tracking is ON for new customers by default. For existing customers, the tracking of UTM Visited remains as is. However, they have the capability to enable or disable the same.

To enable the tracking:

1. Navigate to _Settings_ > _Schema_ > _Events_ from the CleverTap dashboard.
2. Select the _UTM Visited_ event from the _System events_ tab.
3. Click the ![](https://files.readme.io/fb90f6a-Ellipsis.png) icon and select _Enable tracking UTM visited_ from the list.
4. Turn ON the _Track UTM Visited_ toggle and click **Save**. The _UTM visited tracking enable_ message displays at the top of the screen.

(@bajrang: pls add a gif that shows all the above steps.)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4454bcf-UTM_Tracking_Toggle_Off.gif",
        null,
        "Turn off Toggle to Disable Tracking UTM Visited"
      ],
      "align": "center",
      "border": true,
      "caption": "Turn ON Toggle to Disable Tracking UTM Visited"
    }
  ]
}
[/block]

Once enabled, if you want to disable the tracking later, you can do so by clicking the ![](https://files.readme.io/fb90f6a-Ellipsis.png) icon and selecting **Disable tracking UTM Visited** from the list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9b7e631-Disable_tracking_UTM_Visited.png",
        null,
        "Disable Tracking UTM Visited"
      ],
      "align": "center",
      "border": true,
      "caption": "Disable UTM Visited Tracking"
    }
  ]
}
[/block]