---
title: Scribe Prompts (Discard)
excerpt: >-
  Learn how to write effective Scribe prompts, with best practices and
  ready-to-use templates for common campaigns.
deprecated: true
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

A prompt is a short sentence, phrase, or keyword instructing _Scribe_  to generate copywriting ideas. 

You can optimize the message content [Scribe](https://docs.clevertap.com/docs/scribe) generated with effective text prompts. It communicates with the OpenAI APIs to provide you with good suggestions. This guide explains how prompts work, best practices, and provides ready-to-use templates for different industries.

# Best Practices

Following are some best practices you must follow while writing prompts for Scribe:

- **Use the right keywords**: Mention product, brand, or offer clearly.
- **Be concise**: Keep prompts short and focused.
- **Provide context**: Add tone, style, festival, or campaign type.
- **Avoid sensitive words**: Avoid using profanity or senstive words.

You can combine multiple fields (topic, language, style, and so on) in one prompt to get a more specific output.

## Prompt Fields

Refer to the below table to understand prompt fields:

| Field             | Examples                                          | Sample line                                        |
| ----------------- | ------------------------------------------------- | -------------------------------------------------- |
| **Topic**         | “Air Conditioner 20% off”, “New theatre opening”  | `Topic: Air Conditioner with 20% off`              |
| **Brand Name**    | “Cricket Dazzler”, “Cricket Funda”                | `Brand: Cricket Dazzler`                           |
| **Language**      | English, Hindi (mix), Spanish                     | `Language: Mix of Hindi and English`               |
| **Font**          | Devanagari, English, Tamil                        | `Font: Devanagari`                                 |
| **Style**         | Bollywood jingles, Weather report, Rap, Clickbait | `Style: Rap Song`                                  |
| **Include Words** | “delivery”, “cashback”, “finals”                  | `Include Words: cashback, weekend`                 |
| **Exclude Words** | “offer”, “gambling”, “betting”                    | `Exclude Words: offer, betting`                    |
| **Format**        | Title 5 words, Body 20 words                      | `Format: Title (5 words max), Body (20 words max)` |

# Sample Syntaxes for Writing Prompts

The following sample prompts can help you get started with Scribe quickly. You can experiment with more prompts to find a more suitable message tone and style. Browse the sample prompts by industry:

<!DOCTYPE html>

<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

```html

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 1.5rem;
  max-width: 1000px;
  margin: 2rem auto;
  padding: 1rem;
  justify-content: center;
}

.integration-card {
  display: flex;
  align-items: center;
  padding: 1.25rem 1.5rem;
  background: white;
  border-radius: 12px;
  min-height: 100px;
  border: 1px solid rgba(0, 0, 0, 0.08);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.04);
  transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
  text-decoration: none;
}

.integration-card:hover {
  box-shadow: 0px 6px 12px rgba(0, 0, 0, 0.08);
  transform: translateY(-2px);
}

.logo-container {
  display: flex;
  align-items: center;
  padding-right: 1rem;
  border-right: 1px solid rgba(0, 0, 0, 0.08);
  margin-right: 1rem;
}

.logo {
  width: 48px;
  height: 48px;
  object-fit: contain;
  border-radius: 5px;
}

.content {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.name {
  font-size: 1rem;
  font-weight: 600;
  color: #000;
  margin-bottom: 0.3rem;
}

.category {
  font-size: 0.8rem;
  color: #666;
}

/* Responsive rules */
@media (max-width: 768px) {
  .grid {
    grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
    padding: 0 1rem;
  }
}

@media (max-width: 480px) {
  .grid {
    grid-template-columns: 1fr;
  }
}
```

   </style>
</head>
<body>

<div class="grid">
  <a href="#e-commerce" class="integration-card">
    <div class="logo-container">
      <img src="https://img.icons8.com/fluency/48/shopping-cart-loaded.png" class="logo" alt="E-Commerce" />
    </div>
    <div class="content">
      <div class="name">E-Commerce</div>
      <div class="category">Personalization & Offers</div>
    </div>
  </a>

  <a href="#job-portal" class="integration-card">
    <div class="logo-container">
      <img src="https://img.icons8.com/color/48/resume.png" class="logo" alt="Job Portal" />
    </div>
    <div class="content">
      <div class="name">Job Portal</div>
      <div class="category">Hiring & Notifications</div>
    </div>
  </a>

  <a href="#ott" class="integration-card">
    <div class="logo-container">
      <img src="https://img.icons8.com/color/48/tv.png" class="logo" alt="OTT" />
    </div>
    <div class="content">
      <div class="name">OTT</div>
      <div class="category">Content & Engagement</div>
    </div>
  </a>

  <a href="#fintech" class="integration-card">
    <div class="logo-container">
      <img src="https://img.icons8.com/color/48/money-bag.png" class="logo" alt="Fintech" />
    </div>
    <div class="content">
      <div class="name">Fintech</div>
      <div class="category">Finance & Portfolios</div>
    </div>
  </a>

  <a href="#food-delivery" class="integration-card">
    <div class="logo-container">
      <img src="https://img.icons8.com/color/48/meal.png" class="logo" alt="Food Delivery" />
    </div>
    <div class="content">
      <div class="name">Food Delivery</div>
      <div class="category">Menu & Recommendations</div>
    </div>
  </a>

  <a href="#gaming" class="integration-card">
    <div class="logo-container">
      <img src="https://img.icons8.com/color/48/controller.png" class="logo" alt="Gaming" />
    </div>
    <div class="content">
      <div class="name">Gaming</div>
      <div class="category">Rewards & Items</div>
    </div>
  </a>
</div>

</body>
</html>

### E-Commerce

Refer to the below sample prompts for retail offers, festive sales, and multilingual copy.

**Brand Offer**

```
Give me a message for Nike shoes with 20% off for Christmas.
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/796107d-S2EP1.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "100% ",
      "border": true
    }
  ]
}
[/block]


**Discount Campaign**

```
Topic: Air Conditioner with 20% off
Language: Hindi
Font: Devanagari
Style: Humour
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6ac0b15-S1EP1.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "100% ",
      "border": true
    }
  ]
}
[/block]


