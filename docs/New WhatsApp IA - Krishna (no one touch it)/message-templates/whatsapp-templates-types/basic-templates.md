---
title: Basic Templates
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
# Basic Templates

Basic Templates are designed for simplicity and quick setup. Use them when sending a single media item, a text body & footer, or a few buttons. These templates are perfect for straightforward messages without complex formatting. They include the following:

- **Header**: Optional with support for text, image, video, document, and locations.
- **Body**: Mandatory with support for up to 1024 characters in text format.
- **Footer**: Optional with support for up to 60 characters.
- **Buttons**: Optional with support for up to 10 buttons, including copy code, visit website CTA, call phone CTA, and quick reply buttons.

### Use Cases

The following are some of the use cases that can be addressed with basic templates:

- **Order Confirmation:**  
  Example Template: "Dear {{1}}, your order {{2}} has been confirmed. Track your package via {{3}}."
- **Service Updates**:  
  Example Template: "Hello {{1}}, we've made improvements to our service. Stay tuned for enhanced experiences."
- **General Announcements:**  
  Example: Template: "Exciting news, {{1}}! Explore our latest offerings and promotions. Don't miss out!."

To create a Basic template in CleverTap, follow these steps:

1. From the dashboard, navigate to _Account > Settings > Engage > Channels > WhatsApp_. 
2. Select the _Provider Type_ as  **WhatsApp Direct** for CleverTap BSP or **WhatsApp Connect** for external BSPs.

   [block:image]{"images":[{"image":["https://files.readme.io/f2f65ee-image.png",null,"Select WhatsApp Provider"],"align":"center","border":true,"caption":"Select WhatsApp Provider"}]}[/block]
3. Select the appropriate WABA account or provider to add templates.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c423fd6-image.png",
        "image.png",
        1894
      ],
      "align": "center",
      "border": true,
      "caption": "Select the WABA account"
    }
  ]
}
[/block]


4. Navigate to the _Templates_ tab and click **+ Template**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c7bb73b-image.png",
        null,
        "Create a Template"
      ],
      "align": "center",
      "border": true,
      "caption": "Create a Template"
    }
  ]
}
[/block]


5. Select the appropriate category & _Basic_ Template

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9f4219d-basic.png",
        "",
        "Basic Template"
      ],
      "align": "center",
      "border": true,
      "caption": "Basic Template"
    }
  ]
}
[/block]


6. Once you select the Template type and Category, you will land on the Template editor. 
7. Enter the _Template Name_, and configure headers and body as follows:

- For header: Select text, image, video, document, or location.
- For body text formatting:
  - **Adding Emojis**: Copy from [here](https://emojipedia.org/most-popular) and paste in the body.
  - **Bold**: Add asterisks (\*) at the beginning and end.
  - **Italic**: Add underscores (\_) at the beginning and end.
  - **Strikethrough**: Add tilde (~) at the beginning and end.
  - **Monospace**: Add three consecutive backticks (\`\`\`) at the beginning and end.
- (Optional) Add footer text.
- Add the buttons and enter the required information:
  - **Copy Code buttons**: You can include only 1 copy code button. When tapped, the code is copied to the customer's clipboard.
  - **Visit Website CTA buttons**:  You can add up to 2 buttons, giving customers three choices:
    - **Static CTA buttons**: Use static URLs for redirection.
    - **Dynamic CTA Buttons**: Brands must provide the URL prefix (URL domain), and the URL suffix can be personalized for each user. For example: <https://www.clevertap.com/{{1}}>.
    - **CleverTap Click tracking CTA buttons**: Brands can leverage CleverTap click tracking functionality to monitor user details who clicked on the URL. They can personalize the URL for each user during campaign creation.
- **Quick Reply buttons**: You can add up to five quick reply buttons. Brands commonly use these buttons to enable users to swiftly respond to WhatsApp messages without typing.
- **Marketing Opt-out button **: You can add 1 marketing opt-out button. This button sends an unsubscription keyword in quick reply format, making it easy for end-users to opt-out. Brands need to handle these unsubscription flows properly to ensure end-users opt out when they tap this button.

8. Click **Save Template** to save the message template.