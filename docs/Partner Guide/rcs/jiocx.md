---
title: JioCX
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

[JioCX](https://www.jiocx.com/) enables businesses to deliver rich, interactive messages with branded content and multimedia. When integrated with CleverTap, it streamlines RCS campaigns, supports message tracking, and automates workflows for personalized engagement. SMS fallback ensures reliable delivery, enhancing customer communication and optimizing messaging strategies.

> 📘 Note
>
> JioCX RCS is CleverTap's Direct RCS Partner. If you want to enable and use RCS messaging via CleverTap, please contact your Customer Account Manager for more details on activation and setup.

# Prerequisites

Before you can start using **JioCX RCS with CleverTap** at scale, ensure the following prerequisites are completed:

## RCS Agent Onboarding

To use RCS via CleverTap, you must have an **RCS Agent registered with JioCX**. The onboarding process includes:

* Registering your business with JioCX as an RCS sender.
* Submitting brand details and receiving approval from mobile carriers.
* Completing the agent verification process with JioCX.

## API Configuration

Set up the necessary API parameters in CleverTap to integrate with JioCX. You will need the **Base API URL**, an **API Key**, and the **Incoming Message Callback URL**.

### Base API URL

To enable seamless integration between CleverTap and JioCX for sending and managing RCS messages, configure the following:

* **Request Type**: `POST`.
* **HTTPS Endpoint (Base API URL)**: This is the primary endpoint for JioCX’s RCS API. You can find it by logging into your Infobip account and navigating to _Developer Tools > Base API URL_. Copy and paste this URL into CleverTap during provider setup. For more details, refer to the [JioCX documentation](https://www.infobip.com/docs/essentials/api-essentials/base-url).

<Image align="center" alt="API Base URL" border={true} caption="API Base URL (JITHENDRA TO GIVE)" src="https://files.readme.io/3557c6a28a862787b37a6971ec25037e53de8ec77d7eba9dbb12a70ba2dd3635-infobip_api_base_url.png" width="75% " />

### API Key

This key is used for authentication and can be found under _Developer Tools > API Key_ in the JioCX dashboard. If not already created, generate a new [API Key](https://www.infobip.com/docs/essentials/api-essentials/api-authorization) with RCS & SMS messaging scopes. Copy and paste this key into CleverTap to enable secure communication between platforms.\ <br />

<Image align="center" alt="API Key - Infobip" border={true} caption="API Key - Infobip" src="https://files.readme.io/a058cc2a58601c28c887c170d12e4d642a48f2522d504526e35d24448f64837b-image_26.png" width="60% " />

### Inbound Message Callback URL

The Incoming Message Callback URL is generated automatically after saving provider settings in CleverTap. To configure this in JioCX:

1. Log in to the JioCX portal. Navigate to _Channels & Numbers → Channels → RCS_.
2. Click on **Senders**, select the sender you want to configure, and click _More Actions → Edit Configuration_.
3. Under **Forwarding Action**, select _Forward to HTTP_.
4. In the **Callback URL** field, paste the CleverTap Incoming Message Callback URL.
5. Under **Renderer**, select **MO_OTT_MSISDN**, then click **Save**.

<Image align="center" alt="Inbound Message Callback URL - Infobip dashboard" border={true} caption="Inbound Message Callback URL - Infobip" src="https://files.readme.io/4af8cb8ecb3a54ffef469a53cc285bd9887be59dcf773bd7191cc16a04742f7f-image_38.png" />

> 📘 Note
>
> Ensure that the **MO_OTT_MSISDN** option is selected, as it is mandatory for proper integration. This format is required to ensure that incoming messages are correctly processed by CleverTap.

<Image align="center" alt="Inbound Message Callback URL Renderer - Infobip" border={true} caption="Inbound Message Callback URL Renderer - Infobip" src="https://files.readme.io/b9a493f95578fd66d4986a3741916d44d204424acfe34a4252537356ff0e078b-image_41.png" width="65% " />

## RCS Setup in CleverTap

Once your RCS Agent is onboarded, configure RCS settings in CleverTap:

* Navigate to _Settings > Channels > SMS Direct_ in your CleverTap dashboard.
* Select **JioCX RCS** as the provider and enter the required credentials.
* Configure message templates, sender IDs, and any additional settings needed for your use case.

## RCS Agent Go-Live

After setup, your RCS Agent will go live following a brief testing phase:

* JioCX and CleverTap will validate message delivery and subscriber management flows.
* Once testing is successful, your RCS Agent will be fully activated for sending messages.

# Set Up JioCX on CleverTap Dashboard

To successfully integrate JioCX with CleverTap, follow the steps below to configure your RCS settings and ensure seamless communication between the two platforms.

1. Go to _Settings > Channels > SMS > SMS Direct_ and click **+ Add Provider**

<Image align="center" alt="SMS Provider - Infobip" border={true} caption="SMS Provider - Infobip" src="https://files.readme.io/5dbb8ec41b13cf6f4f34da902d7908703fc5414637cc6f7b794270d32834bfbd-Infobip_2.png" />

2. Add the following details:

   <Image align="center" alt="Provider Configuration - Infobip" border={true} caption="Provider Configuration - Infobip" src="https://files.readme.io/5d876c2c438af077e11eef06c59e285cf83a9094d4ae5153731f4cdf620cceab-AD_4nXfti6hHxZz0UhwpxhYm7fU9CMqhsCBtgzhKDBbA3wEAe8peJEWvpwPfGwBFPJB73Ukx8RCOX3Wvbnn1j2DgZCD0sz59O2ba_9QnZ4KZEs2npiaO00W-EkDq.png" />

* ###### **Provider**:
  Select JioCX RCS Provider from the drop-down menu.
* ###### **Nickname**
  A customizable label for your JioCX RCS integration. This name helps you easily identify and manage the integration within the CleverTap dashboard, making it convenient to distinguish between multiple configurations.
* ###### **RCS Sender ID**
  The RCS Sender ID is the unique identifier of your RCS Agent (business profile) used to send messages. It’s what recipients see as the sender of your RCS messages, typically a brand name or number associated with your business. This helps build recognition and trust with your audience. Depending on your region, the Sender ID may be provisioned by JioCX or your telecom partner.
* ###### Inbound Message Callback URL:
  Paste the CleverTap-generated Incoming Message Callback URL here. This URL is used by JioCX to forward user replies back to CleverTap. Refer to the [Inbound Message Callback URL](doc:infobip-rcs#inbound-message-callback-url) section for setup instructions.
* ###### Delivery Report Callback URL:
  The Delivery Report Callback URL is where JioCX sends the delivery status updates for the RCS messages you’ve sent. It provides feedback on whether each message was successfully delivered, failed, or queued, enabling real-time tracking of your RCS campaigns and does not require any manual configuration on your end.
* ###### **Request Type and HTTP Endpoint**

  Enter the Base API URL retrieved from your JioCX dashboard. This is required to establish the connection between CleverTap and JioCX. Refer to the [Base API URL](doc:infobip-rcs#base-api-url) configuration steps for more details.
* ###### **API Key**
  Paste the API Key you generated in your JioCX account under _Developer Tools > API Key_. This key authorizes CleverTap to send RCS messages via JioCX. Refer to the [API Key](doc:infobip-rcs#api-key) configuration steps for more details.
* ###### SMS Fallback:

  SMS fallback ensures message delivery when RCS messages fail due to factors like device incompatibility, lack of internet access, or carrier restrictions. If the recipient’s device doesn’t support RCS or is offline, the message is automatically sent as an SMS to maintain uninterrupted communication.

  To enable SMS fallback in the CleverTap–JioCX integration, the following conditions and configurations apply:

  * **Required Configuration in CleverTap**:
    1. **SMS Sender ID**:  Required if SMS fallback is enabled. This is the sender ID/number used to send SMS messages.
    2. **Enable for India**: Select this checkbox if SMS fallback applies to recipients in India to comply with local messaging regulations.
    3. **Principal Entity ID**: For businesses sending SMS and RCS messages to users in India, DLT (Distributed Ledger Technology) registration is required as per TRAI regulations. Principal Entity ID (PE ID) is a unique identifier assigned to businesses registered on the DLT platform.
       > 📘 Note
       >
       > * If using CleverTap as an RCS provider, you must purchase SMS from CleverTap to enable fallback.
       > * If using a different SMS provider, configure SMS fallback via CleverTap Journeys.
* ###### Enable Provider Click Tracking:

  This feature allows you to track clicks on links within your RCS messages, providing insights into user engagement.

  * **Default Domain**: If selected, this option uses JioCX's default domain for link tracking. It automatically generates trackable links for the RCS messages sent through the JioCX platform.
  * **Custom Domain**: This option allows you to use your own domain for link tracking, ensuring your RCS messages reflect your brand while still enabling you to track user interactions. Configure and verify your [custom domain ](https://www.infobip.com/docs/url-shortening/register-custom-domain)on the JioCX dashboard to get started. Once verified, you can use it within CleverTap to send your campaigns.

> 🚧 JioCX Click Tracking Integration
>
> CleverTap offers native click tracking for RCS campaigns, so using the provider’s click tracking is optional. If you choose to enable JioCX’s Provider Click Tracking, all URLs in your RCS messages will be shortened and tracked by JioCX’s system.
>
> **Important**: Avoid enabling both CleverTap’s and JioCX's click tracking simultaneously. Doing so may result in duplicate URL wrapping, inconsistent or inflated click metric, or double event tracking
>
> For accurate and consistent analytics, we recommend using only one click-tracking system per campaign.

<Image align="center" alt="URL Shortener for Custom Domain - Infobip" border={true} caption="URL Shortener for Custom Domain - Infobip" src="https://files.readme.io/c04cf9f269db8733c458e8cc5bf4a4bad431bc2ef106ad81bdd278360d9a2d79-image_28.png" />

* ###### Set JioCX as Default Service Provider:
  By enabling this option, you designate JioCX as your primary service provider for sending RCS messages. This setting ensures that all outgoing RCS campaigns are routed through JioCX by default.

3. Select **Send Test** to verify that the integration is functioning correctly. When you click **Send Test**, you will be prompted to enter the following details:
   * **Country Code & Phone Number**: Specify the recipient’s country code and phone number to test message delivery.
   * **RCS Message**: Enter the message content to be sent via RCS.
   * **SMS Fallback Message**: Provide the fallback message content that will be sent via SMS if RCS delivery fails.
   * **Template ID**: Enter the template ID required for message sending (if applicable).
   * **Principal Entity ID** _(only if opted for India)_: If sending messages in India, you must enter the registered Principal Entity ID to comply with DLT regulations.
4. Select **Save** after you have successfully verified the integration.

Once the **Provider** is added, navigate to _Provider Listing_ page for [Provider Operations](doc:rcs-setup#provider-operations).

This feature enables businesses to automate messaging workflows, maintain brand consistency, and enhance customer communication through RCS campaigns.
