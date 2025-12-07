---
title: Create Message
excerpt: Understand how to create a campaign for Google Adwords
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: >-
    Refer to the pages listed below to learn more about the following Google
    AdWords section:
  pages:
    - type: link
      title: Google AdWords Campaign Stats
      url: https://docs.clevertap.com/docs/google-adwords-stats_c20
    - type: link
      title: Google AdWords Troubleshooting
      url: https://docs.clevertap.com/docs/troubleshooting-google-adwords_c20
---
## Create a New Campaign

Create a campaign to deliver your Google Adwords message.\
To create a new campaign:

1. From the CleverTap dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **Adwords**. 

<Image title="Select Google Adwords.png" alt={2706} className="border" border={true} src="https://files.readme.io/4e06122-Select_Google_Adwords.png" />

The *Campaigns* page displays.

<Image title="Campaign_Adwords_main.png" alt={1026} className="border" width="80%" border={true} src="https://files.readme.io/48b0288-Campaign_Adwords_main.png" />

Define all the sections and publish the campaign.

## Start Campaign Setup

The *Start here* section displays the setup information. 

This section has the following parts:

* Start here: Displays the information for platforms such as FCM, Xiaomi, or iOS. Check that the required platforms are integrated and ready for campaigns. When the account set up is not done, the following warning message is displayed and you need to set up the account to be able to run campaigns:

<Image title="Account Setup not done.png" alt={2670} className="border" border={true} src="https://files.readme.io/91067c7-Account_Setup_not_done.png" />

When the account setup is done, the following message is displayed and you can now create a campaign:

<Image title="Account Setup done.png" alt={1510} className="border" border={true} src="https://files.readme.io/597d0f3-Account_Setup_done.png" />

* Set a goal: You can track your campaign conversion by setting up a goal. Setting a goal allows you to measure your campaign effectively against what you want to achieve with the campaign. You can define your conversion goal further by filtering an event by event properties. This selection is optional.

  The campaign goal can be as generic or as specific as you want. It can answer questions from *How many users were influenced for purchasing an X amount?* to \*How many first-time visitors purchased red shoes worth a minimum of X amount and blue jackets worth a minimum of Y amount? ". 

<Image title="Push_notification_set_goal_track_conversion.png" alt={919} className="border" border={true} src="https://files.readme.io/00215dc-Push_notification_set_goal_track_conversion.png" />

## Define the Audience

You must indicate the target audience for your Adwords campaign. You can specify your target audience from the *Target segment* section. Here, you can create a new segment or use a previously saved user segment from the *segment* list. 

For Past Behavior segments, you also calculate the *Estimated reach*.

<Image title="SMS_Who.png" alt={961} className="border" border={true} src="https://files.readme.io/5a435b7-SMS_Who.png" />

### Segment

If you want to create an ad-hoc segment, you can select a type of segment on which to base your Adwords campaign. You can create the target based on past user behavior and user properties.

On this basis, you would then set up the *Who* by choosing to send this campaign to all users who qualify or just a portion of the users who qualify under *Estimated reach*. 

### Deliver Adwords Notifications based on Past Behavior (PBS)

You can also target users their past user behavior. For past behavior campaigns, you also have an option to calculate *Estimated reach*. The estimated reach shows the number of users that qualify for the campaign criteria and the number of reachable users.

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign to only reach users who meet specific criteria. 

For example, you can send an Adwords notification to English-speaking female users who live in the United States. 

<Image title="campaigns_user_properties.png" alt={516} className="border" border={true} src="https://files.readme.io/5851a66-campaigns_user_properties.png" />

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

Now, you can set up the *What*, which is the Adwords campaign content. Click *Go To Editor* to create your message. 

### Adwords Editor

You can either append an existing audience list **or** create an audience list. Select the user details such as Email or Phone that you want to upload to this list. 

#### **Add qualified users using CleverTap**

> 🚧 Note
>
> Check that you have available CRM lists before adding users.

<Image title="Campaign_Adwords_What.png" alt={1006} className="border" border={true} src="https://files.readme.io/a4622db-Campaign_Adwords_What.png" />

#### **Create a new audience on Google using CleverTap**

<Image title="Campaign_Adwords_What_create_audience.png" alt={978} className="border" border={true} src="https://files.readme.io/082ca9c-Campaign_Adwords_What_create_audience.png" />

## Define the Campaign Schedule

You can set up the *When* to schedule the campaign start and end using the options below:

The delivery preferences for Past behavior campaigns can be set as follows:

* Send Now: Select this option to send the campaign right away.
* Schedule for later: Select this option to send the campaign on a specific date and time.
* Set as Recurring: Select this option to send the campaign at specific intervals.

<Image title="Push_notification_editor_when.png" alt={978} className="border" border={true} src="https://files.readme.io/ed19319-Push_notification_editor_when.png" />

### Delivery preferences

Global campaign limits are limits you can apply to determine how many Adwords notifications each app user receives per day. If you want to override these settings for an important campaign, you can select the *Don’t apply global campaign limits to this campaign* checkbox.

You can also click the *Advanced* checkbox to specify *Do Not Disturb* (DND) hours during which notifications from this push campaign are prevented from going out, either by discarding them or delaying delivery after DND hours, such as 9 PM to 9 AM.

Since past behavior campaigns can have scheduled times, you have the option to stop a campaign delivery after a certain cut-off time, or even deliver at the specified time in the user’s timezone. For more information, refer to [Delivery in User’s Timezone](doc:notification-delivery-options).

<Image title="Campaign_Adwords_delivery_preferences.png" alt={777} className="border" border={true} src="https://files.readme.io/ac20918-Campaign_Adwords_delivery_preferences.png" />

> 📘 Recurring Day
>
> If you specify a recurring day for a campaign such as the 7th of each month, then the campaign will start for the specified day and ignore the creation date. This is a precaution to avoid sending a campaign unintentionally on a prior date.

## Publish Campaign

After testing and previewing the appearance of your campaign, finalize your campaign by clicking **Publish Campaign**.

<Image title="campaign_Publish.png" alt={1193} className="border" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png" />
