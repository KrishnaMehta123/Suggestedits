---
title: In-App Editor
excerpt: Learn how to edit and design In-App campaigns from the CleverTap dashboard.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

 The In-App editor enables you to add content to pre-built templates or customize and build them. You can select the ready-to-use template of your choice or create a custom HTML template as per your requirements. From the *What* section in the In-App builder, select the *Message Type* and click **Go to Editor.**

The In-App Editor tool displays.

<Image align="center" className="border" border={true} src="https://files.readme.io/0d4cd27-image_interstitial.png" />

# In-App Templates

The following are the four main types of In-App templates for creating engaging and personalized In-App campaigns:

* [*Basic Templates*](doc:in-app-editor#basic-templates)
* [*Ratings Templates* ](doc:in-app-editor#ratings-template)
* [*Lead Generation Templates*](doc:in-app-editor#lead-generation-template)
* [*Custom HTML Templates*](doc:in-app-editor#custom-templates)

## Basic Templates:

Basic Templates are ready-to-use templates that enable you to send tailored and personalized In-App engagements to your mobile users. You can use both text and images with CTAs to send personalized In-App messages basis your business use case.

Using basic templates, you can create the following two types of In-App messages:

* [Content with Image notifications](doc:in-app-editor#content-with-image-notifications)
* [Image-only notifications](doc:in-app-editor#image-only-notifications)

### Content with Image notifications

These templates allow you to use images in combination with text for effective messaging. You can choose from a range of templates such as *Cover*, *Half Interstitial*, *Interstitial*, *Header*, *Footer*, and *Alert*  based on your use case.

### Image-only notifications

These templates allow you to send visually engaging images that can quickly capture users' attention and encourage them to engage with the message when they launch the app. When selecting an *image only* template, you can send a message containing only an image (without CTAs, title, or message).

You can choose from the following four types of Image only notifications:

#### Cover

It is a full-screen notification template that is valuable when the intention is to direct the user's focus toward essential actions, such as requiring them to install a necessary app update.

#### Half Interstitial

It is a center-aligned image notification template for driving better engagements. You can use this template when you want to gain the user's attention towards a sale or discount.

#### Interstitial

 It is a center-aligned image notification template you can use for driving better engagements on app launch.

#### Image Interstitial

> 📘 Availability
>
> The **Image Interstitial** template is available only with CleverTap Advanced and Cutting Edge plans.

This template helps craft personalized In-App messages that seamlessly match your app's aesthetics. You upload an image and elevate the experience by incorporating up to 10 interactive hotspots, each with its own unique actions. For example, you can use this template to create a rewarding offer for your gaming app users. The following image represents a sample In-App campaign for rewarding users using the Image Interstitial template:

<Image alt="Sample In-App Campaign using Image Interstitial Template" align="center" border={true} src="https://files.readme.io/7da5c6a-Image_Interstitial_full.png">
  Sample In-App Campaign using Image Interstitial Template
</Image>

The Image Interstitial template primarily comprises the following three elements:

* Overlay: This element is a middle layer between your In-App message and your app in the background. By default, it is transparent; however, you can select a color of your choice or upload an image to it. Using the Overlay configuration, you can:
  * Opt for a semi-transparent color to softly mask the app in the background, drawing more attention to the in-app message in the foreground.
  * Upload a patterned image to create a captivating, full-screen, layered in-app message experience.
* Content: It is the core element of the template. Click in the center of a blank device or select the **Content** option from the *Element* dropdown to activate it. Further, upload an image (JPG, PNG, or GIF) consisting of all In-App message elements such as background, text, and buttons.\
  The editor fits the image within the Content container while preserving its aspect ratio without any cropping. By default, a 10% margin is applied to the Content container. However, you can change that from the *Margin* field.
* Buttons:  The Image Interstitial buttons are transparent regions that you can place over a Content layer. You can easily move and adjust their size to align with the button elements on the image. 

The selection area within the Content Container automatically adapts to various device screen sizes, eliminating the need to create multiple versions for different devices. To see how the image and buttons scale across different aspect ratios, use the dropdown menu with different device viewport sizes located at the top for a preview.

> 📘 Preview & Test
>
> * The *Preview & Test* feature for sending tests on the device is not available for iOS or Android SDK versions lower than **6.0.0** and Unity **3.0.0.** If you need to test on a device with a lower SDK version, send the campaign exclusively to the user first, and then recreate and send it to the intended audience.

### Guidelines for Template Aspect Ratio and File Size

The following tables include the guidelines that you must keep in mind when creating In-App messages:

<Table align={["left","left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Canvas Type
      </th>

      <th>
        Canvas Aspect Ratio
      </th>

      <th>
        Sample Image Sizes
      </th>

      <th>
        Image Type Supported
      </th>

      <th>
        Image Sample
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Cover
      </td>

      <td>
        Full Screen
      </td>

      <td>
        Screen Resolution
      </td>

      <td>
        Image
      </td>

      <td>
        <ul>
        <li><a href="https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Cover-iPad.jpg">Cover iPad</a></li>
        <li><a href="https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Cover.jpg">Cover</a> </li>
        </ul>  
          
        <br />
      </td>
    </tr>

    <tr>
      <td>
        Interstitial
      </td>

      <td>
        1.78:1
      </td>

      <td>
        16:9
      </td>

      <td>
        Image, gif, audio, video
      </td>

      <td>
        <ul>
        <li><a href="https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Interstitial-iPad-Pro.jpg">Interstitial iPad Pro</a></li>
        <li><a href="https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Interstitial-iPad.jpg">Interstitial iPad</a></li>
        <li><a href="https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Intertitial.jpg">Interstitial</a> </li>
        </ul>  
          
        <br />
      </td>
    </tr>

    <tr>
      <td>
        Half Interstitial
      </td>

      <td>
        1.30:1
      </td>

      <td>
        3:4
      </td>

      <td>
        Image
      </td>

      <td>
        <ul>
        <li><a href="https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Half-Interstitial-ipad-Pro.jpg">Half Interstitial iPad Pro</a></li>
        <li><a href="https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Half-Interstitial-ipad.jpg">Half Interstitial iPad</a></li>
        <li><a href="https://eu1-dashboard-beepluginuploads3bucket-174u3y07szypz.s3.amazonaws.com/images/ZWW-WWW-WWRZ/Sample-Half-Intertitial.jpg">Half Interstitial</a> </li>
        </ul>  
          
        <br />
      </td>
    </tr>

    <tr>
      <td>
        Header
      </td>

      <td>
        Height: 1:1\
        Width: Fit to screen
      </td>

      <td>
        N/A
      </td>

      <td>
        Logo Image
      </td>

      <td>
        Title :parameters]\
        \{\
        , Message \{\
            "h-0": "C\* Title e",\
            "h-1": , Message pect Ratio",\
           Title : "Sample Image, Message \[75 Characters
      </td>
    </tr>

    <tr>
      <td>
        Footer
      </td>

      <td>
        Height: 1:1\
        Width: Fit to screen
      </td>

      <td>
        N/A
      </td>

      <td>
        Logo Image
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Alert
      </td>

      <td>
        Native
      </td>

      <td>
        N/A
      </td>

      <td>
        N/A
      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Image Only Cover
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Image Only Half Interstitial
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>

    <tr>
      <td>
        Image Only Interstitial
      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>

      <td>

      </td>
    </tr>
  </tbody>
</Table>

#### File Size Guidelines

* **Image**: Less than 500 kb.
* **Audio**: Less than 5 Mb.
* **Video**: Less than 50 Mb.

#### Message Character Limit

| Language | Title           | Message          |
| :------- | :-------------- | :--------------- |
| English  | 30              | 128              |
| Chinese  | 9 (Approximate) | 38 (Approximate) |
| Arabic   | 9 (Approximate) | 38 (Approximate) |

> 🚧 Image Cropping
>
> Due to the multiple phone sizes on both Android and iOS, we will center crop images if the image does not fit the screen resolution.\
> We scale the image uniformly (maintaining the image's aspect ratio) so that both dimensions (width and height) of the image will be equal to or larger than the corresponding dimension of the phone (minus padding). The image is then center-aligned.
>
> **Image Cropping does not apply for Image Interstitial template.**

> 🚧 Video Messages
>
> When adding video messages to In-App, ensure an audio track is always present.\
> If required, insert a blank audio track to the video.

## Ratings Template

Marketers can now create feedback-related popups for their mobile app users using the *Ratings Template.*\
They can now create two types of rating templates for gaining feedback from their customers:

* User Rating Popup - It helps assess how happy your customers are with your services by taking feedback in the form of star ratings.
* NPS Popup - It enables you to measure the loyalty of your customers by distinguishing them in three categories - **Promoters**, **Passives**, **Detractors**.  One can view the NPS performance by navigating to the [NPS board](doc:nps-board) available under the *Boards* section.

The following images represent a sample *User Rating Popup* and *NPS popup* in a mobile app.

<Image title="Capture User Rating" alt={568} align="center" width="40% " border={true} src="https://files.readme.io/cc3f275-inapp.png">
  User Ratings Popup
</Image>

<Image title="Capture NPS" alt={542} align="center" width="40% " border={true} src="https://files.readme.io/3d18243-in-app_nps.png">
  NPS Popup
</Image>

Marketers get the complete flexibility to explicitly define the rating scale, style, shape (Star, Heart, Emojis), labels, and the overall content of the popup. One can also choose to add a comment box to get accurate user feedback/comments.

<Image title="Style Rating Template Elements" alt={2044} align="center" border={true} src="https://files.readme.io/d76e790-in_app_styles.png">
  In-App Editor Style
</Image>

Besides, additional styling, such as configuring the color for the message, question, background, and rating scale is also possible from the editor, as shown in the image above. The In-App notification text fields shown below can be personalized for every user based on specific user property or event property values. To learn more about tracking and monitoring user rating data, refer to [Analysing User Rating](doc:user-ratings).

<Image title="Compose In-App Message for Ratings Template" alt={1694} align="center" border={true} src="https://files.readme.io/ae7f02c-rate.png">
  Compose In-App Message
</Image>

### Follow-up Question Templates

A follow-up question to your ratings can provide more insights about the user experience. CleverTap provides the following Follow-up Question templates:

* NPS with Follow-up Question
* User Ratings with Follow-up Question

For example, after a user has submitted a rating on your app, you can ask follow-up questions such as *What did you like most about us?* and provide reply choices such as Variety, Prices, Quality, Customer Service, Delivery Process, and Website Usability. This can help you get more specific feedback to improve your product and services. Following is an image from the in-app editor: 

<Image alt="Short Keyword Choices" align="center" width="50% " border={true} src="https://files.readme.io/4766cd8-inapp_followup_nps.jpg">
  Short Keyword-Based Choices
</Image>

You can also list descriptive choices such as, *I like the available options and variety*, *I like the quality and durability of the products*, and so on. Following is an image from the in-app editor:

<Image alt="Long Sentence Choices" align="center" width="50% " border={true} src="https://files.readme.io/0decade-inapp_followup_qs_list.jpg">
  Descriptive Choices
</Image>

You can configure the follow-up question from the Web Popup editor with a short keyword-based grid (up to six choices) or a longer sentence-based list (up to four choices).

The label will be the text you want to display to your users. If you want to allow the user to select multiple choices, select *Allow multiple selections*.

<Image alt="Configure Follow-up Popup" align="center" width="80% " border={true} src="https://files.readme.io/fd33f9a-image_18.png">
  Configure Follow-up Popup
</Image>

> 📘 Note
>
> In the case of the User Ratings template, the *Notification Clicked* event is raised that records the user's clicks on the CTA buttons and the Close button

## Lead Generation Template

We know that a significant number of App users may remain anonymous. This poses a challenge to continue engaging with potential customers after they leave your App. A lead generation template can solve this issue.

Integrating a lead generation form into your App lets you get important customer details such as name, email address, phone number, etc. This information is helpful for further communication through channels such as SMS, Email, WhatsApp, and others. This post-visit communication helps stay connected with your audience and opens doors for future business opportunities. You can turn anonymous visitors into loyal customers with your App's CleverTap Lead Generation Template.

<Image alt="Sample Lead Generation Template" align="center" width="40% " border={true} src="https://files.readme.io/3658161-InApp_Lead_Gen_sample_window.png">
  Sample Lead Generation Template
</Image>

### Post Submit Actions

When a user submits information on your Lead Generation template:

* A *Notification Clicked* event is raised that records the click on the CTA. 

* A custom event named *Lead Submitted* records the details submitted by the user as of event properties. Following is a sample form image:

<Image alt="Form Submit Actions" align="center" width="50% " src="https://files.readme.io/0cae15f-Lead_Gen_Template_preview_with_fields.png">
  Form Submit Actions
</Image>

Following is a table that records the relevant properties for the fields displayed on the form:

| Submitted Event Properties | Sample Property Value               |
| :------------------------- | :---------------------------------- |
| First Name                 | John                                |
| Last Name                  | Smith                               |
| Email ID                   | [john@abc.com](mailto:john@abc.com) |
| Phone Number               | \+11234567890                       |
| Campaign ID                | 121110987654                        |
| Variant                    | wzrk\_default                       |

* The user profile is automatically updated with the submitted event properties. For example, the lead generation template can ask for additional details from an anonymous user, such as first name, last name, email, and phone number. His profile will be updated with these details, and now you can identify the user as *John Smith*.

### Lead Generation Template Variants

The following are the two types of Lead Generation templates:

* **Text**: You can create a text-only lead generation template to record user information. 
* **Image on Top**: You can add an image on the top to the lead generation template. 

Create the content to record information from your users. The following image displays a preview of the form:

<Image alt="Create Lead Generation Template" align="center" border={true} src="https://files.readme.io/035a137-lead_gen.png">
  Create Lead Generation Template
</Image>

Select the button style and card positions from the *Style* tab.

<Image alt="Style Lead Generation Elements" align="center" border={true} src="https://files.readme.io/06cbbe4-In-App_Template_Lead_Gen_Content_Editor.png">
  Style Lead Generation Elements
</Image>

Enter all the required information. 

* *Text*: Personalize the Title and Description. 
* *Media*: Add the image URL or upload an image. 
* *Input Fields*: You can add up to four input fields. Select input fields such as Name, Phone Number, Birthday, or Email Address for the template. 

<Image title="Lead Gen Template Input Fields.png" alt={1304} align="center" width="60% " border={true} src="https://files.readme.io/6a87857-Lead_Gen_Template_Input_Fields.png">
  Upto Four Input Fields 
</Image>

* *Buttons*: The *Close* button is selected by default. Add a button name such as *Submit* or *Upload*. 
* *Subtext*: Add subtext such as *privacy policy* to your lead generation template.

<Image title="Lead Gen Template SubText preview.png" alt="Add Subtext" align="center" width="55% " border={true} src="https://files.readme.io/bb6e1f2-Lead_Gen_Template_SubText_preview.png">
  Add Subtext
</Image>

The hyperlinked part must be closed between two asterisks. Add the URL where the user will be directed. You can also add a checkbox for your subtext.

<Image title="Lead Gen Template SubText.png" alt="Subtext and redirect URL" align="center" width="55% " border={true} src="https://files.readme.io/d740b86-Lead_Gen_Template_SubText.png">
  Subtext and redirect URL
</Image>

* *Acknowledgement*: You can show appreciation to your user by adding an Acknowledgement popup. Select the auto-close timer for the popup.

Select the button style and card positions from the *Style* tab.

<Image alt="Card Orientation" align="center" border={true} src="https://files.readme.io/92ac44f-In-App_Template_Types_Lead_Gen_Style.png">
  Card Orientation
</Image>

## Custom Templates

You can use the Custom HTML templates in the In-App editor to add more customization to the In-App messages with Javascript.\
Ensure that you select the *Include Javascript* box to add your custom Javascript. 

<Image title="Custom Template with HTML and Javascript" alt={1108} align="center" border={true} src="https://files.readme.io/5638bd2-in-app_journey_custom_HTML.png">
  Custom HTML and Actions
</Image>

> 📘 Create Interactive In-App Messages
>
> You can create interactive in-app campaigns such as scratch card campaigns and swipe interaction campaigns using JavaScript.
>
> Using the *Custom HTML* option, you can use Javascript in the HTML and create deep interactive in-app campaigns by adding the JavaScript code along with the HTML code. 
>
> JavaScript-based campaigns are available for versions 3.5.0 and above.

## Custom Code Templates \{@sunil to remove it}

You can easily import your custom designs into CleverTap using custom code templates. It allows you to maintain your app's unique look and feel. This integration will enable you to conveniently control message delivery preferences, frequency, and other aspects. The custom templates can be used as key-value pairs, providing a simple way to create highly complex and customized messages without needing to write any code. This integration also eliminates the need for third-party tools to update your messaging. CleverTap gives you complete control over message delivery, frequency, and limits without requiring code modifications. You can use your designs and CleverTap's robust delivery capabilities to ensure design, rendering, and visualization consistency.

<Image alt="Sample custom in-app" align="center" border={true} src="https://files.readme.io/bee5455-image.png">
  Sample Custom In-App
</Image>

The key-value pairs can be a string, number, image, or file type. Your developers can send the code to CleverTap using the CleverTap SDK. For more information about the integration, refer to the \{in-app dev doc}. After the integration, you can begin creating templates from the CleverTap dashboard.

<Image alt="Editing a Custom Code Template" align="center" border={true} src="https://files.readme.io/75f1c5a-image.png">
  Edit Custom Code Template
</Image>

## App Functions

App functions are functions provided by CleverTap that can trigger native OS prompts (Android or iOS) for different use cases. These App Functions trigger native prompts to engage users from within the app at the right moment. These prompts are the following: 

* App Rating -  Encourage app ratings during high-satisfaction moments from within the app.
* Push Permission -  Increase opt-in rates for push notifications from within the app.
* Open URL - Guide users to external links or deep-linked screens at key user moments  to improve engagement from within the app.

These functions are designed to be embedded within in-app messages (as button actions) or launched directly as standalone in-app campaigns.

Using app functions as a button in an in-app 

<Image alt="System App Functions" align="center" border={true} src="https://files.readme.io/7dd551689091fc009864e7abcb42f5cf5ad3076f096b1541df5cde697dfdc322-image.png">
  System App Functions
</Image>

### App Function as Button \{@sunil to rethink the headings}

<br />

\{@martin to share the rendered app rating screenshot}

How ths can be used.

Embed app function as a button in in-app.

\{@martin, the app functions as button can be used only from advanced in-app builder right ? should we keep this section here then ?}

Increase the likelihood that a user will allow a push on the device or provide a positive app rating.

<br />

<br />

Using app function as an action button in in-apps allows you to 

Use App Functions as button actions to trigger native app prompts, such as requesting ratings, push permissions, or opening URLs, directly when a user taps a button in your in-app message.

<Image alt="App Function as a button" align="center" border={true} src="https://files.readme.io/afc88054ed2adc8e072e5c216b13905469e64289a6e2f74b762bbb8430e33c6e-image.png">
  App Function as a Button
</Image>

To use an app function as a button in an in-app message:

1. Create In-App campaign.  
2. Go to the *What* section and open the Advanced In-App Builder.
3. Add a button to your message layout.
4. In the On Tap list for the button, select App Function.
5. Select any one of the following App Functions:

Choose one of the following **App Functions** in the button action dropdown:

<Table>
  <thead>
    <tr>
      <th>
        App Function
      </th>

      <th>
        Description
      </th>

      <th>
        Considerations and  Recommended Use Cases
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Request App Rating**
      </td>

      <td>
        Displays the native app store rating prompt.
      </td>

      <td>
        * OS platforms control when and how often the prompt appears (may not always show). <br /> - No analytics events are tracked.<br /> Use after a positive interaction (e.g., subscription renewal, milestone).
      </td>
    </tr>

    <tr>
      <td>
        **Request Push Permission**
      </td>

      <td>
        Prompts the user for push notification permissions.
      </td>

      <td>
        * Prompt won’t show if permission is already granted. <br /> - If previously denied, redirects to app settings.<br /> Use after value explanation in a prior screen.
      </td>
    </tr>

    <tr>
      <td>
        **Open URL**
      </td>

      <td>
        Opens a web page or app deep link.
      </td>

      <td>
        * URL open events are not tracked.<br /> - Ensure URL is valid and accessible across platforms.<br />  Use for external content, offers, or account linking.
      </td>
    </tr>
  </tbody>
</Table>

<br />

> 📘 Tip
>
> Always include a context-setting message before triggering system prompts. For example, explain the value of enabling notifications before displaying the push permission dialog.

### App Function as Campaign

\{@martin to share the rendered app rating screenshot}

You can use App Functions as a campaign when you want to engage the user after specific actions. For example, a user is more likely to accept push prompts from the app after purchasing to track the item's delivery.  

<Image alt="App Function as a campaign" align="center" border={true} src="https://files.readme.io/7d621f9905b1c6cc33e754396027174215e7376ea7915c7f391b20c85e25afb4-image.png">
  App Function as a campaign
</Image>

<br />

To use an app function as a stand-alone campaign: 

1. Create In-App campaign.  
2. Go to the *What* section and open the In-App Editor. 
3. Click the *App Functions* tab. The app functions will display. 
4. Select from the following App functions to run as a standalone campaign: 

<Table>
  <thead>
    <tr>
      <th>
        App Function
      </th>

      <th>
        Description
      </th>

      <th>
        System Behavior
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Request App Rating**
      </td>

      <td>
        Prompts the native app store rating dialog.
      </td>

      <td>
        * May not always appear (controlled by OS)<br />- Cannot be forced or tracked
      </td>
    </tr>

    <tr>
      <td>
        **Request Push Permission**
      </td>

      <td>
        Triggers the OS-level push notification permission prompt.
      </td>

      <td>
        * If **granted**: prompt is skipped<br />- If **denied**: user is redirected to Settings<br />- If **not yet asked**: prompt is shown
      </td>
    </tr>

    <tr>
      <td>
        **Open URL**
      </td>

      <td>
        Opens a web page or deep link.
      </td>

      <td>
        * Tracks `Notification Viewed` for campaign<br />- URL click itself is **not** tracked
      </td>
    </tr>
  </tbody>
</Table>

> 📘 **Note**
>
> App Functions triggered as standalone campaigns do **not** display an in-app message overlay. These are native system calls executed directly from CleverTap.

### Event Tracking Matrix

Understand what system events are tracked when using each App Function. Tracking behavior differs between **button-triggered** functions and **standalone** in-app campaigns.

| App Function                | Used As             | `Notification Viewed` | `Notification Clicked` | Other Events Tracked? | Notes                                                                  |
| --------------------------- | ------------------- | --------------------- | ---------------------- | --------------------- | ---------------------------------------------------------------------- |
| **Request App Rating**      | Button Action       | Yes                   | Yes                    | No                    | Tracks standard in-app events only, not rating prompt outcome.         |
|                             | Standalone Campaign | No                    | No                     | No                    | OS restricts tracking when system rating dialog is triggered directly. |
| **Request Push Permission** | Button Action       | Yes                   | Yes                    | No                    | Tracks campaign events, but **not** the native push prompt             |
|                             | Standalone Campaign | Yes                   | No                     | No                    | Tracks prompt **view**, but not **click** or OS permission result.     |
| **Open URL**                | Button Action       | Yes                   | Yes                    | No                    | Tracks only the in-app message interaction.                            |
|                             | Standalone Campaign | Yes                   | No                     | No                    | Only campaign view tracked; URL destination is not tracked.            |

> 📘 **Note**
>
> *Notification Viewed* and *Clicked* refer to **in-app campaign events**, not the system prompt itself. CleverTap cannot track actions performed within OS-native dialogs.

<br />

### Using App Functions

Turn any in-app that is created on our editor into a pre-permission campaign by connecting it to the in-app function. Native app prompts are generally irreversible and one-time actions. App functions can act as a first and reversible layer for user action and prime the user before presenting the user with the system prompt, such as rating the app or requesting push permission on the device. \{@sunil to reuse this section later}

<br />

#### Push Pre-Permission

\{add a visual here}

Imagine having to ask for permission to deliver a push to the user's device. A native prompt is available in the device OS (Android or iOS) to achieve this. However, this being a native app prompt, it will be executed only once. The user has only one chance to either accept or reject it. There is no chance for regret. However, you can add an introductory layer

<br />

The user can create an in-app message using our editor by simply having a button with this function. fast-track and achieve the push pre-permission use case by using the Out of the box structure provided by clevertap. 

Same for app rating

No steps required. 

<br />

#### App Rating Lead-In

\{add a visual here}

<br />

<br />

as a button

as a campaign

<br />

How to achive push permission \{with images}

How to achieve the ask for rating \{with images}

<br />

Martin wants to add a separate page for app functions.

1. What are app functions
2. How easy it is to create native app prompts using CleverTap 
3. use cases such as app rating, push pre-permissions

[https://docs.leanplum.com/docs/push-pre-permission-message](https://docs.leanplum.com/docs/push-pre-permission-message)

[https://docs.leanplum.com/docs/app-function](https://docs.leanplum.com/docs/app-function)

# Time to Live (TTL)

You can configure the number of days (or hours) to keep the message on the user's device by setting the *time to live*.

<Image title="Configure Time to Live for In-App Message" alt={630} align="center" border={true} src="https://files.readme.io/35148df-in-app_time_to_live.png">
  Time to Live for a Message
</Image>

The TTL can range from 1 day to 365 days. The default value for TTL is two days. The message on the user's device stays for the specified TTL, after which it is automatically removed.

> 🚧 Choosing the Right TTL
>
> You should choose a TTL that resonates with the purpose of your campaign. Some messages need to stay on the user's device for a longer period (coupon codes which are valid for a month) while some should last for a day or two (weekend discount offers).

# In-App Editor

Use the In-App editor to craft your In-app campaign with the desired messaging and styling best suited for your business. You can choose from a range of In-App templates. Alternatively, you can also use the Custom HTML option to build your own campaign.

The elements of the editor vary based on the type of template you select for creating your In-App campaign.

The following image represents the *Content with image notifications* template editor. 

<Image title="Basic Editor" alt={1206} align="center" width="80%" border={true} src="https://files.readme.io/6b590c3-in-app_editor.png">
  In-App Editor for Content with Image notifications
</Image>

At a high level, the In-App editor has the following two primary sections: *Content* and *Style*.

### Content

The Content section allows you to define your In-App message's overall text and visual content. Use this section to create engaging, and personalized In-App messages by entering enticing Title and Message. To [personalize](https://docs.clevertap.com/docs/personalize-message-inapp) the message, click the **Personalization (@)**  icon in the *Title* and *Description* fields.

Using the *Insert image* option, you can upload the desired image to make your In-App campaign visually appealing when the app is in Portrait or Landscape mode.

You can choose to add the same image with different form factors or completely different images to give a unique experience on portrait and landscape.

Additionally, you can add up to two CTAs and configure their On Click Action as per your requirement. You can use the following three types of action buttons:

* Close notification: It closes the notification after a tap. 
* Open URL: A special type of CTA that enables the user to open a deep link for Android or iOS.
* Custom key-value pairs: The key-value pairs send back custom data when a user clicks the in-app button

You can also configure the number of days (or hours) to keep the In-App message on the user's device by setting the Message Time to Live field as per your use case. 

> 📘 Image Interstitial Template Exception
>
> The elements of the In-App editor for the *Image only notifications* templates are similar to those of the  *Content with Image notifications* templates except for the *Title* and *Message* fields.

### Style

The Style section enables you to customize the appearance of your In-App message elements, such as title color, background color, message color, button text color, and so on. 

Customize the overall In-App message elements as per your brand style guidelines to make them visually appealing.

<Image title="Define Elements Style" alt={963} align="center" border={true} src="https://files.readme.io/c9edbb1-In-App_Message.png">
  Style Elements from Editor
</Image>

> 🚧 Typeform and Character Limit
>
> We do not currently support Typeform because its rendering requires access to local storage which is a security risk. CleverTap SDK WebView does not allow access to local storage.
>
> The character limit for a message in English is 30 for the title and 128 for the message.\
> The character limit for a message in Chinese is 9 for the title and 38 for the message.
