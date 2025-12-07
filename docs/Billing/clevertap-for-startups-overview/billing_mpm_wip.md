---
title: Billing_MPM_WIP
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
[block:api-header]
{
  "title": "Overview"
}
[/block]
This section provides billing-related information for CleverTap for Startups.

## **Billing for Monthly Active Users**
This section covers various CleverTap for Startups billing information regarding monthly active users (MAUs).

### Billable MAU
An MAU is an end-user who has recorded one or more events in a calendar month. When tracking mobile apps and websites, a user who is active on both devices with the same identity token is counted as one MAU. An organization is charged based on the total number of MAUs across all projects i.e. if a user performs a qualifying event in multiple projects, they are counted once per project. Events excluded under the MAU calculation are Notification Sent, Push Impression, and Webhook Delivered.

Billable MAU is a combination of MAUs and data points. A data point is an event, event property, or profile property update; a usage measure associated with MAU. A total of 2,000 data points are allowed per MAU.

### Billable MAU Calculation
The total bill amount per month is based on whichever is highest, such as: 
  * MAU tier limit as defined on your plan.
  * Actual MAU usage.
  * Processed MAU, which is the total data points used divided by allowed data points per MAU (2,000 data points). In most cases, users perform fewer than 2,000 data points per month.

### Check Billable MAUs
To check your billable MAUs, navigate to  *Organization* > *Projects* from your dashboard. It displays the billable MAUs for the current month and previous month for all the projects in your organization.
[block:callout]
{
  "type": "info",
  "title": "Note",
  "body": "Only the account administrators have access to the *Organization* section."
}
[/block]
### Data Upload Charges
If data is uploaded to amend a user profile or user activity history, the number of data points uploaded counts toward the total number of data points allocated for the month. The number of data points allocated for each calendar month equals the MAU tier in your pricing agreement times 2,000.

### Data Retention Policy
The default data retention policy for the CleverTap for Startups plan is one year, which cannot be changed.

## **Plan Update**
As a paid subscriber, you can make changes to your plan.

### MAU Tier Upgrade
To upgrade to a higher MAU tier:
1. Navigate to *Organization* > *My Plan* > *Change Plan*. 
2. Choose the new MAU tier. 
3. Click **Save Changes** to confirm the upgrade.

The upgrade is effective right away, and a prorated charge for the current month is incurred, including charges for any paid add-ons. A confirmation with the payment details and invoice is sent to your registered billing address. 
[block:callout]
{
  "type": "info",
  "title": "Upgrade Change",
  "body": "The upgrade is effective only upon successful payment. All paid add-ons are also recalculated as per the new base rate when upgrading the MAU tier."
}
[/block]
To upgrade to an MAU tier of more than 100,000 users, we recommend upgrading to the CleverTap Enterprise plan to better suit your organization’s growing scale and needs. For more information on the plan and pricing contact our team from the CleverTap dashboard.

### MAU Tier Downgrade 
To downgrade to a lower MAU tier, request a plan update from the My Plan section of your account. Your request is reviewed by our team and we notify you with a confirmation of the downgrade in a timely manner. 
[block:callout]
{
  "type": "info",
  "title": "Billing Cycle",
  "body": "MAU tier downgrades are effective starting from the next billing cycle date."
}
[/block]
### Add-ons Inclusion
**Free add-ons** are additional features that are available without any extra charge.** Paid add-ons **are additional features that are available to an account at an extra charge. To include an add-on in your plan, navigate to *Organization* > *Billing* > *My Plan* > *Change Plan*, and then choose the required features you want to add. If you have included a paid add-on in your plan, your card on file is charged right away, and an invoice is generated for this transaction.

### Add-ons Removal
To remove an add-on, navigate to *Organization* > *Billing* > *My Plan* > *Change Plan*, and then choose the add-ons you want to remove. All add-on removals take effect from the next billing cycle, and you can continue using the add-on until then. If you change your mind, you can cancel the removal before the given billing date and continue to access the add-on.

## **Subscription Cancellation**
To cancel your subscription, submit a cancellation request from the dashboard by navigating to *Organization* > *Billing* > *My Plan* > *Cancel Plan*. Once the request is received, our billing team initiates the cancellation process. You receive an email once the cancelation is processed.

##**Payments and Overages**

