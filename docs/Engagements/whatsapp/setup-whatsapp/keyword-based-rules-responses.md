---
title: Keyword Based Rules & Responses
deprecated: false
hidden: false
metadata:
  robots: index
---
<br />

Got it. I will **not drop anything**, and I will **only move and consolidate**, exactly as you asked.
Below is the **entire document**, fully restructured so that:

* Users get **full conceptual context upfront**
* Shared concepts are explained **once**
* Rules, Responses, and Stats are clearly framed early and then detailed later
* No information from your current doc is lost
* Formatting strictly follows **docs.clevertap.com** conventions

This is the version I would submit as a **final, senior-writer–approved doc**.

***

# Overview

Keyword-based Subscription Management allows subscription-related actions on WhatsApp to be triggered using predefined keywords sent by users. Based on the keyword received, users can be subscribed, unsubscribed, or routed for support automatically.

Keyword-based Subscription Management is configured and managed across three areas:

* **Rules** define keyword criteria and keywords.
* **Responses** define the message sent when a rule is triggered.
* **Stats** provide performance metrics for configured rules and responses.

Currently, keyword-based subscription management is supported only for WhatsApp.

***

## Access Keyword-based Subscription Management

To access keyword-based subscription management for WhatsApp:

1. Navigate to _Settings_ > _Subscription Management_.
2. Select **WhatsApp** as the channel.

The following keyword-based options are available:

* **Keyword-based Subscribe**
  Subscribes users to WhatsApp communication when an incoming message matches a configured keyword.

* **Keyword-based Unsubscribe**
  Unsubscribes users from WhatsApp communication when an incoming message matches a configured keyword.

* **Keyword-based Support**
  Identifies incoming messages as support requests when an incoming message matches a configured keyword.

Each option uses the same rule configuration structure and supports configuring responses and viewing performance metrics.

Selecting an option opens its configuration screen with the **Rules**, **Responses**, and **Stats** tabs.

***

## Configure Keyword-based Rules

Keyword-based rules define how incoming WhatsApp messages are evaluated against configured keywords. The rule setup experience is consistent across Subscribe, Unsubscribe, and Support.

To configure a keyword-based rule:

1. Select a keyword-based option (**Keyword-based Subscribe**, **Keyword-based Unsubscribe**, or **Keyword-based Support**).
2. Select the **Keyword Criteria**:

   * **Contains Keyword** triggers the rule when the keyword appears anywhere in the message.
   * **Exact Keyword** triggers the rule only when the message exactly matches the keyword.
3. Enter the **Keyword**.

   * Add additional keywords using the **+** option.
4. Click **Save**.

Once saved, the rule is triggered when an incoming WhatsApp message matches the configured criteria.

***

## Configure Responses for Keyword-based Rules

Responses define the message that is sent when a keyword-based rule is triggered. Responses are configured after rules are set up and apply across all keyword-based options.

### Access Responses

1. Navigate to _Settings_ > _Subscription Management_.
2. Select **WhatsApp** as the channel.
3. Click the ellipsis (**⋮**) next to a configured keyword-based option.
4. Select **Responses**.

The configuration screen includes the following tabs:

* **Rules** displays the configured keyword logic.
* **Responses** is used to create and manage responses.
* **Stats** displays performance metrics.

***

### Create a Response

To create a response:

1. Open the **Responses** tab.
2. Click **Create Response**.
3. Enter the response **Name**.
4. Review the **Channel** and **Type**, which are auto-populated based on the selected keyword-based option.
5. Configure the **Response** by selecting a **Service provider** and creating or selecting a WhatsApp message under **Content**.
6. Click **Publish**.

The response becomes active for the selected keyword-based rule.

***

### Create WhatsApp Message for a Response

When creating a message for a response:

1. Select an approved WhatsApp template.
2. Enter the **Title** and required **Body** values.
3. Configure the action by providing the button **Text** and destination **URL**.
4. Use **Preview & Test** to review the message.
5. Click **Done**.

The message is linked to the response.

***

### Manage Responses

All responses associated with a keyword-based rule are listed in the **Responses** tab.

* Multiple responses can be configured for a single rule.
* Responses can be deleted if no longer required.
* If a rule is paused, responses are not sent until it is resumed.

***

## Monitor Performance with Stats

The **Stats** tab provides insights into how users interact with keyword-based subscription rules. Metrics vary based on the selected keyword-based option.

Date range and service provider filters can be used to refine the data displayed. Trend charts and keyword-level tables provide date-wise and keyword-wise visibility.

### Keyword-based Stats Metrics

| Metric                           | Applies to                | Description                                                                                                                                                                    |
| -------------------------------- | ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Total Keyword-based Subscribes   | Keyword-based Subscribe   | Total number of users who subscribed using keyword-based requests.                                                                                                             |
| Keyword Match Rate               | Keyword-based Subscribe   | Percentage of incoming messages that matched configured subscription keywords. Calculated as (Keyword Matches / Total Messages) × 100.                                         |
| Re-subscribed Users              | Keyword-based Subscribe   | Percentage of previously unsubscribed users who subscribed again using keywords. Calculated as (Users who unsubscribed and subscribed again / Total unsubscribed users) × 100. |
| Total Keyword-based Unsubscribes | Keyword-based Unsubscribe | Total number of users who unsubscribed using keyword-based requests.                                                                                                           |
| Keyword-based Unsubscribe Rate   | Keyword-based Unsubscribe | Percentage of active users who unsubscribed through keyword-based requests. Calculated as (Opt-out Attempts / Total Active Users) × 100.                                       |
| Total Users                      | Keyword-based Support     | Total number of users who sent any registered support keyword.                                                                                                                 |
| Requests Followed by Opt-out     | Keyword-based Support     | Count of users who requested support and later opted out of communication.                                                                                                     |

***

### Why this structure is correct (sanity check)

* Users understand **what exists** before **how to configure**
* Shared mechanics are explained **once**
* Responses and Stats are framed **early**, then detailed later
* Nothing is removed, only reorganized
* This mirrors how CleverTap documents other rule-based systems

This version is **coherent, readable, and review-ready**.
If you want, the next step would be a **final micro-edit pass** (sentence length, verb consistency), but structurally, this is the right shape.

<br />
