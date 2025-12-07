---
title: Email Editor
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
  pages:
    - type: link
      title: Email Personalize
      url: https://docs.clevertap.com/docs/personalize-message-email
    - type: link
      title: Handling Unsubscribes
      url: https://docs.clevertap.com/docs/handling-unsubscribes-c20
    - type: link
      title: Group Unsubscribe
      url: https://docs.clevertap.com/docs/group-unsubscribe-new
    - type: link
      title: Override Link Tracking
      url: https://docs.clevertap.com/docs/override-link-tracking-c20
    - type: link
      title: Email Campaign Stats
      url: https://docs.clevertap.com/docs/email-stats
    - type: link
      title: Email Troubleshooting
      url: https://docs.clevertap.com/docs/troubleshooting-email
---
# Overview

The Email Editor tool is a feature available when building an email message in CleverTap. It lets you add content to pre-built templates or customize and build your templates. After creating an email template, you can use it in the current campaign or save it for future campaigns.

From the *What* section in the Email builder, click **Go to Editor.**  

The Email Editor tool displays.

<Image title="Email_editor_main.png" alt={1121} className="border" border={true} src="https://files.readme.io/670c841-Email_editor_main.png" />

# Select a Template

Decide which template you want and click **Select**.

You can choose between pre-built templates or empty templates under *Basic Templates*. You can also save customized templates and view them under **Saved Templates**.

You can choose from the following types of templates:

* Email with custom HTML - Add your custom HTML to create custom email messages. You can also add personalization by using the **@** and **\{\{}}** icons. For more information on personalization, see [Personalize Message](doc:personalize-message-email).
* Email with rich media - Create a rich message with text and images by using the inbuilt email editor. You can also add personalization by using the **@** and **\{\{}}** icons. For more information on personalization, see [Personalize Message](doc:personalize-message-email).
* Email with drag and drop - Drag and drop elements such as text, images, and buttons to create a beautiful email message. Convert to HTML to add further customization. 
* Templates by use cases - These again drag and drop types of templates. Select from a list of ready templates to suit your purpose, such as a blog with photos, order confirmation, offers and deals, feedback forms, and so on.

## Drag and Drop Template

Learn how to use an *Email with drag and drop* template. There are many edits you can make to this template. In this step, we will look at three of them: how to change an image, add a new block, and delete an element.

### Change an Image

1. Click inside the box of the image you want to change.

<Image title="Email_Campaign_Templates_select.png" alt={1053} className="border" border={true} src="https://files.readme.io/f0237ec-Email_Campaign_Templates_select.png" />

2. Click the image.

<Image title="Email_Campaign_Templates_change_image1.png" alt={1225} className="border" border={true} src="https://files.readme.io/44d57b7-Email_Campaign_Templates_change_image1.png" />

3. Click the **Change Image** button. The *File manager* displays.
4. Select an image from the gallery or upload a custom image. 

<Image title="Email_Campaign_Templates_change_image_select.png" alt={1225} className="border" border={true} src="https://files.readme.io/3cd76ca-Email_Campaign_Templates_change_image_select.png" />

4. Click Insert. Your new image will appear in the selected box.

<Image title="Email_Campaign_Templates_image_inserted.png" alt={1305} className="border" border={true} src="https://files.readme.io/e1e933f-Email_Campaign_Templates_image_inserted.png" />

### Add a New Text Block

1. Under the Content tab, find Text.

<Image title="Email_Campaign_add_new_text.gif" alt={1324} className="border" border={true} src="https://files.readme.io/ceae7fa-Email_Campaign_add_new_text.gif" />

2. Drag the Text icon to the desired location.

Now you have a new text block.

Similarly, you can also drag other elements such as Images, Buttons, or Videos into your template.

### Delete an Element

1. Click the box of the element you want to delete.

<Image title="Email_Editor_delete_element.gif" alt={1324} className="border" border={true} src="https://files.readme.io/7610436-Email_Editor_delete_element.gif" />

2. Click the trashcan icon.

3. Click **Delete**.

The element you deleted will no longer appear.

## Save A Template

This step is optional. You can choose to save a template for future use. 

1. Click **Save template**.

<Image title="Email_Editor_save_template.png" alt={1324} className="border" border={true} src="https://files.readme.io/38aef42-Email_Editor_save_template.png" />

2. Name your template.

3. Click Save.

Your template will now be saved in My Gallery.

