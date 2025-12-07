---
title: Gmail Promotional Annotations (EM-2151)
excerpt: >-
  Understand how to put the most valuable parts of email right at people's
  fingertips.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

[Gmail Promotional Annotations](https://developers.google.com/gmail/promotab/) enables you to highlight your email on the Gmail Promotions tab. Your email can include additional information, such as promotion codes, a featured image, and deal expiration dates. This information is visible to your email subscribers before opening the email. It is an excellent way to excite your users to open your message by setting it apart from other emails in the user's inbox. CleverTap provides you with a no-code way to annotate your email messages. 

> 📘 Feature Deprecation
> 
> Google has deprecated the current single image preview annotations.

# Annotate Emails with Deal Annotation

With Deal Annotation, the deals and offers stand out prominently in the Gmail inbox, capturing the attention of your audience and increasing the likelihood of conversions.

> 📘 Public Beta
> 
> This feature is released in Public Beta and is available in the **new CleverTap campaigns UI**.

Follow the steps listed below to annotate emails in an email campaign:

1. [Create an email campaign](https://docs.clevertap.com/docs/create-message-email). 
2. [Define the message content](https://docs.clevertap.com/docs/create-message-email#define-the-message-content) from the Email Editor. 
3. Click **Sender details**. 
4. To annotate your email, select **Highlight with Gmail promotional annotations **. The following options display:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b9ccbce-Gmail_Promotional_Annotation_.png",
        "Highlight the Gmail Promotional Annotations",
        1136
      ],
      "align": "center",
      "border": true,
      "caption": "Annotate Emails with Deal Annotation"
    }
  ]
}
[/block]


Add the required information. 

| Element        | Description                                                                                                            | Best Practices                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| :------------- | :--------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Sender name    | Add your business name.                                                                                                | This field is populated automatically using the _From_ part of the _Sender Details_.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Subject line   | Add a unique and relevant subject line for the inbox. We recommend a 44-character limit for optimal rendering.         | This field is populated automatically using the _Subject_ part of the _Sender Details_.                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Company logo   | Upload an image or add a URL. Check that the URL is https (not http).                                                  | Ensure that you use an https (not http) URL. This logo selection only shows in the email preview. You must implement [Brand Indicators for Message Identification (BIMI)](https://support.google.com/a/answer/10911320?hl=en) standards to render the logo.                                                                                                                                                                                                                                                                                                    |
| Discount offer | Highlight any offerings such as _20% off_ or _Free Shipping_. We recommend a 20-character limit for optimal rendering. | \*Avoid using more than four words or full sentences in this space, as it competes with your subject line. When your email text space is full, the offer title truncates (for example, "...").<ul> <li> <p>Do not repurpose. Use promotional offerings to ensure clarity and simplicity. Do not utilize it for other actions like <em>Open now</em>.</p> </li> <li> <p>Do not use run-on sentences. Avoid saying things such as <em>25% off unless you’ve already purchased from us in which case other ...</em> Long sentences are truncated.</p> </li> </ul> |
| Offer code     | Add the promo code. We recommend a 20-character limit for optimal rendering.                                           | Only use a discount code if you have it featured in the email. Do not repurpose this space because it always says _Code_ before the text.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Offer period   | Select the offer date range.                                                                                           | Using this feature allows an email to be previewed twice at the top in a bundle:<ul> <li>once when it is first sent.</li> <li>again within 3 days of the offer expiry.</li> </ul>When personalizing _Offer period_, specify the time and timezone. For example, _2018-12-30T23:59:59-0700_.                                                                                                                                                                                                                                                                    |

5. Click **Preview & Test** to preview the annotated email message.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6fd6c27-Annotated_Email.png",
        "Annotated Email Promotion",
        990
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Annotated Email"
    }
  ]
}
[/block]


# Annotate with Product Carousel

The Product Carousel Annotation enhances the impact of email marketing campaigns, introducing a promotional carousel within Gmail to amplify engagement and drive higher conversion rates. This feature enables users to upload a series of Promotional Cards, each tailored with specific attributes. 

> 📘 Private Beta
> 
> This feature is released in Private Beta and is available in the **new CleverTap campaigns UI**.

