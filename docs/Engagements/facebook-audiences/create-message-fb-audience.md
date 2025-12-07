---
title: Create Message
excerpt: Understand how to create a campaign for Facebook Audiences
deprecated: true
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: >-
    Refer to the pages listed below to learn more about the following Facebook
    Audiences section:
---
## Create a New Campaign

Create a campaign to deliver your Facebook Audience message.\
To create a new campaign:

1. From the CleverTap dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **Audience**. 

<Image title="Configure a New Facebook Campaign" alt="Create a New Facebook Campaign " align="center" border={true} src="https://files.readme.io/b229fce9bba060891c24ae3b31cc634525ddbd934c22c39ec852a6ac77337a9c-fd_adsd.png">
  Create a New Facebook Campaign
</Image>

The *Campaigns* page displays.

4. Select the Adset from the list.

<Image title="Facebook Campaign Configuration Page" alt={2748} align="center" width="80%" border={true} src="https://files.readme.io/e3905ab-New_FB_Audience_page.png">
  Facebook Campaign Configuration Page
</Image>

> 📘 Facebook ad set
>
> Refer [here](https://en-gb.facebook.com/business/learn/lessons/ad-set-level-overview) to create a new ad set on Facebook.

Define all the sections and publish the campaign.

## Start Campaign Setup

The *Start here* section displays the setup information. 

This section has the following parts:

* Start here: Displays the information for platforms such as FCM, Xiaomi, or iOS. Check that the required platforms are integrated and ready for campaigns. When the account set up is not done, the following warning message is displayed and you need to set up the account to be able to run campaigns:

<Image title="Facebook Audiences Account Setup Start Page" alt={2698} align="center" border={true} src="https://files.readme.io/0f891c5-Account_Setup_not_done_.png">
  Start the Facebook Audiences Account Setup
</Image>

When the account setup is done, the following message is displayed and you can now create a campaign:

<Image title="Facebook Audiences Account Setup Completed" alt={2684} align="center" border={true} src="https://files.readme.io/5c12d65-Account_Setup_done.png">
  Facebook Audiences Account Setup Completed
</Image>

* Set a goal: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve with the campaign. You can define your conversion goal further by filtering an event by event properties. This selection is optional.

  The campaign goal can be as generic or as specific as you want. It can answer questions from *How many users were influenced for purchasing an X amount?* to \*How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount? ". 

<Image title="Goal Conversion Tracking" alt={2214} align="center" border={true} src="https://files.readme.io/7723483-Conversion_tracking.png">
  Goal Conversion Tracking
</Image>

## Define the Audience

You must indicate the target audience for your Audiences campaign. You can specify your target audience from the *Target segment* section. Here, you can create a new segment or use a previously saved user segment from the *segment* list.

For Past Behavior segments, you also calculate the *Estimated reach*.

<Image title="Define the Target Audience" alt={961} align="center" border={true} src="https://files.readme.io/f2c543d-SMS_Who.png">
  Segment Your Target Audience
</Image>

### Segment

If you want to create an ad-hoc segment, you can select a type of segment on which to base your Audiences campaign. You can create the target based on past user behavior and user properties.

On this basis, you would then set up the *Who* by choosing to send this campaign to all users who qualify or just a portion of the users who qualify under *Estimated reach*. 

### Deliver Audiences Notifications based on Past Behavior (PBS)

You can also target users basis their past behavior. For past behavior campaigns, you also have the option to calculate *Estimated reach*. The estimated reach shows the number of users that qualify for the campaign criteria and the number of reachable users.

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can send an Audiences notification to English-speaking female users who live in the United States. 

<Image title="Filter by User Properties" alt={516} align="center" border={true} src="https://files.readme.io/345e0b1-campaigns_user_properties.png">
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

## Define the Message Content

Now, you can set up the *What* section, that is, you can select the adset to which you want to export the user details.

### Audiences Editor

Choose the adset to export for this campaign. This ensures you can get the stats for this adset back into CleverTap for you to view in the CleverTap dashboard.

Additionally, you have the option to choose from the following user details that you may want to upload to create an audience: email or phone. Customers can select either email, phone, or both. If both options are selected, CleverTap ensures that if any of these details are present in the user's profile, they are sent to Facebook.

<Image alt="Configure Adset In What Section" align="center" width="90% " border={true} src="https://files.readme.io/03a2b0f-image.png">
  Configure Adset In What Section
</Image>

## Define the Campaign Schedule

You can set up the *When* to schedule the campaign start and end using the options below:

The delivery preferences for Past behavior campaigns can be set as follows:

* Send Now: Select this option to send the campaign right away.
* Schedule for later: Select this option to send the campaign on a specific date and time.
* Set as Recurring: Select this option to send the campaign at specific intervals. 

<Image title="Define the Campaign Schedule" alt={978} align="center" border={true} src="https://files.readme.io/ed19319-Push_notification_editor_when.png">
  Define the Campaign Schedule
</Image>

### Delivery preferences

Global campaign limits are limits you can apply to determine how many Audiences notifications each app user receives per day. If you want to override these settings for an important campaign, you can select the *Don’t apply global campaign limits to this campaign* checkbox.

You can also click the *Advanced* checkbox to specify *Do Not Disturb* (DND) hours during which notifications from this push campaign are prevented from going out, either by discarding them or delaying delivery after DND hours, such as 9 PM to 9 AM.

Since past behavior campaigns can have scheduled times, you have the option to stop a campaign delivery after a certain cut-off time, or even deliver at the specified time in the user’s timezone. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

<Image title="Delivery Preferences Settings" alt={777} align="center" border={true} src="https://files.readme.io/ac20918-Campaign_Adwords_delivery_preferences.png">
  Configure the Delivery Preferences
</Image>

> 📘 Recurring Day
>
> If you specify a recurring day for a campaign such as the 7th of each month, then the campaign will start for the specified day and ignore the creation date. This is a precaution to avoid sending a campaign unintentionally on a prior date.

## Publish Campaign

After testing and previewing the appearance of your campaign, finalize your campaign by clicking **Publish Campaign**.

<Image title="Campaign Publish Page" alt={1193} align="center" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png">
  Publish Campaign
</Image>
