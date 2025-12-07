---
title: Style Guide for Documentation (COPY)
excerpt: >-
  Provides detailed guidelines on how to write, structure, and present technical
  documentation to ensure consistency, clarity for a
  user-friendluser-friendliness.
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

The [Style Guide](https://wizrocket.atlassian.net/wiki/x/IoJGag)includes a comprehensive list of technical terms and style guidelines, and serves as a standard for all CleverTap technical documentation. Its purpose is to standardize the documentation process and support writers and editors in producing high-quality, consistent documents across the organization. 

## References

- MSTP
- The Chicago Manual of Style

## Revision History

| Version | Date       | Comments                                                                      |
| :------ | :--------- | :---------------------------------------------------------------------------- |
| 0.1     | 09-01-2023 | First version created.                                                        |
| 0.2     | 04-03-2025 | Revamped the old structure and added new topics and content associated to it. |

# 1. General Writing Principles

## Audience Consideration

Always write with your target audience in mind. Understand their level of technical expertise: **\<Are we writing docs based on these categories?>**

- **Beginner**: Avoid jargon and explain all technical terms.
- **Intermediate**: Introduce more complex concepts but still offer background information.
- **Advanced**: Assume familiarity with core concepts but clarify anything that might be new or unusual.

Tailor your documentation to solve problems from the reader's perspective. Always provide context when introducing features or solutions.

**Example:**

- **Beginner**: "Click the **Submit** button to complete the process. This will save your settings."
- **Intermediate**: "Click **Submit** to save your settings, which will apply changes across the application."
- **Advanced**: "Click **Submit** to commit all changes; this action triggers the application to refresh with the updated configurations."

## Tone and Voice

Maintain a professional yet approachable tone, balancing instruction and encouragement without overly casual language.

- **Voice**: Use a **professional, but approachable** tone. Avoid being overly casual, but ensure the documentation remains friendly and not too rigid.
- **Tone**: Should be **instructive, clear, and encouraging**. Avoid using negative language or jargon unless required by technical accuracy.

**Example:**

- **Correct**: "Ensure that all parameters are defined before proceeding."
- **Incorrect**: "Uh-oh! It seems like something went wrong because you didn’t define all parameters."

## Active vs. Passive Voice

Use **active voice** whenever possible to make the content more direct and easier to follow. 

- **Active**: The system **displays** a confirmation message.
- **Passive**: A confirmation message **is displayed** by the system.

Also, use active voice for clarity and engagement but passive voice when the subject is less important.

**Example**:

- **Active**: Click the **Save** button to store your changes.
- **Passive**: Changes are saved automatically every 10 minutes.

Both are correct here.

## Sentence Structure

Keep sentences **short and concise**. Aim for clarity in each sentence by avoiding unnecessary complexity. Avoid run-on sentences.

**Example**:

- **Concise**: Click **Install** to begin the setup.
- **Complex**: You will need to click **Install**, which will then initiate the setup process and proceed with the installation.

## Vocabulary and Terminology

### Avoid Ambiguity

An antecedent is a word, phrase, or clause referred to by a pronoun. Avoid ambiguous  
antecedents.  
Make sure pronouns—such as this, that, and it—have clear antecedents. Frequently,  
sentences that start with This have no antecedent for the readers to relate to, or the  
antecedent is too far away for readers to understand the connection without rereading  
several sentences.  
An even more common problem with such sentences is that the  
reference is often ambiguous because two or more possible antecedents exist. This  
problem is particularly difficult for translators and non-native English speakers.

**Write**  
The tool assigns the attribute, which must be previously defined, to the cell.  
**Rather than**  
The tool assigns the attribute to the cell. It must be previously defined.

Avoid using when with a participle immediately following it: when using, when calculating,  
when doing that, and so on. In this case, ensure that the subject in the independent clause is the  
agent that performs the action denoted by the verb. The sentence might be confusing if you do not provide the correct antecedent.  
Alternatively, follow the word when with you (or another agent such as the tool) and the verb  
from which the participle is derived.

**Write**

- When reading the file, the tool validates the format.
- Before starting the tool, you must set the environment variables. (or)
- Before you start the tool, set the environment variables.
- After completing the timing analysis, the tool generates a report.

**Rather than**

- When reading the file, the format must be valid.
- Before starting the tool, the environment variables must be set.
- After executing the command, timing analysis generates a report.

### Avoid Redundancy

Redundancy can appear in several forms:  
**Redundant Pairs** – any and all, basic and fundamental, and each and  
every.  
**Redundant Modifiers **– personal opinion, initial preparation, and end result.  
**Redundant Categories**–time period, large in size, the color red, and field  
of mathematics.  
Trimming these redundant phrases down to a single word almost always results in a clearer  
and more direct sentences. The reader still knows that red is a color, the result comes at the end,  
and each also refers to every.

### Jargons and Slangs

Jargon can confuse readers, especially if it’s not specific to their field or if the term is not widely understood. Terms that have specific meanings in the computer industry can be difficult to translate accurately into other languages. To avoid such jargons, using shortened terms or industry-specific vocabulary is necessary, include definitions and explanations within the context to help both translators and readers.

Slang is the informal language of a culture—words and expressions adopted by people in a specific time and place to enhance their daily communication. Similar to jargon, slang terms are difficult to translate and can reduce the accuracy of the translation.

Use consistent terminology and avoid jargon unless necessary. Be **consistent** with terminology. Avoid using **slang** or **idiomatic expressions** that may not be universally understood. Introduce **technical terms** only when necessary, and provide brief explanations or links to more in-depth explanations.

The following examples of English computer jargon may pose challenges for translators, with alternative suggestions provided.

**Example**

- **Correct**: Use the **API Key** to authenticate your requests.
- **Incorrect**: Just throw in your **API** or **key** here.

Avoid jargons when:

- A more familiar term is available (e.g., _symbol_ instead of _glyph_).
- The term is known only to a niche audience.
- It’s not specific to software or other technical fields.

**Testing for Jargon**

- If it’s an acronym, spell it out.
- If reviewers question its use, it may be jargon.
- If the term is commonly used in general-interest publications like _The Wall Street Journal_, it might be suitable for wider audiences.

The following table lists the words that can replaced instead of jargons:

| Instead of this | Use this |
| :-------------- | :------- |
| Abort           | Stop     |
| Boot            | Start up |
| Crash           | Fail     |
| Uncheck         | deselect |

## Word Choice

To enhance readability and comprehension, selecting words thoughtfully and using them consistently throughout your content is essential. This section provides tips for making the right word choices.

### Minimalism

Write only what the user truly needs. Keep your audience in mind and leave out unnecessary information.  
Engineers often focus on technical details, but as a technical writer, your role is to prioritize clear, user-friendly guidance. Unless explaining how the system works is the main point, focus on what users can do with it, not the technicalities.

**Example**

**Write**

Need help? Contact us.

**Rather than**

If you need assistance with your order, please reach out to our support team.

### Use Contractions

If it fits the context, feel free to use common contractions like you'll, that's, we've, can't, and don't. Contractions can make writing sound more natural and conversational. When in doubt about a specific contraction, it’s best to skip it.

Contractions are not recommended because not all languages use them, making translation difficult.

Using contractions makes the writing feel more friendly and informal. However, be careful not to overuse them or choose the ones that are common. 

**Acceptable Contractions** Form contractions from pronouns and verbs (she’s, you’re,  
we’ve) and from verbs and the word not (isn’t, don’t, won’t, can’t).  
**Contractions to Avoid** Don’t form contractions from nouns and verbs. 

For example,  
Avoid constructions such as this:  
CleverTap’s going to introduce a new feature today.

Avoid contractions that may be difficult for localization such as it’ll.

**Its and it’s: **Don’t confuse it’s (the contraction for it is) with the possessive pronoun its.  
It’s important that the department keep track of its computers.

- **Avoid**: Mixing contractions with their spelled-out forms. For example, don't use _can’t_ and _cannot_ together in UI text.
- **Avoid**: Ambiguous or awkward contractions like _there’d_, _it’ll_, or _they’d_.

**Be consistent in using contractions.**

### Use US Spelling and Avoid Non-English Words

When English words differ by locale, use US spelling (for example., _license_ instead of _licence_).

- **Avoid non-English words** like _de facto_ or _ad hoc_, and Latin abbreviations unless space is limited. 

  **_Examples_**

| Instead of this | Use this    |
| :-------------- | :---------- |
| e.g.            | For example |
| i.e.            | that is     |
| viz.            | namely      |

### ** Use Simple Words and Concise Sentences**

Make every word count. Use simple, precise words and concise sentences to save space and improve clarity.

- **Avoid**: Unnecessary words or weak verbs (For example., _be_, _have_, _make_, _do_).

- **Avoid**: Vague or overly complex phrases.

  **_Examples_**

| Instead of this                       | Use this |
| :------------------------------------ | :------- |
| utilize, make use of                  | use      |
| Unload, extract, take away, eliminate | remove   |
| in order to, as a means to            | to       |
| capable of, has the ability to        | able     |
| establish connectivity                | connect  |
| see                                   | view     |

- **Omit unnecessary adverbs** (e.g., _quite_, _very_, _quickly_) unless they’re essential for meaning.

### ** Use Technical Terms Carefully**

Use technical terms only when they’re the clearest way to communicate. If a common word will suffice, use it instead.

- **Define technical terms** in context when necessary and **ensure consistency** in their use across different platforms and materials.

By following these guidelines, you can ensure your content is clear, precise, and easily understood by a wide audience.

# 2. Grammar and Mechanics

Use _Grammarly_ tool effectively to eliminate any grammatical errors.

### **Verbs**

**Verb Tense:** The present tense is typically the easiest to read and understand. It’s often the best choice for most content, as it feels more immediate. 

**Example** Windows Update installs important updates automatically- uses the present tense to clearly convey the action.

**Active vs. Passive Voice:**

Use active voice whenever possible to make the content more direct and easier to follow and where the subject actively performs the action.

**Example**

**Active **The system displays a confirmation message.  
**Passive **A confirmation message is displayed by the system.

   Also, use active voice for clarity and engagement but passive voice when the subject is less important.

**Example**

**Active **Click the Save button to store your changes.  
**Passive **Changes are saved automatically every 10 minutes.

Both are correct here.

### **Verb Agreement**

Ensure that the verb agrees with the subject in number (singular or plural).

**Example** “A variety of games is available” (singular) vs. “Facebook and Twitter are available” (plural).

### **Person**

- **Second-Person Pronouns (you, your):** These create a conversational tone and make the content feel like a direct conversation with the reader. Be careful with product UI, as you don’t want to sound like you're giving commands.  
  **Example** Change your settings.
- **First-Person Pronouns (I, me, my):** Use these sparingly. They are more common in product interfaces, where they express user control over actions. Avoid using “I” or “we” in general documentation or marketing, as it can sound distant.  
  **Example** Notify me when a new Bluetooth device tries to connect.
- **First-Person Plural Pronouns (we, us):** These are typically avoided because they can create a corporate tone. Focus on the user instead.  
  **Example**

**Write **

Change your password

**Rather than**

 We recommend that you change your password

### Nouns and Proper Nouns

Proper nouns refer to unique people, places, or things. Always capitalize proper nouns when they appear in text. 

**Proper Nouns Include:**

- Names and titles of individuals.
- Unique places, organizations, events, shows, corporate or philanthropic programs, and other distinct entities.
- Product, service, app, and tool names.
- Trademarks.
- Titles of books, songs, and other published works.
- Managed standards, such as Bluetooth.

If something has multiple examples, it’s a common noun. For instance, “chief operating officer” is a common noun because there are many people in this role, but “Chief Operating Officer Latasha Sharp” is a proper noun since it refers to a specific individual.

**Don’t capitalize common nouns** unless they are at the start of a sentence or need title-style capitalization. Many technology terms, product categories, devices, and features are common nouns, not proper nouns. For example: “cloud computing,” “smartphone,” “e-commerce,” and “open source” are all lowercase.

**Capitalize technology terms as proper nouns only when:**

You need to distinguish between a specific product and a general term.

Example  SQL Server vs. an SQL database server).

