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
* **Segment-based Unsubscribe**
* **Error-based Unsubscribe**
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

<br />
