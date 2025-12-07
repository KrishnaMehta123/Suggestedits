---
title: Segments
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
# Overview

A segment in CleverTap is a group of users whose actions are performed, actions are not performed, or user profile properties match a set of defined criteria. For example, a segment can be users who launched the app for the first time in the past 30 days. A more complex segment could be users who live in New York, were acquired via a Facebook campaign in April, transacted three or more times in May and June, and have not transacted in the past two weeks.

After you have identified segments of interest, you can save and then target them with any type of messaging campaign. Over time you can also trend segments to understand how a segment behaves in response to your marketing initiatives. The entire CleverTap dashboard can be filtered by any segment you create, including any of our analytics features.

# Types of Segments

There are three types of behavioral segments in CleverTap: *Past behavior* segments,  *Live* segments, and *Custom list* segments.

## Past Behavior Segments

Past behavior segments are users grouped by their actions in the past. 

You can group users based on a single activity (that is, all my users who launched the app in the past 30 days) to complex combinations of actions, inactions, and user properties.

## Live User Segments

While past behavior segments let you evaluate users based on historical criteria, live user segments allow you to track what is happening in your app right now.

When you define a set of behaviors of interest, CleverTap monitors for them as they happen in your app and immediately adds a user to a segment when their behavior matches your action criteria.

You can create live user segments for a single activity (booked a movie ticket), inaction (did not buy a movie ticket in a certain time), off of date/time properties of events, or website-related actions such as page visit, count, or referrer.

## Precomputed Segment
Precomputed segments are past behavior segments that are computed every three hours, optimizing your campaigns for speed of delivery. Using precomputed segments, you can send campaigns with minimal lag and reach out to your users immediately. After you have defined a segment, the system continues to compute this segment every three hours automatically. This lets you send out notifications without any delays to stay in touch with your users. Some use cases include:
  * Breaking news: As soon as important news breaks and you want to send a push notification to your user base, we recommend that you use precomputed segments. 
  * Score updates: As soon as an important event occurs in a match, you want to reach your customers with a push notification. You can use precomputed segments.

Some segment limits include:
  * As an enterprise customer, you are allowed to create up to 20 precomputed segments.
  * You can unmark a precomputed segment from the segment details page itself.
  * After you unmark a precomputed segment, all campaigns running now and in the future will run at a regular pace.
[block:callout]
{
  "type": "warning",
  "body": "As journeys is an orchestration platform, precomputed segments are not applicable when creating journeys.",
  "title": "Using Precomputed Segments in Journeys"
}
[/block]
## Custom List Segments
These are custom segments that you can create based on product analytics. For more information, see [Custom List Segments](https://docs.clevertap.com/docs/custom-list-segments).

## System User Segments

The following are system-defined user segments that are available for your use: 
  * **All Users**: This user segment contains all the users available to your account.
  * **Test Users**: This user segment contains the users who you can test for your campaign response. A campaign or journey can now be tested on this *Test Users* segment before it is sent to an actual segment. The *Test User* segment is available by default for engagement and UI experiences. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/eb9b8b9-1a9589c-Segment_System.png",
        "1a9589c-Segment_System.png",
        1208,
        672,
        "#f0f4f8"
      ],
      "border": true
    }
  ]
}
[/block]

# Segment List Page

The *Segments* list page shows all existing segments available for you. You can choose to do various tasks with these listed segments. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4e1fcdb-Segments_all_operations.png",
        "Segments_all_operations.png",
        1221,
        732,
        "#ecebe8"
      ],
      "caption": ""
    }
  ]
}
[/block]
# Create Segments

To create new segments, navigate to *Segments* under the *Segmentation* tab on the dashboard.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/809321d-d99e397-Screenshot_2020-06-08_at_12.12.29_PM.png",
        "d99e397-Screenshot_2020-06-08_at_12.12.29_PM.png",
        2278,
        1430,
        "#f8f9f9"
      ],
      "border": true
    }
  ]
}
[/block]
Click the **+ Segment** button.

