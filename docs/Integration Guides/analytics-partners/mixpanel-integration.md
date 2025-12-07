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
[block:callout]
{
  "type": "info",
  "title": "Feature in Beta",
  "body": "This feature is released in private Beta. To enable this feature at your end, contact your CleverTap Customer Success Team or Mixpanel Support Team."
}
[/block]

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
[block:callout]
{
  "type": "info",
  "body": "You must be a Mixpanel project admin to enable the CleverTap integration from the Mixpanel dashboard. For more information, see [Project Roles and Permissions – Mixpanel Help Center](https://help.mixpanel.com/hc/en-us/articles/360024613412).",
  "title": "Mixpanel Project Admin"
}
[/block]
# Set Common User Identifier between CleverTap and Mixpanel
A common identifier is used to match users between Mixpanel and CleverTap. For more information about matching user profiles, refer to [User Identity Management](https://docs.clevertap.com/docs/mixpanel-integration#user-identity-management). The common user identifier is set up in the following two ways:  

## Using SDK Methods
The value that is passed in `$CleverTap_user_id` should be the same as passed in `mixpanel.identify` (“123456”)
[block:code]
{
  "codes": [
    {
      "code": "// Sets user \"$CleverTap_user_id\" attribute to \"123\"\nmixpanel.getPeople().set(\"$CleverTap_user_id\", \"123\");\n\n// replace the value of $CleverTap_user_id with the User Identity value set in \n// CleverTap SDK for the profile and not the CleverTap ID.\n",
      "language": "java",
      "name": "Android"
    },
    {
      "code": "// Sets user \"$CleverTap_user_id\" attribute to \"123\"\nMixpanel.mainInstance().people.set(properties: [ \"$CleverTap_user_id\":\"123\"])\n",
      "language": "swift",
      "name": "iOS - Swift"
    },
    {
      "code": "// Sets user $CleverTap_user_id attribute to \"123\"\n[mixpanel.people set:@{@\"$CleverTap_user_id\": @\"123\"}];\n",
      "language": "c",
      "name": "iOS - Objective-C"
    },
    {
      "code": "// Sets user $CleverTap_user_id attribute to \"123\"\nmixpanel.people.set({\n'$CleverTap_user_id': '123'\n});\n",
      "language": "javascript",
      "name": null
    }
  ]
}
[/block]
## Using Mixpanel APIs
The Value that is passed in `$CleverTap_user_id` should be the same as passed in `$distinct_id`.
[block:code]
{
  "codes": [
    {
      "code": "curl --request POST \\\n     --url 'https://api.mixpanel.com/engage#profile-set' \\\n     --header 'Accept: text/plain' \\\n     --header 'Content-Type: application/x-www-form-urlencoded' \\\n     --data 'data={\n    \"$token\": \"YOUR_PROJECT_TOKEN\",\n    \"$distinct_id\": \"13793\",\n    \"$ip\": \"123.123.123.123\",\n    \"$set\": {\n          \"$CleverTap_user_id\": \"123\"\n    }\n}\n\n// replace the value of $CleverTap_user_id with the User Identity value set in \n// CleverTap for the profile.\n",
      "language": "curl"
    }
  ]
}
[/block]
# Enable CleverTap Integration

To enable the integration:
1. Click the ![data](https://files.readme.io/1f692f3-Data_icon.png) icon in the top navigation bar and then select Integrations.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c2d85a0-MIxpanel_dashboard.png",
        "MIxpanel dashboard.png",
        1834,
        1104,
        "#e8e7f6"
      ],
      "border": true
    }
  ]
}
[/block]
2. From the *Integrations* page, select *CleverTap* and then click **Connect**.
3. Enter the following project details to authorize the connection. These details are obtained by navigating to the *Settings* page of the CleverTap dashboard.
    * *Project ID* 
    * *Passcode* 
    * *Region*

    To identify the region of your account, check the URL of your CleverTap account.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/85d119d-Project_details_CT.png",
        "Project details_CT.png",
        2728,
        852,
        "#f8f8f9"
      ],
      "border": true
    }
  ]
}
[/block]
   Refer to the following table to identify the region for your account:
[block:parameters]
{
  "data": {
    "h-0": "CleverTap Dashboard URL",
    "h-1": "Region",
    "0-0": "https://eu1.dashboard.clevertap.com/login.html#/",
    "1-0": "https://in1.dashboard.clevertap.com/login.html#/",
    "2-0": "https://us1.dashboard.clevertap.com/login.html#/",
    "3-0": "https://sg1.dashboard.clevertap.com/login.html#/",
    "0-1": "EU",
    "1-1": "India",
    "2-1": "US",
    "3-1": "Singapore"
  },
  "cols": 2,
  "rows": 4
}
[/block]
After establishing the connection successfully, the CleverTap integration displays a “Connected” tag (see figure below).
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/aad5be9-Connected.png",
        "Connected.png",
        2978,
        762,
        "#f9f8f8"
      ],
      "border": true
    }
  ]
}
[/block]
# Import Cohorts
[block:callout]
{
  "type": "info",
  "body": "To ensure that the user profiles imported from Mixpanel are correctly identified in CleverTap, we recommend importing a smaller cohort before proceeding with larger cohorts.",
  "title": "Verify User Identification"
}
[/block]
To import cohorts from Mixpanel:

