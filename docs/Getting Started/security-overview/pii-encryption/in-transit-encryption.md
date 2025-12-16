---
title: PII Encryption for API (in Transit)
excerpt: Learn how CleverTap protects PII during transmission with TLS 1.3 and AES-256.
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

PII Encryption for API provides an additional security layer for customers who need stronger protection beyond HTTPS/TLS. This feature enables Hybrid Public Key Encryption (HPKE) for encrypting both incoming API requests and outgoing CleverTap responses, so sensitive information remains protected throughout transmission.

The feature preserves existing API behavior, constraints, and performance expectations while adding optional payload-level encryption for customers operating in highly regulated or security-sensitive environments.

<Callout icon="📘" theme="info">
  **Private Beta**

  This feature is available in Private Beta. To enable PII Encryption for API on your account, contact your Customer Success Manager.
</Callout>

## Capabilities of PII Encryption for API

With HPKE-based encryption, you can do the following:

* Protect sensitive values at the payload level in addition to TLS.
* Send encrypted binary request bodies to any CleverTap API.
* Receive encrypted API responses when requested.
* Manage your own public keysets and rotate keys securely.
* Maintain full compatibility with existing API workflows, without modifying request or response schemas.

Encryption applies only to data in transit. No changes occur to API rate limits, payload size limits, throttling rules, or existing functionality.

# Encryption Model

PII Encryption for API uses Hybrid Public Key Encryption (HPKE). Customers encrypt request payloads using their HPKE public key, and CleverTap decrypts the payload using the matching private key. When your request indicates that you want an encrypted response, CleverTap uses its own HPKE public key to encrypt the outgoing payload.

Encryption works as an add-on layer. If encryption headers are not present, the API processes the request exactly as before.

## Supported Encryption Format

CleverTap supports HPKE with Diffie–Hellman key exchange and TINK-formatted public keysets.

All encrypted request bodies must be sent in raw binary form using the following header:

`Content-Type: application/octet-stream+hpke`

To receive an encrypted response, include:

`Accept: application/octet-stream+hpke`

# Encryption Application Rules

## Rules for Incoming Requests

CleverTap treats a request as encrypted only when the following header is present:

`Content-Type: application/octet-stream+hpke`

If this header is missing, the request is processed as a standard JSON request.

## Rules for Outgoing Responses

When the request includes `Accept: application/octet-stream+hpke`, CleverTap encrypts the response using its own published HPKE public key.

If this header is not present, the API returns a normal JSON response.

## Backward Compatibility Behavior

Encryption is optional. Encrypted and plaintext requests can coexist until you choose to enforce encryption for their account.

# Request and Response Lifecycle

1. The client encrypts the request payload using its HPKE public key.  
   The encrypted payload is sent as raw bytes with the HPKE content type.

2. CleverTap decrypts the payload using the customer’s registered HPKE keyset.

3. If the request includes the HPKE Accept header, CleverTap encrypts the response using CleverTap’s HPKE public key.

4. The client decrypts the ciphertext response using CleverTap’s published public key and its own private key.

# Key Management

Customers manage their own public keysets for request decryption and can rotate them securely.

## Customer Public Keyset Upload

When a public keyset is uploaded:

* CleverTap validates the keyset immediately.
* Only supported, well-formed HPKE public keysets are accepted.
* A validated keyset is stored securely and associated with the customer account.

Malformed or unsupported keys are rejected during the upload process.

## CleverTap Response-Encryption Keyset

CleverTap generates its response-encryption keyset using standard TINK formats.

* The public key is available for customers to download and use when decrypting encrypted responses.
* The private key is stored only in encrypted form within secure storage.

## Key Rotation Behavior

Key rotation is supported without downtime.

* At any given time, CleverTap retains two active keys for a customer:

  * Primary key
  * Previous key
* Decryption attempts always try the Primary key first, then fall back to the Previous key.

This behavior ensures that in-flight encrypted requests continue to succeed during rotation.

# Required Headers and Payload Formats

The table below describes the required headers and payload formats for each scenario.

There is a matrix of supported headers and formats:

| Scenario                                | Required Header                               | Payload Format      |
| --------------------------------------- | --------------------------------------------- | ------------------- |
| Encrypted request                       | `Content-Type: application/octet-stream+hpke` | Binary ciphertext   |
| Request that expects encrypted response | `Accept: application/octet-stream+hpke`       | Response ciphertext |
| Plaintext request                       | none                                          | JSON                |
| Plaintext response                      | no HPKE-specific Accept header                | JSON                |

All encrypted request bodies must be binary byte streams, not JSON and not Base64 encoded.

# Error Handling and Responses

If decryption fails, CleverTap returns structured error responses with clear error codes. Failures may result from:

* Invalid ciphertext
* Unsupported or missing encryption headers
* Decryption errors such as key mismatch
* Unsupported content types

Error messages never include sensitive data or decrypted content.

# Account-Level Enforcement

Customers that fully migrate to encrypted flows can choose to enforce encryption at account level.

When enforcement is enabled for an account:

* APIs reject all plaintext requests.
* Only requests using the HPKE headers are accepted.
* Responses remain encrypted when the HPKE Accept header is present.

Enforcement is configurable per customer account.

# Feature Enablement and Billing Behavior

This capability is controlled as follows:

* A feature flag must be enabled for the customer account.
* An associated billing entitlement must be active.

If the feature or entitlement is not enabled, the APIs continue to function normally without encryption.

# Security and Compliance Characteristics

PII Encryption for API enhances data protection for regulated environments and complements TLS by securing sensitive data at the payload layer.

The security properties include:

* Payload encryption using industry-standard HPKE
* Transport encryption using HTTPS/TLS
* Encrypted storage of all private keys
* No logging of sensitive data or decrypted content
* Preservation of existing authentication and authorization models

# API Behavior and Limitations

PII Encryption for API does not change any existing API constraints.

* API schemas remain the same.
* Payload size limits are unchanged.
* Batch size and ingestion limits remain unchanged.
* Rate limits and throttling continue to apply.
* Timeout behavior remains unchanged.

Encryption operates strictly as an additional security layer.

# Audit Logging for Key Operations

CleverTap logs non-sensitive key-related events for traceability, such as:

* Key uploads
* Validation outcomes
* Key rotations

No cryptographic material, decrypted content, or PII appears in logs.

# Non-Functional Expectations

This section outlines the operational guarantees, performance characteristics, and reliability expectations that apply to API-level encryption. The encryption layer functions as an extension of the existing API platform and does not introduce new constraints, SLAs, or usage rules.

## Performance and SLA Alignment

The encryption layer is designed to operate without affecting existing service performance or uptime guarantees.

* Performance remains in line with existing API SLAs.
* Encrypted traffic continues to use HTTPS/TLS in addition to HPKE.
* No additional SLA commitments exist specifically for encryption.

## Fair Usage Policy Alignment

The introduction of payload-level encryption does not modify or add to any existing usage policies.

* Existing fair usage policies continue to apply.
* No encryption-specific FUP rules are introduced.

## Reliability, RTO and RPO Alignment

The encryption layer follows the same reliability and disaster recovery objectives as the underlying API platform.

* Encryption shares the same RTO and RPO targets as the API platform.
* No separate disaster recovery expectations exist specifically for encryption.
