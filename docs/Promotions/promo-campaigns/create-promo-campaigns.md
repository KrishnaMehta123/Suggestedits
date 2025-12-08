---
title: Create Promo Campaigns
excerpt: >-
  Learn how to create and configure a Promo Campaign from scratch using the
  step-by-step campaign builder.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
# Overview

This document provides detailed instructions on creating and configuring a Promo Campaign using the Campaign Builder. It guides you through the key steps to set up your campaign, including defining your campaign goals, selecting the right target audience, choosing the campaign type, and customizing your settings.

# Create Promo Campaign

Go to *Promotions* > *Promo Campaigns* and click **Create Campaign**. The *New Promotion Campaign* page opens. To create a Promo Campaign, perform the following five key steps:

1. [Define Qualification Criteria](doc:create-promo-campaigns#define-qualification-criteria)
2. [Select Target Segment](̉doc:create-promo-campaigns#who-select-target-segment)
3. [Set Up Reward](doc:create-promo-campaigns#set-up-reward)
4. [Set Up Delivery Preference](doc:create-promo-campaigns#when-set-delivery-schedule)
5. [Publish Campaign](doc:create-promo-campaigns#publish-campaign)

## Define Qualification Criteria

The *Start Here* section is where you choose how users will qualify for the reward. The qualification criteria provide the following options:

* **Past behavior/Custom list**: Target users based on actions performed in the past or a custom list uploaded to the CleverTap dashboard. For example, you can target users who have not done a transaction in the last 6 months, and offer them a 20% discount coupon. 
* **Live behavior**: Trigger rewards in real-time when a user performs or does not perform an event. For example, you can trigger a reward when a user adds items to their cart but does not complete the checkout process within a set timeframe.

<Image alt="Define Qualification Criteria" align="center" border={true} src="https://files.readme.io/db8874c06fae7a9f98884e2d01a593742b44a052dc5bd6030f63527b1d42b607-image.png" />  Define Qualification Criteria

## Select Target Segment

The *Who* section allows you to define who should receive the reward using the rule builder. The *Target Segment* rule builder lets you select users from an existing saved segment or create a new segment using event and property-based rules as follows:
* **Find users from segment**: Select users from a saved segment or define a new one. 
* **Create rules based on events**: Build custom logic using event and property-based conditions
  * Users who **have done** specific events
  * Users who **have not done** certain events
  * Users who **have common user properties**, such as device type and location, are part of a particular segment, and so on. 
  * Users who **have common interests** or share common behavioral traits or usage patterns, such as frequent shoppers or high-engagement users.
* Option to enable **Constant event property**, which keeps event property values fixed during evaluation. It is useful when comparing multiple events with shared attributes. For example, you can lock the Product ID property across both events to find users who viewed and purchased the same product.

<Image alt="Select Target Segment" align="center" border={true} src="https://files.readme.io/c0f72135336ae3b88597f99adb1a424fad8b23e8c8d814927a28548d3ef4853c-image.png" />  Select Target Segment

## Set Up Reward

The **What** section allows you to define the **reward type** for your Promo Campaign. Depending on your selection, the configuration options vary. CleverTap supports the following reward types:

* [Wallet Points](doc:create-promo-campaigns-copy-1#loyalty-points) 
* [Coupons](doc:create-promo-campaigns-copy-1#coupons) 
* [Partner Vouchers](doc:create-promo-campaigns-copy-1#partner-vouchers) 
* [Custom Rewards](doc:create-promo-campaigns-copy-1#custom-rewards) 

## Set Delivery Preferences

The *When* section defines when the campaign starts and ends, and the controls available vary based on whether you select a *Past Behavior Segment (PBS)* or a *Live Behavior Segment*.

### For Past Behavior Segments or Custom List (PBS)

When you select Past Behavior or Custom List Segment, the *When* section shows the following options:

| Option                 | Description                                                                                                                       | Example / Use Case                                                                  |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| **Send Now**           | Launches the campaign immediately using the current timestamp and the **account timezone** (for example, GMT+05:30 Asia/Kolkata). | Run a flash-sale promotion as soon as it is configured.                             |
| **Schedule for Later** | Let's you choose a **future start date and time**. You can also adjust the timezone if required.                                  | Schedule a promo to start at 6:00 PM on a Friday evening to capture higher traffic. |

<Image alt="Set Delivery Preferences" align="center" border={true} src="https://files.readme.io/f64c9ea54de2ed6ec5e1f42297e4005d60be73e4dd7e6e07dd3364c20127b795-image.png" />  Set Delivery Preferences in Past Behavior/Custom List Segments

### For Live Behavior Segments

When you select Live Behavior Segment, the *When* section shows the following options:

| Option | Description | Example / Use Case |
| ------ | ----------- | ------------------ |
| **Start Date and Time** | Choose when the campaign should start.<br />• **Now**: Launches the campaign immediately after publishing.<br />• **On a Date/Time**: Launches the campaign at a scheduled date and time. | Start the live campaign immediately to capture ongoing cart abandonment events, or schedule it to go live on the morning of a sale day. |
| **End Date and Time** | Choose when the campaign should stop.<br />• **Never**: Campaign keeps running until manually stopped.<br />• **On a Date/Time**: Campaign automatically ends at a chosen date/time. | End the campaign automatically at midnight on the final day of a seasonal sale. |

<Image alt="Set Deliver Preference in Live Behavior Campaigns" align="center" border={true} src="https://files.readme.io/ac5f953cd43599b7d06b8532535fe1ae8871b5e900f4559687d0b0fa8bba8dfb-image.png" />  Set Deliver Preference in Live Behavior Campaigns

## Publish Campaign

Once you define all the above sections, click **Publish Campaign** to activate or schedule the campaign.

<Image alt="Publish Campaign" align="center" border={true} src="https://files.readme.io/208d31fed015df3703b4e35c6741ded52ecf1b99c62bfef9f5c085323a193ad1-image.png" />  Publish Campaign

# Reward Types

Each reward type includes different configuration settings, described in the sections below:

## Loyalty Points

Use Loyalty Points to incentivize users with loyalty points that can be accumulated and redeemed within your app or platform. This option requires that wallets be pre-created in your CleverTap account.

The following configuration options are available, when Loyalty Points is selected:

<Table align={["left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Option
      </th>

      <th>
        Description
      </th>

      <th>
        Example / Use Case
      </th>

      <th>
        Available In
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Loyalty wallet**
      </td>

      <td>
        Select the wallet from the dropdown. Ensures that points are distributed to the correct wallet.
      </td>

      <td>
        You can reward users based on context if you have multiple wallets (for example, Grocery vs. Food).
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segments
      </td>
    </tr>

    <tr>
      <td>
        **Points earning scheme**
      </td>

      <td>
        Define how points are calculated when users qualify. Options include:<br />
        • **Flat**: A fixed number of points for each qualifying user.<br />
        • **Percentage**: Points calculated as a percentage of an event property (for example, order amount).<br />
        • **Proportional**: Points awarded per defined unit of an event property.<br />
        • **Random**: Points assigned from a defined range; exposes Value Range + Distribution Bias controls.
      </td>

      <td>
        • **Flat**: Every eligible user earns 100 points regardless of order amount.<br />
        • **Percentage**: If set to 10% of the amount, a ₹500 purchase earns 50 points.<br />
        • **Proportional**: For every ₹100 spent, the user gets 10 points.<br />
        • **Random**: Users earn between 10 and 50 points, with distribution bias favoring the average.
      </td>

      <td>
        • **Flat** and **Random**: Available in both Past Behavior/Custom List and Live Behavior segments.<br />
        • **Percentage** and **Proportional**: Available only in Live Behavior segments
      </td>
    </tr>

    <tr>
      <td>
        **Points value**
      </td>

      <td>
        The input control for Points value changes based on the selected Points Earning Scheme:<br />
        • **Flat**: Enter a single fixed value of points/credits awarded to each qualifying user.<br />
        • **Percentage**: Define a percentage of a selected event property (for example, order amount) from the qualifying event (typically a Charged event).<br />
        • **Proportional**: Define "points per unit" of a selected event property (for example, for every X units of the property, award Y points).<br />
        • **Random**: Set a min–max range of points/credits; the system randomly selects a value within this range for each qualifying user (also supports Distribution Bias).
      </td>

      <td>
        • **Flat**: Set to 100 means every qualifying user gets 100 credits.<br />
        • **Percentage**: Set to 10% means a purchase of ₹500 (as per selected event property) gives 50 credits.<br />
        • **Proportional**: Set to 10 credits for every Rs. 100 (per selected event property).<br />
        • **Random**: Set to a range of 10–100 means each qualifying user gets a random value between 10 and 100.
      </td>

      <td>
        • **Flat** and **Random**: Available in both Past Behavior/Custom List and Live Behavior Segment.<br />
        • **Percentage** and **Proportional**: Available only in Live Behavior campaigns.
      </td>
    </tr>

    <tr>
      <td>
        **Distribution bias** (For Random scheme only)
      </td>

      <td>
        Control distribution pattern that allows you to select the following options:<br />
        • **Favor Min**: Skews distribution toward the lower end of the range.<br />
        • **Favor Avg**: Skews distribution toward the midpoint of the range.<br />
        • **Favor Max**: Skews distribution toward the higher end of the range.
      </td>

      <td>
        • **Favor Min**: For a range of 10–100 points, most users receive lower values (for example, 10–30), while fewer receive higher values.<br />
        • **Favor Avg**: For a range of 10–100 points, most users receive values around the midpoint (for example, ~55), with fewer at the extremes.<br />
        • **Favor Max**: For a range of 10–100 points, most users receive higher values (for example, 70–100), while fewer receive lower values.
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segments
      </td>
    </tr>

    <tr>
      <td>
        **Max points per reward**
      </td>

      <td>
        Define the maximum number of points that can be awarded in a single transaction or instance. Applicable only when using **Percentage** or **Proportional** earning schemes in Live Behavior campaigns. Not available for **Flat** or **Random** schemes.
      </td>

      <td>
        Cap points at 500 per purchase, even if the % calculation exceeds this value.
      </td>

      <td>
        Live Behavior Segments
      </td>
    </tr>

    <tr>
      <td>
        **Maximum recurrence per user**
      </td>

      <td>
        Control how many times a single user can receive the reward. Multiple limits can be combined (for example, total + per day/week/month).
      </td>

      <td>
        If the total limit is 5 and the per-day limit is 2, the user can receive the reward up to two times per day until they reach a total of 5 rewards.
      </td>

      <td>
        Live Behavior Segments only
      </td>
    </tr>

    <tr>
      <td>
        **Custom points validity**
      </td>

      <td>
        Define the activation and expiry lifecycle of awarded points.
      </td>

      <td>
        • **Activation**: Immediate (points instantly usable) OR Custom delay (for example, activate after 7 days).<br />
        • **Expiry**: Never, fixed date, or custom duration (for example, 30 days after activation).
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segments
      </td>
    </tr>

    <tr>
      <td>
        **Budget**
      </td>

      <td>
        Define the budget to control how rewards are distributed. Budget can be set at two levels:<br />
        • **Per Campaign Budget**: Caps the total rewards that the campaign can distribute.<br />
        • **Per User Budget**: Caps the maximum rewards a single user can receive during the campaign.<br />
        Once the defined limit is reached (per user or for the entire campaign), no further rewards are issued.
      </td>

      <td>
        If the Per Campaign Budget is 5,000 points, rewards stop once the campaign collectively distributes 5,000 points, even if more users qualify.<br />
        If the Per User Budget is 500 points, each user can only receive up to 500 points during the campaign, even if they continue qualifying.
      </td>

      <td>
        Live Behavior Segments only
      </td>
    </tr>

    <tr>
      <td>
        **Custom metadata**
      </td>

      <td>
        Add dynamic key–value pairs to pass additional data into the wallet points payload. Each row has two modes:<br />
        • **System Key**: Select from predefined system keys.<br />
        • **Custom Key**: Define your own key.<br />
        Duplicate keys are not allowed.
      </td>

      <td>
        Add `{ "orderId": "12345", "promoType": "festival" }` as custom metadata to track order-related rewards.
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segments
      </td>
    </tr>
  </tbody>
</Table>

> 📘 Points to Consider
>
> * Custom Activation does not check user behavior. It delays redemption so businesses can increase net profit on orders.
> * Wallet must be pre-configured in your account.

<Image alt="Set Up Loyalty Points in Rewards" align="center" border={true} src="https://files.readme.io/4d437eec9f1f394b546d51406d53ff000e37dfdcf458a6ec637b06d8f1ced0fb-image.png" />  Set Up Loyalty Points in Rewards

## Coupons

Use Coupons to provide users with discount codes or special offers. Coupons must be pre-created in CleverTap and active.

The following configuration options are available when Coupon is selected:

<Table>
  <thead>
    <tr>
      <th>
        Option
      </th>

      <th>
        Description
      </th>

      <th>
        Example / Use Case
      </th>

      <th>
        Available In
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Coupon Type**
      </td>

      <td>
        Choose Single Code (shared) or Bulk Codes (unique).
      </td>

      <td>
        • **Single Code:** A fixed 20% off coupon shared with all users.<br />
        • **Bulk Codes:** Each user gets a unique 10% off coupon.
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segments
      </td>
    </tr>

    <tr>
      <td>
        **Coupon code**
      </td>

      <td>
        Select from available coupons that match the type. Coupon must be active and not fully redeemed.
      </td>

      <td>
        Dropdown lists valid Single or Bulk codes.
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segments
      </td>
    </tr>

    <tr>
      <td>
        **Max coupons per user**
      </td>

      <td>
        Defines how many times the coupon can be rewarded to the same user. This does not control redemption. If a user-level redemption limit is 2 and the same coupon is rewarded twice, user can redeem 4 times total.
      </td>

      <td>
        Selecting *Limit = 1* means each user can only be rewarded the coupon once.
      </td>

      <td>
        Live Behavior Segments only
      </td>
    </tr>

    <tr>
      <td>
        **Max coupons per campaign**
      </td>

      <td>
        Defines the total number of coupon codes that the campaign can distribute.
      </td>

      <td>
        Selecting *Limit = 1000* means the campaign stops distributing coupons after 1000 coupons are issued.
      </td>

      <td>
        Live Behavior Segments
      </td>
    </tr>

    <tr>
      <td>
        **Coupon redemption activation**
      </td>

      <td>
        Define when coupons can be redeemed, immediately or after a custom delay.
      </td>

      <td>
        • **Immediate:** Flash sale means redeem instantly.<br />
        • **Custom:** Redeemable 48 hours after reward assignment.
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segments
      </td>
    </tr>
  </tbody>
</Table>

<Image alt="Set Up Coupons in Rewards" align="center" border={true} src="https://files.readme.io/362ace8d3ea7a677c7c9a93f885bd75dbd8db80a5f74fc2fda32e1de4b2c66ca-image.png" />
  Set Up Coupons in Rewards

## Partner Vouchers

Use Partner Vouchers to distribute unique codes provided by third-party providers integrated with your account.

The following configuration options are available when Partner Voucher is selected:

| Option                     | Description                                                                                                                                                                                                         | Example / Use Case                                                                                      | Available In                                       |
| :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------------------------------------ | :------------------------------------------------- |
| **Partner**                | Select from integrated and active voucher providers.                                                                                                                                                                | Pick Amazon Gift Cards provider.                                                                        | Past Behavior/Custom List + Live Behavior Segments |
| **List tag**               | Select the voucher batch (list tag) for distribution. Codes are auto-assigned uniquely to users.                                                                                                                    | Batch *Holiday2025* with 10,000 gift codes.                                                             | Past Behavior/Custom List + Live Behavior Segments |
| **Max codes per user**     | Defines how many times the voucher can be rewarded to the same user. This does not control redemption. If a user-level redemption limit is 2 and the same voucher is rewarded twice, user can redeem 4 times total. | Selecting *Limit = 1* means each user can only be rewarded the voucher once.                            | Live Behavior Segments only                        |
| **Max codes per campaign** | Defines the total number of voucher codes that the campaign can distribute.                                                                                                                                         | Selecting *Limit = 1000* means the campaign stops distributing vouchers after 1000 vouchers are issued. | Live Behavior Segments                             |

<Image alt="Set Up Partner Vouchers in Rewards" align="center" border={true} src="https://files.readme.io/5ede864217cd7dc80e936bad3e1ea62efb4de25939eca23a041f1d8f2aa1126e-image.png" />  Set Up Partner Vouchers in Rewards

> 📘 Note
>
> * Only active, unexpired voucher lists are displayed.
> * No preview of voucher details is available.
> * System ensures each user receives a unique, unused code.

## Custom Rewards

Use Custom Rewards to integrate external reward systems. When a user qualifies, CleverTap triggers a webhook call to your configured endpoint, enabling you to issue rewards such as third-party gift cards, credits, or custom incentives.

The following configuration options are available when Custom Reward is selected:

<Table align={["left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Option
      </th>

      <th>
        Description
      </th>

      <th>
        Example / Use Case
      </th>

      <th>
        Available In
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Webhook endpoint (mandatory)**
      </td>

      <td>
        Select a pre-configured webhook endpoint from the dropdown. If none exist, click the link provided to add a new configuration.
      </td>

      <td>
        Connect to an external gift card provider API endpoint.
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segment
      </td>
    </tr>

    <tr>
      <td>
        **Custom reward type**
      </td>

      <td>
        Select whether to issue Physical & digital rewards (tangible gifts) or Self-managed wallet credits (monetary/credit-based).
      </td>

      <td>
        Physical & digital: Send a Bluetooth speaker as a gift.<br />
        Self-managed: Credit ₹200 to a user's wallet.
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segment
      </td>
    </tr>

    <tr>
      <td>
        **Physical & digital rewards**
      </td>

      <td>
        Choose a reward that must be pre-created in your account.
      </td>

      <td>
        Select "Amazon Voucher" or "Smartwatch".
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segment
      </td>
    </tr>

    <tr>
      <td>
        **Max recurrence per user**
      </td>

      <td>
        Allows you to control how many rewards can be granted per user on a daily, weekly, or monthly basis.
      </td>

      <td>
        Max per user = 1 reward in a week
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segment
      </td>
    </tr>

    <tr>
      <td>
        **Self-managed wallet credits**
      </td>

      <td>
        Choose a wallet from the dropdown (must be pre-created).
      </td>

      <td>
        Select a wallet to reward credits or money.
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segment
      </td>
    </tr>

    <tr>
      <td>
        **Credits earning scheme** (only for Self-managed wallet credits)
      </td>

      <td>
        Choose how to define wallet credits. Options include:<br />
        • **Flat**: a fixed number of credits for each qualifying user.<br />
        • **Percentage**: credits calculated as a percentage of an event property (for example, order amount).<br />
        • **Proportional**: credits awarded per defined unit of an event property (for example, 10 credits per ₹100 spent).<br />
        • **Random**: credits assigned from a defined range; exposes Value Range + Distribution Bias controls.
      </td>

      <td>
        • **Flat**: All qualifying users get 100 credits.<br />
        • **Percentage**: 10% of ₹500 purchase, i.e., 50 credits.<br />
        • **Proportional**: 10 credits for every ₹100 spent.<br />
        • **Random**: Users get between 10–100 credits.
      </td>

      <td>
        • **Flat** and **Random**: Available in both Past Behavior/Custom List and Live Behavior segments.<br />
        • **Percentage** and **Proportional**: Only available in Live Behavior campaigns (not supported in PBS).
      </td>
    </tr>

    <tr>
      <td>
        **Value**
      </td>

      <td>
        The input control for the credits value changes based on the selected credits Earning Scheme:<br />
        • **Flat**: Enter a single fixed value of credits awarded to each qualifying user.<br />
        • **Percentage**: Define a percentage of a selected event property (for example, order amount) from the qualifying event (typically a Charged event).<br />
        • **Proportional**: Define "credits per unit" of a selected event property (for example, for every X units of the property, award Y credits).<br />
        • **Random**: Set a min–max range of credits; the system randomly selects a value within this range for each qualifying user (also supports Distribution Bias).
      </td>

      <td>
        • **Flat**: Set to 100 means every qualifying user gets 100 credits.<br />
        • **Percentage**: Set to 10% means a purchase of ₹500 (as per selected event property) gives 50 credits.<br />
        • **Proportional**: Set to 10 credits for every ₹100 (as per selected event property).<br />
        • **Random**: Set to a range of 10–100 means each qualifying user gets a random value between 10 and 100.
      </td>

      <td>
        • **Flat** and **Random**: Available in both Past Behavior/Custom List and Live Behavior Segment.<br />
        • **Percentage** and **Proportional**: Available only in Live Behavior campaigns.
      </td>
    </tr>

    <tr>
      <td>
        **Distribution bias** (For Random scheme only)
      </td>

      <td>
        Control distribution pattern that allows you to select the following options:<br />
        • **Favor Min**: skews distribution toward the lower end of the range.<br />
        • **Favor Avg**: skews distribution toward the midpoint of the range.<br />
        • **Favor Max**: skews distribution toward the higher end of the range.
      </td>

      <td>
        • **Favor Min**: For a range of 10–100 credits, most users receive lower values (for example, 10–30), while fewer receive higher values.<br />
        • **Favor Avg**: For a range of 10–100 credits, most users receive values around the midpoint (for example, ~55), with fewer at the extremes.<br />
        • **Favor Max**: For a range of 10–100 credits, most users receive higher values (for example, 70–100), while fewer receive lower values.
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segments
      </td>
    </tr>

    <tr>
      <td>
        **Max credits per rewards** (only for Percentage and Proportional schemes)
      </td>

      <td>
        Enter the maximum credits per reward.
      </td>

      <td>
        Setting 100 means each user can get a maximum of 100 credits per reward.
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segment
      </td>
    </tr>

    <tr>
      <td>
        **Max recurrence per user**
      </td>

      <td>
        Allows you to control how many rewards can be granted per user on a daily, weekly, or monthly basis.
      </td>

      <td>
        Max per user = 1 reward in a day
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segment
      </td>
    </tr>

    <tr>
      <td>
        **Budget**
      </td>

      <td>
        Defines how many rewards can be distributed.<br />
        • **Physical & digital rewards**: Supports campaign-level and time-based limits.<br />
        • **Self-managed wallet credits**: Supports per-campaign and per-user limits (varies by scheme).<br />
        • **Flat**: Supports Per Campaign budget only.<br />
        • **Percentage**: Supports both Per Campaign and Per User budgets.<br />
        • **Proportional**: Supports both Per Campaign and Per User budgets.<br />
        • **Random**: Supports both Per Campaign and Per User budgets.
      </td>

      <td>
        • **Physical & digital rewards**:<br />
          Campaign limit = 5,000 vouchers; additionally, set 1,000 vouchers per month.<br />
        • **Self-managed wallet credits**:<br />
        • **Flat Credits**: Campaign limit = 10,000 credits.<br />
        • **Percentage Credits**: Campaign limit = 10,000 credits and per-user cap = 500 credits.<br />
        • **Proportional Credits**: Campaign limit = 10,000 credits and per-user cap = 500 credits.<br />
        • **Random Credits**: Campaign limit = 10,000 credits and per-user cap = 500 credits.
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segment
      </td>
    </tr>

    <tr>
      <td>
        **User identifiers key mapping**
      </td>

      <td>
        Map CleverTap's default user identity fields (User ID, Email address, Phone number) to your webhook payload keys. Each field supports the following modes: System key (CleverTap's default field names) or Custom key (specify your own key names).
      </td>

      <td>
        Map CleverTap's identity field to your external system's customerId or use default mapping for email and phone.
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segment
      </td>
    </tr>

    <tr>
      <td>
        **Custom metadata**
      </td>

      <td>
        Add dynamic key-value pairs to include contextual data in the reward payload. Duplicate keys are not allowed.
      </td>

      <td>
        Add `{ "orderType": "electronics", "promoType": "festival" }` as custom metadata to track order-related rewards.
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segments
      </td>
    </tr>

    <tr>
      <td>
        **Preview JSON Payload**
      </td>

      <td>
        Displays a live JSON preview that includes reward metadata and configured key-value parameters.
      </td>

      <td>
        For example, refer to [JSON Payload](doc:create-promo-campaigns-copy-1#json-payload)
      </td>

      <td>
        Past Behavior/Custom List + Live Behavior Segment
      </td>
    </tr>
  </tbody>
</Table>

<Image alt="Set Up Reward in Custom Rewards" align="center" border={true} src="https://files.readme.io/539ebea5210050327666ff4ed929383317200eb806d0ab85a7d1fa1ccd95f621-image.png" /> Set Up Reward in Custom Rewards

> 📘 **Points to Consider**
>
> Before you begin:
>
> * Ensure you configure the webhook endpoint before creating the campaign.
> * Verify that the endpoint can handle campaign volume, retries, and logging.
>
> During setup:
>
> * Physical & Digital Rewards and Self-managed Wallet Credits have separate configuration options; choose the appropriate type based on your use case.
> * The reward payload is fully customizable and scales automatically with campaign volume.
> * Custom Rewards give maximum flexibility but require your external system to handle issuance and redemption.

### JSON Payload

```json
{
  "campaign_id": "string",
  "campaign_name": "string",
  "reward_type": "custom",
  "user": {
    "identity": "string",
    "email": "string",
    "phone": "string"
  },
  "reward": {
    "type": "physical_digital | wallet_credits",
    "details": {
      "reward_name": "string",
      "credits": "number",
      "wallet_id": "string"
    }
  },
  "metadata": {
    "custom_key_1": "custom_value_1",
    "custom_key_2": "custom_value_2"
  },
  "timestamp": "ISO_8601_timestamp"
}
```

# Best Practices

Maximize campaign effectiveness and avoid common pitfalls with the following best practices for setup, execution, and management:

* **Use Segments Wisely**: Tailor rewards with meaningful segmentation.
* **Test Before Scaling**: Start small to validate campaign performance.
* **Set Limits**: Always define per-user and per-campaign limits. 
* **Reward Inventory**: Ensure sufficient reward stock throughout the campaign.