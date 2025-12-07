---
title: Group Unsubscribe New
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: >-
    DOCS NOTE: COMPARE/REVIEW WITH THE EXISTING PAGE:
    https://docs.clevertap.com/docs/handling-unsubscribes
  robots: noindex
next:
  description: ''
  pages:
    - type: link
      title: Override Link Tracking
      url: https://docs.clevertap.com/docs/override-link-tracking-c20
    - type: link
      title: Email Campaign Stats
      url: https://docs.clevertap.com/docs/email-stats
    - type: link
      title: Email Troubleshooting
      url: https://docs.clevertap.com/docs/troubleshooting-email
---
[block:api-header]
{
  "title": "Overview"
}
[/block]
CleverTap offers Group Unsubscribe, which allows customers to opt out of certain groups of messages. With Group Unsubscribe, the customer unsubscribes only from a particular group of messages but continues receiving the messages of interest.

##Subscription Groups
You can group every marketing campaign or outgoing communication message into different subscription group categories. Customers may like to receive messages about a particular category but might opt out of a separate category of messages.

##Create Subscription Groups
Perform the following steps to create a Subscription Group from a particular campaign.

1. From the CleverTap dashboard, select *Settings* > *Engage* > *Setup* *Subscription Groups*.
2. Enter the group's name, provide a brief description, and select the *Email* channel.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2c812d9-Email_subscription_group_setup.png",
        "Email_subscription_group_setup.png",
        1027,
        575,
        "#fafafb"
      ],
      "border": true,
      "sizing": "smart"
    }
  ]
}
[/block]
3. Click **Save**.
[block:callout]
{
  "type": "info",
  "body": "Customers can set up 50 active groups. They can also archive groups to create new ones.",
  "title": "Active Subscription Groups"
}
[/block]

## Use Subscription Groups in Segments
1. From the CleverTap dashboard, select  *Segments*  > *Find People*.
2. From *Display common properties such as* section, click **+Properties.**

3. Click **+Properties** and select *Subscription Groups* from the dropdown menu.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/fca954f-Email_subscription_group_list.png",
        "Email_subscription_group_list.png",
        929,
        369,
        "#f8f8fb"
      ],
      "border": true
    }
  ]
}
[/block]
4. Select the *Exclude/Include* parameter and accept the All default or select one or multiple options.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4412785-Email_subscription_group_include_exclude.png",
        "Email_subscription_group_include_exclude.png",
        926,
        366,
        "#f7f8fb"
      ],
      "border": true,
      "sizing": "smart"
    }
  ]
}
[/block]
## Use Subscription Groups in Campaigns

You can choose to exclude subscription group users from your campaigns. 

1. From the CleverTap dashboard, select *Campaign* and create an email campaign. Refer to [Create Email Campaign](https://docs.clevertap.com/docs/create-message-email).
2. From the *Who* > *Control group and targeting cap* > *Do not send this campaign to users who have unsubscribed from the following groups section*. 
3. Select the groups you don't want to include in your campaign from the *Select subscription groups* list.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3121088-Email_subscription_group_campaign.png",
        "Email_subscription_group_campaign.png",
        773,
        278,
        "#f7f9fb"
      ],
      "border": true,
      "sizing": "smart"
    }
  ]
}
[/block]
3. Click **Apply**.
4. Click **Continue**
5. Complete creating the email campaign.

## Use Subscription Groups in Email Landing Page
Refer to [handling unsubscribes](https://docs.clevertap.com/docs/handling-unsubscribes) to add the Subscription Group configuration to your email landing page.

## Track Unsubscribes
Whenever a user unsubscribes, CleverTap raises a system event called *Channel Unsubscribed* which updates the user's property with the status of subscription for the group.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b1c9872-Unsubscribe_last_step.png",
        "Unsubscribe last step.png",
        1012,
        966,
        "#f7f8fa"
      ],
      "border": true
    }
  ]
}
[/block]