## Custom HTML Template

The Custom HTML template helps you to create custom HTML templates of your choice.

1. Click **Email with custom HTML**.

<Image title="Email_Campaign_select_templates.png" alt={1140} className="border" border={true} src="https://files.readme.io/9eb5ed9-Email_Campaign_select_templates.png" />

2. Add your HTML into the box. You can also add personalization by using the **@** and **\{\{}}** icons. For more information on personalization, see [Personalize Message](doc:personalize-message-email). 

<Image title="Email_Campaign_template_custom_html.png" alt={1140} className="border" border={true} src="https://files.readme.io/d38dd3b-Email_Campaign_template_custom_html.png" />

3. Name and save your template. This step is optional. You can choose to save a template for future use. 

<Image title="Email_Campaign_template_custom_html_Name.png" alt={1140} className="border" border={true} src="https://files.readme.io/6890680-Email_Campaign_template_custom_html_Name.png" />

4. Click Save.

Your customized template will now be saved to *Saved Templates*.

## Rich media Template

Create rich messages using rich text and images. 

1. Select Email with rich media.
2. Add your text. 
3. Click the icon to insert images. 
4. Click the icon to insert links. 
5. Click the **@** and **\{\{}}** icon to add personalization. For more information on personalization, see [Personalize Message](doc:personalize-message-email). 

![1219](https://files.readme.io/b10e8da-Email_template_rich_media.png "Email_template_rich_media.png")

# **Inbox Previews with Code Analysis**

Inbox Previews with Code Analysis offers you an analysis of your HTML code. It also provides you previews across devices and inboxes before you send out a campaign. The Email Add-On offers you 100 inbox previews a month. 

Before we begin, check that you have enabled Inbox Previews. For enabling the Inbox Previews, see [Enable Email Previews](doc:enabling-previews). Follow the steps to create an email campaign. 

1. Select the template. 
2. Create your message.
3. Click the **Preview and Test**button.  The *Previews and test* window displays.
4. Click the **Inbox Previews** tab.
5. Click the **Generate Report** button. The display may take some time if you have selected multiple inboxes. We will render the results and send you a notification email to know when the preview is ready. 

<Image title="Screenshot 2021-07-12 at 7.07.10 PM.png" alt={1648} className="border" border={true} src="https://files.readme.io/9091e36-Screenshot_2021-07-12_at_7.07.10_PM.png" />

6. Click **Inbox Previews** tab to view the preview report. The tests will display email previews across all the selected inboxes. It displays the errors, if any, for each inbox. For selecting inboxes, see [Enabling Previews](doc:enabling-previews). \<\<@harsh, the spam reports and inbox reviews do not render>>

<Image title="Screenshot 2021-07-12 at 7.08.00 PM.png" alt={1646} className="border" border={true} src="https://files.readme.io/439b55a-Screenshot_2021-07-12_at_7.08.00_PM.png" />

7. The *Code Analysis* tab displays the error type and details. You can sort these errors by severity or property. \<\<@harsh to check if the property still holds true>>

<Image title="Screenshot 2021-07-12 at 7.08.29 PM.png" alt={1644} className="border" border={true} src="https://files.readme.io/d94922b-Screenshot_2021-07-12_at_7.08.29_PM.png" />

> 📘 Templates for Inbox Preview
>
> Code Analysis with Inbox Preview is available for the [Custom HTML template](https://docs.clevertap.com/docs/email-editor-templates#custom-html-template) and [Rich Media Template](https://docs.clevertap.com/docs/email-editor-templates#rich-media-template).

8. Click the *Fix issues* in the editor link to fix the issues. \<\<@harsh to check if property still holds true>>You are redirected to the email editor.\
   Rerun the preview tests to check that the previews are in order.

# **Spam Report**

A spam report allows you to test your email for deliverability by creating a spam report. The Email Add-On offers you 100 spam reports a month. 

Follow the steps to create an email campaign. 

1. Select the template. 
2. Create your message.
3. Click the **Preview and Test**button.  The *Previews and test* window displays.
4. Click the **Spam Report** tab.
5. Click the **Generate Report** button. \<\<@harsh, what happens after this step? The spam report does not render>>

<Image title="Screenshot 2021-07-12 at 7.07.10 PM.png" alt={1648} className="border" border={true} src="https://files.readme.io/9091e36-Screenshot_2021-07-12_at_7.07.10_PM.png" />
