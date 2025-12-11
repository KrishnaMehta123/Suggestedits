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

You can perform different actions on the campaigns from the _All Campaigns_ page, including filtering, labeling, editing, archiving, stopping, cloning, and analyzing performance. The following sections briefly discuss each operation.

## Filter Campaigns

You can use filters to quickly search your campaigns by Status, Channel, Time Period, creator, and more. To do so:

1. Go to _Messages_ > _Campaigns_ from the CleverTap dashboard. The _All Campaigns_ page opens.
2. Click the ![](https://files.readme.io/ac0ed6a-Filter_icon.png) icon. The _Filters_ window opens on the left side of the screen.

<Image align="center" alt="Filter Campaigns" border={true} caption="Filter Campaigns" src="https://files.readme.io/8cd9b547d48c83a96dd0269e92389e13d056f0c79334e187826806ab27e6d39a-listing.png" />

3. Select the required filters and click **Apply** to view results on the _All Campaigns_ page.
4. Click **Reset** to reset all the applied filters.

Filters are divided into two main sections, Active and Archived. Refer to the table below for filter operations:

<Table align={["left","left","left"]}>
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
        * <br />
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
        * <br />
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
> * By default, the date range for **Created** campaigns is _All time_.
> * By default, the date range for **Stats** campaigns is the _last 30 days_. The _All time range_ is unavailable for Stats.
> * Resetting reverts the Time Period filters to default values.
> * Date ranges saved in filters are relative to the current date. For example, a _past 2 days_ filter saved on July 2nd will show July 1st–2nd as the date range. When applied on July 20th, it shows July 19th–20th as the date range.

Filters are only applied after you click **Apply**. If you create a filter and do not select **Apply**, the filter criteria are still displayed but not applied directly in the listing view.

All filters except the _Delivery Type_ and _Segment Type_ filters also have individual reset options. You can reset a specific filter and click **Apply** to immediately see the updated results in the campaign list.

## Edit Columns

You can customize the campaign listing view to match your preferences. Click the _Edit Columns_ icon to select and reorder the columns you want displayed on the campaign list. You can view up to 2000 campaigns on the listing page.

The Sent column is toggled off by default. An Engagement Rate column is available to show channel-specific stats.

<Image align="center" alt="Edit Columns" border={true} caption="Edit Columns" src="https://files.readme.io/be3e0d05ae3e25119258ccd03b2cbf862937e840c4991064f92c2dbf0f0b1599-2025-12-11_18-40-00_1.gif" />

> 📘 Note
>
> * In the All Campaigns view, each campaign shows the associated Team.
> * Users can view and manage only the campaigns tied to their respective teams. This ensures visibility and access are aligned with your RBAC configuration.

## Campaign Reports

Selecting _Campaigns_ from the CleverTap Dashboard opens the Campaign Reports table where you can see all your campaigns across every channel in one consolidated view. Campaign Reports include the channel, delivery status, and key statistics to assess and compare performance.

Click Subscribe to reports and enter the details.

<Image align="center" alt={1422} border={true} caption="Filter Campaigns and View Campaign Reports" title="Filter Campaigns and view Campaign reports on CleverTap dashboard." src="https://files.readme.io/4179196a7509ec3d78977a0a4dee6e936edd8ae82e008a16a471d33cfbac1d64-2025-12-11_18-42-58.png" />

You can also email a report by selecting the campaign and clicking the email report icon.

<Image align="center" alt="Email Report" border={true} caption="Email Report" src="https://files.readme.io/815637006b08ebe05fae735f88e536af058eac46685c9c7e3e7b3fd57187d474-2025-12-11_18-46-35.png" />

If the report section opens with _All Time_ as the selected time period, requesting the report will automatically adjust the date range to ±15 days. A warning message will be displayed to inform the user of this change. For more details, refer to [Campaign Reports](https://staging.docs.user.clevertap.net/docs/campaign-reports-copy).

## Add Labels

Labels allow you to tag campaigns with descriptive names or themes. Once applied, labels allow you to group your various messaging campaigns so that you can view their performance or identify user behaviors. For example, you can create a label called _Onboarding_ to identify all the messaging campaigns (across all channels) related to onboarding your new users.

You can select up to 10 labels for a campaign. If a campaign already has more than 10 labels assigned from earlier configurations, they will still be visible under _Selected Labels_. However, in such cases, the user will not be able to select any additional labels.

> 📘 Naming Labels
>
> The labels cannot start with or contain the following symbols: ”, , %, >, \<, and !.

You can create and apply labels from the _All Campaigns_ or the _All Journeys_ page. Labels can be applied to individual campaigns from the All Campaigns page during creation. To do so:

1. Go to _Messages_ > _Campaigns_ from the CleverTap dashboard. The _All Campaigns_ page opens.
2. Select the campaigns you may want to label and click the _Add Label_ icon.
3. Select the labels you want to add. These labels are moved to the _Selected Tag ID_ section. Click **Deselect** to remove any label.
4. Click **Apply**.

<Image align="center" alt="Create Multiple Message Labels" border={true} caption="Create and Assign Multiple Message Labels" src="https://files.readme.io/3dd944e95bec99bc93eba8c1d3a729042e52cc3085530098ae42ee79e531f8fa-2025-12-11_18-49-11_1.gif" />

> 📘 Note
>
> * When applying labels in bulk, the selected labels are applied to _all_ selected campaigns. However, if you later select an individual campaign from that group, the bulk-applied labels do not automatically appear in the _Selected Tag ID_ section.
> * To view or manage the labels for a specific campaign, click the **Labels** icon next to the campaign.
>
> <Image align="center" border={true} src="https://files.readme.io/5ca549107a2598ece1d563f64e3d7e96bc164fa520e76bbe7ced774f45d0dbdd-labelsss.png" className="border" />

You can view and export all labels to a CSV file from the _Settings_ >  _Setup_  > _Labels_  page. You can also edit or delete labels from this page.

<Image align="center" alt="View Labels" border={true} caption="View Labels" src="https://files.readme.io/e96d91674fd5178c48dcf69813fcd9110249717e1d5ffe42e5ed79ab4c8a7dcc-image.png" width="100% " />

## Archive Campaigns

Archiving campaigns helps to keep your CleverTap account organized and clutter-free, making it easy to find and view the campaigns you want. To do so:

1. Go to _Messages_ > _Campaigns_ from the CleverTap dashboard. The _All Campaigns_ page opens.
2. Select the campaigns you may want to archive and click the Archive icon.
3. Click **Save** to archive the selected campaigns or click **Cancel** to undo the action.

Running campaigns cannot be archived.

<Image align="center" alt="Archive Selected Campaigns" border={true} caption="Archive Selected Campaigns" src="https://files.readme.io/99629a5f98ff342e202d24b02c1cadc12487899a05aba35b50bef7086acb34d9-2025-12-11_18-46-35.png" />

> 📘 Note
>
> * Campaigns in Completed or Stopped state are automatically archived after 6 months. To view archived campaigns, click _Filters_ and select the _Archived_ filter.
> * Archived campaigns cannot be unarchived.
> * All archived campaigns (including drafts) are read‑only and cannot be published. To continue working on an archived campaign, clone it. The clone is treated as a new campaign. You can **Save as draft**, **schedule**, or **publish** the cloned (new) campaign.

## Stop Campaigns

You may want to stop a particular campaign after monitoring and evaluating its efficacy. To do so:

1. Go to _Messages_ > _Campaigns_ from the CleverTap dashboard. The _All Campaigns_ page opens.
2. Select the running campaigns you may want to stop and click the ![](https://files.readme.io/c2fcde8-Stop_icon.png) icon.

<Image align="center" alt="Stop Selected Campaigns" border={true} caption="Stop Selected Campaigns" src="https://files.readme.io/0acbeac73896e43f91a0d5f1fbac522c355109387b7123260d23ca6b763ad48a-2025-12-11_18-46-35.png" />

3. Click **Save** to stop the selected campaigns or click **Cancel** to undo the action.

Once a campaign is published, you can stop it, but you cannot pause it. Click the ![](https://files.readme.io/0477193c16626ee55e9ef861d13f6cabfcec39dd80e79424384f83c6a9884089-Menu.png)  icon for the campaign you want to stop and click **Stop**.

<Image align="center" alt="Stop Campaign" border={true} caption="Stop Campaign" src="https://files.readme.io/e6ba3f73e785f15879df03cfd98f6909e8d660e8fc480a03a407cbd362e83413-2025-12-11_18-55-42.png" />

## Clone Campaign

Cloning a campaign helps create a new campaign from an existing one with minor or no modifications. To do so:

1. Go to _Messages_ > _Campaigns_ from the CleverTap dashboard. The _All Campaigns_ page opens.
2. Click the ![](https://files.readme.io/0477193c16626ee55e9ef861d13f6cabfcec39dd80e79424384f83c6a9884089-Menu.png)  icon for the campaign you want to clone and click **Clone**.

<Image align="center" alt="Clone Selected Campaign" border={true} caption="Clone Selected Campaign" src="https://files.readme.io/60ef9756f17593efaf98027f43705cc7449505d10e17fe267808760f050d5d23-2025-12-11_18-54-21.png" />

## Edit Campaigns

All active campaigns except those in the _Stopped_, _Completed_, _Rejected_, or _Draft_ state can be edited. To do so:

1. Go to _Messages_ > _Campaigns_ from the CleverTap dashboard. The _All Campaigns_ page opens.
2. Click the ![](https://files.readme.io/0477193c16626ee55e9ef861d13f6cabfcec39dd80e79424384f83c6a9884089-Menu.png)  icon for the campaign you want to edit and click **Edit**.

<Image align="center" alt="Edit" border={true} caption="Edit" src="https://files.readme.io/57c10e73ccc5ba961fff9979c67d1fa1f8020d2baf1f0400522e78a252c7400c-2025-12-11_18-54-21.png" />

You can also click this icon to open the campaign in a new tab and edit it. In case the campaign is completed, you can view stats.

<Image align="center" alt="Open in new tab" border={true} caption="Open in new tab" src="https://files.readme.io/ac1b1098e0325f2b3628a62366e0f4027f5396a06c35904cd6e110c0ef23302a-labelsss.png" />

<Callout icon="📘" theme="info">
  # Role-Based Access Control (RBAC) enforcement for campaign actions

  The campaign listing page supports Role-Based Access Control (RBAC) to ensure users can only perform actions that align with their assigned roles and team permissions.

  A user should first have access to the Campaigns or Journeys in general. From there, their channel-level permissions determine their role within each channel:

  * Read access: If users have read access to Push Campaigns, they can view content for all Push Campaigns.
  * Write access: If users have write access to certain Campaigns, they can create, edit, clone, publish, or delete content, but only for channels where they have been explicitly granted channel-level write access.

  For more information, refer to [Channel Level Access](https://docs.clevertap.com/docs/role-based-access-control#channel-level-access).

  ### Access Behavior

  Refer to the following table for access behaviour. This applies to all actions across both Active and Archived campaigns.

  | **Access Type**  | **What the user can do**                                                           |
  | ---------------- | ---------------------------------------------------------------------------------- |
  | **Write Access** | Full control over campaigns: Create, Edit, Clone, Archive, Stop, Start, Add Labels |
  | **Read Access**  | View campaign details, apply filters, and email campaign reports                   |

  ### Error Handling

  If a user attempts an action they don’t have permission for (for example, editing a campaign without write access), an error message is shown indicating insufficient permissions.

  Add ss
</Callout>

# Campaign States

Campaign Status helps track progress and manage campaigns efficiently. Each campaign state has distinct characteristics that determine what actions can be performed. The following are the campaign states:

* _Draft_: Indicates that the campaign is still not published.
* _Scheduled_: Indicates that the campaign is set to go live in the future.
* _Awaiting Next Run_: Indicates that the recurring campaign is waiting for its subsequent scheduled execution.
* _Running_: Indicates that the campaign is actively being executed.
* _Pending for Approval_: Indicates that the campaign with Creator Approver workflow is awaiting review and approval from the designated approver before it can be published or scheduled for execution
* _Rejected_: Indicates that the campaign with Creator Approver workflow has not been approved by the designated approver.
* _Stopped_: Indicates that the campaign has been permanently halted.
* _Completed_: Indicates that the campaign has finished running and is no longer active.

For Campaigns Scheduled for Later, you can edit the following sections of the campaign: Who, What, and When.

For Live Campaigns Awaiting Next Run, you can edit the following: _What_ section, Campaign name, and Message labels.

For Campaigns with Creator Approver Workflow, refer to the following table:

| Campaign State           | Scenario                                           | Creator's Action                                                                                                                                                   | Approver's Action                                                                                                                                                                                                                                              |
| :----------------------- | :------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Scheduled**            | Before scheduled time                              | Can edit all campaign information and send it for approval.                                                                                                        | Can edit all campaign information and publish.                                                                                                                                                                                                                 |
|                          | After scheduled time                               | Cannot edit; popup indicating discarded changes displays                                                                                                           | Can only approve; popup indicating discarded changes..                                                                                                                                                                                                         |
|                          |                                                    |                                                                                                                                                                    |                                                                                                                                                                                                                                                                |
| **Awaiting Next Run**    | Before scheduled time                              | Can modify only the _What_ section and send it for approval.                                                                                                       | Can modify only the _What_ section and publish.                                                                                                                                                                                                                |
|                          | After scheduled time                               | Cannot edit; popup indicating discarded changes displays.                                                                                                          | Can only approve; popup indicating discarded changes.                                                                                                                                                                                                          |
|                          |                                                    |                                                                                                                                                                    |                                                                                                                                                                                                                                                                |
| **Running**              | During execution                                   | Can modify only the _What_ section of Live campaigns and send them for approval.                                                                                   | Can modify only the _What_ section of Live campaigns and publish.                                                                                                                                                                                              |
|                          |                                                    |                                                                                                                                                                    |                                                                                                                                                                                                                                                                |
| **Pending For Approval** | Before First run                                   | Can edit all campaign information before and after the scheduled time and send it for approval.                                                                    | <li>Can edit all the campaign information **before the scheduled time** and approve the campaign.</li><li>Popup indicating that the campaign was scheduled in the past time; The approver can edit all the campaign information and publish the campaign.</li> |
|                          | First run was completed, and awaiting the next run | Can only edit the _What_ section before the next scheduled time.                                                                                                   |                                                                                                                                                                                                                                                                |
|                          |                                                    | The creator can edit only the WHAT section **before the scheduled time** and send it to the approver for approval.                                                 | The approver can edit only the WHAT section **before the scheduled time** and publish the campaign.                                                                                                                                                            |
|                          |                                                    | If the creator tries to edit the campaign **after the scheduled time**, a popup opens. The popup indicates that the changes made by the creator will be discarded. | If the approver tries to edit the campaign **after the scheduled time**, a popup opens. The popup indicates that the changes made by the creator will be discarded.                                                                                            |
|                          |                                                    |                                                                                                                                                                    |                                                                                                                                                                                                                                                                |
| **Rejected**             | First run is yet to start                          | The creator can edit all the campaign information **before the scheduled time** and send it to the approver for approval.                                          | The approver can edit only the WHAT section **before the scheduled time** and send it to the approver for approval.                                                                                                                                            |
|                          |                                                    | The creator can edit all the campaign information **after the scheduled time** and send it to the approver for approval.                                           | If the approver tries to edit the campaign **after the scheduled time**, a popup opens. The popup indicates that the changes made by the approver will be discarded.                                                                                           |
|                          |                                                    |                                                                                                                                                                    |                                                                                                                                                                                                                                                                |
|                          | First run was completed, and awaiting the next run | The creator can edit only the WHAT section **before the scheduled time** and send it to the approver for approval.                                                 | The approver can edit only the WHAT section **before the scheduled time** and publish the campaign.                                                                                                                                                            |
|                          |                                                    | If the creator tries to edit the campaign **after the scheduled time**, they can edit only the WHAT section and send it to the approver for approval.              | The approver can only edit the WHAT section of the campaign after the scheduled time. Also, a popup indicates that the campaign can be run today or tomorrow.                                                                                                  |
