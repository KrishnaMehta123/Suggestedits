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

<Table align={["left","left","left","left"]}>
  <thead>
    <tr>
      <th>
        Attribution Partner
      </th>

      <th>
        Inorganic Install Events
      </th>

      <th>
        Organic Install Events
      </th>

      <th>
        Custom Events
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        CleverTap
      </td>

      <td>
        Not applicable
      </td>

      <td>
        Always selected
      </td>

      <td>
        Not applicable
      </td>
    </tr>

    <tr>
      <td>
        Adjust
      </td>

      <td>
        Always selected
      </td>

      <td>
        Not selected
      </td>

      <td>
        Not selected
      </td>
    </tr>

    <tr>
      <td>
        AppsFlyer
      </td>

      <td>
        Always selected
      </td>

      <td>
        Not selected
      </td>

      <td>
        Not selected
      </td>
    </tr>

    <tr>
      <td>
        Branch
      </td>

      <td>
        Always selected
      </td>

      <td>
        Not available
      </td>

      <td>
        Not selected
      </td>
    </tr>

    <tr>
      <td>
        Singular
      </td>

      <td>
        Always selected
      </td>

      <td>
        Not selected
      </td>

      <td>
        Not selected
      </td>
    </tr>
  </tbody>
</Table>

Depending on the requirement, you can choose to track event data from the *Settings* > *Partners* page of the CleverTap dashboard. 

> 📘 Access Permissions
>
> To update the settings of this page, the user must have admin access or the required access rights.

For more information about enabling attribution settings for supported providers, refer to the following documents: 

* [Enable Partner Attribution for Adjust](doc:adjust_pe_2#step-3-enable-the-attribution-partner)
* [Enable Partner Attribution for Appsflyer](doc:appsflyer_pe_2#step-3-enable-the-attribution-partner)
* [Enable Partner Attribution for Branch](doc:branch_pe_2#step-3-enable-the-attribution-partner)
* [Enable Partner Attribution for Singular](doc:singular-formerly-known-as-apsalar_pe_2#step-3-enable-the-attribution-partner)
