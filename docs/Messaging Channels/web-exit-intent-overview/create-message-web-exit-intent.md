---
title: Create Message
excerpt: Learn how to create a Web Exit Intent campaign using the CleverTap dashboard
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Create a New Web Exit Intent Campaign

To create a new Web Exit Intent Popup campaign:

1. From the dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **Web Exit Intent**. 

<Image title="Campaign Button Lists All Channels" alt="Select Messaging Channel" align="center" border={true} src="https://files.readme.io/ef1613e3ed9670c081319ba4fbef48e383bc0a6fde5a595feb23ccadf240fcde-wepuchs.png">
  Select Messaging Channel
</Image>

The campaign page displays.

<Image title="Expand Each Section" alt={976} align="center" width="80%" border={true} src="https://files.readme.io/03e2e61-Web_exit_intent_editor_main.png">
  Create Campaign
</Image>

Define all the sections and publish the campaign.

## Start Campaign Setup

The *Start here* section displays the setup information. 

* **Set a goal**: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. This selection is optional.

The campaign goal can be as generic or as specific as you want. It can answer questions from *How many users were influenced for purchasing an X amount?* to \*How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount? ". 

Define the conversion period by selecting the *Conversion Time*. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, see [Events](doc:events).

<Image title="Track Conversions" alt={919} align="center" border={true} src="https://files.readme.io/4fbbeb2-Push_notification_set_goal_track_conversion.png">
  Set a Goal
</Image>

## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the *Target segment* section. Here, you can create a new segment or use a previously saved user segment from the segment list. 

<Image title="Define the Target Segment" alt={964} align="center" border={true} src="https://files.readme.io/bf4a5f0-campaign_Who_Live_segment.png">
  Define Target Segment - Who
</Image>

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

<Image title="up.png" alt={2242} align="center" border={true} src="https://files.readme.io/0141dfe-up.png">
  Filter by User Properties
</Image>

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
        Geography Radius
      </td>

      <td>
        User's exact location. You can select a city, and then define the target radius. You can also select multiple cities. You can send this information using CleverTap's SDK. For more information, refer to the [iOS](https://developer.clevertap.com/docs/ios#section-send-location-information-to-clevertap) and [Android](https://developer.clevertap.com/docs/android#section-manually-updating-user-location) developer guides.
      </td>

      <td>
        Locations = San Francisco, USA; Paris, France
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

You can define the control group to compare and measure the results of your campaign. For more information on control groups, see [Control Groups](doc:control-groups).

<Image title="Control Group and Targeting Cap" alt={1480} align="center" border={true} src="https://files.readme.io/fd0d08b-cg.png">
  Control Group
</Image>

## Web Exit Intent Pop-up Message Types

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

When you create multiple variants for a campaign, you can also auto-copy what is already present in a current variant.

<Image alt="A/B Test Variant Distribution" align="center" border={true} src="https://files.readme.io/a575c38-B_Test_Variant.png">
  A/B Test Variants
</Image>

### Split Delivery

With split delivery, you can decide what percentage of your audience receives each pop-up variant for the duration of the campaign.

<Image title="Control Variant Distribution" alt={2322} align="center" border={true} src="https://files.readme.io/90063a5-split_delivery_web_exit.png">
  Split Delivery Variant Distribution
</Image>

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, you can use the *+Variant* button to add multiple variants based on a user property value. In the example below, we have used the *Language* user property so users with different language preferences will receive corresponding copies of the campaign in their preferred language (English, Hindi, etc.)

<Image title="Upto 50 Message Variants" alt={2324} align="center" border={true} src="https://files.readme.io/33b57c0-User_property_exit_intent.png">
  Message Variant by User Property
</Image>

## Define the Message Content

After you select a particular message type, you need to choose a template. CleverTap supports two types of templates for web exit intent pop-up creation:

* **Interstitial** -  It's a center-aligned pop-up mainly used for driving better engagements. The image below represents the editor for a sample Interstitial template.

<Image title="Create, Preview and Personalize Interstitial Message" alt={2564} align="center" border={true} src="https://files.readme.io/f98671a-web_exit.png">
  Interstitial Message
</Image>

For web exit intent pop-ups, you can specify a button with text. Upon a web pop-up click, you can either do nothing, open a link, or invoke a JavaScript function.

* **Custom HTML**  - Here the marketers have a choice to customize their exit intent pop-up's appearance for the Interstitial template. One simply needs to insert the custom HTML scripts for the respective template layout in the HTML editor. 

> 🚧 Manually Configured Click Tracking?
>
> If you are already raising the Notification Clicked event manually in your template, then ensure to disable the  *Enable click tracking for Custom HTML* checkbox to avoid overcounting.

To track the campaign stats such as the number of total clicks and CTRs, marketers need to ensure that they check mark the *Enable click tracking for Custom HTML* checkbox.

<Image title="Disable if Clicks Recorded Manually" alt={1528} align="center" src="https://files.readme.io/2c23c02-Screenshot_2022-10-07_at_6.21.52_PM.png">
  Track Campaign Stats
</Image>

## Define the Campaign Schedule

Each web exit intent campaign needs to be scheduled to run actively for a specific timeline. To define the schedule for your popup campaign, you need to specify the *Start date and time* and *End date and time*. You can also define a delay (by seconds, minutes, hours, or days) once a user qualifies for the target segment. Once you define the schedule and click on *Done*, the campaign will be triggered and terminated as per the defined timings.

<Image title="Define When the Campaign is Sent" alt={1904} align="center" border={true} src="https://files.readme.io/0b43104-when.png">
  Campaign Schedule
</Image>

### Delivery preferences

In certain scenarios, you might not want a campaign to run actively on a particular day and time. In such cases, you can set the frequency for that particular campaign.

Finally, you can specify how often users receive the campaign: Bypass global campaign limits by selecting the *Exclude from campaign limits* option from the dropdown or choose the appropriate cadence on how often to send your campaign.

<Image title="Changes Based on Segment Selection" alt={1298} align="center" border={true} src="https://files.readme.io/bf4c04a-DP.png">
  Delivery Preferences
</Image>

## Publish Campaign

* After previewing the appearance of your campaign, finalize your campaign by clicking **Publish Campaign.**

<Image title="Publish Final Campaign" alt={1193} align="center" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png">
  Publish Campaign
</Image>

# Assigning Priorities for Web Exit Intent Campaigns

After publishing the campaign, marketers can assign the priorities to specific campaigns to avoid random delivery of popups. This means, If multiple web popups are scheduled to go live for the same web page at the same time, the priority order defines the order in which the popups are to be shown. 

To assign the priority:

1. Navigate to the *Campaigns* dashboard and select the specific campaign from the campaign list.
2. Click the *Web priority* marker icon below each campaign to open the priority list.

<Image title="Define the Order of Popup Display" alt="Assign Priority to Web Popups" align="center" width="auto" border={true} src="https://files.readme.io/e4a9b6699d0fe59f26d9df4086109254ab83c791473237e2b02145e03f43b1ed-priotrity.png">
  Assign Priority to Web Popups
</Image>

Set the priority as per your choice and click **Save** 

<Image title="Select Web Popup Priorty" alt="Priority List" align="center" width="100%" border={true} src="https://files.readme.io/3d1595f8dc6a3c333ff97de1a3480eab1c7841489a656196bdcfca751aa370c2-low_hight.png">
  Priority List
</Image>
