---
title: Attribution Partners_PE_2
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
For marketers, it is very important to understand where their customers are coming from and how they can engage with them effectively. This is when attribution plays a very important role. CleverTap partners with different attribution providers and tracks app installations, measure attribution with third-party sources, and view reports in the CleverTap Dashboard.

CleverTap supports integrations with the following third-party attribution providers:
  * [Adjust](doc:adjust-1)
  * [AppsFlyer](doc:appsflyer) 
  * [Branch](doc:branch)
  * [Singular](doc:singular-1)

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
    "2-0": "AppsFlyer",
    "3-0": "Branch",
    "0-2": "Always selected",
    "0-1": "Not applicable",
    "0-3": "Not applicable",
    "1-1": "Always selected",
    "3-1": "Always selected",
    "3-2": "Not available",
    "3-3": "Not selected",
    "2-1": "Always selected",
    "2-2": "Not selected",
    "2-3": "Not selected",
    "1-2": "Not selected",
    "1-3": "Not selected",
    "4-0": "Singular",
    "4-1": "Always selected",
    "4-2": "Not selected",
    "4-3": "Not selected"
  },
  "cols": 4,
  "rows": 5
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
* [Enable Partner Attribution for Adjust](doc:adjust_pe_2#step-3-enable-the-attribution-partner)
* [Enable Partner Attribution for Appsflyer](doc:appsflyer_pe_2#step-3-enable-the-attribution-partner)
* [Enable Partner Attribution for Branch](doc:branch_pe_2#step-3-enable-the-attribution-partner)
* [Enable Partner Attribution for Singular](doc:singular-formerly-known-as-apsalar_pe_2#step-3-enable-the-attribution-partner)