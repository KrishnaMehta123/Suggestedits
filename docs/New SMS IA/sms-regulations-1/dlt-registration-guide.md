---
title: DLT Registration Guide
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

India’s SMS compliance framework, governed by the Telecom Regulatory Authority of India (TRAI), mandates that all senders register on a Distributed Ledger Technology (DLT) platform. This document provides a complete overview of the registration process for Principal Entities and Telemarketers, including header and template configuration, URL whitelisting, and integration with CleverTap.

## Understanding DLT Compliance

DLT (Distributed Ledger Technology) is a blockchain-based system used to track and verify all SMS communication initiated by businesses in India. Introduced by TRAI, it aims to curb spam and fraud by enforcing identity, content, and consent-based regulations across all telecom operators.

## Roles Involved in DLT

The DLT ecosystem consists of several stakeholders, each playing a critical role in managing message delivery compliance and user protection.

| Role             | Description                                                                         |
| ---------------- | ----------------------------------------------------------------------------------- |
| Principal Entity | A business, brand, or organization that sends SMS to customers                      |
| Telemarketer     | A registered vendor or SMS aggregator authorized to send messages on behalf of a PE |
| End User         | The mobile subscriber who receives SMS and manages preferences                      |
| Telecom Operator | Network provider that enforces TRAI compliance via DLT implementation               |
| Regulator (TRAI) | Government body enforcing legal, content, and consent standards                     |

## Registering as a Principal Entity

All businesses intending to send SMS must register themselves as a Principal Entity (PE) on any operator-approved DLT portal. This section outlines the required documents, registration steps, and expected timelines.

1. **Select a DLT portal**: Use portals such as Jio TrueConnect, Airtel DLT, Vi Power, or BSNL DLT.
2. **Fill Principal Entity Details**: Include PAN, GSTIN, business type, and authorized contact.
3. **Upload Required Documents**:

   * PAN Card
   * GST Certificate
   * Certificate of Incorporation
   * Address Proof (utility bill, lease agreement)
   * Authorization Letter
4. **Verify Email and Mobile**: Complete OTP-based verification.
5. **Approval Timeline**: Typically granted within 48–72 hours.

## Authorizing a Telemarketer

A Telemarketer (TM) is an SMS aggregator or delivery vendor who sends messages on behalf of the Principal Entity. Binding your PE to a registered TM is mandatory for message submission and delivery.

1. **Go to Telemarketer Management** on your DLT portal.
2. **Add Telemarketer Details**: Use TM Name and TM ID as provided by your aggregator.
3. **No Additional KYC Required**: The TM must already be registered.
4. **Sync Timeline**: Binding syncs across all DLT portals within a few hours.

> 📘 Note
>
> Only Telemarketers bound to your PE can submit headers, templates, and SMS traffic.

## Registering Sender Headers

All sender identities—also known as headers—must be registered and approved under the correct category suffix. Each header must be uniquely mapped to your business and purpose of messaging.

1. **Navigate to the Headers section** in your DLT portal.
2. **Add Header (Sender ID)**:

   * For Transactional: 6-letter alphabetic + suffix -T
   * For Promotional: 6-digit numeric + suffix -P
   * For Service: 6-letter alphabetic + suffix -S
   * For Government: 6-letter alphabetic + suffix -G
3. **Provide Rationale**: In some cases, a business justification or document may be required.
4. **Approval Timeline**: Typically processed within 1–2 business days.

## Whitelisting URLs for SMS Campaigns

TRAI mandates URL whitelisting to ensure safety and avoid misuse in SMS campaigns. This includes static URLs, dynamic URLs, and branded short domains.

| URL Type      | Notes                                                            |
| ------------- | ---------------------------------------------------------------- |
| Static URLs   | Must start with http\:// or https\:// and be publicly accessible |
| Dynamic URLs  | Query strings supported only if base domain is whitelisted       |
| Short Domains | Custom short domains (e.g., go.brand.com) must be registered     |

1. **Navigate to the CTA or URL Whitelisting section** on the DLT portal.
2. **Submit each link** with associated header and message purpose.
3. **Agree to TRAI terms** and submit for approval.
4. **Sync with CleverTap**: Update your CleverTap short link configuration to reflect approved domains.

> 📘 Note
>
> Messages with non-whitelisted URLs will be blocked outright at the operator level.

## Registering Message Templates

All message content must be pre-registered with exact copy and placeholders. No changes can be made after approval unless resubmitted.

1. **Go to the Template Management section** of your DLT portal.
2. **Add Template Text** using placeholder syntax like `Dear {#var#}, your OTP is {#var#}`.
3. **Assign Header and Message Category**:

   * Header: The sender ID this message will be sent from.
   * Message Category: One of Transactional, Promotional, Service, or Government.
4. **Upload Sample Screenshot** if required.
5. **Approval Timeline**: Typically instant to a few hours.

## Integrating DLT Credentials with CleverTap

After obtaining approvals, you must configure your DLT credentials in CleverTap for seamless SMS campaign execution.

| Credential  | Description                                                            |
| ----------- | ---------------------------------------------------------------------- |
| Entity ID   | Unique ID assigned to your business account during PE registration     |
| Header ID   | ID corresponding to the approved Sender Header used for messaging      |
| Template ID | ID linked to the exact message template pre-approved on the DLT portal |

> 📘 Note
>
> These identifiers must be added to your SMS configuration in CleverTap or passed via APIs.

## Maintenance and Ongoing Compliance

To remain compliant with TRAI’s evolving policies, regular maintenance of your DLT registration is essential. This includes:

* Quarterly audits of headers and templates.
* Updating records for revoked or expired entities.
* Monitoring delivery reports for CTA mismatches.
* Ensuring whitelisted links remain active and approved.
