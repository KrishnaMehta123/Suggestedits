---
title: OOTB Templates
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
# Customization Matrix for Email Templates (Approach 1)

This table outlines all common and secondary customizations available in CleverTap's Out-of-the-Box (OOTB) email templates, along with implementation steps and their availability.

[block:parameters]
{
  "data": {
    "h-0": "Customization",
    "h-1": "Steps & Code",
    "h-2": "Template Availability",
    "0-0": "**Replace the Logo**",
    "0-1": "- Locate the `<img>` tag used for the logo. <br> - Replace the `src` attribute with your brand's logo URL. <br> - _UI Option:_ Use the platform editor to upload a new logo or select from the image library. <br><br>**Example:**<br>`html<br><img src=\"https://yourdomain.com/logo.png\" alt=\"Company Logo\" /><br>`",
    "0-2": "Available in all templates",
    "1-0": "**Update Banner/Product Images**",
    "1-1": "- Identify `<img>` tags for banners or product visuals. <br> - Replace the `src` value with your desired image URL. <br> - Maintain aspect ratio. <br> - Use `.jpg`, `.png`, or `.gif`. <br><br>**Example:**<br>`html<br><img src=\"https://yourdomain.com/banner.jpg\" alt=\"Banner Image\" /><br>`",
    "1-2": "Available in all templates",
    "2-0": "**Update Call-To-Actions (CTAs)**",
    "2-1": "- Locate CTA `<a>` tags. <br> - Update button text, URL, and styles. <br><br>**Example:**<br>`html<br><a href=\"https://your-link.com\" style=\"background:#ff5733; color:#fff; padding:10px 20px; text-decoration:none;\">Shop Now</a><br>`",
    "2-2": "Available in all templates",
    "3-0": "**Update Header/Footer Links**",
    "3-1": "- Locate anchor tags in the header/footer. <br> - Update link text and `href` value. <br><br>**Example:**<br>`html<br><a href=\"https://yourdomain.com/privacy\" class=\"f-nav-link\">Privacy Policy</a><br>`",
    "3-2": "Available in all templates",
    "4-0": "**Change Theme or Background Color**",
    "4-1": "- Find the outer `<table>` wrapper. <br> - Update `background` or `bgcolor`. <br><br>**Example:**<br>`html<br><table style=\"background: #FFFFFF; width: 100%;\"> ... </table><br>`",
    "4-2": "Available in all templates",
    "5-0": "**Update the Privacy Policy**",
    "5-1": "- Edit the footer link text and URL. <br><br>**Example:**<br>`html<br><a href=\"https://yourdomain.com/privacy\" class=\"f-nav-link\" style=\"color:#939393; text-decoration:none;\">Privacy Policy</a><br>`",
    "5-2": "All except _Cart Abandonment_",
    "6-0": "**Update Social Media & Download Links**",
    "6-1": "- Replace `href` values and images for icons or store buttons. <br><br>**Example:**<br>`html<br><a href=\"https://facebook.com\"><img src=\"facebook-icon.png\" alt=\"Facebook\"></a><br><a href=\"https://play.google.com/store/apps/details?id=yourapp\"><img src=\"google-play.png\" alt=\"Google Play\"></a><br>`",
    "6-2": "All except _Cart Abandonment_, _Access to Early Sales_",
    "7-0": "**Update Typography / Font-face**",
    "7-1": "- Use `@font-face` in `<style>`. <br> - Apply using `font-family`. <br><br>**Example:**<br>`css<br>@font-face { font-family: 'Poppins'; src: url('https://yourcdn.com/Poppins-Regular.woff') format('woff'); }<br>body { font-family: 'Poppins', Arial, sans-serif; }<br>`",
    "7-2": "All except _Cart Abandonment_, _Access to Early Sales_, _Anniversary_, _Account Verification_",
    "8-0": "**Add Mobile Responsiveness**",
    "8-1": "- Use CSS media queries for responsiveness. <br><br>**Example:**<br>`css<br>@media screen and (max-width: 480px) { .container { max-width: 100% !important; padding: 10px; } .logo { width: 120px; } }<br>`",
    "8-2": "All except _Cart Abandonment_, _Access to Early Sales_, _Anniversary_, _Account Verification_, _Newsletter_, _Loyalty Points_",
    "9-0": "**Image Upload Specifications**",
    "9-1": "- Maintain original dimensions (e.g., `383x247px`). <br> - Use `.jpg`, `.png`, `.gif`. <br> - Optimize size and resolution.",
    "9-2": "All except _Cart Abandonment_, _Access to Early Sales_, _Anniversary_, _Account Verification_, _Referral_",
    "10-0": "**Add/Modify Unsubscribe Links**",
    "10-1": "- Insert `{{UnsubscribeURL}}` in the footer. <br><br>**Example:**<br>`html<br><p style=\"font-size: 12px; color: #999999;\">To stop receiving emails, <a href=\"{{UnsubscribeURL}}\" style=\"color: #FF0000; text-decoration: underline;\">unsubscribe here</a>.</p><br>`",
    "10-2": "Available in 17 templates: _Welcome Mailer - 1_, _Welcome Mailer - 2_, _WinBack_, _What's in the Store_, _Subscription Template_, _Show Recommendation (White)_, _Show Recommendation (Black)_, _Scratch Card_, _Referral_, _Promotional Template_, _Password Reset_, _Order Shipped_, _Order Placed_, _Order Delivered_, _Newsletter_, _Loyalty Points_, _Feedback Request_"
  },
  "cols": 3,
  "rows": 11,
  "align": [
    null,
    null,
    null
  ]
}
[/block]