**Language Target**

```
Give me a message for sports goods in Spanish.
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d422635-S3EP1.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "100% ",
      "border": true
    }
  ]
}
[/block]


**Word Swap**

```
Replace the word savings with something else: 🐰🌸 Hop into Easter savings with our sale! 🌸🐰 Don't miss out on our limited time deals.
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a9abc32-S5EP1.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


**Title Limit**

```
Give a 5-word Title message for: Hop into Easter with our exclusive offers! Get your hands on bunny-tastic deals now. Limited time only. Don't miss out.
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/80817cb-S6EP1.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


### Food Delivery

Refer to the below sample prompts for menus, offers, and delivery promos across languages.

**Brand Offer**

```
Give me a message for an Assorted Dessert Box with 10% off for Diwali.
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/474196a-S2EP2.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "100% ",
      "border": true
    }
  ]
}
[/block]


**Language Target**

```
Give me a message for Pizza in Italian.
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/380a4d5-S3EP2.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


**Bilingual Mix**

```
Give me a message for free delivery charge in a mix of Hindi and English.
```

<br />

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9a3a82d-S4EP2.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


**Word Swap**

```
Replace the word hoggers with something else: Our latest menu will leave even the biggest food hoggers satisfied.
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/db4ff84-S5EP2.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


**Title Limit**

```
Give a 5-word Title message for: Cheers to Happy Hour! Get 50% off on all drinks now!
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3e0ad62-S6EP2.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


**Short Title + Body**

```
Give me a message for corporate offers at a restaurant with a title in 5 words and a body in 15 words or less.
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0eceea0-S7EP2.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


### Gaming

Refer to the below sample prompts for gaming and fantasy sports using styles and emojis.

**Field Builder (Include/Exclude words)**

```
Topic: Create a promotional Campaign for football enthusiasts.
Include Words: Betting, Gambling
Exclude Words: Offer, Adrenaline
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/509a261-S1EP2.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "100% ",
      "border": true
    }
  ]
}
[/block]


**Use Emoji**

```
Topic: Ab firse chadega fantasy ka bukhar. Make your team now.
Brand: Cricket Dazzler
Emoji: Yes
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8a36682-image.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "100% ",
      "border": true
    }
  ]
}
[/block]


**Style (Bollywood) + Language (English/Hindi)**

```
Topic: 58 runs from 39 Balls! C'mon DEL. Join the party and support the team you love.
Style: Bollywood songs
Language: Mix of Hindi and English
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4bfb776-S1EP3A.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "100% ",
      "border": true
    }
  ]
}
[/block]


**Style (Rap)**

```
Topic: Make your cricket team now with India's leading gaming app and win big prizes
Style: Rap Song
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c7267c0-S1EP3B.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "100% ",
      "border": true
    }
  ]
}
[/block]


**Response Length**

```
Topic: Cricket Dhamaka, Try your luck and win amazing prizes.
Brand: Cricket Funda
Response Length: 15 Words
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8b798f7-S1Ep4.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "100% ",
      "border": true
    }
  ]
}
[/block]


### OTT

Refer to the below sample prompts for new releases, subscriptions, and bilingual campaigns.

**Brand Offer**

```
Give me a message for a channel subscription with one month free for New Year.
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9018e43-S2EP3.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "100% ",
      "border": true
    }
  ]
}
[/block]


