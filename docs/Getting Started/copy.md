---
title: PII Encryption-Copy
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

Encryption secures Personally Identifiable Information (PII) by converting it into unreadable formats that only authorized users can decrypt with valid keys. PII includes sensitive data such as names, email addresses, phone numbers, custom properties, and events. By encrypting this information, CleverTap ensures data remains protected from unauthorized access throughout its lifecycle.

The encryption framework uses secure algorithms to protect data while maintaining usability for segmentation, analytics, and campaign delivery.

Encryption helps you do the following:

- Prevent unauthorized access to PII
- Transmit  customer data securely across systems
- Comply with global and local data protection regulations
- Create a detailed audit trail to meet global compliance standards

> 📘 Private Beta
> 
> This feature is currently available in Private Beta for selected customers. To enable PII Encryption, contact your Customer Success Manager or raise a support ticket.

# Encrypt PII

CleverTap encrypts PII using multiple layers of protection, making sensitive values unreadable at different stages:

- **In Transit **: Encrypts data transmitted via SDKs and SFTP.
- **At Rest ** :  Encrypts stored data in databases, backups, and persistent storage.

This layered protection ensures data confidentiality, integrity, and compliance without compromising usability.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/20d467a044d271b9071dfb8c94cd6538bbe4661da3a2562f3e0268f706a33dfa-image.png",
        null,
        "PII Encryption"
      ],
      "align": "center",
      "border": true,
      "caption": "PII Encryption"
    }
  ]
}
[/block]


## Default vs. Custom Encryption

By default, CleverTap encrypts all incoming user data using AES-256 encryption and securely manages the encryption keys. This default protection applies to all user profiles and event attributes.

Custom Encryption provides an additional layer of protection over the default encryption. It allows customers to mark selected fields (such as email, phone, customerType, and so on) for Encryption. CleverTap applies AES-256 encryption using customer-defined keys. It protects sensitive data without impacting performance.

## Security and Compliance

PII Encryption helps your organization to do the following:

- Protect customer data against unauthorized access
- Ensure secure storage and transmission of data
- Meet compliance standards such as GDPR, CCPA, HIPAA, and ISO 27001
- Enforce role-based access and audit controls

## Eligible Data

You can mark any of the following system properties for Encryption:

**System User Properties**

- Email {@meenakshi, email, phone number, and identity are system user properties and event properties too ?}
- Phone number
- Identity
- Name
- Gender
- DOB (Date of Birth)
- Latitude
- Longitude
- Location

**System Event Properties**

- Email
- Phone number
- Identity
- For the event **Identity Set**, the PII property `ID` is masked.
- For the event **Identity Reset**, the PII property `ID` is masked.
- For the event **Identity Error**, the PII property `ID` is masked.

For more information about System Events and properties, refer to [Events](doc:events#overview).

You can also enable encryption for custom events. Once you allow encryption for a custom event property, CleverTap will encrypt the new incoming data. CleverTap does not encrypt historical data.

> 🚧 Encryption is an irreversible process.
> 
> You cannot revert a property to an unencrypted state.

## Encrypt Data at Rest

CleverTap automatically encrypts stored data using industry-standard encryption methods:

- Uses AES-256 encryption for all stored data
- Manages encryption keys through key management.
- Implements key rotation and audit logging based on industry-accepted best practices

## Encrypt Data in Transit

CleverTap secures all data transferred via SDKs ([Android](https://developer.clevertap.com/docs/android-advanced-features#encryption-in-transit)& [iOS](https://developer.clevertap.com/docs/advanced-options-ios#encryption-of-pii-data))  and [SFTP](https://docs.clevertap.com/docs/file-upload-encryption):

- We use TLS 1.3 for transport security
- Uses AES-256(SDK) & PGP encryption(SFTP)
- Supports mutual TLS (mTLS) for SDK communications
- Routes requests to region-specific endpoints for compliance with data residency regulations

# Encrypt Custom Event Properties

You can apply Encryption to event properties either individually or in bulk.

## Encrypt a Single Event Property

To encrypt an individual event property, follow the steps:

1. Go to_ Settings > Schema > Events > Custom Events_.
2. Click **Properties** for the required event.
3. Click the ellipsis menu and select **Encrypt**.
4. In the confirmation dialog, click **Encrypt**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/243c2b2174e002539b50012bb92c9ddea518580dfc437c609e6f298d9c489d42-2025-07-17_13-47-26_1.gif",
        "",
        "Encrypt PII Values"
      ],
      "align": "center",
      "border": true,
      "caption": "Encrypt PII Values"
    }
  ]
}
[/block]


