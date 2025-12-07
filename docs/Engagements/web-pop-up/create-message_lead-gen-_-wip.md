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

1. From the dashboard, navigate to _Campaigns_. 
2. Click **+ Campaign** button.
3. From the _Messaging Channels_ list, select _Web Popup._ 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bc28545-Web_Popup.png",
        "Web Popup.png",
        2858
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



The campaign page displays.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4bf6219-Web_pop_up_Editor_main.png",
        "Web_pop_up_Editor_main.png",
        1100
      ],
      "align": "center",
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]



Define all the sections and publish the campaign.

## Start Campaign Setup

The _Start here_ section displays the setup information. 

**Set a goal:** You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. This selection is optional.

The campaign goal can be as generic or as specific as you want. It can answer questions from _How many users were influenced for purchasing an X amount?_ to _How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount?_". 

Define the conversion period by selecting the Conversion Time. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, see [Events](doc:events).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4fbbeb2-Push_notification_set_goal_track_conversion.png",
        "Push_notification_set_goal_track_conversion.png",
        919
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the Target segment section. Here, you can create a new segment or use a previously saved user segment from the segment list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6e9cb3a-Web_Popup_Segment_.png",
        "Web Popup Segment .png",
        2448
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



Campaigns can be configured based on the following types of user interactions:

- _Single Action_: Target users based on their actions on one of your web pages.
- _Page Visit_: Target users visiting specific web pages. For example, a page such as _<https://ctcart.com/black_friday_sale>_, where you can create a campaign to target users that visit the Black Friday sale on your website. You can add multiple pages. 
- _Page Referral_: Target users visiting your website via any referral web page. For example, users who have visited your website through a Black Friday sale advertisement on google, such as  
  _<https://ctcart.com/redirect?utm_medium=google&utm_campaign=black_friday_sale>_. 
- _Page Count_: Target users based on the specified number of web pages visited in a single session. 

### Deliver Action Based Web Popup Notifications

You can trigger a web popup message based on an action. For example, a web popup with a promo code can be shown to customers who have just completed a purchase. This will help incentivize an existing user. Moreover, such popups make notifications more contextual and result in increased conversion.

### Filter Users Based on Past Behavior

You can also target users basis their past behavior. For example, you might want to target customers who have purchased a specific product in the past. 

### Filter by User Properties

Using the _With user properties_ filter in the _Who_ section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can send a web popup notification to female users who live in the United States. The image below represents a sample target segment that is filtered using specific user properties to target the required audience.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9289ee7-Screenshot_2021-10-26_at_2.53.00_PM.png",
        "Screenshot 2021-10-26 at 2.53.00 PM.png",
        2202
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



The following table explains the various property types:

[block:parameters]
{
  "data": {
    "h-0": "Property Type",
    "h-1": "Description",
    "h-2": "Example",
    "0-0": "User Properties",
    "0-1": "Custom [user profile properties](https://docs.clevertap.com/docs/user-profiles#section-user-profile-data-model) that you define and send to CleverTap.",
    "0-2": "Customer Type = Platinum",
    "1-0": "Demographics",
    "1-1": "Demographics filters include _Age_ and _Gender_.",
    "1-2": "Age = 25 to 40 years  \nGender = Female",
    "2-0": "Geography",
    "2-1": "User's coarse location. Filters include _Country_, _Region_, and _City_. CleverTap's SDK can automatically detect this from the user's IP address.",
    "2-2": "Country = United States  \nState = California  \nCity = San Francisco",
    "3-0": "Reachability",
    "3-1": "Reachability filters include _Has email address_, _Has phone number_, _Unsubscribed email_, and _Unsubscribed SMS_.",
    "3-2": "Unsubscribed email = No",
    "4-0": "App Fields",
    "4-1": "App fields filters include _App Version_, _Device Make_, _Device Model_, _OS Version_, and CleverTap _SDK Version_. This information is sent by CleverTap's SDK for each device that has your app which means a single user can have multiple devices associated with their user profile.",
    "4-2": "OS Version = 10"
  },
  "cols": 3,
  "rows": 5,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]

To know more about what segments can be used, see [Segments](doc:segments).

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information on control groups, see [Control Groups](doc:control-groups)

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ca9ad92-Screenshot_2021-10-22_at_1.25.05_PM.png",
        "Screenshot 2021-10-22 at 1.25.05 PM.png",
        2338
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



## Web Pop-up Message Types

You can create the following types of messages for your web exit intent pop-ups:

- Single Message
- AB Test
- Split Delivery
- By User Property

### Single Message

In this campaign, a standard message is sent to all users who qualify as your target audience. This message type is best for broadcast messages and for applications that do not vary campaign communication based on differences between properties such as language, geography, or any other user properties.

