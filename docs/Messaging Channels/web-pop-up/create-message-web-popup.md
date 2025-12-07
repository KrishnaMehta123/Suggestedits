---
title: Create Message
excerpt: Learn how to create a Web Popup campaign using the CleverTap dashboard
deprecated: false
hidden: false
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

<Image title="Campaign Button Lists All Channels" alt="Select Messaging Channel" align="center" border={true} src="https://files.readme.io/f6767b03204608d45a623ef262192624a0e5458b39afdbd892ff9c35add8d49e-wepuchs.png">
  Select Messaging Channel
</Image>

The campaign page displays.

<Image title="Expand Each Section" alt={1100} align="center" width="80%" border={true} src="https://files.readme.io/4bf6219-Web_pop_up_Editor_main.png">
  Create Campaign
</Image>

Define all the sections and publish the campaign.

## Start Campaign Setup

The *Start here* section displays the setup information. 

**Set a goal:** You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. This selection is optional.

The campaign goal can be as generic or as specific as you want. It can answer questions from *How many users were influenced to purchase an X amount?* to *How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount?*". 

Define the conversion period by selecting the Conversion Time. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, see [Events](doc:events).

<Image title="Track Conversions" alt={919} align="center" border={true} src="https://files.readme.io/4fbbeb2-Push_notification_set_goal_track_conversion.png">
  Set a Goal
</Image>

## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the Target segment section. Here, you can create a new segment or use a previously saved user segment from the segment list.

<Image title="Define Target Audience" alt={2448} align="center" border={true} src="https://files.readme.io/6e9cb3a-Web_Popup_Segment_.png">
  Define Target Segment - Who
</Image>

Campaigns can be configured based on the following types of user interactions:

* Single Action: Target users based on action on one of your web pages.
* Page Visit: Target users visiting specific web pages. For example, a page such as *[https://ctcart.com/black\_friday\_sale](https://ctcart.com/black_friday_sale)*, where you can create a campaign to target users that visit the Black Friday sale on your website. You can add multiple pages. 
* Page Referral: Target users visiting your website via any referral web page. For example, users who have visited your website through a Black Friday sale advertisement on google, such as\
  *[https://ctcart.com/redirect?utm\_medium=google\&utm\_campaign=black\_friday\_sale](https://ctcart.com/redirect?utm_medium=google\&utm_campaign=black_friday_sale)*. 
* Page Count: Target users based on the specified number of web pages visited in a single session. 

### Deliver Action Based Web Popup Notifications

You can trigger a web popup message based on an action. For example, a web popup with a promo code can be shown to customers who have just completed a purchase. This will help incentivize an existing user. Moreover, such popups make notifications more contextual and result in increased conversion.

### Filter Users Based on Past Behavior

You can also target users basis their past behavior. For example, you might want to target customers who have purchased a specific product in the past. 

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can send a web popup notification to female users who live in the United States. The image below represents a sample target segment that is filtered using specific user properties to target the required audience.

<Image title="Add Multiple User Properties" alt={2202} align="center" border={true} src="https://files.readme.io/9289ee7-Screenshot_2021-10-26_at_2.53.00_PM.png">
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

> ℹ️ Web pop-up campaigns with API
>
> Web pop-ups are not supported for events triggered via API; they will only render for events raised from the Web SDK.

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information on control groups, see [Control Groups](doc:control-groups)

<Image title="Control Group and Targeting Cap" alt={2338} align="center" border={true} src="https://files.readme.io/ca9ad92-Screenshot_2021-10-22_at_1.25.05_PM.png">
  Control Group
</Image>

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

<Image title="Identify Best Variant" alt={2326} align="center" border={true} src="https://files.readme.io/561e7ef-Web_popup_AB_test.png">
  A/B Test Variant Distribution
</Image>

### Split Delivery

With split delivery, you can decide what percentage of your audience receives each pop-up variant for the duration of the campaign.

<Image title="Control Variant Distribution" alt={2344} align="center" border={true} src="https://files.readme.io/b3026b1-pop-up_slit_delivery.png">
  Split Delivery Variant Distribution
</Image>

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

Similar to creating A/B test variants, you can use the *+ Variant* button to add multiple variants based on a user property value. In the example below, we have used the *Language* user property so users with different language preferences will receive corresponding copies of the campaign in their preferred language.

<Image title="Upto 50 Message Variants" alt={2320} align="center" border={true} src="https://files.readme.io/3d9b2da-hindi_sale.png">
  Message Variant by User Property
</Image>

## Define the Web Pop-up Message Content

After you select a particular message type, you need to choose a template. CleverTap supports four types of templates for Web popup creation - *Basic*, *Ratings*, *Lead Generation*,  *Custom HTML*, and Drag & Drop Editor template.

<Image alt="Web Popup Template Types" align="center" border={true} src="https://files.readme.io/cc4878c-webpopup_template_drag_and_drop.jpg">
  Web Popup Template Types
</Image>

## Web Pop-up Editor

Select the templates and create a message. For more information on the  Web Pop-up Editor, see [Web Pop-up Editor](https://docs.clevertap.com/docs/web-pop-up-editor) .

### Preview

Once you are all done setting up the content of your Web Popup campaign in the *What* section, you have the option to preview how your popup would look to your end-users. 

Click **Preview** button from the message editor to get a preview of your created web popup.

## Define the Campaign Schedule

Each web popup campaign needs to be scheduled to run actively for a specific timeline. To define the schedule for your popup campaign, you need to specify the *Start date and time* and *End date and time*. You also have the option to start a campaign immediately by selecting *Now*.  Besides, you can also define a delay (by seconds, minutes, hours, or days) once a user qualifies for the target segment. Once you define the schedule and click on *Done*, the campaign will be triggered and terminated as per the defined timings.

<Image title="Define When the Campaign is Sent" alt={1904} align="center" border={true} src="https://files.readme.io/429532e-when.png">
  Campaign Schedule
</Image>

### Delivery preferences

#### Web Campaign Priority

 A user may qualify for multiple web popup campaigns simultaneously. In this case, you may want to prioritize the web popup that provides the highest business value. 

Example:

A Fintech website may want to show web popups to its users for credit cards, car loans, and also personal loans. The business team considers that credit card sales provide higher returns than other offers. In this case, you can assign a higher priority to the web popup campaigns for credit cards.

<Image alt="Define Campaign Priority for Web Popup" align="center" border={true} src="https://files.readme.io/a7a6a05-campaign_priority.jpg">
  Define Campaign Priority
</Image>

The *Web Campaign Priority* option enables you to set priority levels from 1 (lowest) to 100 (highest), with 1 being the default priority. Configuring Web Campaign Priority allows you to prevent priority conflicts, particularly for campaigns configured on the same triggers.

*Example*:\
Consider a scenario where two Web Popup campaigns are triggered on the *Add to cart* event  campaign A with priority 8 and campaign B with priority 10. Both campaigns qualify per the defined trigger; however, end users will receive campaign B because the priority level is higher.

> 📘 Web Popup Campaign with Same Priority
>
> If two campaigns have the same trigger and campaign priority, any one of the campaigns may be displayed.

#### Triggers for Campaign Delivery

Triggers are conditions that determine when to show a web popup campaign to a user. You can activate the campaign based on actions,  such as user qualification, inactivity, scrolling behavior, or detecting when the user is about to leave the page. You can select one or multiple triggers, and the campaign is delivered as soon as any selected trigger condition occurs. This helps you streamline your marketing strategy.

<Image alt="Triggers for Campaign Delivery" align="center" border={true} src="https://files.readme.io/1b6924a-Delivery_preferences_web_triggers.jpg">
  Triggers for Campaign Delivery
</Image>

You can leverage either or all of the following triggers:

* **As soon as user qualifies**:
  * The campaign message is triggered immediately once the user meets the campaign criteria.
* **Specific Trigger:**\
  This option lets you set specific conditions to display the message popup. Select from any of the following triggers:
  * **After qualification, send in:**\
    The campaign is triggered after a specified delay once the user qualifies. You can set the number of seconds to wait before showing the popup.
  * **If inactive for:**\
    The campaign is triggered if the user does not interact with the page for a set duration. You can set the number of seconds of inactivity.
  * **Scroll percentage:**\
    The campaign is triggered when the user scrolls down beyond a certain point on the page. You can set the percentage of the page the user must scroll to trigger the campaign.
  * **Exit intent (about to leave page):**\
    The campaign is triggered when the system detects the user is about to leave the page. This is often used for exit-intent campaigns.

You can choose one or multiple triggers from the options provided. If multiple triggers are selected, the campaign is delivered as soon as the first trigger occurs.

#### Set Frequency

You might not want a campaign to run actively in certain scenarios on a particular day and time. In such cases, you can set the frequency for that particular campaign.

Finally, you can specify how often users receive the campaign: Bypass global campaign limits by selecting the *Exclude from campaign limits* option from the dropdown or choosing the appropriate cadence on how often to send your campaign.

<Image title="Changes Based on Segment Selection" alt={1298} align="center" border={true} src="https://files.readme.io/dcab498-DP.png">
  Delivery Preferences
</Image>

> 📘 Global Session Limits
>
> In the global campaign limits, when you want to show 'x' web popups per session, it actually applies to 'x' distinct web popup campaigns, not the same web popup campaign.
>
> As per CleverTap's web SDK, for a given web popup campaign, it will only be shown once per session.

## Publish Campaign

After previewing the appearance of your campaign, finalize your campaign by clicking **Publish Campaign.**

<Image title="Publish Final Campaign" alt={1193} align="center" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png">
  Publish Campaign
</Image>

# Assigning Priorities for Web Pop-up Campaigns

After publishing the campaign, marketers can assign the priorities to specific campaigns to avoid random delivery of popups. This means, if multiple web popups are scheduled to go live for the same web page at the same time, the priority order defines the order in which the popups are to be shown.

To assign the priority:

1. Navigate to the Campaigns dashboard and select the specific campaign from the campaign list.
2. Click the Web priority marker icon below each campaign to open the priority list.

<Image alt="Assign Priority to Web Pop-up Campaign" align="center" border={true} src="https://files.readme.io/cc78f53c50ff995b73151f6d1c8f508c46ffd4c45dcf24865f9adc6451567737-Web_Pop-up_Priority.png">
  Assign Priority to Web Pop-up Campaign
</Image>

Set the priority as per your choice and click *Save*.

<Image alt="Priority List for Campaigns" align="center" border={true} src="https://files.readme.io/b18d568435064f0c3acdf49a44cc430de2fa5be7b77c4bb24c06d2ebf1c11ea4-image.png">
  Priority List for Campaigns
</Image>