1. Navigate to Cohorts from the Mixpanel dashboard by clicking **Cohorts** under *Users* in the navigation bar.
2. Select the cohort that you want to export and then click on the ![ellipses](https://files.readme.io/770400c-Ellipses.png) icon to the right side of the cohort.
3. Select *Export to* > *CleverTap*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0e0fb35-Export_to_clevertap.png",
        "Export to clevertap.png",
        4096,
        1910,
        "#eae9f5"
      ],
      "border": true
    }
  ]
}
[/block]
4. Select one of the following sync types and then click **Start Sync**:

* **One-time Sync**
In the case of one-time sync, Mixpanel sends a one-time list of users who are currently part of the cohort to CleverTap. The cohort name defined in the Mixpanel dashboard appears as the segment under the *Segment* list page of the CleverTap dashboard.

* **Dynamic Sync**
In the case of dynamic sync, Mixpanel initiates sync between a cohort and CleverTap every **15 minutes**. The imported segment is updated every **15 minutes** to reflect the most recent list of users in the segment. The cohort name defined in the Mixpanel dashboard appears as the segment under the *Segment* list page of the CleverTap dashboard.

[block:callout]
{
  "type": "info",
  "body": "The sync initialization from Mixpanel may take  **up to 15 minutes** to start exporting users after it is enabled from the Mixpanel dashboard.",
  "title": "Delay in Sync Initialization"
}
[/block]

[block:callout]
{
  "type": "info",
  "body": "Every dynamic cohort sync from Mixpanel includes only the users added or removed from the cohort after the last sync.",
  "title": "Mixpanel Cohort Sync"
}
[/block]
# User Identity Management
Mixpanel exports only identified users to other partners, such as CleverTap. When receiving segments from Mixpanel, the user identity is matched in the following manner:

* If the `$CleverTap_user_id` is present, it is matched with the identity value of all the users present in CleverTap. If a match is found, the profile becomes part of the segment.
* If the $CleverTap_user_id` is not present or does not match with a user profile in CleverTap, then a new user profile is created and becomes part of the segment.

Refer to the following scenarios to understand how profiles are merged to become a part of the segment in Clevertap.

* **Scenario 1: `$CleverTap_user_id` is not defined for user identified in the Mixpanel platform**
If the`$CleverTap_user_id` for User A is not set for a Mixpanel profile (identified) and `mixpanel_distinct_id` = 123456, the *Partner Sync* event is raised with Identity = 123456 in the CleverTap platform.  

* **Scenario 2: `$CleverTap_user_id` and `mixpanel_distinct_id` is  defined for the user in the Mixpanel**
If the `$CleverTap_user_id` for User A = 123456 and `mixpanel_distinct_id` = 986791, the Partner Sync event is raised with Identity = 123456 (`$CleverTap_user_id`) in the CleverTap platform.

# Additional User Properties
During Mixpanel cohort export, Mixpanel may also send the Email and Phone numbers of the users to CleverTap when available. These user profile properties are also updated in the Clevertap system user property (email and phone number).

# View Segment
The exported Mixpanel cohort is displayed under the *Segments* list page in the CleverTap dashboard. The *Type* column under the *Segments* list page for the exported cohort is displayed as *Partner - Mixpanel*. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/23f72f0-Mixpanel_-_Partner_Segment.png",
        "Mixpanel - Partner Segment.png",
        2376,
        1170,
        "#f7f8f8"
      ],
      "border": true
    }
  ]
}
[/block]
Click the segment to view the statistics for this segment like any other segment on the CleverTap dashboard.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5b390f9-Mixpanel_Segment_Stats.png",
        "Mixpanel Segment Stats.png",
        2370,
        2114,
        "#f6f8fc"
      ],
      "border": true
    }
  ]
}
[/block]
# Use Partner - Mixpanel Segment for Segmentation

You can also engage with the cohorts imported from Mixpanel by creating different campaigns and journeys. 
The process of creating campaigns for Past Behavior Segment and Live Behavior Segment is the same except where we need to select the segment.

## Select Segment for Past Behavior Campaigns/Journeys
To select the segment:
1. From the dashboard, select **Campaigns**. 
2. Click **+ Campaign**.
3. From the Messaging Channels list, select the messaging channel.
4. Click **Who** and filter the target audience by selecting *With User Properties* > *Segments*.
6.  Select the imported user segment from the available list of segments.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fe5ea72-Filtering_Mixpanel_Segments.png",
        "Filtering Mixpanel Segments.png",
        4316,
        2356,
        "#f8f8fa"
      ],
      "border": true
    }
  ]
}
[/block]
**Scenario: Customer wants to send an In-App Message campaign to the user from Bangalore city when they launch the mobile application.** 

In this case, the customer will create a cohort in the Mixpanel dashboard and initiate a one-time export to CleverTap for engagement activities. On the CleverTap dashboard, the customer will create an In-App campaign for this cohort of users. To create the campaign, the customer will navigate to In-App Campaign and select the segment under the **Who** segment section in the following way:
1. Select **App Launched **event under *As soon as the user does* section.
2. Select *Filter on past behavior and user properties* checkbox.
3. Select *With user properties* > *Segments* and then select the segment name from the list.

## Select Segment for Live Campaigns/Journeys

To select the segment:
1. From the dashboard, select **Campaigns**. 
2. Click **+ Campaign**.
3. From the *Messaging Channels* list, select the messaging channel.
4. Click **Who** and then select *Partner Sync* event from the list.
5. Click *Filter* and then select *Event Property Action* = Added.
[block:callout]
{
  "type": "info",
  "title": "Partner Sync Event",
  "body": "The *Partner Sync* event is raised every time CleverTap receives a cohort sync request from Mixpanel. This event is raised for each user in the cohort sync."
}
[/block]
6. Filter the target audience by selecting **Segments** under *With User Properties*.
7. Select the imported user segment from the available list of segments.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2a81f5f-Filtering_Mixpanel_Live_Behavior_Segment.png",
        "Filtering Mixpanel Live Behavior Segment.png",
        2660,
        1516,
        "#f9f8fc"
      ],
      "border": true
    }
  ]
}
[/block]
**Scenario: Customer wants to send a recurring Email campaign to the users that added an item to the cart but did not purchase the item.** 
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
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e04b5d1-Find_People_-_Mixpanel_Segment.png",
        "Find People - Mixpanel Segment.png",
        2724,
        2636,
        "#f8f8f9"
      ],
      "border": true
    }
  ]
}
[/block]
# Partner Sync Event

The *Partner Sync* event is raised for all the users who are part of the Mixpanel cohort. The following table provides information about the properties of the event:
[block:parameters]
{
  "data": {
    "h-0": "Property Name",
    "h-1": "Description",
    "h-2": "Property Value/Example",
    "0-0": "Partner Segment Name",
    "1-0": "Action",
    "2-0": "Partner Segment ID",
    "3-0": "CT Source",
    "4-0": "Partner Name",
    "0-1": "Indicates the name of the cohort exported from Mixpanel",
    "0-2": "For example, Cart Drop off",
    "1-1": "Indicates if the user has been added or removed from the segment in CleverTap dashboard",
    "1-2": "* Added\n* Removed",
    "2-1": "Indicates the Cohort ID in the Mixpanel dashboard",
    "2-2": "For example, 1638361188",
    "3-1": "Indicates the source of event",
    "3-2": "Mixpanel",
    "4-1": "Indicates the name of the partner",
    "4-2": "Mixpanel"
  },
  "cols": 3,
  "rows": 5
}
[/block]

[block:callout]
{
  "type": "info",
  "body": "The *Partner Sync* event cannot be used as a trigger event to create the campaigns for the following channels as it is not an SDK event:\n* In-App Messages\n* Web Popup\n* Web Exit Intent\n* App Inbox\n* Native Display",
  "title": "Campaign Exceptions for Partner Sync Event"
}
[/block]

[block:callout]
{
  "type": "info",
  "body": "The Partner Sync event contributes to data points for MAU Billing Type and as an event for Container Billing Type.",
  "title": "Contribution towards Billing"
}
[/block]
# Troubleshooting
This section provides information about common errors/problems faced during Mixpanel Import.

**Problem: The cohort does not display on the CleverTap dashboard even after successfully connecting the CleverTap account from the Mixpanel dashboard.**
 
Resolution: Ensure that the following details are correctly entered when connecting the CleverTap account:  
* CT Account ID 
* Passcode
* Region
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/092a85c-CT_Project_Details.png",
        "CT Project Details.png",
        1660,
        1086,
        "#e2e2e9"
      ],
      "border": true
    }
  ]
}
[/block]
For more information about identifying the region of your account, refer to [Enable Integration](https://docs.clevertap.com/docs/mixpanel-integration#:~:text=Refer%20to%20the%20following%20table%20to%20identify%20the%20region%20for%20your%20account%3A).