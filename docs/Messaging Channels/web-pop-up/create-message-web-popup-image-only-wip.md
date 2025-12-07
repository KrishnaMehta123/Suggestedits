---
title: Create Message (Web popup image only WIP)
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
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bc28545-Web_Popup.png",
        "Web Popup.png",
        2858,
        1284,
        "#ececf2"
      ],
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
        1100,
        1080,
        "#fbfafb"
      ],
      "border": true,
      "sizing": "80"
    }
  ]
}
[/block]
Define all the sections and publish the campaign.

## Start Campaign Setup

The *Start here* section displays the setup information. 

**Set a goal:** You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. This selection is optional.

The campaign goal can be as generic or as specific as you want. It can answer questions from *How many users were influenced for purchasing an X amount?* to *How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount?*". 

Define the conversion period by selecting the Conversion Time. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, see [Events](doc:events).
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4fbbeb2-Push_notification_set_goal_track_conversion.png",
        "Push_notification_set_goal_track_conversion.png",
        919,
        361,
        "#fafafc"
      ],
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
        "https://files.readme.io/a92d833-campaign_Who_Live_segment.png",
        "campaign_Who_Live_segment.png",
        964,
        439,
        "#f6f6fc"
      ],
      "border": true
    }
  ]
}
[/block]
Campaigns can be configured based on the following types of user interactions:

* Single action: User performs an action on one of your web pages.
* Page visit: User visits a particular web page on your website.
* Page referral: User visits your website via any specific referral URL.
* Page count: Number of your web pages a user has visited so far in their session.


### Deliver Action Based Web Popup Notifications
You can trigger a web popup message based on an action. For example, a web popup with a promo code can be shown to a set of customers who have just completed a purchase. This will help in incentivizing an existing user. Moreover, such popups make notifications more contextual and result in increased conversion.

### Filter Users Based on Past Behavior

You can also target users basis their past behavior. For example, you might want to target customers who have purchased a specific product in the past. 

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can send a web popup notification to female users who live in the United States. The image below represents a sample target segment that is filtered using specific user properties to target the required audience.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9289ee7-Screenshot_2021-10-26_at_2.53.00_PM.png",
        "Screenshot 2021-10-26 at 2.53.00 PM.png",
        2202,
        822,
        "#decfad"
      ],
      "border": true
    }
  ]
}
[/block]
The following table explains the various property types:
[block:parameters]
{
  "data": {
    "h-2": "Example",
    "h-0": "Property Type",
    "h-1": "Description",
    "0-0": "User Properties",
    "1-0": "Demographics",
    "2-0": "Geography",
    "3-0": "Reachability",
    "3-1": "Reachability filters include *Has email address*, *Has phone number*, *Unsubscribed email*, and *Unsubscribed SMS*.",
    "2-1": "User's coarse location. Filters include *Country*, *Region*, and *City*. CleverTap's SDK can automatically detect this from the user's IP address.",
    "1-1": "Demographics filters include *Age* and *Gender*.",
    "0-1": "Custom [user profile properties](https://docs.clevertap.com/docs/user-profiles#section-user-profile-data-model) that you define and send to CleverTap.",
    "1-2": "Age = 25 to 40 years\nGender = Female",
    "2-2": "Country = United States\nState = California\nCity = San Francisco",
    "0-2": "Customer Type = Platinum",
    "3-2": "Unsubscribed email = No",
    "4-0": "App Fields",
    "4-1": "App fields filters include *App Version*, *Device Make*, *Device Model*, *OS Version*, and CleverTap *SDK Version*. This information is sent by CleverTap's SDK for each device that has your app which means a single user can have multiple devices associated with their user profile.",
    "4-2": "OS Version = 10"
  },
  "cols": 3,
  "rows": 5
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
        2338,
        616,
        "#fcfcfd"
      ],
      "border": true
    }
  ]
}
[/block]

## Web Pop-up Message Types 
You can create the following types of messages for your web exit intent pop-ups:

* Single Message
* AB Test
* Split Delivery
* By User Property

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
        2326,
        616,
        "#f9fafa"
      ],
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
        2344,
        922,
        "#f8f0f1"
      ],
      "border": true
    }
  ]
}
[/block]
### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, you can use the *+ Variant* button to add multiple variants based on a user property value. In the example below, we have used the *Language* user property so users with different language preferences will receive corresponding copies of the campaign in their preferred language.
[block:image]
{
  "images": [
    {
      "image": [],
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
        "https://files.readme.io/3d9b2da-hindi_sale.png",
        "hindi sale.png",
        2320,
        980,
        "#faf5ee"
      ]
    }
  ]
}
[/block]

## Define the Web Pop-up Message Content

After you select a particular message type, you need to choose a template. CleverTap supports three types of templates for Web popup creation - *Basic*, *Ratings*, and *Custom HTML.*
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bfdf7b0-all_templates.png",
        "all templates.png",
        1726,
        738,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]

* **Basic Templates**

    At a high level, one can choose from three styles of popup layouts available under Basic Templates:

    * **Box** - It's a small popup that can be placed at the desired corners of the browser window.
    * **Banner**- It's a wide horizontal popup that can either be placed at the browser window's top or bottom.
    * **Interstitial** - It's a center-aligned popup used to drive better engagements
    * **Image only** - As the name suggests, this template can be used to render an Image as a popup on your website. The Image can have all the content like title, description and CTA as part of it.

