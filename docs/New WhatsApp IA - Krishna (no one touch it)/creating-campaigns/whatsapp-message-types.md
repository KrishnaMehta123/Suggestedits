---
title: WhatsApp Message Types
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
You can create the following types of messages in your WhatsApp campaign:

- Single Message
- A/B Test
- Split Delivery
- By User Property

> 📘 Legacy UI
> 
> A/B Test and Split Delivery message types are only available for new campaign UI.

### Single Message

In this campaign, a standard message is sent to all users who qualify as your target audience. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between properties such as language, geography, or any other user properties.

### A/B Testing

A/B testing helps you understand what type of message copy works best to get clicks from users.  
You can test up to three message variants on a test group. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6139527-WhatsApp_AB_Test.png",
        "WhatsApp A/B Test",
        "The image represents a sample distribution between two variants for A/B testing"
      ],
      "align": "center",
      "border": true,
      "caption": "WhatsApp A/B Tests"
    }
  ]
}
[/block]


> 📘 Winning Variant
> 
> The variant that gets the most views is declared the winning variant and is automatically sent to the rest of your target audience.

When you create multiple variants (max: 3 variants) for a campaign, you can also auto-copy the content present in the current variant. Further, let us understand A/B Test delivery for Live user segments.

#### A/B Test Delivery To Live User Segments

With campaigns sent to live user segments (triggered campaigns), messages are delivered immediately when a user’s activity matches the criteria you have selected. For example, you can send a message when the user has completed a booking or purchase. Since it is not possible to determine the reach of triggered campaigns upfront, you need to decide how many total messages to send for A/B testing before a winner is declared.

> 👍 Triggered Campaign Example
> 
> If you select 500 users as your test audience, we will alternate delivery of Variant A and Variant B as users qualify for the campaign. After a total of messages are sent (Variant A – 250 and Variant B – 250), we then decide the winner based on the number of views and continue only with this winning message for the duration of the campaign.

Deciding on a test audience for A/B testing triggered campaigns requires some estimation. We recommend you check the total messages that were sent for similar triggered campaigns in the past to get a sense of how many users may qualify. If you select a test audience that is too small such as 25 users, you will get a statistically insignificant sample. If your test group size exceeds the total number of users who ultimately qualify for that campaign, then no winner will be declared and each message variant will be alternatively delivered for the duration of the campaign.

### Split Delivery

With split delivery, you can decide what percentage of your audience receives each message variant for the duration of the campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1b5d9aa-Whatsapp_Split_delivery.png",
        "Whatsapp Split delivery",
        "As the image represents, you can define the percentage split for your message variants"
      ],
      "align": "center",
      "border": true,
      "caption": "WhatsApp Split Delivery"
    }
  ]
}
[/block]


### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, you can use the _+Variant_ button to add multiple variants based on a user property value. In the example below, we have used the _Language_ user property so users with different language preferences will receive corresponding copies of the campaign in their preferred language (English, Hindi, etc.)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7fe4f5c-WhatsApp_user_property.png",
        "WhatsApp user property",
        "You can add multiple variants based on a user property value."
      ],
      "align": "center",
      "border": true,
      "caption": "Targetting Based on User Property"
    }
  ]
}
[/block]