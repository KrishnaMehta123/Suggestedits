---
title: Gmail Promotional Annotations
excerpt: Put the most valuable parts of email right at people's fingertips.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
# Overview
[Gmail Promotional Annotations](https://developers.google.com/gmail/promotab/) enables you to highlight your email on the Gmail Promotions tab. Your email can include additional information such as promotion codes, a featured image, and deal expiration dates. This information is visible to your email subscribers before opening the email. It is an excellent way to excite your users to open your message by setting it apart from other emails in the user's inbox. CleverTap provides you with a no-code way to annotate your email messages. 
[block:callout]
{
  "type": "info",
  "title": "Beta Release",
  "body": "This feature is available in public beta and will be rolled out for all organizations over the next few weeks.\n\nThis feature is only available in the new CleverTap campaigns UI. Please raise a support ticket from the* need help* section in the CleverTap dashboard to move to the new UI."
}
[/block]

[block:callout]
{
  "type": "info",
  "body": "The Gmail app for Android & iOS supports highlighting emails with promotional annotations. Google will extend this capability to Gmail for desktop soon.",
  "title": "Supported Inboxes"
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/21c3ec7-promo_email_teaser_1440_1.png",
        "promo_email_teaser_1440 (1).png",
        990,
        309,
        "#ecebe7"
      ]
    }
  ]
}
[/block]

# Annotate Emails 
Follow the steps to annotate emails in an email campaign:
1. [Create an email campaign](https://docs.clevertap.com/docs/create-message-email). 
2. [Define the message content](https://docs.clevertap.com/docs/create-message-email#define-the-message-content) from the Email Editor. 
3. Click **Sender details**. 
4. To annotate your email, click **Highlight with Gmail promotional annotations **. The following options display:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0467468-Annotations_with_explanations.png",
        "Annotations_with_explanations.png",
        1136,
        562,
        "#f6f6f5"
      ],
      "border": true
    }
  ]
}
[/block]
5. Add the required information. 

[block:parameters]
{
  "data": {
    "h-0": "Element",
    "h-1": "Description",
    "h-2": "Best Practices",
    "0-0": "Sender name for inbox",
    "0-1": "Add your business name.",
    "1-0": "Subject line for inbox",
    "1-1": "Add a unique and relevant subject line for the inbox. We recommend a 44 character limit for optimal rendering.",
    "2-0": "Add company logo",
    "2-1": "Upload an image or add a URL. Check that the URL is https (not http).",
    "3-0": "Add card image",
    "3-1": "Add an image to display on the email frame.",
    "4-0": "Offer title",
    "4-1": "Highlight any offerings such as *20% off* or *Free Shipping*. We recommend a 20 character limit for optimal rendering.",
    "5-0": "Promo code",
    "5-1": "Add the promo code. We recommend a 20 character limit for optimal rendering.",
    "6-0": "Offer period",
    "6-1": "Select the offer date range.",
    "3-2": "  *  Visual Appeal: Avoid only text. Create a visual promotion by adding product or lifestyle images.\n  *  Image Cropping: Images are center-cropped automatically. Images are recommended to be 538 x 138 pixels in size and have a 3.9 aspect ratio. GIF and WEBP images are not supported.\n  *  Don't repeat images. Create unique and engaging promotions by using different images. Your users may consider your email messages as repetitive or duplicate if you reuse the same image. ",
    "1-2": "Add a unique subject line for the inbox to avoid duplicate text between the subject, deal badge, and discount code. This alternative subject will only be displayed if the discount code or sale badges are also displayed. For example, if the original subject was *20% Off Sale Ends Today* and the offer badge is *20% Off*, add a subject line that says **Sale Ends Today** to avoid duplication.",
    "2-2": "Be sure to use an https (not http) URL. This logo selection only shows in the email preview.",
    "4-2": "*Avoid using more than four words or full sentences in this space, as it competes with your subject line. When your email text space is full, the offer title truncates (for example, \"...\").\n\n * Don’t repurpose. Use promotional offerings to ensure clarity and simplicity. Don't utilize  for other actions like *Open now*.\n\n * Don’t use run-on sentences. Avoid saying things such as *25% off unless you’ve already purchased from us in which case other ...* Long sentences are truncated.",
    "6-2": "Using this feature allows an email to be previewed twice at the top in a bundle:\n* once when it is first sent.\n* again within 3 days of the offer expiry.\n\nWhen personalizing *Offer period*, specify the time and timezone. For example, *2018-12-30T23:59:59-0700*.",
    "5-2": "Only use a discount code if you have it featured in the email. Don't repurpose this space, because it always says *Code* before the text.",
    "0-2": "Add your *Business Name* or *From Name* for the Campaign."
  },
  "cols": 3,
  "rows": 7
}
[/block]
6. Click **Preview & Test** to preview the annotated email message.