<br />

# Template Editing Capabilities (Approach 2)

## Common Customizations (Available in All 26 Templates)

### Replace the Logo

- Update the logo using the `src` attribute of an `<img>` tag:
  ```html
  <img src="https://yourdomain.com/logo.png" alt="Company Logo" />
  ```
- _UI Option:_ Use the platform editor to upload a new logo or select from the image library.

### Update Banner/Product Images

- Modify the `src` value of banner or product images:
  ```html
  <img src="https://yourdomain.com/banner.jpg" alt="Banner Image" />
  ```
- Maintain correct aspect ratio and use `.jpg`, `.png`, or `.gif` formats.

### Update Call-To-Actions (CTAs)

- Change CTA text, destination URLs, and styling in anchor tags:
  ```html
  <a href="https://your-link.com" style="background:#ff5733; color:#fff; padding:10px 20px; text-decoration:none;">Shop Now</a>
  ```

### Update Header/Footer Links

- Modify navigation and legal links in the header or footer:
  ```html
  <a href="https://yourdomain.com/privacy" class="f-nav-link">Privacy Policy</a>
  ```

### Change Theme or Background Color

- Update the background styling in outer container elements:
  ```html
  <table style="background: #FFFFFF; width: 100%;"> ... </table>
  ```

***

## Secondary Customizations (Not in All Templates)

These customizations are available in most, but not all templates.

### Update the Privacy Policy (25/26 Templates)

- Typically found in the footer:
  ```html
  <a href="https://yourdomain.com/privacy" class="f-nav-link" style="color:#939393; text-decoration:none;">Privacy Policy</a>
  ```

### Update Social Media Links and Download Links (24/26 Templates)

- Replace the social icons and app store links as needed:
  ```html
  <a href="https://facebook.com"><img src="facebook-icon.png" alt="Facebook"></a>
  <a href="https://play.google.com/store/apps/details?id=yourapp"><img src="google-play.png" alt="Google Play"></a>
  ```

### Update Typography / Font-face (22/26 Templates)

- Use `@font-face` to declare web fonts in the `<style>` section:
  ```css
  @font-face {
    font-family: 'Poppins';
    src: url('https://yourcdn.com/fonts/Poppins-Regular.woff') format('woff');
    font-style: normal;
    font-weight: 400;
  }
  ```
  ```css
  body {
    font-family: 'Poppins', Arial, sans-serif;
  }
  ```

### Add Mobile Responsiveness / Media Queries (20/26 Templates)

- Media queries ensure emails adapt to smaller screens:
  ```css
  @media screen and (max-width: 480px) {
    .container { max-width: 100% !important; padding: 10px !important; }
    .logo { width: 120px !important; }
  }
  ```

### Image Upload Specifications (21/26 Templates)

- Follow these guidelines for optimal image rendering:
  - Maintain original dimensions (e.g., `383px` height x `247px` width).
  - Use supported formats: `.jpg`, `.png`, `.gif`
  - Optimize for fast loading and clear rendering.

### Add/Modify Unsubscribe Links (17/26 Templates)

- Typically located in the footer:
  ```html
  <p style="font-size: 12px; color: #999999;">To stop receiving emails, <a href="{{UnsubscribeURL}}" style="color: #FF0000; text-decoration: underline;">unsubscribe here</a>.</p>
  ```

***

For implementation details, refer to the source HTML or associated template documentation.

This table outlines available customizations across CleverTap's OOTB email templates, along with steps and examples for each customization.

| Template Name               | Replace the Logo | Update Banner/Product Images | Update CTAs | Update Header/Footer Links | Change Theme/Background | Update Privacy Policy | Update Social & App Links | Update Typography | Mobile Responsive | Image Specs | Unsubscribe Link |
| --------------------------- | ---------------- | ---------------------------- | ----------- | -------------------------- | ----------------------- | --------------------- | ------------------------- | ----------------- | ----------------- | ----------- | ---------------- |
| Welcome Mailer - 1          | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ✔️                | ✔️          | ✔️               |
| Welcome Mailer - 2          | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ✔️                | ✔️          | ✔️               |
| WinBack                     | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ✔️                | ✔️          | ✔️               |
| What's in the Store         | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ✔️                | ✔️          | ✔️               |
| Subscription Template       | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ✔️                | ✔️          | ✔️               |
| Show Recommendation (White) | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ✔️                | ✔️          | ✔️               |
| Show Recommendation (Black) | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ✔️                | ✔️          | ✔️               |
| Scratch Card                | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ✔️                | ✔️          | ✔️               |
| Referral                    | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ✔️                | ❌           | ✔️               |
| Promotional Template        | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ✔️                | ✔️          | ✔️               |
| Password Reset              | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ✔️                | ✔️          | ✔️               |
| Order Shipped               | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ✔️                | ✔️          | ✔️               |
| Order Placed                | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ✔️                | ✔️          | ✔️               |
| Order Delivered             | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ✔️                | ✔️          | ✔️               |
| Newsletter                  | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ❌                 | ✔️          | ✔️               |
| Loyalty Points              | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ❌                 | ✔️          | ✔️               |
| Loyalty Expiry              | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ✔️                | ✔️          | ❌                |
| Informative Mailer          | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ✔️                | ✔️          | ❌                |
| Flash Sale                  | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ❌                 | ✔️          | ❌                |
| First Purchase Incentive    | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ✔️                | ✔️          | ❌                |
| Feedback Request            | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ✔️                | ❌           | ✔️               |
| Birthday                    | ✔️               | ✔️                           | ✔️          | ✔️                         | ✔️                      | ✔️                    | ✔️                        | ✔️                | ❌                 | ❌           | ❌                |
| Anniversary                 |                  |                              |             |                            |                         |                       |                           |                   |                   |             |                  |