* **Ratings Template**

  Marketers can now create feedback-related popups (Interstitials only) for their website users using the *Ratings Template*. 

    Marketers can now create two types of rating templates for gaining feedback from their customers:
    * User Rating Popup
    * NPS Popup

    The images below represent a sample user rating popup and an NPS popup.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8ea6741-feedback1.png",
        "feedback1.png",
        1200,
        614,
        "#faf9f9"
      ],
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
        1276,
        966,
        "#f7f6f8"
      ],
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
        1710,
        1424,
        "#f6f4fa"
      ],
      "border": true
    }
  ]
}
[/block]
Besides, additional styling such as the background color of the notification, text color, button color, and the color of the rating scale is also possible from the editor as shown in the image above. Refer to the [Analysing User Rating] (https://docs.clevertap.com/docs/user-ratings) document to learn more about tracking and monitoring user rating data.

The web popup notification text fields shown below can be personalized for every user based on specific user property or event property values. For more information, refer to [User Profiles](https://docs.clevertap.com/docs/user-profiles).

Enter all the required information. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0c72705-web_pop_up_editor.png",
        "web pop up editor.png",
        2862,
        1552,
        "#f3eef6"
      ],
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "warning",
  "title": "Browser Considerations",
  "body": "Some of the optional items only apply to a certain browser, such as Firefox, Chrome, or KaiOS."
}
[/block]
* **Custom HTML Templates**

    Users have a choice to customize their popup's appearance for the Box, Banner, and Interstitial templates. One simply needs to insert the custom HTML scripts for the respective template layout in the HTML editor.

[block:callout]
{
  "type": "warning",
  "title": "Manually Configured Click Tracking?",
  "body": "If you are already raising the Notification Clicked event manually in your template, then ensure to disable the  *Enable click tracking for Custom HTML* checkbox to avoid overcounting."
}
[/block]
To track the campaign stats such as the number of total clicks and CTRs, marketers need to ensure that they check mark the *Enable click tracking for Custom HTML* checkbox.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/76d8b12-custom_html_click_tracking_web_popup.png",
        "custom html click tracking web popup.png",
        1510,
        856,
        "#efe9f6"
      ],
      "border": true
    }
  ]
}
[/block]

### Preview

Once you are all done setting up the content of your Web Popup campaign in the *What* section, you have the option to preview how your popup would look like to your end-users. 

Click **Preview** button from the message editor to get a preview of your created web popup.

## Define the Campaign Schedule

Each web popup campaign needs to be scheduled to run actively for a specific timeline. To define the schedule for your popup campaign, you need to specify the *Start date and time* and *End date and time*. You also have the option to start a campaign immediately by selecting *Now*.  Besides, you can also define a delay (by seconds, minutes, hours, or days) once a user qualifies for the target segment. Once you define the schedule and click on *Done*, the campaign will be triggered and terminated as per the defined timings.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/429532e-when.png",
        "when.png",
        1904,
        868,
        "#fbfaf9"
      ],
      "border": true
    }
  ]
}
[/block]
### Delivery preferences

In certain scenarios, you might not want a campaign to run actively on a particular day and time. In such cases, you can set the frequency for that particular campaign.

Finally, you can specify how often users receive the campaign: Bypass global campaign limits by selecting the *Exclude from campaign limits* option from the dropdown or choose the appropriate cadence on how often to send your campaign.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/dcab498-DP.png",
        "DP.png",
        1298,
        768,
        "#f9fafc"
      ],
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "Global Session Limits",
  "body": "In the global campaign limits, when you want to show 'x' web popups per session, it actually applies to 'x' distinct web popup campaigns, not the same web popup campaign.\n\nAs per CleverTap's web SDK, for a given web popup campaign, it will only be shown once per session."
}
[/block]

## Publish Campaign

After previewing the appearance of your campaign, finalize your campaign by clicking **Publish Campaign.**


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b521e92-campaign_Publish.png",
        "campaign_Publish.png",
        1193,
        356,
        "#f0f0fc"
      ],
      "border": true
    }
  ]
}
[/block]
# Assigning Priorities for Web Pop-up Campaigns

After publishing the campaign, marketers can assign the priorities to specific campaigns to avoid random delivery of popups. This means, If multiple web popups are scheduled to go live for the same web page at the same time, the priority order defines the order in which the popups are to be shown. 

To assign the priority:

1. Navigate to the *Campaigns* dashboard and select the specific campaign from the campaign list.
2. Click the *Web priority* marker icon below each campaign to open the priority list.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1d8fb30-wp2.png",
        "wp2.png",
        1848,
        706,
        "#f8f8fa"
      ],
      "border": true,
      "sizing": "original"
    }
  ]
}
[/block]
3. Set the *Priority* as per your choice and click **Save**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/02664d2-WP2.png",
        "WP2.png",
        1780,
        718,
        "#afb0b3"
      ],
      "border": true,
      "sizing": "80"
    }
  ]
}
[/block]