### Payment Methods
Under CleverTap for Startups plan, CleverTap accepts all major credit or debit cards (for example, Visa, Mastercard, Discover, and JCB). 
For Indian Customers, we also allow eNACH (eMandate via Net Banking). For more information about how eMandate via NetBanking works, refer to [eMandate](https://docs.clevertap.com/docs/emandate-via-netbanking) section.

#### Managing Payment Methods
CleverTap provides the flexibility of having more than one payment method. One of the payment methods is always marked as Default. You can update any one of the saved methods as the default payment method. In this case, all future transactions will be made through the default method.

### Update Billing Information and Card Details
If you are an organization member with billing permissions (Admins), you can update the billing and payment information by clicking **Organization** on the left navigation menu of the dashboard. Then, click **Payment Methods** to update the required details.
[block:callout]
{
  "type": "info",
  "title": "Update Billing Currency",
  "body": "You cannot update the currency of [billing](https://google.com). for more, see this."
}
[/block]
### Payment Failure

In case your payment fails, we notify you right away. You are required to complete your payment within a grace period of 10 days. You can choose to retry with the existing default payment method or use a new payment method. We automatically make the payment method you choose to pay with a default method post successful transaction.

During the grace period, the incoming data, data exports, and dashboard access are affected. If the payment details are not updated within the grace period, your account access is locked. If you do not clear all outstanding payments within ten days of the account lock, your account is suspended. After account suspension, you can no longer retrieve your account, and all the data is deleted permanently.
[block:callout]
{
  "type": "info",
  "body": "For Indian Customers, with new Reserve Bank of India (RBI) e-mandate regulations coming in to effect, there are high chances your payment may fail. This is because the processing of e-mandate on cards for recurring transactions require an Additional Factor of Authentication (AFA). For more information, refer to [Compliance with RBI eMandate Regulations](https://docs.clevertap.com/docs/compliance-with-rbi-emandate-regulations).",
  "title": "New RBI eMandate Regulations"
}
[/block]
### Exceeding Plan Limits
If you exceed your plan limits, you can upgrade to a higher MAU tier before the end of the billing period to avoid overage charges. For more information on how overages are calculated, refer to [Overages Calculation](https://docs.clevertap.com/docs/billing#section-overage-calculations).

### Overages Calculation
Any overage is charged for every additional billable MAU over the plan's MAU tier limit. A total of 2,000 data points are allowed per MAU. Any excess data points over the specified limit are counted as an additional MAU. 

For every additional 100 MAUs, an overage is charged at 1.2x of the plan's base price (refer to the table for calculation). All paid add-ons are charged overages at 1.2x of the plan price.

Example 
Following is an example of overage charges for a subscription with an MAU tier limit of up to 20,000, including add-ons:
[block:parameters]
{
  "data": {
    "h-0": "MAU Limit",
    "h-1": "Billable MAU",
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
**Not inclusive of taxes, if applicable *

You can view the estimated billable MAU and overages for your plan under *Organization* > *My Plan* > 
*Usage Summary*. Overage charges are calculated on a pro-rated basis from the start of the billing period for the month in which overages occurred. To avoid overages charges, you need to upgrade your subscription to a higher MAU tier limit. 
[block:callout]
{
  "type": "info",
  "title": "Billable MAU Usage over 300%",
  "body": "You may lose access to your account for any billable MAU usage over 300%. There are no overage charges levied during the trial period."
}
[/block]
### Alerts for Overages
All account admins receive alert emails when their account exceeds their MAU tier limit cap by the following percentages: 80%, 100%, 125%, 150%, 200%, 250%, 300%, and 600%. Account admins are also notified to upgrade to a higher MAU tier through a popup if the account exceeds the MAU tier limit.

### Account Lock and Suspension
If your MAU overages exceed 300%, your account can be locked. During this time, you can no longer access the dashboard. To restore account access and avoid overages, you are required to upgrade your subscription to a higher MAU tier limit. During this time, data ingestion and any scheduled or recurring campaigns are not affected. All data exports via API, SFTP, and third-party partners are disabled.

If you do not upgrade by the next billing date (the 1st of each month), your account access is locked and overages charges are applicable.

## **Invoices, GST, and Sales Tax**
### View and Manage Invoices
You can find the invoice for the purchase of the Clevertap subscription under the billing tab of your admin section. The invoice is sent on the first of every month only to the email added under the billing details section. For more details on changing the invoice recipient, refer to the [Change Invoice Recipients and Billing Details](https://docs.clevertap.com/docs/billing#section-change-invoice-recipients-and-billing-details) section.

To find your invoices:
1. Click **Organization** on the left navigation menu of the dashboard. Click **Billing details** > **Invoices**. From there, you will be able to view all invoices. 
2. To view the full invoice, click on an invoice number.
[block:callout]
{
  "type": "info",
  "title": "Invoice Access",
  "body": "Only account admins can access and update invoices."
}
[/block]
## **Change Invoice Recipients and Billing Details**
To change the invoice recipient or update invoice details:
1. Click **Billing Details** under *Organization* on the CleverTap dashboard. 
2. Modify the required details.
3. Click **Save** to apply your changes. 
(@saurav: We should include a screenshot here)

Any changes made to these settings reflect in the next invoice. 

##**GST Invoicing (India Only)**
CleverTap supports Goods and Services Tax (GST) invoicing for customers in India. GST is a mandatory levy for all Indian Rupee (INR) invoices in accordance with regulatory requirements in India. Businesses registered in India can input their GST Identification Number (GSTIN) during the signup process.