### A/B Testing

A/B testing helps you understand what type of message copy works best in the pop-up to get clicks from users.  
You can test up to three pop-up message variants on a test group. The variant that gets the most clicks is declared the winning variant and is automatically sent to the rest of your target audience.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/561e7ef-Web_popup_AB_test.png",
        "Web popup A:B test.png",
        2326
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



### Split Delivery

With split delivery, you can decide what percentage of your audience receives each pop-up variant for the duration of the campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b3026b1-pop-up_slit_delivery.png",
        "pop-up slit delivery.png",
        2344
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, you can use the _+ Variant_ button to add multiple variants based on a user property value. In the example below, we have used the _Language_ user property so users with different language preferences will receive corresponding copies of the campaign in their preferred language.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e88802a-Lead_Gen_Template_Tab.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



## Define the Web Pop-up Message Content

After you select a particular message type, you need to choose a template. CleverTap supports four types of templates for Web popup creation - _Basic_, _Ratings_, _Lead Generation_, and _Custom HTML._

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2be9ae6-Web_Popup_Templates.png",
        "Web Popup Templates.png",
        1874
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



### Basic Templates

At a high level, one can choose from three styles of popup layouts available under Basic Templates:

- Box - It's a small popup that can be placed at the desired corners of the browser window.
- Banner- It's a wide horizontal popup that can be either placed at the top or bottom of the browser window.
- Interstitial - It's a center-aligned popup particularly used for driving better engagements.

### Ratings Template

 Marketers can now create feedback-related popups (Interstitials only) for their website users using the _Ratings Template_. 

Marketers can now create two types of rating templates for gaining feedback from their customers:

- User Rating Popup
- NPS Popup

The images below represent a sample user rating popup and NPS popup.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8ea6741-feedback1.png",
        "feedback1.png",
        1200
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/76e9149-NPS_feedback.png",
        "NPS feedback.png",
        1276
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



Marketers get the complete flexibility to explicitly define the rating scale, style,  its shape (Star, Heart, Emojis), labels, and the overall content of the popup. One can also choose to add a comment box to get accurate user feedback/comments. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7bbc6cc-styling.png",
        "styling.png",
        1710
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



Additional styling, such as the background color of the notification, text color, button color, and the color of the rating scale, is also possible from the editor, as shown in the image above. To learn more about tracking and monitoring user rating data, refer to [Analysing User Rating](https://docs.clevertap.com/docs/user-ratings).

The web popup notification text fields shown below can be personalized for every user based on specific user property or event property values. For more information, refer to [User Profiles](https://docs.clevertap.com/docs/user-profiles).

Enter all the required information. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0c72705-web_pop_up_editor.png",
        "web pop up editor.png",
        2862
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



### Lead Generation Templates

We know that a significant number of website visitors remain anonymous. This poses a challenge to continue engaging with potential customers after they leave a website. A lead generation template can solve this issue. 

By integrating a lead generation form on your website, you can get important customer details such as name, email address, phone number, and so on. This information is helpful for further communication through channels such as SMS, Email, WhatsApp, and others. This post-visit communication not only helps to stay connected with your audience but also opens doors for future business opportunities. You can turn anonymous visitors into loyal customers with the CleverTap Lead Generation template.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/888a43a-Lead_Gen_Template_Sample.png",
        "Lead Gen Template Sample.png",
        1368
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



#### Post Submit Actions

When a user submits information on your Lead Generation template:

- A _Notification Clicked_ event is raised that records the click on the CTA. 

- A custom event named _Lead Submitted_ records the details submitted by the user as of event properties. Following is a sample form image:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0cae15f-Lead_Gen_Template_preview_with_fields.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "50% "
    }
  ]
}
[/block]



Following is a table that records the relevant properties for the fields displayed on the form:

| Submitted Event Properties | Sample Property Value |
| :------------------------- | :-------------------- |
| First Name                 | John                  |
| Last Name                  | Smith                 |
| Email ID                   | john@abc.com          |
| Phone Number               | +11234567890          |
| Campaign ID                | 121110987654          |
| Variant                    | wzrk_default          |

- The user profile is automatically updated with the submitted event properties. For example, the lead generation template can ask for additional details from an anonymous user, such as first name, last name, email, and phone number. His profile will be updated with these details, and now you can identify the user as _John Smith_. 

#### Lead Generation Template Variants

The Lead Generation template has the following three variants:

- Text 
- Image on Side
- Image on Top

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dd75b54-Lead_Gen_Template_Tab.png",
        null,
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



Select any of the variants to create your Lead Generation template. 

#### Lead Generation Content

Create the content to record information from your users. The following image displays a preview of the form:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2daa708-Lead_Gen_Template_Editor_Content.png",
        "Lead Gen Template Editor Content.png",
        2364
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



