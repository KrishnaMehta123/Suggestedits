---
title: Billing-copy
excerpt: >-
  The CleverTap for Startups helps early to mid-stage startups looking for an
  all-in-one engagement platform to grow their business.
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

This document provides information about billing terminologies and calculations for CleverTap Essentials users. The billing is based on the Monthly Billable Users, derived from Monthly Active Users and the Data Points as explained in the following sections. 

> 📘 Annual Plan
>
> The **CleverTap Essentials** plan also offers an annual plan option. To check if you are eligible, navigate to *Organization*> *My Plan* section.

# **Billing Terminologies**

## **Monthly Active User (MAU)**

An MAU is an end-user who has recorded one or more events in a calendar month. When tracking mobile apps and websites, a user active on both devices with the same identity token will be counted as one MAU.\
An organization is charged based on the total number of MAUs across all projects, which means that if a user performs a qualifying event in multiple projects, they are counted once per project.

### System Event Included in MAU Calculation

The following list displays the [System](https://docs.clevertap.com/docs/events?utm_source=C4S\&utm_medium=doc\&utm_id=KB#system-events) events considered in the MAU calculation for the different CleverTap for Essentials:

1. App Launched
2. UTM Visited 
3. Web Session Started

> 📘 Manage UTM Visited and Web Session Started
>
> You can disable UTM Visited and Web Session Started. For more information, refer to [Configure System Events](https://docs.clevertap.com/docs/schema?utm_source=C4S\&utm_medium=doc\&utm_id=KB#configure-system-events).

## **Data Point**

An event, event property, or profile property update is a data point, a usage measure associated with MAU. A total of 10,000 data points are allowed per MAU.

> 📘 Profile Property Update
>
> If the user updates more than one profile property at one time, it is counted as one data point.

The Partner Sync system event and its properties are included in the Data Point calculation. For more information, refer to [System Event](https://docs.clevertap.com/docs/events?utm_source=C4S\&utm_medium=doc\&utm_id=KB#system-events).

## **Monthly Billable User (MBU)**

MBU reflects the highest value amongst Selected MAU Tier, MAU Actual Usage, or Processed MAU.\
Processed MAU is calculated as the total data points used divided by allowed data points per MAU (10,000 data points). In most cases, users perform fewer than 10,000 data points per month.

**Where do I check my MBU?**\
To check your MBUs, the account administrators need to navigate to  *Organization* > *Billing* > *My Plan* from your dashboard. It displays the estimated MBUs for the current month for all your organization's projects. 

## **Data Upload Charges**

If data is uploaded to amend a user profile or user activity history, the number of data points uploaded counts toward the total number of data points allocated for the month. The number of data points allocated for each calendar month equals the MAU tier in your pricing agreement times 10,000.

## **Data Retention Policy**

The default data retention policy for the CleverTap Essential plan is three years, which cannot be changed.

## **Overages**

Overages are over usage charges which will be added as a billable amount if you exceed your plan limits. You can always upgrade to a plan of higher MAU to avoid paying overages. For more details on overage calculation, refer to this [section](https://staging.docs.user.clevertap.net/docs/payments-and-overagescopy?utm_source=C4S\&utm_medium=doc\&utm_id=KB).

To access details on commonly encountered problems, refer to the [FAQ section](https://staging.docs.user.clevertap.net/docs/faqs-on-billing-and-overagescopy?utm_source=C4S\&utm_medium=doc\&utm_id=KB).
