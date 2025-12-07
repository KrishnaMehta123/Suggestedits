---
title: App Functions Deprecate
excerpt: ''
deprecated: true
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

CleverTap's App Functions allow you to trigger native OS-level prompts, such as requesting app ratings, push notification permissions, or opening URLs. These functions can be embedded in in-app campaigns or triggered as standalone system prompts to engage users contextually and effectively.

***

## Available App Functions

Below is a list of supported App Functions, their descriptions, use cases, and important platform considerations.

### 1. **Request App Rating**

* **Description**: Triggers the OS-native app store rating prompt.
* **Use Case**: Ask for ratings after high-satisfaction moments (e.g., feature success, subscription renewal).
* **System Behavior**:

  * OS controls when and how often the prompt appears (may not show every time).
  * Cannot be forced or tracked.
  * No outcome data (rating result) is available.
* **Best Practice**: Precede with a message explaining the value of the rating to improve chances of success.

### 2. **Request Push Permission**

* **Description**: Prompts the user to grant push notification permissions.
* **Use Case**: Ask after explaining value—e.g., after onboarding, feature walkthroughs.
* **System Behavior**:

  * Shown only if permission hasn’t already been granted or denied.
  * Redirects to app settings if previously denied.
  * One-time prompt by OS; cannot be re-shown.

### 3. **Open URL**

* **Description**: Opens an external web page or deep-linked screen in the app.
* **Use Case**: Link to external offers, help pages, account settings, etc.
* **System Behavior**:

  * URL opens immediately on tap.
  * Campaign-level analytics track only the in-app click/view, not destination behavior.
* **Best Practice**: Ensure the URL is mobile-optimized and secure (HTTPS).

***

## How to Use App Functions

App Functions can be added to your in-app campaign in two ways:

### Option 1: As Button Action in In-App Campaign

You can attach an App Function to a button in an in-app message using the Advanced In-App Builder:

**Steps:**

1. Create an in-app campaign.
2. Go to **What > Advanced In-App Builder**.
3. Add a button element to the layout.
4. In the **On Tap** dropdown, select `App Function`.
5. Choose one of the available functions: `Request App Rating`, `Request Push Permission`, or `Open URL`.

<Callout icon="💡" theme="default">
  ### Always add a lead-in message to set context before invoking the system prompt.
</Callout>

### Option 2: As Standalone App Function Campaign

You can use App Functions as stand-alone system prompt campaigns with no visual UI.

**Steps:**

1. Create an in-app campaign.
2. In the **What** section, select the `App Functions` tab.
3. Select a function from the list.
4. Define campaign targeting and scheduling as usual.

**Note:** These campaigns do not display a UI. They directly invoke the system function.

***

## Event Tracking Matrix

| App Function            | Used As       | Notification Viewed | Notification Clicked | Tracks Other Events? | Notes                                              |
| ----------------------- | ------------- | ------------------- | -------------------- | -------------------- | -------------------------------------------------- |
| Request App Rating      | Button Action | Yes                 | Yes                  | No                   | OS controls dialog visibility; no feedback tracked |
|                         | Standalone    | No                  | No                   | No                   | No campaign interaction tracking possible          |
| Request Push Permission | Button Action | Yes                 | Yes                  | No                   | Tracks in-app only; not OS prompt result           |
|                         | Standalone    | Yes                 | No                   | No                   | Can track prompt view only                         |
| Open URL                | Button Action | Yes                 | Yes                  | No                   | Tracks click on CTA, not the URL open itself       |
|                         | Standalone    | Yes                 | No                   | No                   | Tracks campaign view only                          |

***

# Push Primer In-App Campaigns

Push primer campaigns are used to warm up the user before showing the irreversible native push permission prompt. They serve as a reversible pre-permission layer.

### 📋 Steps to Create:

1. Create an in-app campaign.
2. Use the Advanced In-App Builder.
3. Add a message explaining the value of enabling push (e.g., "Stay updated with order alerts and offers!").
4. Add a **button** and set its `On Tap` action to **App Function > Request Push Permission**.
5. Style and preview your campaign.
6. Launch the campaign.

> 📘 Best Practice
>
> Use compelling visuals and clear reasons why the user should opt in.

***

# App Rating Primer In-App Campaigns

Rating primer campaigns aim to guide users to leave a review during moments of satisfaction.

### 📋 Steps to Create:

1. Create an in-app campaign.
2. Use the Advanced In-App Builder.
3. Add contextual messaging like: "Enjoying the app? Let us know!"
4. Add a **button** and set its `On Tap` action to **App Function > Request App Rating**.
5. Preview and test the campaign.
6. Launch the campaign to a satisfied segment.

> 📘 Tip
>
> Ideal after a purchase, milestone, or subscription renewal.
