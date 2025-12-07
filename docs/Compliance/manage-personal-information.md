---
title: Manage Personal Information
excerpt: >-
  Understand different ways in which CleverTap protects end-user personal
  information.
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

Personally Identifiable Information (**PII**) is any data that can identify an individual. PII may be used alone or in combination with other relevant data to identify an individual.

PII may include the following:

- Name
- Address
- Email
- Telephone Number
- Date of Birth
- Passport Number
- Fingerprint
- Credit or Debit Card Number
- Social Security Number

CleverTap does not automatically collect PII information, such as usernames, advertising identifiers, email addresses, mailing addresses, phone numbers, precise locations (such as GPS coordinates of four decimal places or more), and so on. PII data must be explicitly pushed to CleverTap for it to be collected.

# Manage PII

To manage PII for end-users, you may use any or a combination of the following practices:

- [PII Masking](doc:masking)
- [Encrypt PII](doc:manage-personal-information#encrypt-pii) 
- [Audit Your Integration](doc:manage-personal-information#audit-your-integration)
- [Use Non-PII Identifiers](doc:manage-personal-information#use-non-pii-identifiers)
- [Use Server-Side Implementation](doc:manage-personal-information#use-server-side-implementation)
- [Track Malicious Users](doc:manage-personal-information#track-malicious-users)

## Mask PII

PII masking is the process of hiding or obscuring sensitive information to protect individuals' privacy and security. It is commonly used in data storage and transmission, especially when the data needs to be shared with third parties or stored in a less secure location. Organizations need to use PII masking techniques to prevent data breaches and protect the privacy of their customers or users.

CleverTap lets you mask PII information to ensure security. For more information, refer to [Enable PII Masking](https://docs.clevertap.com/docs/role-based-access-control#define-access-for-advanced-custom-roles) and [Masking Personally Identifiable Information](https://docs.clevertap.com/docs/role-based-access-control#mask-personally-identifiable-information-and-events).

## Encrypt PII

CleverTap implements encryption to safeguard data through a two-step process utilizing a symmetric encryption algorithm, specifically to protect sensitive information such as email addresses and phone numbers.

PII encryption enables the following:

- Protects customer data against potential security breaches by adding an extra encryption layer.
- Ensures accountability and privacy since CleverTap employees' access to customer data is restricted and logged. {@sunil, to write here that CT employees cannot see customer data unless the customer permits for troubleshooting purposes.}

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/90609aeb8f0e4b4f389d58517af68b3a0d288a04365675d73dae4640bd47bf27-image.png",
        null,
        "Data Encryption with CleverTap"
      ],
      "align": "center",
      "border": true,
      "caption": "Data Encryption with CleverTap"
    }
  ]
}
[/block]


### Encryption Levels {@sunil to rethink this}

You can select how you want to encrypt your data. CleverTap provides the following levels{@sunil to rethink the levels of encryption}: {@sunil to add that data is not encrypted retrospectively}

- **Dual-Layer Encryption:**
  - **First Layer:** Data is initially protected with a specific encryption algorithm.
  - **Second Layer:** The encrypted data is re-encrypted using a key from the user or assigned by CleverTap.
- **Selective Encryption:** This encryption is applied only to new data after the feature is enabled. {@sunil,, this is WIP }

### Encryption Stages

The encryption and decryption of data adhere to the highest standards to maintain security. Following are the scenarios for encryption and decryption of data: {@sunil to rethink the levels of encryption, also consider encryption of data at rest and transit in SDK}:

1. **Data Ingestion:** Data is encrypted before entering the CleverTap system.
2. **Data Decryption:** Occurs only before campaigns are sent and is logged for transparency.
3. **Data Dispatch:** Data is decrypted solely during campaign transmission, maintaining its security.

### Encrypt and Access PII Data

- Encrypt Events - link to schema- events page
- Encrypt Custom User Profile Properties - Link to schema - user profile page
- Access Data- Link to RBAC page

## Audit Your Integration

While planning your Integration, you should consult your internal legal counsel before pushing sensitive information such as PII to CleverTap. Get your [Event Design](https://docs.clevertap.com/docs/sample-events-by-business-verticals) document audited to prevent any _arbitrary data_ from being pushed to CleverTap. We recommend only pushing the _data needed_ to achieve the business objectives. For live integrations, use our Schema framework to audit the data pushed to CleverTap.

## Use Non-PII Identifiers

CleverTap's client-side SDKs automatically assign a unique random identifier called a CleverTap ID. You can associate the _CleverTap ID_ with an identifier such as an email address, phone number, or database ID via client-side SDKs or APIs. We strongly recommend using a non-PII identifier. 

## Use Server-Side Implementation

CleverTap SDKs are open source and can be viewed in the [CleverTap Github Repository](https://github.com/CleverTap). You can also push data to CleverTap using our APIs or SFTP. We recommend a hybrid approach of client-side SDKs and APIs wherein the APIs pass sensitive information to CleverTap when required.

## Track Malicious Users

CleverTap SDKs use iOS or Android native storage. If a device's security is compromised or a user roots their Android device or jail breaks their iOS device, the data may be available for access to other third-party apps. We recommend using Non-PII identifiers and [Server-Side Implementation](https://developer.clevertap.com/docs/upload-user-profiles-api) for PII data. It can help you avoid any leakages.

# GDPR Compliance

CleverTap does not collect any of the data types by default, thus ensuring GDPR compliance for our clients. We go to great lengths to ensure customer data security, privacy, and confidentiality. We provide a role-based app­ level access control to customers to manage access to their data.

For more information, refer to [SDK Changes for GDPR Compliance](https://developer.clevertap.com/docs/sdk-changes-for-gdpr-compliance).