---
title: Email Editor(TEC-1105)(gargi)
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
# Overview

The Email Editor tool is a feature available when building an email message in CleverTap. It lets you add content to pre-built templates or customize and build your templates. After creating an email template, you can use it in the current campaign or save it for future campaigns.

From the *What* section in the Email builder, click **Go to Editor**.  

The Email Editor tool displays.

<Image title="Email Editor Templates" alt={1424} align="center" border={true} src="https://files.readme.io/c9ee983-Email_Editor.png" />  Select Email Editor Type

# Select a Template

Decide which template you want and click **Select**.

You can choose between pre-built or empty templates under *Basic Templates*. You can also save customized templates and view them under **Saved Templates**. 

You can choose from the following types of templates:

* **Email with rich media** - Create a rich message with text and images using the built-in email editor. You can also use the Source mode to type or paste in your HTML code. You can also add personalization by using the **@** and **\{\{}}** icons. For more information about personalization, refer to  [Personalize Message](doc:personalize-message-email).
* **Email with drag and drop** - Drag and drop elements such as text, images, and buttons to create a beautiful email message. Convert to HTML to add further customization. 
* **Out-of-the-box templates** - These are drag-and-drop types of templates. Select from the list of ready templates to suit your purposes, such as a blog with photos, order confirmation, offers and deals, feedback forms, and so on.

## Rich Media Template

Create rich messages using rich text and images. There are two ways in which you can create a message.

### Using Built-in Editor

To create a message using a built-in editor:

1. Select *Email with rich media*.
2. Create a template using the Built-in Editor:\
   i. Add the text.\
   ii. Click the icon to insert images.\
   iii. Click the icon to insert links. 

<Image title="Create a Template using Build-in Editor" alt={1410} align="center" border={true} src="https://files.readme.io/2a757b2-Rich_Media_Template.png" />  Email with Rich Media Template

### Using Source Mode

To create a message using a source mode:

1. Select *Email with rich media*.
2. Create a template using Source mode:\
   i. Add your HTML content into the box.
<Image title="Add HTML Content using Source View" alt={1413} align="center" border={true} src="https://files.readme.io/bf4ca46-Source.png" />  View Source Mode











ii. (Optional) Name and save your template for future use. The customized template is saved to *Saved Templates*.

<Image title="View Saved Templates" alt={1408} align="center" border={true} src="https://files.readme.io/60317ea-Search_Template.png" />  Saved Templates











3. Click the **@** and **\{\{}}** icon to add personalization. For more information on personalization, refer to  [Personalize Message](doc:personalize-message-email).

## Drag and Drop Template

Learn how to use an *Email with drag and drop* template. There are many edits you can make to this template. In this step, we will look at three of them: how to change an image, add a new block, and delete an element.

### Change an Image

1. Click inside the box of the image you want to change.

<Image title="Create Content in Email Campaign's Body" alt={1053} align="center" border={true} src="https://files.readme.io/f0237ec-Email_Campaign_Templates_select.png" />  Drag and Drop Editor











2. Click the image.

<Image title="Change and Existing Image Content" alt={1225} align="center" border={true} src="https://files.readme.io/44d57b7-Email_Campaign_Templates_change_image1.png" />  Add Image











3. Click the **Change Image** button. The *File manager* displays.
4. Select an image from the gallery or upload a custom image. 

<Image title="Upload an Image from the Gallery" alt={1225} align="center" border={true} src="https://files.readme.io/3cd76ca-Email_Campaign_Templates_change_image_select.png" />  Upload Image











5. Click Insert. Your new image will appear in the selected box.

<Image title="Insert the Uploaded Image" alt={1305} align="center" border={true} src="https://files.readme.io/e1e933f-Email_Campaign_Templates_image_inserted.png" />  Insert Image











### Add a New Text Block

1. Under the Content tab, find Text.

<Image title="Add a Text Box to Email Content" alt={1324} align="center" border={true} src="https://files.readme.io/ceae7fa-Email_Campaign_add_new_text.gif" />  Add a Tex Block











2. Drag the Text icon to the desired location.

Now you have a new text block.

Similarly, you can also drag other elements such as Images, Buttons, or Videos into your template.

### Delete an Element

1. Click the box of the element you want to delete.
<Image title="Delete an Element from Email Content" alt={1324} align="center" border={true} src="https://files.readme.io/7610436-Email_Editor_delete_element.gif" />  Delete an Element











2. Click the trashcan icon.

3. Click **Delete**.

The element you deleted will no longer appear.

## Rows

You can drag and drop, delete, rename, or re-organize your saved rows, right inside the editor.

