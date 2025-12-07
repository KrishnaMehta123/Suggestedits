---
title: Define the Message Content
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
Now, you need to set up the _What_ section where you have to define the content for the WhatsApp campaign  Click _Go To Editor_ to create your message. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e4cc8d9-WhatsApp_What.png",
        "Define the Message Type",
        " Define the Message Type for the campaign creation"
      ],
      "align": "center",
      "border": true,
      "caption": "Define Message Type"
    }
  ]
}
[/block]


## WhatsApp Editor

Select from the approved templates.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b4f4fbf-whatsapp_editor.png",
        "Whatsapp Templates",
        "Select any template from the list of Approved Templates"
      ],
      "align": "center",
      "border": true,
      "caption": "Select a Template"
    }
  ]
}
[/block]


Fill in the details and click **Done**. For information about using WhatsApp editor, refer to [WhatsApp editor](https://docs.clevertap.com/docs/whatsapp-message-templates).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/98aa909-Whatsapp_editor_create_message.png",
        "Whatsapp Editor",
        "Personalize the placeholders based on user/event properties and craft the template"
      ],
      "align": "center",
      "border": true,
      "caption": "Personalizing Message"
    }
  ]
}
[/block]


### Custom Key-Value Pair

Marketers utilizing Generic integration can leverage custom Key-Value pairs to transmit additional data within the message payload.

> 🚧 Generic Integration Support
> 
> The Custom Key-Value feature support is currently supported for Generic WhatsApp Integrations.

### Preview & Test

Once you are all done setting up the content of your campaign in the _What_ section, you can send a test notification to any CleverTap user profile you have marked as a _Test profile_.  
Click the **Preview & Test** button from the message editor to test a message.

### Import Templates

> 🚧 Template Import Limitations for External Providers
> 
> Importing templates is exclusive to CleverTap BSP, and for other providers, you must recreate templates separately within their interfaces.

You can also import templates when creating a new message. 

1. Click _Go To Editor_ to create your message.
2. From the message editor, click **Import Templates**. A window for _Import Templates_ displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d48c8e0-2023-09-25_17-21-03.jpg",
        null,
        "Add or Replace Templates"
      ],
      "align": "center",
      "sizing": "60% ",
      "border": true,
      "caption": "Add or Replace Templates"
    }
  ]
}
[/block]


4. Click _Import_ to replace all the templates on your CleverTap dashboard. 
5. Click **Continue** to replace templates.  The CleverTap dashboard shows the new templates. Your previous templates are mailed to your email account.

> 📘 Template Import Impact on Failing WhatsApp Campaigns
> 
> Importing templates will not automatically resolve errors or issues related to the existing WhatsApp campaigns or journeys. These campaigns and journeys will continue to fail until you manually update the imported template in the affected campaign's _What_ section.
> 
> To address campaign failures resulting from template-related errors, please follow the below steps:
> 
> 1. Identify the specific campaign or journey that is encountering the error.
> 2. Access the _What_ section of the campaign or the specific journey node.
> 3. Edit the campaign or journey and select the specific imported templates.
> 4. Save and publish the changes, and check that the campaigns and journeys use the updated templates.

### Quick Reply Button with Custom Payload

CleverTap's _Quick Reply_ feature lets you easily collect user information, track responses, and trigger chat workflows using custom payloads.  
Key-Value Pair

The custom payload Marketers utilizing Generic integration can include custom attributes with the _Quick Reply_ button in the Quick Reply templates when creating campaigns. These custom attributes are not visible to the end user. The purpose of these attributes is to track end-user responses when interacting with specific Quick Reply buttons.

To send a leverage custom payload from the Quick Reply button, you can utilize the [WhatsApp Editor](https://docs.clevertap.com/docs/create-message-whatsapp#whatsapp-editor) provided by CleverTap. When users reply Key-Value pairs to the Quick Reply, the custom payloads are returned along with their responses. These custom payloads can trigger chat workflows and enable further actions based on the user's reply.

To send a custom payload from the WhatsApp Editor, select a Quick Reply template and then select _Add Custom Payload_.

Add a custom payload. You can also [personalize](https://docs.clevertap.com/docs/personalize-message-whatsapp#message-personalization) transmit additional data within the custom message payload.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/862aa69-small-quick_reply_button.png",
        null,
        "Add a Custom Payload"
      ],
      "align": "center",
      "border": true,
      "caption": "Add a Custom Payload"
    }
  ]
}
[/block]


> 📘 Character Limit for Custom Payload
> 
> 🚧 Generic Integration Support
> 
> Check that your custom payload is under **128** characters to ensure deliverability. Although CleverTap does not restrict characters in a custom payload, WhatsApp limits it to 128 characters.

For example, a bus service called ACME operates within a city. ACME wants to make it easy for regular passengers to confirm their daily bus rides. To do this, ACME sends reminder notifications in the evening and morning, matching each user's typical travel schedule.

