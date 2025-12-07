---
title: Message Archiving
excerpt: >-
  Learn to archive outgoing messages across different channels in real-time to
  your AWS S3, Azure bucket or GCP bucket using CleverTap's Message Archiving
  feature.
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

CleverTap’s Message Archiving feature stores a copy of each outgoing message sent through campaigns or journeys to your AWS S3 bucket, Azure Blob Storage, or GCP bucket, such as a push notification, email, SMS, or WhatsApp message. Storing copies of outgoing messages from campaigns and journeys across multiple channels in real time provides evidence of compliance. It also allows access to archived communication for compliance, audit, or customer support.

> 📘 Enable Message Archiving
>
> The feature is available as a paid add-on. To enable this feature, contact your Customer Success Manager or the [CleverTap Support.](https://help.clevertap.com/hc/en-us/requests/new).

Some of the key benefits of archiving your messages are:

* **Audit Readiness** Maintains a comprehensive record of all user communications, ensuring adherence to regulatory compliance.
* **Real-Time Archiving:** Archives messages in real-time with minimal impact on daily operations.
* **Low Maintenance:** Requires less ongoing maintenance, releasing resources for other tasks.

# Supported Channels

Currently, Message Archiving is available for the following channels:

* Email
* Push notifications
* SMS
* WhatsApp

# Introduction to Message Archiving

When the Message Archiving feature is enabled, CleverTap will:

1. Archive outgoing messages to your AWS S3 bucket, Azure Blob Storage, or GCP bucket in real-time.
2. Send messages through selected channels as part of campaigns and journeys.

> 🚧 Message Delivery Lag
>
> Enabling this feature may introduce additional latency, as the archiving is performed before message delivery to ensure accuracy. The lag is dependent on the storage provider latencies and rate limits.

# File Structure

The archived message files on the AWS contain a JSON payload.

## Create File Structure and Path

The archived messages are saved in your AWS S3 bucket, Azure Blob Storage, or GCP bucket using a specific key structure, helping organize and retrieve the files efficiently. The general structure of the file path is as follows:

```
sent_messages/<channel>/<yyyymm>/<campaign_id>/<user_id>/message_id.json.lz4

where:
<*> = folder
<yyyymm> = year, month // batchId(<yyyymmdd> year, month, day) from the message
<channel> = Push OR Sms OR Email or WhatsApp 
<user_id> = MD5 encoded data of Device Identity if exists, else, Customer Identity for Push, Mobile Number in CountryCode format for Sms & Whatsapp, EmailId for Email channel
message_id.json.lz4 is a lz4 compressed file representing one message. // support lz4 compression

```

An example file path may look like this:

```
sent_messages/WhatsApp/202409/1725435360/6e6d748a7cc752fbe4f72c777cc50a74/49482d489b871510eeff7db9a8ab443248ad1ea596e5108e02d16ab5b2ea47db.json.lz4
```

## Sample JSON Payloads

The archived files on the AWS contain a JSON payload representing the final message sent to the user. Here is an example of the JSON structure:

```json Push
{
  "version" : 1, // numerical version of the json structure.
  "to": "frfsgvrwe:APfdsafsgdfsgghfgfgjkhfsfgdhjhbvcvnetry767456fxsasdf", // platformId or pushToken.
  "payload": JsonOfEntirePushPayload,
  "platform": "iOS" or "Android",
  "sent_at": 1722443282680, // Message Archiving epoch in millis.
  "message_id": "57040f2b01ac851c2b2538e817983d1e2e6cdd01cc5e20740550729525a3f345", // unique hash per message.
  "campaign_id": 1722529032, // the campaign ID is unique to each campaign, will always exist.
  "campaign_name": "Flat Offer Sale Campaign", // the campaign Name for current campaign, will always exist.
  "user_id": 45142169, // CleverTap internal Device Identity if exists, else, Customer Identity.
  "journey_id": 2450, // may not be available, exists only if this campaign is a journey node.
  "journey_node_id": 1, // may not be available, exists only if campaign is a journey node.
  "journey_name": "Flat Offer Sale Journey", // may not be available, exists only if campaign is a journey node.
}
```
```json Email
{
  "version" : 1, // numerical version of the json structure.
  "to": ToAddress, // ("customer@example.com").
  "subject": SubjectLine, // ("20% off coupon inside!").
  "from_name": DisplayName, // ("CleverTap").
  "from_address": FromAddress, // ("no-reply@clevertap.com").
  "cc": , // List of CC's if available.
  "bcc": , // List of BCC's if available.
  "html_body": HtmlBody,
  "plaintext_body": PlainTextBody,
  "amp_body": AMPEmailBody, // will only be available if the email has ampBody.
  "headers": , // headers for the email.
  "sent_at": 1722443282680, // Message Archiving epoch in millis.
  "message_id": "5fae1e791db5f2e61ef39fb34a853aa6e9c8847e78e2766c888d10ee65221abc", // unique hash per message.
  "campaign_id": 1722529032, // the campaign ID is unique to each campaign, will always exist.
  "campaign_name": "Flat Offer Sale Campaign", // the campaign Name for current campaign, will always exist.
  "user_id": 45142169, // CleverTap internal Device Identity if exists, else, Customer Identity.
  "journey_id": 2450, // may not be available, exists only if this campaign is a journey node.
  "journey_node_id": 1, // may not be available, exists only if campaign is a journey node.
  "journey_name": "Flat Offer Sale Journey", // may not be available, exists only if campaign is a journey node.
}
```
```json SMS
{
  "version" : 1, // numerical version of the json structure.
  "to": PhoneNumber, // ("15555555555").
  "body": Body, // ("Hi there!").
  "provider": "twilio", // StringOfProviderName.
  "sent_at": 1722443282680, // Message Archiving epoch in millis.
  "message_id": "9f8c76ccdaf0895515f813af702670324d996296788652b50b3475d6fe6e719a", // unique hash per message.
  "campaign_id": 1722529032, // the campaign ID is unique to each campaign, will always exist.
  "campaign_name": "Flat Offer Sale Campaign", // the campaign Name for current campaign, will always exist.
  "user_id": 45142169, // CleverTap internal Device Identity if exists, else, Customer Identity.
  "journey_id": 2450, // may not be available, exists only if this campaign is a journey node.
  "journey_node_id": 1, // may not be available, exists only if campaign is a journey node.
  "journey_name": "Flat Offer Sale Journey", // may not be available, exists only if campaign is a journey node.
}
```
```json WhatsApp
{
  "version" : 1, // numerical version of the json structure.
  "to": PhoneNumber, // ("15555555555").
  "body": Body, // ("Hi there!").
  "provider": "twilio", // StringOfProviderName.
  "sent_at": 1722443282680, // Message Archiving epoch in millis.
  "message_id": "9f8c76ccdaf0895515f813af702670324d996296788652b50b3475d6fe6e719a", // unique hash per message.
  "campaign_id": 1722529032, // the campaign ID is unique to each campaign, will always exist.
  "campaign_name": "Flat Offer Sale Campaign", // the campaign Name for current campaign, will always exist.
  "user_id": 45142169, // CleverTap internal Device Identity if exists, else, Customer Identity.
  "journey_id": 2450, // may not be available, exists only if this campaign is a journey node.
  "journey_node_id": 1, // may not be available, exists only if campaign is a journey node.
  "journey_name": "Flat Offer Sale Journey", // may not be available, exists only if campaign is a journey node.
}
```

## Browse Archived Message From AWS S3 Bucket

The following image shows the steps to browse the archived messages on the AWS S3 bucket:

<Image alt="Sample Message Archive" align="center" border={true} src="https://files.readme.io/6dbc6e767772b915a0d9db56f9a4484df2c91b36c829f06d6f781d2ad4721e99-AWS_Slow.gif">
  Sample Message Archive
</Image>

# Set Up Message Archiving

## Prerequisites

Before setting up Message Archiving, check that you have the following:

* An active CleverTap account.
* An AWS S3 bucket, Azure Blob Storage, or GCP bucket in the same region as your CleverTap account region.

## Set Up Message Archiving

To set up message archiving, perform the following steps: 

1. **Configure AWS S3 bucket, Azure Blob Storage, or GCP bucket on CleverTap dashboard**: Provide the necessary details for your AWS S3 bucket, including the bucket name and region. For more information, refer to [Configure AWS S3 Bucket on CleverTap Dashboard](doc:data-export-to-aws-s3#configure-s3-bucket-details-on-clevertap-dashboard), [Configure Azure Blob Storage](https://docs.clevertap.com/docs/microsoft-azure) or [Configure GCP Bucket on CleverTap Dashboard.](https://staging.docs.user.clevertap.net/v5.0/docs/data-export-to-gcp#configure-clevertap-dashboard)
2. **Configure Data Retention Policy**: You must set up the data retention policy for your AWS S3 bucket according to your organizational needs directly in the AWS S3 console. 

For more information and detailed configuration steps, refer to [Data Export to AWS S3](https://docs.clevertap.com/docs/data-export-to-aws-s3#create-an-aws-s3-bucket), [Data Export to Azure](https://docs.clevertap.com/docs/microsoft-azure#create-a-new-data-export), or [Data Export to GCP](https://staging.docs.user.clevertap.net/v5.0/docs/data-export-to-gcp#create-a-new-data-export).

# Security and Data Protection

Clevertap is committed to safeguarding your data. We ensure the protection of your data by implementing the following measures:

* **Data in Transit:** All data is transmitted using the HTTPS protocol, ensuring secure data transfer between CleverTap and your AWS S3 bucket, Azure Storage Blob, or GCP bucket.
* **Data at Rest:** The security of data at rest within the AWS S3 bucket, Azure Storage Blob, or GCP bucket is the customer's responsibility. This includes ensuring that proper encryption and access controls are in place.

# Frequently Asked Questions (FAQs)

Explore concise troubleshooting tips and FAQs for Messaging Archival in this section.

The following information provides useful troubleshooting tips and common questions about Message Archiving. 

#### **Q: Is there a user interface for Message Archiving?**

A: No, the Message Archiving feature operates without a user interface. Once enabled, it seamlessly archives messages to your AWS S3 bucket, Azure Storage Blob, or GCP bucket. We will provide one in the future. 

#### **Q: How long is the data stored?**

A: You define the data retention policy within your AWS S3 bucket, Azure Storage Blo,b or GCP bucket settings.

#### **Q: Who bears the cost of storage?**

A: The customer bears all storage and data transfer costs associated with their AWS S3 bucket, Azure Storage Blob, or GCP bucket.

#### **Q: Does archiving happen in real-time?**

A: Yes, message archiving occurs in real-time, ensuring that all communications are promptly saved.

#### **Q: What happens if my AWS credentials are invalid?**

A: If your AWS credentials become invalid, CleverTap cannot archive messages to your AWS S3 bucket or Azure Storage Blob, and no further campaign messages will be sent to your users. This is to ensure that every message that is sent out is archived first.

#### **Q: How are retries handled?**

A: If the bucket is unreachable, we will retry up to three times for AWS errors (such as AccessDenied).  CleverTap handles the AWS S3 rate limit errors. 

#### **Q: What happens if archiving fails ?**

If the archiving fails after multiple retries, messages are marked as  *Failed to Archive Message*.

<Image alt="Failed to archive message" align="center" border={true} src="https://files.readme.io/4b8eca3f061741697bca2f07b0307f88efd5ee2f3b5600a1f70bbe72865356d1-image.png">
  Failed to archive message
</Image>

#### **Q: Why does my archive*sent\_at* timestamp differ slightly from the actual send time?**

A: The message is archived just before it is sent to the end user, due to which slight delays can occur. This may lead to minor differences in timestamps.
