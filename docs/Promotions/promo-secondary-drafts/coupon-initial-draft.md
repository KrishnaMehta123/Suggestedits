---
title: Coupons (Initial Draft)
excerpt: ''
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

The Coupons feature allows businesses to create, manage, and track coupon-based campaigns. This guide provides an in-depth understanding of how to configure coupons, track coupon events, manage bulk coupon codes, and set up redemption limits and cashback systems.

# Purpose and Benefits

# Key Features

# Coupon System Overview

Coupons can be assigned to users in two primary ways:

- **All Users Coupons**: Available to all users based on predefined criteria.
- **Campaign Users Coupons**: Assigned based on campaign-specific rules.

Coupons follow a structured lifecycle, including reward, activation, redemption, and expiration. The system also allows for cashback integration and webhook-based reward distribution.

## Coupons List Page

### Current Tab (All Coupon)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/385d230334e6af66ccc688695dad25c10ca60f741c525d07cb5d4264d5488a4f-image.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


### Archive Tab (Archived Coupons)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b99c733eb1eae34d51385cd26b1f8463c2e8750b3296b2118639b4a12d6d98b1-image.png",
        null,
        null
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


<br />

#### Filters and Operations

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/79b6a6c536e008fd35ac125973fc1a4f6ada382d9b488267546c4e149fbbe705-image.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


# Create Coupon

1. Navigate to Promotions > Rewards > Coupons
2. Click Create Coupon button. The coupon setup pop up opens.

   [block:image]{"images":[{"image":["https://files.readme.io/268d88a3e4fbfb24a5edc6d0049149012323b34bf78092391a00d71015c4d274-image.png",null,""],"align":"center","border":true}]}[/block]

## Coupon Setup

### Code Types

1. **Single Code: Open to All Users**  
   Create a single code available to all users, usable multiple times or as defined by campaign rules.
2. **Single Code: Rule-Based Assignment**  
   Assign a single code to specific users based on their actions, managed through predefined rules.
3. **Bulk Codes: Downloadable**  
   Generate multiple unique codes that users can download, with each code usable only once per
4. **Bulk Codes: Rule-Based Assignment**  
   Distribute multiple unique codes to users automatically based on their actions, with each

### Apply to

- **Entire Order**: Apply the discount to all items in the order, regardless of quantity.
- **Selected Items Only**: Apply the discount to specific order properties like shipping price, handling fees etc
- **Custom Order Property**: Apply the discount only to specific items selected by you, leaving the rest of the order unaffected.

# Coupon System Events

The system tracks the following key events associated with coupons:

- Coupon Rewarded
- Coupon Activated
- Coupon Redeemed
- Coupon Reverted

## Coupon Rewarded

Raised when a user is rewarded with a coupon from a campaign.

### Properties

Identity, Coupon Name, Coupon ID, Coupon Code, Campaign ID & Name, Campaign Type, Coupon Description, Coupon Terms and Conditions, Coupon Start Date, Activation Date, and Expiry Date, Timestamp

## Coupon Activated

Raised when the coupon is activated based on the activation days set in the campaign. If activation days are set to 0, only the _Coupon Rewarded_ event is triggered.

### Properties

Identity, Coupon Name, Coupon ID, Coupon Code, Campaign ID & Name, Campaign Type, Coupon Description, Coupon Terms and Conditions, Coupon Start Date, Activation Date, and Expiry Date, Timestamp

## Coupon Redeemed

Raised when a coupon is redeemed via the redemption API.

### Properties

Identity, Order ID, Coupon Code, Coupon ID, Coupon Name, Discount Amount, Cashback Points, Timestamp

## Coupon Reverted

Raised when a previously redeemed coupon is reverted.

### Properties

Identity, Order ID, Coupon Code, Coupon ID, Coupon Name, Discount Amount, Cashback Points, Timestamp

# Coupon Activation and Expiry

## Coupon Activation Rules

### All Users Coupons (Fixed & Bulk Downloadable)

- Activation is based on the coupon’s activation date.
- If the coupon’s start date is in the future, its status is set to "Scheduled."

### Campaign Users Coupons (Fixed & Bulk)

- Activation follows the campaign reference.
- Coupon start date = Timestamp of first reward recurrence.
- Coupon activation date = Start date + X activation days (if not set, it activates immediately).
- If additional coupons are rewarded from the same or different campaigns, redemption counts increase, but activation happens after X days.

## Coupon Expiry Rules

### All Users Coupons (Fixed & Bulk Downloadable)

- Expiry is based on the end date.
- All users share the same expiry date.

### Campaign Users Coupons (Fixed & Bulk)

- Expiry is based on activation and expiry days.
- Each user’s expiry date varies depending on their activation date.
- Example: If a coupon is activated on September 15 at 2:30 PM with a 2-day expiry, it expires on September 17 at 2:30 PM.

# Bulk Coupon Code Generation

- **Bulk Codes Downloadable**: Generate and download bulk codes based on the configured format.
- **Bulk Codes for Campaign Users**: Generate unique codes for eligible users.
- **Retry Mechanism**: If generation fails, an automatic retry mechanism is triggered.
- **Duplicate Prevention**: Prevents duplicate coupon codes for the same user across campaigns.
- **Concurrency Control**: Ensures bulk codes are generated uniquely using resource locking.
- **Code Limits**:
  - Calculate total possible codes based on format.
  - Error handling if required codes exceed available unique codes.
- **Speed**: The system generates 1,000 codes per second.
- **Pausing/Ending/Archiving**: When a bulk code series is paused or ended, all related coupons are paused or ended as well.

# Redemption Limit and Consumption

## Prioritization of Redemption Limits

1. **Limit Type:** Per Code > Per User
2. **Time-Based Limits:** Total > Month > Week > Day

## Default Redemption Limits

- **Single Codes**:
  - Per Code Total Limit: Unlimited (by default).
  - Per User Total Limit: 1 (customizable).
- **Bulk Codes**:
  - Default to 1 per user.

## Redemption Flow

- If no daily/weekly/monthly limit is set, users can redeem up to the total limit.
- If the same coupon is rewarded multiple times, a new record is created for each instance.
- Redemption limits can be edited post-assignment; negative values appear if the limit is reduced retroactively.

## Consumption Logic

#### **Rule-Based Coupons with Multiple Assignments**

1. Identify all available active coupon instances.
2. Select the coupon with the earliest expiry date.
3. If tied, choose based on the lowest remaining redemption limit.
4. If still tied, use the earliest activation date or randomly select one.

#### **Coupons with Never Expiry & Unlimited Limits**

- The system keeps consuming from the same record unless multiple assignments exist.

#### **Coupons with Never Expiry & Limited Redemptions**

- Selection prioritizes the coupon with the lowest remaining redemptions.
- If multiple coupons have the same limit, the earliest activation date is used.