**Language Target**

```
Give me a message for movie releases in French.
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6e08cca-S3EP4.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


**Bilingual Mix**

```
Give me a message in a mix of Hindi and English for the latest music releases.
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b47d566-S4EP3.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


**Word Swap**

```
Replace the word rib-tickling with something else: Check out our rib-tickling movie collection now.
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3ae9c2a-S5EP3.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


**Title Limit**

```
Give a 10-word Title message for: Get unstoppable streaming power! Ready to try out our channel? Enjoy a FREE trial now!
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5d60c53-S6EP3.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


**Title + Body**

```
Give me a message for a new theatre opening near your area with a title in 5 words and a body in 25 words or less.
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/91b8ebf-S7EP3.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


### Fintech

Refer to the below sample prompts for cards, loans, and savings in single or mixed languages.

| Sample Prompt                                                                 | On Dashboard                                   |
| :---------------------------------------------------------------------------- | :--------------------------------------------- |
| Give me a message for a credit card with cash back for a customer's Birthday. | ![](https://files.readme.io/70e15c1-S2EP4.jpg) |
|                                                                               |                                                |

**Language Target**

```
Give me a message for a house loan offer in Hindi.
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8393545-S3EP4.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


**Bilingual Mix**

```
Give me a message in a mix of Hindi and English for a new bank account opening.
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3481a50-S4EP4.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


**Word Swap**

```
Replace the word reliable with something else: Need extra cash? Get a loan from our reliable bank today!
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8a068ba-S5EP4.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


**Title Limit**

