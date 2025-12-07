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
      url: https://docs.clevertap.com/docs/personalize-message-web-popup_c20
    - type: link
      title: Define a Custom Callback
      url: https://docs.clevertap.com/docs/setup-web-popup_c20
    - type: link
      title: Web Popup Stats
      url: https://docs.clevertap.com/docs/web-popup-stats_c20
    - type: link
      title: Analyze User Ratings
      url: https://docs.clevertap.com/docs/user-ratings_c20
---
# Create a New Campaign

Create a campaign to deliver your Web Popup message. Follow the steps below to create a new web popup campaign:

1. From the dashboard, navigate to *Campaigns*. 
2. Click **+ Campaign** button.
3. From the *Messaging Channels* list, select *Web Popup.* 

<Image title="Web Popup.png" alt={2858} className="border" border={true} src="https://files.readme.io/bc28545-Web_Popup.png" />

The campaign page displays.

<Image title="Web_pop_up_Editor_main.png" alt={1100} className="border" width="80%" border={true} src="https://files.readme.io/4bf6219-Web_pop_up_Editor_main.png" />

Define all the sections and publish the campaign.

## Start Campaign Setup

The *Start here* section displays the setup information. 

**Set a goal:** You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. This selection is optional.

The campaign goal can be as generic or as specific as you want. It can answer questions from *How many users were influenced for purchasing an X amount?* to *How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount?*". 

Define the conversion period by selecting the Conversion Time. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, see [Events](doc:events).

<Image title="Push_notification_set_goal_track_conversion.png" alt={919} className="border" border={true} src="https://files.readme.io/4fbbeb2-Push_notification_set_goal_track_conversion.png" />

## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the Target segment section. Here, you can create a new segment or use a previously saved user segment from the segment list.

<Image title="campaign_Who_Live_segment.png" alt={964} className="border" border={true} src="https://files.readme.io/a92d833-campaign_Who_Live_segment.png" />

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

<Image title="Screenshot 2021-10-26 at 2.53.00 PM.png" alt={2202} className="border" border={true} src="https://files.readme.io/9289ee7-Screenshot_2021-10-26_at_2.53.00_PM.png" />

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

<Image title="Screenshot 2021-10-22 at 1.25.05 PM.png" alt={2338} className="border" border={true} src="https://files.readme.io/ca9ad92-Screenshot_2021-10-22_at_1.25.05_PM.png" />

## Define the Web Popup Message Content

Now, you need to set up the *What* section to define the content for the Web Popup campaign.

 Click *Go To Editor* to create your message. 

<Image title="Webhook_what_without_options.png" alt={1048} className="border" border={true} src="https://files.readme.io/8a73e71-Webhook_what_without_options.png" />

The *Create Web Popup Message* window displays.

## Web Popup Editor

Select the desired template. CleverTap supports three types of templates for Web popup creation - *Basic*, *Ratings*, and *Custom HTML.*

<Image title="Screenshot 2021-10-18 at 3.04.35 PM.png" alt={1740} className="border" border={true} src="https://files.readme.io/fd619f5-Screenshot_2021-10-18_at_3.04.35_PM.png" />

* **Basic Templates**

    At a high level, one can choose from three styles of popup layouts available under Basic Templates:

  * **Box** - It's a small popup that can be placed at the desired corners of the browser window.
  * **Banner**- It's a wide horizontal popup that can be either placed at the top or bottom of the browser window.
  * **Interstitial** - It's a center-aligned popup particularly used for driving better engagements.

* **Ratings Template**

  Marketers can now create feedback-related popups (Interstitials only) for their website users using the *Ratings Template*. 

    You can create two types of rating templates for gaining feedback from the customers:

  * User Rating Popup
  * NPS Popup

    The images below represent a sample user rating popup and NPS popup.

<Image title="feedback1.png" alt={1200} className="border" border={true} src="https://files.readme.io/8ea6741-feedback1.png" />