# Common Components (Approach 3)

# Overview

CleverTap provides a suite of prebuilt HTML and AMP email templates—referred to as _Out-of-the-Box (OOTB) templates_—designed to empower marketers with versatile and user-friendly solutions for a wide range of communication needs. These templates are fully customizable and support common use cases such as cart abandonment, subscription confirmations, welcome messages, festive promotions, newsletters, and more.

Each template is built with flexibility in mind, allowing teams to tailor designs to match their unique brand guidelines. To ensure ease of use, a comprehensive _README_ section accompanies every template, enabling marketers to confidently customize content without the need for developer assistance.

This guide outlines the core customization options that are consistently available across all templates. Individual template documentation can link to relevant sections in this document to reduce redundancy.

***

## Common Customizations (Available in All 26 Templates)

### Replace the Logo

- Update the logo using the `src` attribute of an `<img>` tag:
  ```html
  <img src="https://yourdomain.com/logo.png" alt="Company Logo" />
  ```
- _UI Option:_ Use the platform editor to upload a new logo or select from the image library.

### Update Banner/Product Images

- Modify the `src` value of banner or product images:
  ```html
  <img src="https://yourdomain.com/banner.jpg" alt="Banner Image" />
  ```
- Maintain correct aspect ratio and use `.jpg`, `.png`, or `.gif` formats.

### Update Call-To-Actions (CTAs)

- Change CTA text, destination URLs, and styling in anchor tags:
  ```html
  <a href="https://your-link.com" style="background:#ff5733; color:#fff; padding:10px 20px; text-decoration:none;">Shop Now</a>
  ```

### Update Header/Footer Links

- Modify navigation and legal links in the header or footer:
  ```html
  <a href="https://yourdomain.com/privacy" class="f-nav-link">Privacy Policy</a>
  ```

### Change Theme or Background Color

- Update the background styling in outer container elements:
  ```html
  <table style="background: #FFFFFF; width: 100%;"> ... </table>
  ```

***

## Secondary Customizations (Not in All Templates)

These customizations are available in most, but not all templates.

### Update the Privacy Policy (25/26 Templates)

- Typically found in the footer:
  ```html
  <a href="https://yourdomain.com/privacy" class="f-nav-link" style="color:#939393; text-decoration:none;">Privacy Policy</a>
  ```

### Update Social Media Links and Download Links (24/26 Templates)

- Replace the social icons and app store links as needed:
  ```html
  <a href="https://facebook.com"><img src="facebook-icon.png" alt="Facebook"></a>
  <a href="https://play.google.com/store/apps/details?id=yourapp"><img src="google-play.png" alt="Google Play"></a>
  ```

### Update Typography / Font-face (22/26 Templates)

- Use `@font-face` to declare web fonts in the `<style>` section:
  ```css
  @font-face {
    font-family: 'Poppins';
    src: url('https://yourcdn.com/fonts/Poppins-Regular.woff') format('woff');
    font-style: normal;
    font-weight: 400;
  }
  ```
  ```css
  body {
    font-family: 'Poppins', Arial, sans-serif;
  }
  ```

### Add Mobile Responsiveness / Media Queries (20/26 Templates)

- Media queries ensure emails adapt to smaller screens:
  ```css
  @media screen and (max-width: 480px) {
    .container { max-width: 100% !important; padding: 10px !important; }
    .logo { width: 120px !important; }
  }
  ```

### Image Upload Specifications (21/26 Templates)

- Follow these guidelines for optimal image rendering:
  - Maintain original dimensions (e.g., `383px` height x `247px` width).
  - Use supported formats: `.jpg`, `.png`, `.gif`
  - Optimize for fast loading and clear rendering.

### Add/Modify Unsubscribe Links (17/26 Templates)

- Typically located in the footer:
  ```html
  <p style="font-size: 12px; color: #999999;">To stop receiving emails, <a href="{{UnsubscribeURL}}" style="color: #FF0000; text-decoration: underline;">unsubscribe here</a>.</p>
  ```

## Template