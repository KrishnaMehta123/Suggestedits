---
title: Common Ninja
excerpt: Workflow Automation
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

[Common Ninja](https://www.commoninja.com/)  is an interactive content platform that enables marketers to create engaging widgets such as scratch cards, spin-the-wheel games, and quizzes. These widgets can be embedded in CleverTap campaigns to enhance engagement and reward distribution.

### Use Case Example

A retail brand is running a Holiday Rewards Campaign and wants to send customers an interactive email featuring a scratch card that reveals exclusive discounts or gifts. By integrating Common Ninja with CleverTap via Zapier, the marketing team can automate engagement tracking and view all scratch card interactions within CleverTap analytics.

This integration allows you to:

* **Deliver Gamified Campaigns**: Embed interactive scratch cards in CleverTap email campaigns.
* **Track Engagement Automatically**: Log scratch and reward events in CleverTap for real-time analytics.
* **Segment Users by Reward Data**: Use event data to drive personalized engagement workflows.

# Prerequisites for Integration

The following are the prerequisites for this integration:

* A Common Ninja account with a published scratch card
* An active Zapier account
* A CleverTap account with a valid **Account ID** and **Passcode**

# Integrate Common Ninja with CleverTap

The integration involves the following steps:

1. [Create a Passcode on the CleverTap Dashboard](doc:common-ninja#create-a-passcode-on-the-clevertap-dashboard)
2. [Create and Configure Scratch Card in Common Ninja](doc:common-ninja#create-and-configure-scratch-card-in-common-ninja)
3. [Configure CleverTap Campaign](doc:common-ninja#configure-clevertap-campaign)
4. [Connect Common Ninja and CleverTap via Zapier](doc:common-ninja#connect-common-ninja-and-clevertap-via-zapier)

## Create a Passcode on the CleverTap Dashboard

CleverTap uses a header-based authentication model to authenticate requests to the API. Every CleverTap API request must include the Account ID and Passcode as the request headers. To create a passcode, refer to [Create Account Passcode](https://developer.clevertap.com/docs/authentication#create-account-passcode).

## Create and Configure Scratch Card in Common Ninja

In our Holiday Rewards Campaign example, the marketing team creates a scratch card that reveals rewards such as _10% off coupons_, _free shipping_, or _gift vouchers_. To do so, perform the following steps:

1. In Common Ninja dashboard, go to _Content_ and select _Scratch Image_.
2. Customize the card’s design, text, and rewards for your promotion. Refer to [Scratch Card](https://help.commoninja.com/hc/en-us/articles/21959994228125-How-to-Set-Up-and-Use-Scratch-Card-Modes).

<Image align="center" alt="Create and Configure Scratch Card" border={true} caption="Create and Configure Scratch Card" src="https://files.readme.io/d04128fbb70e12208ebccb1a342fc65571fd1b4aca5b95d4781b89acecc2a7a8-image.png" width="75% " />

3. Click **Publish**.
4. Click **Copy Code** to copy the Email **HTML** Snippet (for embedding in CleverTap Email Campaigns).

<Image align="center" alt="Copy HTML Snippet" border={true} caption="Copy HTML Snippet" src="https://files.readme.io/3f96ef2e04f74df05476c494302381c200beaf7a8799076b0e13bca7f6a7b908-image.png" width="75% " />

## Configure CleverTap Campaign

The Common Ninja Scratch Card can be used in any CleverTap messaging channel that supports HTML or image URLs. While this guide includes an example for an email campaign, you can also use Common Ninja Scratch Card content in [Push Notification](doc:create-message-push), [In-App campaigns](doc:create-message-in-app), and other CleverTap messaging channels that support dynamic visuals.

To integrate a Common Ninja Scratch Card into your CleverTap Email campaign, perform the following steps:

1. Go to the _Campaigns_ page, click **+ Campaign**, and select _Email_ from the list of messaging channels.
2. Click **Go to Editor** under the _What_ section.
   1. Select a _Basic Template_ or _Saved Template_.
   2. Switch to **Source** mode in the email editor to edit the HTML code of the email body.
3. Paste the HTML Snippet copied in _step 4_ of [Create and Configure Scratch Card in Common Ninja](doc:common-ninja#create-and-configure-scratch-card-in-common-ninja) inside the `<body>` tag.

<Image align="center" alt="Insert the HTML Code Snippet" border={true} caption="Insert the HTML Code Snippet" src="https://files.readme.io/82a52d9f81856a7df6178eae5e9d585735b7aef4410cd90c67a1250f316d9bc3-2025-05-11_21-52-41_1.gif" width="75% " />

4. Send a test email to verify that the integration functions correctly.

<Image align="center" alt="Test Email" border={true} caption="Test Email" src="https://files.readme.io/c99dd845be09e5a1793a2e42bdb126202445c00de0d112b5f05a8e0895b4a659-image.png" width="75% " />

5. Publish the campaign only after configuring the Zap as an Upload Event.

## Connect Common Ninja and CleverTap via Zapier

Zapier acts as a bridge between Common Ninja and CleverTap. Whenever a user interacts with the scratch card, Zapier captures the event and sends it to CleverTap.

Only the **Upload Event** action is supported for this integration.

1. Log in to the [Zapier dashboard](https://zapier.com/app/home) and click **+ Create Zap**. Zapier can connect different applications such as Common Ninja.

<Image align="center" alt="Create a Zap on Zapier Dashboard" border={true} caption="Create a Zap on Zapier Dashboard" src="https://files.readme.io/81d24bf2bb62b05403da728cf54af63674995a31f21a25485fac5d5a980c24d4-image.png" width="75% " />

2. **Set up a Trigger**: To do so, perform the following steps:  
   1. Select Common Ninja from the App section.
   2. Select _Scratch Card Submission_ as the Trigger Event.
   3. Connect your Common Ninja account.

<Image align="center" alt="Set up a Trigger" border={true} caption="Set up a Trigger" src="https://files.readme.io/446a4144c0fe8abbb1c12461d2f3de6d9f84c14f1b05f77328a300ffb9eb0106-2026-01-05_11-40-26_1.gif" width="75% " />

3. Click **Test Trigger** to confirm Zapier pulls the most recent responses.
4. **Set up the Action**:
   1. Select _CleverTap_ from the App dropdown.
   2. Select _Upload Event_ as the Action Event. This ensures that each submission is recorded as an event in CleverTap.
   3. Connect your CleverTap account using the Account ID and Passcode obtained in [Create a Passcode on the CleverTap Dashboard](doc:common-ninja#create-a-passcode-on-the-clevertap-dashboard).

<Image align="center" alt="Set up the Action" border={true} caption="Set up the Action" src="https://files.readme.io/439bce205fd7cd04599cb29160b8db2c0bbd20865a620bf3beefdbb8bfa008bb-2026-01-05_11-50-36_1.gif" width="65% " />

5. **_Configure the Action_**: Map Common Ninja data fields to CleverTap fields as follows:

| CleverTap Field  | Common Ninja Field                 |
| :--------------- | :--------------------------------- |
| User ID          | Email or unique identifier         |
| Object ID        | Leave blank if User ID is provided |
| Event Name       | Scratch Card Interaction           |
| Creation Date    | Event timestamp                    |
| Event Properties | Reward type, card ID, source       |

> 🚧 Mapping Identity and Object ID
>
> You can keep the Identity field blank if you provide an Object ID, and vice versa.

6. Click **Continue**, then click **Test Step** to validate that the event is sent successfully to CleverTap.
7. Click **Publish**. Also publish the campaign created in [Configure CleverTap Campaign](doc:common-ninja#configure-clevertap-campaign).

In the example campaign, when users scratch the card and reveal their reward, CleverTap records an event (for example, `Reward_Won`) that can be used for segmentation or follow-up emails.

# FAQs

### Can I use this integration for In-App or web popups?

Yes. You can use the **iFrame embed code** provided by Common Ninja to add the scratch card to CleverTap In-App or Web Popup campaigns.

### Can I update user profiles with reward data?

No. Common Ninja provides event-based triggers, so this integration only supports the **Upload Event** flow, not profile updates.

### What event data is sent to CleverTap?

Each event includes the user identifier, reward details, scratch card ID, and timestamp.

### Can I use this for marketing campaigns like holiday or referral programs?

Absolutely. This setup works perfectly for seasonal campaigns, user reactivation offers, or referral promotions — anywhere you want to track engagement with gamified content.

### Can I customize event names?

Yes. You can rename the event in the Zapier setup (for example, `Scratch_Completed`, `Reward_Claimed`, or `Promo_Engagement`).