The following image shows the encrypted PII properties:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fd5aeb3c96ab14bada82f33000502147d8d8985f199ef19f2ed13844eacd08f0-image.png",
        null,
        "Encrypted Properties"
      ],
      "align": "center",
      "border": true,
      "caption": "Encrypted Properties"
    }
  ]
}
[/block]


## Encrypt Multiple Event Properties

To encrypt multiple properties, follow the steps:

1. Go to_ Settings > Schema > Events > Custom Events_
2. Click **Properties** for the required event
3. Select multiple properties.
4. Click the ellipsis menu and select **Encrypt**.
5. In the confirmation dialog, click **Encrypt**.

CleverTap queues the selected fields for encryption and displays the encrypted fields as  
Encrypted.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ec06009cee093f2b52eba568fd2c6ac23d45381460b3f27d300636c188c7cb05-2025-08-14_19-43-21_1.gif",
        "",
        "Bulk Encryption"
      ],
      "align": "center",
      "border": true,
      "caption": "Bulk Encryption"
    }
  ]
}
[/block]


> 📘 Viewing Encrypted Values
> 
> Only Admins and authorized users can view or download encrypted values.
> 
> The visibility of encrypted values on the _Segment _ and _Analytics _ pages depends on your role. For roles without encryption access, these values remain hidden. Roles with encryption permissions can view and use the encrypted values for segmentation and analytics.

# Supported Entities

The following are the supported entities where the users can retrieve encrypted data based on the role granted to them :

{@meenakshi, give a bulleted list here with cross-references to the following headings so that the user can get an overview }

## Segments

You can create Segments and apply filters to encrypted fields based on your permissions. The segmentation functionality is available in **Create segment** and **Find People**.

### Create Segment Using Encrypted Properties

When creating segments, you can use encrypted fields such as Email, Phone, Identity, and other custom properties as filters. {@meenakshi, lead-in misisng}

1. Go to **Segments **and click **Segment**.
2. Build a segment using past or live events and the filters based on encrypted fields. 

The system applies permission checks to ensure only authorized users can view or segment these properties. Segments created with encrypted fields are usable across analytics and engagement workflows. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b2295177bba75adbf5e8c668a88a6c56ba136b7d4cc4a9cd05aedf90ea96ef14-image.png",
        null,
        "Encrypted Values in Segment Builder"
      ],
      "align": "center",
      "sizing": "70% ",
      "border": true,
      "caption": "Encrypted Values in Segment Builder"
    }
  ]
}
[/block]


## Find People

If you have permission to access the encrypted data, you can search for users using encrypted fields, such as Search by Email or Phone.

The following image shows how to set up an event filter rule in an analytics or engagement platform. The rule builder excludes specific user events, such as a _ChargedAction_ within the last 30 days, and applies {@meenakshi, applies automatically or simply offers ?}additional filtering by narrowing down event properties. When users without decryption access query encrypted fields, the drop-down {@meenakshi, it is not a dropdown it is a list}displays **This is an encrypted value** in the list to indicate restricted visibility of results.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c81c5c53494c9ab72866bace1d2b39fa3bb3ca0931ef1937d37dd2d38d4e1769-image.png",
        null,
        "Query using Encrypted Values"
      ],
      "align": "center",
      "border": true,
      "caption": "Query using Encrypted Values in Find People"
    }
  ]
}
[/block]


For more details on user permissions and access, refer to [Role-Based Access Control: Advanced Governance Limits](https://docs.clevertap.com/docs/role-based-access-control-advanced-governance-limits#engagement-permissions).

## Engagements

You can create **Campaigns** and **Journeys** using segments that include encrypted fields. These workflows support targeting, personalization, and analytics without exposing the underlying PII.

### Create Campaigns with Encrypted Fields

1. Go to **Campaigns **and click **Campaign**.
2. In the _Who_ section, define the segment using an encrypted property.

The following image shows the drop-down {@meenakshi, list}showing {@meenakshi, shows and showing used twice, rephrase the sentence}that the selected event property is encrypted:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/706634a1ed9f9c1c195c3f0b9ac108d8a54a22ad517158349083a8f041319c11-image.png",
        null,
        "Filter using Encrypted Values in Campaigns"
      ],
      "align": "center",
      "border": true,
      "caption": "Filter using Encrypted Values in Campaigns"
    }
  ]
}
[/block]


