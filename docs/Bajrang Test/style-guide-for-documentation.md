---
title: Style Guide for Documentation
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
# Purpose of the Guide

This style guide aims to provide detailed guidelines on how to write, structure, and present technical documentation to ensure consistency, clarity, and user-friendliness. It is meant to standardize the documentation process across various teams and projects, making it easier for users to understand and engage with the content.

# Table of Contents

## [1. General Writing Principles](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#1-general-writing-principles-1)

* [Audience Consideration](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#audience-consideration)
* [Tone and Voice](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#tone-and-voice)
* [Active vs. Passive Voice](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#active-vs-passive-voice)
* [Sentence Structure](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#sentence-structure)
* [Vocabulary and Terminology](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#vocabulary-and-terminology)

## [2. Formatting Guidelines](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#2-formatting-guidelines-1)

* [Headings and Subheadings](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#headings-and-subheadings)
* [Lists and Bullet Points](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#lists-and-bullet-points)
* [Code Blocks](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#code-blocks)
* [Emphasis (Bold, Italics, Underline)](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#emphasis-bold-italics-underline)
* [Links](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#links)
* [Notes, Warnings, and Tips](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#notes-warnings-and-tip)

## [3. Content Structuring](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#3-content-structuring-1)

* [Overview and Introduction](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#overview-and-introduction)
* [Task-Based vs. Concept-Based Documentation](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#task-based-vs-concept-based-documentation)
* [Step-by-Step Instructions](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#step-by-step-instructions)
* [Use Cases and Examples](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#use-cases-and-examples)
* [Screenshots and Diagrams](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#screenshots-and-diagrams)

## [4. Technical Conventions](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#4-technical-conventions-1)

* [Code and Syntax](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#code-and-syntax)
* [File Paths and Command Line Instructions](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#file-paths-and-command-line-instructions)
* [Error Messages](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#error-messages)

## [5. Grammar and Punctuation](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#5-grammar-and-punctuation-1)

* [Common Grammar Rules](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#common-grammar-rules)
* [Punctuation Usage](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#punctuation-usage)

## [6. Special Considerations](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#6-special-considerations-1)

* [Localization and Internationalization](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#localization-and-internationalization)
* [Accessibility](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#accessibility)
* [SEO for Documentation](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#accessibility)

## [7. Review and Editing Process](https://staging.docs.user.clevertap.net/docs/style-guide-for-documentation#7-review-and-editing-process-1)

***

# 1. General Writing Principles

## Audience Consideration

Always write with your target audience in mind. Understand their level of technical expertise:

* **Beginner**: Avoid jargon and explain all technical terms.
* **Intermediate**: Introduce more complex concepts but still offer background information.
* **Advanced**: Assume familiarity with core concepts but clarify anything that might be new or unusual.

Tailor your documentation to solve problems from the reader's perspective. Always provide context when introducing features or solutions.

**Example:**

* **Beginner**: "Click the **Submit** button to complete the process. This will save your settings."
* **Intermediate**: "Click **Submit** to save your settings, which will apply changes across the application."
* **Advanced**: "Click **Submit** to commit all changes; this action triggers the application to refresh with the updated configurations."

## Tone and Voice

Maintain a professional yet approachable tone, balancing instruction and encouragement without overly casual language.

* **Voice**: Use a **professional, but approachable** tone. Avoid being overly casual, but ensure the documentation remains friendly and not too rigid.
* **Tone**: Should be **instructive, clear, and encouraging**. Avoid using negative language or jargon unless required by technical accuracy.

**Example:**

* **Correct**: "Ensure that all parameters are defined before proceeding."
* **Incorrect**: "Uh-oh! It seems like something went wrong because you didn’t define all parameters."

## Active vs. Passive Voice

Use **active voice** whenever possible to make the content more direct and easier to follow. 

* **Active**: The system **displays** a confirmation message.
* **Passive**: A confirmation message **is displayed** by the system.

Also, use active voice for clarity and engagement but passive voice when the subject is less important.

**Example**:

* **Active**: Click the **Save** button to store your changes.
* **Passive**: Changes are saved automatically every 10 minutes.

Both are correct here.

## Sentence Structure

Keep sentences **short and concise**. Aim for clarity in each sentence by avoiding unnecessary complexity. Avoid run-on sentences.

**Example**:

* **Concise**: Click **Install** to begin the setup.
* **Complex**: You will need to click **Install**, which will then initiate the setup process and proceed with the installation.

## Vocabulary and Terminology

Use consistent terminology and avoid jargon unless necessary. Be **consistent** with terminology. Avoid using **slang** or **idiomatic expressions** that may not be universally understood. Introduce **technical terms** only when necessary, and provide brief explanations or links to more in-depth explanations.

**Example**:

* **Correct**: Use the **API Key** to authenticate your requests.
* **Incorrect**: Just throw in your **API** or **key** here.

# 2. Formatting Guidelines

## Headings and Subheadings

Use headings to **break down content** logically. Each heading should represent a key idea. Use **Title Case** for headings and subheadings.

**Exmaple**

* **Correct**:
  * H1: Creating an Account
  * H2: Account Settings
  * H3: Managing Account Security
* **Incorrect**:
  * H1: Start Here
  * H2: Settings Options
  * H3: Security Details

## Lists and Bullet Points

Use **bullet points** for unordered lists and **numbers** for step-by-step instructions. Keep list items **parallel** in structure (e.g., start all items with a verb).

**Example:**

* **Correct**:
  1. Open the file.
  2. Click **Save As**.
  3. Enter a filename and click **Save**.
* **Incorrect**:
  1. Open the file.
  2. Save by clicking **Save As**.
  3. Filename and Save.

## Code Blocks

Format code or commands using **monospace font** and present them in **code blocks**. Always ensure code examples are **fully tested and functional**.

## Emphasis (Bold, Italics, Underline)

* Use **bold** for UI elements, menu options, and important commands.
* Use **italics** to introduce new technical terms or emphasize key concepts.
* Avoid underlining as it suggests hyperlinks.

  * **Example**:
    * **Correct**: Click **Save** to store changes. *Webhooks* allow real-time communication.
    * **Incorrect**: Click Save to store changes. Webhooks **allow real-time communication**.

## Links

Use **descriptive links** instead of generic phrases like "click here."

**Example**:

* **Correct:** For more information, refer to the [Install SDK](#install-sdk) documentation.
* **Correct**: For more information, refer to the [our installation guide](#installation-guide).
* **Incorrect**: For more information, [click here](#).
* **Incorrect**: For more details, check out the [Documentation](#documentation).

## Notes, Warnings, and Tip

Use distinct **icons or labels** to call out important information:

* **Note**: Provides additional helpful information.
  * **Example:** Make sure the file is in the correct directory.
* **Warning**: Alerts users to a potential issue or something that could break the system.
  * **Example:** This action can not be undone.
* **Tip**: Offers a useful shortcut or enhancement to standard procedures.
  * **Example**: Use shortcut **Ctrl+S** to save quickly.

# 3. Content Structuring

## Overview and Introduction

Begin each document with a **brief introduction** to the topic or feature. Clearly state the purpose of the documentation and what the user will achieve by following it.

**Example:**

* **Correct**: This guide will help you set up webhooks for automated responses. By the end, you will know how to configure a webhook for real-time data updates.
* **Incorrect**: This is a guide about webhooks. Follow it to learn some things.

## Task-Based vs. Concept-Based Documentation

Differentiate tasks from concept explanations to improve readability and focus.

* **Task-Based Documentation**: Focus on guiding users step-by-step through specific tasks. These documents should be concise and focused on outcomes.

**Exmaple:** Follow these steps to install the software.

* **Concept-Based Documentation**: Explain broader ideas, concepts, or system functionality. These can be more in-depth and exploratory.

**Example**: Software installation refers to the process of placing and configuring a program on a device.

## Step-by-Step Instructions

Write clear, **sequential instructions** with numbers. Each step should contain a **single action** to avoid confusion.

**Example:**

1. Navigate to the **Settings** tab.
2. Under **Account**, click **Change Password**.
3. Enter your new password and click **Save**.

## Use Cases and Examples

Include **real-world use cases** or scenarios that demonstrate how the feature might be used. 

Also, provide **examples** of inputs and outputs where applicable.

**Example**:

* For a fitness app, a webhook can notify users when their step count reaches their daily goal.

## Screenshots and Diagrams

Use screenshots to illustrate steps. Label them appropriately and **provide context** for each image.

# 4. Technical Conventions

## Code and Syntax

* Ensure all code samples are correct and conform to the programming language’s conventions.
* Indent and format code for readability.
* Clearly differentiate between **user inputs** and **outputs**.

**Example**:

```javascript
function add(a, b) {
  return a + b;
}
```

### File Paths and Command Line Instructions

Always use **absolute file paths** where applicable.

**Example**:

* **Correct**: `/usr/local/bin/myapp`
* **Incorrect**: `bin/myapp`

## Error Messages

When documenting errors, explain **errors** and provide **solutions**.

**Example:**

* **Error**: *FileNotFoundException: File /path/to/file not found.*
* **Solution**: Ensure the file path is correct and that the file exists.

# 5. Grammar and Punctuation

## Common Grammar Rules

* Use the **Oxford comma** in lists.
* Avoid unnecessary use of **articles** like "a" or "the" unless needed for clarity.

## Punctuation Usage

Add **Periods** to end complete thoughts or sentences. Aso, use **colons** to introduce lists or examples.

**Example:**

* **Correct**: Ensure that you have the following: 
  * A CleverTap Account with Admin access.
  * mParticle production account with Creator access.
* **Incorrect**: Ensure that you have - a Admin access of the CleverTap account and Creator access of the mParticle production account.

# 6. Special Considerations

## Localization and Internationalization

Avoid culturally specific references or terms that may not be universally understood. Instead, use neutral, universally recognizable terms.

**Example**

* **Correct**: During peak hours, response times may vary due to increased server load.
* **Incorrect**: During rush hour, response times may vary due to increased server load.
* **Correct**: Ensure all users have the required access rights.
* **Incorrect**: Ensure all users have the necessary clearances before the weekend.

Use **international date formats** (YYYY-MM-DD) This format minimizes confusion across regional date standards.

**Example**

* **Correct**: The subscription renewal date is 2024-12-15.
* **Incorrect**: The subscription renewal date is 12/15/24. (MM/DD/YY format)

Use commas for thousands and periods for decimals to make numbers clearer for an international audience.

**Example**

**Correct**: The application supports up to 1,000,000 users simultaneously. The final price is $1,234.56.

**Incorrect**: The application supports up to 1000000 users simultaneously. The final price is $1234.56.

## Accessibility

* Ensure all images have **alt text**.
* Use **heading structures** for screen readers.
* Ensure proper **color contrast** for visibility.

# 7. Review and Editing Process

* **First Draft**: Write the initial version and check for clarity.
* **Peer Review**: Have another writer or SME (subject matter expert) review the content for accuracy.
* **Copyediting**: Check for grammar, punctuation, and style consistency.
* **Final Review**: Confirm with relevant stakeholders (e.g., Product Manager) before publishing.
