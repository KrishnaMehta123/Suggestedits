---
title: Recommended Delay for Inaction Campaigns
excerpt: Understand how to send delayed messages on Users' inaction.
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
      title: Regex
      url: https://docs.clevertap.com/docs/regex_c20
    - type: link
      title: Best Time
      url: https://docs.clevertap.com/docs/best-time_c20
    - type: link
      title: Constant Event Property
      url: https://docs.clevertap.com/docs/constant-property_c20
    - type: link
      title: Geofencing
      url: https://docs.clevertap.com/docs/geofencing_c20
    - type: link
      title: API
      url: https://docs.clevertap.com/docs/api-campaigns_c20
    - type: link
      title: Campaign Reports
      url: https://docs.clevertap.com/docs/campaign-reports_c20
---
# Overview

*Recommended Delay* is a feature that recommends the best time to send a message for an inaction campaign which is designed to engage users who do not do a certain action. 

# Use Cases

First Scenario: Nudge users who install your app (action) but do not purchase something within a two-hour (inaction) timeframe.  Here, the two-hour gap is selected based on manual analytics. Using the *Recommend Delay* feature, you can let CleverTap automatically decide the golden period within which the user should have purchased and then send out a message to re-engage users who do not purchase within that period.

Second Scenario: The average time it takes a user to add an item to their cart (action 1) and then checkout (action 2) is five minutes. If the user has not completed the checkout process within five minutes of adding the item to their cart (inaction), then the likelihood that a user will check out drops substantially. If you use the *Recommended Delay* feature, we will recommend the best time to wait before you send a notification to the user if they have not completed the checkout process.

# How It Works

CleverTap creates this recommendation by calculating the average time users take to convert from one action to another action. 

Beyond this average time, the likelihood that a user completes the second action drops substantially; however, if you send a message to the user at that point, you can increase the conversion rate for the second action.

# Create an Inaction Campaign

To create an inaction campaign:

1. From the dashboard, navigate to *Campaigns*. 
2. Click **+ Campaign**.
3. Select a messaging channel.

<Image title="2x Create a campaign.png" alt={1571} className="border" border={true} src="https://files.readme.io/5de46d2-2x_Create_a_campaign.png" />

4. Under *Start here* > *Qualification Criteria*, select *Live Behavior*. 
5. Click **Done**.

<Image title="Qualification_Criteria.png" alt={758} className="border" border={true} src="https://files.readme.io/fdcf0e8-Qualification_Criteria.png" />

7. Under the *Set a goal* section, select *Conversion Tracking*.
8. Select event properties, conversion time, and revenue property.
9. Click **Done**.

<Image title="Set_Goal.png" alt={354} className="border" border={true} src="https://files.readme.io/791e6d3-Set_Goal.png" />

10. Navigate to *Who* > *Target Segment*.
11. Under *Find users from segment*, select **Inaction**
12. Click **or find best delay**.

<Image title="Find_best_delay.png" alt={854} className="border" border={true} src="https://files.readme.io/05b40cc-Find_best_delay.png" />
