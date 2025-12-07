---
title: Create Message
excerpt: Understand how to create a campaign for Facebook Audiences
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: >-
    Refer to the pages listed below to learn more about the following Facebook
    Audiences section:
  pages:
    - type: link
      title: Facebook Audiences Campaign Stats
      url: https://docs.clevertap.com/docs/facebook-audience-stats_c20
---
[block:api-header]
{
  "title": "Create a New Campaign"
}
[/block]
Create a campaign to deliver your Facebook Audience message. 
To create a new campaign:

1. From the CleverTap dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **Audience**. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/930c308-Select_FB_Audiences.png",
        "Select FB Audiences.png",
        2858,
        2682,
        "#f1f2f6"
      ],
      "border": true
    }
  ]
}
[/block]
The *Campaigns* page displays.

4. Select the Adset from the list.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e3905ab-New_FB_Audience_page.png",
        "New FB Audience page.png",
        2748,
        1426,
        "#fbfbfb"
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

This section has the following parts:
* Start here: Displays the information for platforms such as FCM, Xiaomi, or iOS. Check that the required platforms are integrated and ready for campaigns. When the account set up is not done, the following warning message is displayed and you need to set up the account to be able to run campaigns:
 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0f891c5-Account_Setup_not_done_.png",
        "Account Setup not done .png",
        2698,
        958,
        "#fbf5f6"
      ],
      "border": true
    }
  ]
}
[/block]
When the account setup is done, the following message is displayed and you can now create a campaign:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5c12d65-Account_Setup_done.png",
        "Account Setup done.png",
        2684,
        934,
        "#f7f6fa"
      ],
      "border": true
    }
  ]
}
[/block]
* Set a goal: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve with the campaign. You can define your conversion goal further by filtering an event by event properties. This selection is optional.

  The campaign goal can be as generic or as specific as you want. It can answer questions from *How many users were influenced for purchasing an X amount?* to *How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount? ". 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7723483-Conversion_tracking.png",
        "Conversion tracking.png",
        2214,
        644,
        "#fbfbfd"
      ],
      "border": true
    }
  ]
}
[/block]
## Define the Audience

You must indicate the target audience for your Audiences campaign. You can specify your target audience from the *Target segment* section. Here, you can create a new segment or use a previously saved user segment from the *segment* list.

For Past Behavior segments, you also calculate the *Estimated reach*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f2c543d-SMS_Who.png",
        "SMS_Who.png",
        961,
        766,
        "#f8f8fc"
      ],
      "border": true
    }
  ]
}
[/block]
### Segment
If you want to create an ad-hoc segment, you can select a type of segment on which to base your Audiences campaign. You can create the target based on past user behavior and user properties.

On this basis, you would then set up the *Who* by choosing to send this campaign to all users who qualify or just a portion of the users who qualify under *Estimated reach*. 


### Deliver Audiences Notifications based on Past Behavior (PBS)

You can also target users basis their past behavior. For past behavior campaigns, you also have an option to calculate *Estimated reach*. The estimated reach shows the number of users that qualify for the campaign criteria and the number of reachable users.

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can send an Audiences notification to English-speaking female users who live in the United States. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/345e0b1-campaigns_user_properties.png",
        "campaigns_user_properties.png",
        516,
        204,
        "#f7f8fc"
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

## Define the Message Content

Now, you can set up the *What*, which is the Audiences campaign content. Click *Go To Editor* to create your message. 

### Audiences Editor 

Choose the adset to export for this campaign. This ensures you can get the stats for this adset back into CleverTap for you to view in the CleverTap dashboard.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/46d0b68-Audiences_What.png",
        "Audiences_What.png",
        2670,
        746,
        "#fbf9f9"
      ],
      "border": true
    }
  ]
}
[/block]
## Define the Campaign Schedule

You can set up the *When* to schedule the campaign start and end using the options below:

The delivery preferences for Past behavior campaigns can be set as follows:

* Send Now: Select this option to send the campaign right away.
* Schedule for later: Select this option to send the campaign on a specific date and time.
* Set as Recurring: Select this option to send the campaign at specific intervals. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ed19319-Push_notification_editor_when.png",
        "Push_notification_editor_when.png",
        978,
        485,
        "#fbfaf8"
      ],
      "border": true
    }
  ]
}
[/block]
###Delivery preferences
 
Global campaign limits are limits you can apply to determine how many Audiences notifications each app user receives per day. If you want to override these settings for an important campaign, you can select the *Don’t apply global campaign limits to this campaign* checkbox.

You can also click the *Advanced* checkbox to specify *Do Not Disturb* (DND) hours during which notifications from this push campaign are prevented from going out, either by discarding them or delaying delivery after DND hours, such as 9 PM to 9 AM.

Since past behavior campaigns can have scheduled times, you have the option to stop a campaign delivery after a certain cut-off time, or even deliver at the specified time in the user’s timezone. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ac20918-Campaign_Adwords_delivery_preferences.png",
        "Campaign_Adwords_delivery_preferences.png",
        777,
        384,
        "#fafbfd"
      ],
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "Recurring Day",
  "body": "If you specify a recurring day for a campaign such as the 7th of each month, then the campaign will start for the specified day and ignore the creation date. This is a precaution to avoid sending a campaign unintentionally on a prior date."
}
[/block]
## Publish Campaign

After testing and previewing the appearance of your campaign, finalize your campaign by clicking **Publish Campaign**.
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