When a passenger receives the notification, they see a _Confirm Ride_ button. This button enables them to quickly respond and indicate their intention to travel with the bus service immediately. Now, depending on how ACME sets up its system, there are two possible scenarios:

- Without Custom Payload: If ACME does not use a custom payload when a user clicks on the_ Confirm Ride_ button, the user's response is sent directly to ACME's WhatsApp phone number. However, it is unclear to which specific notification the user is responding. For example, ACME does not know whether the user is confirming their ride for today's notification or a previous one. In this case, ACME needs more information, such as the ride details and route, to generate a payment link and complete the transaction.
- With The Custom Payload - When ACME sends the WhatsApp notification, it includes personalized information about the user's route and timing. There is also a _Confirm Ride_ button with a unique identifier attached as a custom payload. This allows ACME to distinguish between different notifications and campaigns. The response and custom payload are captured when the user clicks the _ Confirm Ride_ button. This means ACME knows the exact notification that received a user response. ACME can now directly share the payment link with the user to complete the transaction.

The custom payload Key-Value feature simplifies the process for ACME and its passengers. It eliminates the need for additional confirmation workflows and ensures users receive the correct payment link for their intended ride. Ultimately, this helps ACME provide its customers with a smoother and more efficient experience.

### Track Clicks in WhatsApp Campaigns

The WhatsApp click tracking feature in Meta Dashboard allows you to track the clicks on the CTA (Call To Action) included in your WhatsApp messages. By enabling click tracking, you can gain valuable insights into user engagement and optimize the performance of your WhatsApp campaigns. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d82dc12-Whatsapp_click_track_end_user.jpg",
        null,
        "WhatsApp Click Tracking Message "
      ],
      "align": "center",
      "sizing": "25% ",
      "border": true,
      "caption": "WhatsApp Click Tracking Message "
    }
  ]
}
[/block]


### Branded Domain (Optional)

A branded domain is a custom domain name that replaces CleverTap’s default short URL domains (like `ct3.io`) in your messages. It allows you to display your own company-branded link, improving brand visibility and customer trust.

When **Track Links** is enabled, CleverTap shortens your URLs using a default regional domain. To maintain brand identity and improve user trust, you can configure a branded domain for these links. Once configured, all shortened links in your WhatsApp messages will use your custom domain instead of the default.

To set up your branded domain, follow the steps in the [Branded Domain documentation](https://docs.clevertap.com/docs/branded-domain).

> 📘 Note
> 
> If you send messages to Indian users, ensure your branded domain is also whitelisted on your DLT platform to comply with TRAI regulations.

#### Key Points to Remember

Let us understand how to track a click for various template fields in WhatsApp campaigns. 

##### Headers

- Click tracking support is available only for text headers.
- When using custom variables (for example, {{1}}) in text headers, the system automatically detects URLs in the input box and provides an option to enable click tracking.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e14bea3-Whatsapp_editor_click_track_header_.jpg",
        null,
        "Click Track Text Header"
      ],
      "align": "center",
      "border": true,
      "caption": "Click Track Text Header"
    }
  ]
}
[/block]


- _Example_: If you enter a URL such as  <https://example.com> in a custom variable, the system will automatically detect it and give you the option to enable click tracking. The link will be wrapped (for example, <https://ct1.io/8eytiry>), capturing click information before redirecting the user to the actual URL.

##### Body

- When using custom variables (for example, {{1}}) in the message body, the system automatically detects URLs in the input box and provides an option to enable click tracking.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3234965-Whatsapp_editor_click_track_body.jpg",
        null,
        "Click Track Message Body"
      ],
      "align": "center",
      "border": true,
      "caption": "Click Track Message Body"
    }
  ]
}
[/block]


- _Example_: If you include a URL like <https://example.com> in a custom variable input box, the system will detect it and allow you to enable click tracking. The link will be wrapped (for example, <https://ct1.io/8eytiry>), capturing click information before redirecting the user to the actual URL.

##### Footer

Click tracking is not currently supported for footers because footers cannot be dynamic.

##### CTAs

- To track clicks on CTAs within WhatsApp templates, you must create _ Dynamic URL type CTA _ templates with CleverTap tracking domains in the Generic WhatsApp Account Manager.
- Save these templates as _CleverTap click tracking type templates_ in the CleverTap dashboard.
- _Example_: To track clicks on a _Visit Website_ CTA, create a template with the CTA set as a CleverTap click tracking type. Enter the complete redirection URL in the _What_ section during the campaign creation. The link will be wrapped (for example, <https://ct1.io/8eytiry>), capturing click information before redirecting the user to the actual URL.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/92ab31c-Whatsapp_editor_click_track_button.jpg",
        null,
        "Click Track CTA"
      ],
      "align": "center",
      "border": true,
      "caption": "Click Track CTA "
    }
  ]
}
[/block]