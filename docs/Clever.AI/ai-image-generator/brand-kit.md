---
title: Brand Kit
excerpt: Learn how to set up a consolidated Brand Kit in AI Designer Agent.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

The **Brand Kit** helps ensure consistency across all generated assets, including copy and creative, and serves as a brand governance framework that defines your brand logos, colors, tone, and buttons. Once configured, these settings are automatically applied across AI tools (Designer and Copywriter agents), ensuring a unified branding experience in every campaign.

> 📘 Private Beta
>
> Currently, this feature is released in Private Beta. If you want to access this feature, contact your Customer Success Manager.

The following are the benefits of using a Brand Kit for your assets:

* Automatic application of brand-specific colors, typography, and button styles. 
* Consistent look and feel across all content and visuals.
* Faster approvals and campaign iterations. 
* Easy scaling of campaigns while preserving brand recognition.
* Smarter content reuse with Campaign Lookback, enabling AI to learn from past campaign language and styles.
* Reduced dependency on the Copy and Design teams, enabling faster campaign iterations.

> 📘 **Modifying Brand Kit**
>
> Any updates made to a Brand Kit apply automatically across AI Copywriter and Designer Agent once published.

# Accessing Brand Kit

You can access and manage Brand Kits from the Content Manager section of your account. Only users with CMS Brand Kit access can view or edit Brand Kits. Brand Kit permissions are managed through CMS role-based access control (RBAC) as follows:

| Role Type                                                 | Default Access | Description                                                                                                    |
| --------------------------------------------------------- | -------------- | -------------------------------------------------------------------------------------------------------------- |
| Admin                                                     | Read and Write | Full control to create, edit, clone, or delete Brand Kits. Changes apply across all AI tools once published.   |
| System Roles                                              | Read-only      | Can view Brand Kits but cannot edit or create new ones.                                                        |
| Custom Roles (for example, Content Manager, Content Head) | Configurable   | Access can be customized based on organizational needs. Admins can enable or restrict Create/Edit permissions. |

## Brand Kit Access in Teams

