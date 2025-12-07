---
title: Create Promo Campaigns (COPY)
excerpt: >-
  Learn how to create and configure a Promo Campaign from scratch using the
  step-by-step campaign builder.
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

This document provides detailed instructions on creating and configuring a Promo Campaign using the Campaign Builder. It guides you through the key steps to set up your campaign, including defining your campaign goals, selecting the right target audience, choosing the campaign type, and customizing your settings.

# Create Promo Campaign

Go to *Promotions* > *Promo Campaigns* and click **Create Campaign**. The *New Promotion Campaign* page opens. To create a Promo Campaign, perform the following five key steps:

1. [Define Qualification Criteria](doc:create-promo-campaigns#start-here-define-qualification-criteria)
2. [Select Target Segment](̉doc:create-promo-campaigns#who-select-target-segment)
3. [Set Up Reward](doc:create-promo-campaigns#set-up-reward)
4. [Set Up Delivery Preference](doc:create-promo-campaigns#when-set-delivery-schedule)
5. [Publish Campaign](doc:create-promo-campaigns#publish-campaign)

## Define Qualification Criteria

The *Start Here* section is where you choose how users will qualify for the reward. The qualification criteria provide the following options:

* **Past behavior/Custom list**: Target users based on actions performed in the past or custom list uploaded to the CleverTap dashboard. For example, you can target users who received a specific reward but have not redeemed it yet.
* **Live behavior**: Trigger rewards in real-time when a user performs or does not perform an event. For example, you can trigger a reward when a user adds items to their cart but does not complete the checkout process within a set timeframe.

<Image alt="Define Qualification Criteria" align="center" border={true} src="https://files.readme.io/db8874c06fae7a9f98884e2d01a593742b44a052dc5bd6030f63527b1d42b607-image.png">
  Define Qualification Criteria
</Image>

## Select Target Segment

The *Who* section allows you to define who should receive the reward using the rule builder. The *Target Segment* rule builder Includes the following:

* **Find users from segment**: allows you to select users from an already existing segment. 
* **Create rules based on events**:
  * Users who **have done** specific events
  * Users who **have not done** certain events
  * Users who **have common user properties** such as device type, location, are part of a particular segment, and so on.
  * Users who **have common interests** or behavior on your platform.
* Option to check **Constant event property** if needed to simplify the logic.

<Image alt="Select Target Segment" align="center" border={true} src="https://files.readme.io/c0f72135336ae3b88597f99adb1a424fad8b23e8c8d814927a28548d3ef4853c-image.png">
  Select Target Segment
</Image>

## Set Up Reward

The *What* section allows you to define the reward type for your Promo Campaign. Choose from various reward options such as:

* [Wallet Points](̉̉̉̉̉̉doc:loyalty-wallets),
* [Coupons](doc:coupons), OR
* [Partner Vouchers](doc:partner-vouchers)

<Image alt="Create Message to Setup the Reward" align="center" border={true} src="https://files.readme.io/45d3cd35423edf0c2f76e338fc31149ae5af55bef3252e5e09a696f90e0b35eb-image.png">
  Set Up a Reward to Create Message
</Image>

This section ensures you set up the right reward mechanism to engage your users effectively.

## If Wallet Points is Selected

When you select **Wallet Points** as the type of reward when creating a Promo Campaign, you see the following options:

* **Choose wallet**: Select the wallet from the dropdown (must be created beforehand)
* **Points type**: Choose between the following types:  

  @Bajrang Percentage and Proportional points type are missing. this will show up in case of live action campaign with following condition is true 

  * Campaign type = Live-User Actions (not applicable in live inaction rue)
  * Rule Builder = Single Event, Single with filter on past behaviour, Selected event should have at least one numeric property
* **Flat**: Fixed value of the wallet points that you want to distribute to the qualified users. For example, 100 points
* **Random**: Allows you to define a range of possible reward values, along with a probability bias, to influence distribution behavior. When selecting **Random** allows the following options:
  * **Reward between**: Set the *minimum* and *maximum* values to define the range within which the points will be randomized. For example, 10 to 100 points.
  * **Probability favor**: Choose how the system should favor distribution across the following reward ranges:
    * **Favor Min**: More users will receive lower point values within the range.
    * **Favor Avg**: Points will be distributed with an average value bias.
    * **Favor Max**: More users will receive higher point values within the range.
* **Value**: Select the *flat* value or a *reward between* value.
* **Custom Points Lifecycl&#x65;*(Optional)***: Enable this option to customize when the wallet points get activated and how long they remain valid. If disabled, default wallet-level settings apply.
  * **Activation**: It provides the following options for activation:
    * **Immediate**: Points are credited to the Active bucket as soon as they are rewarded.
    * **Custom**: Points go into a Promised bucket first and are activated after a set delay. For example, 7 days after the reward.
  * **Expiry**: It provides the following options for expiry:
    * **Never**: Points never expire.
    * **Date Picker**: Set a fixed expiry date using a calendar selector. 
    * **Custom**: Define expiry based on a delay from the activation date. For example, expires after 7 days of being rewarded.

@Bajrang Budget section is not explained. this will show up in case of live action campaign.  per user is false for flat points and campaign level budget is true for all points type. refer to the PRD more details 

@Bajrang Reward recurrence section is not explained. this will show up in case of live campaign. 

<Image alt="Set Up Wallet Points Reward in the Message" align="center" border={true} src="https://files.readme.io/c76e763e12b3a4ce6c3ac5d49c55c59dd9fbd8535272920a5c234c9cdc396f0f-image.png">
  Set Up Wallet Points Reward in the Message
</Image>

## If Coupons is Selected

When you select **Coupons** as the reward type while creating a Promo Campaign, you will see the following configuration options:

* **Select coupon type**: Choose between the two available coupon types:
  * **Single Code**: A single fixed code is shared with all eligible users.
  * **Bulk Codes**: A set of unique codes is generated and distributed, one per user.

> 📘 Note
>
> Select **Single Code** for simple, general promotions and **Bulk Codes** when each user should get a unique coupon.

* **Choose coupon**: A dropdown list shows available coupons that match the selected coupon type. You must select one coupon to proceed.
  * If **Single Code** is selected, only single-code coupons are listed.
  * If **Bulk Codes** is selected, only coupon series with bulk codes are shown.

> 📘 Note
>
> The coupon must be active and not fully redeemed to appear in the list.

* **Coupon redemption activation**: Define when the user should be allowed to redeem the coupon after it is rewarded. Two options are available:
  * **Immediate**: Coupons can be redeemed as soon as it is distributed to the user.
  * **Custom**: Delay redemption by a specific time. For example, redeemable only after 2 days of reward assignment. This is useful for setting engagement goals or time-based unlocks. When *Custom* redemption activation is enabled, the coupon is still returned via the fetch coupon API so the user can see it. However, the redemption will remain disabled until the configured activation delay is completed.

<Image alt="Set Up Coupons Reward in the Message" align="center" border={true} src="https://files.readme.io/f00662e1417c332e7fb6c1085496e0671f3f375f5e209018508044cf6d06c061-image.png">
  Set Up Coupons Reward in the Message
</Image>

@Bajrang Max coupons per user and max coupons per campaign section is missing. this will show up in live action campaign

## If Partner Vouchers is Selected

When you select **Partner Vouchers** as the reward type while creating a Promo Campaign, you will be able to configure it using the following fields:

* **Code provider**: Select the **provider** from the dropdown list. This identifies the partner brand or service from which the vouchers originate. The dropdown shows all integrated and active voucher providers available in your account.

* **Code snippet name**: After selecting a provider, choose the associated **code snippet**. This snippet contains a batch of voucher codes ready for distribution. The list is filtered based on the selected provider.

<Image alt="Set Up Partner Vouchers Reward in the Message" align="center" border={true} src="https://files.readme.io/1ba540cf44b226bf31657f69cc8f5024db04ebc664d847b37b118d86ed852142-image.png">
  Set Up Partner Vouchers Reward in the Message
</Image>

> 📘 Note
>
> * Only active and unexpired voucher lists will be displayed.
> * No preview of the voucher or its properties is shown in this version.
> * When a user qualifies for the campaign, a code is picked from the selected voucher list and assigned to them.
> * The system ensures that each user receives a unique and unassigned voucher code.

@Bajrang Max vouchers per user and campaign section is missing. this will show up in live action campaign 

# When: Set Delivery Schedule

@Bajrang you have not covered when section for live action campaign

The *When* section defines when the campaign should start and whether it should be scheduled or sent immediately. It allows the following options:

* **Send Now:** Uses the current timestamp and account timezone. For example, `(GMT+05:30) Asia/Kolkata`.
* **Schedule for later:** Opens a date/time picker to select a future start time. 

<Image alt="Set Delivery Preferences" align="center" border={true} src="https://files.readme.io/f64c9ea54de2ed6ec5e1f42297e4005d60be73e4dd7e6e07dd3364c20127b795-image.png">
  Set Delivery Preferences
</Image>

# Publish Campaign

Once all the above sections are completed, the *Publish Campaign* button at the bottom unlocks. Clicking it activates or schedules the campaign.

<Image alt="Publish Campaign" align="center" border={true} src="https://files.readme.io/208d31fed015df3703b4e35c6741ded52ecf1b99c62bfef9f5c085323a193ad1-image.png">
  Publish Campaign
</Image>

# Reward Type Comparison

Promo Campaigns support multiple reward types to suit different marketing goals, from flexible loyalty points to personalized coupons and third-party brand vouchers. The table below compares the available reward types side by side to help you select the most suitable one while setting up a Promo Campaign based on your campaign needs, distribution logic, and user engagement strategy.

| Feature                     | Wallet Points                                                      | Coupons                                                                                          | Partner Vouchers                                                                    |
| --------------------------- | ------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------- |
| **Use Case**                | Provide loyalty points that can be redeemed in-app                 | Offer discounts or benefits using single or unique coupon codes                                  | Distribute external brand vouchers                                                  |
| **Reward Format**           | Digital points credited to user's wallet                           | Alphanumeric coupon codes (single or bulk)                                                       | Pre-generated voucher codes from third-party providers                              |
| **Reward Options**          | Flat, Random (with probability favor), Percentage and Proportional | Single Code or Bulk Codes                                                                        | Code Provider and Code Snippet                                                      |
| **Distribution Logic**      | Based on user segmentation and campaign rules                      | Code selected based on coupon type; the user gets the same or unique code depending on the setup | Voucher is picked from the list and assigned uniquely to each eligible user         |
| **When to Use**             | Incentivize actions with flexible loyalty mechanics                | Run sales or targeted discount offers with traceable redemption                                  | Reward users with brand vouchers during promotions, contests, or referral campaigns |
| **Eligibility Requirement** | Requires at least one wallet to be set up                          | Requires at least one active coupon in the system                                                | Requires you to pre-upload a list of a third-party voucher provider.                |
