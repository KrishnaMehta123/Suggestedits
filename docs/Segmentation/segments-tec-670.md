---
title: Segments (TEC-670)
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

A segment in CleverTap is a group of users whose actions performed, actions not performed, or user profile properties match a set of defined criteria. For example, a segment can be users who launched the app for the first time in the past 30 days. A more complex segment could be users who live in New York, were acquired via a Facebook campaign in April, transacted three or more times in May and June, and have not transacted in the past two weeks.

After you have identified segments of interest, you can save and then target them with any type of messaging campaign. You can also trend segments over time to understand how a segment behaves in response to your marketing initiatives. The entire CleverTap dashboard can be filtered by any segment you create, including any of our analytics features.

# Types of Segments

There are three types of segments in CleverTap, which are explained in the following sections:

- [Past Behavior Segments](https://docs.clevertap.com/docs/segments#past-behavior-segments)
- [Live User Segments](https://docs.clevertap.com/docs/segments#live-user-segments)
- [System User Segments](https://docs.clevertap.com/docs/segments#system-user-segments)

## Past Behavior Segments

Past behavior segments are users grouped by their actions in the past. 

You can group users based on a single activity to complex combinations of actions, inactions, and user properties.

> 👍 Past Behavior Segments Example
> 
> An example would be to segment by all my users who launched the app in the past 30 days.

## Live User Segments

While past behavior segments let you evaluate users based on historic criteria, live user segments let you track what is happening in your app right now.

When you define a set of behaviors of interest, CleverTap monitors for these behaviors as they happen in your app and immediately adds a user to a segment the moment their behavior matches your action criteria.

You can create live user segments for a single activity (booked a movie ticket), inaction (did not buy a movie ticket in a certain time), off of date/time properties of events, or website-related actions, such as page visit, count, or referrer.

## System User Segments

The following are system-defined user segments that are available for your use: 

- All Users: This user segment contains all the users available to your account.
- Test Users: This user segment contains the users who you can test for your campaign response. A campaign or journey can now be tested on this _Test Users_ segment before it is sent to an actual segment. The _Test User_ segment is available by default for engagement and UI experiences. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/eb9b8b9-1a9589c-Segment_System.png",
        "View System Defined User Segments",
        1208
      ],
      "align": "center",
      "border": true,
      "caption": "Segments - Overview"
    }
  ]
}
[/block]


# Create Segments

To create a new segment, perform the following steps:

1. From the dashboard, navigate to _Segments_ > _Segments_.
2. Click **+ Segment**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/471192b-3_main_section.png",
        "Click +Segment to Create a Segment",
        1396
      ],
      "align": "center",
      "border": true,
      "caption": "Create Segment"
    }
  ]
}
[/block]


3. The main segment creation page displays a list of options for types of past behavior and live user segments. Select an option based on the required segment.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c000bf0-select_an_option.png",
        "Select Your Preferred Type of Past Behavior Segment",
        1199
      ],
      "align": "center",
      "border": true,
      "caption": "Past Behavior Segment"
    }
  ]
}
[/block]


Past behavior segments can be based on:

- Past user actions (for example, users who added a product to the cart in the past 30 days)
- Past user action/inaction combination (for example, users who added a product to the cart but did not purchase in the last 30 days)
- Past user action/inaction combination along with common user properties (for example, platinum-level users who added a product to the cart but did not purchase in the last 30 days)

Live user segments can add users to the segment as soon as users qualify based on the following:

- Single action (for example, users who have added a product to the cart)
- Inaction within time (for example, users who have added a product to the cart but did not purchase within 10 minutes of adding product to the cart)
- On a date/time (for example, users who have an appointment five days from today)
- Page visit (for example, users who have visited a certain URL on your website)
- Referrer entry (for example, users who have visited your website via a certain external referrer URL)
- Page count (for example, users who have visited a certain number of pages on your website)

# Segment List Page

