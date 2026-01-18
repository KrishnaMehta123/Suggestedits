---
title: Keyword Based Rules & Responses
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

Keyword-based Subscription Management allows you to manage user subscription preferences on WhatsApp using predefined keywords sent by users. Based on the keywords received, users can be subscribed, unsubscribed, or routed for support without manual intervention.

Currently, keyword-based subscription management is supported only for WhatsApp.

## Access Keyword-based Subscription Management

To access keyword-based subscription management for WhatsApp:

1. Navigate to _Settings_ > _Subscription Management_.
2. Select **WhatsApp** as the channel.

The following options are available:

* **Keyword-based Subscribe**
* **Keyword-based Unsubscribe**
* **Keyword-based Support**

Selecting an option opens the corresponding setup screen.

## Keyword-based Subscribe

Keyword-based Subscribe allows users to opt in to WhatsApp communication by sending predefined keywords.

To configure keyword-based subscribe:

1. Select **Keyword-based Subscribe**.
2. Select the **Opt-in Criteria**:

   * **Contains Keyword** subscribes users when the keyword appears anywhere in the message.
   * **Exact Keyword** subscribes users only when the message exactly matches the keyword.
3. Enter the **Keyword**, add additional keywords if required, and click **Save**.

Once saved, CleverTap automatically subscribes users to WhatsApp communication when incoming messages match the configured criteria.

## Keyword-based Unsubscribe

Keyword-based Unsubscribe allows users to opt out of WhatsApp communication by sending predefined keywords.

To configure keyword-based unsubscribe:

1. Select **Keyword-based Unsubscribe**.
2. Select the **Opt-out Criteria**:

   * **Contains Keyword** unsubscribes users when the keyword appears anywhere in the message.
   * **Exact Keyword** unsubscribes users only when the message exactly matches the keyword.
3. Enter the **Keyword**, add additional keywords if required, and click **Save**.

Once saved, CleverTap automatically unsubscribes users from WhatsApp communication when incoming messages match the configured criteria.

## Keyword-based Support

Keyword-based Support allows users to request help on WhatsApp by sending predefined support keywords.

To configure keyword-based support:

1. Select **Keyword-based Support**.

2. Select the **Keyword Criteria**:

   * **Contains** triggers support when the keyword appears anywhere in the incoming message.
   * **Exact Keyword** triggers support only when the incoming message exactly matches the keyword.

3. Enter the **Keyword**.

   * You can add multiple support keywords using the **+** option.

4. Click **Save**.

Once saved, CleverTap detects incoming WhatsApp messages that match the configured criteria and routes them as support requests.

## Configure Responses for Keyword-based Rules

Responses define the message that is sent when a keyword-based rule is triggered.

### Access Responses

1. Navigate to _Settings_ > _Subscription Management_.
2. Select **WhatsApp** as the channel.
3. Click the ellipsis (**⋮**) next to a configured keyword-based option.
4. Select **Responses**.

The configuration screen includes the following tabs:

* **Rules** shows the keyword configuration.
* **Responses** is used to create and manage responses.
* **Stats** displays performance metrics.

## Create a Response

Responses define the message that is sent when a keyword-based rule is triggered.

To create a response:

1. Open the **Responses** tab.
2. Click **Create Response**.
3. Enter the response **Name**.
4. Review the **Channel** and **Type**, which are auto-populated based on the selected keyword-based option.
5. Configure the **Response** by selecting a **Service provider** and creating or selecting a WhatsApp message under **Content**.
6. Click **Publish**.

The response is published and becomes active for the selected keyword-based rule.

## Create WhatsApp Message for a Response

When creating a message for a response:

1. Select an approved WhatsApp template.
2. Configure the message content by entering the **Title** and required **Body** values.
3. Configure the action by providing the button **Text** and destination **URL**.
4. Use **Preview & Test** to review the message.
5. Click **Done**.

The message is linked to the response.

## Manage Responses and View Stats

All responses associated with a keyword-based rule are listed in the **Responses** tab.

* Responses can be viewed or deleted as required.
* Multiple responses can be configured for a single rule.
* If a rule is paused, responses are not sent until it is resumed.

The **Stats** tab provides performance metrics for the configured responses.

## Stats

The **Stats** tab provides insights into how users interact with keyword-based subscription rules. Metrics vary based on the selected keyword-based option.

Date range and service provider filters can be used to refine the data displayed.

### Keyword-based Stats Metrics

| Metric                               | Applies to                | Description                                                                                                                                                                    |
| ------------------------------------ | ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Total Keyword-based Unsubscribes** | Keyword-based Unsubscribe | Total number of users who unsubscribed using keyword-based requests.                                                                                                           |
| **Keyword-based Unsubscribe Rate**   | Keyword-based Unsubscribe | Percentage of active users who unsubscribed through keyword-based requests. Calculated as (Opt-out Attempts / Total Active Users) × 100.                                       |
| **Total Keyword-based Subscribes**   | Keyword-based Subscribe   | Total number of users who subscribed using keyword-based requests.                                                                                                             |
| **Keyword Match Rate**               | Keyword-based Subscribe   | Percentage of incoming messages that matched configured subscription keywords. Calculated as (Keyword Matches / Total Messages) × 100.                                         |
| **Re-subscribed Users**              | Keyword-based Subscribe   | Percentage of previously unsubscribed users who subscribed again using keywords. Calculated as (Users who unsubscribed and subscribed again / Total unsubscribed users) × 100. |
| **Total Users**                      | Keyword-based Support     | Total number of users who sent any registered support keyword.                                                                                                                 |
| **Requests Followed by Opt-out**     | Keyword-based Support     | Count of users who requested support and later opted out of communication.                                                                                                     |

Trend charts and keyword-level tables provide date-wise and keyword-wise visibility for the selected metric.