Industry conventions capitalize the term. Check reliable sources like The American Heritage Dictionary and other trusted websites, but avoid unedited sources.

If unsure whether a term should be cpitalized, consult The American Heritage Dictionary or an A–Z word list. When in doubt, use lowercase unless there’s a strong reason to capitalize.

### **Plural Nouns**

Some plural forms can be tricky. Here are simple rules to help with pluralization:

- For common and proper nouns that end in "s," add “es” (e.g., “the Johnsons”).
- For abbreviations, simply add “s” (e.g., “ISVs” for independent software vendors).
- For single letters, add an apostrophe and “s” (e.g., “x’s”).
- For numbers, add “s” (e.g., “the 1950s”).
- For variables, don’t add “s” unless necessary (e.g., “Wait for x minutes”).

### **Pronouns and Gender**

Avoid using gendered pronouns for general references. Instead, use the second person ("you") or refer to a person’s role (e.g., customer, employee, or client). It's fine to use "he," "she," or "they" when referring to real people who use those pronouns. 

In cases where you don't know someone’s gender, "they" can be used as a singular, non-binary pronoun.

**Pronouns with Collective Nouns:**  
A collective noun (like "company") takes a singular pronoun. Don’t use a plural pronoun (e.g., “they”) when referring to collective nouns unless you're emphasizing the individuals within the group.