The _Segments_ list page shows all existing segments available for you. You can choose to do various tasks with these listed segments. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4e1fcdb-Segments_all_operations.png",
        "Click the Ellipsis to View Segment Operations",
        1221
      ],
      "align": "center",
      "border": true,
      "caption": "Segment List"
    }
  ]
}
[/block]


# Create Live User Segments

Live user segments can add users to the segment as soon as users qualify based on the following:

- Single action: users who have added a product to the cart.
- Inaction within time: users who have added a product to the cart but did not purchase within 10 minutes of adding a product to the cart.
- On a date/time: users who have an appointment five days from today.
- Page visit: users who have visited a certain URL on your website.
  - Referrer entry: users who have visited your website via a certain external referrer URL.
  - Page count: users who have visited a certain number of pages on your website.

In this example, we can create an _Inaction within time_ segment for which users will qualify in real-time as soon as they add a product to cart but do not purchase the product within 10 minutes.

> 📘 Golden Window for Mobile Transactions
> 
> The golden window within which most users transact on our iOS and Android app platforms is within 10 minutes.

To create a live segment with CleverTap, perform the following steps:

1. From the dashboard, navigate to _Segments_ > _Segments_.
2. Click **+ Segment**.
3. Under _Live user segments_, select the _Inaction within time_ box.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/db039c0-1_live_user_segment_selection.png",
        "Click Select to Create an Inaction Within Time",
        1207
      ],
      "align": "center",
      "border": true,
      "caption": "Create Live User Segment"
    }
  ]
}
[/block]


5. Select the appropriate properties for your live user segment. 

You may choose to select the _Filter on past user behavior and common properties_ checkbox to apply past action, inaction, or common user property filters.

6. Click **Save segment**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/033db1c-2_set_up_Live_user_segment_-_Inaction_within_time.png",
        "Set Up Segment Options and Click Save Segment",
        1403
      ],
      "align": "center",
      "border": true,
      "caption": "Save Segment"
    }
  ]
}
[/block]


7. Name the segment, then click **Save**.

> 📘 Segment Naming Best Practices
> 
> Convey the core meaning of the segment while keeping the name brief.

8. You can now see your new segment in the main section as _Added to cart but no charge within 10 minutes_.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d546264-3_main_section.png",
        "View Created Segment in Segment List Page",
        1396
      ],
      "align": "center",
      "border": true,
      "caption": "View Created Segment"
    }
  ]
}
[/block]


## View Live User Segment Reports

To view a live user segment report, perform the following steps:

1. From the dashboard, navigate to _Segments_ > _Segments_.
2. Search for the segment you are looking for, then click on it.  

At the top of the report, you can click _View segment definition_ to understand more about the underlying query. 

The two graphs describe the following:

- The left-hand side shows the plot of the number of users who qualified for the segment going forward from the first complete day after creating the segment.
- The right-hand side shows the real-time rate at which users are qualifying for the segment vs. all user activity on your app/website. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/821380f-4a_top_report.png",
        "View Live User Segment Reports",
        1272
      ],
      "align": "center",
      "border": true,
      "caption": "Segment Reports"
    }
  ]
}
[/block]


- The lower portion of the live user segment report consists of a list of sample users trickling into your segment in real-time on the right-hand side. It also shows the reachability percentages for these users within each messaging channel on the left-hand side.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/25d5194-4b_middle_report.png",
        "View Segment Size and Reachability",
        1269
      ],
      "align": "center",
      "border": true,
      "caption": "Segment Size and Reachability"
    }
  ]
}
[/block]


- The lower-most part of the report shows how to do more with this segment by either filtering relevant analytics dashboard views by this particular user segment or reaching out to this segment via relevant messaging channels.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/44308a1-4c_bottom_report.png",
        "View Sample Users for an Event",
        1266
      ],
      "align": "center",
      "border": true,
      "caption": "Sample Users"
    }
  ]
}
[/block]


# Create Past Behavior Segments

To create a past behavior segment, perform the following steps: 

1. From the dashboard, navigate to _Segments_ > _Segments_.
2. Select any of the options underneath _Past behavior user segments_ from the main segment creation page.

