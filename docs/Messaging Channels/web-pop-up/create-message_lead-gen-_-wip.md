---
title: Create Message_Lead Gen _ WIP
excerpt: Learn how to create a Web Popup campaign using the CleverTap dashboard
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Create a New Web Pop-up Campaign

Create a campaign to deliver your Web Popup message. Follow the steps below to create a new web popup campaign:

1. From the dashboard, navigate to *Campaigns*. 
2. Click **+ Campaign** button.
3. From the *Messaging Channels* list, select *Web Popup.* 

<Image title="Web Popup.png" alt={2858} align="center" className="border" border={true} src="https://files.readme.io/bc28545-Web_Popup.png" />

The campaign page displays.

<Image title="Web_pop_up_Editor_main.png" alt={1100} align="center" className="border" width="80%" border={true} src="https://files.readme.io/4bf6219-Web_pop_up_Editor_main.png" />

Define all the sections and publish the campaign.

## Start Campaign Setup

The *Start here* section displays the setup information. 

**Set a goal:** You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. This selection is optional.

The campaign goal can be as generic or as specific as you want. It can answer questions from *How many users were influenced for purchasing an X amount?* to *How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount?*". 

Define the conversion period by selecting the Conversion Time. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, see [Events](doc:events).

<Image title="Push_notification_set_goal_track_conversion.png" alt={919} align="center" className="border" border={true} src="https://files.readme.io/4fbbeb2-Push_notification_set_goal_track_conversion.png" />

## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the Target segment section. Here, you can create a new segment or use a previously saved user segment from the segment list.

<Image title="Web Popup Segment .png" alt={2448} align="center" className="border" border={true} src="https://files.readme.io/6e9cb3a-Web_Popup_Segment_.png" />

Campaigns can be configured based on the following types of user interactions:

