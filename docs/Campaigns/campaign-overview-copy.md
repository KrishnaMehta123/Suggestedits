---
title: Campaign Overview
excerpt: Understand how to engage with users through Campaigns.
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

Campaigns promote products through various media types and are designed with specific goals, such as building brand awareness, introducing new products, or driving conversions.

The campaign listing page in CleverTap helps you manage all your campaigns efficiently. It allows you to filter them, edit columns, view performance, organize using labels, and more. This guide walks you through all key operations on the new campaigns page.

> 📘 Private Beta
>
> Currently, this feature is a Private Beta Release. If you want access to this feature, contact your Account Manager.

# Campaigns Operations

You can perform different actions on the campaigns from the *All Campaigns* page, including filtering, labeling, editing, archiving, stopping, cloning, and analyzing performance. The following sections briefly discuss each operation. 

## Filter Campaigns

You can use filters to quickly search your campaigns by Status, Channel, Time Period, creator, and more. To do so: 

1. Go to *Messages* > *Campaigns* from the CleverTap dashboard. The *All Campaigns* page opens.
2. Click the ![](https://files.readme.io/ac0ed6a-Filter_icon.png) icon. The *Filters* window opens on the left side of the screen.

<Image alt="Filter Campaigns" align="center" border={true} src="https://files.readme.io/cb4445f55fa911570e0468447bf785041e3b6b03930b19dc4a50be6e0999b1da-Campaign_Listing.png">
  Filter Campaigns
</Image>

3. Select the required filters and click **Apply** to view results on the *All Campaigns* page.
4. Click **Reset** to reset all the applied filters. 

Filters are divided into two main sections, Active and Archived. Refer to the table below for filter operations: 

<Table>
  <thead>
    <tr>
      <th>
        Filter Section
      </th>

      <th>
        Filter Description
      </th>

      <th>
        Options
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **Saved Filters**
      </td>

      <td>
        Select from a list of saved filters. In that case, all the fields will be automatically populated. You can also create a new filter and click 

        **Save**

        . Filters are saved at the account level and are available for the Active campaigns.
      </td>

      <td>
        \-
      </td>
    </tr>

    <tr>
      <td>
        **Status**
      </td>

      <td>
        <li>Filters campaigns based on their current status. These options are available for **active** campaigns. </li><li>Possible values: Scheduled, Running, Stopped, Completed, Approval Pending, Rejected, Draft, Awaiting Next Run.</li> For more information, refer to [Campaign States]().
      </td>

      <td>
        \-
      </td>
    </tr>

    <tr>
      <td>
        **Time Period**
      </td>

      <td>
        Filters based on the time period when the campaigns were created or started. The list is automatically sorted in descending order, based on either the start time or the creation date, depending on the selected filter.
      </td>

      <td>
        Campaigns Created / Started
      </td>
    </tr>

    <tr>
      <td>
        **Stats Period**
      </td>

      <td>
        Filters based on the stats period of the campaigns.
      </td>

      <td>
        Choose stats duration
      </td>
    </tr>

    <tr>
      <td>
        **Mobile Channel**
      </td>

      <td>
        Filters based on the type of mobile channel used.
      </td>

      <td>
        Push Notification, In-App Message, App Inbox, Native Display
      </td>
    </tr>

    <tr>
      <td>
        **Web Channel**
      </td>

      <td>
        Filters based on the type of web channel used.
      </td>

      <td>
        Web Popup, Exit Intent, Web Push Notification, Web Native Display, Web Inbox
      </td>
    </tr>

    <tr>
      <td>
        **Direct-to-User Channel**
      </td>

      <td>
        Filters based on the type of Direct-to-User channel used.
      </td>

      <td>
        Email, SMS, WhatsApp, Unified Inbox
      </td>
    </tr>

    <tr>
      <td>
        **Streaming Channel**
      </td>

      <td>
        Filters based on the type of streaming channel used.
      </td>

      <td>
        Facebook Audiences, Webhook, Google Adwords, Amazon EB, mParticle, Segment, TikTok
      </td>
    </tr>

    <tr>
      <td>
        **Created By**
      </td>

      <td>
        Filters based on the email ID of the person who created the campaign.
      </td>

      <td>
        Filter by email ID of campaign creator
      </td>
    </tr>

    <tr>
      <td>
        **Label**
      </td>

      <td>
        Filters based on the labels assigned to the campaign. Clicking 

        **Manage Labels**

         will redirect you to the labels page in account setup. You can create or manage labels as per your assigned roles.
      </td>

      <td>
        Based on labels assigned to campaigns
      </td>
    </tr>

    <tr>
      <td>
        **Delivery Type**
      </td>

      <td>
        Filters based on the delivery type of the campaign.
      </td>

      <td>
        One Time, Recurring, Multiple Dates
      </td>
    </tr>

    <tr>
      <td>
        **Segment Type**
      </td>

      <td>
        Filters based on the type of segment used.
      </td>

      <td>
        In-Action, Action, On Date/Time, External Trigger
      </td>
    </tr>

    <tr>
      <td>
        **External Campaigns**
      </td>

      <td>
        Filters based on the type of external campaign.
      </td>

      <td>
        API Campaigns, Bulletins, Notification via Server API
      </td>
    </tr>
  </tbody>
</Table>

> 📘 Time Period Filters
>
> * By default, the date range for **Created** campaigns is *All time*.
> * By default, the date range for **Stats** campaigns is the *last 30 days*. The *All time range* is unavailable for Stats.
> * Resetting reverts the Time Period filters to default values.
> * Date ranges saved in filters are relative to the current date. For example, a *past 2 days* filter saved on July 2nd will show July 1st–2nd as the date range. When applied on July 20th, it shows July 19th–20th as the date range.

### Example

For example, consider a scenario where you want to view all Push campaigns created in the last 30 days, and are currently in the *Scheduled* or *Draft* state. Then you reset the date range from the last 30 days to *All time* and apply the *Test* label, and filter for *Action Type* segments. Here is how you can apply the filters: 

All matching campaigns will now appear in the list. 

Add GIF

Filters are only applied after you click **Apply**. If you create a filter and do not select **Apply**, the filter criteria are still displayed but not applied directly in the listing view.

All filters except the *Delivery Type* and *Segment Type* filters also have individual reset options. You can reset a specific filter and click **Apply** to immediately see the updated results in the campaign list.

## Edit Columns

You can customize the campaign listing view to match your preferences. Click the *Edit Columns* icon to select and reorder the columns you want displayed on the campaign list. You can view up to 2000 campaigns on the listing page.

The Sent column is toggled off by default. A new Engagement column is available to show channel-specific stats.

<Image alt="Edit Columns" align="center" border={true} src="https://files.readme.io/05bd2ec0f8c74cb89ce160267e739614a66e6f175ea2bd47d8b5a8ab66357951-2025-08-04_16-20-09_1.gif">
  Edit Columns
</Image>

## Campaign Reports

Selecting *Campaigns* from the CleverTap Dashboard opens the Campaign Reports table where you can see all your campaigns across every channel in one consolidated view. Campaign Reports include the channel, delivery status, and key statistics to assess and compare performance. 

Click Subscribe to reports and enter the details.

<Image title="Filter Campaigns and view Campaign reports on CleverTap dashboard." alt={1422} align="center" border={true} src="https://files.readme.io/5d2fc9b5e41e56926108dc575793b08b82a68b2ae5ef9f176767e8ffee73fc85-Campaign_Reports.png">
  Filter Campaigns and View Campaign Reports
</Image>

You can also email a report by selecting the campaign and clicking the email report icon. 

<Image alt="Email Report" align="center" border={true} src="https://files.readme.io/f8c0da53dd6aea9a0858d5a82118bd514171ae4cbf9bba4953421fe210e442b4-Email_reports.png">
  Email Report
</Image>

If the report section opens with *All Time* as the selected time period, requesting the report will automatically adjust the date range to ±15 days. A warning message will be displayed to inform the user of this change. For more details, refer to [Campaign Reports](https://staging.docs.user.clevertap.net/docs/campaign-reports-copy). 

## Add Labels

Labels allow you to tag campaigns with descriptive names or themes. Once applied, labels allow you to group your various messaging campaigns so that you can view their performance or identify user behaviors. For example, you can create a label called *Onboarding* to identify all the messaging campaigns (across all channels) related to onboarding your new users. 

You can select up to 10 labels for a campaign. If a campaign already has more than 10 labels assigned from earlier configurations, they will still be visible under *Selected Labels*. However, in such cases, the user will not be able to select any additional labels.

> 📘 Naming Labels
>
> The labels cannot start with or contain the following symbols: ”, \, %, >, \<, and !.

You can create and apply labels from the *All Campaigns* or the *All Journeys* page. Labels can be applied to individual campaigns from the All Campaigns page during creation. To do so:

1. Go to *Messages* > *Campaigns* from the CleverTap dashboard. The *All Campaigns* page opens.
2. Select the campaigns you may want to label and click the *Add Label* icon.
3. Select the labels you want to add. These labels are moved to the *Selected Tag ID* section. Click **Deselect** to remove any label. 
4. Click **Apply**.

<Image alt="Create Multiple Message Labels" align="center" border={true} src="https://files.readme.io/93019fa3fad015ac90de2faa18ba0255a67a0a1c899c9ee78b866109ea724ce0-2025-08-04_12-47-58_1.gif">
  Create and Assign Multiple Message Labels
</Image>

> 📘 Note
>
> * When applying labels in bulk, the selected labels are applied to *all* selected campaigns. However, if you later select an individual campaign from that group, the bulk-applied labels do not automatically appear in the *Selected Tag ID* section. 
> * To view or manage the labels for a specific campaign, click the **Labels** icon next to the campaign.
>
> <Image align="center" className="border" border={true} src="https://files.readme.io/1448d0f81e81413e3c206a4c85872c85a3dfb718c57754ed17cca37c8f54416b-Labels.png" />

You can view and export all labels to a CSV file from the *Settings* >  *Setup*  > *Labels*  page. You can also edit or delete labels from this page.

<Image alt="View Labels" align="center" width="100% " border={true} src="https://files.readme.io/e96d91674fd5178c48dcf69813fcd9110249717e1d5ffe42e5ed79ab4c8a7dcc-image.png">
  View Labels
</Image>

## Archive Campaigns

Archiving campaigns helps to keep your CleverTap account organized and clutter-free, making it easy to find and view the campaigns you want. To do so:

1. Go to *Messages* > *Campaigns* from the CleverTap dashboard. The *All Campaigns* page opens.
2. Select the campaigns you may want to archive and click the Archive icon.
3. Click **Save** to archive the selected campaigns or click **Cancel** to undo the action.

Running campaigns cannot be archived.

<Image alt="Archive Selected Campaigns" align="center" border={true} src="https://files.readme.io/0463ee95226683f426f48be57535b8d4241a59429c651c5a7aebca13e5fa03ee-Archive.png">
  Archive Selected Campaigns
</Image>

> 📘 Note
>
> * Campaigns in Completed or Stopped state are automatically archived after 6 months. To view archived campaigns, click *Filters* and select the *Archived* filter.
> * Archived campaigns cannot be unarchived.
> * All archived campaigns (including drafts) are read‑only and cannot be published. To continue working on an archived campaign, clone it. The clone is treated as a new campaign. You can **Save as draft**, **schedule**, or **publish** the cloned (new) campaign.

## Stop Campaigns

You may want to stop a particular campaign after monitoring and evaluating its efficacy. To do so:

1. Go to *Messages* > *Campaigns* from the CleverTap dashboard. The *All Campaigns* page opens.
2. Select the running campaigns you may want to stop and click the ![](https://files.readme.io/c2fcde8-Stop_icon.png) icon.

<Image alt="Stop Selected Campaigns" align="center" border={true} src="https://files.readme.io/b79b1f1cc7220ad4b588ffce7a0ebffc7fdac2ceaaea9663e16ed6aaa0a8858c-Stop_C.png">
  Stop Selected Campaigns
</Image>

3. Click **Save** to stop the selected campaigns or click **Cancel** to undo the action.

Once a campaign is published, you can stop it, but you cannot pause it. Click the ![](https://files.readme.io/0477193c16626ee55e9ef861d13f6cabfcec39dd80e79424384f83c6a9884089-Menu.png)  icon for the campaign you want to stop and click **Stop**.

<Image alt="Stop Campaign" align="center" border={true} src="https://files.readme.io/7bfb3be76729a674dabe4b13a764658f6a1d6155677d66ed436ef78734f71d4d-Stop.png">
  Stop Campaign
</Image>

## Clone Campaign

Cloning a campaign helps create a new campaign from an existing one with minor or no modifications. To do so:

1. Go to *Messages* > *Campaigns* from the CleverTap dashboard. The *All Campaigns* page opens.
2. Click the ![](https://files.readme.io/0477193c16626ee55e9ef861d13f6cabfcec39dd80e79424384f83c6a9884089-Menu.png)  icon for the campaign you want to clone and click **Clone**.

<Image alt="Clone Selected Campaign" align="center" border={true} src="https://files.readme.io/4368a25089f3cac6007bd9badbb19baf8778a8922c90671c13a481b740805484-Clone.png">
  Clone Selected Campaign
</Image>

## Edit Campaigns

All active campaigns except those in the *Stopped*, *Completed*, *Rejected*, or *Draft* state can be edited. To do so: 

1. Go to *Messages* > *Campaigns* from the CleverTap dashboard. The *All Campaigns* page opens.
2. Click the ![](https://files.readme.io/0477193c16626ee55e9ef861d13f6cabfcec39dd80e79424384f83c6a9884089-Menu.png)  icon for the campaign you want to edit and click **Edit**.

<Image alt="Edit" align="center" border={true} src="https://files.readme.io/1e76dcb3b0ebff7ed6031037eac198c55463684d61fc92824d89ef08d9d102f6-Edits.png">
  Edit
</Image>

You can also click this icon to open the campaign in a new tab and edit it. In case the campaign is completed, you can view stats.

<Image alt="Open in new tab" align="center" border={true} src="https://files.readme.io/eb612e1bd7f734ae78e90d9c2fd23a2372d7b66213b44869dbc370e53861ff01-OPen_in_new_tab.png">
  Open in new tab
</Image>

# Campaign States

Campaign Status helps track progress and manage campaigns efficiently. Each campaign state has distinct characteristics that determine what actions can be performed. The following are the campaign states:

* *Draft*: Indicates that the campaign is still not published.
* *Scheduled*: Indicates that the campaign is set to go live in the future.
* *Awaiting Next Run*: Indicates that the recurring campaign is waiting for its subsequent scheduled execution.
* *Running*: Indicates that the campaign is actively being executed.
* *Pending for Approval*: Indicates that the campaign with Creator Approver workflow is awaiting review and approval from the designated approver before it can be published or scheduled for execution
* *Rejected*: Indicates that the campaign with Creator Approver workflow has not been approved by the designated approver.
* *Stopped*: Indicates that the campaign has been permanently halted.
* *Completed*: Indicates that the campaign has finished running and is no longer active.

For Campaigns Scheduled for Later, you can edit the following sections of the campaign: Who, What, and When.

For Live Campaigns Awaiting Next Run, you can edit the following: *What* section, Campaign name, and Message labels.

For Campaigns with Creator Approver Workflow, refer to the following table:

| Campaign State           | Scenario                                           | Creator's Action                                                                                                                                                   | Approver's Action                                                                                                                                                                                                                                              |
| :----------------------- | :------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Scheduled**            | Before scheduled time                              | Can edit all campaign information and send it for approval.                                                                                                        | Can edit all campaign information and publish.                                                                                                                                                                                                                 |
|                          | After scheduled time                               | Cannot edit; popup indicating discarded changes displays                                                                                                           | Can only approve; popup indicating discarded changes..                                                                                                                                                                                                         |
|                          |                                                    |                                                                                                                                                                    |                                                                                                                                                                                                                                                                |
| **Awaiting Next Run**    | Before scheduled time                              | Can modify only the *What* section and send it for approval.                                                                                                       | Can modify only the *What* section and publish.                                                                                                                                                                                                                |
|                          | After scheduled time                               | Cannot edit; popup indicating discarded changes displays.                                                                                                          | Can only approve; popup indicating discarded changes.                                                                                                                                                                                                          |
|                          |                                                    |                                                                                                                                                                    |                                                                                                                                                                                                                                                                |
| **Running**              | During execution                                   | Can modify only the *What* section of Live campaigns and send them for approval.                                                                                   | Can modify only the *What* section of Live campaigns and publish.                                                                                                                                                                                              |
|                          |                                                    |                                                                                                                                                                    |                                                                                                                                                                                                                                                                |
| **Pending For Approval** | Before First run                                   | Can edit all campaign information before and after the scheduled time and send it for approval.                                                                    | <li>Can edit all the campaign information **before the scheduled time** and approve the campaign.</li><li>Popup indicating that the campaign was scheduled in the past time; The approver can edit all the campaign information and publish the campaign.</li> |
|                          | First run was completed, and awaiting the next run | Can only edit the *What* section before the next scheduled time.                                                                                                   |                                                                                                                                                                                                                                                                |
|                          |                                                    | The creator can edit only the WHAT section **before the scheduled time** and send it to the approver for approval.                                                 | The approver can edit only the WHAT section **before the scheduled time** and publish the campaign.                                                                                                                                                            |
|                          |                                                    | If the creator tries to edit the campaign **after the scheduled time**, a popup opens. The popup indicates that the changes made by the creator will be discarded. | If the approver tries to edit the campaign **after the scheduled time**, a popup opens. The popup indicates that the changes made by the creator will be discarded.                                                                                            |
|                          |                                                    |                                                                                                                                                                    |                                                                                                                                                                                                                                                                |
| **Rejected**             | First run is yet to start                          | The creator can edit all the campaign information **before the scheduled time** and send it to the approver for approval.                                          | The approver can edit only the WHAT section **before the scheduled time** and send it to the approver for approval.                                                                                                                                            |
|                          |                                                    | The creator can edit all the campaign information **after the scheduled time** and send it to the approver for approval.                                           | If the approver tries to edit the campaign **after the scheduled time**, a popup opens. The popup indicates that the changes made by the approver will be discarded.                                                                                           |
|                          |                                                    |                                                                                                                                                                    |                                                                                                                                                                                                                                                                |
|                          | First run was completed, and awaiting the next run | The creator can edit only the WHAT section **before the scheduled time** and send it to the approver for approval.                                                 | The approver can edit only the WHAT section **before the scheduled time** and publish the campaign.                                                                                                                                                            |
|                          |                                                    | If the creator tries to edit the campaign **after the scheduled time**, they can edit only the WHAT section and send it to the approver for approval.              | The approver can only edit the WHAT section of the campaign after the scheduled time. Also, a popup indicates that the campaign can be run today or tomorrow.                                                                                                  |
