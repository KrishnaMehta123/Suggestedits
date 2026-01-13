---
title: Tier Program
excerpt: >-
  Learn how to drive user engagement and retention with personalized, real-time
  reward campaigns across any industry.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

Tier Program allows you to group users into different levels (tiers) based on their activity and reward them accordingly. As users engage more with your app by spending more, performing key actions, or earning points, they can progress to higher tiers and unlock enhanced benefits. 

Common examples of tiers include airline loyalty tiers (Silver, Gold, Platinum), E-commerce membership levels (Bronze, Silver, Gold), and so on. Tier Systems work seamlessly with Rewards such as [Loyalty Wallets](doc:loyalty-wallets), [Coupons](doc:coupons), [Partner Vouchers](doc:partner-vouchers), and [Custom Rewards](doc:custom-rewards) within CleverTap Promotions. 

With Tier Systems, you can:

* Automatically assign users to tiers based on their actions in the app
* Define clear upgrade and downgrade rules
* Reward users differently at each tier
* Control how long tiers remain valid
* Periodically re-evaluate user eligibility

# How Tier Systems Work (Conceptual Model)

A Tier System consists of five core components:

1. **Program Details** – Who enters the tier system and what activity is tracked
2. **Tier Definition** – The tiers and the criteria to reach them
3. **Tier Rewards** – Rewards assigned to each tier
4. **Qualification and Expiry** – When and how users are evaluated
5. **Downgrade Policy** – What happens when users no longer qualify

> **Important:**
> A Tier System must include:
>
> * At least **one tier upgrade criterion**
> * At least **one earned tier** (beyond the default tier)

***

## Creating a Tier System

Navigate to:
**Promotions → Tier Systems → Create Tier System**

***

## 1. Program Details

This section defines **entry rules** and **upgrade signals** for your tier system.

### Tier System Name

Enter a name to identify this tier system internally.

**Example:**
`Airmiles Plus`, `BlueChip Membership`

***

### Existing Users Tier

Choose how existing users should be handled when the tier system is published.

* Existing users can be placed:

  * In the default tier, or
  * In specific tiers based on available data

This ensures historical users are not excluded.

***

### Default Tier Assignment

Defines **how users enter the tier system**.

Select an event that adds users to the default tier.

**Example:**

* Event: `Signup`
* Result: Every user who signs up enters the tier system in the default tier

You can optionally apply filters to narrow eligibility.

***

### Tier Upgrade Criteria

Tier upgrade criteria define **what user activity is tracked** for tier progression.

You must add **at least one criterion**.

Supported criterion types include:

* Count of an event (for example, number of purchases)
* Sum of an event property (for example, total order value)
* Points collected in a loyalty wallet

> These criteria are **reused later** when defining individual tiers.

***

## 2. Tier Definition

This section defines the **tier hierarchy** and **conditions to reach each tier**.

***

### Tier 1 (Default)

* All users start in the default tier
* Default tiers are **permanent** and **do not expire**
* Entry criteria are defined in Program Details and cannot be edited here

**Use case:**
Provide entry-level benefits for new or low-engagement users.

***

### Earned Tiers (Tier 2 and above)

Earned tiers represent higher status levels that users must qualify for.

For each earned tier, configure:

#### Tier Name

Example: `Silver`, `Gold`, `Diamond`

***

#### Tier Expiry

Choose whether this tier:

* Does not expire, or
* Expires based on evaluation rules

***

#### Tier Criteria

Define the conditions required to enter this tier using the upgrade criteria defined earlier.

You can combine criteria using **OR** logic.

**Example (Silver Tier):**

* Points collected ≥ 500 **OR**
* Orders completed between 5 and 10 **OR**
* Total spend between ₹5,000 and ₹10,000

> If a user satisfies **any** condition, they qualify for the tier.

***

### Adding Tiers

* You must add **at least one earned tier**
* Tiers follow a hierarchy from lowest to highest

***

## 3. Tier Rewards

This section defines **what users receive** at each tier.

Rewards are applied **while users are in the tier**.

***

### Default Tier Rewards

Rewards applied to all users in the default tier.

**Examples:**

* Basic wallet points
* Welcome coupons

***

### Earned Tier Rewards

Rewards applied to users who qualify for higher tiers.

Supported reward types:

* Wallet points
* Coupons
* Partner vouchers
* Custom rewards (via webhook)

Each tier can have different reward configurations.

***

### Adding a Reward

When adding a reward, configure:

* **Reward type**
* **Reward value**
* **Expiry behavior**

For wallet points, you can also configure:

* Fixed or random points
* Points expiry (never, when tier expires, or custom date)

***

## 4. Qualification and Expiry

This section controls **how often users are evaluated** and **how long tiers remain valid**.

***

### Tier Expiry

Choose when tier benefits expire and users are re-evaluated.

#### Every Calendar Year

* All users are evaluated at the end of each calendar year
* Tier entry date does not matter

#### Custom Duration

* Tiers are evaluated after a fixed duration (for example, 12 months)
* Duration is calculated from when the user enters the tier

***

### Qualification Period

Defines which user activity is considered during evaluation.

#### Within Tier Validity

* Only activity after the user entered the tier is considered

#### Rolling Window

* Only activity within the selected time window is considered
* The window moves forward as time progresses

**Example:**
Evaluate user spend in the last 6 months, regardless of tier entry date.

***

## 5. Downgrade Policy

This section defines what happens when users **no longer qualify** for their current tier.

### Downgrade Options

* **Highest tier they qualify for**
  Users are reassigned to the highest tier they still meet criteria for.
  If none, they move to the default tier.

* **Next lower tier**
  Users move down one tier at a time.

* **Default tier**
  Users are moved directly to the default tier.

Choose the option that best matches your loyalty strategy.

***

## Validation and Publish Rules

A Tier System cannot be published unless:

* At least **one tier upgrade criterion** is added
* At least **one earned tier** is created

Clear error messages guide you to resolve missing configuration before publishing.

***

## Example: E-commerce Tier System

**Program Details**

* Entry: Signup
* Upgrade criteria: Orders placed, total spend

**Tier Definition**

* Bronze: Default
* Silver: 5+ orders
* Gold: ₹20,000+ spend

**Tier Rewards**

* Bronze: Free delivery once
* Silver: Extra cashback
* Gold: Priority delivery + exclusive coupons

**Qualification**

* Rolling 12-month window

**Downgrade**

* Move to highest qualifying tier

***

## Key Notes and Best Practices

* Keep tier criteria simple and understandable
* Avoid too many tiers (3–5 is ideal)
* Ensure rewards increase meaningfully across tiers
* Align qualification periods with business cycles
* Communicate tier benefits clearly to users

***

## Related Features

* Loyalty Wallets
* Coupons
* Partner Vouchers
* Promo Campaigns

***

If you want, I can next:

* Convert this into **official docs.clevertap.com formatting**
* Write **developer-facing API documentation**
* Create **CSM enablement guides**
* Add **UX screenshots + callouts**
* Create a **short “How Tier Systems Work” explainer section**

Just tell me what’s next.