The main segment creation page displays a list of options for types of past behavior and live user segments. Select an option based on the required segment.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a622721-Types_of_Segment.gif",
        "Types of Segment.gif",
        1246,
        594,
        "#f9fbfa"
      ],
      "border": true
    }
  ]
}
[/block]
Past Behavior segments can be based on:
  * Past user actions  ( for example, users who added a product to the cart in the past 30 days)
  * Past user action/inaction combination (for example, users who added a product to the cart but didn’t purchase in the last 30 days)
  * Past user action/inaction combination along with common user properties (for example, platinum-level users who added a product to the cart but didn’t purchase in the last 30 days)

Live User segments can add users to the segment as soon as users qualify based on the following:
  * Single action (for example, users who have added a product to the cart)
  * Inaction within time (for example, users who have added a product to the cart but did not purchase within 10 minutes of adding product to the cart)
  * On a date/time, (for example, users who have an appointment five days from today)
  * Page visit (for example, users who have visited a certain URL on your website)
  * Referrer entry (for example, users who have visited your website via a certain external referrer URL)
  * Page count (for example, users who have visited a certain number of pages on your website)


## Create Live User Segments

To create a live segment with CleverTap, choose any of the options underneath *Live user segments* from the main segment creation page.

For instance, in the current example, we will create an *Inaction within time* segment for which users will qualify in realtime, as soon as they add a product to cart but do not purchase the product within 10 minutes (the golden window within which most users transact on our iOS and Android app platforms).

Select the *Inaction within time* box, which displays the following page where you can set up the segment as follows.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2c9213f-Segments_Inaction_with_Time.png",
        "Segments_Inaction_with_Time.png",
        1197,
        439,
        "#fbfbfc"
      ],
      "border": true
    }
  ]
}
[/block]
The user can choose to check the *Filter on past user behavior and common properties* checkbox to apply past action, inaction, or common user property filters.

The next step would be to click** Save segment**, name the segment, and then see it show up in the main *Segments* menu by its name, which in this case is “Added to cart but no charge 10 mins.”  
[block:callout]
{
  "type": "info",
  "title": "Segment Naming Best Practices",
  "body": "Convey the core meaning of the segment while keeping the name brief."
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ccf346b-Segments_Created_Segment.png",
        "Segments_Created_Segment.png",
        788,
        505,
        "#f4f6f6"
      ],
      "border": true
    }
  ]
}
[/block]
### View Live User Segment Report

The top portion of the live user segment report consists of a way to first *Show segment definition* to understand its underlying query. 

There are also two graphs: 
  * One on the left-hand side showing the plot of the number of users who qualified for the segment going forward from the first complete day post-segment creation.
  * One on the right-hand side showing the real-time rate at which users are qualifying for the segment (vs. all user activity on your app/website). 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2b9ceec-Segment_Live_Segment_Report.gif",
        "Segment_Live_Segment_Report.gif",
        1218,
        658,
        "#faf9fa"
      ],
      "border": true
    }
  ]
}
[/block]
The lower portion of the live user segment report consists of a list of sample users trickling into your segment in real-time on the right-hand side. 

It also shows the reachability percentages for these users within each messaging channel on the left-hand side. 

The lower-most part of the report shows you how to do more with this segment by either filtering relevant analytics dashboard views by this particular user segment or reaching out to this segment via relevant messaging channels.

## Create Past Behavior Segments

To create a Past Behavior segment with CleverTap, choose any of the options underneath *Past behavior user segments *from the main segment creation page.

For example, we will create an *Action* based segment where users will qualify if they have applied a payment offer at least one time in the past 30 days.

