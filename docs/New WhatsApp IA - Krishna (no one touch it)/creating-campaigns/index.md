---
title: Getting Started with Campaigns
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
# Getting Started with WhatsApp Campaigns

This document outlines the foundational steps and requirements for creating and executing WhatsApp campaigns in CleverTap. WhatsApp campaigns enable businesses to engage users through personalized, time-sensitive, and interactive messages via the WhatsApp Business Platform.

## Overview

A WhatsApp campaign in CleverTap is created through a structured, step-by-step process within the campaign builder. Each stage of the campaign serves a specific purpose in defining, targeting, and scheduling user communication.

The campaign creation flow includes the following steps:

1. Create a new campaign and select WhatsApp as the messaging channel.
2. Configure initial campaign setup, including service provider and qualification criteria.
3. Define the target audience using behavioral or property-based segmentation.
4. Select the message delivery type.
5. Compose the campaign message using an approved WhatsApp template.
6. Set the campaign schedule, including start time, delay, and delivery conditions.
7. Publish the campaign.

## When to Use WhatsApp Campaigns

WhatsApp campaigns are suitable for the following use cases:

* Transactional notifications such as order confirmations, payment alerts, and booking updates.
* Promotional offers, including flash sales, discount codes, and product launches.
* Behavioral triggers, for example, sending messages based on user activity or inactivity.
* Re-engagement campaigns targeted at inactive users or those requiring follow-up.

WhatsApp is an effective channel for high-engagement communication due to its delivery reliability and user reach.

## Prerequisites

Before initiating a WhatsApp campaign, ensure that the following components are in place:

* **WhatsApp Templates**\
  At least one approved WhatsApp message template must be available. Templates must comply with Meta’s policies. If using CleverTap as the Business Service Provider (BSP), templates can be created directly in the CleverTap dashboard. For external BSPs, templates must be created and approved via the vendor’s dashboard, then replicated in CleverTap.

* **User Segments**\
  Segments should be defined based on user behavior or properties. These segments can be predefined or created during campaign setup. For more information, refer to the Segments documentation.

* **WhatsApp Service Provider Configuration**\
  A valid BSP configuration is required. CleverTap supports two types of integration:

  * WhatsApp Direct (CleverTap BSP)
  * WhatsApp Connect (External BSP)

  The appropriate provider must be set up and connected to a verified WhatsApp Business Account (WABA).

## Next Steps

Once all prerequisites are met, proceed with the campaign setup using the following documents:

1. [Create a New WhatsApp Campaign](doc:create-whatsapp-campaign)
2. [Configure Initial Setup](doc:start-setup-whatsapp-campaign)
3. [Define Target Audience](doc:define-target-whatsapp)
4. [Select Message Type](doc:message-types-whatsapp)
5. [Compose Message Content](doc:define-message-content-whatsapp)
6. [Schedule the Campaign](doc:schedule-whatsapp-campaign)
7. [Publish and Monitor Campaign](doc:publish-whatsapp-campaign)