### Prerequisites

- Add the designated domains to the Google Allowlist by reaching out to [p-gmail-outreach@google.com](mailto:p-gmail-outreach@google.com).
- Register the domain with [DMARC](https://support.google.com/a/answer/2466563?hl=en). 

> 📘 Note
> 
> You can upload a minimum of 2 and a maximum of 10 cards in the carousel, each featuring customizable properties.

### Annotate Email

Follow the steps listed below to annotate emails in an email campaign:

1. [Create an email campaign](https://docs.clevertap.com/docs/create-message-email). 
2. [Define the message content](https://docs.clevertap.com/docs/create-message-email#define-the-message-content) from the Email Editor. 
3. Click **Sender details**. 
4. To annotate your email, select **Highlight with Gmail promotional annotations ** and select **Product Carousel**. The following options display for each promotional card:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/78c56f1-image.png",
        null,
        "Annotate Email with Product Carousel Annotation"
      ],
      "align": "center",
      "border": true,
      "caption": "Annotate Email with Product Carousel Annotation"
    }
  ]
}
[/block]


Add the required information.

[block:parameters]
{
  "data": {
    "h-0": "Element",
    "h-1": "Description",
    "0-0": "_Upload Image_",
    "0-1": "You can upload images in PNG or JPEG format and ensure compatibility with aspect ratios such as 4:5, 1:1, or 1.91:1. Each image within the carousel must use the same aspect ratio.",
    "1-0": "\\* _Image URL_",
    "1-1": "Provide the URL to your image in PNG or JPEG format, ensuring compatibility with aspect ratios such as 4:5, 1:1, and 1.91:1.  \nExample: <https://www.example.com/image.png>  \nEach image within the carousel must have a unique URL and use the specified aspect ratio standards.  For more information, refer to the [Google Documentation](https://developers.google.com/gmail/promotab/overview#microdata_1).  \n  \n**NOTE**: Google recommends not using personalized elements or user-specific UTM parameters in carousel image URLs. Only static images must be used across all users in the campaign for annotations to render in the email.",
    "2-0": "\\* _Target Image URL_",
    "2-1": "Provide the specific URL that opens when the user clicks on the promotional image.",
    "3-0": "_Headline_",
    "3-1": "Provide a concise 1 to 2-line description accompanying the promotional image. ",
    "4-0": "_Price_",
    "4-1": "Provide the price of the featured promotion. ",
    "5-0": "_Price Currency_",
    "5-1": "Select the currency of the displayed price from the drop-down list. The currency format is displayed in a 3-letter ISO 4217 format, such as USD. This field appears when you select the _Price Tag_ checkbox.",
    "6-0": "_Price_",
    "6-1": "Provide the numerical value representing the original price for the promotional product. This field appears when you select the _Price_ checkbox.",
    "7-0": "_Discount Value_",
    "7-1": "Provide the discount value, which represents the amount deducted from the original price. This field appears when you select the _Price_ checkbox.  \nExample: If the discount value is 25 and the original price is 100, the final price displayed is $75."
  },
  "cols": 2,
  "rows": 8,
  "align": [
    "left",
    "left"
  ]
}
[/block]


\*The fields marked with asterisk signs are mandatory fields.

5. Click **Preview & Test** to preview the annotated email message.

> 📘 Key Points to Consider
> 
> - **Deal Annotation** and **Product Carousel** are currently accessible in the Gmail (Android and iOS) applications for users outside the EU region.
> - The Gmail app for Android and iOS supports highlighting emails with promotional annotations. Google plans to extend this capability to Gmail for desktop soon.

# Test Annotation

Create a unique Gmail testing account ending with [promotabtesting@gmail.com](mailto:promotabtesting@gmail.com) for your team. For example, _[mycompany.promotabtesting@gmail.com](mailto:mycompanypromotabtesting@gmail.com)_. This unique account will have a more aggressive email ranking and bundling to make testing easier and faster. 

> 📘 Testing Product Carousel
> 
> For Product Carousels to render, Google recommends a campaign with atleast 100 users.

# Troubleshooting