Select the box *Action*, which takes you to the page where you can set up our segment as follows.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6f6d353-Segments_PSB_Create_New.png",
        "Segments_PSB_Create_New.png",
        1228,
        682,
        "#fbfcfc"
      ],
      "border": true
    }
  ]
}
[/block]
The next step would be to click **Save segment**, name the segment, and then see it show up in the main *Segments* menu by its name, which in this case is *Frequent Buyers*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f1a1ce2-Segments_PSB_Created_Segment.png",
        "Segments_PSB_Created_Segment.png",
        800,
        494,
        "#f3f5f6"
      ],
      "border": true
    }
  ]
}
[/block]
### View a Past Behavior Segment Report

The top portion of the past behavior user segment report consists of a way to first *Show segment definition* to understand its underlying query. There are graphs on the left-hand side showing the plot of the number of users who qualified for the segment going forward from the first complete day post-segment creation. The list on the right-hand side shows the sample list of users who qualified for the segment on this day.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/77138b9-Segment_PSB_Report.gif",
        "Segment_PSB_Report.gif",
        1218,
        658,
        "#f7f8f9"
      ],
      "border": true
    }
  ]
}
[/block]
The lower portion of the live user segment report consists of reachability percentages for these users within each messaging channel. The lower-most part of the report shows you how to do more with this segment by either filtering relevant analytics dashboard views by this particular user segment or reaching out to this segment via appropriate messaging channels.

## Create Precomputed Segment
Any past behavior segment can be made a precomputed segment. To mark any Past Behavior Segment as a Precomputed segment:
1. From the dashboard, navigate to *Segments* > *Segments*.
2. Select a past behavior segment. The segment details are displayed as shown in the following figure.
3. Click **Mark Precomputed**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c8aa3e0-Segment_Details_page.png",
        "Segment Details page.png",
        1233,
        734,
        "#f3f5f8"
      ],
      "border": true
    }
  ]
}
[/block]
# View Analytics Filtered by Segment

Under the *Do more with this segment section,* you have the option to view an analytics report. This will be for the chosen segment alone and not your entire user base. 

Analysis dashboard views have the following filter at the top to enable this:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a8df120-321ce60-Screenshot_2020-06-08_at_1.18.47_PM.png",
        "321ce60-Screenshot_2020-06-08_at_1.18.47_PM.png",
        2310,
        1552,
        "#fbfbfb"
      ],
      "border": true
    }
  ]
}
[/block]
Realtime dashboard views such as the Today dashboard only enables filtering by Live User segments. Analytics based on past behavior such as Mobile App, Revenue, Funnels, Cohorts, Trends, and Events will only enable filtering their stats by Past Behavior segments.

# Create Campaigns for a Chosen Segment

Under the *Do more with this segment* section, under *Engage*, you have the option to create a campaign to message a specific segment.

This immediately takes you to the messaging channel with your segment criteria pre-populated in the target.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3c7905e-Segments_Do_More_Campaign.png",
        "Segments_Do_More_Campaign.png",
        617,
        292,
        "#fcfcfd"
      ],
      "border": true,
      "caption": ""
    }
  ]
}
[/block]
#Include/Exclude Segments

You can simplify complex queries by including or excluding the existing user segments. Create segments with complex conditions once and then reuse them in different scenarios. 

You can create powerful segmentation that is valid for a variety of scenarios. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/30d054b-0fd3c96-Find_people_include_exclude_segments.png",
        "0fd3c96-Find_people_include_exclude_segments.png",
        715,
        382,
        "#f6f7fb"
      ],
      "border": true
    }
  ]
}
[/block]
##Exclude Segments

There may be instances when you want to exclude some users based on specific criteria. 

For example, you want to offer discounts to all the users who have expressed interest by adding the product to the cart in the past 30 days; however, you want to save your engagement dollars by excluding the power users. 
The parameters for these power users can be the following:
  * Users who have charged three times in the past three months, and 
  * Users who have launched the app 15 times in the past month, and
  * Users who rated a product 10 times in the past year

Now you can create a segment with these criteria called *Power Users* and use it every time rather than creating a complex query each time. You can save all these parameters in a segment called *Power Users* and exclude them from the discount message. 

