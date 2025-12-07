---
title: In-app backlog
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
## Troubleshooting and FAQ

## Overview

The selection of different segments such as Custom list segment and Past Behaviour segments is not available in the in-app notification campaigns because In-app is a live triggering action campaign that requires the user to do the qualifying event at the present time to enter into the campaign and receive the in-app notification. 

This can be solved via Journeys. By using the entry for the engagement node as the required segment

![1648](https://files.readme.io/ec8ee47-1_Journeys.png "1 Journeys.png")

![1610](https://files.readme.io/7f60601-2_Journeys.png "2 Journeys.png")

# Use Case

Send in-app notification when the user launches the app stating there are new arrivals. The navigation button can consist of a deep link to the page of the new arrivals.

![900](https://files.readme.io/568e1bf-3_Use_case.png "3 Use case.png")

## Target different segments such as Custom list segment and Past Behaviour segments in the in-app notification campaigns {user["Sunil to Add this to backlog. Needs more input. and review"]}

The selection of different segments such as the *Custom list* and *Past Behaviour* is not available in the in-app notification campaigns. In-app is a live triggering action campaign that requires the user to perform the qualifying event to enter into the campaign and receive the in-app notification. 

This issue can be solved via Journeys. By using the entry for the engagement node as the required segment

<Image title="in-app_journey_past_behavior.png" alt={733} src="https://files.readme.io/51c87c3-in-app_journey_past_behavior.png">
  Past Behavior Entry Node
</Image>

<Image title="in-app_journey_inaction_entry.png" alt={853} src="https://files.readme.io/538bb69-in-app_journey_inaction_entry.png">
  Inaction Entry Node
</Image>

## Use Case {user["Sunil to Add this to backlog. Needs more input. and review"]}

Send in-app notification when the user launches the app stating there are new arrivals. The navigation button can consist of a deep link to the page of the new arrivals.

<Image title="3 Use case.png" alt={900} width="smart" src="https://files.readme.io/568e1bf-3_Use_case.png" />

## Q. My partial user base is on an old SDK, and the rest are on new. How do I send them the same campaign? {user["Sunil to Add this to backlog. Needs more input. and review"]}

* To send a campaign, you will have to pick the legacy option.
* This will open two variants of the campaign.
* The *New In-App* will send the campaign to users on SDK version 3.3.0 and above.
* The *Legacy In-App* will send the campaign to users on SDK version 3.2.x and below.
* This legacy option will be available until March 31, 2019, and deprecates after this date.\
  \<\<@dk does this apply now ?>>

## Q. Why does In-app not work on API events?

The In-app should be triggered only on the SDK events. In-apps require the user to be present on the application. Therefore, the in-app campaigns do not work on an event that is triggered via API. Additionally, events from API may not be in real-time, and hence the trigger will not work.

## Q. Can multiple in-app campaigns run on the same triggering event?  {user["Sunil to Add this to backlog. Needs more input. and review"]}

 There should not be more than one in-app campaign on the same triggering event, as it creates a race condition between the campaigns and then sends any random campaign to the user.

## Q. What are the text and image specifications for in-app campaigns in each template? {user["Sunil to add this. to Create message section"]}

Text limit:

* Selected template - Header: Title [22 Characters], Message [75 Characters]\* 
* Selected template - Half Interstitial: Title [25 Characters], Message [100 Characters]
* Selected template - Interstitial: Title [20 Characters], Message [75 Characters]
* Selected template - Header: Title [30 Characters], Message [128 Characters]
* Selected template - Header: Title [22 Characters], Message [75 Characters]

For image specifications, refer to \[template aspect ratio and image size guide]  ([https://docs.clevertap.com/docs/inapp-campaigns#section-template-aspect-ratio-and-image-size-guide](https://docs.clevertap.com/docs/inapp-campaigns#section-template-aspect-ratio-and-image-size-guide)).

## Q. I need to send crisp template campaigns. Do I need to update my SDK? {user["Sunil to Add this to backlog. Needs more input. and review"]}

* Yes, the new and improved templates only work with SDK version 3.3.0 and above.
* You cannot send these campaigns on SDK versions below that.