Enter all the required information. 

- _Text_: Personalize the Title and Description. 
- _Media_: Add the image URL or upload an image. 
- _Input Fields_: You can add up to four input fields. Select input fields such as Name, Phone Number, Birthday, or Email Address for the template. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6a87857-Lead_Gen_Template_Input_Fields.png",
        "Lead Gen Template Input Fields.png",
        1304
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



- _Buttons_: The _Close_ button is selected by default. Add a button name such as _Submit_ or _Upload_. 
- _Subtext_: Add subtext such as _privacy policy_ to your lead generation template.

![](https://files.readme.io/bb6e1f2-Lead_Gen_Template_SubText_preview.png "Lead Gen Template SubText preview.png")

The hyperlinked part must be closed between two asterisks. Add the URL where the user will be directed. You can also add a checkbox for your subtext.

![](https://files.readme.io/d740b86-Lead_Gen_Template_SubText.png "Lead Gen Template SubText.png")

- _Acknowledgement_: You can show appreciation to your user by adding an Acknowledgement popup. Select the auto-close timer for the popup. 

#### Lead Generation Template Style

You can select the layout and card position from this screen. You can also select the color of the text, input fields, and buttons. 

> 📘 Mobile View
> 
> The Mobile view can display images only at the _Top_, _Bottom_ or in the _Center_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ae9c7d6-Lead_Gen_Template_Editor_Style.png",
        "Lead Gen Template Editor Style.png",
        2378
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



### Custom HTML Templates

Users have a choice to customize their popup's appearance for the Box, Banner, and Interstitial templates. One simply needs to insert the custom HTML scripts for the respective template layout in the HTML editor.

> 🚧 Configuring Click Tracking Manually
> 
> If you are already raising the Notification Clicked event manually in your template, then ensure to disable the  _Enable click tracking for Custom HTML_ checkbox to avoid overcounting.

To track the campaign stats such as the number of total clicks and CTRs, marketers need to ensure that they check mark the _Enable click tracking for Custom HTML_ checkbox.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/76d8b12-custom_html_click_tracking_web_popup.png",
        "custom html click tracking web popup.png",
        1510
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



### Preview

Once you are all done setting up the content of your Web Popup campaign in the _What_ section, you have the option to preview how your popup would look to your end-users. 

Click the **Preview** button from the message editor to get a preview of your created web popup.

## Define the Campaign Schedule

Each web popup campaign needs to be scheduled to run actively for a specific timeline. To define the schedule for your popup campaign, you need to specify the _Start date and time_ and _End date and time_. You also have the option to start a campaign immediately by selecting _Now_.  Besides you can also define a delay (by seconds, minutes, hours, or days) once a user qualifies for the target segment. Once you define the schedule and click on _Done_, the campaign will be triggered and terminated as per the defined timings.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/429532e-when.png",
        "when.png",
        1904
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



### Delivery preferences

In certain scenarios, you might not want a campaign to run actively on a particular day and time. In such cases, you can set the frequency for that particular campaign.

Finally, you can specify how often users receive the campaign: Bypass global campaign limits by selecting the _Exclude from campaign limits_ option from the dropdown or choose the appropriate cadence on how often to send your campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dcab498-DP.png",
        "DP.png",
        1298
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



> 📘 Global Session Limits
> 
> In the global campaign limits, when you want to show 'x' web popups per session, it actually applies to 'x' distinct web popup campaigns, not the same web popup campaign.
> 
> As per CleverTap's web SDK, for a given web popup campaign, it will only be shown once per session.

## Publish Campaign

After previewing the appearance of your campaign, finalize your campaign by clicking **Publish Campaign.**

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b521e92-campaign_Publish.png",
        "campaign_Publish.png",
        1193
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



# Assigning Priorities for Web Pop-up Campaigns

After publishing the campaign, marketers can assign the priorities to specific campaigns to avoid random delivery of popups. This means, If multiple web popups are scheduled to go live for the same web page at the same time, the priority order defines the order in which the popups are to be shown. 

To assign the priority:

1. Navigate to the _Campaigns_ dashboard and select the specific campaign from the campaign list.
2. Click the _Web priority_ marker icon below each campaign to open the priority list.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1d8fb30-wp2.png",
        "wp2.png",
        1848
      ],
      "align": "center",
      "sizing": "auto",
      "border": true
    }
  ]
}
[/block]



3. Set the _Priority_ as per your choice and click **Save**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/02664d2-WP2.png",
        "WP2.png",
        1780
      ],
      "align": "center",
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]



# FAQs and Troubleshooting

Q. What if a user property is not available ?

You can add user properties to your user profile. You can send a test profile to CleverTap with the required properties.