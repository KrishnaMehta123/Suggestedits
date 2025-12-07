---
title: Promo Campaign Stats
excerpt: >-
  This document explains how Promo Campaign Stats provide clear, reward-specific
  insights into user engagement, reward distribution, and redemption trends
  through KPIs and time-based charts.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

The **Stats** tab of a Promo Campaign provides a comprehensive overview of campaign performance, displaying real-time and historical analytics for user engagement, reward distribution, and redemption activity. The metrics and charts displayed depend on the *Reward type* selected when creating the campaign.

Each reward type includes:

* Key Performance Indicators (KPIs) for campaign outcomes.
* Interactive charts visualizing trends over time.
* Date filters to customize your analysis by day, week, or month.

> 📘 Note
>
> The Campaigns with the Past Behavior Segments show total metrics only (no time charts), while Campaigns with the Live Behavior Segments include interactive, time-based performance graphs along with the total metrics.

# Loyalty Points Campaign Stats

Loyalty Points campaigns display wallet-based reward performance, tracking the number of users who received points and the total number of points distributed overall.

The KPIs in this section help you understand how actively rewards were issued during the campaign and the total volume of loyalty points granted to users. These metrics highlight both the frequency of reward triggers and the overall point distribution, giving you a clear picture of the campaign’s reward activity.

* **Rewards Distributed**: Represents the total number of times a reward was distributed during the campaign. For example, if rewards were triggered multiple times for the same user, each instance is counted toward the total.
* **Points Distributed**: Indicates the total number of loyalty points issued to all qualifying users. For example, a total of 6,132 loyalty points were distributed.

<Image alt="KPIs for Promo Campaign with Loyalty Wallet Reward" align="center" border={true} src="https://files.readme.io/6718f39d9a2fc22e213f497bcb5b41ccebbd1bdd49c02c1af0caff25d5a5408e-image.png">
  KPIs for Promo Campaign with Loyalty Wallet Reward
</Image>

<br />

<Image alt="KPIs for Promo Campaign with Loyalty Wallet Reward" align="center" border={true} src="https://files.readme.io/fdfa8745de95f5e9d7ec996f446baae4f3f3bcb4c13491d490be5da1568b12dd-image.png">
  KPIs for Promo Campaign with Loyalty Wallet Reward
</Image>

The **Stats** tab also includes two line charts that show how user participation and point distribution changed throughout the campaign. These charts help you visually identify patterns such as high-engagement days, reward spikes, or periods of inactivity.

For example, if users were rewarded on multiple days, both charts will show recurring spikes corresponding to user qualification and points issuance.

### Rewards Issued

This line chart illustrates the frequency of rewards issued on each day, week, or month within the selected date range.

* **Y-axis:** Represents the total number of times rewards were issued.
* **Chart aggregation:** You can aggregate chart data by *Day*, *Week*, or *Month* using the dropdown in the top-right corner of the chart.
* **Hover interaction:** When you hover over any data point, the chart displays the exact number of rewards issued for that period along with the percentage change compared to the previous period (Day/Week/Month based on selection). This helps you quickly identify spikes, drops, or stable trends in reward distribution over time.

<Image alt="Qualified User Over Time in Loyalty Wallet" align="center" border={true} src="https://files.readme.io/989b5b942b6395d05622d9d9310b06ebca470642d9cbb97caf49a809c027c6f7-image.png">
  Qualified User Over Time in Loyalty Wallet
</Image>

<Image alt="Qualified User Over Time in Loyalty Wallet" align="center" border={true} src="https://files.readme.io/8d8d05ca9d3d82e328b15faa7fa313c5d83342ba5bb4558c77df8b4e11dee2d7-image.png">
  Qualified User Over Time in Loyalty Wallet
</Image>

### Points Distributed

This line chart illustrates the number of loyalty points issued on each date within the campaign range. It highlights distribution trends, such as reward bursts on high-activity days or consistent distribution throughout the campaign.

<Image alt="Points Distributed Over Time in Loyalty Wallets" align="center" border={true} src="https://files.readme.io/6d2e0f2c8a263c3755b20a527328bdeb2bbb41749ae1dffbccf064c12da2e4a7-image.png">
  Points Distributed Over Time in Loyalty Wallets
</Image>

# Coupon Campaign Stats

Coupon campaigns track both the distribution and redemption of coupons throughout the campaign period, helping you understand user engagement and the financial impact of the rewards issued.

The KPIs in this section help you quickly assess the number of rewards issued, the number of coupons distributed, and the total discount value redeemed by users through these coupons.

* **Rewards Issued**: Represents the total number of times a coupon reward was issued during the campaign. This counts every reward event triggered for users, including repeat rewards for the same user. For example, the system may show *100 rewards issued* during the campaign period.