* *Single Action*: Target users based on their actions on one of your web pages.
* *Page Visit*: Target users visiting specific web pages. For example, a page such as *[https://ctcart.com/black\_friday\_sale](https://ctcart.com/black_friday_sale)*, where you can create a campaign to target users that visit the Black Friday sale on your website. You can add multiple pages. 
* *Page Referral*: Target users visiting your website via any referral web page. For example, users who have visited your website through a Black Friday sale advertisement on google, such as\
  *[https://ctcart.com/redirect?utm\_medium=google\&utm\_campaign=black\_friday\_sale](https://ctcart.com/redirect?utm_medium=google\&utm_campaign=black_friday_sale)*. 
* *Page Count*: Target users based on the specified number of web pages visited in a single session. 

### Deliver Action Based Web Popup Notifications

You can trigger a web popup message based on an action. For example, a web popup with a promo code can be shown to customers who have just completed a purchase. This will help incentivize an existing user. Moreover, such popups make notifications more contextual and result in increased conversion.

### Filter Users Based on Past Behavior

You can also target users basis their past behavior. For example, you might want to target customers who have purchased a specific product in the past. 

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can send a web popup notification to female users who live in the United States. The image below represents a sample target segment that is filtered using specific user properties to target the required audience.

<Image title="Screenshot 2021-10-26 at 2.53.00 PM.png" alt={2202} align="center" className="border" border={true} src="https://files.readme.io/9289ee7-Screenshot_2021-10-26_at_2.53.00_PM.png" />

The following table explains the various property types:

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Property Type
      </th>

      <th>
        Description
      </th>

      <th>
        Example
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        User Properties
      </td>

      <td>
        Custom [user profile properties](https://docs.clevertap.com/docs/user-profiles#section-user-profile-data-model) that you define and send to CleverTap.
      </td>

      <td>
        Customer Type = Platinum
      </td>
    </tr>

    <tr>
      <td>
        Demographics
      </td>

      <td>
        Demographics filters include *Age* and *Gender*.
      </td>

      <td>
        Age = 25 to 40 years\
        Gender = Female
      </td>
    </tr>

    <tr>
      <td>
        Geography
      </td>

      <td>
        User's coarse location. Filters include *Country*, *Region*, and *City*. CleverTap's SDK can automatically detect this from the user's IP address.
      </td>

      <td>
        Country = United States\
        State = California\
        City = San Francisco
      </td>
    </tr>

    <tr>
      <td>
        Reachability
      </td>

      <td>
        Reachability filters include *Has email address*, *Has phone number*, *Unsubscribed email*, and *Unsubscribed SMS*.
      </td>

      <td>
        Unsubscribed email = No
      </td>
    </tr>

    <tr>
      <td>
        App Fields
      </td>

      <td>
        App fields filters include *App Version*, *Device Make*, *Device Model*, *OS Version*, and CleverTap *SDK Version*. This information is sent by CleverTap's SDK for each device that has your app which means a single user can have multiple devices associated with their user profile.
      </td>

      <td>
        OS Version = 10
      </td>
    </tr>
  </tbody>
</Table>

To know more about what segments can be used, see [Segments](doc:segments).

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information on control groups, see [Control Groups](doc:control-groups)

<Image title="Screenshot 2021-10-22 at 1.25.05 PM.png" alt={2338} align="center" className="border" border={true} src="https://files.readme.io/ca9ad92-Screenshot_2021-10-22_at_1.25.05_PM.png" />

## Web Pop-up Message Types

You can create the following types of messages for your web exit intent pop-ups:

* Single Message
* AB Test
* Split Delivery
* By User Property

### Single Message

In this campaign, a standard message is sent to all users who qualify as your target audience. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between properties such as language, geography, or any other user properties.

### A/B Testing

A/B testing helps you understand what type of message copy works best in the pop-up to get clicks from users.\
You can test up to three pop-up message variants on a test group. The variant that gets the most clicks is declared the winning variant and is automatically sent to the rest of your target audience.

<Image title="Web popup A:B test.png" alt={2326} align="center" className="border" border={true} src="https://files.readme.io/561e7ef-Web_popup_AB_test.png" />

### Split Delivery

With split delivery, you can decide what percentage of your audience receives each pop-up variant for the duration of the campaign.

<Image title="pop-up slit delivery.png" alt={2344} align="center" className="border" border={true} src="https://files.readme.io/b3026b1-pop-up_slit_delivery.png" />

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, you can use the *+ Variant* button to add multiple variants based on a user property value. In the example below, we have used the *Language* user property so users with different language preferences will receive corresponding copies of the campaign in their preferred language.

<Image align="center" className="border" border={true} src="https://files.readme.io/e88802a-Lead_Gen_Template_Tab.png" />

## Define the Web Pop-up Message Content

After you select a particular message type, you need to choose a template. CleverTap supports four types of templates for Web popup creation - *Basic*, *Ratings*, *Lead Generation*, and *Custom HTML.*

<Image title="Web Popup Templates.png" alt={1874} align="center" className="border" border={true} src="https://files.readme.io/2be9ae6-Web_Popup_Templates.png" />

### Basic Templates

At a high level, one can choose from three styles of popup layouts available under Basic Templates:

* Box - It's a small popup that can be placed at the desired corners of the browser window.
* Banner- It's a wide horizontal popup that can be either placed at the top or bottom of the browser window.
* Interstitial - It's a center-aligned popup particularly used for driving better engagements.

### Ratings Template

 Marketers can now create feedback-related popups (Interstitials only) for their website users using the *Ratings Template*. 

Marketers can now create two types of rating templates for gaining feedback from their customers:

* User Rating Popup
* NPS Popup

The images below represent a sample user rating popup and NPS popup.

<Image title="feedback1.png" alt={1200} align="center" className="border" border={true} src="https://files.readme.io/8ea6741-feedback1.png" />

<Image title="NPS feedback.png" alt={1276} align="center" className="border" border={true} src="https://files.readme.io/76e9149-NPS_feedback.png" />

Marketers get the complete flexibility to explicitly define the rating scale, style,  its shape (Star, Heart, Emojis), labels, and the overall content of the popup. One can also choose to add a comment box to get accurate user feedback/comments. 

<Image title="styling.png" alt={1710} align="center" className="border" border={true} src="https://files.readme.io/7bbc6cc-styling.png" />

Additional styling, such as the background color of the notification, text color, button color, and the color of the rating scale, is also possible from the editor, as shown in the image above. To learn more about tracking and monitoring user rating data, refer to [Analysing User Rating](https://docs.clevertap.com/docs/user-ratings).

The web popup notification text fields shown below can be personalized for every user based on specific user property or event property values. For more information, refer to [User Profiles](https://docs.clevertap.com/docs/user-profiles).

Enter all the required information. 

<Image title="web pop up editor.png" alt={2862} align="center" className="border" border={true} src="https://files.readme.io/0c72705-web_pop_up_editor.png" />

### Lead Generation Templates

We know that a significant number of website visitors remain anonymous. This poses a challenge to continue engaging with potential customers after they leave a website. A lead generation template can solve this issue. 

By integrating a lead generation form on your website, you can get important customer details such as name, email address, phone number, and so on. This information is helpful for further communication through channels such as SMS, Email, WhatsApp, and others. This post-visit communication not only helps to stay connected with your audience but also opens doors for future business opportunities. You can turn anonymous visitors into loyal customers with the CleverTap Lead Generation template.

<Image title="Lead Gen Template Sample.png" alt={1368} align="center" className="border" border={true} src="https://files.readme.io/888a43a-Lead_Gen_Template_Sample.png" />

#### Post Submit Actions

When a user submits information on your Lead Generation template:

* A *Notification Clicked* event is raised that records the click on the CTA. 

* A custom event named *Lead Submitted* records the details submitted by the user as of event properties. Following is a sample form image:

<Image align="center" width="50% " src="https://files.readme.io/0cae15f-Lead_Gen_Template_preview_with_fields.png" />

Following is a table that records the relevant properties for the fields displayed on the form:

| Submitted Event Properties | Sample Property Value               |
| :------------------------- | :---------------------------------- |
| First Name                 | John                                |
| Last Name                  | Smith                               |
| Email ID                   | [john@abc.com](mailto:john@abc.com) |
| Phone Number               | +11234567890                        |
| Campaign ID                | 121110987654                        |
| Variant                    | wzrk\_default                       |

* The user profile is automatically updated with the submitted event properties. For example, the lead generation template can ask for additional details from an anonymous user, such as first name, last name, email, and phone number. His profile will be updated with these details, and now you can identify the user as *John Smith*. 

#### Lead Generation Template Variants

The Lead Generation template has the following three variants:

* Text 
* Image on Side
* Image on Top

<Image align="center" className="border" border={true} src="https://files.readme.io/dd75b54-Lead_Gen_Template_Tab.png" />

Select any of the variants to create your Lead Generation template. 

#### Lead Generation Content

Create the content to record information from your users. The following image displays a preview of the form:

<Image title="Lead Gen Template Editor Content.png" alt={2364} align="center" className="border" border={true} src="https://files.readme.io/2daa708-Lead_Gen_Template_Editor_Content.png" />

Enter all the required information. 

* *Text*: Personalize the Title and Description. 
* *Media*: Add the image URL or upload an image. 
* *Input Fields*: You can add up to four input fields. Select input fields such as Name, Phone Number, Birthday, or Email Address for the template. 

<Image title="Lead Gen Template Input Fields.png" alt={1304} align="center" className="border" border={true} src="https://files.readme.io/6a87857-Lead_Gen_Template_Input_Fields.png" />

* *Buttons*: The *Close* button is selected by default. Add a button name such as *Submit* or *Upload*. 
* *Subtext*: Add subtext such as *privacy policy* to your lead generation template.

![](https://files.readme.io/bb6e1f2-Lead_Gen_Template_SubText_preview.png "Lead Gen Template SubText preview.png")

The hyperlinked part must be closed between two asterisks. Add the URL where the user will be directed. You can also add a checkbox for your subtext.

![](https://files.readme.io/d740b86-Lead_Gen_Template_SubText.png "Lead Gen Template SubText.png")

* *Acknowledgement*: You can show appreciation to your user by adding an Acknowledgement popup. Select the auto-close timer for the popup. 

#### Lead Generation Template Style

You can select the layout and card position from this screen. You can also select the color of the text, input fields, and buttons. 

> 📘 Mobile View
>
> The Mobile view can display images only at the *Top*, *Bottom* or in the *Center*.

<Image title="Lead Gen Template Editor Style.png" alt={2378} align="center" className="border" border={true} src="https://files.readme.io/ae9c7d6-Lead_Gen_Template_Editor_Style.png" />

### Custom HTML Templates

Users have a choice to customize their popup's appearance for the Box, Banner, and Interstitial templates. One simply needs to insert the custom HTML scripts for the respective template layout in the HTML editor.

> 🚧 Configuring Click Tracking Manually
>
> If you are already raising the Notification Clicked event manually in your template, then ensure to disable the  *Enable click tracking for Custom HTML* checkbox to avoid overcounting.

To track the campaign stats such as the number of total clicks and CTRs, marketers need to ensure that they check mark the *Enable click tracking for Custom HTML* checkbox.

<Image title="custom html click tracking web popup.png" alt={1510} align="center" className="border" border={true} src="https://files.readme.io/76d8b12-custom_html_click_tracking_web_popup.png" />

### Preview

Once you are all done setting up the content of your Web Popup campaign in the *What* section, you have the option to preview how your popup would look to your end-users. 

Click the **Preview** button from the message editor to get a preview of your created web popup.

## Define the Campaign Schedule

Each web popup campaign needs to be scheduled to run actively for a specific timeline. To define the schedule for your popup campaign, you need to specify the *Start date and time* and *End date and time*. You also have the option to start a campaign immediately by selecting *Now*.  Besides you can also define a delay (by seconds, minutes, hours, or days) once a user qualifies for the target segment. Once you define the schedule and click on *Done*, the campaign will be triggered and terminated as per the defined timings.

<Image title="when.png" alt={1904} align="center" className="border" border={true} src="https://files.readme.io/429532e-when.png" />

### Delivery preferences

In certain scenarios, you might not want a campaign to run actively on a particular day and time. In such cases, you can set the frequency for that particular campaign.

Finally, you can specify how often users receive the campaign: Bypass global campaign limits by selecting the *Exclude from campaign limits* option from the dropdown or choose the appropriate cadence on how often to send your campaign.

<Image title="DP.png" alt={1298} align="center" className="border" border={true} src="https://files.readme.io/dcab498-DP.png" />

> 📘 Global Session Limits
>
> In the global campaign limits, when you want to show 'x' web popups per session, it actually applies to 'x' distinct web popup campaigns, not the same web popup campaign.
>
> As per CleverTap's web SDK, for a given web popup campaign, it will only be shown once per session.

## Publish Campaign

After previewing the appearance of your campaign, finalize your campaign by clicking **Publish Campaign.**

<Image title="campaign_Publish.png" alt={1193} align="center" className="border" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png" />

# Assigning Priorities for Web Pop-up Campaigns

After publishing the campaign, marketers can assign the priorities to specific campaigns to avoid random delivery of popups. This means, If multiple web popups are scheduled to go live for the same web page at the same time, the priority order defines the order in which the popups are to be shown. 

To assign the priority:

1. Navigate to the *Campaigns* dashboard and select the specific campaign from the campaign list.
2. Click the *Web priority* marker icon below each campaign to open the priority list.

<Image title="wp2.png" alt={1848} align="center" className="border" width="auto" border={true} src="https://files.readme.io/1d8fb30-wp2.png" />

3. Set the *Priority* as per your choice and click **Save**.

<Image title="WP2.png" alt={1780} align="center" className="border" width="80%" border={true} src="https://files.readme.io/02664d2-WP2.png" />

# FAQs and Troubleshooting

Q. What if a user property is not available ?

You can add user properties to your user profile. You can send a test profile to CleverTap with the required properties.