The following is a campaign query for an e-commerce app that excludes the *Power Users* segment.


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2fb7f6a-exclude_segments_campaign.png",
        "exclude_segments_campaign.png",
        1050,
        1506,
        "#fafaf9"
      ],
      "sizing": "full",
      "border": true
    }
  ]
}
[/block]
##Include Segments

There may be instances when you want to include some users based on specific criteria. 

Consider the example of a ride-hailing app. You want to nudge your users to enroll for a monthly pass as soon as they open the app. The parameters for these users can be the following:
  * The users must be power users, and
  * The users have booked more than five rides in a month, and
  * They belong to select cities in the country
 
Now you can create a segment with these criteria called *Power Users* and using it repeatedly rather than creating a complex query each time. 

The following is a campaign query for a ride-hailing app that includes the *Power Users* segment.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f9f341a-include_segments_campaign.png",
        "include_segments_campaign.png",
        1067,
        1270,
        "#fbfbfc"
      ],
      "sizing": "full",
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "body": "  * You can include and exclude segments in the same query. It is considered as an AND condition between the two segments.\n  * The include and exclude segments are currently unavailable for bulletins and A/B Testing.\n  * The segments available for including or excluding users can only be of the type [PBS](https://docs.clevertap.com/docs/segments#section-past-behavior-segments) segment. ",
  "title": "Include and Exclude Segments"
}
[/block]
# Additional AND By Behavior Filters
*AND By behavior* filters provide customers the ability to segment users based on the count, average, or total sum of a property value.

### Count
The *Count* filter allows customers to filter users by event count. The query finds all users who performed a *Charged* event greater than five (5) times in the past 30 days. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0678593-2020-11-24_17-51-01_Count.png",
        "2020-11-24_17-51-01_Count.png",
        1192,
        378,
        "#fafbfd"
      ],
      "border": true
    }
  ]
}
[/block]
### Average of Property Filter
The *Average of property *filter allows customers to filter users by the average of a chosen event property. The query finds all users who performed a *Charged* event such that the average *Revenue* event property per event is greater than $10. 

The Average of property filter allows averaging the value of the selected event property. For example, you can find out the average revenue earned from all users who performed purchases worth $10 or less. Let us assume that 5 users charged for each for $3, $5, $7, $2, and $8. The average value of all the purchases lower than $10 is ($ 3+ 5 +7+2+8)/5 events = 25/5= $5 per event. 

Let us assume that the value for 2 charged events is missing. The charged event values received are $3, $5, and $7. The value of the missing events will be considered as “0”. The average of property is now ($3 + 5 +7 +0 +0)/5 events = 15/5 =$3 per event. 
If you want to exclude all the events that do not have event properties, you can select the property exists condition in the Filter by section.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/09c3239-2020-11-24_17-52-22_Average_of_property.png",
        "2020-11-24_17-52-22_Average of property.png",
        1192,
        382,
        "#fafbfd"
      ],
      "border": true
    }
  ]
}
[/block]
### Total Sum of Property
The *Total sum of property* filter allows customers to filter users by the sum of a chosen event property. The query finds all users who performed a *Charged* event such that the *Revenue* event property is greater than $10.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d973ab4-2020-11-24_17-53-50_Total_sum_of_property.png",
        "2020-11-24_17-53-50_Total sum of property.png",
        1194,
        382,
        "#fafbfd"
      ],
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "Include users who did not do the event",
  "body": "If the query is to find people who performed the charged event fewer than five times, by default, the users who have not performed the charged event are not included in the result set. Only the users who did the charged event but did it fewer than five times are included; however, if the checkbox for *Include users who didn’t do the event* is selected, those users are also included in the result set. The same is true for sum and average."
}
[/block]

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/db44a26-2020-11-24_17-56-46_Checkbox_message.png",
        "2020-11-24_17-56-46_Checkbox message.png",
        1187,
        412,
        "#fdfdfd"
      ],
      "border": true
    }
  ]
}
[/block]