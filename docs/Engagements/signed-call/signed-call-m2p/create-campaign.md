---
title: Create Campaign
excerpt: Learn how to create a Signed Call™ campaign using the CleverTap dashboard
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
> 📘 Private Beta
>
> Currently, this feature is a Private ![BETA](https://files.readme.io/7776b09-Beta.svg) Release. If you want access to this feature, contact your Account Manager.

## Create a New Campaign

To create a new Signed Call™ campaign:

1. From the dashboard, select *Campaigns*.
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select **Signed Call** 

<Image alt="Create a Signed Call Campaign" align="center" border={true} src="https://files.readme.io/ea82a2f-Signed_Call_Campaign.png">
  Create a Signed Call Campaign
</Image>

The Campaign page displays.

Define all the sections and publish the campaign. 

> 📘 Qualification Criteria
>
> The Signed Call campaigns are currently based on Past behavior/Custom list. It means that the users will qualify based on an activity they performed or have been performing in the past, for example **check-out**.

## Define the Audience

Under the *Who* section, you must define the target audience for your Signed Call campaign.

<Image align="center" className="border" border={true} src="https://files.readme.io/73c0311-Signed_Call_Who.png" />

### Filter Users Based on Past Behavior

You can target users basis their past behavior. For example, you might want to target customers who installed the app, launched the app, and viewed a specific product but did not make a purchase.

### Filter by User Properties

Using the *With user properties* filter in the *Who* section, you can segment your campaign only to reach users who meet specific criteria. 

For example, you can create a Signed Call campaign to target users based in Mumbai.

<Image title="Filter on Past Behaviour and User Properties" alt={2088} align="center" border={true} src="https://files.readme.io/bc728e4-sc_user_property.png">
  Define the Target Audience
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
        Custom [user profile properties](doc:user-profiles#section-user-profile-data-model) that you define and send to CleverTap.
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
        User's exact location. You can select a city, and then define the target radius. You can also select multiple cities. You can send this information using CleverTap's SDK. For more information, refer to this [document](https://developer.clevertap.com/docs/concepts-user-profiles#user-location-handling).
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
  </tbody>
</Table>

To know more about what segments can be used, refer to [Segments](doc:segments).

### Control Group

You can define the control group to compare and measure your campaign results. For more information, refer to [Control Groups](doc:control-groups).

<Image title="Control Group and Target Cap" alt="Define Control Group" align="center" border={true} src="https://files.readme.io/2feef06-Control_Group_and_Target_Cap.png">
  Define Control Group
</Image>

### Targeting Cap

You can limit the number of users receiving the calls. 

A relevant use case is a limited offer where you want to distribute a fixed number of coupon codes. If the total reach for your campaign exceeds the number of coupon codes you can distribute, then you can limit the number of users who will receive the message to precisely the number of coupons you want to distribute.

> 📘 Campaign Limit
>
> Ensure that you set up a limit of 100 or more, regardless of the qualified user segment size. If the limit specified is less than 100, an error occurs.

## Creating Signed Call Campaigns

Click **Go to Editor** to select the voice campaign template of your choice. For more information, refer to the [Signed Call Editor](https://staging.docs.user.clevertap.net/docs/signed-call-editor) document.

## Define the Campaign Schedule

Under the *When* section, you need to define the Signed Call campaign schedule. Schedule the call campaign for the desired date and time as shown in the image below:

<Image title="Define the Campaign Schedule" alt={1680} align="center" width="80%" border={true} src="https://files.readme.io/55ab405-When_SC.png">
  Define the Campaign Schedule
</Image>

### Delivery preferences

Under the *Delivery preferences* section, defining the Do Not Disturb (DND) days and hours is mandatory. The calls scheduled during DND time are discarded by default.

You must also define a cut-off time, after which the campaign automatically stops calling the qualified end users.

<Image align="center" className="border" border={true} src="https://files.readme.io/4c27a77-SC_Delivery_preferrences.png" />

## Publish Campaign

As a final step, review your overall campaign summary and click **Publish Campaign**. Upon final confimation, you must agree on the disclaimer and click **Publish**.

<Image title="Publish Campaign" alt={1193} align="center" className="border" border={true} src="https://files.readme.io/b521e92-campaign_Publish.png" />

> 🚧 Telecom Compliance
>
> It's mandatory to confirm your compliance with telecom regulations specific to each region's time zones. CleverTap will not be responsible for any legal or compliance breach.
