---
title: WhatsApp Add-ons (Table version)
excerpt: Learn about the WhatsApp Add-ons Offered by CleverTap.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Introduction

CleverTap offers WhatsApp add-ons to enhance your messaging capabilities and boost customer engagement. With these add-ons, you can use WhatsApp for various purposes, such as FAQs, auto-replies, agent chats, and much more.

> 📘 WhatsApp Add-Ons
> 
> CleverTap's WhatsApp Add-ons are available as a paid feature.

Incorporating WhatsApp as part of your customer engagement strategy significantly enhances your customer engagement rate and overall customer experience.

Prior to learning about WhatsApp Add-ons offered by CleverTap, here are a few points you must bear in mind:

- You can save and test provider credentials without buying the WhatsApp add-on in CleverTap.
- You will be unable to create or publish WhatsApp campaigns or journeys without purchasing the add-on.
- WhatsApp conversations (FAQ, auto-reply, and agent chat) require an add-on purchase.

# WhatsApp Add-ons by CleverTap

CleverTap offers two add-ons for WhatsApp integration: 

- CleverTap Connect
- CleverTap Direct

> 🚧 Note
> 
> CleverTap Connect subscribers have limited access to external providers. Subscribers can set up a WhatsApp Business Account (WABA) with CleverTap but can not use CleverTap as a Business Service Provider (BSP) in campaigns and journeys.

Let's take a look at the detailed comparison.

| <p>Name of the Add-On</p>                    | <p>CleverTap Connect</p>                                                                                                                                                                                                                                                                                                                   | <p>CleverTap Direct</p>                                                                                                                                                                                                                                                                                                                               |
| :------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p><strong>Description</strong> </p>         | <p>CleverTap Connect is a suitable Add-on for customers willing to use external WhatsApp providers. </p><p>With this add-on, customers will receive access to external providers only and will be charged based on their chosen tier. Any additional usage will be charged at the end of the month.</p>                                    | <p>Using CleverTap Direct, customers can set up both external and internal providers, but they can use only CleverTap WhatsApp Business Account for creating campaigns and journeys.</p>                                                                                                                                                              |
| <p><strong>Billing Logic</strong> </p>       | <p>CleverTap bills you as per the total notifications sent to your end users.  </p><p>Here, it is assumed that notifications sent successfully from CleverTap are delivered to the end user if they are not considered errors at the provider's end at the time of delivery.</p>                                                           | <p>Customers are billed for the conversation count recorded at WhatsApp's end.</p>                                                                                                                                                                                                                                                                    |
| <p><strong>Overage Calculation</strong> </p> | <p>The overage for the month is calculated based on the total number of additional notifications used over and above the monthly base fee for the tier allotted.</p><p>Refer to the <a href="https://docs.clevertap.com/docs/whatsapp-add-ons-table-version#clevertap-connect-overage-calculation-logic">overage calculation logic</a></p> | <p>CleverTap considers two types of overages for CleverTap Direct: </p><ul><li><a href="https://docs.clevertap.com/docs/whatsapp-add-ons-table-version#consumption-based-overages">Consumption-based Overage</a></li><li><a href="https://docs.clevertap.com/docs/whatsapp-add-ons-table-version#fair-usage-overage">Fair Usage Overage</a></li></ul> |

# Examples of Overage Billing

The following section explains the overage calculation logic for both add-ons.

## CleverTap Connect Overage Calculation Logic

Let's take an example to understand this better:

A business has actively subscribed for a monthly base plan of $30 for up to 10,000 notifications. By the month end, the business ends up using 5000 additional notifications.

To calculate the overage usage in this case, we can use the following formula:

Overage cost = Number of overage notifications \* cost per notification

Where:  
Number of overage notifications = 5000 (as specified in the scenario)  
Cost per notification = ($30 base plan / 10,000 notifications) = $0.003

Therefore, the overage cost = 5000 \* $0.003 = $15  
So, the total cost for the base plan + overage usage would be $30 (base plan) + $15 (overage cost) = $45.

## CleverTap Direct Overage Calculation Logic

### Consumption-based Overages

If a customer consumes more conversations than their commitment, agreed overage rates will be applied for the additional conversations.

### Fair Usage Overage

CleverTap calculates the pricing based on WhatsApp's rate card and the target audience estimated by the business in various countries. If conversations are sent to countries that are not part of the target audience, additional fees may be charged, calculated as the difference between the final WhatsApp charges and the monthly base fee, plus a margin on this difference as per the applicable conversation slab.

Let's take an example to understand this better:

A business has a monthly base fee of $100 for WhatsApp with CleverTap's margin on top of WhatsApp charges at 10%. They commit to sending conversations in USA, Canada, and Mexico, but end up sending conversations in France, and their final WhatsApp bill comes as $150.

The overage is calculated as the difference between the final bill and the monthly base fee ($150-$100 = $50). CleverTap will charge the business an additional 10% margin on the difference, resulting in a total overage of ($150-$100) + ($50 \* 10%) = $55.