Before troubleshooting a problem, check your account-level settings in your Gmail app. Check that you have enabled the following settings to test the latest experiences in the _Gmail promotions_ tab. The following are the default settings: 

- Images: Always show.
- Conversation view: On.
- Enable Bundling of Top Email: On.

The following sections include information about common issues encountered when attempting to test:

### Not seeing email bundles at all

To resolve this issue:

- Check that the device has the latest version of the Gmail app. Refresh your email by pulling down on the screen within the promotions tab.
- Try restarting your device.
- If the issue is still not resolved, try viewing the bundle on another device. For example, a tablet may have a different Gmail version and show the bundle differently.

> 📘 Email Held Up
> 
> There is a chance your email could be in a holdback group. If none of the measures work, create a new account ending with _[promotabtesting@gmail.com](mailto:promotabtesting@gmail.com)_. For example, create _[mycompanypromotabtesting@gmail.com](mailto:mycompanypromotabtesting@gmail.com)_ and use that new account for testing.

### Email does not show up on the Promotions tab

To resolve this issue:

- Check if the marketing email was sent from the usual subdomain. Sending from less recognized subdomains can confuse the Gmail tab classifier and prevent an email from being placed on the Promotions tab.
- Check that your account has no email filters that send email to the primary tab because annotations are only visible on the Promotions tab.
- Send from different sender subdomains to ensure the email ends up on the correct tab. For more details about the Gmail classifier, refer to [Bulk Senders Guidelines](https://support.google.com/mail/answer/81126).
- If you are using a _[promotabtesting@gmail.com](mailto:promotabtesting@gmail.com)_ account, the first email does not appear on the Promotions tab. Drag the email onto the Promotions tab, and send an email from the same sender address, with a different subject line, to the testing account.

### Cannot see your brand's annotated email in a bundle

To resolve this issue:

- Check if the email is on the Gmail Promotions tab.
- Annotated emails are currently not available for Gmail for Business accounts. Ensure that you are testing on your personal Gmail address.
- Check that the email was not opened or sent on the previous day.
- An email does not populate in a bundle on another device after it is viewed on one device. You must send a new test email to preview.
- Create multiple testing accounts if you want to visualize on multiple devices. One of your team members might open the email, thus making it unavailable in the bundle for the rest of the team. 
- Check that the annotation is not past the expiration date. 
- Check that you are using the latest version of the Gmail app. Try viewing on another device. For example, a tablet may have a different version of the Gmail app and show email differently. 
- Refresh the Gmail app by pulling down the Gmail Promotions tab screen.
- Check that you are not using sensitive categories in the Gmail Promotions tab. For example, adult content or debt collection.

### The email bundle is visible on one device but not on another

To resolve this issue:

- Check that you are viewing from the same email account.
- If the email is opened on one device first, the ranking of the bundle may change on another device.

# Best Practices

Gmail recommends the following [best practices](https://developers.google.com/gmail/promotab/best-practices) to optimize your email annotations:

### Leverage the Power of Visuals

Gmail has observed improved results when emails feature captivating images that complement the message. Instead of text-only designs, focus on incorporating visually appealing elements. Avoid using images with text that gets cut off or reusing the same visuals across multiple campaigns.

### Concise Offer Descriptions

Gmail recommends concise and compelling offer descriptions. Avoid lengthy sentences or phrases, such as "Limited Time Offer: 50% Off All Accessories" or "Exclusive Deals on Summer Collection," as they might get clipped and compete with the subject line. Opt for clear, engaging language that encourages recipient engagement without repeating the subject line verbatim.

# FAQs

### Q. Can I see how many users received a product carousel?

Ans. Gmail decides when to show the product carousel, so not every person who gets the email will see it. Therefore, there's no definite way to know how many people received the product carousel.

### Q. Why is my promotional message not displaying the product carousel in the user's inbox?

Ans. There are a few reasons why the product carousel might not appear in the Gmail Promotion Tab. Firstly, all the images in the promotion need to be of good quality and the right size. They should mostly be pictures of the product itself, without too much text or anything inappropriate.

Moreover, Gmail limits the number of product carousels it shows in the Promotion tab. So, if a user receives a lot of emails with product carousels, Gmail might not show all of them.