```
Give a 6-word Title message for: Unlock exclusive savings! Lower interest rates for Senior Citizens. Don't miss out; act now.
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b62fcef-S6EP4.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


**Title + Body**

```
Give me a message to open a fixed deposit easily using the mobile app with a title in 5 words and a body in 25 words or less.
```

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/91d02a9-S7EP4.jpg",
        null,
        ""
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true
    }
  ]
}
[/block]


<br />

### E-Commerce

<table style="width:100%; table-layout:fixed; border-collapse:collapse;">
  <colgroup>
    <col style="width:36%;">
    <col style="width:64%;">
  </colgroup>
  <thead>
    <tr>
      <th style="text-align:left; padding:8px;">Prompt</th>
      <th style="text-align:left; padding:8px;">Screenshot</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give me a message for Nike shoes with 20% off for Christmas.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/796107d-S2EP1.jpg" alt="E-commerce Brand Offer" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Topic: Air Conditioner with 20% off<br/>
        Language: Hindi<br/>
        Font: Devanagari<br/>
        Style: Humour
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/6ac0b15-S1EP1.jpg" alt="Discount Campaign Field Builder" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give me a message for sports goods in Spanish.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/d422635-S3EP1.jpg" alt="Language Target Spanish" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give me a message for a new bag collection with a Title in 4 words and a Body in 20 words.
      </td>
      <td style="vertical-align:top; padding:8px;">—</td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Replace the word savings with something else: 🐰🌸 Hop into Easter savings with our sale! 🌸🐰 Don't miss out on our limited time deals.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/a9abc32-S5EP1.jpg" alt="Word Swap Savings → ?" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give a 5-word Title message for: Hop into Easter with our exclusive offers! Get your hands on bunny-tastic deals now. Limited time only. Don't miss out.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/80817cb-S6EP1.jpg" alt="Title Limit 5 words" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
  </tbody>
</table>

***

### Food Delivery

<table style="width:100%; table-layout:fixed; border-collapse:collapse;">
  <colgroup>
    <col style="width:36%;">
    <col style="width:64%;">
  </colgroup>
  <thead>
    <tr>
      <th style="text-align:left; padding:8px;">Prompt</th>
      <th style="text-align:left; padding:8px;">Screenshot</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give me a message for an Assorted Dessert Box with 10% off for Diwali.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/474196a-S2EP2.jpg" alt="Dessert Box Brand Offer" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give me a message for Pizza in Italian.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/380a4d5-S3EP2.jpg" alt="Language Target Italian" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give me a message for free delivery charge in a mix of Hindi and English.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/9a3a82d-S4EP2.jpg" alt="Bilingual Mix Free Delivery" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Replace the word hoggers with something else: Our latest menu will leave even the biggest food hoggers satisfied.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/db4ff84-S5EP2.jpg" alt="Word Swap Hoggers → ?" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give a 5-word Title message for: Cheers to Happy Hour! Get 50% off on all drinks now!
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/3e0ad62-S6EP2.jpg" alt="Title Limit Happy Hour" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give me a message for corporate offers at a restaurant with a title in 5 words and a body in 15 words or less.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/0eceea0-S7EP2.jpg" alt="Short Title + Body Restaurant Offer" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
  </tbody>
</table>

***

### Gaming

<table style="width:100%; table-layout:fixed; border-collapse:collapse;">
  <colgroup>
    <col style="width:36%;">
    <col style="width:64%;">
  </colgroup>
  <thead>
    <tr>
      <th style="text-align:left; padding:8px;">Prompt</th>
      <th style="text-align:left; padding:8px;">Screenshot</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Topic: Create a promotional Campaign for football enthusiasts.<br/>
        Include Words: Betting, Gambling<br/>
        Exclude Words: Offer, Adrenaline
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/509a261-S1EP2.jpg" alt="Field Builder Include/Exclude" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Topic: Ab firse chadega fantasy ka bukhar. Make your team now.<br/>
        Brand: Cricket Dazzler<br/>
        Emoji: Yes
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/8a36682-image.png" alt="Use Emoji Example" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Topic: 58 runs from 39 Balls! C'mon DEL. Join the party and support the team you love.<br/>
        Style: Bollywood songs<br/>
        Language: Mix of Hindi and English
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/4bfb776-S1EP3A.jpg" alt="Bollywood + Hinglish Style" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Topic: Make your cricket team now with India's leading gaming app and win big prizes<br/>
        Style: Rap Song
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/c7267c0-S1EP3B.jpg" alt="Rap Style Example" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Topic: Cricket Dhamaka, Try your luck and win amazing prizes.<br/>
        Brand: Cricket Funda<br/>
        Response Length: 15 Words
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/8b798f7-S1Ep4.jpg" alt="Response Length Example" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
  </tbody>
</table>

***

### OTT

<table style="width:100%; table-layout:fixed; border-collapse:collapse;">
  <colgroup>
    <col style="width:36%;">
    <col style="width:64%;">
  </colgroup>
  <thead>
    <tr>
      <th style="text-align:left; padding:8px;">Prompt</th>
      <th style="text-align:left; padding:8px;">Screenshot</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give me a message for a channel subscription with one month free for New Year.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/9018e43-S2EP3.jpg" alt="Subscription Brand Offer" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give me a message for movie releases in French.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/6e08cca-S3EP4.jpg" alt="Language Target French" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give me a message in a mix of Hindi and English for the latest music releases.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/b47d566-S4EP3.jpg" alt="Bilingual Mix Music Releases" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Replace the word rib-tickling with something else: Check out our rib-tickling movie collection now.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/3ae9c2a-S5EP3.jpg" alt="Word Swap Rib-tickling → ?" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give a 10-word Title message for: Get unstoppable streaming power! Ready to try out our channel? Enjoy a FREE trial now!
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/5d60c53-S6EP3.jpg" alt="Title Limit 10 words" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give me a message for a new theatre opening near your area with a title in 5 words and a body in 25 words or less.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/91b8ebf-S7EP3.jpg" alt="Title + Body Theatre Opening" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
  </tbody>
</table>

***

### Fintech

<table style="width:100%; table-layout:fixed; border-collapse:collapse;">
  <colgroup>
    <col style="width:36%;">
    <col style="width:64%;">
  </colgroup>
  <thead>
    <tr>
      <th style="text-align:left; padding:8px;">Prompt</th>
      <th style="text-align:left; padding:8px;">Screenshot</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give me a message for a credit card with cash back for a customer's Birthday.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/70e15c1-S2EP4.jpg" alt="Credit Card Cashback Brand Offer" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give me a message for a house loan offer in Hindi.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/8393545-S3EP4.jpg" alt="Language Target House Loan Hindi" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give me a message in a mix of Hindi and English for a new bank account opening.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/3481a50-S4EP4.jpg" alt="Bilingual Mix New Bank Account" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Replace the word reliable with something else: Need extra cash? Get a loan from our reliable bank today!
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/8a068ba-S5EP4.jpg" alt="Word Swap Reliable → ?" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give a 6-word Title message for: Unlock exclusive savings! Lower interest rates for Senior Citizens. Don't miss out; act now.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/b62fcef-S6EP4.jpg" alt="Title Limit 6 words" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
    <tr>
      <td style="vertical-align:top; padding:8px;">
        Give me a message to open a fixed deposit easily using the mobile app with a title in 5 words and a body in 25 words or less.
      </td>
      <td style="vertical-align:top; padding:8px;">
        <img src="https://files.readme.io/91d02a9-S7EP4.jpg" alt="Title + Body Fixed Deposit" style="width:100%; height:auto; border:1px solid #eee; border-radius:8px;" />
      </td>
    </tr>
  </tbody>
</table>