# Test Annotation

Create a unique Gmail testing account ending with promotabtesting@gmail.com for your team. For example, *mycompany.promotabtesting@gmail.com*. This unique account will have a more aggressive email ranking and bundling to make testing easier and faster.

# Troubleshooting

Before troubleshooting a problem, check your account-level settings in your Gmail app. Check that you've enabled the following settings to test the latest experiences in the Gmail promotions tab. These are the default settings: 
  * Images: Always show.
  * Conversation view: On.
  * Enable Bundling of Top Email: On.

The following sections discuss common issues encountered when attempting to test:

### Not seeing email bundles at all.
  *  Check that the device has the latest version of the Gmail app. Refresh email by pulling down on the screen within the promotions tab.
  * Try restarting your device.
  * If the issue is still not resolved, try viewing the bundle on another device. For example, a tablet may have a different Gmail version and show the bundle differently.

[block:callout]
{
  "type": "info",
  "body": "There is a chance your email could be in a holdback group. If none of the measures worked, create a new account ending with *promotabtesting@gmail.com*. For example, create *mycompanypromotabtesting@gmail.com* and use that new account for testing.",
  "title": "Email is held up"
}
[/block]

### Email does not show up on the Promotions tab.
Use the following measures:
* Check if the marketing email was sent from the usual subdomain. Sending from less recognized subdomains can confuse the Gmail tab classifier and prevent an email from being placed on the Promotions tab.
* Check that your account has no email filters that send email to the primary tab because annotations are only visible on the Promotions tab.
* Send from different sender subdomains to ensure email ends up on the correct tab. Refer to  [Bulk Senders Guidelines](https://support.google.com/mail/answer/81126) for more detail about the Gmail classifier.
* If you are using a *promotabtesting@gmail.com* account, the first email does not appear on the Promotions tab. Drag the email onto the Promotions tab, and send an email from the same sender address, with a different subject line, to the testing account.

### Cannot see your brand's annotated email in a bundle.
  * Check if the email is on the Gmail Promotions tab.
  * Annotated emails are currently not available for Gmail for Business accounts. Ensure that you are testing on your personal Gmail address.
  * Check that the email was not opened or sent on a previous day.
  * An email does not populate in a bundle on another device after it is viewed on one device. You must send a new test email to preview.
  * Create multiple testing accounts if you want to visualize on multiple devices. One of your team members might open the email, thus making it unavailable in the bundle for the rest of the team. 
  * Check that the annotation is not past the expiration date. 
  * Check that you are using the latest version of the Gmail app. Try viewing on another device. For example, a tablet may have a different version of the Gmail app and show email differently. 
  * Refresh the Gmail app by pulling down the Gmail Promotions tab screen.
  * Check that you are not using sensitive categories in the Gmail Promotions tab. For example, adult content or debt collection.

### Single image preview display is not visible when the annotation includes the image.
  * Refresh the Gmail app by pulling down the Gmail Promotions tab screen.
  * If your image is considered a sensitive topic, the image may not be shown in the Gmail Promotions tab (for example, adult content or debt collection).
  * Gmail may decide not to render the image for your device. It is not guaranteed for the *Single image* to display for every email.

### The email bundle is visible on one device but not another.
  * Check that you are viewing from the same email account.
  * If email is opened on one device first, it may change the ranking of the bundle on another device.