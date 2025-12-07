---
title: Campaign Reports_Export Options
excerpt: View comprehensive reports for your Campaigns
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

Campaign reports provide you with campaign performance at a glance. Using these reports, you can compare campaigns' performance and understand engagement trends. You can email or export the summary report of all campaigns sent out for a specific period or even for a specific day. This report includes metrics such as campaign deliveries, engagements, conversions, and errors. To optimize dashboard performance, the data in the report is cached, and you can receive data that has been generated up to 4 hours earlier. The report may take up to 6 hours, depending on the other activities happening when requesting the report.

# Generate Reports

You can view the campaigns from the campaigns list page. Follow the steps to view a report:

1. Navigate to _Campaigns_ page from the main menu. The _All Campaigns_ page opens.
2. Select the campaigns or select the filter criteria to export the reports for the required campaigns.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/bd1b02d-Subscribe_to_Reports.gif",
        "Subscribe to Reports.gif",
        1376
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



3. Click the ![Email Report](https://files.readme.io/5e252c3-Email_Report_icon.jpg) icon or the ![Subscribe to Reports](https://files.readme.io/f0ac781-Click_Subscribe_to_report_link.png) link. The Campaign Report window opens on the right side.

4. Configure the following settings:  

| <p>Field</p>                | <p>Description</p>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Report name</p>          | <p>Enter the name to identify your report uniquely.</p>                                                                                                                                                                                                                                                                                                                                                                                            |
| <p>Create a report. for</p> | <p>Select from the following options for which you want to create a report:</p><ul><li>Selected Campaigns - Generates reports only for the campaigns selected from the list. </li><li>All campaigns with filters applied - Generates report for all the campaigns displayed after applying filters on the campaigns list page.</li></ul>                                                                                                           |
| <p>Data to include</p>      | <p>Select the data from the following options that you want to include in the report:</p><ul><li>Campaign overview</li><li>Campaign stats</li><li>Campaign detailed stats</li><li>Campaign errors</li></ul>                                                                                                                                                                                                                                        |
| <p>Split all data by</p>    | <p>Select the option to split your data. The following are the available options:</p><ul><li>Day</li><li>OS</li><li>Variant type</li></ul>                                                                                                                                                                                                                                                                                                         |
| <p>Frequency</p>            | <p>Select the export frequency for your report. The following are the available options:</p><ul><li>One-time</li><li>Recurring</li></ul>                                                                                                                                                                                                                                                                                                           |
| <p>Delivery Method</p>      | <p>Select from the following delivery options:</p><ul><li><strong>Email</strong>: You must enter the recipient's email address when you select this option. </li><li><strong>Partner Export</strong>: Select any one from the following export partners and then select the bucket where you want to export the reports: <ul><li>Amazon S3 </li><li>Google Cloud Platform</li></ul></li></ul><p>The reports are always exported in CSV format.</p> |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9e45c4e-Campaign_Reports.png",
        "Campaign Reports.png",
        1696
      ],
      "align": "center",
      "sizing": "smart",
      "border": true
    }
  ]
}
[/block]



5. Click **Send Report** to send the report immediately or click **Subscribe** to send the reports at defined intervals.

You can include _Campaign stats_ and _Campaign overview_ in the campaign report for a maximum of 2500 campaigns. 

> 📘 Campaign Reports Enhancement in Private Beta
> 
> You can now include _Campaign details stats_ in the campaign report for a maximum of 2000 campaigns, which was 100 campaigns earlier. This enhancement is currently available in Private Beta.

# Subscribe to Reports

