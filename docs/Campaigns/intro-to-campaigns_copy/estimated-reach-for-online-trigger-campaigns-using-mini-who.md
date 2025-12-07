---
title: Estimated Reach for Online Trigger Campaigns
excerpt: >-
  Learn how to estimate audience reach for online trigger campaigns using Mini
  WHO filters based on event summary data, enabling smarter targeting and
  campaign planning.
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

Estimate Reach helps you preview how many users meet your targeting criteria in an online trigger campaign, before you publish it. This is especially helpful when you are using Mini WHO filters such as behavioral conditions (for example, users who did/did not do an action) and user properties (for example, app version, platform, location).

You see an estimated user count alongside a breakdown by platform and device. This visibility ensures your campaign reaches the expected scale and helps you adjust filters before finalizing.

Estimate Reach helps you to do the following:

* Validate your targeting logic
* Anticipate campaign scale
* Avoid under- or over-targeting

Use this tool to fine-tune segmentation before activating your campaign.

## Visibility of the Estimate Reach Panel

You can view the *Estimated Reach* panel in the *Who* section when:

* You are creating an **online trigger campaign**
* You are defining a **trigger event** (for example, App Launched)
* You are enabling **Filter on past behavior and user properties**
* You are adding at least one behavior or user property filter

Once these conditions are met, the **Calculate** button becomes available in the side panel. Clicking it displays your estimated user count.

## Supported Filter Types

| Filter Type | Description                                                          | Example                                              |
| ----------- | -------------------------------------------------------------------- | ---------------------------------------------------- |
| First Time  | Users who performed an event for the first time within a time window | “App Launched” for the first time in the last 7 days |
| Last Time   | Users who performed an event for the last time within a time window  | “Charged” for the last time more than 30 days ago    |
| Occurrences | Users who performed an event a specific number of times              | “Added to Cart” more than 3 times                    |
| Did Not Do  | Users who have not performed a given event (occurrence \< 1)         | “Did not purchase”                                   |

These filters use event summary data, precomputed insights per user making queries faster and more scalable than scanning raw event logs.

# Estimate Reach in Mini Who

To estimate the reach for online trigger campaigns, follow the steps below:

1. [Create a Trigger Campaign](doc:https://staging.docs.user.clevedoc:estimated-reach-for-online-trigger-campaigns-using-mini-who#create-a-trigger-campaign)
2. [Define the Trigger Event](doc:https://staging.docs.user.cdoc:estimated-reach-for-online-trigger-campaigns-using-mini-who#define-the-trigger-event)
3. [Enable and Configure Mini WHO Filters](doc:estimated-reach-for-online-trigger-campaigns-using-mini-who)
4. [Select Delivery Platforms and Devices](doc:https://staging.docs.user.doc:estimated-reach-for-online-trigger-campaigns-using-mini-who#select-delivery-platforms-and-devices)
5. [Calculate Estimated Reach](doc:estimated-reach-for-online-trigger-campaigns-using-mini-who#calculate-estimated-reach)

## Create a Trigger Campaign

Start a new trigger campaign from the Campaigns dashboard and select the trigger-based campaign type.

## Define the Trigger Event

In the *Target Segment* section, do the following:

1. Set the real-time event that triggers the message (for example, “App Launched”)
2. Optionally, apply filters to this event (for example, app version = latest)

## Enable and Configure Mini WHO Filters

Turn on the checkbox labeled **Filter on past behavior and user properties**.

Then add filters across the following categories:

* **Have done**\
  For example: Users who have added an item to cart more than twice  
* **Have not done**\
  For example: Users who have not visited a pricing page  
* **With user properties**\
  For example: Users whose location is “India” or platform is “iOS”

You can add multiple filters in each section and combine them using AND logic.

## Select Delivery Platforms and Devices

In the *Deliver to* section, do the following:

1. Choose the platform: Android, iOS, or both
2. Choose the device types: Mobile, Tablet, or TV

Your selection affects the reach estimate, which only includes users matching the delivery filters.

## Calculate Estimated Reach

Click **Calculate** in the side panel to get an estimate of the audience.

You can view the following:

* **Total Users**: Number of users matching your conditions and delivery filters
* **Breakdown by Platform**: Android vs iOS user counts
* **Visual Indicator**: A doughnut chart summarizing the share by OS

The estimate refreshes based on the latest filters and event data available at the time of calculation.

<Image alt="Calculate Estimate Reach" align="center" border={true} src="https://files.readme.io/c9e4e54785c7b6278061b4ea84da74b08d2e88e98b46ff0bd63bf2c3eb833d83-2025-07-29_12-49-09_1.gif">
  Calculate Estimate Reach
</Image>

The estimate includes the following:

* Users who qualify for the segment based on your trigger event and filters
* Users who can be messaged based on platform and device settings
* Only those currently eligible for delivery (for example, not uninstalled or unsubscribed)

The count reflects the **event summary** data available in the system, not a live or real-time lookup.

## Use Cases

You want to target users who:

* Launch the app (real-time trigger event)
* Have **not** visited a *Pricing*  page in the last 7 days
* Belong to the *Returning Users* cohort
* Use Android devices only

As you set these conditions in the **Who** section:

* The Estimated Reach panel shows the total Android users matching the above filters
* You can toggle to see the count by devices (e.g., Mobile, Tablet)
* If the count is too low or high, you can adjust filters accordingly

This helps ensure your campaign reaches the right audience before it goes live.

Estimate Reach is not available in the following scenarios:

* If you do not enable behavioral or property filters, the estimate is not available
* If your filters result in zero eligible users, the panel shows a zero count

# FAQs

### What type of filters are supported?

Estimate Reach supports Mini WHO filters based on the following:

* Event frequency (First Time, Last Time, Occurrences)
* Inactivity (Did Not Do)

User properties (for example, platform, app version, location)

These filters rely on event summary data to provide fast estimates.

### Is Estimate Reach available for all campaign types?

No. Estimate Reach is only available for online trigger campaigns that use Mini WHO filters. It is not available for one-time, recurring, or journey-based campaigns.

### Why am I not seeing the Estimate Reach panel?

The following are the possible reasons for the Estimate Reach panel being invisible:

* You are not in an online trigger campaign
* You have not enabled the Filter on past behavior and user properties checkbox'
* You have not added any behavioral or property filters
* Your filters return zero matching users

### Is the estimate based on live user data?

No. The estimate is based on event summary data, which aggregates user behavior. It’s not a real-time lookup but is accurate as per the latest available summary data.

### Can I estimate reach for users who qualify but cannot be messaged (e.g., uninstalled users)?

No. The estimate only includes users who are currently eligible for delivery, excluding those who are uninstalled, unsubscribed, or otherwise unreachable.

### Does changing the delivery platform affect the estimate?

Yes. The platform (Android, iOS) and device type (Mobile, Tablet, TV) filters directly affect the reach count. Only users who match your delivery settings are included in the estimate.

### Can I see a breakdown of the estimated reach?

Yes. Once calculated, you can view the following:

* Total users who match your filters
* Platform-wise breakdown (Android vs iOS)
* A doughnut chart summarizing the share

### What should I do if the estimated reach is too low or too high?

Use the insights to adjust your filters. You can do the following:

* Broaden or narrow event criteria
* Modify user property conditions
* Adjust platform or device filters

This lets you fine-tune the campaign before launch.