Team-based Brand Kit access is currently available in Private Beta and visible only to accounts with Teams enabled. For more information on how Teams works, refer to [Teams Setup](https://docs.clevertap.com/docs/teams-setup). 

| User Scenario                       | Brand Kit Visibility                                       | Description                                                                                                                                                                                                                       |
| ----------------------------------- | ---------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Team A user (Teams enabled)**     | Team A kits + kit with all teams access                    | Can access Brand Kits assigned to their team, as well as any kit with all teams access available across the account.                                                                                                              |
| **Team B user (Teams not enabled)** | Kit with all teams access                                  | Can view and use only the global Brand Kits configured at the account level.                                                                                                                                                      |
| **Admin user**                      | Kits for their logged-in team + kits with all teams access | Admins can view all Brand Kits assigned to the team they are currently logged in with, along with any kits that have all teams access. Admins cannot view kits exclusive to other teams unless logged in with that specific team. |

# Create Brand Kit

Admins and content owners define elements such as logos, brand colors, button styles, and content guidelines to ensure that every AI-generated asset aligns with your brand identity.

To create a new Brand Kit, perform the following steps:

1. Go to *Content Manager* > *Brand Kit* and click **Add Brand Kit**. 

<Image alt="Add Brand Kit" align="center" border={true} src="https://files.readme.io/ff5a845b1c5609c09b13c0208e9c02c23ba4279706f9364e99f3915a9471763b-Screenshot_2025-12-03_at_1.12.58PM.png">
  Add Brand Kit
</Image>

2. Enter the brand details such as *Setup, Content Guidelines, and Image Guidelines* and click **Create**.

<br />

<Image alt="Create Brand Kit" align="center" width="65% " border={true} src="https://files.readme.io/548eaa09b6a7d5a205a8c05c4ece1c0231da09853628eabe8baae985c62757b9-image.png">
  Enter Brand Kit Details
</Image>

## Brand Kit Fields

Refer to the following table for details on the brand kit fields:

<Table align={["left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Required/Optional
      </th>

      <th>
        Description
      </th>

      <th>
        Notes
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Name**
      </td>

      <td>
        Required
      </td>

      <td>
        The display name for the Brand Kit. It must start with a letter. Supports letters, numbers, underscores, hyphens, parentheses, and spaces (limit: 150 characters).
      </td>

      <td>
        This is the only mandatory field. All other fields are optional.
      </td>
    </tr>

    <tr>
      <td>
        **Lock Brand Kit**
      </td>

      <td>
        Optional
      </td>

      <td>
        When turned on, this prevents users from editing brand settings in campaign flows. Locking ensures brand consistency across global teams and eliminates off-brand variations.
      </td>

      <td>
        If you want every AI-generated image or content asset to strictly follow brand guidelines, you can lock the Brand Kit. Prompts that conflict with brand settings will automatically use the brand-defined option. For example, if your Brand Kit defines a red primary color and a user’s prompt requests a blue background, the AI will use red. Only admins can unlock or update a locked kit.
      </td>
    </tr>

    <tr>
      <td>
        **Campaign Lookback**
      </td>

      <td>
        Optional
      </td>

      <td>
        Determines how far back the AI can reference past campaigns to maintain tone, language, and visual consistency.
      </td>

      <td>
        Options: 3 Months, 6 Months (default), or 1 Year.
      </td>
    </tr>

    <tr>
      <td>
        **Creativity Level**
      </td>

      <td>
        Optional
      </td>

      <td>
        Controls how much creative variation the AI introduces based on insights from your past campaigns. A higher creativity level allows the AI to draw broader inspiration from previous messaging and design styles, while lower levels maintain closer alignment with your brand kit settings.
      </td>

      <td>
        * \*Low:**AI adheres closely to your Brand Kit (safe, consistent).<br />**&#x4D;edium:**Balanced — allows small creative deviations for variety.<br />**&#x48;igh:\*\* Gives AI more freedom to explore alternate tones or visuals.
      </td>
    </tr>

    <tr>
      <td>
        **Tone (Brand Tonality)**
      </td>

      <td>
        Optional
      </td>

      <td>
        Defines tone and voice for AI-generated content. Allows multiple tone selections.
      </td>

      <td>
        Up to 3 tones can be selected (for example, Friendly, Professional, Confident).
      </td>
    </tr>

    <tr>
      <td>
        **Instructions (Content Guidelines)**
      </td>

      <td>
        Optional
      </td>

      <td>
        Provides writing and language guidance for AI-generated text.
      </td>

      <td>
        Example: “Use active voice, prefer ‘affordable’ over ‘cheap,’ avoid gendered or racial terms.”
      </td>
    </tr>

    <tr>
      <td>
        **Brand Logos**
      </td>

      <td>
        Optional
      </td>

      <td>
        Add up to 3 logo variations to maintain consistent visual branding.
      </td>

      <td>
        You can upload via **URL** or select from the **Content Manager**. Supported file types: `.png`, `.jpeg`, `.jpg`, `.pdf` (Max size: 2 MB per file).
      </td>
    </tr>

    <tr>
      <td>
        **Brand Colors**
      </td>

      <td>
        Optional
      </td>

      <td>
        Define up to 5 primary brand colors.
      </td>

      <td>
        Default: White (#FFFFFF). Used as base colors for visuals.
      </td>
    </tr>

    <tr>
      <td>
        **Button Colors**
      </td>

      <td>
        Optional
      </td>

      <td>
        Add up to 3 button colors used in AI-generated creatives.
      </td>

      <td>
        Default: Black (#000000). Used for CTAs or highlights in campaign visuals.
      </td>
    </tr>

    <tr>
      <td>
        **Instructions (Image Guidelines)**
      </td>

      <td>
        Optional
      </td>

      <td>
        Defines guidance for how visuals should represent the brand.
      </td>

      <td>
        Example: “Use minimal design, clean layouts, and product-first focus. Avoid excessive gradients or heavy shadows.”
      </td>
    </tr>
  </tbody>
</Table>

> 📘 Note
>
> * Maximum **10 Brand Kits** can be configured per account.
> * Each Brand Kit is stored at the **account level** and applies across all channels once enabled.
> * Create separate Brand Kits for each brand, sub-brand, or seasonal campaign.
> * Use meaningful kit names. For example, Diwali Offers, Luxe Collection, and so on.

# Manage Brand Kits

From the **Brand Kit** page, you can:

* View all existing Brand Kits in a list or grid view.
* Edit, rename, or delete kits.
* Reassign a kit to a different team (for example, from **Team A** to **Global**).
* Duplicate an existing kit to create a variant.

## Edit Brand Kit

To edit an existing Brand Kit, perform the following steps:

1. Click ![](https://files.readme.io/213881709f49a2867e2c7698fc0b3ecf1f750323d98d98a4431a8425b1413af7-ellipses_icon.png) icon and select *Edit*. 

<Image alt="Edit Brand Kit" align="center" width="80% " border={true} src="https://files.readme.io/111ba1fbe586d322e7c3d314792991e6aecfec6f837694d1d0a543b1057f0628-Edit_Brand_Kit.png">
  Edit Brand Kit Details
</Image>

2. Modify the required details and click **Save**.

<Image alt="Edit Setup" align="center" width="65% " border={true} src="https://files.readme.io/92e5631734e738d49ea5da226e1ef5da88c46e55c592ec8258f1ca17eb6540f7-image.png">
  Edit Brand Kit
</Image>

> 📘 **Brand Kit Precedence**
>
> When generating or editing images or content, the selected Brand Kit always takes precedence over text prompts. If a prompt conflicts with the Brand Kit’s settings (for example, color codes, borders, or tone), AI prioritizes the Brand Kit.
>
> For example, if your Brand Kit specifies a red border and the prompt requests a blue one, the generated image uses red, maintaining your brand consistency.

# Best Practices for Defining Brand Kit Guidelines

The Instructions field in your Brand Kit defines how the AI should represent your brand, both in tone and visual style. By setting clear guidelines, you help ensure that every AI-generated message or image reflects your brand’s voice, values, and visual identity.

These instructions directly influence how the AI interprets phrasing, tone, and design choices across all generated content.

> 📘 Note
>
> Both Content Guidelines and Image Guidelines instruction fields have a maximum limit of 500 characters.

Following these best practices when defining your Brand Kit guidelines:

* Always use the active voice, for example, “Get started with rewards” instead of “Rewards can be earned.”
* Choose simple, approachable adjectives such as “affordable,” “smart,” “simple”; avoid superlatives such as “best” or “#1.”
* Avoid gender, racial, or culturally biased language.
* Use action-oriented phrasing such as “discover,” “explore,” or “save.”
* Maintain consistent punctuation and capitalization. Use Title Case for headlines and sentence case for subtext.
* Ensure text is localization-friendly, and avoid region-specific slang or idioms.
* For image prompts, describe the layout and mood accurately. For example, “Bright, inviting layout with product focus.”
* For content prompts, specify intent clearly. For example, “promote trust,” “encourage engagement,” “drive conversion”, and so on.

## Sample Instructions

These are example instruction sets you (or customers) can pre-fill in the Instructions field under *Content Guidelines* and *Image Guidelines* in the Brand Kit. They tell the AI how to represent the brand’s style and tone.

| Industry                         | Content Guidelines                                                                                                                                                                     | Image Guidelines                                                                                                                                                           |
| -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Consumer / Retail**            | “Use an active, conversational tone. Highlight benefits and promotions in clear, positive language. Avoid jargon or overpromising. Keep copy short and easy to scan.”                  | “Use bright, engaging visuals with product focus. Maintain natural lighting and clean composition. Avoid excessive text or dark filters.”                                  |
| **Financial Services / Banking** | “Maintain a professional, confident tone. Use factual, non-exaggerated statements. Avoid words like ‘guaranteed’ or ‘risk-free.’ Ensure all claims comply with regulatory guidelines.” | “Use trustworthy, calm visuals — clean design, corporate colors, and professional imagery. Avoid any visuals that may misrepresent returns, outcomes, or endorsements.”    |
| **Healthcare / Pharma**          | “Write in an empathetic, factual tone. Avoid making clinical claims or outcome promises. Ensure all messaging aligns with approved regulatory language.”                               | “Use clean, minimal visuals that focus on care and trust. Avoid imagery suggesting medical results or diagnoses. Prefer healthcare professionals and real people imagery.” |
| **Technology / SaaS / B2B**      | “Maintain a clear, formal tone. Use precise, informative statements highlighting value and reliability. Avoid hyperbolic or casual expressions.”                                       | “Use minimal, professional visuals with abstract or product-based graphics. Keep color palette brand-aligned and consistent. Avoid unlicensed or stock-heavy visuals.”     |
| **Food & Beverage**              | “Use appetizing, sensory language while keeping tone friendly and inviting. Avoid unrealistic or exaggerated claims like ‘best ever.’”                                                 | “Use warm, natural lighting and authentic food photography. Keep focus on product quality and freshness. Avoid overly edited or artificial looks.”                         |
| **Gaming / Entertainment**       | “Use an energetic, motivational tone. Highlight rewards or events with excitement, but avoid misleading outcome statements.”                                                           | “Use vibrant, high-contrast visuals with bold elements. Maintain consistent color palettes and avoid off-brand effects.”                                                   |

# FAQs

### Can I edit or clone a Brand Kit later?

Yes. You can edit all fields or clone a kit to create a new variant with similar settings.

### How many Brand Kits can I create?

You can create up to **10 Brand Kits** per account.

### Can I assign a Brand Kit to multiple teams?

Yes. You can assign it to a single team or make it Global, so all teams can use it. Teams feature is in Private Beta. For more information, refer to Teams.

### Can I edit Brand Kits later?

Yes. All fields, including name, team, and brand assets, are editable during Edit Mode.

### What happens if I lock a Brand Kit?

Locked kits ensure all AI-generated visuals and content follow brand rules. Users cannot override these settings in campaign flows.

### What happens if I try to create something outside the Brand Kit settings?

If a Brand Kit is active, the AI automatically enforces its rules to maintain consistency. If your prompt or request conflicts with Brand Kit specifications (such as using a different color, font, or tone), the AI will prioritize the Brand Kit settings and adjust the output accordingly.
