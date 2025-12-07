---
title: Checklist
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

This guide walks you through the complete configuration and setup process for sending SMS through CleverTap. Whether you are using the Native SMS option or connecting your own provider, the following steps will ensure that your messaging infrastructure is compliant, functional, and test-ready.

## Setup Workflow

To successfully send SMS from CleverTap, follow the configuration steps below in sequence. These steps will help ensure regional compliance, correct integration with SMS gateways, and functional campaign delivery and tracking.

1. Choose your target countries.\
   Different regions enforce different regulatory requirements (e.g., 10DLC in the US, DLT in India). Confirm the documentation needed for each.

2. Select your SMS option.

   * **SMS Direct**: Fully managed by CleverTap.
   * **SMS Connect (BYOP)**: Configure using API credentials for your SMS vendor.\
     Tip: Confirm your provider supports callbacks for Delivery Receipts (DLR) and Mobile-Originated (MO) messages.

3. Register sender IDs and templates.

   * Supported sender types include long code, short code, TFN, and alphanumeric.
   * Template registration:

     * In India: Submit templates via the DLT portal.
     * In the US: Include templates during your 10DLC campaign registration.

4. Connect your provider.

   * Navigate to *Settings > Engage > Channels > SMS*.
   * Click **Add Provider**.
   * Enter API credentials (e.g., API key, Auth token, Sender ID).
   * Click **Test Connection** to validate integration.

5. Configure delivery and MO callbacks.

   * **DLR (Delivery Receipts)**: Captures message delivery states such as Sent, Delivered, and Failed.
   * **MO (Mobile-Originated)**: Captures user replies such as **STOP** and **HELP**.\
     Paste CleverTap's callback URLs into your SMS provider’s dashboard and confirm receipt with a test message.

6. Import or capture opt-in consent.

   * **Bulk Upload**: Use a CSV file with E.164-formatted phone numbers and opt-in timestamps.
   * **Real-Time Capture**: Fire a `sms_optin` event via the CleverTap SDK or API when users give consent.

7. Define opt-out and help keywords.

   * Add standard keywords like **STOP** (unsubscribe) and **HELP** (information).
   * Include regional variants such as **BAJA** (Spanish) and **SAIR** (Portuguese).
   * Configure keyword mappings in *Settings > Engage > Channels > SMS*.

8. Create and send a test campaign.

   * Build a test segment using internal or test phone numbers.
   * Compose a basic test message and send it.
   * Confirm delivery, character count, dynamic field rendering, and reply behavior.

9. Validate two-way interactions.

   * Reply **STOP**: User is unsubscribed and reflected in their profile.
   * Reply **HELP**: An auto-response message is sent.
   * Custom replies (e.g., surveys): Logged as user events within CleverTap.

10. Monitor campaign performance.

    * Navigate to *Analytics > SMS Stats*.
    * Review delivery metrics including Sent, Delivered, Failed, and Replies.
    * Use the **Campaign ID** to track performance and A/B test variations.
