---
title: Mixpanel Import
excerpt: Understand how to import cohorts from Mixpanel
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
> 📘 Feature in Beta
>
> This feature is released in private Beta. To enable this feature at your end, contact your CleverTap Customer Success Team or Mixpanel Support Team.

# Overview

Mixpanel integration enables the following capabilities:

* Import Mixpanel cohorts to CleverTap dashboard
* Engage with users from the imported cohort by using Campaigns and Journeys in the CleverTap dashboard
* Export campaign events to Mixpanel for further analysis. For more information, refer to [Mixpanel Export](doc:mixpanel-export).

When exporting cohorts from Mixpanel, the Partner Sync event is raised and cohorts are exported as segments in CleverTap. The user from the CleverTap dashboard can then engage with the segment and export the engagement events data to Mixpanel for further analysis.

# Prerequisites

The following are the prerequisites for Mixpanel Import:

1. Integrate CleverTap SDK and set `$CleverTap_user_id` in Mixpanel using Mixpanel SDK methods or APIs. For more information, refer to [Set Common User Identifier between CleverTap and Mixpanel](https://docs.clevertap.com/docs/mixpanel-integration#set-common-user-identifier-between-clevertap-and-mixpanel).
2. [Enable Mixpanel Integration](https://docs.clevertap.com/docs/mixpanel-integration#enable-mixpanel-integration).

> 📘 Mixpanel Project Admin
>
> You must be a Mixpanel project admin to enable the CleverTap integration from the Mixpanel dashboard. For more information, see [Project Roles and Permissions – Mixpanel Help Center](https://help.mixpanel.com/hc/en-us/articles/360024613412).

# Set Common User Identifier between CleverTap and Mixpanel

A common identifier is used to match users between Mixpanel and CleverTap. For more information about matching user profiles, refer to [User Identity Management](https://docs.clevertap.com/docs/mixpanel-integration#user-identity-management). The common user identifier is set up in the following two ways:  

## Using SDK Methods

The value that is passed in `$CleverTap_user_id` should be the same as passed in `mixpanel.identify` (“123456”)

```java Android
// Sets user "$CleverTap_user_id" attribute to "123"
mixpanel.getPeople().set("$CleverTap_user_id", "123");

// replace the value of $CleverTap_user_id with the User Identity value set in 
// CleverTap SDK for the profile and not the CleverTap ID.
```
```swift iOS - Swift
// Sets user "$CleverTap_user_id" attribute to "123"
Mixpanel.mainInstance().people.set(properties: [ "$CleverTap_user_id":"123"])
```
```c iOS - Objective-C
// Sets user $CleverTap_user_id attribute to "123"
[mixpanel.people set:@{@"$CleverTap_user_id": @"123"}];
```
```javascript
// Sets user $CleverTap_user_id attribute to "123"
mixpanel.people.set({
'$CleverTap_user_id': '123'
});
```

## Using Mixpanel APIs

The Value that is passed in `$CleverTap_user_id` should be the same as passed in `$distinct_id`.

```curl
curl --request POST \
     --url 'https://api.mixpanel.com/engage#profile-set' \
     --header 'Accept: text/plain' \
     --header 'Content-Type: application/x-www-form-urlencoded' \
     --data 'data={
    "$token": "YOUR_PROJECT_TOKEN",
    "$distinct_id": "13793",
    "$ip": "123.123.123.123",
    "$set": {
          "$CleverTap_user_id": "123"
    }
}

// replace the value of $CleverTap_user_id with the User Identity value set in 
// CleverTap for the profile.
```

# Enable CleverTap Integration

To enable the integration:

1. Click the ![data](https://files.readme.io/1f692f3-Data_icon.png) icon in the top navigation bar and then select Integrations.

<Image title="MIxpanel dashboard.png" alt={1834} className="border" border={true} src="https://files.readme.io/c2d85a0-MIxpanel_dashboard.png" />

2. From the *Integrations* page, select *CleverTap* and then click **Connect**.
3. Enter the following project details to authorize the connection. These details are obtained by navigating to the *Settings* page of the CleverTap dashboard.

   * *Project ID* 
   * *Passcode* 
   * *Region*

   To identify the region of your account, check the URL of your CleverTap account.

<Image title="Project details_CT.png" alt={2728} className="border" border={true} src="https://files.readme.io/85d119d-Project_details_CT.png" />

   Refer to the following table to identify the region for your account:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        CleverTap Dashboard URL
      </th>

      <th>
        Region
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        [https://eu1.dashboard.clevertap.com/login.html#/](https://eu1.dashboard.clevertap.com/login.html#/)
      </td>

      <td>
        EU
      </td>
    </tr>

    <tr>
      <td>
        [https://in1.dashboard.clevertap.com/login.html#/](https://in1.dashboard.clevertap.com/login.html#/)
      </td>

      <td>
        India
      </td>
    </tr>

    <tr>
      <td>
        [https://us1.dashboard.clevertap.com/login.html#/](https://us1.dashboard.clevertap.com/login.html#/)
      </td>

      <td>
        US
      </td>
    </tr>

    <tr>
      <td>
        [https://sg1.dashboard.clevertap.com/login.html#/](https://sg1.dashboard.clevertap.com/login.html#/)
      </td>

      <td>
        Singapore
      </td>
    </tr>
  </tbody>
</Table>

After establishing the connection successfully, the CleverTap integration displays a “Connected” tag (see figure below).

<Image title="Connected.png" alt={2978} className="border" border={true} src="https://files.readme.io/aad5be9-Connected.png" />

# Import Cohorts

> 📘 Verify User Identification
>
> To ensure that the user profiles imported from Mixpanel are correctly identified in CleverTap, we recommend importing a smaller cohort before proceeding with larger cohorts.

To import cohorts from Mixpanel:

1. Navigate to Cohorts from the Mixpanel dashboard by clicking **Cohorts** under *Users* in the navigation bar.
2. Select the cohort that you want to export and then click on the ![ellipses](https://files.readme.io/770400c-Ellipses.png) icon to the right side of the cohort.
3. Select *Export to* > *CleverTap*.

<Image title="Export to clevertap.png" alt={4096} className="border" border={true} src="https://files.readme.io/0e0fb35-Export_to_clevertap.png" />

4. Select one of the following sync types and then click **Start Sync**:

* **One-time Sync**\
  In the case of one-time sync, Mixpanel sends a one-time list of users who are currently part of the cohort to CleverTap. The cohort name defined in the Mixpanel dashboard appears as the segment under the *Segment* list page of the CleverTap dashboard.

* **Dynamic Sync**\
  In the case of dynamic sync, Mixpanel initiates sync between a cohort and CleverTap every **15 minutes**. The imported segment is updated every **15 minutes** to reflect the most recent list of users in the segment. The cohort name defined in the Mixpanel dashboard appears as the segment under the *Segment* list page of the CleverTap dashboard.

> 📘 Delay in Sync Initialization
>
> The sync initialization from Mixpanel may take  **up to 15 minutes** to start exporting users after it is enabled from the Mixpanel dashboard.

> 📘 Mixpanel Cohort Sync
>
> Every dynamic cohort sync from Mixpanel includes only the users added or removed from the cohort after the last sync.

# User Identity Management

Mixpanel exports only identified users to other partners, such as CleverTap. When receiving segments from Mixpanel, the user identity is matched in the following manner:

* If the `$CleverTap_user_id` is present, it is matched with the identity value of all the users present in CleverTap. If a match is found, the profile becomes part of the segment.
* If the $CleverTap\_user\_id\` is not present or does not match with a user profile in CleverTap, then a new user profile is created and becomes part of the segment.

Refer to the following scenarios to understand how profiles are merged to become a part of the segment in Clevertap.

* **Scenario 1:`$CleverTap_user_id` is not defined for user identified in the Mixpanel platform**\
  If the`$CleverTap_user_id` for User A is not set for a Mixpanel profile (identified) and `mixpanel_distinct_id` = 123456, the *Partner Sync* event is raised with Identity = 123456 in the CleverTap platform.  

* **Scenario 2:`$CleverTap_user_id` and `mixpanel_distinct_id` is  defined for the user in the Mixpanel**\
  If the `$CleverTap_user_id` for User A = 123456 and `mixpanel_distinct_id` = 986791, the Partner Sync event is raised with Identity = 123456 (`$CleverTap_user_id`) in the CleverTap platform.

# Additional User Properties

During Mixpanel cohort export, Mixpanel may also send the Email and Phone numbers of the users to CleverTap when available. These user profile properties are also updated in the Clevertap system user property (email and phone number).

# View Segment

The exported Mixpanel cohort is displayed under the *Segments* list page in the CleverTap dashboard. The *Type* column under the *Segments* list page for the exported cohort is displayed as *Partner - Mixpanel*. 

<Image title="Mixpanel - Partner Segment.png" alt={2376} className="border" border={true} src="https://files.readme.io/23f72f0-Mixpanel_-_Partner_Segment.png" />

Click the segment to view the statistics for this segment like any other segment on the CleverTap dashboard.

<Image title="Mixpanel Segment Stats.png" alt={2370} className="border" border={true} src="https://files.readme.io/5b390f9-Mixpanel_Segment_Stats.png" />

# Use Partner - Mixpanel Segment for Segmentation

You can also engage with the cohorts imported from Mixpanel by creating different campaigns and journeys.\
The process of creating campaigns for Past Behavior Segment and Live Behavior Segment is the same except where we need to select the segment.

## Select Segment for Past Behavior Campaigns/Journeys

To select the segment:

1. From the dashboard, select **Campaigns**. 
2. Click **+ Campaign**.
3. From the Messaging Channels list, select the messaging channel.
4. Click **Who** and filter the target audience by selecting *With User Properties* > *Segments*.
5. Select the imported user segment from the available list of segments.

<Image title="Filtering Mixpanel Segments.png" alt={4316} className="border" border={true} src="https://files.readme.io/fe5ea72-Filtering_Mixpanel_Segments.png" />

**Scenario: Customer wants to send an In-App Message campaign to the user from Bangalore city when they launch the mobile application.** 

In this case, the customer will create a cohort in the Mixpanel dashboard and initiate a one-time export to CleverTap for engagement activities. On the CleverTap dashboard, the customer will create an In-App campaign for this cohort of users. To create the campaign, the customer will navigate to In-App Campaign and select the segment under the **Who** segment section in the following way:

1. Select **App Launched** event under *As soon as the user does* section.
2. Select *Filter on past behavior and user properties* checkbox.
3. Select *With user properties* > *Segments* and then select the segment name from the list.

## Select Segment for Live Campaigns/Journeys

To select the segment:

1. From the dashboard, select **Campaigns**. 
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select the messaging channel.
4. Click **Who** and then select *Partner Sync* event from the list.
5. Click *Filter* and then select *Event Property Action* = Added.

> 📘 Partner Sync Event
>
> The *Partner Sync* event is raised every time CleverTap receives a cohort sync request from Mixpanel. This event is raised for each user in the cohort sync.

6. Filter the target audience by selecting **Segments** under *With User Properties*.
7. Select the imported user segment from the available list of segments.

<Image title="Filtering Mixpanel Live Behavior Segment.png" alt={2660} className="border" border={true} src="https://files.readme.io/2a81f5f-Filtering_Mixpanel_Live_Behavior_Segment.png" />

**Scenario: Customer wants to send a recurring Email campaign to the users that added an item to the cart but did not purchase the item.**\
In this case, the customer will create a cohort in the Mixpanel dashboard and initiate a recurring export to CleverTap for engagement activities. On the CleverTap dashboard, the customer will create a recurring Email campaign for this cohort of users. To create the campaign, the customer will navigate to Email Campaign and create the campaign in the following way:

1. Select *Start here* > *Live Behavior*.
2. Select **Partner Sync** event under *As soon as the user does* section.
3. Click *Filter* and then select Event Property *Action* = *Added*.
4. Select *Filter on past behavior and user properties* checkbox.
5. Select *Segments* under *With user properties* and then select the segment name from the list.

## Use Partner-Mixpanel Segment in Find People

To find the Partner-Mixpanel Segment:

1. Navigate to Segments > Find People from the CleverTap dashboard.
2. Select **Partner Sync** event from the *Users who did* section.
3. Select *Segments* under *Display common properties such as* and select the segment name from the list.

<Image title="Find People - Mixpanel Segment.png" alt={2724} className="border" border={true} src="https://files.readme.io/e04b5d1-Find_People_-_Mixpanel_Segment.png" />

# Partner Sync Event

The *Partner Sync* event is raised for all the users who are part of the Mixpanel cohort. The following table provides information about the properties of the event:

<Table align={["left","left","left"]}>
  <thead>
    <tr>
      <th>
        Property Name
      </th>

      <th>
        Description
      </th>

      <th>
        Property Value/Example
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Partner Segment Name
      </td>

      <td>
        Indicates the name of the cohort exported from Mixpanel
      </td>

      <td>
        For example, Cart Drop off
      </td>
    </tr>

    <tr>
      <td>
        Action
      </td>

      <td>
        Indicates if the user has been added or removed from the segment in CleverTap dashboard
      </td>

      <td>
        * Added
        * Removed
      </td>
    </tr>

    <tr>
      <td>
        Partner Segment ID
      </td>

      <td>
        Indicates the Cohort ID in the Mixpanel dashboard
      </td>

      <td>
        For example, 1638361188
      </td>
    </tr>

    <tr>
      <td>
        CT Source
      </td>

      <td>
        Indicates the source of event
      </td>

      <td>
        Mixpanel
      </td>
    </tr>

    <tr>
      <td>
        Partner Name
      </td>

      <td>
        Indicates the name of the partner
      </td>

      <td>
        Mixpanel
      </td>
    </tr>
  </tbody>
</Table>

> 📘 Campaign Exceptions for Partner Sync Event
>
> The *Partner Sync* event cannot be used as a trigger event to create the campaigns for the following channels as it is not an SDK event:
>
> * In-App Messages
> * Web Popup
> * Web Exit Intent
> * App Inbox
> * Native Display

> 📘 Contribution towards Billing
>
> The Partner Sync event contributes to data points for MAU Billing Type and as an event for Container Billing Type.

# Troubleshooting

This section provides information about common errors/problems faced during Mixpanel Import.

**Problem: The cohort does not display on the CleverTap dashboard even after successfully connecting the CleverTap account from the Mixpanel dashboard.**

Resolution: Ensure that the following details are correctly entered when connecting the CleverTap account:  

* CT Account ID 
* Passcode
* Region

<Image title="CT Project Details.png" alt={1660} className="border" border={true} src="https://files.readme.io/092a85c-CT_Project_Details.png" />

For more information about identifying the region of your account, refer to [Enable Integration](https://docs.clevertap.com/docs/mixpanel-integration#:~:text=Refer%20to%20the%20following%20table%20to%20identify%20the%20region%20for%20your%20account%3A).