For example, we can create an action-based segment where users will qualify if they have applied a payment offer at least one time in the past 30 days.

3. Select the box _Actions_ which takes you to the segment setup page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6f6d353-Segments_PSB_Create_New.png",
        "Set Up Segment Options to Create a Past Behavior Segment",
        1228
      ],
      "align": "center",
      "border": true,
      "caption": "Create Past Behavior Segment"
    }
  ]
}
[/block]


4. Click **Save segment** and name the segment. You can now view your new segment on the overview page.

## View a Past Behavior Segment Report

The top portion of the past behavior user segment report consists of a way to first view the segment definition to understand its underlying query. There are graphs on the left-hand side showing the plot of the number of users who qualified for the segment going forward from the first complete day post-segment creation. The list on the right-hand side shows the sample list of users who qualified for the segment on this day.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1225063-report.png",
        "View Segment Trend Report",
        1204
      ],
      "align": "center",
      "border": true,
      "caption": "Segment Trend"
    }
  ]
}
[/block]


The past behavior segment statistics are computed daily. When used in campaigns, the users who qualify for these segments are computed in real-time.

The lower portion of the past behavior segment report consists of reachability percentages for these users within each messaging channel. The lower-most part of the report shows you how to do more with this segment by either filtering relevant analytics dashboard views by this particular user segment or reaching out to this segment via relevant messaging channels.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8f416de-lower_report.png",
        "View Segment Size and Reachability Report",
        1206
      ],
      "align": "center",
      "border": true,
      "caption": "Segment Size and Reachability"
    }
  ]
}
[/block]


# View Analytics Filtered by Segment

Under the _Do more with this segment section,_ you have the option to view an analytics report. This is for the chosen segment alone and not your entire user base. 

Real-time dashboard views such as the _Today_ dashboard only enable filtering by live user segments. Analytics based on past behavior such as mobile app, revenue, funnels, cohorts, trends, and events will only enable filtering their stats by past behavior segments.

# Create Campaigns for a Chosen Segment

Under the _Do more with this segment_ section, under _Engage_, you have the option to create a campaign to message a specific segment.

This immediately takes you to the messaging channel with your segment criteria pre-populated in the target.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3c7905e-Segments_Do_More_Campaign.png",
        "Click Campaign from the Do More with this Segment option",
        617
      ],
      "align": "center",
      "border": true,
      "caption": "Create Campaign from Segment"
    }
  ]
}
[/block]


# Include and Exclude Segments

You can simplify complex queries by including or excluding the existing user segments. Create segments with complex conditions once and then reuse them in different scenarios. 

You can create powerful segmentation that is valid for a variety of scenarios. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/30d054b-0fd3c96-Find_people_include_exclude_segments.png",
        "Create Segments with Complex Conditions",
        715
      ],
      "align": "center",
      "border": true,
      "caption": "Include and Exclude Segments"
    }
  ]
}
[/block]


> 📘 Searching Segments under Include and Exclude Filters
> 
> When searching for your segments, CleverTap allows visibility for only the most recently created 1000 segments under the include and exclude filters. To ensure that the dropdowns display the newly-created segments, we highly recommend deleting any unused segments to optimize the visibility and accessibility of your segments in the dropdown menus.

## Exclude Segments

There may be instances when you want to exclude some users based on specific criteria. 

For example, you want to offer discounts to all the users who have expressed interest by adding the product to the cart in the past 30 days; however, you want to save your engagement dollars by excluding the power users.  
The parameters for these power users can be the following:

- Users who have charged three times in the past three months, and 
- Users who have launched the app 15 times in the past month, and
- Users who rated a product 10 times in the past year

Now, you can create a segment with these criteria called _Power Users_ and use it every time rather than creating a complex query each time. You can save all these parameters in a segment called _Power Users_ and exclude them from the discount message. 

The following is a campaign query for an e-commerce app that excludes the _Power Users_ segment.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2fb7f6a-exclude_segments_campaign.png",
        "Set Up the Options to Exclude a Segment from Campaign",
        1050
      ],
      "align": "center",
      "sizing": "100",
      "border": true,
      "caption": "Exclude Segments"
    }
  ]
}
[/block]


