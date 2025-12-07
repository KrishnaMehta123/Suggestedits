---
title: Promo Campaign Errors
excerpt: >-
  Learn how Promo Campaign Errors work across all reward types and understand
  why reward distributions fail, so you can quickly troubleshoot and resolve
  issues.
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

The **Errors** tab displays all failed reward distribution attempts for a Promo Campaign. This helps you understand why a reward could not be issued, how frequently each error occurred, and whether limits, configurations, or system-level failures affected campaign performance.

These Errors also help you:

- Diagnose reward delivery failures.
- Verify whether limits like _user-level_, _campaign-level_, or _redemption limits_ are being hit.
- Identify configuration issues with wallets, coupons, vouchers, or reward setups.
- Detect system-level failures such as assignment failures, _parsing errors_, or _inactive reward systems_.

By monitoring these errors, you can take targeted action, such as updating reward configurations, increasing budgets, replacing exhausted code lists, or troubleshooting webhook integrations.

This tab is available for all campaign types and shows historical error logs for the selected date range.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b4306397c0fc8c480f018c5ab3b411f7bce911d99d7f38ee60870b4c142cdccb-image.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


# Total Errors

At the top of the **Errors** tab, you see a summary, i.e., the total number of failed reward distributions for the campaign. If no errors have occurred, the page displays an empty state, indicating that the campaign has been running smoothly without any reward distribution issues.

Errors vary depending on the reward type selected in the campaign:

- [Loyalty Wallet Errors](doc:promo-campaign-errors#loyalty-wallet-errors) 
- [Coupon Errors](doc:promo-campaign-errors#coupon-errors) 
- [Partner Voucher Errors](doc:promo-campaign-errors#partner-voucher-errors) 

## Loyalty Wallet Errors

The following errors may occur when distributing _Loyalty Points_ via a wallet.

| Error Type                                | Description                                                                                     |
| ----------------------------------------- | ----------------------------------------------------------------------------------------------- |
| _Invalid wallet configuration_            | Reward ID or wallet details are invalid.                                                        |
| _Inactive user wallet_                    | User’s wallet is inactive or does not exist.                                                    |
| _Invalid points calculated_               | Calculated points are less than 0 or not a numeric value.                                       |
| _User’s reward recurrence limit exceeded_ | User has already been rewarded the maximum number of times allowed per user from this campaign. |
| _Campaign’s points budget exceeded_       | Campaign has reached the maximum points distribution budget.                                    |
| _User’s points budget exceeded_           | User has already been rewarded the maximum number of points allowed per user in this campaign.  |
| _Points credit failed_                    | Failed to credit points due to a system error.                                                  |

## Coupon Errors

The following errors may occur for _Single Code_ or _Bulk Code_ coupon rewards.

| Error Type                                | Description                                                                     |
| ----------------------------------------- | ------------------------------------------------------------------------------- |
| _Invalid coupon configuration_            | Reward ID or coupon details are invalid.                                        |
| _Inactive coupon_                         | Coupon has expired or is inactive.                                              |
| _Campaign’s coupon limit exceeded_        | Campaign has reached the maximum number of coupons that can be rewarded.        |
| _User’s coupon limit exceeded_            | User has reached the maximum coupon rewards allowed per user for this campaign. |
| _Codes from bulk coupon series exhausted_ | All possible codes from the bulk series have been distributed.                  |
| _Coupon redemption limit exceeded_        | Coupon has reached its maximum redemption limit.                                |
| _Coupon assignment failed_                | Failed to assign a coupon due to a system error.                                |

## Partner Voucher Errors

The following errors may occur when the reward type is a _Partner Voucher List_.

| Error Type                               | Description                                                                      |
| ---------------------------------------- | -------------------------------------------------------------------------------- |
| _Invalid voucher configuration_          | Reward ID or voucher details are invalid.                                        |
| _Inactive voucher list_                  | Voucher list has expired or is inactive.                                         |
| _Campaign’s voucher code limit exceeded_ | Campaign has reached the maximum number of vouchers that can be rewarded.        |
| _User’s voucher code limit exceeded_     | User has reached the maximum voucher rewards allowed per user for this campaign. |
| _Codes from voucher list exhausted_      | All codes from the uploaded voucher list have been distributed.                  |
| _Voucher code assignment failed_         | Failed to assign voucher code due to a system error.                             |