<Image title="NPS feedback.png" alt={1276} className="border" border={true} src="https://files.readme.io/76e9149-NPS_feedback.png" />

Marketers get the complete flexibility to explicitly define the rating scale, style,  its shape (Star, Heart, Emojis), labels, and the overall content of the popup. One can also choose to add a comment box to get accurate user feedback/comments. 

<Image title="styling.png" alt={1710} className="border" border={true} src="https://files.readme.io/7bbc6cc-styling.png" />

Besides, additional styling such as the background color of the notification, text color, button color, and the color of the rating scale is also possible from the editor as shown in the image above. Refer to the [Analysing User Rating] ([https://docs.clevertap.com/docs/user-ratings](https://docs.clevertap.com/docs/user-ratings)) document to learn more about tracking and monitoring user rating data.

The web popup notification text fields shown below can be personalized for every user based on specific user property or event property values. For more information, refer to [User Profiles](https://docs.clevertap.com/docs/user-profiles).

Enter all the required information. 

<Image title="web pop up editor.png" alt={2862} className="border" border={true} src="https://files.readme.io/0c72705-web_pop_up_editor.png" />

> 🚧 Browser Considerations
>
> Some of the optional items only apply to a certain browser, such as Firefox, Chrome, or KaiOS.

* **Custom HTML Templates**

Users have a choice to customize their popup's appearance for the Box, Banner, and Interstitial templates. One simply needs to insert the custom HTML scripts for the respective template layout in the HTML editor.

### Preview

Once you are all done setting up the content of your Web Popup campaign in the *What* section, you have the option to preview how your popup would look like to your end-users. 

Click **Preview** button from the message editor to get a preview of your created web popup.

## Define the Campaign Schedule

Each web popup campaign needs to be scheduled to run actively for a specific timeline. To define the schedule for your popup campaign, you need to specify the *Start date and time* and *End date and time*. You also have the option to start a campaign immediately by selecting *Now*.  Besides, you can also define a delay (by seconds, minutes, hours, or days) once a user qualifies for the target segment. Once you define the schedule and click on *Done*, the campaign will be triggered and terminated as per the defined timings.

<Image title="when.png" alt={1904} className="border" border={true} src="https://files.readme.io/429532e-when.png" />

### Delivery preferences

In certain scenarios, you might not want a campaign to run actively on a particular day and time. In such cases, you can set the frequency for that particular campaign.

Finally, you can specify how often users receive the campaign: Bypass global campaign limits by selecting the *Exclude from campaign limits* option from the dropdown or choose the appropriate cadence on how often to send your campaign.

<Image title="DP.png" alt={1298} className="border" border={true} src="https://files.readme.io/dcab498-DP.png" />

> 📘 Global Session Limits
>
> In the global campaign limits, when you want to show 'x' web popups per session, it actually applies to 'x' distinct web popup campaigns, not the same web popup campaign.
>
> As per CleverTap's web SDK, for a given web popup campaign, it will only be shown once per session.

## Publish Campaign

After previewing the appearance of your campaign, finalize your campaign by clicking **Publish Campaign.**

<Image title="campaign_Publish.png" alt={1193} className="border" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png" />

# Assigning Priorities for Web Popup Campaigns

After publishing the campaign, marketers can assign the priorities to specific campaigns to avoid random delivery of popups. This means, If multiple web popups are scheduled to go live for the same web page at the same time, the priority order defines which popup will be shown. To assign the priority, navigate to the Campaigns dashboard and select the specific campaign from the campaign list.

Below each campaign, there's a *Web priority* marker. Click the marker icon to open the priority list.

<Image title="wp.png" alt={1788} className="border" width="auto" border={true} src="https://files.readme.io/0805d48-wp.png" />

Set the priority as per your choice and click **Save** 

<Image title="WP2.png" alt={1780} className="border" width="smart" border={true} src="https://files.readme.io/02664d2-WP2.png" />
