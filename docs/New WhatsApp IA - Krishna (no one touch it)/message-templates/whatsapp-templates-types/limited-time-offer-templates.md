---
title: Limited-Time Offer Templates
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
Limited-time Offer templates are designed for time-sensitive promotions to create a sense of urgency. These templates are ideal for flash sales, special discounts, or any offers that require immediate attention and action from your customers. 

> 📘 Availability
> 
> These Templates are only available with Marketing Category Templates.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/cd2ade8-LTO_sample.png",
        "",
        "Limited Time Offer Message Components"
      ],
      "align": "center",
      "sizing": "50% ",
      "border": true,
      "caption": "Limited-Time Offer Message Components"
    }
  ]
}
[/block]


LTO templates include the following components:

- **Header**: Optional with support only for text, image, video, document, and location.
- **Limited-Time Offer**: Optional with sub-components:
  - Offer Title: Offer detailed text with a character limit of 16 characters.
  - Offer Expiration Timer: Optional field displaying offer expiration details.
- **Body**: Mandatory with support for up to 600 characters in text format.
- **Buttons**: These are optional and can support up to 10 characters. Button types include Copy code, Visit Website CTA, Call phone CTA, and Quick reply.
- **Limited-Time Offer Templates:** Limited-Time Offer Templates are designed for time-sensitive promotions. They include headers, limited-time offer components, body, and buttons.

> 🚧 Support for Limited-Time Offer (LTO) Templates in Utility Category
> 
> Limited-Time Offer (LTO) Templates are not supported in the _Utility_ category by WhatsApp. Be aware of this restriction when planning your campaigns. You can explore other categories for optimal template utilization.

### Use Cases

The following are some of the use cases that can be addressed with Limited Time Offer templates:

- **Flash Sales or Exclusive Discounts**

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5932e3b-B1g1.png",
        null,
        "Flash Sale"
      ],
      "align": "center",
      "sizing": "45% ",
      "border": true,
      "caption": "Flash Sale"
    }
  ]
}
[/block]


To create a Limited-Time Offer template in CleverTap, follow these steps:

1. From the dashboard, navigate to _Account > Settings > Engage > Channels > WhatsApp_.

2. Choose the _Provider Type_  as **WhatsApp Direct** for CleverTap BSP or **WhatsApp Connect** for external BSPs.

   [block:image]{"images":[{"image":["https://files.readme.io/ebaed56-image.png",null,"Select WhatsApp Provider"],"align":"center","border":true,"caption":"Select WhatsApp Provider"}]}[/block]

3. Select the WABA account or provider to add templates.

   [block:image]{"images":[{"image":["https://files.readme.io/c423fd6-image.png","image.png",1894],"align":"center","border":true,"caption":"Select WABA account"}]}[/block]

4. Select the _Templates_ tab and click **+Template**.

   [block:image]{"images":[{"image":["https://files.readme.io/fb10d89-temp.png",null,"Create a Template"],"align":"center","border":true,"caption":"Create a Template"}]}[/block]

5. Select the _Limited Time Offer_ template. **_Limited Time Offer_ templates are only available with Marketing category. **

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4fe4736-LTO.png",
        "",
        "Limited Time Offer"
      ],
      "align": "center",
      "border": true,
      "caption": "Limited Time Offer"
    }
  ]
}
[/block]


6. Enter the _Template Name_ and configure headers and body as follows:

- For header: Select image or video.
- For body text formatting:
  - **Adding Emojis:** Copy from [here](https://emojipedia.org/most-popular) and paste in the body.
  - **Bold:** Add asterisks (\*) at the beginning and end.
  - **Italic:** Add underscores (\_) at the beginning and end.
  - **Strikethrough:** Add tilde (~) at the beginning and end.
  - **Monospace: **Add three consecutive backticks (\`\`\`) at the beginning and end.
- If required, add the buttons and fill in the required information.
  - **Copy Code buttons:** You can include only 1 copy code button. When tapped, the code is copied to the customer's clipboard.
  - **Visit Website CTA buttons:**  You can add up to 2 buttons, giving customers three choices:
    - **Static CTA buttons:** Use static URLs for redirection.
    - **Dynamic CTA Buttons:** Brands must provide the URL prefix (URL domain), and the URL suffix can be personalized for each user. For example: <https://www.clevertap.com/{{1}}>.
    - **CleverTap Click tracking CTA buttons:** Brands can leverage CleverTap click tracking functionality to monitor details of the user who clicked the URL. The entire URL can be personalized for each user during campaign creation.
- **Quick Reply buttons:** Add up to 5 quick reply buttons. Brands commonly use these buttons to enable users to swiftly respond to WhatsApp messages without typing.
- **Marketing Opt-out button:** You can add 1 marketing opt-out button. This button sends an unsubscription keyword in quick reply format, making it easy for end-users to opt out. Brands need to handle these unsubscription flows properly to ensure end-users get opted out when they tap on this button

7. Configure the Limited-Time Offer (LTO) component according to your specific requirements. The LTO component includes two essential components:

- **Offer Title:** Utilize this section to create a captivating heading for your promotional offer. 
- **Offer Expiry Timer:** This field is optional. If selected, the template will display the time remaining for the offer's expiration, dynamically updating to reflect the time left for the offer to conclude.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f3c7941-image.png",
        null,
        "Select Offer Expiration Timer"
      ],
      "align": "center",
      "border": true,
      "caption": "Select Offer Expiration Timer"
    }
  ]
}
[/block]


8. Click **Save Template** to save the message template.