* **Coupons Distributed**: The definition of this KPI depends on the type of coupon used in the campaign:

  * **Single Coupon**: Shows how many times the *same coupon code* was distributed to users as part of the campaign.
  * **Bulk Code Coupon**: Shows how many *unique coupon codes* from the bulk series were distributed. Each trigger assigns a different code to the user. For instance, if a campaign using a bulk code coupon series assigns 50 unique codes during the period, this KPI will reflect *50 coupons distributed*.

* **Discount Redeemed**: Shows the total discounts redeemed from the coupons issued in the campaign. This includes all discount values applied through coupon redemptions. For example, the *Stats* tab may display *0 redeemed* if users have not yet redeemed the coupons.

* @Bajrang Cashback Points Credited KPI is missing. this is applicable for cashback coupon

<Image align="center" className="border" border={true} src="https://files.readme.io/f2fdec6cba684b504ef93e0c0ad03f30765fc889166eba2f55eb5a11e548b37d-image.png" />

<Image align="center" className="border" border={true} src="https://files.readme.io/7ea7b114b69b3add51a6088106eca227dcbc9bdaa6d49aee1fd31f964faf099a-image.png" />

The **Stats** tab also includes a line chart that visualizes coupon distribution trends throughout the campaign. This chart helps you identify patterns such as sudden spikes in coupon issuance or periods of low activity.

For example, if one coupon was issued on October 28, the chart will display a sharp peak on that date, followed by a flat trend line on days without distribution.

## Coupons Distributed

This line chart illustrates the number of coupons issued on each day, week, or month within the selected campaign period. It helps you understand the timing and volume of coupon distribution and identify high-activity days.

<Image align="center" className="border" border={true} src="https://files.readme.io/4b3e86e8374abb52af32bfd19a8189254ea42be3d88d66d7848e23d5620e316b-image.png" />

# Partner Voucher Campaign Stats

Partner Voucher campaigns track the distribution of unique voucher codes sourced from external providers. These analytics help you understand how many vouchers were issued and how distribution patterns evolved during the campaign.

The KPIs for Partner Voucher campaigns help you track the number of voucher codes assigned and the level of user engagement with the voucher reward.

* **Voucher Codes Distributed**: Indicates the total number of partner voucher codes assigned to users during the campaign. For example, the system may report that five voucher codes have been distributed. This KPI tracks every voucher issuance event, regardless of whether a user receives multiple vouchers.

<Image align="center" className="border" border={true} src="https://files.readme.io/84a3744a31b64dd70d175e967906b49c27f96e76b7ba9bba205e536ac1374d50-image.png" />

<Image align="center" className="border" border={true} src="https://files.readme.io/dc60b6689337ca1849a311cf4f06b0210ddf5c8b2e0b8cdac9bf7627e5e2d42d-image.png" />

The **Stats** tab includes a line chart that displays voucher distribution patterns over time. This helps you analyze days with higher voucher issuance and spot trends or anomalies in campaign performance.

For example, if five vouchers were issued on October 30, the chart will show a tall spike on that date, with minimal or no activity on surrounding dates.

### Voucher Codes Distributed

This line chart illustrates the distribution of voucher codes across each day, week, or month within the selected date range. It provides a clear view of distribution frequency and peak issuance dates.

<Image align="center" className="border" border={true} src="https://files.readme.io/6b6e821e9ebc41f4e394382bd5cf47465850268e7583df855ab1e766ec22c171-image.png" />

<Image align="center" className="border" border={true} src="https://files.readme.io/5a357d0066172aa21b09882aa13634f06fda3a3b90711d99099381cf2b9f43aa-image.png" />

# Custom Rewards Campaign Stats

Custom Rewards campaigns rely on webhook calls to deliver rewards, such as wallet credits, digital items, or third-party payouts. The Stats tab displays the number of webhook-triggered rewards that succeeded, were sent, or failed.

The KPIs in this section help you evaluate the effectiveness of the webhook integration and identify any system-level issues that may impact reward delivery.

* **Webhook Credits Rewarded**: Represents the total credits successfully issued through webhook calls when *Self-Managed Wallet Credits* are used as the reward type. This KPI does not apply to *Physical & Digital Rewards*. For example, the system may display 395 credits rewarded during the campaign.
* **Webhook Sent**: Indicates how many webhook requests were successfully triggered from CleverTap to the external endpoint. For example, 17 webhook calls were sent.
* **Webhook Failed**: Shows how many webhook requests resulted in errors due to issues such as endpoint failure, timeouts, or invalid payloads. For example, 11 webhook calls failed.

These KPIs help determine whether reward delivery failures stem from configuration issues, endpoint downtime, or external service limitations.

<Image align="center" className="border" border={true} src="https://files.readme.io/8715ca9cc75e88be4302d5ff0ae6d9575e601b9a2069b68111f17883c479af06-image.png" />