**Examples:**

- "The company upgraded its cloud storage solution to Microsoft Azure."
- "Meet with up to 250 people. All they need is a phone or internet connection."

### **Words Ending in -ing**

Words ending in "-ing" can serve as verbs, nouns, or adjectives. Be careful and make sure the sentence clearly shows the role of the word. 

For instance:

- **"The meeting requirements"** (noun)
- **"Meeting the requirements"** (verb)
- **"The requirements for the meeting"** (noun)
- **"How to meet the requirements"** (verb)

### **Prepositions**

A prepositional phrase consists of a preposition and a noun that provides additional information about other parts of the sentence. For example, in “The reading pane displays the content of the selected message,” the phrase "of the selected message" describes “content.”

Avoid using too many prepositional phrases in one sentence, as long chains can be confusing and hard to follow. If possible, end sentences with prepositions if it makes the sentence more readable.

**Examples:**

- "Use a different instrumentation key for each environment that your application runs in."
- "Specify which event hub you want to send the data to."

### **Dangling and Misplaced Modifiers**

Modifiers are words or phrases that describe other words or phrases in the sentence. Always position modifiers so it's clear what they are modifying. 

- A **dangling modifier** is one that doesn’t modify anything in the sentence.
- A **misplaced modifier** is one that’s too far from the word it should modify or too close to something else that it might mistakenly modify.

Having sentences simple and in active voice, you can avoid both dangling and misplaced modifiers.

## Articles

Articles are usually described as certain kinds of adjectives. There are only three: a, an, and the. A and an are known as indefinite articles, the as a definite article. 

- Use "a" before words starting with a consonant sound (a network, a user).
- Use "an" before words starting with a vowel sound (an update, an hour).
- Use "the" to refer to a unique or previously mentioned entity (the server, the cloud infrastructure).

Importance of articles in writing helps readers and translation software identify nouns and modifiers in a sentence.  
**_Example_**

- Empty the container.
- The empty container.

Do not capitalize an article in titles and headings unless it is the first word in the title. However, avoid using an article as the first word in a title or heading. 

Avoid starting list items with articles (a, an, the) in technical writing.

Do not start captions with articles (Avoid "The front panel view." Instead, write "Front panel view.").

## Punctuation