1. Select the email with a drag and drop template. 
2. Click the ROWS tab. 
3. Select the **Empty**, **Default**, or **Saved Rows** from the list. You can also update the **Display Condition** for the rows.
4. Drag and drop the row to the editor. 

### Save Rows

To save a row:

1. Double-click the row. 
2. Click the ![folder](https://files.readme.io/54b1fcd-Email_save_icon.png) icon to save the row for future use.

<Image title="Save, Delete and Duplicate the Rows" alt={1164} align="center" border={true} src="https://files.readme.io/67215bf-email_editor_rows_edit_clone_delete.gif" />  Row Properties











### Delete Rows

1. You can delete saved rows from the editor. 
2. Click the ROWS tab in the editor. 
3. Select the saved row and click the ellipsis. 
4. Click **Delete**. 

<Image title="Delete a Saved Row" alt={1306} align="center" border={true} src="https://files.readme.io/eeae8e5-email_editor_rows_delete.png" />  Delete a Saved Row











## Display Condition

Display conditions determine when and under what circumstances certain content is rendered to the recipients.

1. Click the row to which you want to add the display condition.
2. Click **Add Condition** under the **DYNAMIC CONTENT** section. The **Add display conditions** pop-up window appears. The following columns appear.
| Column Name                                   | Description                                                                                                                                                                           |
| :-------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Name                                          | Add your condition name.                                                                                                                                                              |
| Description                                   | Add your description for the condition.                                                                                                                                               |
| Add display condition before the selected row | Add a criteria that is checked before the selected row from the email is rendered. This feature ensures that particular rows are shown only to recipients who meet specific criteria. |
| Add display condition after the selected row  | Add a criteria that is checked after the selected row from the email is rendered. This feature controls the visibility of the content that follows the selected row.                  |

<br />

<Image alt="Email Editor Display Condition" align="center" border={true} src="https://files.readme.io/bb8dfbc-Email_Editor_-_Liquid_Tags.gif" />  Email Editor Display Condition











3. Click **Add** to add the display condition and its details. Click **Cancel** to discard the changes. 

## Mobile View

You can switch between the mobile and desktop views of your message to view and edit content. You can check how the content will display on a mobile phone without going to Previews or sending a test message. Any changes made to the mobile view will be reflected on the desktop view as well. It is a What You See is What You Get (WYSIWYG) editor.

<Image title="View Email Content in Mobile" alt={1096} align="center" border={true} src="https://files.readme.io/bb4fe41-email_editor_mobile_view.gif" />  View Responsiveness











## Template Operations

### Save A Template

This step is optional. You can choose to save a template for future use. Click **Save template**.
<Image title="Save a Template for Future Use" alt={1324} align="center" border={true} src="https://files.readme.io/38aef42-Email_Editor_save_template.png" />  Save a Template











2. Name your template and click Save.

Your template is now saved under **Saved Templates**  tab.

## Search for Saved Template(s)

From the *Create Email* page, you can search for a template by *Template Name*  in the search bar.

<Image alt="Search a Template" align="center" border={true} src="https://files.readme.io/3c269b6-Search_Saved_Template.gif" />  Search a Saved Template











### To Filter Saved Templates

You can filter the saved templates according to HTML or Drag and Drop type. 

1. Click  the <img src= "https://files.readme.io/eca4b7d-Filter_by_icon.png" height="30px" width="30px" /> icon. The *Filter Templates* pane appears on the right side of the screen. 
2. Choose from the filter options in the  *Filter Templates*  pane based on your template search preferences.  

| Drop-down List      | Description                                                                                                      |
| :------------------ | :--------------------------------------------------------------------------------------------------------------- |
| Type                | Select from the following options to filter templates by their type: *Select All*,  *HTML*,  and *Drag and Drop* |
| Created by          | Filter by email ID of the user who created the templates.                                                        |
| Edited by           | Filter by user email ID of the user who edited the templates.                                                    |
| Show only AMP Email | Toggle *Show only AMP Email* option to display only AMP templates.                                               |

3. Click **Apply** to filter templates as per your set preferences, or click **Cancel** to discard the changes.

<Image alt="Filter Saved Templates" align="center" border={true} src="https://files.readme.io/194af74-Filter_Saved_Templates_-_Amp_Email.gif" />  Filter Saved Templates











## To Sort Saved Templates

Select from the *Sort by* dropdown list your desired sorting criteria:

* Created On (Most recent)
* Created On (Oldest)
* Edited On (Most recent)
* Edited On (Oldest)
* Template Name (A to Z)
* Template Name (Z to A)

<Image alt="Sort Saved Templates" align="center" border={true} src="https://files.readme.io/98fe1ac-Sort_Saved_Templates.gif" />
Sort Saved Templates











> 📘 Default Sorting Critera
>
> The templates are sorted using  *Edited Date*  in descending order by default. The *Created On* date of a template is same as the *Edited Date* if you do not edit the template.

# Device Preview

## Dark Mode

You can preview how your email displays in dark mode on a desktop or a mobile phone.

> 📘 Note
>
> Dark Mode is only available in the *Email with drag and drop* editor.

Follow the steps to preview your template in Dark Mode:

1. Select the *Email with drag and drop* editor.

<Image title="Select the Email with Drag and Drop" alt={2866} align="center" border={true} src="https://files.readme.io/fc1d8a8-Select_the_template.png" />  Email with Drag and Drop











2. Draft your message.

<Image title="Create the Email Content" alt={2880} align="center" border={true} src="https://files.readme.io/2e30dbe-Create_message.png" />  Add Content











3. Click the **Preview and Test** button. The *Preview and test* window displays. You can preview how the email will look in dark mode by turning the *Dark Mode* toggle ON.

<Image title="Preview Content in Dark Mode" alt={1440} align="center" border={true} src="https://files.readme.io/c6ed33f-Dark_Mode_Preview.gif" />  View in Dark Mode











> 📘 Dark Mode Preview
>
> Dark Mode support varies across email clients and devices. Test the mails on an email client with dark mode enabled for best results. The Dark Mode preview generates a generic dark mode color scheme when enabled.
>
> Refer to the links below for dark mode email design tips:\
> [5 Tips for Dark Mode Email Design](https://emaildesign.beefree.io/5-tips-for-dark-mode-email-design/)\
> [The Ultimate Guide to Dark Mode for Email Marketers](https://www.litmus.com/blog/the-ultimate-guide-to-dark-mode-for-email-marketers/)

## Inbox Previews with Code Analysis

Inbox Previews with Code Analysis offers you an analysis of your HTML code. It also provides you previews across devices and inboxes before you send out a campaign. The Email Add-On offers you 100 inbox previews a month. 

Before we begin, check that you have enabled Inbox Previews. For enabling the Inbox Previews, see [Enable Email Previews](doc:enabling-previews). Follow the steps to create an email campaign.
1. Select the template. 
2. Create your message.
3. Click the **Preview and Test** button.  The *Previews and test* window displays.
4. Click the **Inbox Previews** tab.
5. Click the **Generate Report** button. The display may take some time if you have selected multiple inboxes. We will render the results and send you a notification email to know when the preview is ready.

<Image title="Generate Report of a Campaign" alt={1648} align="center" border={true} src="https://files.readme.io/9091e36-Screenshot_2021-07-12_at_7.07.10_PM.png" />  Generate Report

6. Click **Inbox Previews** tab to view the preview report. The tests will display email previews across all the selected inboxes. It displays the errors, if any, for each inbox. For selecting inboxes, see [Enabling Previews](doc:enabling-previews).

<Image title="View the Preview Report" alt={1646} align="center" border={true} src="https://files.readme.io/439b55a-Screenshot_2021-07-12_at_7.08.00_PM.png" />  Inbox Previews

7. The *Code Analysis* tab displays the error type and details. You can sort these errors by severity or property.

<Image title="View the Code Analysis" alt={1644} align="center" border={true} src="https://files.readme.io/d94922b-Screenshot_2021-07-12_at_7.08.29_PM.png" />  Code Analysis for Inbox Previews

> 📘 Templates for Inbox Preview
>
> Code Analysis with Inbox Preview is available for the [Custom HTML template](https://docs.clevertap.com/docs/email-editor-templates#custom-html-template) and [Rich Media Template](https://docs.clevertap.com/docs/email-editor-templates#rich-media-template).

8. Click the *Fix issues* in the editor link to fix the issues. You are redirected to the email editor.\
   Rerun the preview tests to check that the previews are in order.

## Spam Report

A spam report allows you to test your email for deliverability by creating a spam report. The Email Add-On offers you 100 spam reports a month.

Follow the steps to create an email campaign.

1. Select the template. 
2. Create your message.
3. Click the **Preview and Test** button. The *Previews and test* window displays.
4. Click the **Spam Report** tab.
5. Click the **Generate Report** button.

<Image title="Generate Spam Report" alt={1648} align="center" border={true} src="https://files.readme.io/9091e36-Screenshot_2021-07-12_at_7.07.10_PM.png" />  Generate Spam Report