---
title: Create Message
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
      title: Personalize Message
      url: https://docs.clevertap.com/docs/personalize-message-web-exit-intent_c20
    - type: link
      title: Define a Custom Callback
      url: https://docs.clevertap.com/docs/setup-web-exit-intent_c20
    - type: link
      title: Web Exit Intent Stats
      url: https://docs.clevertap.com/docs/web-exit-intent-stats_c20
---
[block:api-header]
{
  "title": "Create a New Web Exit Intent Campaign"
}
[/block]
To create a new Web Exit Intent Popup campaign:

1. From the dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **Web Exit Intent**. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/39044fd-webexit.png",
        "webexit.png",
        2846,
        1264,
        "#eaebf1"
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
        "https://files.readme.io/03e2e61-Web_exit_intent_editor_main.png",
        "Web_exit_intent_editor_main.png",
        976,
        1064,
        "#faf9fa"
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

* **Set a goal**: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. This selection is optional.

The campaign goal can be as generic or as specific as you want. It can answer questions from *How many users were influenced for purchasing an X amount?* to *How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount? ". 

Define the conversion period by selecting the *Conversion Time*. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, see [Events](doc:events).
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

You must indicate the target audience for your campaign. You can specify your target audience from the *Target segment* section. Here, you can create a new segment or use a previously saved user segment from the segment list. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bf4a5f0-campaign_Who_Live_segment.png",
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
Campaigns can be set up as follows:

* Single action: User does an action on one of your web pages.
* Page visit: User visits one of your specific webpage URLs.
* Page referral: User visits your website via any specific referral URL.
* Page count: Number of your web pages a user has visited so far in their session.

### Deliver Action Based Web Exit Intent Notifications
You can trigger a web exit intent popup based on an action. For example, a web exit intent popup with an irresistible discount voucher can be shown to a set of customers who have just viewed a specific product page. This will help in incentivizing an existing customer. Moreover, such exit intent popups make notifications more contextual and result in increased conversion.

### Deliver Messages based on Past Behavior (PBS)

You can also target users basis their past behavior. For example, you can show a web exit intent popup to customers who had recently added products to the cart but didn't complete the purchase.

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can send a web exit Intent popup to customers from **Mumbai** who have added items to the cart but didn't complete the transaction in the past 10 days.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0141dfe-up.png",
        "up.png",
        2242,
        1122,
        "#ece5d7"
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
    "3-0": "Geography Radius",
    "4-0": "Reachability",
    "5-0": "App Fields",
    "5-1": "App fields filters include *App Version*, *Device Make*, *Device Model*, *OS Version*, and CleverTap *SDK Version*. This information is sent by CleverTap's SDK for each device that has your app which means a single user can have multiple devices associated with their user profile.",
    "4-1": "Reachability filters include *Has email address*, *Has phone number*, *Unsubscribed email*, and *Unsubscribed SMS*.",
    "3-1": "User's exact location. You can select a city, and then define the target radius. You can also select multiple cities. You can send this information using CleverTap's SDK. For more information, refer to the [iOS](https://developer.clevertap.com/docs/ios#section-send-location-information-to-clevertap) and [Android](https://developer.clevertap.com/docs/android#section-manually-updating-user-location) developer guides.",
    "2-1": "User's coarse location. Filters include *Country*, *Region*, and *City*. CleverTap's SDK can automatically detect this from the user's IP address.",
    "1-1": "Demographics filters include *Age* and *Gender*.",
    "0-1": "Custom [user profile properties](https://docs.clevertap.com/docs/user-profiles#section-user-profile-data-model) that you define and send to CleverTap.",
    "1-2": "Age = 25 to 40 years\nGender = Female",
    "2-2": "Country = United States\nState = California\nCity = San Francisco",
    "0-2": "Customer Type = Platinum",
    "3-2": "Locations = San Francisco, USA; Paris, France",
    "5-2": "OS Version = 10",
    "4-2": "Unsubscribed email = No"
  },
  "cols": 3,
  "rows": 6
}
[/block]

To know more about what segments can be used, see [Segments](doc:segments).

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information on control groups, see [Control Groups](doc:control-groups).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fd0d08b-cg.png",
        "cg.png",
        1480,
        516,
        "#fafbfd"
      ],
      "border": true
    }
  ]
}
[/block]
## Define the Message Content

Now, you need to set up the *What* section to define the content for the Web Exit Popup campaign.


Click **Go to Editor**. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8a73e71-Webhook_what_without_options.png",
        "Webhook_what_without_options.png",
        1048,
        188,
        "#f8f3f5"
      ],
      "border": true
    }
  ]
}
[/block]
The *Create Web Exit Intent Message* window displays.

## Message Editor
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f98671a-web_exit.png",
        "web exit.png",
        2564,
        1510,
        "#f3eff6"
      ],
      "border": true
    }
  ]
}
[/block]
For web exit intent pop-ups, you can specify a button with text. Upon a web pop-up click, you can either do nothing, open a link, or invoke a JavaScript function.

## Define the Campaign Schedule

Each web exit intent campaign needs to be scheduled to run actively for a specific timeline. To define the schedule for your popup campaign, you need to specify the *Start date and time* and *End date and time*. You can also define a delay (by seconds, minutes, hours, or days) once a user qualifies for the target segment. Once you define the schedule and click on *Done*, the campaign will be triggered and terminated as per the defined timings.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0b43104-when.png",
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
        "https://files.readme.io/bf4c04a-DP.png",
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
## Publish Campaign

* After previewing the appearance of your campaign, finalize your campaign by clicking **Publish Campaign.**
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

# Assigning Priorities for Web Exit Intent Campaigns

After publishing the campaign, marketers can assign the priorities to specific campaigns to avoid random delivery of exit-intent popups. This means, If multiple web popups are scheduled to go live for the same web page at the same time, the priority order defines which popup will be shown. To assign the priority, navigate to the Campaigns dashboard and select the specific campaign from the campaign list.

Below each campaign, there's a *Web priority * marker. Click the marker icon to open the priority list.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0805d48-wp.png",
        "wp.png",
        1788,
        694,
        "#f6f7fa"
      ],
      "border": true,
      "sizing": "original"
    }
  ]
}
[/block]
Set the priority as per your choice and click **Save** 
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
      "sizing": "smart"
    }
  ]
}
[/block]