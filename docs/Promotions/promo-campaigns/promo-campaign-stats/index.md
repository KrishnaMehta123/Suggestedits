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

The **Stats** tab of a Promo Campaign provides a comprehensive overview of campaign performance, displaying real-time and historical analytics for user engagement, reward distribution, and redemption activity. The metrics and charts displayed depend on the _Reward type_ selected when creating the campaign.

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

<Image align="center" border={true} caption="KPIs for Promo Campaign with Loyalty Wallet Rewards" src="https://files.readme.io/7bbbd5a59eb1604a797ef115f65e89fe0db97a47a8ac64793961116be082cd31-image.png" />

The _Rewards Distributed_ tab also includes two line charts that show how user participation and point distribution changed throughout the campaign. These charts help you visually identify patterns such as high-engagement days, reward spikes, or periods of inactivity.

For example, if users were rewarded on multiple days, both charts will show recurring spikes corresponding to user qualification and points issuance.

### Rewards Distributed

This line chart illustrates the frequency of rewards issued on each day, week, or month within the selected date range.

* **Y-axis:** Represents the total number of times rewards were distributed.
* **Chart aggregation:** You can aggregate chart data by _Day_, _Week_, or _Month_ using the dropdown in the top-right corner of the chart.
* **Hover interaction:** When you hover over any data point, the chart displays the exact number of rewards issued for that period along with the percentage change compared to the previous period (Day/Week/Month based on selection). This helps you quickly identify spikes, drops, or stable trends in reward distribution over time.

<Image align="center" border={true} src="https://files.readme.io/0099b8772a477101867024a8c5f4247eafe3f64bd9932c39b712c6117d6732fb-image.png" className="border" />

### Points Distributed

This line chart illustrates the number of loyalty points issued on each date within the campaign range. It highlights distribution trends, such as reward bursts on high-activity days or consistent distribution throughout the campaign.

<Image align="center" alt="Points Distributed Over Time in Loyalty Wallets" border={true} caption="Points Distributed Over Time in Loyalty Wallets" src="https://files.readme.io/6d2e0f2c8a263c3755b20a527328bdeb2bbb41749ae1dffbccf064c12da2e4a7-image.png" />

# Coupon Campaign Stats

Coupon campaigns track both the distribution and redemption of coupons throughout the campaign period, helping you understand user engagement and the financial impact of the rewards issued.

The KPIs in this section help you quickly assess the number of rewards issued, the number of coupons distributed, and the total discount value redeemed by users through these coupons.

* **Rewards Distributed**: Represents the total number of times a coupon reward was distributed during the campaign. This counts every reward event triggered for users, including repeat rewards for the same user. For example, the system may show _100 rewards issued_ during the campaign period.

* **Coupons Distributed**: The definition of this KPI depends on the type of coupon used in the campaign:

  * **Single Coupon**: Shows how many times the _same coupon code_ was distributed to users as part of the campaign.
  * **Bulk Code Coupon**: Shows how many _unique coupon codes_ from the bulk series were distributed. Each trigger assigns a different code to the user. For instance, if a campaign using a bulk code coupon series assigns 50 unique codes during the period, this KPI will reflect _50 coupons distributed_.

* **Discount Redeemed**: Shows the total discounts redeemed from the coupons issued in the campaign. This includes all discount values applied through coupon redemptions. For example, the _Rewards Distributed_ tab may display _0 redeemed_ if users have not yet redeemed the coupons.

* **Cashback Points Credited**: Applicable only for cashback coupons, this KPI represents the total number of cashback points credited to users’ wallets as a result of coupon redemptions. For example, the campaign may show 5,000 cashback points credited during the selected period.

<Image align="center" border={true} src="https://files.readme.io/f2fdec6cba684b504ef93e0c0ad03f30765fc889166eba2f55eb5a11e548b37d-image.png" className="border" />

<Image align="center" border={true} src="https://files.readme.io/7ea7b114b69b3add51a6088106eca227dcbc9bdaa6d49aee1fd31f964faf099a-image.png" className="border" />

The _Rewards Distributed_ tab also includes a line chart that visualizes coupon distribution trends throughout the campaign. This chart helps you identify patterns such as sudden spikes in coupon issuance or periods of low activity.

For example, if one coupon was issued on October 28, the chart will display a sharp peak on that date, followed by a flat trend line on days without distribution.

## Coupons Distributed

This line chart illustrates the number of coupons issued on each day, week, or month within the selected campaign period. It helps you understand the timing and volume of coupon distribution and identify high-activity days.

<Image align="center" border={true} src="https://files.readme.io/4b3e86e8374abb52af32bfd19a8189254ea42be3d88d66d7848e23d5620e316b-image.png" className="border" />

OR

# Coupon Campaign Stats

