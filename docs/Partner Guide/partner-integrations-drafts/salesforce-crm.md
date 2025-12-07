---
title: Salesforce
excerpt: >-
  Learn how integrating Salesforce with CleverTap bridges structured CRM data
  with real-time engagement, enabling personalized experiences and lifecycle
  automation at scale.
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

Salesforce is a leading Customer Relationship Management (CRM) platform that manages leads, contacts, accounts, opportunities, and support activities across sales, marketing, and service functions. It centralizes structured customer data and tracks critical lifecycle interactions. (@Parth: Should we add a hyperlink to the Salesforce website like we do for all the integrations docs??)

CleverTap’s native integration with Salesforce enables organizations to unify structured CRM data with behavioral insights captured across digital touchpoints. The integration supports seamless data import and export, allowing teams to build rich user profiles, trigger personalized campaigns, and align messaging with sales activity in real time.

This bi-directional sync allows CRM records and engagement behavior to inform each other, empowering marketing, sales, and support teams to deliver more contextual and timely customer experiences.

# Use Cases

Integrating CleverTap with Salesforce enables a wide range of cross-functional use cases:

- **Unify Customer Profiles**  
  Bring in Salesforce records such as contacts, leads, accounts, or opportunities as profile data in CleverTap to create a centralized view of your customer.

- **Trigger Campaigns from CRM Events**  
  Use events and status updates, such as task creation, opportunity movement, or case resolution, to trigger real-time journeys and messaging in CleverTap.

- **Sync Behavioral Data Back to Salesforce**  
  Export user activity and campaign engagement from CleverTap into Salesforce to help sales teams prioritize outreach and improve conversion tracking.

- **Segment Based on CRM Attributes**  
  Build dynamic audience segments in CleverTap using Salesforce attributes such as lead stage, industry, or deal value.

- **Backfill Historical Records**  
  Import historical Salesforce data, such as leads, events, and cases, to enrich user profiles in CleverTap and inform segmentation, targeting, and analytics.

- **Automate Lead Enrichment**  
  Use CleverTap campaigns to capture user signals (for example, NPS, Feedback survey) and push them into Salesforce objects for sales or success follow-up.

# Map Fields for Import and Define Payload for Export

To enable seamless data exchange between Salesforce and CleverTap, you must configure field mappings for imports and define structured payloads for webhook-based exports. These configurations ensure that CRM records are properly ingested into CleverTap and that outgoing data is delivered to Salesforce in the expected format.

### For Import

Map Salesforce object fields, such as _Email_, _Lead ID_, or _Opportunity Status_, to profile attributes or event parameters in CleverTap. This ensures that structured CRM records are accurately ingested as **profiles** or **events** within the CleverTap platform.

- For **Profile Imports**, map identifiers and attributes from objects such as _Lead_, _Contact_, or _Account_ to CleverTap profile fields.
- For **Event Imports**, map lifecycle activities (for example, _Opportunity Created_, _Case Closed_) to event names and properties in CleverTap.

For step-by-step guidance, refer to the [Import Guide](https://staging.docs.user.clevertap.net/docs/salesforce-crm-import).

### For Export

When exporting data from CleverTap to Salesforce via webhook, define a custom JSON payload that matches the expected structure of your Salesforce Apex REST endpoint.

- Use dynamic fields such as `email`, `leadScore`, or `city` to populate the POST body. These values are typically drawn from user profile attributes or event properties within CleverTap.
- Ensure that the destination object in Salesforce has matching fields to receive this data, typically configured using a custom object and Apex class.

For more information about configuring exports, refer to the [Export Guide](https://staging.docs.user.clevertap.net/docs/salesforce-crm-export).