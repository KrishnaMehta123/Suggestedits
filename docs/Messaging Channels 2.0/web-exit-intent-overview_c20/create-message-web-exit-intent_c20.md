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
## Create a New Web Exit Intent Campaign

To create a new Web Exit Intent Popup campaign:

1. From the dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **Web Exit Intent**. 

<Image title="webexit.png" alt={2846} className="border" border={true} src="https://files.readme.io/39044fd-webexit.png" />

The campaign page displays.

<Image title="Web_exit_intent_editor_main.png" alt={976} className="border" width="80%" border={true} src="https://files.readme.io/03e2e61-Web_exit_intent_editor_main.png" />

Define all the sections and publish the campaign.

## Start Campaign Setup

The *Start here* section displays the setup information. 

* **Set a goal**: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve in the campaign. This selection is optional.

The campaign goal can be as generic or as specific as you want. It can answer questions from *How many users were influenced for purchasing an X amount?* to \*How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount? ". 

Define the conversion period by selecting the *Conversion Time*. You can define your conversion goal further by filtering an event by event properties. For more information on event properties, see [Events](doc:events).

<Image title="Push_notification_set_goal_track_conversion.png" alt={919} className="border" border={true} src="https://files.readme.io/4fbbeb2-Push_notification_set_goal_track_conversion.png" />

## Define the Audience

You must indicate the target audience for your campaign. You can specify your target audience from the *Target segment* section. Here, you can create a new segment or use a previously saved user segment from the segment list. 

<Image title="campaign_Who_Live_segment.png" alt={964} className="border" border={true} src="https://files.readme.io/bf4a5f0-campaign_Who_Live_segment.png" />

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

<Image title="up.png" alt={2242} className="border" border={true} src="https://files.readme.io/0141dfe-up.png" />

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

<Image title="cg.png" alt={1480} className="border" border={true} src="https://files.readme.io/fd0d08b-cg.png" />

## Define the Message Content

Now, you need to set up the *What* section to define the content for the Web Exit Popup campaign.

Click **Go to Editor**. 

<Image title="Webhook_what_without_options.png" alt={1048} className="border" border={true} src="https://files.readme.io/8a73e71-Webhook_what_without_options.png" />

The *Create Web Exit Intent Message* window displays.

## Message Editor

<Image title="web exit.png" alt={2564} className="border" border={true} src="https://files.readme.io/f98671a-web_exit.png" />

For web exit intent pop-ups, you can specify a button with text. Upon a web pop-up click, you can either do nothing, open a link, or invoke a JavaScript function.

## Define the Campaign Schedule

Each web exit intent campaign needs to be scheduled to run actively for a specific timeline. To define the schedule for your popup campaign, you need to specify the *Start date and time* and *End date and time*. You can also define a delay (by seconds, minutes, hours, or days) once a user qualifies for the target segment. Once you define the schedule and click on *Done*, the campaign will be triggered and terminated as per the defined timings.

<Image title="when.png" alt={1904} className="border" border={true} src="https://files.readme.io/0b43104-when.png" />

### Delivery preferences

In certain scenarios, you might not want a campaign to run actively on a particular day and time. In such cases, you can set the frequency for that particular campaign.

Finally, you can specify how often users receive the campaign: Bypass global campaign limits by selecting the *Exclude from campaign limits* option from the dropdown or choose the appropriate cadence on how often to send your campaign.

<Image title="DP.png" alt={1298} className="border" border={true} src="https://files.readme.io/bf4c04a-DP.png" />

## Publish Campaign

* After previewing the appearance of your campaign, finalize your campaign by clicking **Publish Campaign.**

<Image title="campaign_Publish.png" alt={1193} className="border" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png" />

# Assigning Priorities for Web Exit Intent Campaigns

After publishing the campaign, marketers can assign the priorities to specific campaigns to avoid random delivery of exit-intent popups. This means, If multiple web popups are scheduled to go live for the same web page at the same time, the priority order defines which popup will be shown. To assign the priority, navigate to the Campaigns dashboard and select the specific campaign from the campaign list.

Below each campaign, there's a *Web priority* marker. Click the marker icon to open the priority list.

<Image title="wp.png" alt={1788} className="border" width="auto" border={true} src="https://files.readme.io/0805d48-wp.png" />

Set the priority as per your choice and click **Save** 

<Image title="WP2.png" alt={1780} className="border" width="smart" border={true} src="https://files.readme.io/02664d2-WP2.png" />
