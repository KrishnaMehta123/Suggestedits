---
title: SMS Glossary and Compliance Reference
excerpt: ''
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

This glossary defines key SMS-related terms and regulatory concepts to help you navigate global compliance, message formatting, sender types, and technical behaviors in CleverTap. Refer to this document whenever you need clarity on terminology or country-specific requirements.

## Messaging Standards

The following terms define the core structure and routing logic behind SMS communication.

| Term                        | Definition                                                                                            |
| --------------------------- | ----------------------------------------------------------------------------------------------------- |
| A2P (Application-to-Person) | SMS sent from a platform (like CleverTap) to a user.                                                  |
| P2P (Person-to-Person)      | SMS sent directly between two individuals.                                                            |
| MT (Mobile-Terminated)      | Outbound message delivered to a user’s device.                                                        |
| MO (Mobile-Originated)      | Inbound message sent by a user, such as a reply.                                                      |
| Message Segment             | A 160-character block (GSM-7) or 70 characters (Unicode). Longer messages are split and concatenated. |

## Sender and Channel Types

These terms explain how sender identities appear to users and how they impact routing, throughput, and interactivity.

| Term                       | Definition                                                                                      |
| -------------------------- | ----------------------------------------------------------------------------------------------- |
| Alphanumeric Sender ID     | A branded sender name (e.g., ACME) made up of 6–11 characters. Cannot receive replies.          |
| Long Code / Virtual Number | A full-length phone number (e.g., +1 408 XXX XXXX) that supports two-way communication.         |
| Toll-Free Number (TFN)     | A U.S. or Canada-based number (e.g., 1-800) used for higher throughput and two-way SMS.         |
| Shortcode                  | A 3–6 digit number used for high-volume A2P traffic.                                            |
| Dedicated Shortcode        | Exclusive to your brand; requires provisioning and approval.                                    |
| Shared Shortcode           | Shared across brands; opt-out and interaction depends on unique keywords (e.g., **STOP ACME**). |

## Compliance and Opt-In Terms

These definitions clarify how CleverTap handles SMS subscriptions, consent, and user interaction workflows.

| Term              | Definition                                                                                             |
| ----------------- | ------------------------------------------------------------------------------------------------------ |
| Opt-Out           | The process by which a user unsubscribes from SMS, typically by replying **STOP**.                     |
| Double Opt-In     | A two-step confirmation process where the user first subscribes and then confirms via a follow-up SMS. |
| Keyword           | A specific word (e.g., **STOP**, **HELP**) that users send to trigger system actions.                  |
| Silent Hours      | Time blocks during which marketing SMS should not be sent (e.g., 10 PM – 9 AM local).                  |
| Frequency Capping | A control that limits how many messages a user can receive in a given time window.                     |
| Snowshoeing       | The non-compliant practice of spreading traffic across multiple sender numbers to bypass filters.      |

## Technical and Delivery

These terms relate to message transmission, reporting, and deliverability infrastructure.

| Term                   | Definition                                                                                                                 |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| DLR (Delivery Receipt) | A status update (Sent, Delivered, Failed) returned by the carrier.                                                         |
| E.164 Format           | The international number format required for SMS: “+” followed by country code and subscriber number (e.g., +14155550101). |
| Throughput             | The maximum number of messages that can be sent per second via a given sender route.                                       |
| Carrier Filtering      | Filtering done by telecom networks to block spam or suspicious messages.                                                   |
| Flash SMS              | An SMS that displays instantly on the user’s screen and is not stored in the inbox.                                        |
| URL Whitelisting       | Registering and approving branded domains to avoid SMS link blocking.                                                      |
| Template ID            | A registered, pre-approved format for messages required by DLT (India) and 10DLC (US).                                     |
| Campaign ID            | A unique identifier applied to each campaign in CleverTap to support tracking and performance analysis.                    |

## Regional Frameworks

Different countries and regions require specific registration and approval processes to deliver A2P SMS.

| Region | Requirement                                      | Summary                                                                                            |
| ------ | ------------------------------------------------ | -------------------------------------------------------------------------------------------------- |
| India  | DLT (Distributed Ledger Technology) Registration | All sender IDs and templates must be pre-approved via telecom operator portals.                    |
| USA    | 10DLC (10-Digit Long Code)                       | Brands must register with The Campaign Registry to send A2P traffic via standard 10-digit numbers. |
| UAE    | Carrier-Level Approval                           | Manual registration of both sender and message content with local telecom authorities is required. |