---
title: Heap
excerpt: Analytics Platforms
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

[Heap](https://heap.io/) is a product analytics platform that automatically captures every user interaction, clicks, taps, form fills, and more, without requiring manual tracking. It helps teams visualize user journeys, identify drop-offs, and optimize engagement flows.

By integrating Heap with CleverTap, you can forward CleverTap events to Heap for deeper behavioral analysis. This integration allows marketing and product teams to connect CleverTap campaign performance with Heap’s funnel and retention analytics, providing actionable insights into user behavior. For example:

* Funnel Optimization: Track *Add to Cart* and *Purchase* events to identify checkout drop-offs.
* Retention Analysis: Forward post-purchase events to measure long-term engagement and repeat usage.
* Campaign Attribution: Correlate CleverTap campaigns with Heap behavioral data to see which touchpoints drive conversions.

## Use Case: Track Campaign-Driven Purchase Conversions

Consider an example where users who added items to their cart but did not purchase receive a CleverTap push campaign. When they complete a purchase, CleverTap sends a **Purchase event** to Heap. Heap then visualizes this event to show how campaign recipients move through the funnel, from cart to checkout, enabling the team to measure conversion performance and retention trends.

# Prerequisites for Integration

Before starting, ensure you have access to both systems and API permissions.

* A valid CleverTap account with permission to create Webhook campaigns.
* A valid Heap account with [Track API](https://developers.heap.io/reference/track) access.
* Basic knowledge of JSON payloads and event tracking.

# Integrating Heap with CleverTap

The integration process involves the following four major steps:

1. [Locate Heap Project Details](doc:heap#locate-heap-project-details)
2. [Configure a Webhook Campaign](doc:heap#create-a-webhook-in-clevertap)
3. [Create a Webhook in CleverTap](doc:heap#create-a-webhook-campaign)
4. [Verify Data in Heap](doc:heap#verify-data-in-heap)

## Locate Heap Project Details

Before configuring your webhook in CleverTap, collect the necessary information from your Heap account. These details ensure your CleverTap events are sent to the correct Heap project and accepted by the API.

To get your Heap credentials:

1. Log in to your Heap Dashboard at heap.io.
2. From the top-right navigation, select *Projects* > *Your Project Name*.
3. Copy your App ID (you’ll need this when setting up your CleverTap payload).

> 🚧 Important
>
> Verify that your Heap `app_id` matches your project credentials. Mismatched IDs prevent event recording.

4. Review your Track API endpoint—typically:

```
https://heapanalytics.com/api/track
```

> 📘 Note
>
> Some enterprise Heap accounts may use region-specific endpoints (for example, `https://eu.heapanalytics.com/api/track`).

5. Check your authentication method:
   * Heap’s public API does not require API keys for event tracking.
   * However, enterprise plans may use private tokens; verify with your Heap admin if required.

## Create a Webhook in CleverTap

A webhook allows CleverTap to automatically send event data, such as  *Purchase*, to Heap in real time.

To create a webhook:

1. Go to *Settings* > *Channels* > *Webhook* in CleverTap dashboard
2. Click **+ Add Webhook**.

<Image alt="Create webhook" align="center" width="65% " border={true} src="https://files.readme.io/5e58c0eb1ba1070b73e8c10a6f25c72297cb4ae0491cd50a4bb52c81021ed84f-2025-11-10_10-39-40_1.gif">
  Create Webhook
</Image>

3. Enter the following details: Webhook Configuration Details:

| Action          | Value                                                                       |
| --------------- | --------------------------------------------------------------------------- |
| Name            | Name the webhook (for example,`Heap Purchase Tracker`)                      |
| HTTP Method     | Set *HTTP Method* to`POST`                                                  |
| Destination URL | Enter the following *Destination URL*:`https://heapanalytics.com/api/track` |
| Header          | Add key-value pair as `Content-Type: application/json`                      |

4. Click **Save**.

<Image align="center" className="border" width="55% " border={true} src="https://files.readme.io/14b1d3edf33a1a031b925fbb56c095c464824fe70cb03b10bd79e5e5adcf7415-image.png" />

Your webhook now serves as a secure connection between CleverTap and Heap, ensuring events are transmitted accurately. To validate payload structure or authentication methods, refer to [Heap’s Track API](https://developers.heap.io/reference/track).

## Create a Webhook Campaign

Create a CleverTap campaign that triggers the webhook when a user completes a purchase. To do so, perform the following steps:

1. Go to *Campaigns* > **+ Campaign** > *Webhooks*.
2. Set your campaign name (for example, `Post-Purchase Heap Sync`).

<Image alt="Create Webhook Campaign" align="center" width="65% " border={true} src="https://files.readme.io/2413130f036cd48aaabfa67d13bb027f0fbf1daf666b37331fae2efce0b4d844-2025-11-10_11-20-25_1.gif">
  Create Webhook Campaign
</Image>

3. Define your target audience, for example, users who received a *Cart Reminder* push notification.
4. Under the *What* section:

   * *Content Format*: `JSON`
   * *Custom Body*: Enter your event payload. [Example Heap payload](doc:heap#example-heap-payload)

#### Example Heap payload:

```json
{
  "app_id": "<app id>",
  "identity": "{{ Profile.Email | default: 'user@example.com' }}",
  "event": "Purchase",
  "properties": {
      "item_names": "{{ Profile.MyStuff | default: 'Watch' }}",
      "value": "{{ Profile.wallet_balance | default: '100' }}",
      "campaign_name": "Cart Reminder Push"
  }
}
```

Use [Liquid tags](doc:personalize-message-all#liquid-tags) `{{ }}` to personalize event data dynamically based on user profile attributes.

<Image alt="Example Payload" align="center" width="65% " border={true} src="https://files.readme.io/f37e71007be91601f2ede19ed4cf3863680137d2d54e79c8fb5f216a63bf02e8-image.png">
  Example Payload
</Image>

5. Click **Preview and Test** to send a test event to Heap.

<Image alt="Preview and Test" align="center" width="65% " border={true} src="https://files.readme.io/7a552d584fb140008d544e141ccf28a50149de4fb81469eb5b2319315f208d67-image.png">
  Preview and Test
</Image>

6. Verify that Heap receives the data successfully. Refer to [Verify Data in Heap](doc:heap#verify-data-in-heap).
7. Click **Publish** to activate the live campaign.

Each time a user completes a purchase after receiving your campaign, CleverTap automatically forwards the event data to Heap for tracking.

## Verify Data in Heap

After your campaign is live, verify that CleverTap is successfully sending both **event data** and **user data** to Heap. This confirmation ensures your integration is capturing user interactions accurately for analysis.

### Verify Event Data

1. Log in to your **Heap Dashboard**.
2. Go to your project workspace, and click *Data* in the left-hand menu.
3. Search for the event name *Purchase* to confirm that the event is being received by Heap.
4. Click the event name to review details such as:

   * Event count and frequency
   * Associated properties (such as., `item_names`, `value`, `campaign_name`)
   * Timestamp alignment with your CleverTap campaign

   <Image alt="Verify Event Data" align="center" width="75% " border={true} src="https://files.readme.io/eff422878dd54c35124825a8527e5f93a9d0bf9c5a98e59dddc9130c02389e8d-tuja.png">
     Verify Event Data
   </Image>

> 📘 Note
>
> If the event doesn’t appear immediately, refresh the dashboard or adjust the date/time filters.

### Verify User Data

1. Go to your project workspace, and click *User* in the left-hand menu.
2. Click the user’s profile to view event details and confirm that:

   * The user identity (`identity` property, such as email or user ID) matches what was passed from CleverTap

   <Image alt="Verify User Data" align="center" width="75% " border={true} src="https://files.readme.io/85712305b33f4a012b9fb482c9d54bd49c66a3dc2466bc3ed1a1d5435bb55952-aaja.png">
     Verify User Data
   </Image>

Verifying user data ensures that Heap correctly attributes events to the intended profiles, enabling accurate behavioral and cohort analysis.

### Confirm Data Consistency

Finally, cross-check that:

* Event timestamps in Heap align with CleverTap campaign trigger times.
* User-level event properties are correctly mapped (such as, `identity`, `value`, `item_names`).
* No duplicate or missing data entries appear across events.

Both the *Purchase* event and corresponding user data appear in Heap’s timeline with the same metadata passed from CleverTap, confirming that your integration is functioning correctly.

### Analyzing Results in Heap

With *Purchase* events now tracked in Heap, your marketing team can explore insights such as:

* Conversion Rates: Compare users who received a CleverTap campaign vs. those who didn’t.
* Behavioral Paths: Analyze how users move from *Add to Cart* to *Purchase*.
* Retention Cohorts: Measure repeat activity after initial purchase triggered by campaigns.
