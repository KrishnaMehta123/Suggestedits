---
title: Using Personalization in Linked Content Response
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
> 📘 Private Beta
>
> This feature is released in Private Beta. If you want to access this feature, contact your Customer Success Manager.

# Overview

CleverTap supports personalization in Linked Content, allowing you to dynamically replace personalization placeholders with user-specific values. This ensures messages are customized before delivery, even for translated or localized content.

With this feature, you can send highly targeted messages across multiple languages using profile attributes and event properties, improving user engagement and relevance.

# Supported and Unsupported Variables

### Supported Variables

You can personalize Linked Content responses using the following placeholders with Liquid syntax:

* Profile attributes: `{{Profile.name}}`, `{{Profile.accounttype}}`
* Event properties: `{{Event["offerPercentage"]}}` (only for actions delayed by less than 24 hours)
* Campaign ID: `{{Campaign.campaignId}}`
* External Trigger values: `{{ExternalTrigger.somekey}}`
* Identity: `{{Profile.Identity}}`

### Unsupported Variables

* For Event Personalization with a delay of more than 24 hours, default values are used.
* Catalog and recommendation variables fall back to default values.
* As @ Personalization is not supported, any variable prefixed with @ (for example, @Profile - Name) is not parsed, that is, the variable is not replaced with a value.
* Messages with invalid Liquid syntax are flagged as errors to prevent delivery with unresolved placeholders.

# Syntax

Use the following syntax when configuring personalization in Linked Content responses:

* Profile Personalization:`{{Profile.name | default:\"Name\"}}`
* Event Personalization: `{{Event[\"offerPercentage\"] | default:\"0\"}}`
* Campaign ID: `{{Campaign.campaignId | default:\"0_0\"}}`
* External Trigger: `{{ExternalTrigger.somekey | default:\"def\"}}`
* Identity: `{{Profile.Identity | default:\"idFail\"}}`

***

# Use Case: Translating Personalized Messages Across Languages

Learn how to use personalization for translated messages.

### Scenario

A bank customer in Germany receives notifications from his bank about promotional offers. The English version of the final notification delivered to the user is as follows:

```Text Output
Hi John! Now you can earn up to €50 in your savings account.
```

However, when the message is translated into German using Linked Content, it displays as follows:

```
Hallo {{Profile.name | default:"Namefailed"}}! Jetzt kannst du bis zu {{Profile.currency | default:"Currency"}} {{Event["offerPercentage"] | default:"0"}} in dein {{Profile.accounttype | default:"Account"}} Konto verdienen.
```

### Solution

When using message translation, personalized parameters such as \{\{}} placeholders often remain unchanged in translated messages and notifications. This results in the German version of the message not being fully personalized when delivered to the user. 

With this feature, CleverTap dynamically resolves all placeholders within translated content before the message is delivered, ensuring a fully personalized experience in the user's preferred language. 

### How it works

This is how the above-mentioned use case is achieved:

1. When the bank sends him the same promotional message, Linked Content fetches the German message from the translation service. 
2. All personalization placeholders are dynamically replaced using real-time user data, such as `Profile.name, Event["offerPercentage"]`, and so on. 
3. If a placeholder is invalid or unsupported (for example, prefixed with @), it is either left as-is or flagged as an error.
4. The fully personalized message is delivered in the user’s preferred language, here, German:

```Text Output
Hallo John! Jetzt kannst du bis zu €50 in dein Sparkonto verdienen.
```

This use case can be extended for further personalization using Liquid setup, or through API-based translations.

> 📘 Key Consideration
>
> * Resolving personalization placeholders adds processing time, which may slightly delay message delivery compared to standard notifications.
> * No changes are required in the campaign setup process.

This ensures that personalization works seamlessly across multiple languages, improving engagement and user experience.
