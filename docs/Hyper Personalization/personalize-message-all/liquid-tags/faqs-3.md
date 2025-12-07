---
title: FAQs
excerpt: Explore the answers to frequently asked questions about Liquid Tags.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
### Is there a limit to the number of Liquid commands I can use?

There is no limit on the number of Liquid Tag commands you can use in a message.

### How does Linked Content behave if the campaign hits its limits?

Linked Content is resolved before the campaign checks for the campaign and frequency limits. This means Linked Content (like a coupon API) may still trigger even if a push is not sent due to a campaign limit. CleverTap checks the campaign and frequency limits before resolving Linked Content when dispatching the message.

### Can I use segmentation within Liquid?

Segmentation inside Liquid is not allowed (for example, you cannot create user groups within Liquid logic). To handle different user segments, use profile or event properties within Liquid, or create segments in the “Who” section of the campaign targeting settings.

### In case of missing user data, how do I use Liquid Tags?

You can use the `default` filter to handle cases where user data is unavailable.

### Can I troubleshoot Liquid execution errors?

CleverTap currently does not support viewing Liquid execution logs. To troubleshoot and validate your Liquid logic, send test notifications to internal users while creating a campaign.



### How do I test or validate the Liquid Tags used for my message?

When creating a campaign message with Liquid tags, errors appear in real time if the syntax is incorrect. Errors also surface when clicking **Done** on the campaign creation page if the message contains invalid Liquid Tag syntax. You can also use **Preview & Test** in the message editor to validate your message and send [test campaigns](doc:send-test-personalization-for-unified-inbox) with personalized values. You should test your liquid tags with test user profiles to verify correct behavior.

**Example:** How to add Liquid Tags in the message editor:

![Message Editor](https://files.readme.io/e7aa86c-Add_Liquid_tags.png)

**Validation Example:**

![Validating the Liquid Tag Syntax](https://files.readme.io/0f35bde51577891264842c57d7064bb06d2e0e4608e466c245cf8aa366912050-image.png)

***

Is it possible to use Liquid Tags with HTML?

Yes. Liquid Tags can be used with HTML; however, this section applies only to the email channel. You can combine your HTML code with Liquid Tags to create beautiful and personalized messages for your users. To do so:

1. Open the message editor and paste your HTML code.  
2. Click the ![Liquid tag](https://files.readme.io/651c228-Liquid_tag_icon.png) icon and add your Liquid Tags.

![Add Liquid Tags](https://files.readme.io/e7aa86c-Add_Liquid_tags.png)

### Are Liquid Tags and Linked Content available in Drag-and-Drop Editor? How do I use it?

The drag-and-drop email editor supports Liquid Tags and Linked Content. This functionality allows customers to design and personalize emails using dynamic content when creating an [email campaign](https://docs.clevertap.com/docs/email#section-email-campaign-creation-steps).

1. Select a template.  
   ![Select Media Template](https://files.readme.io/0fc50d2-Select_Media_Template.png)

2. Click the **Row item** in _Preview_.  
   ![Select the Row Tab](https://files.readme.io/b461f6b-2020-07-28_19-19-33_Select_row_item.png)

3. Click _More_ and select **Customize with Liquid Tags**.  
   ![Customize with Liquid Tags](https://files.readme.io/6404ab8-Select_Customize_with_Liquid_Tags.png)

4. Add your Liquid script inside the popup.  
   ![Add Liquid Script](https://files.readme.io/57f0cf4-Add_liquid_script.png)

5. Click **Add**.