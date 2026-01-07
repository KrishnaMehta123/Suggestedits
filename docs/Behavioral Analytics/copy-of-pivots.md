---
title: Pivots 2.0
excerpt: Understand what are Pivots in CleverTap.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

Pivots enables you to explore, compare, and analyze user behavior across multiple dimensions using flexible, interactive tables and visualizations. It helps you break down large volumes of event data into meaningful patterns, allowing you to answer what is happening, where it is happening, and why it is happening.

With Pivotd, you can quickly identify trends, outliers, and correlations across user segments, properties, and time without writing complex queries.

# Key Benefits

Pivots help you answer questions such as:

* Which products, categories, or content types perform best?
* How does user behavior vary across cities, devices, or languages?
* Which user segments generate the highest revenue or engagement?
* At what times or days does a specific action peak or drop?

By slicing and aggregating event data across dimensions, Pivots transform raw events into actionable insights.

# Getting Started

To create a pivot analysis:

1. Navigate to _Analytics > Pivots_
2. Select the **event** you want to analyze
3. Apply **filters and segments** (optional)
4. Choose **properties to pivot on**
5. Select a **measurement** and **visualization**
6. Run the analysis to explore insights

## Select an Event

Start by selecting the event you want to analyze. This event forms the foundation of your pivot analysis.

The selected event determines:

* The dataset being analyzed
* The event properties available for pivoting
* The measurements that can be applied

For example:

* `Product Viewed`
* `Video Watched`
* `Charged`
* `App Launched`

## Apply Segments (Optional)

You can restrict the pivot analysis to a specific user segment or compare behavior across segments.

Segmenting helps you understand how different groups of users behave differently for the same event.

**Example use cases:**

* Compare engagement between **New Users** and **Returning Users**
* Analyze purchases by **High-Value Users**
* Understand content consumption for **Subscribed vs Free users**

## Choose Properties to Pivot On

Pivots allow you to analyze events across multiple dimensions. You can pivot on:

* **Event properties** (for example, product name, content category)
* **User profile properties** (for example, language, customer type)
* **Geographic properties** (for example, city, country)
* **Technographic properties** (for example, device type, OS)
* **App fields** (for example, app version)

These properties can be used as:

* **Rows**
* **Columns**
* **Axes** in visualizations

You can mix and match properties to explore different analytical angles.

## Select Measurement

The measurement defines **what you want to quantify** for the selected event.

Pivots 2.0 supports two primary measurement types:

### Event Count

Counts how many times the selected event occurred.

**Use this when you want to:**

* Measure frequency or volume
* Compare activity levels across dimensions

**Example:**
Number of `Product Viewed` events per category per day

### Sum of Property

Aggregates the total value of a numeric event property.

This is useful when the event represents a value-bearing action.

**Example use cases:**

* Total revenue using the `amount` property of the `Charged` event
* Total watch time using `video_duration` for `Video Watched`

## Understanding the Pivot Analysis

A pivot analysis consists of the following components:

### Available Properties

The pool of properties you selected during setup. You can dynamically assign these properties as rows, columns, or chart axes to explore different views of the same data.

### Rows and Columns

Rows and columns define how data is grouped in tabular views.

For example:

* Rows: Day of Week
* Columns: Product Category

This structure allows you to compare values across dimensions at a glance.

### Visualizations

Pivots 2.0 supports multiple visualization types to help you interpret data effectively.

You can switch between views without changing the underlying query.

## Supported Visualizations and When to Use Them

### Table

Best for getting a precise, detailed overview of the data.

Use tables when you want exact values or need to export results.

### Heatmaps

Heatmaps highlight intensity using color, making it easy to spot patterns.

#### Table Heatmap

Best for identifying highest contributors in the dataset.

**Insight example:**
Which product-category and day combinations generate the most revenue?

#### Column-wise Heatmap

Best for identifying outliers within each column.

**Insight example:**
Which product performs best on each day of the week?

#### Row-wise Heatmap

Best for identifying outliers within each row.

**Insight example:**
Which day performs best for each content title?

### Bar Chart

Best for comparing categorical data.

**Use this to:**
Compare performance across categories such as products, regions, or languages.

### Stacked Bar Chart

Best for comparing how multiple variables contribute to a total over time or across categories.

**Use this to:**
Understand composition changes across dimensions.

### Line Chart

Best for analyzing trends over time.

**Use this to:**
Identify correlations or similar behavioral patterns between variables.

### Area Chart

Best for understanding part-to-whole relationships over time.

**Use this to:**
Analyze contribution of individual categories to overall performance.

## Example Use Case: Content Consumption Analysis

A video streaming app wants to analyze content performance beyond just views.

**Setup:**

* Event: `Video Watched`
* Measurement: Sum of `video_duration`
* Rows: Day of Week
* Columns: Video Name

**Insights derived:**

* Identify which shows drive the most watch time
* Understand viewing patterns across weekdays
* Optimize content promotion and scheduling

## Data Sampling

To ensure fast query performance, CleverTap applies intelligent sampling when analyzing very large datasets.

* Sampling is applied when queries exceed **100,000 events**
* Sample rate beyond this threshold is **10%**
* Results remain **directionally accurate**

Minor differences may appear when comparing pivot data with unsampled dashboards.

## When to Use Pivots vs Funnels

| Use Case                           | Use Pivots | Use Funnels |
| ---------------------------------- | ---------- | ----------- |
| Explore trends and distributions   | ✅          |             |
| Compare dimensions and segments    | ✅          |             |
| Analyze step-by-step user journeys |            | ✅           |
| Identify drop-offs between steps   |            | ✅           |

***

## Summary

Pivots 2.0 empowers you to:

* Slice user behavior across multiple dimensions
* Visualize complex datasets with clarity
* Identify trends, patterns, and anomalies
* Make informed, data-driven decisions quickly

By combining flexibility, performance, and powerful visualizations, Pivots 2.0 makes exploratory analytics accessible to every marketer.

***

If you want, next I can:

* Create **migration notes** from old Pivots → Pivots 2.0
* Write **inline UI tooltips** for Pivots
* Add **FAQs or troubleshooting**
* Tighten this for **ReadMe-style publishing**
