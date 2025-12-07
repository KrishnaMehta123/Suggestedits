---
title: USA Compliance Guide
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

SMS communication in the United States is governed by federal regulations and carrier-enforced industry guidelines. This guide outlines the key legal frameworks, sender registration requirements, enforcement standards, and message content rules you must comply with to send SMS in the U.S. through CleverTap.

## Regulatory Landscape

The following federal and industry regulations form the basis of SMS compliance in the U.S.:

- **TCPA (Telephone Consumer Protection Act)**: Requires prior **express written consent** for promotional SMS. For transactional SMS (e.g., OTPs), **express consent** (oral or written) is sufficient. Businesses must retain records of this consent.
- **CTIA Messaging Principles & Best Practices**: CTIA provides industry-wide standards for SMS content, throughput, opt-out handling, and acceptable use. These guidelines are enforced by individual carriers such as AT\&T, Verizon, and T-Mobile.

Non-compliance with TCPA or CTIA guidelines may result in fines, carrier filtering, or legal action.

## Consent and Opt-Out Requirements

You must capture and retain appropriate consent and provide mandatory keyword-based opt-out functionality.

| Consent Type            | Use Case                   | Example Collection Method             |
| ----------------------- | -------------------------- | ------------------------------------- |
| Express Written Consent | Promotional/Marketing SMS  | Checkbox + form submission on website |
| Express Consent         | Transactional (e.g., OTPs) | Voice/phone opt-in or in-app consent  |

| Keyword  | Requirement | Behavior                                        |
| -------- | ----------- | ----------------------------------------------- |
| **STOP** | Mandatory   | Immediately unsubscribes user from campaign     |
| **HELP** | Mandatory   | Responds with customer service/help information |

Maintain consent records for at least four years to comply with TCPA retention guidelines.

## Sending Windows

There is no federal law mandating sending hours in the U.S., but industry best practices recommend sending SMS between **8:00 AM and 8:00 PM** in the recipient’s local time zone to reduce opt-outs and complaints.

## Data Privacy

You must comply with TCPA’s record-keeping provisions and any applicable state laws like CCPA when storing Personally Identifiable Information (PII).

## Available Sender Types

The U.S. supports multiple sender identities based on message throughput and campaign type.

| Sender Type      | Throughput     | Two-Way SMS | Portability | Sender ID Preserved | Provisioning Time | Typical Use Cases                        |
| ---------------- | -------------- | ----------- | ----------- | ------------------- | ----------------- | ---------------------------------------- |
| 10DLC Long Code  | \~1–10 msg/sec | Yes         | Yes         | Yes                 | 1–3 business days | Transactional alerts, moderate marketing |
| Toll-Free Number | \~50 msg/sec   | Yes         | Yes         | Yes                 | 1–2 business days | High-volume support, notifications       |
| Short Code       | 100+ msg/sec   | Yes         | N/A         | Yes                 | 6–10 weeks        | Large-scale promotions, emergencies      |

Short code leasing fees range from \$500–\$1,500/month, with setup and approval fees additional.

## Registration Process

All sender types require registration with appropriate campaign details and sample messages.

### 10DLC Registration

1. Brand Registration: Submit legal name, EIN, business URL, and address.
2. Campaign Registration: Define use case (e.g., OTP, promo) and message samples.
3. Number Registration: Associate 10DLC long codes with approved brand and campaign.

### Toll-Free Registration

- Apply through your SMS provider.
- Follow the same campaign registration workflow as 10DLC.
- Toll-free numbers also require verification before going live.

### Short Code Registration

- Choose between dedicated or shared codes.
- Register via The Campaign Registry (TCR).
- Carriers review all use cases and templates. Approval typically takes 8–12 weeks.

## Content Restrictions

U.S. carrier policies prohibit certain content types and impose fines for violations.

| Content Category                              | Allowed? | Notes                                                    |
| --------------------------------------------- | -------- | -------------------------------------------------------- |
| SHAFT (Sex, Hate, Alcohol, Firearms, Tobacco) | No       | Blocked by default by most carriers.                     |
| Gambling & Sweepstakes                        | No       | Must be explicitly approved; often denied.               |
| High-Risk Financial Services                  | No       | Includes payday loans, credit repair.                    |
| Political Messaging                           | Caution  | Allowed with additional disclosures and opt-out support. |
| Spam & Phishing                               | No       | Strictly blocked and fined.                              |
| Deceptive or Misleading Ads                   | No       | May trigger penalties or suspension.                     |
| Filter Evasion Techniques                     | No       | Includes snowshoeing and URL cycling.                    |

SHAFT is an acronym for restricted content: Sex, Hate, Alcohol, Firearms, Tobacco.

## Non-Compliance Penalties

| Violation Type                    | Penalty                                    |
| --------------------------------- | ------------------------------------------ |
| 10DLC Evasion (e.g., snowshoeing) | \$1,000 per incident                       |
| SHAFT/Spam/Phishing Violations    | \$10,000 per message after initial warning |
| Opt-Out Keyword Non-Compliance    | Carrier account suspension or fines        |

## URL Filtering and Branding

U.S. carriers routinely filter messages containing links from generic URL shorteners like bit.ly or goo.gl. Unlike India, there's no URL whitelisting requirement, but using branded domains (e.g., go.yourbrand.com) improves deliverability and avoids filtering.

Branded URLs should be pre-tested within your SMS campaigns to ensure high deliverability.

## Enforcement Bodies and Carrier Policies

- CTIA sets overarching messaging guidelines, enforced by carriers.
- Carriers (e.g., T-Mobile, Verizon, AT\&T) may also enforce additional restrictions through their Codes of Conduct.
- T-Mobile enforces stricter guidelines for political messaging and requires opt-out confirmation even for transactional flows.

For a comprehensive overview of carrier enforcement, refer to [Twilio’s Messaging Policy](https://www.twilio.com/legal/messaging-policy).