---
title: India Compliance Guide
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

India enforces one of the world’s most comprehensive SMS compliance frameworks, governed by the Telecom Regulatory Authority of India (TRAI) through a Distributed Ledger Technology (DLT) platform. This guide outlines the required setup, permitted messaging types, registration process, and enforcement rules for sending SMS via CleverTap in India.

## Regulatory Framework Overview

SMS delivery in India requires full registration and approval through a centralized blockchain-based platform mandated by TRAI. This section introduces the core entities involved in the regulatory structure.

| Component             | Description                                                                                |
| --------------------- | ------------------------------------------------------------------------------------------ |
| Regulatory Authority  | Telecom Regulatory Authority of India (TRAI)                                               |
| Enforcement System    | Distributed Ledger Technology (DLT), implemented via operator portals like Jio, Airtel, Vi |
| Required Registration | Business entity (Principal Entity), Sender ID (Header), Message Templates, URLs            |
| Message Categories    | Promotional, Transactional, Service, Government                                            |
| Compliance Features   | Time-bound delivery, opt-in consent, template approval, URL whitelisting                   |

## Classification of Sender ID Types

Sender IDs—called Headers—must be registered under the appropriate category and format. TRAI mandates suffix-based enforcement to distinguish use cases.

> Choosing the correct header type ensures message delivery and compliance with time and category restrictions.

| Header Type   | Format            | Suffix | Two-Way SMS | Provisioning Time   | Example Use Cases                   |
| ------------- | ----------------- | ------ | ----------- | ------------------- | ----------------------------------- |
| Transactional | 6-character alpha | \-T    | No          | \~1–2 business days | OTPs, payment alerts, order updates |
| Promotional   | 6-digit numeric   | \-P    | No          | \~1–2 business days | Offers, sales, marketing promotions |
| Service       | 6-character alpha | \-S    | No          | \~1–2 business days | Password resets, account statements |
| Government    | 6-character alpha | \-G    | No          | \~1–2 business days | Civic messaging, government alerts  |

## Complete DLT Registration Flow

To send SMS messages, all business entities must complete registration on a TRAI-approved DLT portal. This section outlines the step-by-step onboarding and approval workflow.

> DLT registration is a one-time setup process that synchronizes across all major operator portals once completed.

### Principal Entity Registration

You must begin by registering as a Principal Entity (PE).

1. Choose an operator DLT portal (e.g., Jio TrueConnect, Airtel DLT, ViPower, BSNL DLT).
2. Go to **Principal Entity Registration**.
3. Provide the following:

   - Legal Name, Entity Type, PAN, GSTIN
   - Valid email and mobile number
   - Upload supporting KYC documents: incorporation certificate, address proof, authorization letter
4. Verify email and phone via OTP
5. Submit for approval (typically within 48–72 hours)

### Telemarketer Binding

After Principal Entity approval, you must authorize your SMS aggregator—referred to as the **Telemarketer**—for header and template submission.

> Binding your Principal Entity to a Telemarketer allows that aggregator to provision headers and templates on your behalf.

| Step                   | Description                                                               |
| ---------------------- | ------------------------------------------------------------------------- |
| Access Telemarketer UI | Go to **Telemarketer Management**                                         |
| Add Aggregator Info    | Input your aggregator's Telemarketer Name and Telemarketer ID             |
| Submit Binding         | No additional KYC needed; syncs across all DLT portals within hours       |
| Confirm Access         | Once complete, your aggregator can register headers and templates for you |

### Header Registration

Once your Principal Entity is bound to a Telemarketer, you can proceed to register Sender IDs.

1. Navigate to **Headers / Sender IDs**.
2. Select the header type: Transactional, Promotional, Service, or Government.
3. Apply the corresponding suffix (-T, -P, -S, -G).
4. Provide rationale if prompted.
5. Submit for approval (1–2 business days typical).

> Headers define the sender’s identity in each SMS. Each must align with your registered business use case and template category.

### URL Whitelisting

TRAI mandates all domains and short links in SMS messages must be whitelisted before usage.

> Non-whitelisted URLs will result in outright delivery failure—this is a mandatory compliance check.

| Requirement           | Detail                                                                 |
| --------------------- | ---------------------------------------------------------------------- |
| Type of URLs          | Static, dynamic, or branded short links (e.g., <https://go.brand.com>) |
| Whitelisting Location | “Content Templates” or dedicated “URL Whitelisting” tab                |
| Link & Header Mapping | Associate each URL with an approved header                             |
| Approval Timeframe    | Usually within 1 business day                                          |
| CleverTap Sync        | Update whitelisted links in CleverTap’s SMS link shortener config      |

### Template Registration

Templates define the SMS message body and must be approved before use.

1. Go to **Message Templates**.
2. Add message content using `{#var#}` placeholders for personalization.
3. Assign a **Header** and **Message Category**:

   - _Header_ refers to the approved Sender ID that the message will be sent from.
   - _Message Category_ defines the classification of the message (Promotional, Transactional, etc.).
4. Upload a sample screenshot if requested.
5. Submit for approval (instant to 1–2 hours depending on operator).

> Templates with minor copy variations must be filed separately. Reuse without approval will result in blocking.

### Integration with CleverTap

Following registration, you must map the DLT credentials inside your CleverTap account to enable delivery.

1. Gather your approved credentials:

   - **Entity ID**: Identifies your registered business (Principal Entity) in the DLT system.
   - **Header ID**: Represents the approved sender name that will appear in user inboxes.
   - **Template ID**: Corresponds to each pre-approved SMS body with variables.
2. Add these to your SMS provider configuration inside CleverTap.
3. Set up variable mappings in the message composer.
4. Perform a test send to confirm setup integrity.

> All fields are mandatory for India-based sends. Ensure all mappings are accurate before scheduling campaigns.

## Delivery Restrictions and Messaging Requirements

TRAI imposes message-level rules to safeguard consumer interests. These vary by SMS type and must be adhered to strictly.

> Failure to comply with delivery windows, DND filtering, or content guidelines may result in penalties and blocked messages.

### SMS Timing and DND Rules

| Message Type  | Allowed Times   | DND Delivery | Notes                                        |
| ------------- | --------------- | ------------ | -------------------------------------------- |
| Promotional   | 9 AM – 9 PM IST | Blocked      | Only to non-DND users with explicit opt-in   |
| Transactional | 24×7            | Allowed      | Can be sent to DND numbers                   |
| Service       | Action-based    | Varies       | Implicit (password reset) or explicit opt-in |
| Government    | 24×7            | Allowed      | No restrictions                              |

### Prohibited Content Categories

Certain message content types are entirely disallowed under Indian telecom law.

- Adult content and services
- Lottery, gambling, cryptocurrency
- Hate speech, defamation, obscenity
- Fraudulent schemes (“you’ve won a prize”)
- Political messages during election blackout periods
- Unapproved short URLs or non-whitelisted domains
- Spam volume (>6 identical messages/hour to same user)

### Template Format and Variables

| Rule               | Enforcement                                               |
| ------------------ | --------------------------------------------------------- |
| Pre-registration   | Mandatory—messages without template ID will be blocked    |
| Placeholder Syntax | Use `{#var#}`; limit 5–6 variables per message            |
| Branding           | Include sender brand name clearly within the message text |

## Enforcement and Audits

TRAI enforces ongoing compliance through regular audits and message filtering.

> Maintain all approvals and audit trails—non-compliance may lead to delivery suspension or DLT portal blocks.

- Reverify headers and templates quarterly
- Renew or update expired approvals
- Monitor campaign reports in CleverTap for blocked message rates
- Resubmit any edited content