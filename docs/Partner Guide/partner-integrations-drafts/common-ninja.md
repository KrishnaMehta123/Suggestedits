---
title: Common Ninja
deprecated: false
hidden: true
metadata:
  robots: index
---
# Overview

[Common Ninja](https://www.commoninja.com/)  is an interactive content platform that enables marketers to create engaging widgets such as scratch cards, spin-the-wheel games, and quizzes. These widgets can be embedded in CleverTap campaigns to enhance engagement and reward distribution.

### Use Case Example

A retail brand is running a **Holiday Rewards Campaign** and wants to send customers an interactive email featuring a scratch card that reveals exclusive discounts or gifts. By integrating **Common Ninja** with **CleverTap** via **Zapier**, the marketing team can automate engagement tracking and view all scratch card interactions within CleverTap analytics.

This integration allows you to:

* **Deliver Gamified Campaigns**: Embed interactive scratch cards in CleverTap email campaigns.
* **Track Engagement Automatically**: Log scratch and reward events in CleverTap for real-time analytics.
* **Segment Users by Reward Data**: Use event data to drive personalized engagement workflows.

# Prerequisites for Integration

You’ll need the following to set up the integration:

* A **Common Ninja** account with a published scratch card
* An active **Zapier** account
* A **CleverTap** account with a valid **Account ID** and **Passcode**

# Integrate Common Ninja with CleverTap Using Zapier

The integration involves the following steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:common-ninja#create-a-passcode-on-the-clevertap-dashboard)
2. [Create and Configure Scratch Card in Common Ninja](doc:common-ninja#create-and-configure-scratch-card-in-common-ninja)
3. [Configure CleverTap Campaign](doc:common-ninja#configure-clevertap-campaign)
4. [Connect Common Ninja and CleverTap via Zapier](doc:common-ninja#connect-common-ninja-and-clevertap-via-zapier)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate API requests. Every API call must include **Account ID** and **Passcode** as request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create and Configure Scratch Card in Common Ninja

In our **Holiday Rewards Campaign** example, the marketing team creates a scratch card that reveals rewards such as _10% off coupons_, _free shipping_, or _gift vouchers_.

1. Log in to your **Common Ninja** dashboard.
2. Go to **Scratch Cards** and click **Create New**.
3. Customize the card’s design, text, and rewards for your promotion.
4. Click **Publish**.
5. Copy the **Email HTML Snippet** (for embedding in CleverTap Email Campaigns).

## Configure CleverTap Campaign

In this step, you’ll embed the scratch card into your CleverTap email campaign.

1. Go to **Campaigns → Email Campaigns** in CleverTap.
2. Create or edit an email campaign for the **Holiday Rewards** promotion.
3. Select **Custom HTML Template** under the _What_ section.
4. Paste the **Email HTML Snippet** from Common Ninja.
5. Click **Preview and Test** to verify the scratch card renders properly.
6. Do not publish yet; proceed to configure Zapier.

This ensures the email will display the scratch card, allowing recipients to interact directly within the email.

## Connect Common Ninja and CleverTap via Zapier

Zapier acts as a bridge between Common Ninja and CleverTap. Whenever a user interacts with the scratch card, Zapier captures the event and sends it to CleverTap.

Only the **Upload Event** action is supported for this integration.

1. Log in to your [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**.

2. **Set up Trigger**:

   * **App:** Common Ninja
   * **Trigger Event:** Scratch Completed or Reward Won
   * Connect your Common Ninja account and test the trigger.

3. **Set up Action**:

   * **App:** CleverTap
   * **Action:** Upload Event
   * Connect your CleverTap account using Account ID and Passcode.

4. **Map Fields**:

   | CleverTap Field  | Common Ninja Field           |
   | ---------------- | ---------------------------- |
   | User ID          | Email or unique identifier   |
   | Event Name       | Scratch Card Interaction     |
   | Creation Date    | Event timestamp              |
   | Event Properties | Reward type, card ID, source |

5. Test the Zap to confirm event data is sent to CleverTap.

6. Publish the Zap and then publish your CleverTap campaign.

In the example campaign, when users scratch the card and reveal their reward, CleverTap records an event (for example, `Reward_Won`) that can be used for segmentation or follow-up emails.

## Verify the Integration

1. Send a test email from CleverTap.
2. Interact with the scratch card in your inbox.
3. Verify that the event appears in the CleverTap **Events** dashboard under the configured name (for example, `Scratch_Reward_Won`).

In our **Holiday Rewards Campaign** example, the marketing manager can now view a report of all rewards claimed, identify high-value users, and retarget them with personalized offers.

# FAQs

### Can I use this integration for in-app or web popups?

Yes. You can use the **iFrame embed code** provided by Common Ninja to add the scratch card to CleverTap In-App or Web Popup campaigns.

### Can I update user profiles with reward data?

No. Common Ninja provides event-based triggers, so this integration only supports the **Upload Event** flow, not profile updates.

### What event data is sent to CleverTap?

Each event includes the user identifier, reward details, scratch card ID, and timestamp.

### Can I use this for marketing campaigns like holiday or referral programs?

Absolutely. This setup works perfectly for seasonal campaigns, user reactivation offers, or referral promotions — anywhere you want to track engagement with gamified content.

### Do I need support from CleverTap to enable this integration?

No. The integration uses publicly available Zapier and CleverTap APIs and can be set up without additional support.

### Can I customize event names?

Yes. You can rename the event in the Zapier setup (for example, `Scratch_Completed`, `Reward_Claimed`, or `Promo_Engagement`).
