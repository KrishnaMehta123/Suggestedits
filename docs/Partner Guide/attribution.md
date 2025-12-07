---
title: Attribution Partners
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview
For marketers, it is very important to understand where their customers are coming from and how they can engage with them effectively. This is when attribution plays a very important role. CleverTap partners with different attribution providers and tracks app installations, measure attribution with third-party sources, and view reports in the CleverTap Dashboard.

CleverTap supports integrations with the following third-party attribution providers:
  * [Adjust](https://developer.clevertap.com/docs/adjust)
  * [Airbridge](https://developer.clevertap.com/docs/airbridge)
  * [AppsFlyer](https://developer.clevertap.com/docs/appsflyer) 
  * [Branch](https://developer.clevertap.com/docs/branch)
  * [Singular](https://developer.clevertap.com/docs/singular-apsalar)

# Types of Data
CleverTap receives the following event data from the specified attribution partner and then processes and saves it:

  * **Inorganic Install Events** - These install events are attributed to some media source, for example, paid advertisements running on some third-party applications. It implies that the application is installed as a result of engaging with any advertisement.
  * **Organic Install Events** - These install events are attributed to the website or app store or referrals. It implies that the application is installed either from the website, app store or via referrals and not by engaging with any kind of advertisements.
  * **Custom Events** - These events can be any events (other than install events) that are provided by the attribution partner and tracked in the app. 

The following table lists the default CleverTap dashboard settings to track the events:
[block:parameters]
{
  "data": {
    "h-0": "Attribution Partner",
    "h-1": "Inorganic Install Events",
    "h-2": "Organic Install Events",
    "h-3": "Custom Events",
    "0-0": "CleverTap",
    "1-0": "Adjust",
    "2-0": "Airbridge",
    "3-0": "AppsFlyer",
    "0-2": "Always selected",
    "0-1": "Not applicable",
    "0-3": "Not applicable",
    "1-1": "Always selected",
    "3-1": "Always selected",
    "3-2": "Not selected",
    "3-3": "Not selected",
    "2-1": "Always selected",
    "2-2": "Not selected",
    "2-3": "Not selected",
    "1-2": "Not selected",
    "1-3": "Not selected",
    "4-0": "Branch",
    "4-1": "Always selected",
    "4-2": "Not available",
    "4-3": "Not selected",
    "5-0": "Singular",
    "5-1": "Always selected",
    "5-2": "Not selected",
    "5-3": "Not selected"
  },
  "cols": 4,
  "rows": 6
}
[/block]
Depending on the requirement, you can choose to track event data from the *Settings* > *Partners* page of the CleverTap dashboard. 
[block:callout]
{
  "type": "info",
  "title": "Access Permissions",
  "body": "To update the settings of this page, the user must have admin access or the required access rights."
}
[/block]
For more information about enabling attribution settings for supported providers, refer to the following documents: 
* [Adjust](https://developer.clevertap.com/docs/adjust)
* [Airbridge](https://developer.clevertap.com/docs/airbridge)
* [Appsflyer](https://developer.clevertap.com/docs/appsflyer)
* [Branch](https://developer.clevertap.com/docs/branch)
* [Singular (formerly known as Apsalar)](https://developer.clevertap.com/docs/singular-apsalar)