Punctuation plays a crucial role in helping readers understand the meaning of a sentence. While it follows established rules, there are also stylistic choices to consider. For example, every English sentence needs to end with punctuation, except in titles and headings. The more punctuation you use, the more complex the sentence becomes. If a sentence contains more than a couple of commas or other punctuation, consider rewriting it to make it simpler and clearer.

This section covers various punctuation topics:

- Formatting punctuation in text that references UI interactions, parentheses, and brackets
- Apostrophes used in possessives and contractions
- Colons used for lists or to elaborate on statements
- Commas in lists, clauses, and dates
- Dashes and hyphens, including em dashes for setting off phrases, en dashes for ranges, and hyphens for compound words
- Ellipses for omissions or pauses
- Exclamation points (used sparingly)
- Periods in sentences and lists
- Question marks (used sparingly)
- Quotation marks for direct quotations
- Semicolons in independent clauses, contrasting statements, and lists
- Slashes for phrases, file paths, and URLs

### Formatting Punctuation

Generally, format punctuation in the same font style as the rest of the sentence.

#### Text Describing UI Interaction

When referencing commands, options, keywords, placeholders, links, pop-up text, or user input:

- If the punctuation is part of the UI element, format it the same as the element.  
  Example: "Enter Balance due: in cell A14" (The colon is bold because it is part of the user input).