If the campaign user role permits access, you can use personalization fields such as email and phone. Campaign messages sent via email or push will use encrypted data securely.

### Create Journeys with Encrypted Fields

{@meenakshi, lead-in missing}

1. Go to **Journeys **and click **Journey**.
2. Define triggers and paths using encrypted segments.

Use encrypted data fields for decision splits and personalization based on permissions. 

### Analytics

Users with the right permissions can query events using encrypted values. The drop-down{@meenakshi, list} in the following image displays **This is an encrypted value**, ensuring PII remains protected and usable for Analytics.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3f77c0333db9af68ad1e1a6d62e35339ae3a6c74fa7a92ddcf8b507d78510d9e-image.png",
        null,
        "Query using Encrypted Values in Analytics"
      ],
      "align": "center",
      "border": true,
      "caption": "Query using Encrypted Values in Analytics"
    }
  ]
}
[/block]


> 📘 Require Permission
> 
> Only users with appropriate permissions can use encrypted fields in engagement workflows. Unauthorized users only see placeholder values or cannot select segments.

The following image shows the message displayed when the system restricts access:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/24217dba1ca61abb4006cd5cfa51e6a9553f69ad82f888e5702441cf5bac8be1-image.png",
        null,
        "Restricted Access"
      ],
      "align": "center",
      "border": true,
      "caption": "Restricted Access"
    }
  ]
}
[/block]


## Manage Entities with Encrypted Data

Campaign management involving encrypted data are supported through **CGL (Campaign Global List)** and **GTL (Global Test List)**, {@meenakshi, link the relevant pages here}with certain limitations:

- Lists {@meenakshi, what lists are these ? GCL and GTL ? use the direct names here}using encrypted fields are partially supported.
- Authorized users can create and manage campaigns that leverage encrypted fields for segmentation and targeting.
- Campaign targeting and delivery remain functional with encrypted data while preserving data confidentiality.
- Use filtered segments instead of global lists where direct access is restricted.
- Configure audience targeting using segment-based filters.

# Frequently Asked Questions

The following FAQs address common questions about how PII encryption works, where it applies, and what limitations to expect.

### What encryption algorithm does CleverTap use?

CleverTap supports encrypting customer data using AES-256 encryption keys.

### Is data encrypted at rest?

Yes. All stored data is encrypted by default using AES-256 encryption keys, which are managed securely through key management. We also provide the feasibility of encrypting data by adopting the customer's chosen encryption keys.

### Can I search or segment on encrypted fields?

Yes. You can search and segment on encrypted fields. The usability of encrypted fields depends on your dashboard [access permissions](https://docs.clevertap.com/docs/role-based-access-control-advanced-governance-limits#engagement-permissions). If you can access encrypted data, you can use these fields for segmentation and targeting without restrictions.

### Can I disable Encryption for a field later?

No. Encryption is irreversible.

### Does Encryption impact performance?

No. CleverTap handles encryption at the infrastructure level to ensure minimal latency and no noticeable impact on dashboard or campaign performance.

### How does masking interact with encryption?

If a property is both encrypted and masked, encryption always prevails. Encrypted values remain protected even if masking is also applied. For more information, refer [PII Masking](doc:masking).

### Who can view encrypted or masked values?

Access depends on the user role:

- Admins:  Can view both encrypted and masked values.
- Authorized Users:  Can view masked values, but encrypted values remain hidden.
- Unauthorized users Cannot view encrypted or masked values; the system displays placeholders instead. Also, queries based on PII fields are blocked.

### Can I build a segment using encrypted fields?

With the right permissions, you can build a segment using encrypted fields. Only authorized users can access the decrypted values.

### Can campaigns be created with encrypted data?

Yes. Campaigns and Journeys can use encrypted fields for personalization and targeting, subject to role-based permissions.