You may want to subscribe to a report in various scenarios. For example, select and subscribe to four campaigns on a monthly recurrence, or only subscribe to push campaigns that you created with a label for a monthly/daily recurrence.  
The subscriptions are displayed on the _Subscriptions_ tab of the _Campaign Report_ window. To create a new report or create a new report subscription, refer to [Genetate Reports](doc:campaign-reports#generate-reports).

# Edit/Delete Reports

The existing schedule for the reports is displayed on the _Subscribe_ tab. To edit or delete a subscription to a report,  

1. Click **Subscribe to Reports** on the campaign list page. The Campaign Summary Emails pane appears.
2. Select the _Subscriptions_ tab
3. Click the ellipsis icon to edit or delete a report subscription.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/95f9da4-Edit_subscriptions.gif",
        "Edit_subscriptions.gif",
        570
      ],
      "align": "center",
      "border": true
    }
  ]
}
[/block]



# Reports API

You can use the [Get Campaign Report API](https://developer.clevertap.com/docs/get-campaign-report-api) to programmatically generate campaign reports for your consumption.

# Campaign Report Data

The following table provides all the report's columns based on the selected data group. For example, the first column, Campaign ID, will be part of each report, irrespective of the data group.  
However, the Campaign Name appears as a column in your report only if you select _Campaign overview_ when requesting the report.

> 📘 Send Copy of Push Campaign to App Inbox
> 
> When you choose to send a copy of a Push campaign to the App Inbox, it appears as a single campaign on the _All Campaigns_ page on the dashboard. However, you will see two separate entries for the campaign in the campaign reports.

| <p>Report Column</p>                     | <p>Campaign overview</p> | <p>Campaign stats</p> | <p>Campaign detailed stats</p> | <p>Campaign errors</p> | <p>Description</p>                                                                                             |
| :--------------------------------------- | :----------------------- | :-------------------- | :----------------------------- | :--------------------- | :------------------------------------------------------------------------------------------------------------- |
| <p>Campaign ID</p>                       | <p>Yes</p>               | <p>Yes</p>            | <p>Yes</p>                     | <p>Yes</p>             | <p>The unique ID for the campaign.</p>                                                                         |
| <p>Campaign Name</p>                     | <p>Yes</p>               |                       |                                |                        | <p>The name provided for the campaign during its creation.</p>                                                 |
| <p>Channel</p>                           | <p>Yes</p>               |                       |                                |                        | <p>The channel such as Email, Mobile Push, and so on that is used for the campaign.</p>                        |
| <p>Delivery</p>                          | <p>Yes</p>               |                       |                                |                        | <p>The campaign delivery such as Action, Inaction, One time, and so on.</p>                                    |
| <p>Type</p>                              | <p>Yes</p>               |                       |                                |                        | <p>The type of campaign such as single message, message on user property, or A/B test.</p>                     |
| <p>Variant</p>                           | <p>Yes</p>               |                       |                                |                        | <p>The message variant. Applicable only to A/B test messages and message on user property.</p>                 |
| <p>OS</p>                                | <p>Yes</p>               |                       |                                |                        | <p>The device operating system, such as iOS and Android.</p>                                                   |
| <p>Device</p>                            | <p>Yes</p>               |                       |                                |                        | <p>Devices such as mobile, TV, or a Tablet.</p>                                                                |
| <p>DND / set campaign frequency</p>      | <p>Yes</p>               |                       |                                |                        | <p>DND or campaign frequency setting configured at the time of campaign creation.</p>                          |
| <p>timezone</p>                          | <p>Yes</p>               |                       |                                |                        | <p>Configuration for the delivery in the user timezone.</p>                                                    |
| <p>cutoff</p>                            | <p>Yes</p>               |                       |                                |                        | <p>Configuration of the cutoff period after which the campaign is not delivered.</p>                           |
| <p>fcap (global campaign limits)</p>     | <p>Yes</p>               |                       |                                |                        | <p>Configuration for the  maximum number of messages that a user can receive in a day.</p>                     |
| <p>throttle</p>                          | <p>Yes</p>               |                       |                                |                        | <p>Configuration for the  throttle limits applied to the campaigns.</p>                                        |
| <p>Safety check limit</p>                | <p>Yes</p>               |                       |                                |                        | <p>The campaign is not sent to any user if the number of qualified users exceed the limit.</p>                 |
| <p>Campaign per day limit</p>            | <p>Yes</p>               |                       |                                |                        | <p>Number of maximum messages sent per day for the campaign.</p>                                               |
| <p>Campaign overall limit</p>            | <p>Yes</p>               |                       |                                |                        | <p>Number of maximum messages sent overall for the campaign.</p>                                               |
| <p>estimated reach</p>                   | <p>Yes</p>               |                       |                                |                        | <p>Estimated qualification of users.</p>                                                                       |
| <p>Reach (Send to all / last active)</p> | <p>Yes</p>               |                       |                                |                        | <p>Send to all devices or the last active device.</p>                                                          |
| <p>WHO query</p>                         | <p>Yes</p>               |                       |                                |                        | <p>The who query defined in the campaign.</p>                                                                  |
| <p>Constant event property</p>           | <p>Yes</p>               |                       |                                |                        | <p>Shows whether the Constant event property is applicable or not.</p>                                         |
| <p>Title</p>                             | <p>Yes</p>               |                       |                                |                        | <p>The title of the notification</p>                                                                           |
| <p>Message</p>                           | <p>Yes</p>               |                       |                                |                        | <p>Message of the notification.</p>                                                                            |
| <p>iOS Rich Media type</p>               | <p>Yes</p>               |                       |                                |                        | <p>Media type such as, Single or Carousel for iOS push notifications</p>                                       |
| <p>IOS Rich media URL</p>                | <p>Yes</p>               |                       |                                |                        | <p>Image URL  for iOS push notifications</p>                                                                   |
| <p>IOS sound file</p>                    | <p>Yes</p>               |                       |                                |                        | <p>iOS sound or the file URL if custom.</p>                                                                    |
| <p>IOS Badge Count</p>                   | <p>Yes</p>               |                       |                                |                        | <p>Badge count on IOS notification</p>                                                                         |
| <p>IOS Category</p>                      | <p>Yes</p>               |                       |                                |                        | <p>Category for iOS push notifications (if applicable).</p>                                                    |
| <p>IOS Deep link / External URL</p>      | <p>Yes</p>               |                       |                                |                        | <p>Deep link for iOS push notifications.</p>                                                                   |
| <p>IOS Mutable content</p>               | <p>Yes</p>               |                       |                                |                        | <p>Shows whether the content is mutable. The values are Yes/No.</p>                                            |
| <p>Android Subtitle</p>                  | <p>Yes</p>               |                       |                                |                        | <p>Subtitle of the Android push notifications.</p>                                                             |
| <p>Android Image URL</p>                 | <p>Yes</p>               |                       |                                |                        | <p>Image URL for Android push notifications.</p>                                                               |
| <p>Android Summary</p>                   | <p>Yes</p>               |                       |                                |                        | <p>Summary text for Android push notifications.</p>                                                            |
| <p>Android large Icon URL</p>            | <p>Yes</p>               |                       |                                |                        | <p>Large icon for Android push notifications.</p>                                                              |
| <p>Android Small App Icon colour</p>     | <p>Yes</p>               |                       |                                |                        | <p>Small app icon for Android push notifications.</p>                                                          |
| <p>Android Deep link / External URL</p>  | <p>Yes</p>               |                       |                                |                        | <p>Deep link for Android push notifications.</p>                                                               |
| <p>Android Sound File</p>                | <p>Yes</p>               |                       |                                |                        | <p>The values are:</p><ul><li>NA </li><li>Default OS sound</li><li>file URL,  if the file is custom</li></ul>  |
| Android Notification tray priority       | Yes                      |                       |                                |                        | Shows the priority of display in tray of android device                                                        |
| Android Notification delivery priority   | Yes                      |                       |                                |                        | Server priority for Android push notifications                                                                 |
| Collapse notification                    | Yes                      |                       |                                |                        | Shows whether the notification is collapsible or not                                                           |
| Notification channels                    | Yes                      |                       |                                |                        | Communication channel, for which the user consent is received.                                                 |
| Badge ID                                 | Yes                      |                       |                                |                        | Badge ID for Android push notifications.                                                                       |
| Badge Icon                               | Yes                      |                       |                                |                        | Badge count Android push notifications.                                                                        |
| Send to App Inbox as well                | Yes                      |                       |                                |                        | Applicable only for push. Sent to app inbox as well or not.                                                    |
| Time to live                             | Yes                      |                       |                                |                        | Time for the notification to live in the user device.                                                          |
| SMS/ Email/ WA service provider          | Yes                      |                       |                                |                        | The service provider.                                                                                          |
| Start Date                               | Yes                      |                       |                                |                        | Start date of the campaign.                                                                                    |
| Start Time                               | Yes                      |                       |                                |                        | Displays the start time of the campaign. Displays the time value if the campaign is set to best time.          |
| Conversion Event                         | Yes                      |                       |                                |                        | The conversion is tracked for this event in the campaign.                                                      |
| Conversion Time (in minutes)             | Yes                      |                       |                                |                        | Time period within which conversion is tracked for the campaign.                                               |
| Campaign URL                             | Yes                      |                       |                                |                        | The URL of the campaign to access it on Clevertap dashboard.                                                   |
| Status                                   | Yes                      |                       |                                |                        | Current status of the campaign.                                                                                |
| Created By                               | Yes                      |                       |                                |                        | The creator of the campaign.                                                                                   |
| Created time                             | Yes                      |                       |                                |                        | Time of creating the campaign.                                                                                 |
| Labels                                   | Yes                      |                       |                                |                        | The Labels / tags used to identify and organize campaigns.                                                     |
| AmplifiedByInbox                         | Yes                      |                       |                                |                        | Shows whether the campaign was amplified by sending it to inbox as well or not.                                |
| AmplifiedByPush                          | Yes                      |                       |                                |                        | If Enhanced Push Delivery is applied or not.                                                                   |
| Web Priority                             | Yes                      |                       |                                |                        | Priority of web notifications. It can be High, Medium or low.                                                  |
| Run Date                                 |                          | Yes                   |                                |                        | Applicable for Day-wise reports only. Displays the run date.                                                   |
| Total Sent (users)                       |                          | Yes                   |                                |                        | Displays the total count for the sent users. Shows as N/A for channels that are not supported, such as In-app. |
| Total Viewed (users)                     |                          | Yes                   |                                |                        | Displays the total count for the users who viewed the notification.                                            |
| Total Clicked (users)                    |                          | Yes                   |                                |                        | Displays the total count for the users who clicked the notification.                                           |
| Total Sent (events)                      |                          | Yes                   |                                |                        | Total events. Total devices (if 'Send to all' is applied)                                                      |
| Total Viewed (events)                    |                          | Yes                   |                                |                        | Total events. Total devices (in case of 'Send to all' is applied)                                              |
| Total Clicked (events)                   |                          | Yes                   |                                |                        | Total events. Total devices (in case of 'Send to all' is applied)                                              |
| Errors                                   |                          | Yes                   |                                |                        | Errors                                                                                                         |
| Click through conversions                |                          | Yes                   |                                |                        | Total converting users ( as per funnel, including clicked step)                                                |
| Click through conversions %              |                          | Yes                   |                                |                        | Total converting users / Total sent users.                                                                     |
| Click through conversion revenue         |                          | Yes                   |                                |                        | Revenue as per the revenue property related to Total conversions.                                              |
| Total control group count                |                          | Yes                   |                                |                        | Total number of users in control group.                                                                        |
| Total control group conversions          |                          | Yes                   |                                |                        | Total number of control group users converting.                                                                |
| Total control group conversions %        |                          | Yes                   |                                |                        | Total number of control group users converting / Total number of users in control group.                       |
| Total control group revenue              |                          | Yes                   |                                |                        | Revenue as per revenue property related to conversion.                                                         |
| Unique Sent (users)                      |                          |                       | Yes                            |                        | Unique users who were sent notification                                                                        |
| Unique Viewed Within Conversion Time     |                          |                       | Yes                            |                        | Unique users who viewed the notifications within the set conversion time.                                      |
| Unique Clicked Within Conversion Time    |                          |                       | Yes                            |                        | Unique users who clicked the notifications within set conversion time.                                         |
| Unique Converted Within Conversion Time  |                          |                       | Yes                            |                        | Unique users who converted  within the set conversion time.                                                    |
| Revenue Within Conversion Time           |                          |                       | Yes                            |                        | Revenue as per the revenue property related to conversion.                                                     |
| View through Conversions                 |                          |                       | Yes                            |                        | Users who were sent a message and they converted. Referred as influenced conversions on the dashboard.         |
| View through Conversions %               |                          |                       | Yes                            |                        | Influenced conversion (above) / Total sent users                                                               |
| View through conversions Revenue         |                          |                       | Yes                            |                        | Revenue as per the revenue property related to conversion.                                                     |
| System Control Group Conversions         |                          |                       | Yes                            |                        | Total number of system control group users converting.                                                         |
| System Control Group Conversions %       |                          |                       | Yes                            |                        | Total number of system control group users converting / Total number of users in system control group.         |
| System Control Group Revenue             |                          |                       | Yes                            |                        | Revenue as per the revenue property related to conversion.                                                     |
| Campaign Control Group Conversions       |                          |                       | Yes                            |                        | Total number of campaign control group users converting                                                        |
| Campaign Control Group Conversions %     |                          |                       | Yes                            |                        | Total number of campaign control group users converting / Total number of users in campaign control group.     |
| Campaign Control Group Revenue           |                          |                       | Yes                            |                        | Revenue as per the revenue property related to conversion                                                      |
| Custom Control Group Conversions         |                          |                       | Yes                            |                        | Total number of custom control group users converting.                                                         |
| Custom Control Group Conversions %       |                          |                       | Yes                            |                        | Total number of custom control group users converting / Total number of users in custom control group.         |
| Custom Control Group Revenue             |                          |                       | Yes                            |                        | Revenue as per the revenue property related to conversion.                                                     |
| Custom Control Group Name                |                          |                       | Yes                            |                        | Name of the custom control group.                                                                              |
| System Control Group Count               |                          |                       | Yes                            |                        | Total number of users in system control group.                                                                 |
| Custom Control Group count               |                          |                       | Yes                            |                        | Total number of users in custom control group.                                                                 |
| Campaign Control Group count             |                          |                       | Yes                            |                        | Total number of users in campaign control group.                                                               |
| Invalid FCM key                          |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| App uninstalled(Android)                 |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| Wrong FCM API key                        |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| Invalid APNS certificate                 |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| APNS error                               |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| APNS Format error                        |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| APNS Account Temporarily Blacklisted     |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| App Uninstalled(iOS)                     |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| Invalid Profiles                         |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| Duplicate APNS Token                     |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| Invalid token - FCM                      |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| Unknown error - FCM                      |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| Dispatch error                           |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| Internal error due to amplification      |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| Global frequency cap exceeded            |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| Campaign frequency cap exceeded          |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| Campaign limit reached for day           |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| Campaign limit reach for run             |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| Profile not reachable                    |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| Campaign stopped                         |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| User DND                                 |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| Duplicate profile for channel            |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| APNS bad topic error                     |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| APNS disallowed topic                    |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| APNS bad device token                    |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| APNS device token and topic mismatch     |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| APNS inactive device token for topic     |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| APNS wrong environment certificate       |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| APNS bad certificate                     |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| APNS idle timeout                        |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| APNS missing certificate topic           |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| APNS Bad Priority                        |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| FCM payload too large                    |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| User not reachable                       |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| User not qualified                       |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| Notification during campaign DND         |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |
| Campaign cut-off time reached            |                          |                       |                                | Yes                    | Campaign error description.                                                                                    |