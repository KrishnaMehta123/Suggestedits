---
title: Funnels Beta
excerpt: >-
  Learn how to use the new and improved visualization using Funnels to gain
  deeper insights into your data and make more informed decisions.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
# Overview

Funnels show users' progress through defined paths in your app and pinpoint where they drop off between steps. Funnels are a series of events that a user performs in a particular order.

A typical example is a user onboarding flow, where a user progresses from the app's initial launch through activities such as registration, profile completion, and orientation. Another example is a purchase flow, where a user progresses through a shopping cart experience to complete a purchase.

<Callout icon="📘" theme="info">
  #### Public Beta

  This feature is released in Public Beta. For more information about this feature or any queries, contact your Success Manager or the [CleverTap Support](https://help.clevertap.com/hc/en-us/requests/new).
</Callout>

# Creating a Funnel

To create a funnel, go to _Analytics_ > _Funnels Beta_ and perform the following steps:

* [Select Events](doc:funnels-v2#select-events)
* [Select Segments](doc:funnels-v2#select-segments)
* [Split by Property](doc:funnels-v2#split-by-property)
* [Select Measured by Options](doc:funnels-v2#select-measured-by-options)

## Select Events

Select the events in the desired order to create up to an eight-step funnel. You can also select event properties for each event to constrain the analysis for the users who performed that event/property combination.

<Image align="center" border={true} caption="Select Funnel Events" src="https://files.readme.io/698381e8f564ec79290e3f589d750385dd98ee602cf9aa6c8a883c7778728895-image.png" />

You can also add multiple events (up to four) with an OR condition by clicking the ellipsis menu. For example, you can add Mobile Login and Website Login as two events with OR logic in a step of the Funnel.

<Image align="center" border={true} caption="Add Multiple Events with an OR Condition" src="https://files.readme.io/43b1604c14a3fd8b3cee34c3b5563dec6f22a49b165b065382c7db87e94de83c-image.png" />

## Select Segments

You can compare funnel conversions across different user segments to analyze how behavior varies between user groups. For example, compare the funnel for _App Launched_ > _Product Viewed_ > _Charged_ across the _All Users_ and the _Engaged Users_ segments. The differences in conversion trends could reveal variations in your users' behavior across each segment and result in invaluable insights.

<Image align="center" border={true} caption="Segment Comparison Results" src="https://files.readme.io/94ae0749e8e0b36aa53ec6e7860b0625b1b3e6111fae76b3d5215e978f4e8634-image.png" />

## Split by Property

You can split a funnel by profile properties for sessions, geographies, and technographics, or by an event property associated with any event. This lets you compare your conversion flows across product categories, geographies, devices, and more.

<Image align="center" border={true} caption="Split Funnel by Event Property" src="https://files.readme.io/db0c4c73ebfd5874869ae362b54bde3ea5cb834b4e87dae943fc51f8756b3bcd-image.png" />

<Image align="center" border={true} caption="Split Funnel by User Property" src="https://files.readme.io/959e4ab3fcef7f905082f8930ddbd5746f506e1e76fe3f02c2cc59492a105cab-image.png" />

## Select Measured By Options

The _MEASURED BY_ section controls how funnel conversions are calculated, grouped, and evaluated. These settings directly impact how users are counted and how funnel results are displayed.

From the _MEASURED BY_ section, you can query:

* [Measurement Mode](doc:funnels-v2#measurement-mode)
* [Conversion Window](doc:funnels-v2#conversion-window)
* [Step Order](doc:funnels-v2#step-order)

## Measurement Mode

The measurement mode determines whether funnel performance is displayed as a single aggregated value or as a trend over time.

You can choose one of the following measurement modes:

* [Total Conversion](doc:funnels-v2#total-conversion)
* [Trends](doc:funnels-v2#trends)

### Total Conversion

Selecting **Total Conversion** allows you to view the aggregate conversion count or conversion rate for the selected time range. Results are shown as a single value and are not broken down by time.

<Image align="center" border={true} caption="Measured By Total Conversion" src="https://files.readme.io/bb8d24cbf8632ce064c529da93367986bb336bc6c72260c1b96edbc0716de140-image.png" />

Use the Total Conversion option when you want to:

* Get a high-level summary of funnel performance
* Compare overall conversion rates across segments
* Report a single conversion metric for a given period

For example, compare the total conversion rate of _All Users_ versus _Engaged Users_ for a checkout funnel.

### Trends

Selecting **Trends** allows you to analyze how funnel conversions change over time. When **Trends** is selected, you must also choose a time granularity, i.e., Day, Week, or Month, to view the trend.

<Image align="center" border={true} caption="Measured By Trends" src="https://files.readme.io/fdac5620cbf09d1ee9a53999b384fd1785d0826c2159c92dc4f7e2e27f91ff8b-image.png" />

Use the Trends option when you want to:

* Track conversion performance over time
* Identify spikes, drops, or seasonality in funnel conversions
* Compare trends across segments or properties

For example, analyze daily conversion trends for the funnel _App Installed → App Launched → Added to Cart_ over the last 30 days.

## Conversion Window

Funnels are calculated based on a specified conversion window (set to five days by default). The conversion window is the total elapsed time for the user to complete all the steps in the funnel (that is, to convert). Shorter duration windows generally result in fewer users completing the funnel steps, whereas longer windows result in more user conversions.

<Image align="center" border={true} caption="Set Conversion Window" src="https://files.readme.io/97a73f12ec359477da234ef50ad379553f6bf28f38c59a1e6f165e2c9908aa9b-image.png" />

<Callout icon="📘" theme="info">
  #### Time Interval for Conversion Window

  CleverTap recommends setting the _Conversion Window_ to a duration shorter than the _Actual Date Range_ to avoid data variance.
</Callout>

## Step Order

The _Step Order_ setting determines how strictly users must follow the defined sequence of funnel steps to be counted as converted. These orders determine how users are counted as they progress through funnel steps, primarily when steps are repeated or performed out of sequence.

<Image align="center" border={true} caption="Funnel Step Order" src="https://files.readme.io/0a03b55656f6066ebb8ff9e59b3fe3344e6526a45ad37a317c64bff3fef5fcd2-image.png" />

You can choose one of the following options:

* [Flexible Order](doc:funnels-v2#flexible-order)
* [Strict Order](doc:funnels-v2#strict-order)

### Flexible Order

By default, funnels count users who complete all defined steps in the specified sequence. Users may repeat earlier steps, but they must still complete every funnel step to be counted as converted. If a user completes a later step before a required earlier step, the funnel does not count that user as converted.

For example, if a funnel's steps are defined as:

**Step A → Step B → Step C → Step D**

The following table explains how different users are counted based on their progress through the funnel steps:

| User   | Step Sequence                              | Counted in Funnel? | Reason                                                                |
| ------ | ------------------------------------------ | ------------------ | --------------------------------------------------------------------- |
| User 1 | Step A → Step B → Step C → Step D          | Yes                | Completes all funnel steps in the correct order.                      |
| User 2 | Step A → Step C → Step D                   | No                 | Skips Step B, which is required in the funnel.                        |
| User 3 | Step A → Step C → Step B → Step D          | No                 | Performs funnel steps out of sequence.                                |
| User 4 | Step A → Step B → Step A → Step C → Step D | Yes                | Repeats Step A but still completes all steps in the correct sequence. |

#### Why Use Flexible Order?

Flexible ordering is useful when you want to measure overall funnel completion without penalizing users for repeated or exploratory behavior.

In many user journeys, users may repeat steps, go back and forth between screens, or perform actions multiple times before moving forward. Flexible Order ensures that these natural behaviors do not prevent users from being counted as converted, as long as they eventually complete all required steps in the correct sequence.

For example, consider the following Conversion flow of two users in an app:

**User A**: App Launched → Viewed Product → Viewed Product → Added to Cart → Viewed Product → Purchased

**User B**: App Launched → Viewed Product → Added to Cart → Purchased

With Flexible Order enabled, both users are counted as converted because they complete all funnel steps in the defined order, even though User A repeats some steps.

### Strict Order

When _Strict Order_ is selected, funnels count users only if they complete every step exactly in the defined sequence. Any repetition of a funnel step or deviation from the specified order disqualifies the user from being counted as converted.

For example, if a funnel's steps are defined as:

**Step A → Step B → Step C → Step D**

The following table explains how different users are counted based on how they progress through the funnel steps:

| User   | Step Sequence                              | Counted in Funnel? | Reason                                                     |
| ------ | ------------------------------------------ | ------------------ | ---------------------------------------------------------- |
| User 1 | Step A → Step B → Step C → Step D          | Yes                | Completes all funnel steps exactly in the specified order. |
| User 2 | Step A → Step C → Step D                   | No                 | Skips Step B, breaking the required step sequence.         |
| User 3 | Step A → Step C → Step B → Step D          | No                 | Performs funnel steps out of order.                        |
| User 4 | Step A → Step B → Step A → Step C → Step D | No                 | Repeats Step A, which violates strict ordering rules.      |

#### Why Use Strict Order?

Strict ordering is useful when you want to identify friction or unexpected behavior within a process.

For example, consider the following Login Flow of two users in an app:

* **User A:** App Launched → Login Attempted → Login Attempted → Login Attempted → Logged In
* **User B:** App Launched → Login Attempted → Logged In

With strict order enabled, User A would not be counted as a clean conversion, highlighting repeated login attempts and potential user friction. This makes strict order particularly valuable for diagnosing issues in critical flows such as authentication, onboarding, or payments.

# Reading Funnel Analysis

CleverTap provides multiple views to help you interpret funnel performance effectively. Depending on whether you want a visual overview or a detailed comparison, you can analyze funnel data using [Chart View](doc:funnels-v2#chart-view) or [Table View.](doc:funnels-v2#chart-view) Each view highlights different aspects of user progression and conversion behavior.

## Chart View

Chart View provides a visual representation of how users progress through each step of the funnel, making it easy to identify drop-offs and overall conversion trends at a glance.

The default chart shows cumulative conversions per step for the selected time range. You can view the data either as an absolute count of users completing each step or as a percentage.

<Image align="center" border={true} caption="Chart View of Funnel Analysis" src="https://files.readme.io/25abe447ff6abb54742459f0155ec8215a73ac47fa07a1e2bf3d1bcc076eaf5f-image.png" />

## Table View

Table View presents the same funnel data in a structured, tabular format, making it easier to compare conversions across segments or property-based splits.

Each row in the table represents a funnel categorization, such as a user or event property used to split the funnel. You can sort the table by any column to quickly identify patterns or outliers.

The table includes the following metrics for each row:

* Overall conversion percentage from the first step to the last step
* Conversion number and percentage between consecutive steps

In the example shown below, sorting the table reveals that English speakers have the highest overall conversion rate.

<Image align="center" border={true} caption="Table View of Funnel Analysis" src="https://files.readme.io/9aeb7ed709958f6ef3ce3ffa1cb23d594a84466a827bd6ae1586f7752da823d5-image.png" />

# Bookmark a Funnel Analysis

You can bookmark any Funnel analysis to quickly revisit it later. Bookmarks are user-specific; only the logged-in user can view their saved bookmarks on the CleverTap dashboard.

Bookmarks are especially useful for tracking frequently accessed conversion journeys. For example, if you regularly monitor funnel steps such as _App Launched_ > _Product Viewed_ >  _Charged_, bookmarking it lets you instantly return to the same setup without recreating the funnel each time.

To bookmark a Funnel:

1. Click **Bookmark** in the top-right corner of the dashboard after generating the Funnel analysis.
2. Enter a descriptive name to help you easily identify the analysis later.
3. Click **Bookmark**.

<Image align="center" border={true} caption="Bookmark a Funnel Analysis" src="https://files.readme.io/0a95c2524453a5d5e5b88f4d133534cefadfa02b54ced32746f4b63b34aa6eb7-2026-01-02_15-18-05_1.gif" />

You can add up to 50 bookmarks.

<Callout icon="📘" theme="info">
  #### Note

  Funnels are accessible only to the user who created them. You can access all your saved bookmarks from the bookmark list under the _Funnels_ section.
</Callout>
