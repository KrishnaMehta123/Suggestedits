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

1. From the dashboard, select _Campaigns_.
2. Click **+ Campaign**.
3. From the _Messaging Channels_ list, select **Signed Call** 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ea82a2f-Signed_Call_Campaign.png",
        "",
        "Create a Signed Call Campaign"
      ],
      "align": "center",
      "border": true,
      "caption": "Create a Signed Call Campaign"
    }
  ]
}
[/block]


The Campaign page displays.

Define all the sections and publish the campaign. 

> 📘 Qualification Criteria
> 
> The Signed Call campaigns are currently based on Past behavior/Custom list. It means that the users will qualify based on an activity they performed or have been performing in the past, for example **check-out**.

## Define the Audience

Under the _Who_ section, you must define the target audience for your Signed Call campaign.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/73c0311-Signed_Call_Who.png",
        "",
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


### Filter Users Based on Past Behavior

You can target users basis their past behavior. For example, you might want to target customers who installed the app, launched the app, and viewed a specific product but did not make a purchase.

### Filter by User Properties

Using the _With user properties_ filter in the _Who_ section, you can segment your campaign only to reach users who meet specific criteria. 

For example, you can create a Signed Call campaign to target users based in Mumbai.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bc728e4-sc_user_property.png",
        "Filter on Past Behaviour and User Properties",
        2088
      ],
      "align": "center",
      "border": true,
      "caption": "Define the Target Audience"
    }
  ]
}
[/block]


The following table explains the various property types:

[block:parameters]
{
  "data": {
    "h-0": "Property Type",
    "h-1": "Description",
    "h-2": "Example",
    "0-0": "User Properties",
    "0-1": "Custom [user profile properties](doc:user-profiles#section-user-profile-data-model) that you define and send to CleverTap.",
    "0-2": "Customer Type = Platinum",
    "1-0": "Demographics",
    "1-1": "Demographics filters include _Age_ and _Gender_.",
    "1-2": "Age = 25 to 40 years  \nGender = Female",
    "2-0": "Geography",
    "2-1": "User's coarse location. Filters include _Country_, _Region_, and _City_. CleverTap's SDK can automatically detect this from the user's IP address.",
    "2-2": "Country = United States  \nState = California  \nCity = San Francisco",
    "3-0": "Geography Radius",
    "3-1": "User's exact location. You can select a city, and then define the target radius. You can also select multiple cities. You can send this information using CleverTap's SDK. For more information, refer to this [document](https://developer.clevertap.com/docs/concepts-user-profiles#user-location-handling).",
    "3-2": "Locations = San Francisco, USA; Paris, France",
    "4-0": "Reachability",
    "4-1": "Reachability filters include _Has email address_, _Has phone number_, _Unsubscribed email_, and _Unsubscribed SMS_.",
    "4-2": "Unsubscribed email = No"
  },
  "cols": 3,
  "rows": 5,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


To know more about what segments can be used, refer to [Segments](doc:segments).

### Control Group

You can define the control group to compare and measure your campaign results. For more information, refer to [Control Groups](doc:control-groups).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2feef06-Control_Group_and_Target_Cap.png",
        "Control Group and Target Cap",
        "Define Control Group"
      ],
      "align": "center",
      "border": true,
      "caption": "Define Control Group"
    }
  ]
}
[/block]


### Targeting Cap

You can limit the number of users receiving the calls. 

A relevant use case is a limited offer where you want to distribute a fixed number of coupon codes. If the total reach for your campaign exceeds the number of coupon codes you can distribute, then you can limit the number of users who will receive the message to precisely the number of coupons you want to distribute.

> 📘 Campaign Limit
> 
> Ensure that you set up a limit of 100 or more, regardless of the qualified user segment size. If the limit specified is less than 100, an error occurs.

## Creating Signed Call Campaigns

Click **Go to Editor ** to select the voice campaign template of your choice. For more information, refer to the [Signed Call Editor](https://staging.docs.user.clevertap.net/docs/signed-call-editor) document.

## Define the Campaign Schedule

Under the _When_ section, you need to define the Signed Call campaign schedule. Schedule the call campaign for the desired date and time as shown in the image below:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/55ab405-When_SC.png",
        "Define the Campaign Schedule",
        1680
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Define the Campaign Schedule"
    }
  ]
}
[/block]


### Delivery preferences

Under the _Delivery preferences_ section, defining the Do Not Disturb (DND) days and hours is mandatory. The calls scheduled during DND time are discarded by default.

You must also define a cut-off time, after which the campaign automatically stops calling the qualified end users.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4c27a77-SC_Delivery_preferrences.png",
        "",
        ""
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


## Publish Campaign

As a final step, review your overall campaign summary and click **Publish Campaign**. Upon final confimation, you must agree on the disclaimer and click **Publish**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b521e92-campaign_Publish.png",
        "Publish Campaign",
        1193
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]


> 🚧 Telecom Compliance
> 
> It's mandatory to confirm your compliance with telecom regulations specific to each region's time zones. CleverTap will not be responsible for any legal or compliance breach.