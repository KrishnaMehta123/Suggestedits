---
title: Native Display Stats
excerpt: Measure the performance of your Native Display campaign.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# View Native Display Campaign Stats

You can use the Campaign filter to [Filters](https://docs.clevertap.com/docs/intro-to-campaigns) to find your campaigns.  Once the campaign is live, you can view its stats by selecting a *Native Display* campaign from the *Campaigns* page on the CleverTap dashboard. Click to view its deliveries, clicks, and conversions. 

<Image title="Filter by Channels" alt={1012} align="center" border={true} src="https://files.readme.io/0c18fa81db54343c91c59cb83ce2b9b18a2aa479d9330190f182df547c651b4c-Filter_By_Channels.png">
  Filter by Channels
</Image>

Click to open the selected campaign. The campaign stats page displays.

You can track the following stats:

* Viewed: The total number of user devices that received the notification. 
* Clicks: Number of clicks on the notification. Calculated as (Clicks/Viewed) \* 100.
* CTR: The clickthrough rate of the campaign. It is measured by (Click/Viewed) \* 100.\
  Converted users: The number of users that converted after receiving the campaign. 
* Errors: Number of errors for the campaign. 
* Control group: The number of users considered in the control group for the campaign.

# Message Trend

Shows the daily, weekly, and monthly trends for campaign messages. 

<Image alt="Daily Message Trend for Native Display Campaign" align="center" border={true} src="https://files.readme.io/033cac4cc82f83f52bc5b2d8687334cb1ac8c176b1da5999b633578aa15013be-image.png">
  Daily Message Trend for Native Display Campaign
</Image>

# Conversion Performance Overview

Shows the Conversion performance, Revenue performance, Users conversion funnel, and Influenced conversion funnel. 

<Image alt="Conversion Performance and Revenue Numbers shown In the Table" align="center" width="75% " border={true} src="https://files.readme.io/87f30608162fa412b672adf42fa957e5763dd6e8771414f4b829110cd353abbd-Native_Display_Conversion_Performance.png">
  Conversion Performance and Revenue Numbers shown In the Table
</Image>

For A/B Test, Split Delivery, and Message on User Property campaigns, you can view stats for each variant under User conversion funnel.

## Conversion Performance

Shows conversion performance. 

## Revenue Performance

The Revenue Performance section shows the revenue boost achieved from the campaign.

## Users conversion funnel

Allows you to view conversion by OS.

<Image alt="Users Conversion Funnel" align="center" border={true} src="https://files.readme.io/ffd18448d007076100c489e956a59c461f6edbc6194b4333190de06a328bade6-image.png">
  Users Conversion Funnel
</Image>

> 📘 Key Points to Remember
>
> The Conversion Performance number for *All Variants* may be equal to or less than the combined Conversion Performance number for each individual variant. For example, if the Conversion Performance number for All Variants is 10500, with Variant A at 5575 and Variant B at 5053, the total for Variants A and B combined is 10628, exceeding the total for *All Variants*.
>
> This scenario can occur due to the following reasons:
>
> * For Live campaigns, different variants are delivered to various devices, identified by different GUIDs for the same user. Consequently, the Conversion Performance number for All Variants might not match the sum of the Conversion Performance numbers for each variant. For instance, a user may receive Variant A before uninstalling the app and then receive Variant B after reinstalling it until their identity is established.
> * For Recurring campaigns (user property campaigns), the user can qualify more than once when and receive different message copy each time. For example, the user upgrades to a new plan. In this case, the message copy received by the user before and after upgrading the *Membership type* can be different.
>
> In both the cases, the same user is counted twice, once for Variant A and once for Variant B. However, when calculating the Conversion Performance number for *All Variants*, each user is counted only once.

# Errors

You can view campaign errors from the Stats > Errors tab.

<Image alt="Native Display Errors Tab" align="center" border={true} src="https://files.readme.io/124db61afd96f9f082696d69b960291e87fb425ece050e1d1dd3236a84080a4d-image.png">
  Native Display Errors Tab
</Image>
