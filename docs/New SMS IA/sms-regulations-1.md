---
title: SMS Regulations
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
# Registration and Compliance Overview

Running SMS campaigns globally requires strict adherence to carrier regulations and government mandates. To maintain high deliverability, protect users, and stay legally compliant, CleverTap offers structured support for regional registration requirements and sender provisioning. This document provides a foundational overview before diving into country-specific compliance guides.

## Document Scope

This document outlines the global considerations businesses must take into account when sending SMS. It introduces the types of sender identities available, explains template registration, and provides a summary of keyword handling and callback integration. Additional country-specific guides expand on these topics in depth.

## Sender Types

SMS can be sent from various sender identities, each with different properties and compliance implications. Selecting the correct sender type impacts throughput, delivery success, and user experience.

| Sender Type      | Description                                                           | Supports Replies | Typical Use Case                  |
| ---------------- | --------------------------------------------------------------------- | ---------------- | --------------------------------- |
| 10DLC Long Code  | 10-digit number sanctioned for A2P use in the USA                     | Yes              | Transactional and marketing       |
| Toll-Free Number | Number starting with 800, 888, etc., sanctioned for two-way messaging | Yes              | Customer support, notifications   |
| Short Code       | 3–6 digit number used for high-throughput A2P messaging               | Yes              | Flash sales, urgent alerts        |
| Alphanumeric ID  | Sender name (up to 11 chars), often used in India, UAE                | No               | Brand recognition; one-way alerts |

> **Note**: Two-way messaging is supported only on specific number types. Refer to region-specific compliance guides for eligibility.

## Template Registration

In many countries, regulatory frameworks require businesses to register their SMS content before messages can be sent. This process ensures that message formats are approved, traceable, and compliant.

- **India**: TRAI’s DLT framework mandates that entities, headers, and message templates must all be registered before delivery.
- **United States**: Through the Campaign Registry, brands must declare use cases and submit sample content for 10DLC approval.
- **Other Regions**: Countries such as the UAE may require manual review of templates or restrict certain keywords or content types.

CleverTap helps you manage this process via Native SMS (pre-integrated partners) or BYOP (Bring Your Own Provider) mode.

## Keyword Requirements

Certain keywords are monitored by carriers globally and must be supported by all sender types that accept replies. These keywords are used to manage user consent and compliance.

- **STOP** – Opt-out from future messaging.
- **HELP** – Receive help information or contact details.

Carriers monitor and enforce handling of these replies. If unprocessed, they may suspend or filter the sender ID. CleverTap automatically processes these keywords when enabled through our Native SMS service.

## Delivery and Reply Callbacks

To ensure accurate delivery tracking and regulatory compliance, SMS providers must send delivery receipts (DLRs) and mobile-originated replies (MOs) back to CleverTap.

- **DLRs** confirm message status—delivered, failed, or queued.
- **MOs** provide user responses, such as **STOP** or **HELP**, or any inbound interaction.

Callback URLs can be configured within the CleverTap dashboard for providers using the BYOP mode. Native SMS users do not need to configure this manually—callbacks are handled directly by CleverTap.

## URL Whitelisting

Some countries require SMS campaigns to use only pre-approved links or short domains. This ensures that recipients are not exposed to misleading or malicious content and helps preserve sender reputation.

- **India**: All URLs in templates must be whitelisted during DLT registration.
- **USA**: Using generic shorteners like `bit.ly` may trigger spam filters; use branded URLs instead.

Consult the relevant compliance guide to understand regional requirements for link whitelisting and how to configure short links within CleverTap.

## Regional Compliance Guides

To meet SMS regulations in your target countries, refer to the following detailed guides:

- [USA Compliance Guide](#)
- [India Compliance Guide](#)
- [DLT Registration](#)

Each guide provides country-specific regulations, sender ID types, template requirements, quiet hours, prohibited content, and callback configurations.

## Legal Notice

This document does not constitute legal advice. All brands using SMS must ensure compliance with local laws, telecom frameworks, and data protection mandates. Always consult your legal counsel before launching campaigns.