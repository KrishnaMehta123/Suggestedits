---
title: Billing_$99 tier
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
# **Overview**
This document provides information about billing terminologies and calculations for CleverTap Basic users. The billing is based on the Monthly Billable Users, derived from Monthly Active Users and the Data Points as explained in the following sections.

# **Billing Terminologies**
### **Monthly Active User (MAU)**
An MAU is an end-user who has recorded one or more events in a calendar month. When tracking mobile apps and websites, a user active on both devices with the same identity token will be counted as one MAU. 
An organization is charged based on the total number of MAUs across all projects, which means that if a user performs a qualifying event in multiple projects, they are counted once per project.

### **Data Point**
An event, event property, or profile property update is a data point, a usage measure associated with MAU. A total of 2,000 data points are allowed per MAU.
[block:callout]
{
  "type": "info",
  "title": "Profile Property Update",
  "body": "If the user updates more than one profile property at one time, it is counted as one data point."
}
[/block]
Some system and debug events are excluded from the MAU and Data Point calculations. For more information about these events, refer to [Events Excluded from Billing in CleverTap Basic](https://docs.clevertap.com/docs/events-excluded-from-billing-in-clevertap-for-startups).

### **Monthly Billable User (MBU)**
MBU reflects the highest value amongst Selected MAU Tier, MAU Actual Usage, or Processed MAU.
Processed MAU is calculated as the total data points used divided by allowed data points per MAU (2,000 data points). In most cases, users perform fewer than 2,000 data points per month.

**Where do I check my MBU?**
To check your MBUs, navigate to  *Organization* > *Billing* > *My Plan* from your dashboard. It displays the estimated MBUs for the current month for all your organization's projects.
[block:callout]
{
  "type": "info",
  "title": "Access to Organization Section",
  "body": "Only the account administrators have access to the *Organization* section."
}
[/block]
### Data Upload Charges
If data is uploaded to amend a user profile or user activity history, the number of data points uploaded counts toward the total number of data points allocated for the month. The number of data points allocated for each calendar month equals the MAU tier in your pricing agreement times 2,000.

### Data Retention Policy
The default data retention policy for the CleverTap Basic plan is one year, which cannot be changed.

# **Plan Changes and Cancelation**
As a paid subscriber, you can make changes to your plan.

### MAU Tier Upgrade
You can upgrade to a higher MAU tier. To upgrade:
1. Navigate to *Organization* > *My Plan* > *Change Plan*. 
2. Choose the new MAU tier. 
3. Click **Save Changes** to confirm the upgrade.

The upgrade will be effective right away, and a prorated charge for the current month will occur, including charges for any paid add-ons. A confirmation with the payment details and invoice will be sent to your registered billing address. 

[block:callout]
{
  "type": "info",
  "title": "Upgrade Change",
  "body": "The upgrade is effective only upon successful payment. All paid add-ons will also be recalculated as per the new base rate when upgrading the MAU tier."
}
[/block]
To upgrade to an MAU tier of more than 100,000 users, we recommend upgrading to the CleverTap for Enterprise plan to better suit your organization's growing scale and needs. For more information on the plan and pricing, contact our team from the CleverTap dashboard.

### MAU Tier Downgrade 
To downgrade to a lower MAU tier, navigate to your account's *My Plan* > *Change Plan* section and click **downgrading MAU**. For accounts in the trial period, the downgrade happens instantly. For active accounts, the MAU downgrade will be effective after the current billing period. You can cancel the downgrade request anytime before that. And, if you upgrade to a higher MAU tier before the current billing period ends, the scheduled downgrade will get canceled.

###Add-ons Inclusion
Free add-ons are additional features that are available without any extra charge. Paid add-ons are additional features available to an account at an extra cost. To include an add-on in your plan, navigate to *Organization* > *Billing* > *My Plan* > *Change Plan*, then choose the required features you want to add. If you have included a paid add-on in your plan, your card on file will be charged immediately, and an invoice will be generated for this transaction.

###Add-ons Removal
To remove an add-on, navigate to *Organization* > *Billing* > *My Plan* > *Change Plan*, then choose the add-ons you want to remove. For the trial accounts, all add-on removals take effect immediately. Whereas for non-trial accounts, all add-on removals take effect from the next billing cycle, and you can continue using the add-on until then. Removing the add-on disables the running campaigns, journeys, and exports that require the add-on.  If you change your mind, you can cancel the removal before the given billing date and continue to access the add-on. 

###Subscription Cancelation
The project admin can cancel the subscription by navigating to *Organization* > *Billing* > *My Plan* > *Cancel Plan*. You are prompted to select the reason and enter *DELETE* in the acknowledgment field. After the account is canceled, all the projects and corresponding data under the organization are deleted permanently and cannot be retrieved. 
Auto-cancelation of subscription for the entire organization occurs if the payment is overdue for more than 14 days after the account is locked.
[block:callout]
{
  "type": "info",
  "title": "Sign Up Again",
  "body": "After canceling the subscription, you can always [sign up](https://clevertap.com/startup-pricing/) again and start your new project."
}
[/block]
# **Payments and Overages**
### Payment Methods
Under the CleverTap Basic plan, CleverTap accepts all major credit or debit cards (for example, Visa, Mastercard, Discover, and JCB). 
For Indian Customers paying in INR, we also allow eNACH (eMandate via Net Banking). For more information about how it works, refer to [eMandate via NetBanking](https://docs.clevertap.com/docs/emandate-via-netbanking) section.

#### Managing Payment Methods
CleverTap provides the flexibility of having more than one payment method. One of the payment methods is always marked as Default. You can update any one of the saved methods as the default payment method. In this case, all future transactions will be made through the default method.

### Update Billing Information and Card Details
If you are an organization member with billing permissions (Admins), you can update the billing and payment information by clicking **Organization** on the left navigation menu of the dashboard. Then, click **Payment Methods** to update the required details.
[block:callout]
{
  "type": "info",
  "title": "Billing Currency",
  "body": "You cannot change the currency for billing."
}
[/block]
### Payment Failure
In case your payment fails, we notify you right away. You must complete your payment within a grace period of ten days. You can choose to retry with the existing default payment method or use a new payment method. We automatically make the payment method you choose to pay with a default method post successful transaction.

During the grace period, the incoming data, data exports, and dashboard access are not affected. If the payment details are not updated within the grace period, your account access is locked. If you do not clear all outstanding payments within 14 days of the account lock, your account is canceled. After the account is canceled, you can no longer retrieve your account, and all the data is deleted permanently.
[block:callout]
{
  "type": "info",
  "title": "New RBI eMandate Regulations",
  "body": "For Indian Customers, with new Reserve Bank of India (RBI) e-mandate regulations coming into effect, there are high chances your payment may fail. This is because the processing of e-mandate on cards for recurring transactions requires an Additional Factor of Authentication (AFA). For more information, refer to [Compliance with RBI eMandate Regulations](https://docs.clevertap.com/docs/compliance-with-rbi-emandate-regulations)."
}
[/block]
### Exceeding Plan Limits
If you exceed your plan limits, you can upgrade to a higher MAU tier before the end of the billing period to avoid overage charges. For more information on how overages are calculated, refer to [overages calculations](https://docs.clevertap.com/docs/billing#section-overages-calculations).

### Overages Calculations
Any overage is charged for each additional MBU over the plan's MAU tier limit. A total of 2,000 data points are allowed per MAU. Any excess data points over the specified limit will be counted as an additional MAU. 

For every additional 100 MAUs, an overage is charged at 1.2x of the plan's base price (view calculation below). All paid add-ons are charged overages at 1.2x of the plan price.

Example 
Below is an example of overage charges for a subscription with an MAU tier limit of up to 20,000, including add-ons:



[block:parameters]
{
  "data": {
    "h-0": "MAU Limit",
    "h-1": "Monthly Billable Users",
    "h-2": "Base Price",
    "h-3": "Add-on Price",
    "h-4": "Overage for MAU",
    "h-5": "Overage for Add-on",
    "h-6": "Billable Amount*",
    "0-0": "Up to 20,000",
    "1-0": "Up to 20,000",
    "2-0": "Up to 20,000",
    "3-0": "Up to 20,000",
    "0-1": "<20,000 without add-ons",
    "1-1": "<20,000 with add-ons",
    "2-1": "22,000 (2,000 MAUs overage) without add-ons",
    "3-1": "22,000 (2,000 MAUs overage) with add-ons",
    "0-2": "$200",
    "1-2": "$200",
    "2-2": "$200",
    "3-2": "$200",
    "0-3": "$0",
    "2-3": "$0",
    "1-3": "$20",
    "3-3": "$20",
    "0-4": "$0",
    "1-4": "$0",
    "2-4": "Overage (2,000/100*1.2) \n$24",
    "3-4": "Overage (2,000/100*1.2) \n$24",
    "0-5": "$0",
    "1-5": "$0",
    "2-5": "$0",
    "3-5": "$2.4\n($24*10/100)",
    "0-6": "$200",
    "1-6": "$220",
    "2-6": "$224",
    "3-6": "$246.4"
  },
  "cols": 7,
  "rows": 4
}
[/block]
*Not inclusive of taxes, if applicable 


[block:callout]
{
  "type": "info",
  "title": "Overage Calculation for $99 Tier"
}
[/block]
You can view your plan's estimated MBU and overages under *Organization* > *My Plan* > *Usage Summary*. Overage charges get calculated on a pro-rated basis from the start of the billing period for the month in which overages occurred. To avoid overages charges, you will need to upgrade your subscription to a higher MAU tier limit. 
[block:callout]
{
  "type": "info",
  "title": "MBU Usage over 300%",
  "body": "You may lose access to your account for any MBU usage over 300%. There are no overage charges levied during the trial period."
}
[/block]
### Alerts for Overages
All account admins will receive alert emails when their account exceeds their MAU tier limit cap by the following percentages: 80%, 100%, 125%, 150%, 200%, 250%, 300%, and 600%. Account admins are also notified to upgrade to a higher MAU tier through a popup if the account exceeds the MAU tier limit.

### Account Lock and Suspension
#### Account Lock Due to Overages
If your MAU overages exceed 300%, your account may be locked. During this time, you will no longer be able to access the dashboard. To restore account access and avoid overages, you will need to upgrade your subscription to a higher MAU tier limit. Data ingestion and any scheduled or recurring campaigns will not be affected during this time. All data exports via API, SFTP, and third-party partners will be disabled.

If you do not upgrade by the next billing date (the 1st of each month), your account access will be locked, and overages charges will be applicable.

# **Invoices, GST, and Sales Tax**
### View and Manage Invoices
Whenever you purchase a CleverTap Basic subscription, you can find your invoices under the billing tab of your admin section. The invoice is sent on the first of every month only to the email added under the billing details section. For more details on changing the invoice recipient, refer to the [Change Invoice Recipients and Billing Details](https://docs.clevertap.com/docs/billing#section-change-invoice-recipients-and-billing-details) section. 

To find your invoices:
1. Click **Organization** on the left navigation menu of the dashboard. Click **Billing details** > **Invoices**. From there, you will be able to view all invoices. 
2. To view the entire invoice, click on an invoice number.

[block:callout]
{
  "type": "info",
  "title": "Invoice Access",
  "body": "Only account admins can access and update invoices."
}
[/block]
# **Change Invoice Recipients and Billing Details**
To change the invoice recipient or update invoice details:
1. Click on the **Billing Details** section under *Organization* on the CleverTap dashboard. 
2. Click **Save** to apply your changes. 

Any changes made to these settings will reflect on the next invoice. 

# **GST Invoicing (India Only)**
CleverTap supports GST invoicing for customers in India. GST (Goods and Services Tax) is a mandatory levy for all Indian Rupee (INR) invoices as per regulatory requirements in India. Businesses registered in India can input their GSTIN (GST Identification Number) during the signup process.