## Include Segments

There may be instances when you want to include some users based on specific criteria. 

Consider the example of a ride-hailing app. You want to nudge your users to enroll for a monthly pass as soon as they open the app. The parameters for these users can be the following:

- The users must be power users, and
- The users have booked more than five rides in a month, and
- They belong to select cities in the country

Now, you can create a segment with these criteria called _Power Users_ and using it repeatedly rather than creating a complex query each time. 

The following is a campaign query for a ride-hailing app that includes the _Power Users_ segment.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f9f341a-include_segments_campaign.png",
        "Set Up the Options to Include a Segment from Campaign",
        1067
      ],
      "align": "center",
      "sizing": "100",
      "border": true,
      "caption": "Include Segment"
    }
  ]
}
[/block]


> 📘 Include and Exclude Segments
> 
> - You can include and exclude segments in the same query. It is considered as an _AND_ condition between the Included and the Excluded segments.
>   - The include and exclude segments are currently unavailable for bulletins and A/B Testing.
>   - The segments available for including or excluding users can only be of the type [PBS](https://docs.clevertap.com/docs/segments#section-past-behavior-segments) segment.

# Additional AND By Behavior Filters

_AND By behavior_ filters provide customers the ability to segment users based on the count, average, or total sum of a property value.

### Count

The count filter allows customers to filter users by event count. The query finds all users who performed a _Charged_ event greater than 5 times in the past 30 days. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0678593-2020-11-24_17-51-01_Count.png",
        "Select Count to Filter Users by Count",
        1192
      ],
      "align": "center",
      "border": true,
      "caption": "Count Filter"
    }
  ]
}
[/block]


### Average of Property Filter

The _Average of property_ filter allows customers to filter users by the average of a chosen event property. The query finds all users who performed a _Charged_ event such that the average _Revenue_ event property per event is greater than $10. 

The _Average of property_ filter allows averaging the value of the selected event property. For example, you can find out the average revenue earned from all users who performed purchases worth $10 or less. Let us assume that 5 users charged for each for $3, $5, $7, $2, and $8. The average value of all the purchases lower than $10 is ($ 3+ 5 +7+2+8)/5 events = 25/5= $5 per event. 

Let us assume that the value for 2 charged events is missing. The charged event values received are $3, $5, and $7. The value of the missing events will be considered as 0. The average of property is now ($3 + 5 +7 +0 +0)/5 events = 15/5 =$3 per event. 

If you want to exclude all the events that do not have event properties, you can select the property that exists a condition in the _Filter by_ section.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/09c3239-2020-11-24_17-52-22_Average_of_property.png",
        "Select Average of Property Filter",
        1192
      ],
      "align": "center",
      "border": true,
      "caption": "Average of Property Filter"
    }
  ]
}
[/block]


### Total Sum of Property

The _Total sum of property_ filter allows customers to filter users by the sum of a chosen event property. The query finds all users who performed a _Charged_ event such that the _Revenue_ event property is greater than $10.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d973ab4-2020-11-24_17-53-50_Total_sum_of_property.png",
        "Select Total Sum of Property Filter",
        1194
      ],
      "align": "center",
      "border": true,
      "caption": "Total Sum of Property Filter"
    }
  ]
}
[/block]


> 📘 Include Users Who Did Not Do the Event
> 
> If the query is to find people who performed the charged event fewer than five times, by default, the users who have not performed the charged event are not included in the result set. Only the users who did the charged event but did it fewer than five times are included; however, if the checkbox for _Include users who didn’t do the event_ is selected, those users are also included in the result set. The same is true for sum and average.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/db44a26-2020-11-24_17-56-46_Checkbox_message.png",
        "Select the Checkmark to Include Users Who Did Not Do an Event",
        1187
      ],
      "align": "center",
      "border": true,
      "caption": "Include Users Who Did Not Do an Event"
    }
  ]
}
[/block]