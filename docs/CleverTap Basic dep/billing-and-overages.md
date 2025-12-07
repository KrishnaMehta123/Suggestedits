---
title: Billing and Overages
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

This document provides information about billing terminologies and calculations for CleverTap Basic users. The billing is based on the Monthly Billable Users, derived from Monthly Active Users and the Data Points as explained in the following sections.

# Billing Terminologies

The following terminologies are often used in CleverTap for Startups billing operations:

### Monthly Active User (MAU)

An MAU is an end-user who has recorded one or more events in a calendar month. When tracking mobile apps and websites, a user active on both devices with the same identity token will be counted as one MAU.\
An organization is charged based on the total number of MAUs across all projects, which means that if a user performs a qualifying event in multiple projects, they are counted once per project.

### Data Point

An event, event property, or profile property update is a data point, a usage measure associated with MAU. A total of 10,000 data points are allowed per MAU.

> 📘 Profile Property Update
>
> If the user updates more than one profile property at one time, it is counted as one data point.

The MAU and Data Point calculations exclude some system and debug events. For more information about these events, refer to [Events Excluded from Billing in CleverTap Basic](https://docs.clevertap.com/docs/events-excluded-from-billing-in-clevertap-for-startups).

### Monthly Billable User (MBU)

MBU reflects the highest value amongst Selected MAU Tier, Actual Usage, or Processed MAU.\
Processed MAU is calculated as the total data points divided by allowed data points per MAU (10,000). In most cases, users perform fewer than 10,000 data points per month.

To check your MBUs, navigate to  *Organization* > *Billing* > *My Plan* from your dashboard. It displays the estimated MBUs for the current month for all your organization's projects.

> 📘 Access to Organization Section
>
> Only the account administrators can access the *Organization* section on the CleverTap dashboard.

### Overages

Overages are over usage charges which will be added as a billable amount if you exceed your plan limits. You can always upgrade to a plan of higher MAU to avoid paying overages. For more details on overages calculation, refer to [Overages Calculation](https://docs.clevertap.com/docs/billing-and-overages#overages-calculations).

### Data Upload Charges

If data is uploaded to amend a user profile or activity history, the number of data points uploaded counts toward the total number allocated for the month. The number of data points allocated for each calendar month equals the MAU tier in your pricing agreement times 10,000.

### Data Retention Policy

The default data retention policy for the CleverTap Basic plan is one year, which cannot be changed.

# Plan Changes and Cancelation

As a paid subscriber, you can make changes to your existing plan. The following sections help to understand the different plan changes and plan cancellation:

### MAU Tier Upgrade

You can upgrade to a higher MAU tier. To upgrade:

1. Navigate to *Organization* > *My Plan* > *Change Plan*. 
2. Choose the new MAU tier. 
3. Click **Save Changes** to confirm the upgrade.

The upgrade will be effective right away, and a prorated charge for the current month will occur, including charges for any paid add-ons. A confirmation with the payment details and invoice will be sent to your registered billing address. 

> 📘 Upgrade Change
>
> The upgrade is effective only upon successful payment. All paid add-ons will also be recalculated per the new base rate when upgrading the MAU tier.

To upgrade to an MAU tier of more than 100,000 users, we recommend upgrading to the CleverTap for Enterprise plan better to suit your organization's growing scale and needs. For more information on the plan and pricing, contact our team from the CleverTap dashboard.

### MAU Tier Downgrade

To downgrade to a lower MAU tier, navigate to your account's *My Plan* > *Change Plan* section and click **downgrading MAU**. For accounts in the trial period, the downgrade happens instantly. For active accounts, the MAU downgrade will be effective after the current billing period. You can cancel the downgrade request anytime before that. And, if you upgrade to a higher MAU tier before the current billing period ends, the scheduled downgrade will get cancelled.

### Add-ons Inclusion

Free add-ons are additional features that are available without any extra charge. Paid add-ons are additional features available to an account at an extra cost. To include an add-on in your plan, navigate to *Organization* > *Billing* > *My Plan* > *Change Plan*, then choose the required features you want to add. If you have included a paid add-on in your plan, your card on file will be charged immediately, and an invoice will be generated for this transaction.

### Add-ons Removal

To remove an add-on, navigate to *Organization* > *Billing* > *My Plan* > *Change Plan*, then choose the add-ons you want to remove. For the trial accounts, all add-on removals take effect immediately. Whereas for non-trial accounts, all add-on removals take effect from the next billing cycle, and you can continue using the add-on until then. Removing the add-on disables the running campaigns, journeys, and exports that require the add-on.  If you change your mind, you can cancel the removal before the given billing date and continue to access the add-on. 

### Subscription Cancelation

The project admin can cancel the subscription by navigating to *Organization* > *Billing* > *My Plan* > *Cancel Plan*. You are prompted to select the reason and enter *DELETE* in the acknowledgement field. After the account is cancelled, all the projects and corresponding data under the organization are deleted permanently and cannot be retrieved.\
Auto-cancellation of subscription for the entire organization occurs if the payment is overdue for more than 14 days after the account is locked.

> 📘 Sign Up Again
>
> After cancelling the subscription, you can always [sign up](https://clevertap.com/startup-pricing/) again and start your new project.

# Payments and Overages

### Payment Methods

Under the CleverTap Basic plan, CleverTap accepts all major credit or debit cards (for example, Visa, Mastercard, Discover, and JCB).\
For Indian Customers paying INR, we also allow eNACH (eMandate via Net Banking). For more information about how it works, refer to [eMandate via NetBanking](https://docs.clevertap.com/docs/emandate-via-netbanking) section.

#### Managing Payment Methods

CleverTap provides the flexibility of having more than one payment method. One of the payment methods is always marked as Default. You can update any of the saved methods as the default payment method. In this case, all future transactions will be made through the default method.

### Update Billing Information and Card Details

If you are an organization member with billing permissions (Admins), you can update the billing and payment information by clicking **Organization** on the left navigation menu of the dashboard. Then, click **Payment Methods** to update the required details.

> 📘 Billing Currency
>
> You cannot change the currency for billing.

### Payment Failure

In case your payment fails, we will notify you right away. You must complete your payment within a grace period of ten days. You can retry with the existing default payment method or use a new one. We automatically make the payment method you choose with a default method post successful transaction.

The incoming data, data exports, and dashboard access are not affected during the grace period. Your account access is locked if the payment details are not updated within the grace period. If you do not clear all outstanding payments within 14 days of the account lock, your account is cancelled. After the account is cancelled, you can no longer retrieve your account, and all the data is deleted permanently.

> 📘 New RBI eMandate Regulations
>
> For Indian Customers, with new Reserve Bank of India (RBI) e-mandate regulations coming into effect, there are high chances your payment may fail. This is because processing e-mandate on cards for recurring transactions requires an Additional Factor of Authentication (AFA). For more information, refer to [Compliance with RBI eMandate Regulations](https://docs.clevertap.com/docs/compliance-with-rbi-emandate-regulations).

### Exceeding Plan Limits

If you exceed your plan limits, you can upgrade to a higher MAU tier before the end of the billing period to avoid overage charges. For more information on how overages are calculated, refer to [overages calculations](https://docs.clevertap.com/docs/billing#section-overages-calculations).

### Overages Calculations

Any overage is charged for each additional MBU over the plan's MAU tier limit. A total of 10,000 data points are allowed per MAU. Any excess data points over the specified limit will be counted as an additional MAU. 

For every additional 100 MAUs, an overage is charged at 1.2x of the plan's base price (view calculation below). All paid add-ons are charged overages at 1.2x of the plan price.

**Example**\
Below is an example of overage charges for a subscription with an MAU tier limit of up to 20,000, including add-ons:

<Table align={["left","left","left","left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        MAU Limit
      </th>

      <th>
        Monthly Billable Users
      </th>

      <th>
        Base Price
      </th>

      <th>
        Add-on Price
      </th>

      <th>
        Overage for MAU
      </th>

      <th>
        Overage for Add-on
      </th>

      <th>
        Billable Amount

        \*
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Up to 20,000
      </td>

      <td>
        \<20,000 without add-ons
      </td>

      <td>
        $200
      </td>

      <td>
        $0
      </td>

      <td>
        $0
      </td>

      <td>
        $0
      </td>

      <td>
        $200
      </td>
    </tr>

    <tr>
      <td>
        Up to 20,000
      </td>

      <td>
        \<20,000 with add-ons
      </td>

      <td>
        $200
      </td>

      <td>
        $20
      </td>

      <td>
        $0
      </td>

      <td>
        $0
      </td>

      <td>
        $220
      </td>
    </tr>

    <tr>
      <td>
        Up to 20,000
      </td>

      <td>
        22,000 (2,000 MAUs overage) without add-ons
      </td>

      <td>
        $200
      </td>

      <td>
        $0
      </td>

      <td>
        Overage (2,000/100\*1.2)\
        $24
      </td>

      <td>
        $0
      </td>

      <td>
        $224
      </td>
    </tr>

    <tr>
      <td>
        Up to 20,000
      </td>

      <td>
        22,000 (2,000 MAUs overage) with add-ons
      </td>

      <td>
        $200
      </td>

      <td>
        $20
      </td>

      <td>
        Overage (2,000/100\*1.2)\
        $24
      </td>

      <td>
        $2.4\
        ($24\*10/100)
      </td>

      <td>
        $246.4
      </td>
    </tr>
  </tbody>
</Table>

('\*' indicates Not inclusive of taxes, if applicable.)

You can view your plan's estimated MBU and overages under *Organization* > *My Plan* > *Usage Summary*. Overage charges get calculated on a pro-rated basis from the start of the billing period for the month in which overages occurred. To avoid overages charges, you will need to upgrade your subscription to a higher MAU tier limit. 

> 📘 MBU Usage over 300%
>
> You may lose access to your account for any MBU usage over 300%. There are no overage charges levied during the trial period.

### Alerts for Overages

All account admins will receive alert emails when their account exceeds their MAU tier limit cap by the following percentages: 80%, 100%, 125%, 150%, 200%, 250%, 300%, and 600%. Account admins are also notified to upgrade to a higher MAU tier through a popup if the account exceeds the MAU tier limit.

### Account Lock and Suspension

#### Account Lock Due to Overages

If your MAU overages exceed 300%, your account may be locked. During this time, you will no longer be able to access the dashboard. To restore account access and avoid overages, you will need to upgrade your subscription to a higher MAU tier limit. Data ingestion and any scheduled or recurring campaigns will not be affected during this time. All data exports via API, SFTP, and third-party partners will be disabled.

If you do not upgrade by the next billing date (the 1st of each month), your account access will be locked, and overages charges will be applicable.

# Invoices, GST, and Sales Tax

### View and Manage Invoices

Whenever you purchase a CleverTap Basic subscription, you can find your invoices under the billing tab of your admin section. The invoice is sent on the first of every month only to the email added under the billing details section. For more details on changing the invoice recipient, refer to the [Change Invoice Recipients and Billing Details](https://docs.clevertap.com/docs/billing#section-change-invoice-recipients-and-billing-details) section. 

# Tax Invoicing

Following are the types of tax invoicing applicable in CleverTap for Startups:

## VAT

There is a field provided to USD customers for entering tax numbers, which is shown in the invoice for USD accounts.

## GST

CleverTap supports GST invoicing for customers in India. GST (Goods and Services Tax) is a mandatory levy for all Indian Rupee (INR) invoices as per regulatory requirements in India. Businesses registered in India can input their GSTIN (GST Identification Number) during the signup process.

## TDS

Compliance with regards to the TDS or withholding taxes is required to be taken by the customer. To comply with the requirement, you are required to gross up the amount paid to CleverTap and accordingly calculate the TDS on the same.\
For example, If INR 14000 + GST is the monthly invoice and you need to withhold 2% TDS,then 2% of Rs.14000 or INR 280 becomes the withholding tax, and you have to expense it out at your end. Please check the terms and conditions mentioned on the online page related to TDS or withholding taxes. Please refer to [section 6.2](https://clevertap.com/terms-service) of the terms and conditions.
