---
title: Generate Message Copy with Scribe
excerpt: >-
  Learn how to write effective Scribe prompts, with best practices and
  ready-to-use templates for common campaigns across industries.
deprecated: false
hidden: false
link:
  new_tab: false
metadata:
  title: ''
  description: ''
  robots: index
---
# Overview

You can optimize the message content that [Scribe](https://docs.clevertap.com/docs/scribe) generated with effective text prompts. A prompt is a short sentence, phrase, or keyword instructing Scribe to generate copywriting ideas. Scribe uses AI to help you generate relevant and engaging message suggestions.

Key capabilities of Scribe's AI:

* Speeds up production: Turns a short prompt into multiple copy options in seconds.
* Optimizes emotion and tone: Ask for humour, urgency, celebratory, reassuring emotion, and so on, based on your specific use case.
* Adapts to context: Scribe already knows the channel (such as WhatsApp, Email, Web Push, and so on) from CleverTap. However, you can further customize the prompt by adding brand, product, offer, festival, language, font, or audience details to guide the message style and tone. The more specifics you provide, the better the output.
* Follows constraints: Scribe considers title and body word limits, must-include or avoid words, and bilingual output, if mentioned.

# Best Practices

Following are some best practices you must follow while writing prompts for Scribe:

* **Use clear keywords**: Clearly mention the product, brand, or offer to focus the message generation.
  * *Example*: `Brand: FitFuel | Offer: 25% off on protein bars` — This helps generate message options that highlight the brand and deal.
* **Provide details**: Keep prompts detailed. Lead with a one-line goal, then add brief details for Brand, Product/Offer, Tone/Emotion, Language/Font, Include/Exclude words, Title/Body limits. 
  * *Example*: `Goal: Promote a flash sale for a new launch. Brand: LuxeWear | Tone: Urgent | Style: Clickbait | Include Words: today, sale | Format: Title (5 words max), Body (20 words max)`
* **Provide context and numbers**: Include campaign type (e.g., festival offer, back-to-school), emotion, or urgency markers. Add offer values, product names, coupon codes, deadlines, or locations to help generate sharper copy. 
  * *Example*: `Festival: Diwali | Product: LED Strip Lights | Discount: ₹500 off | Expires: Nov 12 | Emotion: Joy`
* **Guide the emotion**: Mention the feeling required for your campaign, such as playful, FOMO, trust-building, premium, friendly, and so on. 
  * *Example*: `Tone: Playful | Emotion: Surprise | Style: Bollywood jingle`
* **Avoid sensitive words**: Avoid using profanity or sensitive words. 
  * *Example*: Instead of "bet big on Diwali," use "grab the best Diwali deal."

You can combine multiple fields (topic, language, style, and so on) in one prompt to get a more specific output.

## Prompt Fields

Refer to the table below to understand prompt fields:

| Field             | Example                                           | Sample line                                        |
| ----------------- | ------------------------------------------------- | -------------------------------------------------- |
| **Topic**         | "Air Conditioner 20% off", "New theatre opening"  | `Topic: Air Conditioner with 20% off`              |
| **Brand Name**    | "Basketball Blitz", "GamePlay Central"            | `Brand: Cricket Dazzler`                           |
| **Language**      | English, Hindi (mix), Spanish                     | `Language: Mix of Hindi and English`               |
| **Font**          | Devanagari, English, Helvetica                    | `Font: Devanagari`                                 |
| **Style**         | Bollywood jingles, Weather report, Rap, Clickbait | `Style: Rap Song`                                  |
| **Include Words** | "delivery", "cashback", "finals"                  | `Include Words: cashback, weekend`                 |
| **Exclude Words** | "offer", "gambling", "betting"                    | `Exclude Words: offer, betting`                    |
| **Format**        | Title 5 words, Body 20 words                      | `Format: Title (5 words max), Body (20 words max)` |

# Sample Syntaxes to Write Prompts

The following sample prompts can help you get started with Scribe quickly. You can experiment with more prompts to find a more suitable message tone and style. Browse the sample prompts by industry:

<Cards columns="3">
  <Card title="E-Commerce" href="#e-commerce" icon="shopping-cart">
    Personalization & Offers
  </Card>
  <Card title="OTT" href="#ott" icon="tv">
    Content & Engagement
  </Card>
  <Card title="Fintech" href="#fintech" icon="money-bill">
    Finance & Portfolios
  </Card>
  <Card title="Food Delivery" href="#food-delivery" icon="utensils">
    Menu & Recommendations
  </Card>
  <Card title="Gaming" href="#gaming" icon="gamepad">
    Rewards & Items
  </Card>
</Cards>

## E-Commerce

Refer to the below sample prompts for retail offers, festive sales, and multilingual copy.

#### Brand related offers

```
Topic: Nike running shoes—20% off for Christmas
Brand: Nike
Tone: Cheerful, gift-ready, FOMO
Channel: Push
Format: Title (5 words), Body (20 words)
```

<Image align="center" className="border" width="100% " border={true} src="https://files.readme.io/0900b2dd053298faa3afe59f1bf16abc850b36e8eeb7db8b320e28ff4dbc6059-Scribe_message.png" />

<Accordion title="More E-Commerce examples" icon="plus">

**Language Target** — Give me a message for sports goods in Spanish.

![Spanish sports goods message](https://files.readme.io/d422635-S3EP1.jpg)

**Discount Campaign** — Topic: Air Conditioner with 20% off · Language: Hindi · Font: Devanagari · Style: Humour

![Hindi AC discount message](https://files.readme.io/6ac0b15-S1EP1.jpg)

**Word Swap** — Replace the word savings with something else: 🐰🌸 Hop into Easter savings with our sale! 🌸🐰 Don't miss out on our limited time deals.

![Easter word swap example](https://files.readme.io/a9abc32-S5EP1.jpg)

**Title Limit** — Give a 5-word Title message for: Hop into Easter with our exclusive offers!

![Easter title limit example](https://files.readme.io/80817cb-S6EP1.jpg)

</Accordion>

## OTT

Refer to the below sample prompts for new releases, subscriptions, and bilingual campaigns.

#### Brand related offers

```
Topic: Channel subscription—1 month free (New Year)
Tone: Excited, celebratory
Include Words: free month, New Year
Format: Title (7 words), Body (25 words)
```

<Image align="center" className="border" width="100%" border={true} src="https://files.readme.io/52878c2d7c23ad5e2f33a892b3685c263ae24526527427e2246818e6d0e24ccd-subscription.png" />

<Accordion title="More OTT examples" icon="plus">

**Bilingual Mix** — Give me a message in a mix of Hindi and English for the latest music releases.

![Hindi-English music message](https://files.readme.io/b47d566-S4EP3.jpg)

**Language Target** — Give me a message for movie releases in French.

![French movie message](https://files.readme.io/6e08cca-S3EP4.jpg)

**Word Swap** — Replace the word rib-tickling with something else: Check out our rib-tickling movie collection now.

![Word swap movie example](https://files.readme.io/3ae9c2a-S5EP3.jpg)

**Title Limit** — Give a 10-word Title message for: Get unstoppable streaming power! Ready to try out our channel? Enjoy a FREE trial now!

![Streaming title limit example](https://files.readme.io/5d60c53-S6EP3.jpg)

**Title + Body** — Give me a message for a new theatre opening near your area with a title in 5 words and a body in 25 words or less.

![Theatre opening example](https://files.readme.io/91b8ebf-S7EP3.jpg)

</Accordion>

## Fintech

Refer to the below sample prompts for cards, loans, and savings in single or mixed languages.

#### Brand related offers

```
Topic: Credit card—birthday cashback
Audience: Existing cardholders
Tone: Warm, appreciative
Exclude Words: limited time
Format: Title (6 words), Body (20 words)
```

<Image align="center" src="https://files.readme.io/870ae0a865dfa22b61bfaa961b1dfd8350f27e42d974431ce1f56e801272d128-Fintech.png" />

<Accordion title="More Fintech examples" icon="plus">

**Bilingual Mix** — Give me a message in a mix of Hindi and English for a new bank account opening.

![Hindi-English bank account message](https://files.readme.io/3481a50-S4EP4.jpg)

**Language Target** — Give me a message for a house loan offer in Hindi.

![Hindi house loan message](https://files.readme.io/8393545-S3EP4.jpg)

**Word Swap** — Replace the word reliable with something else: Need extra cash? Get a loan from our reliable bank today!

![Bank word swap example](https://files.readme.io/8a068ba-S5EP4.jpg)

**Title Limit** — Give a 6-word Title message for: Unlock exclusive savings! Lower interest rates for Senior Citizens. Don't miss out; act now.

![Senior citizen savings example](https://files.readme.io/b62fcef-S6EP4.jpg)

**Title + Body** — Give me a message to open a fixed deposit easily using the mobile app with a title in 5 words and a body in 25 words or less.

![Fixed deposit app example](https://files.readme.io/91d02a9-S7EP4.jpg)

</Accordion>

## Food Delivery

Refer to the below sample prompts for menus, offers, and delivery promos across languages.

#### Brand related offers

```
Topic: Summer drinks—buy 2 get 1 free
Brand: RefreshCo
Tone: Cool, refreshing, beat-the-heat
Include Words: summer, free, cool
Format: Title (6 words), Body (18 words)
```

<Image align="center" className="border" width="100%" border={true} src="https://files.readme.io/4d7ee7d7897fd3828c674ec623c15023dfbd4441c4416148f6a091d3a9f7b6be-scribe.png" />

<Accordion title="More Food Delivery examples" icon="plus">

**Bilingual Mix** — Give me a message for free delivery charge in a mix of Hindi and English.

![Hindi-English delivery message](https://files.readme.io/9a3a82d-S4EP2.jpg)

**Language Target** — Give me a message for Pizza in Italian.

![Italian pizza message](https://files.readme.io/380a4d5-S3EP2.jpg)

**Word Swap** — Replace the word hoggers with something else: Our latest menu will leave even the biggest food hoggers satisfied.

![Food word swap example](https://files.readme.io/db4ff84-S5EP2.jpg)

**Title Limit** — Give a 5-word Title message for: Cheers to Happy Hour! Get 50% off on all drinks now!

![Happy hour title example](https://files.readme.io/3e0ad62-S6EP2.jpg)

**Short Title + Body** — Give me a message for corporate offers at a restaurant with a title in 5 words and a body in 15 words or less.

![Corporate restaurant example](https://files.readme.io/0eceea0-S7EP2.jpg)

</Accordion>

## Gaming

Refer to the below sample prompts for gaming and fantasy sports using styles and emojis.

#### Emoji Prompt

```
Topic: Ab firse chadega fantasy ka bukhar. Make your team now.
Brand: Cricket Dazzler
Emoji: Yes
```

<Image align="center" className="border" width="100%" border={true} src="https://files.readme.io/8a36682-image.png" />

<Accordion title="More Gaming examples" icon="plus">

**Field Builder (Include/Exclude)** — Topic: Create a promotional Campaign for football enthusiasts. · Include: Betting, Gambling · Exclude: Offer, Adrenaline

![Football campaign example](https://files.readme.io/509a261-S1EP2.jpg)

**Style (Bollywood) + Hinglish** — Topic: 58 runs from 39 Balls! … · Style: Bollywood songs · Language: Mix of Hindi and English

![Bollywood cricket example](https://files.readme.io/4bfb776-S1EP3A.jpg)

**Style (Rap)** — Topic: Make your cricket team now with India's leading gaming app and win big prizes · Style: Rap Song

![Rap cricket example](https://files.readme.io/c7267c0-S1EP3B.jpg)

**Response Length** — Topic: Cricket Dhamaka, Try your luck and win amazing prizes. · Brand: Cricket Funda · Response Length: 15 Words

![Cricket response length example](https://files.readme.io/8b798f7-S1Ep4.jpg)

</Accordion>