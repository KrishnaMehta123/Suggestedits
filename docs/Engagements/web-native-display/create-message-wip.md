---
title: Create Message (WIP)
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
## Create a New Campaign

Create a campaign to deliver your message.\
To create a new campaign:

1. From the dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **Web Native Display**. 

<Image title="Web Native Display.png" alt={2544} width="80%" border={true} src="https://files.readme.io/a19d60f-Web_Native_Display.png">
  Select Messaging Channel
</Image>

The *Campaign* page displays.

<Image title="Native display web.png" alt={1472} width="80%" border={true} src="https://files.readme.io/aecb9e8-Native_display_web.png">
  Create Campaign
</Image>

Define all the sections and publish the campaign. 

## Start Campaign

The *Start here* section displays the setup information. 

This section has the following parts:

* Set a goal: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. This selection is optional.

The campaign goal can be as generic or as specific as you want. It can answer questions from "*How many users were influenced for purchasing an X amount?*" to "*How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount?* ". 

Define the conversion period by selecting the *Conversion Time*. You can define your conversion goal further by filtering an event by event properties.  For more information on event properties, see [Events](https://docs.clevertap.com/docs/events#event-properties). 

<Image title="Push_notification_set_goal_track_conversion.png" alt={919} border={true} src="https://files.readme.io/4fbbeb2-Push_notification_set_goal_track_conversion.png">
  Set a Goal
</Image>

## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the *Target segment* section. Here, you can create a new segment or use a previously saved user segment from the *segment* list. 

<Image title="campaign_Who_Live_segment.png" alt={964} className="border" border={true} src="https://files.readme.io/f1fee47-campaign_Who_Live_segment.png" />

### Segment

If you want to create an ad-hoc segment, you can select a type of segment on which to base your campaign. You can create the target based on user properties or live (ongoing) user behavior. The latter is helpful to send out real-time, triggered campaigns.

### Deliver Action-Based Web Native Display Campaign

You can trigger a web native display campaign based on an action. Users receive this campaign when they perform an action on the website. For example, creating a campaign that displays a personalized contextual banner with images of fitness equipment for users who have shown interest in the fitness category.\
It makes the web experience more contextual and increases conversion. 

### Filter Users Based on Past Behavior

You can also target users basis their past behavior. For example, you might want to create a personalized campaign for a set of customers who have purchased a specific product in the past. 

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can create a web native display campaign specifically for female users who live in the United States. The image below represents a sample target segment that is filtered using specific user properties to target the required audience.

<Image title="user prop.png" alt={2202} border={true} src="https://files.readme.io/d3dca2d-user_prop.png">
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

### Control Group

You can define the control group to compare and measure the results of your campaign. For more information, refer to [Control Groups](doc:control-groups).

<Image title="control group.png" alt={825} border={true} src="https://files.readme.io/99861e7-control_group.png">
  Control Group
</Image>

## Message Types

You can create the following types of messages:

* Single Message
* AB Test
* Split Delivery
* By User Property

### Single Message

Here, a standard web campaign is rolled out for all the users who qualify as your target audience. This type of campaign is best suited for use cases where the campaign communication does not vary based on the differences between properties such as language, geography, or any other user properties.

### A/B Testing

A/B testing helps you understand what type of message copy works best to get clicks from users.

You can test up to three message variants on a test group and the variant that gets the most clicks is declared the winning variant and is automatically sent to the rest of your target audience.

When you create multiple variants for a campaign, you can also auto-copy what is already present in a current variant.

### Split Delivery

With split delivery, you can decide what percentage of your audience receives each message variant for the duration of the campaign.

<Image title="campaign_split_delivery.png" alt={577} className="border" border={true} src="https://files.readme.io/73d579a-campaign_split_delivery.png" />

#### Split Delivery to Live User Segments

With campaigns sent to live user segments (triggered campaigns), messages are delivered immediately when a user’s activity matches the criteria you have selected. For example, you can send a message when the user has completed a booking or purchase. Since it is not possible to determine the reach of triggered campaigns upfront, you need to decide how many total messages to send for A/B testing before a winner is declared.

> 👍 Triggered Campaign Example
>
> If you select 500 users as your test audience, we will alternate delivery of Variant A and Variant B as users qualify for the campaign. After a total of messages are sent (Variant A – 250 and Variant B – 250), we then decide the winner based on the number of clicks and continue only with this winning message for the duration of the campaign.

Deciding on a test audience for A/B testing triggered campaigns requires some estimation. We recommend you check the total messages that were sent for similar triggered campaigns in the past to get a sense of how many users may qualify. If you select a test audience that is too small such as 25 users, you will get a statistically insignificant sample. If your test group size exceeds the total number of users who ultimately qualify for that campaign, then no winner will be declared and each message variant will be alternatively delivered for the duration of the campaign.

### By User Property

If you would like to send different message variants to your target audience based on the user properties they possess, this campaign type is your best bet. A good example would be when you want to send a localized update to people based on their preferred language.

## Web Native Display Templates

<Image title="carousel and banner.png" alt={2558} className="border" border={true} src="https://files.readme.io/feade00-carousel_and_banner.png" />

Marketers get instant access to ready-to-use message templates for creating engaging campaigns. These templates are mobile responsive, which means marketers can deliver personalized campaigns across devices (mobiles, tablets, desktops etc). CleverTap supports

### Custom Key Value

Marketers can use the custom Key-Value template for delivering an engaging and personalized user experience.\
The custom key value can have any value. 

> 🚧 Note
>
> The first key of your object will always be **topic**. The marketer can provide the relevant value of this key while configuring the campaign. The developer must use this value to access the right payload for that campaign.

For example, if you want to change the carousel images for your users based on their language and favorite products, you can set the custom key-value pairs for this change.

<Image title="web native display key value.png" alt={1596} className="border" border={true} src="https://files.readme.io/bd5c152-web_native_display_key_value.png" />

### Banner

The banner template allows you to create visually appealing banners for your website. You can directly upload the banner image or add a URL to the banner. Besides, you also get the flexibility to upload a dedicated image for mobile users to deliver an optimal experience for mobile audiences. 

You need to enter the [Div ID](https://developer.clevertap.com/docs/web-native-display#banner-templates) for the relevant container where you wish to render the banner on your website. Optionally, you can also define the Div height to adjust the appearance of your banner.\
You can also provide a URL for redirecting the users to a specific web page when they click a banner.

<Image title="banner 1.png" alt={2558} className="border" border={true} src="https://files.readme.io/79e565b-banner_1.png" />

### Banner with Text

Similar to the Banner template, the Banner with Text template allows you to create visually appealing banners with personalized messages for contextual communications. Marketers can add title and descriptions to their banners and personalize them to deliver individualized experiences. For example, marketers can target their audience by personalizing names in the banner title for enhanced engagement.

You need to enter the [Div ID](https://developer.clevertap.com/docs/web-native-display#banner-templates) for the relevant container where you wish to render the banner on your website. Optionally, you can also define the Div height to adjust the appearance of your banner.\
You can also provide a URL for redirecting the users to a specific web page when they click the banner.

<Image title="banner text.png" alt={2868} className="border" border={true} src="https://files.readme.io/fe8f080-banner_text.png" />

Under the *Style* tab in the editor, you also have the option to align the title and description of your banner as per your design guidelines. Additionally, you can also define the font style, size,  and color of the title and description.

<Image title="banner font 2.png" alt={2544} className="border" border={true} src="https://files.readme.io/12ecfc1-banner_font_2.png" />

### Banner Carousel

Banner Carousels let you quickly create or modify up to seven rotating banners that help you deliver engaging content faster. It primarily lets you display broader and more engaging content within restricted real estate on your website.

Using the Banner Carousel template, you can create promotional and engaging banner slides that can auto-rotate. You can use this template for various purposes, such as displaying the latest product releases on e-commerce sites, banners of web series on OTT platforms, and showcasing festive offers on home pages. 

![1272](https://files.readme.io/ec98127-banner_carousel_gif_1.gif "banner carousel gif (1).gif")

You need to enter the Div ID for the relevant container where you wish to render the banner carousel on your website. Optionally, you can also define the Div height to adjust the appearance of the banner carousel.

You can also provide a URL for redirecting the users to a specific web page when they click a specific banner slide.  Additionally, you can also use a different image for mobile users to optimize the viewing experience for your mobile audience.

You need to define the *Slider time* (in seconds) so that the banner slides auto-rotate after the defined time. You also have the option to enable the *Carousel dots* and *Navigation arrows* to scroll banner slides manually.

<Image title="Screenshot 2022-12-11 at 4.35.07 PM.png" alt={1454} className="border" border={true} src="https://files.readme.io/37db7f7-Screenshot_2022-12-11_at_4.35.07_PM.png" />

### Banner Carousel With Text

This template is similar to the *Banner Carousel* template with an additional option of adding a Title and Description on top of each banner in the carousel. 

<Image title="banner carousel.gif" alt={1264} className="border" border={true} src="https://files.readme.io/3fa56dc-banner_carousel.gif" />

Under the *Style* tab in the editor, you also have the option to align the title and description of your banner as per your design guidelines. Additionally, you can also define the font style, size,  and color of the title and description.

<Image title="font.png" alt={2554} className="border" border={true} src="https://files.readme.io/7ccd87d-font.png" />

## Define the Campaign Schedule

The delivery preferences for Live campaigns can be set as follows:

* Start Date and Time
* End Date and Time
* Set Delay

<Image title="Campaign_When_Live_segment.png" alt={974} className="border" border={true} src="https://files.readme.io/0637733-Campaign_When_Live_segment.png" />

### Delivery preferences

#### Set frequency

From the *Delivery preferences* section, select the days and the time frame to deliver the message.\
Click *Apply to all* to copy the choices from the selected day to all other days. 

<Image title="delivery_preferences.png" alt={1085} className="border" border={true} src="https://files.readme.io/f4ad363-delivery_preferences.png" />

## Publish Campaign

After testing and once you are satisfied with the appearance of your campaign, finalize your campaign with the following steps:

1. Click **Continue** to view your campaign summary. The overview page displays.
2. View your campaign summary, then click **Publish Campaign**.

<Image title="campaign_Publish.png" alt={1193} className="border" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png" />
