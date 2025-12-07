---
title: Custom Key-Value Pairs
excerpt: Learn how you can use custom key-value pairs to enrich your user experience.
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

Custom key-value pairs offer a powerful way to enrich your email campaigns, providing an extra layer of flexibility. By allowing you to attach additional metadata to your emails, you can easily personalize messages, track campaign performance, and connect seamlessly with external systems.

Custom key-value pairs are text-based attributes you can define and include in your email campaigns. CleverTap supports adding these pairs under the _What_ section of the campaign. They enable you to pass additional information alongside the email payload using HTTP or SMTP protocols. For example, if an e-commerce business wants to track the campaign that generated traffic on your portal. In that case, it can use a key-value pair such as: `utm_campaign: summer_sale`. Any analytics tool can process this information, and the e-commerce business can modify its engagement strategy if required.

CleverTap supports adding these custom key-value pairs in the email headers or message extras as follows:

## Custom Headers

Custom Headers allow you to define additional fields in the email headers section. These are then read by email clients or servers to provide extra information. These parameters usually include information about the sender, recipient, authentication protocols, and email routing. 

For example, you can include `dkim-signature` header to allow receiving email servers to authenticate the sender’s domain. This ensures your emails are validated and trusted by recipient servers, reducing the risk of them being marked as spam.

Custom Headers are supported by the following Email Providers: PayTM, SendGrid, Amazon SES, Generic SMTP, PostMark, Mandrill, Nexmo, Kenscio, and Netcore HTTP

## Custom Extras

Custom Extras allow sending additional information back to the email providers along with the email payload. These parameters are not embedded in the email headers. This is essential for post-processing, tracking, and custom analysis on the ESP or customer side. This information can be used to derive insights and take appropriate actions.

For example, you can include `recent_purchase: "T-Shirt"`in the email payload. Based on this, you can recommend related products such as Jeans, Trousers, and so on in the follow-up email.

Custom Extras are supported by the following Email Providers: PayTM and SendGrid. (Rest @Shreejith to confirm)

# Use Cases

Here are some use cases to demonstrate how you can leverage key-value pairs for improved tracking and personalization:

- **Tracking and Analytics**: You can track how your emails are performing across different channels and platforms. For example, by adding parameters such as `utm_source: newsletter` and `utm_medium: email`, you can integrate email campaign data into your analytics tool for detailed reporting.
- **Dynamic Content Personalization**: You can tailor email content dynamically based on the user attributes or behaviors. For example, you can show special offers or exclusive content to premium users if you include `user_tier: premium`.
- **BIMI Selector Configuration:** You can improve brand recognition by configuring BIMI selectors and displaying your brand logo alongside authenticated emails. For example, you can include `bimi_selector: selector1` in the email payload to fetch and display the correct logo.
- **Gmail Feedback ID**: You can incorporate a `gmail_feedback_id` as a custom key-value pair within your email headers to leverage Gmail’s Feedback Loop (FBL). This enables you to monitor campaigns with high complaint volumes from Gmail users and aids in early abuse detection.

# Add Custom Key-Value Pairs

To add custom key-value pairs in your email campaigns:

1. Go to the **What** section of the email campaign and click **Go to Editor**.
2. Draft your email campaign and select the _Sender Details_ tab. 
3. Select **Custom Headers** and/or **Custom Extras** to add the respective key-value pairs.
4. Click **+ Header** and/or **+ Extra** to add the key and value in the respective fields.

> 📘 Note
> 
> - You can add a maximum of 10 key-value pairs for both Custom Headers and Custom Extras.
> - A maximum of 1KB of Key and Value can be added in both Custom Headers and Custom Extras. (@shreejith is this correct?) - combined
> 
> Should we add the following information as well here?  
> HTTP supports both as a protocol, SMTP only supports headers

What about Personalization? We haven't mentioned anything about that. 

5. Click **Done**.

saying - before sending it out - you can test it with Send Test personalization. - default value, if you do not have this feature enabled

@shreejith: Should we list the reserved attributes under the Best Practices callout? - arif - callout