Coupon campaigns help you track how coupons are issued and redeemed over time, providing visibility into user engagement and the financial impact of discounts or cashback rewards delivered through the campaign.

The _Rewards Distribution_ tab adapts dynamically based on the Coupon Type (Single Code or Bulk Code) and the Coupon Benefit (Discount or Cashback). Only the KPIs and charts relevant to the selected configuration are displayed.

The KPIs in this section help you understand how frequently coupon rewards were issued, how coupons were distributed, and how much value was redeemed by users.

* **Rewards Distributed**: Represents the total number of times a coupon reward was issued during the campaign. Each reward trigger is counted, including repeat rewards issued to the same user. For example, if the campaign triggered coupon rewards 100 times, this KPI displays 100, regardless of the number of unique users.

* **Coupons Distributed**: Indicates how coupons were issued, based on the coupon type used in the campaign:

  * **Single Code Coupon**: Shows how many times the same coupon code was distributed to users.
  * **Bulk Code Coupon**: Shows how many unique coupon codes from the bulk series were distributed. Each campaign trigger assigns a new code to the user. For example, if a bulk coupon campaign assigns 50 unique codes, this KPI displays 50 coupons distributed.

* **Discount Redeemed**: Applicable only for discount coupons, this KPI shows the total value of discounts redeemed using coupons issued by the campaign. For example, if users have not yet redeemed any coupons, this KPI displays 0.

* **Cashback Points Credited**: Applicable only for cashback coupons, this KPI represents the total number of cashback points credited to users’ wallets as a result of coupon redemptions. For example, the campaign may show **5,000 cashback points credited** during the selected period.

## Coupons Distributed Over Time

The **Coupons Distributed** line chart visualizes how coupon issuance changed over the course of the campaign.

* Displays the number of coupons distributed for each selected time interval.
* Supports aggregation by **Day**, **Week**, or **Month** using the dropdown in the top-right corner.
* On hover, the chart shows:

  * The exact number of coupons distributed for that period
  * The percentage change compared to the previous period

This chart helps you quickly identify trends such as high-distribution days, promotional spikes, or periods of low activity. For example, if a coupon was issued only on October 28, the chart displays a sharp spike on that date with a flat trend on other days.

# Partner Voucher Campaign Stats

Partner Voucher campaigns track the distribution of unique voucher codes sourced from external providers. These analytics help you understand how many vouchers were issued and how distribution patterns evolved during the campaign.

The KPIs for Partner Voucher campaigns help you track the number of voucher codes assigned and the level of user engagement with the voucher reward.

* **Voucher Codes Distributed**: Indicates the total number of partner voucher codes assigned to users during the campaign. For example, the system may report that five voucher codes have been distributed. This KPI tracks every voucher issuance event, regardless of whether a user receives multiple vouchers.

<Image align="center" border={true} src="https://files.readme.io/a53f44e93a25ebc9c4c278c31eb483bd8140a68c19a9c64ee3a8b0ba34db8f7c-image.png" className="border" />

The _Rewards Distributed_ tab includes a line chart that displays voucher distribution patterns over time. This helps you analyze days with higher voucher issuance and spot trends or anomalies in campaign performance.

For example, if five vouchers were issued on October 30, the chart will show a tall spike on that date, with minimal or no activity on surrounding dates.

### Voucher Codes Distributed

This line chart illustrates the distribution of voucher codes across each day, week, or month within the selected date range. It provides a clear view of distribution frequency and peak issuance dates.

<Image align="center" border={true} src="https://files.readme.io/9db18f74caff43027141697e3a2a0188d895c1b67b90e3128782d4c1a56f3f75-image.png" className="border" />

# Custom Rewards Campaign Stats

Custom Rewards campaigns rely on webhook calls to deliver rewards, such as wallet credits, digital items, or third-party payouts. The _Rewards Distributed_ tab displays the number of webhook-triggered rewards that succeeded, were sent, or failed.

The KPIs in this section help you evaluate the effectiveness of the webhook integration and identify any system-level issues that may impact reward delivery.

* **Webhook Credits Rewarded**: Represents the total credits successfully issued through webhook calls when _Self-Managed Wallet Credits_ are used as the reward type. This KPI does not apply to _Physical & Digital Rewards_. For example, the system may display 395 credits rewarded during the campaign.
* **Webhook Sent**: Indicates how many webhook requests were successfully triggered from CleverTap to the external endpoint. For example, 17 webhook calls were sent.
* **Webhook Failed**: Shows how many webhook requests resulted in errors due to issues such as endpoint failure, timeouts, or invalid payloads. For example, 11 webhook calls failed.

These KPIs help determine whether reward delivery failures stem from configuration issues, endpoint downtime, or external service limitations.

<Image align="center" border={true} src="https://files.readme.io/8715ca9cc75e88be4302d5ff0ae6d9575e601b9a2069b68111f17883c479af06-image.png" className="border" />
