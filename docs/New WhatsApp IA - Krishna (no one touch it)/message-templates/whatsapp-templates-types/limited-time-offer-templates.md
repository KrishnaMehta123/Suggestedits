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

<Image alt="Limited Time Offer Message Components" align="center" width="50% " border={true} src="https://files.readme.io/cd2ade8-LTO_sample.png">
  Limited-Time Offer Message Components
</Image>

LTO templates include the following components:

* **Header**: Optional with support only for text, image, video, document, and location.
* **Limited-Time Offer**: Optional with sub-components:
  * Offer Title: Offer detailed text with a character limit of 16 characters.
  * Offer Expiration Timer: Optional field displaying offer expiration details.
* **Body**: Mandatory with support for up to 600 characters in text format.
* **Buttons**: These are optional and can support up to 10 characters. Button types include Copy code, Visit Website CTA, Call phone CTA, and Quick reply.
* **Limited-Time Offer Templates:** Limited-Time Offer Templates are designed for time-sensitive promotions. They include headers, limited-time offer components, body, and buttons.

> 🚧 Support for Limited-Time Offer (LTO) Templates in Utility Category
>
> Limited-Time Offer (LTO) Templates are not supported in the *Utility* category by WhatsApp. Be aware of this restriction when planning your campaigns. You can explore other categories for optimal template utilization.

### Use Cases

The following are some of the use cases that can be addressed with Limited Time Offer templates:

* **Flash Sales or Exclusive Discounts**

<Image alt="Flash Sale" align="center" width="45% " border={true} src="https://files.readme.io/5932e3b-B1g1.png">
  Flash Sale
</Image>

To create a Limited-Time Offer template in CleverTap, follow these steps:

1. From the dashboard, navigate to *Account > Settings > Engage > Channels > WhatsApp*.

2. Choose the *Provider Type*  as **WhatsApp Direct** for CleverTap BSP or **WhatsApp Connect** for external BSPs.

   <Image alt="Select WhatsApp Provider" align="center" border={true} src="https://files.readme.io/ebaed56-image.png">
     Select WhatsApp Provider
   </Image>

3. Select the WABA account or provider to add templates.

   <Image title="image.png" alt={1894} align="center" border={true} src="https://files.readme.io/c423fd6-image.png">
     Select WABA account
   </Image>

4. Select the *Templates* tab and click **+Template**.

   <Image alt="Create a Template" align="center" border={true} src="https://files.readme.io/fb10d89-temp.png">
     Create a Template
   </Image>

5. Select the *Limited Time Offer* template. ***Limited Time Offer* templates are only available with Marketing category.**

<Image alt="Limited Time Offer" align="center" border={true} src="https://files.readme.io/4fe4736-LTO.png">
  Limited Time Offer
</Image>

6. Enter the *Template Name* and configure headers and body as follows:

* For header: Select image or video.
* For body text formatting:
  * **Adding Emojis:** Copy from [here](https://emojipedia.org/most-popular) and paste in the body.
  * **Bold:** Add asterisks (\*) at the beginning and end.
  * **Italic:** Add underscores (\_) at the beginning and end.
  * **Strikethrough:** Add tilde (\~) at the beginning and end.
  * **Monospace:** Add three consecutive backticks (\`\`\`) at the beginning and end.
* If required, add the buttons and fill in the required information.
  * **Copy Code buttons:** You can include only 1 copy code button. When tapped, the code is copied to the customer's clipboard.
  * **Visit Website CTA buttons:**  You can add up to 2 buttons, giving customers three choices:
    * **Static CTA buttons:** Use static URLs for redirection.
    * **Dynamic CTA Buttons:** Brands must provide the URL prefix (URL domain), and the URL suffix can be personalized for each user. For example: [https://www.clevertap.com/\{\{1}}](https://www.clevertap.com/\{\{1}}).
    * **CleverTap Click tracking CTA buttons:** Brands can leverage CleverTap click tracking functionality to monitor details of the user who clicked the URL. The entire URL can be personalized for each user during campaign creation.
* **Quick Reply buttons:** Add up to 5 quick reply buttons. Brands commonly use these buttons to enable users to swiftly respond to WhatsApp messages without typing.
* **Marketing Opt-out button:** You can add 1 marketing opt-out button. This button sends an unsubscription keyword in quick reply format, making it easy for end-users to opt out. Brands need to handle these unsubscription flows properly to ensure end-users get opted out when they tap on this button

7. Configure the Limited-Time Offer (LTO) component according to your specific requirements. The LTO component includes two essential components:

* **Offer Title:** Utilize this section to create a captivating heading for your promotional offer. 
* **Offer Expiry Timer:** This field is optional. If selected, the template will display the time remaining for the offer's expiration, dynamically updating to reflect the time left for the offer to conclude.

<Image alt="Select Offer Expiration Timer" align="center" border={true} src="https://files.readme.io/f3c7941-image.png">
  Select Offer Expiration Timer
</Image>

8. Click **Save Template** to save the message template.