- If the punctuation isn't part of the element, format it the same as the main text.  
  Example: "On the Insert menu, go to Pictures, and then select From File." (The comma and period are not bold because they aren't part of the UI elements.)

#### Parentheses and Brackets

Use the same font for parentheses and brackets as you do for the main text.

Example: "Open any Office app and select File > Account. (If you're using Outlook, select File > Office Account.)" (The parentheses are not bold.)

### Apostrophes

Apostrophes are used to:

1. Form possessives for singular nouns (add an apostrophe + s), even if the noun ends in s, x, or z.  
   Examples: _insider's guide_, _the box's contents_
2. Indicate missing letters in contractions.  
   Examples: _can't_, _don't_, _it's_

Do **not** use an apostrophe for:

- The possessive form of _it_.  
  Example: _Replace a formula with its calculated value_ (not _it's_).
- Possessive pronouns.  
  Example: _The choice is yours_ (not _your's_).
- To form the plural of a singular noun.  
  Example: _Play your favorite games on all your devices_ (not _device's_).

### Colons

- Use a colon to introduce a list after a statement.  
  Example: _You can create a backup of many things, including:_
  - The apps you've installed on your phone.
  - The passwords for your accounts.

- Use a colon to elaborate on a statement, but don't overuse them in a sentence.  
  Example: _Microsoft ActiveSync doesn't recognize this device for one of two reasons: the device wasn’t connected properly, or it isn’t a smartphone._

- After a colon, lowercase the first word unless it’s a proper noun or a direct quotation.  
  Example: _We're considering three cities for the event: Los Angeles, Munich, and Tokyo._

### Commas

- Use a comma before the conjunction in a list of three or more items (Oxford or serial comma).  
  Example: _Outlook includes Mail, Calendar, People, and Tasks._

- Use a comma after introductory phrases.  
  Example: _With the Skype app, you can call any phone._

- Use commas to join independent clauses with conjunctions (and, but, or, so).  
  Example: _Select Options, and then select Enable fast saves._

- Do not use a comma between independent clauses without a conjunction. Use a semicolon instead.  
  Example: _Select Options; then select Enable fast saves._

- Don’t use a comma between verbs in a compound predicate.  
  Example: _The program evaluates your computer system and then copies the essential files._

### Dashes and Hyphens

- **Em Dashes**: Use to set off or emphasize a phrase within a sentence. Do not add spaces around the em dash.  
  Example: _The information in your spreadsheet—numbers, formulas, and text—is stored in cells._

- **En Dashes**: Use for ranges (numbers, dates), negative numbers, and compound modifiers.  
  Example: _2015–2017_ (range), _12 – 3 = 9_ (minus sign).

- **Hyphens**: Use to join words or connect prefixes to words. Don't use two hyphens in place of an em dash.  
  Example: _built-in drive_, _high-level-language compiler_.

### Quotation Marks

Avoid using quotation marks (“ ”) unless they are part of a user input, a standards document,  
graphical user interface, or code samples:  
**_Example_**

/_Declare the string to have length of “constant +1”._/

> 📘 Note
> 
> If you do use quotation marks, remember that in US English they should be placed  
> outside commas and periods:
> 
> I can never remember how to spell  
> “bureaucracy.”

### Compound Modifiers and Hyphenation

- Do not hyphenate predicate adjectives (adjectives that follow linking verbs), unless specifically stated.  
  Example: _The text is left aligned._

- Hyphenate compound words before a noun.  
  Example: _high-level-language compiler_, _read-only memory_.

- Do not use suspended compound modifiers unless space is limited. Use the full phrase instead.  
  Example: _upper-right or lower-right corner_.

### Prefixes

- Avoid using hyphens after certain prefixes (auto-, co-, cyber-, etc.), unless the hyphen clarifies meaning.  
  Example: _non-native_, _pre-provisioned_.

- Capitalize parts of hyphenated compound words that would be capitalized if there were no hyphen.  
  Example: _Windows 10–compatible products_.

By following these punctuation and capitalization rules, you'll enhance clarity and readability in your writing.

## Capitalization

Microsoft style uses **sentence-style capitalization**, which means that only the first word of a sentence and proper nouns (such as names of brands, products, or services) are capitalized. Everything else should be lowercase. Given that Microsoft has over 500 products and services, it's important to reserve capitalization only for product and service names to help customers easily identify them.

Here are the key guidelines for Microsoft content:

- **Sentence-style capitalization** is preferred for most cases.
  - Capitalize the first word of a sentence, heading, title, UI label (like a button or checkbox), or standalone phrase.
  - Capitalize proper nouns (e.g., names of people, places, or products).
  - Everything else should be lowercase.

- Always capitalize the **first word** of a new sentence. Avoid starting sentences with words that should remain lowercase unless absolutely necessary.

- **Avoid using all uppercase** for emphasis. Instead, you may use **italic text** sparingly for emphasis.

- **Don't use all lowercase** as a design choice, even though all uppercase may occasionally be used for design purposes.

- **Avoid internal capitalization** (e.g., "AutoScale" or "e-Book") unless it’s part of a brand name.

- Don’t capitalize the spelled-out form of an acronym unless it’s a proper noun.

- When words are connected by a slash, capitalize the word after the slash if the word before the slash is capitalized.

  **Examples**:

  - Country/Region
  - Turn on the On/Off toggle

- If you're unsure about whether to capitalize a term, refer to the **A–Z word list** and **The Chicago Manual of Style**.

### Capitalization in Titles and Headings

- **Use sentence-style capitalization** in most titles and headings:

  - Capitalize the first word and lowercase the rest.
  - **Exceptions**: Proper nouns (including brand, product, and service names) are always capitalized. Also, if a title or heading contains a colon, capitalize the first word after it.

  **Examples**:

  - Watch your favorite HD movies, TV shows, and more.
  - 1 TB of cloud storage.
  - Choose the Office version that's right for you.

- **Title-style capitalization**: Occasionally, title-style capitalization (capitalizing most words) is appropriate. This is typically used for the titles of products, services, blogs, songs, books, and articles in citations. In these cases, the first and last words should always be capitalized, but avoid capitalizing short prepositions (e.g., "on," "to," "in") or conjunctions unless they are the first or last word in the title.

  **Examples of Title-Style Capitalization**

  - A Home to Go Back To
  - Microsoft on the Issues
  - The Official Microsoft Blog

- **Do not capitalize** small prepositions (on, to, in, up, down, of, for) unless they are the first or last word. Similarly, do not capitalize conjunctions like and, but, or, nor, unless they are the first or last word.

  **Example**:

  - Achieving Excellence in the Classroom Through Technology

- **For hyphenated words**, capitalize the second word if it would be capitalized without the hyphen or if it’s the last word of the title.

  **Examples**:

  - Self-Paced Training for Microsoft Visual Studio
  - Copy-and-Paste Support in Windows Apps

- For **UI labels and programming terms**, follow the traditional capitalization used in programming languages. For instance, capitalize the first word of labels and terms that appear in the UI unless they are always lowercase (like "fdisk").

## Abbreviations, Acronyms, and Initialisms

Avoid two-letter abbreviations, acronyms, and initialisms unless they are widely recognized industry terms.  
Do not create new abbreviations, acronyms, or initialisms without consulting the Style Team.  
Never use an acronym or abbreviation where CleverTap is shortened to the letter CT.

### Abbreviations

An abbreviation is a shortened form of a word or phrase (e.g., cont. for continued). Once introduced, use abbreviations consistently. In text, avoid using no. to represent "number," but it is acceptable in figures and tables.  
Use abbreviations in job aids where space is limited (e.g., in. for inch). 

### Acronyms and Initialisms

An acronym is a combination of the first letters of several words, forming a term that can be pronounced as a word.  
An initialism is a combination of the first letters of words, pronounced separately. Introduce acronyms and initialism at the first instance 

# 3. Formatting Guidelines

## Headings and Subheadings

### Writing Headings

Think of headings as an outline—just more engaging. If readers don't engage with the headings, they are unlikely to read the content that follows. Use concise headings and subheadings to describe and highlight each section.

Use headings to **break down content** logically. Each heading should represent a key idea.

Headings provide structure and visual cues, helping readers quickly scan and navigate content. Consistency in using headings is crucial whether you're writing UI, web content, marketing materials, or advertising.

**_Examples_**

**Correct**

- H1: Creating an Account
- H2: Account Settings
- H3: Managing Account Security

**Incorrect**

- H1: Start Here
- H2: Settings Options
- H3: Security Details

**Top-level headings** must clearly communicate the most important points and divide the content into major sections. Make them specific enough to grab the reader's attention.

- If the content under a top-level heading is lengthy, break it into more digestible sections with **second-level headings (subheads)**. However, only use subheads if you can identify at least two distinct topics. If not, avoid them.

- Don’t place two headings in a row without content in between—this can indicate poor organization or redundancy. Don't insert filler text just to separate headings.

- Each new heading introduces a new or more specific topic. Make sure it piques interest and clearly introduces that topic.

- **Use headings judiciously**. For shorter content, one heading level may be enough. For longer content, consider adding additional heading levels—this guide, for example, uses four.

- Keep headings **short** and ensure the most important idea is at the beginning. This is especially important in blogs and social media.

- **Be as specific as possible**. Lower-level headings should be more detailed than higher-level ones. For example, a second-level heading should provide more detail than a first-level heading.

- Focus on **what matters to customers** and use the language they would use. Avoid focusing on products, features, or commands in headings. Instead, emphasize what the customers can achieve or what they need to know.

- Use **parallel sentence structure** across headings at the same level. 

  - First-level headings: Use noun phrases (for example., **Source data**).
  - Second-level headings: Use verb phrases (for example., **Prepare headings**).
  - Instructional headings: Use infinitive phrases (for example., **To create a heading**).

  **Examples**

  - Source data
  - Prepare headings
  - To create a heading

- **Avoid using ampersands (&)** or plus signs (+) in headings unless they're part of the UI or space is constrained.

- **Avoid hyphens** in headings when possible, as they can result in awkward line breaks on smaller screens or mobile devices.

- Use **"vs."** (not "v." or "versus") in headings.

- Do not go beyond level-five headings. 

- Do not repeat the exact text of higher-level headings in subheads later in the document.

- Do not use italics in headings.

- **Avoid colons** in any heading level.

### Formatting Headings

- Apply **Title case** to headings. .

  **Examples**:

  - Say hello to Surface Pro
  - Set up the Deployment Environment

- **Do not end headings with a period**. If necessary, use a question mark or, in rare cases, an exclamation point.

  **Examples**:

  - Not seeing what you want?
  - What can we help you find?

- **Use italics** for emphasis if needed, just as you would in the body text.

- When a heading spans two lines, break it thoughtfully. Consider the screen size and avoid awkward line breaks. If you're not working with responsive design, break the heading where it makes the most sense.

  - Keep adjectives and prepositions with the words they modify.
  - Keep hyphenated words or proper nouns (e.g., **New York**) together.
  - Ideally, break after punctuation or at the end of a complete phrase.
  - If a heading doesn’t fit on two lines, consider rewriting it.

- **Use vertical spacing** to make headings stand out. This usually means extra space above the heading and less space below it. Keep the heading closely spaced with the content to signal their connection. Use built-in heading styles in templates for consistent spacing.

- **Don’t use extra line breaks** for spacing, especially in web content. In responsive design, extra breaks can mess with how content appears on different screen sizes.

### Run-in Headings

If you regularly highlight specific content, such as benefits, tips, or warnings, consider using **run-in headings**. These bold headings, which are part of the paragraph, don’t add extra white space but still draw attention to important information. They are ideal for highlighting short blurbs, web content, or callouts.

- **Make the first few words of a run-in heading engaging** and relevant to the paragraph's content.
- Common phrases like **Tip**, **Note**, and **See also** can work well as run-in headings for emphasizing helpful or non-essential information.

For consistency, use **character styles** instead of manual formatting. This allows you to easily apply and maintain heading styles across documents. In Microsoft Word, for instance, you can apply styles like **Subtle Emphasis** by selecting the text and adding the appropriate style.

## Lists and Bullets

Lists are a great way to organize and present complex information. Lists are an effective way to present complex information in a way that's easy to scan. Use **bullet points** for unordered lists and **numbers** for step-by-step instructions. Keep list items **parallel** in structure. Make the purpose of the list clear by introducing it with a heading, complete sentence, or a fragment that ends with a colon.

### Numbered Lists

Use numbered lists for sequential steps (such as a procedure) or when items are prioritized.

**_Examples_**  
To sign on to a database:

1. On the File menu, select **Open database**.
2. Enter your username.
3. Enter your password and select **OK**.

**_Examples_**

- **Correct**
  1. Open the file.
  2. Click **Save As**.
  3. Enter a filename and click **Save**.
- **Incorrect**
  1. Open the file.
  2. Save by clicking **Save As**.
  3. Filename and Save.

### Bulleted Lists

Use bulleted lists for items that share a common theme but don’t need to appear in any particular order. 

**_Examples_**  
The database owner can:

- Create and delete a database.
- Add, delete, or modify a document.
- Modify any information in the database.

**_Examples_**

- Bring your customers into focus.
- Own your customer relationship.
- Create raving fans.
- Engage in new ways.

Here are some best practices:

- A list must contain **at least two items**, but no more than seven. Each item must be short enough for the reader to see at least two or three items at a glance. It’s acceptable to have a few short paragraphs as list items, but avoid long explanations.

- **Keep the number of items between two and seven**. Each item should be short enough that the reader can see at least two or, ideally, three items at once. You can include a couple of short paragraphs within a list item, but don’t do this too frequently.

- **Maintain consistency** in the structure of the list. For example, each item should be a noun or a phrase starting with a verb.

- **Maintain consistency** in list structure. For example, each item should either be a noun or a phrase that starts with a verb.

- **Use bulleted lists** for items that share something in common but don’t require a specific order.

  **Example**:  
  The database owner can:

  - Create and delete a database.
  - Add, delete, or modify a document.
  - Modify any information in the database.

By following these guidelines for headings, formatting, and lists, your content is easier to scan and more engaging for readers.

#### Capitalization and Punctuation

- Start each list item with a capital letter unless there's a reason not to (For example, a command that is always lowercase). If required, rewrite the list items so they are all capitalized or all lowercase.
- Do not use semicolons, commas, or conjunctions (like "and" or "or") at the end of list items.
- Do not use periods at the end of list items unless they are complete sentences. Even if the sentence is very short, avoid a period unless necessary.

#### Special Cases for Periods

If the list is introduced by a sentence fragment that ends with a colon, use periods at the end of each item if any item forms a complete sentence when combined with the introduction. 

**_Examples_**  
Knowledge managers can:

- Confirm or remove topics that were discovered in your tenant.
- Create new topics manually as needed.
- Edit existing topic pages.

However, **do not use periods** if all the list items have three or fewer words or if the items are UI labels, headings, subheadings, strings, or similar short text.

**_Examples_**

- The administrative templates for Microsoft Edge are:
  - msedge.admx
  - msedgeupdate.admx

- The topic answer displays:
  - The topic name
  - Alternate names
  - The definition

## Tables

Tables organize complex information into rows and columns, making it easier to understand. Use tables when presenting data, simple instructions, categories with examples, or collections with multiple attributes. Avoid using tables for lists of similar items; a list would work better.

#### Key Guidelines

- **Purpose**: Clearly define the purpose of the table. Include a title or brief introduction if needed.

- **Row Identification**: Place identifying information in the leftmost column.

- **Consistency**: Ensure entries are parallel (e.g., all nouns or all verbs).

- **Empty Cells**: Don’t leave cells blank or use em dashes. Use “Not applicable” or “None” instead.

- **Responsive Design**: Keep text brief (ideally one line per cell) and limit column numbers. Adjust column width for text-heavy data.

#### Header Rows

- **Header Design**: Make header rows stand out (larger, bold, or a different color).
- **Specificity**: Be precise with column headers  ("Group" instead of "Name").
- **Visibility**: Ensure the header row is always visible, especially in long tables (example, fixed header on the web or repeat headers in documents).

#### Capitalization and Punctuation

- Use **sentence-style capitalization** for table titles, column headers, and text within cells unless there's a reason to use lowercase.
- **Punctuation**: If the table is introduced by text, end it with a period, not a colon. Use punctuation in cells only if they contain complete sentences.

#### Code Blocks

Format code or commands using **monospace font** and present them in **code blocks**. Always ensure code examples are **fully tested and functional**.

## Numbers

### General Number Formatting

- Spell out numbers zero through nine; use numerals for 10 and greater.  
  **Example **five databases, 10 screen savers
- Use numerals for time, measurements, and UI values even when the number is less than 10.  
  Example: 3 feet, 1.76 lb, 6:30 PM.
- Do not start a sentence with a numeral; rewrite or spell it out.  
  **Example **Eleven apps are included instead of 11 apps are included.
- Commas and Large Numbers  
  Use commas in numbers with four or more digits (e.g., 1,024; 10,000).  
  **Exception **Do not use commas in page numbers, addresses, years, pixels, or baud rates.  
  **Example **2500 B.C.; 1920 × 1080 pixels.
- Ordinal Numbers  
  Always spell out ordinal numbers (first, second, twentieth).  
  Do not use "1st, 2nd, 3rd" except in tables or figures.  
  **Example **the twenty-first anniversary.
- Ranges of Numbers  
  Use "to" for number ranges in text (e.g., 10 to 20).  
  Use an en dash (–) for number ranges in tables and job aids (e.g., 10–20).  
  For adjacent numbers, spell out one to avoid confusion.  
  **Example **six 1/2-inch cables.
- Fractions and Decimals  
  Spell out simple fractions (one-half, two-thirds), but use numerals in figures and tables.  
  Use a zero before decimal values less than one (e.g., 0.75 inches, 0.5 cm).  
  Do not use a slash for fractions unless in an equation (e.g., ½ + ½ = 1 is okay).
- Negative Numbers and Mathematical Signs  
  Use an en dash (–) for negative numbers (e.g., –64).  
  Use en dashes surrounded by spaces for mathematical operations (e.g., 10 – 9 = 1).  
  Use ± (plus/minus symbol) when indicating a range (e.g., ±5% tolerance).

## Emphasis (Bold, Italics, Underline)

- Use **bold** for UI elements, menu options, and important commands.
- Use **italics** to introduce new technical terms or emphasize key concepts.
- Avoid underlining as it suggests hyperlinks.

  - **Examples**
    - **Correct** Click **Save** to store changes. _Webhooks_ allow real-time communication.
    - **Incorrect** Click Save to store changes. Webhooks **allow real-time communication**.

## Cross-Referencing, Links, and Citations

- **Cross-Referencing** Best practices for internal and external references.
- **Citing Sources **When and how to cite sources, with examples.
- **Linking **Guidelines for internal hyperlinks and external URLs.

Use **descriptive links** instead of generic phrases like "click here."

**_Examples_**

- **Correct** For more information, refer to the [Install SDK](#install-sdk) documentation.
- **Correct** For more information, refer to the [our installation guide](#installation-guide).
- **Incorrect** For more information, [click here](#).
- **Incorrect** For more details, check out the [Documentation](#documentation).

## Notes, Warnings, and Tip

Use distinct **icons or labels** to call out important information:

- **Note**Provides additional helpful information.
  - **Example** Make sure the file is in the correct directory.
- **Warning** Alerts users to a potential issue or something that could break the system.
  - **Example** This action can not be undone.
- **Tip**Offers a useful shortcut or enhancement to standard procedures.
  - **Example**: Use shortcut **Ctrl+S** to save quickly.

# 4. Content Structuring

## Overview and Introduction

Begin each document with a **brief introduction** to the topic or feature. Clearly state the purpose of the documentation and what the user will achieve by following it.

**_Example_**

- **Correct**: This guide will help you set up webhooks for automated responses. By the end, you will know how to configure a webhook for real-time data updates.
- **Incorrect**: This is a guide about webhooks. Follow it to learn some things.

## Task-Based vs. Concept-Based Documentation

Differentiate tasks from concept explanations to improve readability and focus.

- **Task-Based Documentation**: Focus on guiding users step-by-step through specific tasks. These documents should be concise and focused on outcomes.

**_Example_** Follow these steps to install the software.

- **Concept-Based Documentation**: Explain broader ideas, concepts, or system functionality. These can be more in-depth and exploratory.

**_Example_** Software installation refers to the process of placing and configuring a program on a device.

## Step-by-Step Instructions

Write clear, **sequential instructions** with numbers. Each step should contain a **single action** to avoid confusion.

**_Examples_**

1. Navigate to the **Settings** tab.
2. Under **Account**, click **Change Password**.
3. Enter your new password and click **Save**.

## Use Cases and Examples

Include **real-world use cases** or scenarios that demonstrate how the feature might be used. 

Also, provide **examples** of inputs and outputs where applicable.

**_Examples_**

- For a fitness app, a webhook can notify users when their step count reaches their daily goal.

## Screenshots and Diagrams

Use screenshots to illustrate steps. Label them appropriately and **provide context** for each image.

# 5. Technical Conventions

## Code and Syntax

- Ensure all code samples are correct and conform to the programming language’s conventions.
- Indent and format code for readability.
- Clearly differentiate between **user inputs** and **outputs**.

**Example**:

```javascript
function add(a, b) {
  return a + b;
}
```

### File Paths and Command Line Instructions

Always use **absolute file paths** where applicable.

**Example**:

- **Correct**: `/usr/local/bin/myapp`
- **Incorrect**: `bin/myapp`

## Error Messages

When documenting errors, explain **errors** and provide **solutions**.

**Example:**

- **Error**: _FileNotFoundException: File /path/to/file not found._
- **Solution**: Ensure the file path is correct and that the file exists.

# 6. Special Considerartions

## Localization and Internationalization

CleverTap serves customers globally, who speak various languages and come from diverse cultural backgrounds. This section offers guidance on creating content suitable for worldwide communication.

It’s important to recognize that your content will likely be read by people in different countries, many of whom may not speak English as their primary language. Additionally, some content will likely be translated into other languages or localized for specific regions.

- **Translation** refers to changing content from one language to another, often through machine translation.
- **Localization** involves adapting content (including text and other elements) to meet the language, cultural, and political needs of a specific region. Localization is typically done by professionals who understand the local language and culture.

This section provides tips for creating content that works well for global audiences using English and helps streamline the processes of localization and machine translation. A few exceptions to the usual Microsoft voice and style guidelines are included to account for these needs.

Avoid culturally specific references or terms that may not be universally understood. Instead, use neutral, universally recognizable terms.

**Example**

- **Correct**: During peak hours, response times may vary due to increased server load.
- **Incorrect**: During rush hour, response times may vary due to increased server load.
- **Correct**: Ensure all users have the required access rights.
- **Incorrect**: Ensure all users have the necessary clearances before the weekend.

Use **international date formats** (YYYY-MM-DD) This format minimizes confusion across regional date standards.

**Example**

- **Correct**: The subscription renewal date is 2024-12-15.
- **Incorrect**: The subscription renewal date is 12/15/24. (MM/DD/YY format)

Use commas for thousands and periods for decimals to make numbers clearer for an international audience.

**Example**

**Correct**: The application supports up to 1,000,000 users simultaneously. The final price is $1,234.56.

**Incorrect**: The application supports up to 1000000 users simultaneously. The final price is $1234.56.

## Accessibility

- Avoid using directional terms like "left" or "right" as the sole indication of location. People with cognitive disabilities, as well as those who are blind and use screen readers, may struggle to interpret these terms. It's acceptable to use directional terms when another clue to the location is also provided, such as in the "Save As" dialog box, on the Standard toolbar, or in the title bar.

# 7. Review and Editing

## Process

- **First Draft**: Write the initial version and check for clarity.
- **Self Review**: Writer must ensure that the draft is thoroughly reviewed by self referring to the self review    checklist (link for self-review checklist to be provided).
- **Technical Review**: Writer must share the draft to relevant SME (subject matter expert) to ensure technical accuracy.
- **Peer Review**: After technical review, writer can share the draft with the peer to review the content for accuracy. The peer reviewer reviews the document referring to the [Peer Review Checklist](https://wizrocket.atlassian.net/wiki/spaces/PMM/pages/2219671652/Peer+Review+Checklist)based on the following:
  - Editorial Check- for style, tone, and terminology consistency.
  - Technical Check- for technical accuracy of the content.
  - Version Control- for managing appropriate versions.
- **Final Review**: Confirm with relevant stakeholders (for example, Product Manager) before publishing.