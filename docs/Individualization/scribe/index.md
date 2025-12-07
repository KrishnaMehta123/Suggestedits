---
title: Scribe
excerpt: >-
  The first and only content generator that can create emotionally resonant
  content at scale.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
  pages:
    - type: basic
      slug: how-to-write-prompts-for-scribe
      title: How to Write Effective Prompts for Scribe
    - type: basic
      slug: scribe-faqs
      title: Scribe FAQs
---
# Overview

Scribe is the first and only AI-powered writing assistant that can also analyze and adjust the emotional tone of your content. Scribe communicates with the OpenAI APIs to generate messages for you. You can use a few text [prompts](https://docs.clevertap.com/docs/how-to-write-prompts-for-scribe) to automatically generate attractive and emotionally relevant messages. It removes writer's block, allowing you to create message copies effortlessly and add emotional appeal to them. Scribe also uses emojis and hashtags wherever appropriate to generate appealing messages that help you drive engagement. 

# Create a Push Notification Message using Scribe

This section describes the steps to create a Push Notification message using Scribe. This feature can generate relevant copies for the message title and body.

To create a push notification message using Scribe:

1. Create a **Push Notification Message** using **Campaigns** or **Journeys**. 

   <Image alt="Create a Push Notification Message" align="center" border={true} src="https://files.readme.io/e0c88b9-image.png">
     Create a Push Notification Message
   </Image>
2. On the message editor, click the **Scribe**![Magic Wand](https://files.readme.io/18c307a-ScribeNewIcon.jpg) icon next to the *Title* or *Message* field.\
   The **Scribe** window displays.

   <Image alt="Scribe Window" align="center" border={true} src="https://files.readme.io/0287977-image.png">
     Scribe Window
   </Image>
3. Enter your text in the *[Message/Prompt](https://docs.clevertap.com/docs/how-to-write-prompts-for-scribe)* field and click any of the following buttons to:
   * [Generate Copy](scribe#generate-options): Generate multiple campaign copies with varying emotions based on the prompt you enter.
   * [Optimize for Emotions](doc:scribe#paraphrase): Paraphrase and calibrate the emotional tone of the message.
     > 📘 Note
     >
     > The maximum character limit for the *Message/Prompt* field is 250.
4. Click **[View sample prompts](https://staging.docs.user.clevertap.net/docs/sample-syntaxes-for-scribe-prompts)** if necessary. This will provide you with sample syntaxes for writing effective prompts. 
5. To copy the generated content, hover over the message, click the **Copy to clipboard** ![](https://files.readme.io/8a9e8dc-CopyToClipboard.png)icon, click **Done** to exit the Scribe window, and paste the message. 

## Generate Copy

Based on the [prompt](https://docs.clevertap.com/docs/how-to-write-prompts-for-scribe) you enter, Scribe generates up to **three** message options. It also analyzes the emotional tone of the content. For example, you can enter *Give me a message with 30% off on Smart TV for Black Friday Sale*. The message is evaluated for emotions such as Anticipation, Fear Of Missing Out (FOMO), Joy, Surprise, and Trust. It enables you to understand how the audience may perceive the message. The emotional appeal of these messages can help you achieve a higher engagement. Based on the emotion analysis, you can select a message. You can also optimize the emotional tone of your generated message copy. For more information about optimizing emotions, refer to [Optimize for Emotions](scribe#generate-options). 

<Image alt="Suggested Option and Emotion Analysis" align="center" border={true} src="https://files.readme.io/5e3040d-image.png">
  Suggested Option and Emotion Analysis
</Image>

## Optimize for Emotions

After you generate different variations of the current message, copy the one that best aligns with your use case and brand tone. Paste the copied message into the *Message/Prompt* field, then click **Optimize for Emotions** to fine-tune the emotional tone of the selected message. Scribe displays up to ten options on the screen. Use the **Increase** drop-down to increase a specific emotion for your target audience. For example, enter the message *Black Friday Sale Alert! Get a Smart TV with 30% off now! Don't miss out on this amazing deal!* and click **Optimize For Emotions**. If you want the message to evoke more *Joy*, it displays the messages with the highest *Joy* emotion in descending order. You can click *Optimize for Emotions* again to generate more options.

<Image alt="Optimized for Emotions" align="center" border={true} src="https://files.readme.io/b02578e-image.png">
  Optimized for Emotions
</Image>

# Create WhatsApp Messages using Scribe

> 📘 Scribe Access
>
> Currently, Scribe is available exclusively to WhatsApp Direct customers on Cutting Edge plans. For further information, talk to your Customer Success Representative.

You can leverage Scribe while setting up different message templates for your WhatsApp business account. Scribe helps you craft enticing, contextual, and personalized Titles, Body, and Footer Text messages subjective to your templates.

To create a WhatsApp message template using Scribe:

1. Navigate to *Settings* > *Channels* > *WhatsApp*
2. Select your WhatsApp Business Account 
3. Navigate to *Templates* and click **+Template**

<Image align="center" className="border" border={true} src="https://files.readme.io/02aada3-templates.jpg" />

4. Select the message template type. Let us take Basic for this example.

<Image align="center" className="border" border={true} src="https://files.readme.io/63ba896-basic_temp.jpg" />

5. Click the **Scribe**![Magic Wand](https://files.readme.io/18c307a-ScribeNewIcon.jpg) icon next to the *Title* or *Message* field. The **Scribe** window will display. 

<Image alt="Scribe Window" align="center" border={true} src="https://files.readme.io/0287977-image.png">
  Scribe Window
</Image>

6. Enter your prompt in the *Message/Prompt* and click any of the following buttons to:

* [Generate Copy](scribe#generate-copy): Generate multiple message copies with varying emotions based on the prompt you enter.
* [Optimize for Emotions](doc:scribe#optimize-for-emotions): Paraphrase and calibrate the emotional tone of the Title/ Message.

Here's a sample prompt to create an enticing Title using Scribe for Festive Sale.

<Image alt="Scribe For WhatsApp." align="center" border={true} src="https://files.readme.io/a93654f-scribe_whatsapp.jpg">
  Scribe For WhatsApp.
</Image>

> 🚧 Scribe Responses
>
> Before adding a Scribe-generated response to your template, review and refine it to ensure compliance with the[ meta guidelines](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/).

# Error Messages in Scribe

Scribe alerts you with the following error messages if an issue occurs: 

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Error
      </th>

      <th>
        Error Message
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        When the API server is unavailable or busy.
      </td>

      <td>
        *Server error: Try again in some time.*
      </td>
    </tr>

    <tr>
      <td>
        When a user uses profane words in the message or prompt.
      </td>

      <td>
        *Inappropriate language: Rewrite to get emotion analysis.*
      </td>
    </tr>

    <tr>
      <td>
        When Scribe is unable to generate options.
      </td>

      <td>
        The following error messages appear:  

        * Generate Options: *No output: Rewrite the prompt to get suggestions.*
        * Paraphrase: *Server error: Try again in some time.*
      </td>
    </tr>

    <tr>
      <td>
        When Scribe does not have any options to display to the user.
      </td>

      <td>
        *No output: Paraphrase again to get suggestions.*
      </td>
    </tr>
  </tbody>
</Table>
