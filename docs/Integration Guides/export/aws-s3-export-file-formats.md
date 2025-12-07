---
title: Export File Formats
excerpt: Learn about different AWS S3 export files and data formats
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
# Export Format
The CleverTap dashboard allows the data exporting in the following formats: CSV, XML, JSON, and Parquet. Each file exported to the AWS S3 bucket follows a naming convention, and the data presented in each of these files is different. This section provides information about each event's name format and data format exported to the S3 bucket.

## File Name Format 
The following is the naming convention for files exported to theS3 bucket:
[block:code]
{
  "codes": [
    {
      "code": "<export request id>-<timestamp of the export run>-<event name>-<yyyymmdd>-<file index>-<database-id>.<file format>.gz",
      "language": "text"
    }
  ]
}
[/block]
 * Export request ID: The export request ID is generated when you create a request in the CleverTap dashboard. It indicates the timestamp when the export was created.
  * Timestamp of export run: Indicates the timestamp when the export was run.
  * Event name: Indicates the event's name for which the data is included in the file.
  * Date of export run: Indicates the date the export was run.
  * File index: Each export file has a size limit of 100 MB to make it more consumable. CleverTap organizes the event data into smaller chunks spread across multiple files for larger exports. The file index indicates the serial order of the file in the file series. 
  * Database ID: Indicates the database ID of the CleverTap database in which the file is located.
  * File format: Indicates the format of the exported file. It can be either JSON, XML, CSV, or Parquet.

## File Data Format
Data can be exported in the following formats from the CleverTap dashboard:
* JSON
* XML
* CSV
* Parquet

Event data exported is organized by event names. Each file includes information about different properties for the given period.

# File Format for Different Events
This section provides all the file formats for different events exported from the CleverTap dashboard.

## System Events

### App Launched
This event is recorded every time a user launches your application. 
[block:code]
{
  "codes": [
    {
      "code": "{\n  \"ts\": 20220212004131,\n  \"eventName\": \"App Launched\",\n  \"profile\": {\n    \"platform\": \"Android\",\n    \"push_token\": \"fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf\"\n  },\n  \"deviceInfo\": {\n    \"make\": \"samsung\",\n    \"model\": \"SM-G781B\",\n    \"appVersion\": \"4.3.0.0-prod-android12\",\n    \"sdkVersion\": \"40300\",\n    \"osVersion\": \"Others\",\n    \"browser\": \"MobileApp\",\n    \"dpi\": 480,\n    \"dimensions\": {\n      \"width\": 47,\n      \"height\": 115,\n      \"unit\": \"mm\"\n    }\n  },\n  \"eventProps\": {\n    \"CT Network Carrier\": \"airtel\",\n    \"CT Source\": \"Mobile\",\n    \"CT OS Version\": \"12\",\n    \"CT SDK Version\": 40300,\n    \"CT Session Id\": 1644606691,\n    \"CT App Version\": \"4.3.0.0-prod-android12\"\n  }\n}",
      "language": "json"
    },
    {
      "code": "<root>\n<Event>\n    <ts>20220212004131</ts>\n    <eventName>App Launched</eventName>\n    <profile>\n        <platform>Android</platform>\n        <push_token>fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf</push_token>\n    </profile>\n    <deviceInfo>\n        <make>samsung</make>\n        <model>SM-G781B</model>\n        <appVersion>4.3.0.0-prod-android12</appVersion>\n        <sdkVersion>40300</sdkVersion>\n        <osVersion>Others</osVersion>\n        <browser>MobileApp</browser>\n        <dpi>480</dpi>\n        <dimensions>\n            <width>47</width>\n            <height>115</height>\n            <unit>mm</unit>\n        </dimensions>\n    </deviceInfo>\n    <eventProps>\n        <entry>\n            <key>CT Network Carrier</key>\n            <value>airtel</value>\n        </entry>\n        <entry>\n            <key>CT Source</key>\n            <value>Mobile</value>\n        </entry>\n        <entry>\n            <key>CT OS Version</key>\n            <value>12</value>\n        </entry>\n        <entry>\n            <key>CT SDK Version</key>\n            <value>40300</value>\n        </entry>\n        <entry>\n            <key>CT Session Id</key>\n            <value>1644606691</value>\n        </entry>\n        <entry>\n            <key>CT App Version</key>\n            <value>4.3.0.0-prod-android12</value>\n        </entry>\n    </eventProps></root>",
      "language": "xml"
    },
    {
      "code": "ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.CT Network Carrier,eventProps.CT Source,eventProps.ct_app_version,eventProps.CT Bluetooth Version,eventProps.Keyword,eventProps.CT SDK Version,eventProps.CT Bluetooth Enabled,eventProps.CT OS Version,eventProps.CT Network Type,eventProps.Model,eventProps.CT Longitude,eventProps.CT Latitude,eventProps.CT Connected To WiFi,eventProps.CT Session Id,eventProps.CT App Version\n20220307124926,App Launched,,,,Android,,,,fcm:eNf3g3l_RKmYURl-z4psKo:APA91bEKaXMYxVwHWoi8C-sxWyEmhC3fWWRtqGjehfY6sKUx5HARzIe4rors5jouDZdX8gIaQ1C_DKbCMIgKhYD23XmCnpWPyzJIOusZnjtwJjtNrOa0oqSHzJIJ4g-Gsk8AYL3O7Clo,google,sdk_gphone_x86,1.0,40400,11,MobileApp,420,65,104,mm,,Android,Mobile,,,,40400,,11,,,,,,1646637566,1.0",
      "language": "text",
      "name": "CSV"
    }
  ]
}
[/block]
### App Installed
This event is recorded when the user launches the app for the first time.
[block:code]
{
  "codes": [
    {
      "code": "{\n  \"ts\": 20220212004131,\n  \"eventName\": \"App Installed\",\n  \"profile\": {\n    \"platform\": \"Android\",\n    \"push_token\": \"fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf\"\n  },\n  \"deviceInfo\": {\n    \"make\": \"samsung\",\n    \"model\": \"SM-G781B\",\n    \"appVersion\": \"4.3.0.0-prod-android12\",\n    \"sdkVersion\": \"40300\",\n    \"osVersion\": \"Others\",\n    \"browser\": \"MobileApp\",\n    \"dpi\": 480,\n    \"dimensions\": {\n      \"width\": 47,\n      \"height\": 115,\n      \"unit\": \"mm\"\n    }\n  },\n  \"eventProps\": {\n    \"ct_app_version\": \"4.3.0.0-prod-android12\",\n    \"CT Source\": \"Mobile\"\n  }\n}",
      "language": "json"
    },
    {
      "code": "<?xml version='1.0' encoding='UTF-8'?>\n<root>\n<Event>\n    <ts>20220212004131</ts>\n    <eventName>App Installed</eventName>\n    <profile>\n        <platform>Android</platform>\n        <push_token>fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf</push_token>\n    </profile>\n    <deviceInfo>\n        <make>samsung</make>\n        <model>SM-G781B</model>\n        <appVersion>4.3.0.0-prod-android12</appVersion>\n        <sdkVersion>40300</sdkVersion>\n        <osVersion>Others</osVersion>\n        <browser>MobileApp</browser>\n        <dpi>480</dpi>\n        <dimensions>\n            <width>47</width>\n            <height>115</height>\n            <unit>mm</unit>\n        </dimensions>\n    </deviceInfo>\n    <eventProps>\n        <entry>\n            <key>ct_app_version</key>\n            <value>4.3.0.0-prod-android12</value>\n        </entry>\n        <entry>\n            <key>CT Source</key>\n            <value>Mobile</value>\n        </entry>\n    </eventProps></root>",
      "language": "xml"
    },
    {
      "code": "ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.ct_app_version,eventProps.CT Source,eventProps.ct_latitude,eventProps.ct_longitude\n20220330171124,App Installed,,,,Android,,,,,google,Android SDK built for x86,1.0,40400,10,MobileApp,420,65,108,mm,,1.0,Mobile,,\n20220330143803,App Installed,,,,Android,,,,,samsung,SM-M307F,1.0,40400,11,MobileApp,420,65,128,mm,,1.0,Mobile,,",
      "language": "text"
    }
  ]
}
[/block]
### App Uninstalled
This event is recorded when a user uninstalls your application.
[block:code]
{
  "codes": [
    {
      "code": "{\n  \"ts\": 20220212000212,\n  \"eventName\": \"App Uninstalled\",\n  \"profile\": {\n    \"platform\": \"Web\"\n  },\n  \"deviceInfo\": {\n    \"browser\": \"Others\"\n  },\n  \"eventProps\": {\n    \"clevertapId\": \"__g3c83c420053a4bb8a27b665f10aa1677\",\n    \"CT Source\": \"API\",\n    \"source\": \"REALTIME_FIREBASE\"\n  }\n}",
      "language": "json"
    },
    {
      "code": "<?xml version='1.0' encoding='UTF-8'?>\n<root>\n<Event>\n    <ts>20220212041124</ts>\n    <eventName>App Uninstalled</eventName>\n    <profile>\n        <platform>Web</platform>\n    </profile>\n    <deviceInfo>\n        <browser>Others</browser>\n    </deviceInfo>\n    <eventProps>\n        <entry>\n            <key>clevertapId</key>\n            <value>__g577b9e571268456aa8168894f12b0ae2</value>\n        </entry>\n        <entry>\n            <key>CT Source</key>\n            <value>API</value>\n        </entry>\n        <entry>\n            <key>source</key>\n            <value>REALTIME_FIREBASE</value>\n        </entry>\n    </eventProps></root>",
      "language": "xml"
    },
    {
      "code": "ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.CT Network Carrier,eventProps.CT Source,eventProps.ct_app_version,eventProps.CT Bluetooth Version,eventProps.Keyword,eventProps.CT SDK Version,eventProps.CT Bluetooth Enabled,eventProps.CT OS Version,eventProps.CT Network Type,eventProps.Model,eventProps.CT Longitude,eventProps.CT Latitude,eventProps.CT Connected To WiFi,eventProps.CT Session Id,eventProps.CT App Version\n20220307124926,App Launched,,,,Android,,,,fcm:eNf3g3l_RKmYURl-z4psKo:APA91bEKaXMYxVwHWoi8C-sxWyEmhC3fWWRtqGjehfY6sKUx5HARzIe4rors5jouDZdX8gIaQ1C_DKbCMIgKhYD23XmCnpWPyzJIOusZnjtwJjtNrOa0oqSHzJIJ4g-Gsk8AYL3O7Clo,google,sdk_gphone_x86,1.0,40400,11,MobileApp,420,65,104,mm,,Android,Mobile,,,,40400,,11,,,,,,1646637566,1.0\n",
      "language": "text",
      "name": "CSV"
    }
  ]
}
[/block]
### UTM Visited
This event is tracked when a user clicks on a link from a marketing campaign with a UTM parameter defined. This event is also tracked when a CleverTap-integrated attribution platform, such as Branch or Apsalar, sends this information to CleverTap.
[block:code]
{
  "codes": [
    {
      "code": "{\n  \"ts\": 20220212004131,\n  \"eventName\": \"UTM Visited\",\n  \"profile\": {\n    \"platform\": \"Android\",\n    \"push_token\": \"fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf\"\n  },\n  \"deviceInfo\": {\n    \"make\": \"samsung\",\n    \"model\": \"SM-G781B\",\n    \"appVersion\": \"4.3.0.0-prod-android12\",\n    \"sdkVersion\": \"40300\",\n    \"osVersion\": \"Others\",\n    \"browser\": \"MobileApp\",\n    \"dpi\": 480,\n    \"dimensions\": {\n      \"width\": 47,\n      \"height\": 115,\n      \"unit\": \"mm\"\n    }\n  },\n  \"eventProps\": {\n    \"Install\": \"y\"\n  },\n  \"session_props\": {\n    \"session_referrer\": \"wzrk://track?install=true&utm_source=google-play&utm_medium=organic\",\n    \"utm_medium\": \"organic\",\n    \"session_source\": \"Others\",\n    \"utm_source\": \"google-play\"\n  }\n}",
      "language": "json"
    },
    {
      "code": "<?xml version='1.0' encoding='UTF-8'?>\n<root>\n<Event>\n    <ts>20220212004131</ts>\n    <eventName>UTM Visited</eventName>\n    <profile>\n        <platform>Android</platform>\n        <push_token>fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf</push_token>\n    </profile>\n    <deviceInfo>\n        <make>samsung</make>\n        <model>SM-G781B</model>\n        <appVersion>4.3.0.0-prod-android12</appVersion>\n        <sdkVersion>40300</sdkVersion>\n        <osVersion>Others</osVersion>\n        <browser>MobileApp</browser>\n        <dpi>480</dpi>\n        <dimensions>\n            <width>47</width>\n            <height>115</height>\n            <unit>mm</unit>\n        </dimensions>\n    </deviceInfo>\n    <eventProps>\n        <entry>\n            <key>Install</key>\n            <value>y</value>\n        </entry>\n    </eventProps>\n    <sessionProps>\n        <entry>\n            <key>session_referrer</key>\n            <value>wzrk://track?install=true&amp;utm_source=google-play&amp;utm_medium=organic</value>\n        </entry>\n        <entry>\n            <key>utm_medium</key>\n            <value>organic</value>\n        </entry>\n        <entry>\n            <key>session_source</key>\n            <value>Others</value>\n        </entry>\n        <entry>\n            <key>utm_source</key>\n            <value>google-play</value>\n        </entry>\n    </sessionProps>\n</Event>\n</root>",
      "language": "xml"
    },
    {
      "code": "ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.wzrk_cts,eventProps.firstname,eventProps.CT Source,eventProps.wzrk_push_amp,eventProps.wzrk_ck,eventProps.utm_medium,eventProps.ltmpl,eventProps.wzrk_sound,eventProps.wzrk_ttl_s,eventProps.UTM,eventProps.wzrk_c2a,eventProps.feature,eventProps.provider,eventProps.wzrk_pid,eventProps.continue,eventProps.Campaign id,eventProps.browser,eventProps.action,eventProps.CT Latitude,eventProps.Install,eventProps.Campaign type,eventProps.CT App Version,eventProps.wzrk_acct_id,eventProps.utm_campaign,eventProps.wzrk_pivot,eventProps.wzrk_dl,eventProps.wzrk_cid,eventProps.wzrk_bi,eventProps.wzrk_bc,eventProps.wzrk_rnv,eventProps.wzrk_pn,eventProps.RAW_STRING,eventProps.passive,eventProps.lastname,eventProps.0,eventProps.1,eventProps.followup,eventProps.2,eventProps.time_continue,eventProps.wzrk_id,eventProps.wzrk_ttl,eventProps.v,eventProps.service,eventProps.CT Longitude,eventProps.wzrk_animated,eventProps.wzrk_bp,eventProps.wzrk_dt,eventProps.utm_source,sessionProps.utm_campaign,sessionProps.session_referrer,sessionProps.utm_medium,sessionProps.session_source,sessionProps.utm_source\n20220307124926,UTM Visited,,,,Android,,,,fcm:eNf3g3l_RKmYURl-z4psKo:APA91bEKaXMYxVwHWoi8C-sxWyEmhC3fWWRtqGjehfY6sKUx5HARzIe4rors5jouDZdX8gIaQ1C_DKbCMIgKhYD23XmCnpWPyzJIOusZnjtwJjtNrOa0oqSHzJIJ4g-Gsk8AYL3O7Clo,google,sdk_gphone_x86,1.0,40400,11,MobileApp,420,65,104,mm,,,,,,,,,,,,,,,,,,,,,y,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,wzrk://track?install=true&utm_source=google-play&utm_medium=organic,organic,Others,google-play",
      "language": "text",
      "name": "CSV"
    }
  ]
}
[/block]
### Notification Sent
This event is tracked when a campaign message is sent to a user. This event is always recorded, even if the user does not open or click on the message. This event is recorded for email, mobile push, SMS, and web push campaigns. The Notification Sent event is available on the Event dashboard, but it is not displayed on the User Profile.
[block:code]
{
  "codes": [
    {
      "code": "{\n  \"ts\": 20220212210100,\n  \"eventName\": \"Notification Sent\",\n  \"profile\": {\n    \"all_identities\": [\n      \"testingmom@gmail.com\"\n    ],\n    \"platform\": \"Android\",\n    \"email\": \"testingmom@gmail.com\",\n    \"push_token\": \"fcm:ffvb4LIsf3k:APA91bHtWKK-Zl4Ba-7iJ-Y8v9sAzjGxtHVNN2BZnksiLuFaUOZ7D3plpA2R79Xx-MDv2jdl9OFlI1a1LSagT8bjEUHyaQTBBuEto45ipAFjDHq2RdMS9qgGi0nZFTe5fBLjhznWhBX7\"\n  },\n  \"deviceInfo\": {\n    \"make\": \"Vivo\",\n    \"model\": \"1716\",\n    \"appVersion\": \"2.0\",\n    \"sdkVersion\": \"30701\",\n    \"osVersion\": \"8.1.0\",\n    \"dpi\": 320,\n    \"dimensions\": {\n      \"width\": 68,\n      \"height\": 128,\n      \"unit\": \"mm\"\n    }\n  },\n  \"eventProps\": {\n    \"Campaign id\": \"1524576510\",\n    \"Campaign name\": \"Test\",\n    \"Campaign type\": \"Mobile Push - Android\"\n  }\n}",
      "language": "json"
    },
    {
      "code": "<?xml version='1.0' encoding='UTF-8'?>\n<root>\n<Event>\n    <ts>20220212210100</ts>\n    <eventName>Notification Sent</eventName>\n    <profile>\n        <all_identities>testingmom@gmail.com</all_identities>\n        <platform>Android</platform>\n        <email>testingmom@gmail.com</email>\n        <push_token>fcm:ffvb4LIsf3k:APA91bHtWKK-Zl4Ba-7iJ-Y8v9sAzjGxtHVNN2BZnksiLuFaUOZ7D3plpA2R79Xx-MDv2jdl9OFlI1a1LSagT8bjEUHyaQTBBuEto45ipAFjDHq2RdMS9qgGi0nZFTe5fBLjhznWhBX7</push_token>\n    </profile>\n    <deviceInfo>\n        <make>Vivo</make>\n        <model>1716</model>\n        <appVersion>2.0</appVersion>\n        <sdkVersion>30701</sdkVersion>\n        <osVersion>8.1.0</osVersion>\n        <dpi>320</dpi>\n        <dimensions>\n            <width>68</width>\n            <height>128</height>\n            <unit>mm</unit>\n        </dimensions>\n    </deviceInfo>\n    <eventProps>\n        <entry>\n            <key>Campaign id</key>\n            <value>1524576510</value>\n        </entry>\n        <entry>\n            <key>Campaign name</key>\n            <value>Test</value>\n        </entry>\n        <entry>\n            <key>Campaign type</key>\n            <value>Mobile Push - Android</value>\n        </entry>\n    </eventProps></root>",
      "language": "xml"
    },
    {
      "code": "ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.Campaign id,eventProps.Campaign name,eventProps.Campaign type\n20220331141100,Notification Sent,,,,Android,,,,,xaomi,mi a2,,30700,9.2,,,,,,,1648716020,Non-Broadcast,Webhook",
      "language": "text",
      "name": "CSV"
    }
  ]
}
[/block]
### Notification Viewed
This event is tracked when a user views an email, in-app notification, or a web notification sent from CleverTap.
[block:code]
{
  "codes": [
    {
      "code": "{\n  \"ts\": 20220212004133,\n  \"eventName\": \"Notification Viewed\",\n  \"profile\": {\n    \"platform\": \"Android\",\n    \"push_token\": \"fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf\"\n  },\n  \"deviceInfo\": {\n    \"make\": \"samsung\",\n    \"model\": \"SM-G781B\",\n    \"appVersion\": \"4.3.0.0-prod-android12\",\n    \"sdkVersion\": \"40300\",\n    \"osVersion\": \"Others\",\n    \"browser\": \"MobileApp\",\n    \"dpi\": 480,\n    \"dimensions\": {\n      \"width\": 47,\n      \"height\": 115,\n      \"unit\": \"mm\"\n    }\n  },\n  \"eventProps\": {\n    \"CT Source\": \"Mobile\",\n    \"wzrk_id\": \"275227_20220212\",\n    \"wzrk_ttl\": 1644779493,\n    \"wzrk_pivot\": \"wzrk_default\",\n    \"CT Session Id\": 1644606691,\n    \"CT App Version\": \"4.3.0.0-prod-android12\",\n    \"Campaign type\": \"InApp\"\n  }\n}",
      "language": "json"
    },
    {
      "code": "<?xml version='1.0' encoding='UTF-8'?>\n<root>\n<Event>\n    <ts>20220212004133</ts>\n    <eventName>Notification Viewed</eventName>\n    <profile>\n        <platform>Android</platform>\n        <push_token>fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf</push_token>\n    </profile>\n    <deviceInfo>\n        <make>samsung</make>\n        <model>SM-G781B</model>\n        <appVersion>4.3.0.0-prod-android12</appVersion>\n        <sdkVersion>40300</sdkVersion>\n        <osVersion>Others</osVersion>\n        <browser>MobileApp</browser>\n        <dpi>480</dpi>\n        <dimensions>\n            <width>47</width>\n            <height>115</height>\n            <unit>mm</unit>\n        </dimensions>\n    </deviceInfo>\n    <eventProps>\n        <entry>\n            <key>CT Source</key>\n            <value>Mobile</value>\n        </entry>\n        <entry>\n            <key>wzrk_id</key>\n            <value>275227_20220212</value>\n        </entry>\n        <entry>\n            <key>wzrk_ttl</key>\n            <value>1644779493</value>\n        </entry>\n        <entry>\n            <key>wzrk_pivot</key>\n            <value>wzrk_default</value>\n        </entry>\n        <entry>\n            <key>CT Session Id</key>\n            <value>1644606691</value>\n        </entry>\n        <entry>\n            <key>CT App Version</key>\n            <value>4.3.0.0-prod-android12</value>\n        </entry>\n        <entry>\n            <key>Campaign type</key>\n            <value>InApp</value>\n        </entry>\n    </eventProps></root>",
      "language": "xml"
    },
    {
      "code": "ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.wzrk_acts,eventProps.CT Source,eventProps.wzrk_cts,eventProps.Client Name,eventProps.wzrk_sound,eventProps.wzrk_c2a,eventProps.wzrk_pid,eventProps.Campaign id,eventProps.browser,eventProps.CT Latitude,eventProps.Campaign type,eventProps.CT App Version,eventProps.wzrk_acct_id,eventProps.wzrk_pivot,eventProps.wzrk_cid,eventProps.wzrk_dl,eventProps.wzrk_bi,eventProps.wzrk_bc,eventProps.wzrk_rnv,eventProps.wzrk_pn,eventProps.User Agent,eventProps.wzrk_id,eventProps.wzrk_ttl,eventProps.CT Longitude,eventProps.wzrk_animated,eventProps.wzrk_bp,eventProps.CT Session Id\n20220325131632,Notification Viewed,aks123,,\"[adarsh@clevertap.com, aks123]\",Chrome,919999594213,Adarsh,adarsh@clevertap.com,,,,,,,Chrome,,,,,,,,,Gmail,,,,,,,Email,,,Variant A,,,,,,,Mozilla/5.0 (Windows NT 5.1; rv:11.0) Gecko Firefox/11.0 (via ggpht.com GoogleImageProxy),1648191410_20220325,,,,,",
      "language": "text",
      "name": "CSV"
    }
  ]
}
[/block]
### Push Impressions
This event is tracked when a push notification sent from CleverTap is delivered on a user’s device. The funnels on the Push campaign statistics page reflect the count for this event.

### App Version Changed
This event is raised when a user’s current app version is different from the user’s previous app version.
[block:code]
{
  "codes": [
    {
      "code": "",
      "language": "text"
    }
  ]
}
[/block]
### Notification Replied
[block:code]
{
  "codes": [
    {
      "code": "<?xml version='1.0' encoding='UTF-8'?>\n<root>\n<Event>\n    <ts>20220330143846</ts>\n    <eventName>Notification Replied</eventName>\n    <profile>\n        <identity>6102608768475532,645676746</identity>\n        <all_identities>6102608768475532</all_identities>\n        <all_identities>deepak@clevertap.com</all_identities>\n        <all_identities>645676746</all_identities>\n        <platform>Chrome</platform>\n        <name>deepak yadav</name>\n        <email>deepak@clevertap.com</email>\n        <push_token>d-q28mLIUX4:APA91bHi2UiOaDIs9FUTqLRBO_7vATEIipJwmq2H3q4iGfVfD9wNTZNgKVFmwWZTyjxzzbg6G77AnfrQcSkQFHuDW9bJOso9b-Wo7Mtf2_9dRBy5be5VkYOzn4nRBiRS62wcnZuQvOMQBFMVl_2D2tVwiIeIQrymcsw8ilrDNn9Iv3XBT3Qg66eOUZcgSMg1cvf0yiaGdp7zBW71GQ3Ww2w5TiF4VOcRCKcnkP94EraOCaiHUsllA2DLg</push_token>\n        <phone>919930079420</phone>\n    </profile>\n    <deviceInfo>\n        <browser>Chrome</browser>\n    </deviceInfo>\n    <eventProps/><Event>\n    <ts>20220330143906</ts>\n    <eventName>Notification Replied</eventName>\n    <profile>\n        <identity>6102608768475532,645676746</identity>\n        <all_identities>6102608768475532</all_identities>\n        <all_identities>deepak@clevertap.com</all_identities>\n        <all_identities>645676746</all_identities>\n        <platform>Chrome</platform>\n        <name>deepak yadav</name>\n        <email>deepak@clevertap.com</email>\n        <push_token>d-q28mLIUX4:APA91bHi2UiOaDIs9FUTqLRBO_7vATEIipJwmq2H3q4iGfVfD9wNTZNgKVFmwWZTyjxzzbg6G77AnfrQcSkQFHuDW9bJOso9b-Wo7Mtf2_9dRBy5be5VkYOzn4nRBiRS62wcnZuQvOMQBFMVl_2D2tVwiIeIQrymcsw8ilrDNn9Iv3XBT3Qg66eOUZcgSMg1cvf0yiaGdp7zBW71GQ3Ww2w5TiF4VOcRCKcnkP94EraOCaiHUsllA2DLg</push_token>\n        <phone>919930079420</phone>\n    </profile>\n    <deviceInfo>\n        <browser>Chrome</browser>\n    </deviceInfo>\n    <eventProps>\n        <entry>\n            <key>CT Source</key>\n            <value>GUPSHUP</value>\n        </entry>\n        <entry>\n            <key>wzrk_id</key>\n            <value>1596537111_20220330</value>\n        </entry>\n        <entry>\n            <key>Campaign id</key>\n            <value>1596537111</value>\n        </entry>\n        <entry>\n            <key>Campaign type</key>\n            <value>WhatsApp</value>\n        </entry>\n    </eventProps>\n    </root>",
      "language": "xml"
    },
    {
      "code": "ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.CT Source,eventProps.wzrk_id,eventProps.Campaign id,eventProps.Campaign type\n20220330143846,Notification Replied,\"6102608768475532,645676746\",,\"[6102608768475532, deepak@clevertap.com, 645676746]\",Chrome,919930079420,deepak yadav,deepak@clevertap.com,d-q28mLIUX4:APA91bHi2UiOaDIs9FUTqLRBO_7vATEIipJwmq2H3q4iGfVfD9wNTZNgKVFmwWZTyjxzzbg6G77AnfrQcSkQFHuDW9bJOso9b-Wo7Mtf2_9dRBy5be5VkYOzn4nRBiRS62wcnZuQvOMQBFMVl_2D2tVwiIeIQrymcsw8ilrDNn9Iv3XBT3Qg66eOUZcgSMg1cvf0yiaGdp7zBW71GQ3Ww2w5TiF4VOcRCKcnkP94EraOCaiHUsllA2DLg,,,,,,Chrome,,,,,,,,,",
      "language": "text",
      "name": "CSV"
    }
  ]
}
[/block]
### AB Experiment Stopped
This event is raised when the experiment was stopped.
[block:code]
{
  "codes": [
    {
      "code": "",
      "language": "text"
    }
  ]
}
[/block]
### AB Experiment Rolled Out
This event is raised when the winner variant is sent to all devices.
[block:code]
{
  "codes": [
    {
      "code": "",
      "language": "text"
    }
  ]
}
[/block]
### AB Experiment Disqualified
This event is raised when the device is disqualified.
[block:code]
{
  "codes": [
    {
      "code": "",
      "language": "text"
    }
  ]
}
[/block]
### AB Experiment Rendered
This event indicates that the variant has reached the device.
[block:code]
{
  "codes": [
    {
      "code": "{\n  \"ts\": 20220212004133,\n  \"eventName\": \"AB Experiment Rendered\",\n  \"profile\": {\n    \"platform\": \"Android\",\n    \"push_token\": \"fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf\"\n  },\n  \"deviceInfo\": {\n    \"make\": \"samsung\",\n    \"model\": \"SM-G781B\",\n    \"appVersion\": \"4.3.0.0-prod-android12\",\n    \"sdkVersion\": \"40300\",\n    \"osVersion\": \"Others\",\n    \"browser\": \"MobileApp\",\n    \"dpi\": 480,\n    \"dimensions\": {\n      \"width\": 47,\n      \"height\": 115,\n      \"unit\": \"mm\"\n    }\n  },\n  \"eventProps\": {\n    \"Variant\": \"Control Variant\",\n    \"Variant Id\": 0,\n    \"CT Source\": \"Mobile\",\n    \"Version\": 1,\n    \"Experiment Id\": 16,\n    \"Stickiness\": \"true\",\n    \"Mutually Exclusive\": \"true\"\n  }\n}",
      "language": "json"
    },
    {
      "code": "<?xml version='1.0' encoding='UTF-8'?>\n<root>\n<Event>\n    <ts>20220212004133</ts>\n    <eventName>AB Experiment Rendered</eventName>\n    <profile>\n        <platform>Android</platform>\n        <push_token>fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf</push_token>\n    </profile>\n    <deviceInfo>\n        <make>samsung</make>\n        <model>SM-G781B</model>\n        <appVersion>4.3.0.0-prod-android12</appVersion>\n        <sdkVersion>40300</sdkVersion>\n        <osVersion>Others</osVersion>\n        <browser>MobileApp</browser>\n        <dpi>480</dpi>\n        <dimensions>\n            <width>47</width>\n            <height>115</height>\n            <unit>mm</unit>\n        </dimensions>\n    </deviceInfo>\n    <eventProps>\n        <entry>\n            <key>Variant</key>\n            <value>Control Variant</value>\n        </entry>\n        <entry>\n            <key>Variant Id</key>\n            <value>0</value>\n        </entry>\n        <entry>\n            <key>CT Source</key>\n            <value>Mobile</value>\n        </entry>\n        <entry>\n            <key>Version</key>\n            <value>1</value>\n        </entry>\n        <entry>\n            <key>Experiment Id</key>\n            <value>16</value>\n        </entry>\n        <entry>\n            <key>Stickiness</key>\n            <value>true</value>\n        </entry>\n        <entry>\n            <key>Mutually Exclusive</key>\n            <value>true</value>\n        </entry>\n    </eventProps></root>",
      "language": "xml"
    },
    {
      "code": "ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.Variant,eventProps.Variant Id,eventProps.CT Source,eventProps.Version,eventProps.Experiment Id,eventProps.Stickiness,eventProps.Mutually Exclusive\n20220331151803,AB Experiment Rendered,,,,Android,,,,fcm:eM2qyPvaQb-LiySepSzYKk:APA91bG4ezAYx_achDjcgwy0MM7TC6TsU9bCQ1uWxyY1DnqHP42CqEX1h6hEefsAdwZLOidgPYePpmFoqGHtPdRJvjuwv_ckZ9mVAX5qXwoCeaqhfWRcCe8nuuCRXUS5L8c6d8VcggeD,samsung,SM-G781B,4.3.0.0-prod-android12,40300,12,MobileApp,480,47,115,mm,,Variant A,1,Mobile,1,16,true,true",
      "language": "text",
      "name": "CSV"
    }
  ]
}
[/block]
### GeoCluster Exited
The event is only applicable if you have enabled the geofence feature. This event is recorded to mark when a device exits a geofence.
[block:code]
{
  "codes": [
    {
      "code": "",
      "language": "text"
    }
  ]
}
[/block]
### GeoCluster Entered
The event is only applicable if you have enabled the geofence feature. This event is recorded to mark when a device enters a geofence.
[block:code]
{
  "codes": [
    {
      "code": "",
      "language": "text"
    }
  ]
}
[/block]
### Channel Unsubscribed
This event is raised when an email is not acknowledged.
[block:code]
{
  "codes": [
    {
      "code": "{\n  \"ts\": 20220214175719,\n  \"eventName\": \"Channel Unsubscribed\",\n  \"profile\": {\n    \"all_identities\": [\n      \"shweta.chile+38814Campaigns@clevertap.com\",\n      \"shweta.chile+38814campaigns@clevertap.com\"\n    ],\n    \"platform\": \"Android\",\n    \"email\": \"shweta.chile+38814campaigns@clevertap.com\",\n    \"phone\": 918879382967\n  },\n  \"deviceInfo\": {\n    \"make\": \"samsung\",\n    \"appVersion\": \"2.4.1.2\",\n    \"sdkVersion\": \"30800\",\n    \"osVersion\": \"9\",\n    \"browser\": \"MobileApp\",\n    \"dpi\": 380,\n    \"dimensions\": {\n      \"width\": 68,\n      \"height\": 121,\n      \"unit\": \"mm\"\n    }\n  },\n  \"eventProps\": {\n    \"Resubscribed\": \"false\",\n    \"Variant\": \"wzrk_default\",\n    \"Group\": \"all\",\n    \"Type\": \"unsubscribe\",\n    \"Campaign id\": 1644841452,\n    \"Subscription Type\": \"Account Level\",\n    \"Identity\": \"shweta.chile@clevertap.com\",\n    \"Campaign type\": \"email\"\n  }\n}",
      "language": "json"
    },
    {
      "code": "<?xml version='1.0' encoding='UTF-8'?>\n<root>\n<Event>\n    <ts>20220217100621</ts>\n    <eventName>Channel Unsubscribed</eventName>\n    <profile>\n        <identity>13bbf7943e584-0885c2531-5c793977-3e8000-13bbf7943e609553768</identity>\n        <all_identities>testnew553768@gmail.com</all_identities>\n        <all_identities>13bbf7943e584-0885c2531-5c793977-3e8000-13bbf7943e609553768</all_identities>\n        <platform>Web</platform>\n        <email>testnew553768@gmail.com</email>\n    </profile>\n    <deviceInfo>\n        <browser>Others</browser>\n    </deviceInfo>\n    <eventProps>\n        <entry>\n            <key>Resubscribed</key>\n            <value>false</value>\n        </entry>\n        <entry>\n            <key>Variant</key>\n            <value>wzrk_default</value>\n        </entry>\n        <entry>\n            <key>Group</key>\n            <value>all</value>\n        </entry>\n        <entry>\n            <key>Type</key>\n            <value>unsubscribe</value>\n        </entry>\n        <entry>\n            <key>Campaign id</key>\n            <value>1645072550</value>\n        </entry>\n        <entry>\n            <key>Subscription Type</key>\n            <value>Account Level</value>\n        </entry>\n        <entry>\n            <key>Identity</key>\n            <value>rahul.agarwal@clevertap.com</value>\n        </entry>\n        <entry>\n            <key>Campaign type</key>\n            <value>email</value>\n        </entry>\n    </eventProps><Event>",
      "language": "xml"
    },
    {
      "code": "ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.Variant,eventProps.Resubscribed,eventProps.Group,eventProps.Type,eventProps.Campaign id,eventProps.Subscription Type,eventProps.Identity,eventProps.Reason,eventProps.Campaign type\n20220303175015,Channel Unsubscribed,664454,,[664454],Web,,,,,,,,,,Others,,,,,,wzrk_default,false,all,bounced,35024,Account Level,pragya@clevertap.com,,email\n",
      "language": "text",
      "name": "CSV"
    }
  ]
}
[/block]
### Reply Sent
This is an event raised only for WhatsApp. This event is recorded when an agent (CleverTap user) replies to a WhatsApp message from the end-user.
[block:code]
{
  "codes": [
    {
      "code": "{\n  \"ts\": 20220330144227,\n  \"eventName\": \"Reply Sent\",\n  \"profile\": {\n    \"identity\": \"6102608768475532,645676746\",\n    \"all_identities\": [\n      \"6102608768475532\",\n      \"deepak@clevertap.com\",\n      \"645676746\"\n    ],\n    \"platform\": \"Chrome\",\n    \"name\": \"deepak yadav\",\n    \"email\": \"deepak@clevertap.com\",\n    \"push_token\": \"d-q28mLIUX4:APA91bHi2UiOaDIs9FUTqLRBO_7vATEIipJwmq2H3q4iGfVfD9wNTZNgKVFmwWZTyjxzzbg6G77AnfrQcSkQFHuDW9bJOso9b-Wo7Mtf2_9dRBy5be5VkYOzn4nRBiRS62wcnZuQvOMQBFMVl_2D2tVwiIeIQrymcsw8ilrDNn9Iv3XBT3Qg66eOUZcgSMg1cvf0yiaGdp7zBW71GQ3Ww2w5TiF4VOcRCKcnkP94EraOCaiHUsllA2DLg\",\n    \"phone\": 919930079420\n  },\n  \"deviceInfo\": {\n    \"browser\": \"Chrome\"\n  },\n  \"eventProps\": {\n    \"CT Source\": \"System\",\n    \"Campaign id\": 1596537111,\n    \"Campaign type\": \"WhatsApp\"\n  }\n}",
      "language": "json"
    },
    {
      "code": "<?xml version='1.0' encoding='UTF-8'?>\n<root>\n<Event>\n    <ts>20220330144227</ts>\n    <eventName>Reply Sent</eventName>\n    <profile>\n        <identity>6102608768475532,645676746</identity>\n        <all_identities>6102608768475532</all_identities>\n        <all_identities>deepak@clevertap.com</all_identities>\n        <all_identities>645676746</all_identities>\n        <platform>Chrome</platform>\n        <name>deepak yadav</name>\n        <email>deepak@clevertap.com</email>\n        <push_token>d-q28mLIUX4:APA91bHi2UiOaDIs9FUTqLRBO_7vATEIipJwmq2H3q4iGfVfD9wNTZNgKVFmwWZTyjxzzbg6G77AnfrQcSkQFHuDW9bJOso9b-Wo7Mtf2_9dRBy5be5VkYOzn4nRBiRS62wcnZuQvOMQBFMVl_2D2tVwiIeIQrymcsw8ilrDNn9Iv3XBT3Qg66eOUZcgSMg1cvf0yiaGdp7zBW71GQ3Ww2w5TiF4VOcRCKcnkP94EraOCaiHUsllA2DLg</push_token>\n        <phone>919930079420</phone>\n    </profile>\n    <deviceInfo>\n        <browser>Chrome</browser>\n    </deviceInfo>\n    <eventProps>\n        <entry>\n            <key>CT Source</key>\n            <value>System</value>\n        </entry>\n        <entry>\n            <key>Campaign id</key>\n            <value>1596537111</value>\n        </entry>\n        <entry>\n            <key>Campaign type</key>\n            <value>WhatsApp</value>\n        </entry>\n    </eventProps><Event>",
      "language": "xml"
    },
    {
      "code": "ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.CT Source,eventProps.Campaign id,eventProps.Campaign type\n20220330144227,Reply Sent,\"6102608768475532,645676746\",,\"[6102608768475532, deepak@clevertap.com, 645676746]\",Chrome,919930079420,deepak yadav,deepak@clevertap.com,d-q28mLIUX4:APA91bHi2UiOaDIs9FUTqLRBO_7vATEIipJwmq2H3q4iGfVfD9wNTZNgKVFmwWZTyjxzzbg6G77AnfrQcSkQFHuDW9bJOso9b-Wo7Mtf2_9dRBy5be5VkYOzn4nRBiRS62wcnZuQvOMQBFMVl_2D2tVwiIeIQrymcsw8ilrDNn9Iv3XBT3Qg66eOUZcgSMg1cvf0yiaGdp7zBW71GQ3Ww2w5TiF4VOcRCKcnkP94EraOCaiHUsllA2DLg,,,,,,Chrome,,,,,,System,1596537111,WhatsApp",
      "language": "text",
      "name": "CSV"
    }
  ]
}
[/block]
### Webhook Delivered
This event is recorded when a Webhook campaign is delivered successfully.
[block:code]
{
  "codes": [
    {
      "code": "ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.ContentName,eventProps.CT Source,eventProps.ct_app_version,eventProps.ct_latitude,eventProps.all_identities,eventProps.ct_longitude,eventProps.session_props | session_source,eventProps.Campaign Id,eventProps.mp_processing_time_ms,eventProps.ts\n20220331141127,Webhook Delivered,,,[t1@t.com],Chrome,,,t1@t.com,,,,,,,Chrome,,,,,,,System,,,,,,1648716020,,",
      "language": "text",
      "name": "CSV"
    }
  ]
}
[/block]
### State Transitioned
This event is recorded for the lifecycle optimizer when a user transitions from one stage to another.
[block:code]
{
  "codes": [
    {
      "code": "{\n  \"ts\": 20220213235900,\n  \"eventName\": \"State Transitioned\",\n  \"profile\": {\n    \"platform\": \"Android\"\n  },\n  \"deviceInfo\": {\n    \"make\": \"oneplus\",\n    \"model\": \"GM1901\",\n    \"appVersion\": \"2.0\",\n    \"sdkVersion\": \"30702\",\n    \"osVersion\": \"10\",\n    \"browser\": \"MobileApp\",\n    \"dpi\": 420,\n    \"dimensions\": {\n      \"width\": 68,\n      \"height\": 139,\n      \"unit\": \"mm\"\n    }\n  },\n  \"eventProps\": {\n    \"Destination\": 0,\n    \"Type\": \"retention\",\n    \"Model\": 1591889096,\n    \"Source\": 1\n  }\n}",
      "language": "json"
    },
    {
      "code": "<?xml version='1.0' encoding='UTF-8'?>\n<root>\n<Event>\n    <ts>20220213235900</ts>\n    <eventName>State Transitioned</eventName>\n    <profile>\n        <platform>Android</platform>\n    </profile>\n    <deviceInfo>\n        <make>oneplus</make>\n        <model>HD1901</model>\n        <appVersion>2.0</appVersion>\n        <sdkVersion>30702</sdkVersion>\n        <osVersion>10</osVersion>\n        <browser>MobileApp</browser>\n        <dpi>420</dpi>\n        <dimensions>\n            <width>68</width>\n            <height>138</height>\n            <unit>mm</unit>\n        </dimensions>\n    </deviceInfo>\n    <eventProps>\n        <entry>\n            <key>Destination</key>\n            <value>0</value>\n        </entry>\n        <entry>\n            <key>Type</key>\n            <value>retention</value>\n        </entry>\n        <entry>\n            <key>Model</key>\n            <value>1591889096</value>\n        </entry>\n        <entry>\n            <key>Source</key>\n            <value>1</value>\n        </entry>\n    </eventProps></root>",
      "language": "xml"
    },
    {
      "code": "ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.Destination,eventProps.Type,eventProps.Model,eventProps.Source\n20220313235900,State Transitioned,,,[piyush1234dutta@gmail.com],Web,,Sachin gupta,piyush1234dutta@gmail.com,,,,,,,Others,,,,,,0,retention,1591889096,1",
      "language": "text",
      "name": "CSV"
    }
  ]
}
[/block]
### Session Concluded
This event is recorded to mark the end of a session. Session tracking must be enabled for the event to be tracked.
[block:code]
{
  "codes": [
    {
      "code": "{\n  \"ts\": 20220212195454,\n  \"eventName\": \"Session Concluded\",\n  \"profile\": {\n    \"identity\": \"coinsidentity\",\n    \"all_identities\": [\n      \"harsh+coinsph@clevertap.com\",\n      \"coinsidentity\"\n    ],\n    \"platform\": \"Web\",\n    \"email\": \"harsh@clevertap.com\"\n  },\n  \"deviceInfo\": {\n    \"browser\": \"Others\"\n  },\n  \"eventProps\": {\n    \"Session Length\": 0,\n    \"Session Id\": 1644675894\n  }\n}",
      "language": "json"
    },
    {
      "code": "<?xml version='1.0' encoding='UTF-8'?>\n<root>\n<Event>\n    <ts>20220212004554</ts>\n    <eventName>Session Concluded</eventName>\n    <profile>\n        <all_identities>arnabtest@clevertap.com</all_identities>\n        <platform>Android</platform>\n        <name>Arnab</name>\n        <email>arnabtest@clevertap.com</email>\n    </profile>\n    <deviceInfo>\n        <make>samsung</make>\n        <model>SM-G781B</model>\n        <appVersion>4.3.0.0-prod-android12</appVersion>\n        <sdkVersion>0</sdkVersion>\n        <osVersion>Others</osVersion>\n        <browser>MobileApp</browser>\n        <dpi>480</dpi>\n        <dimensions>\n            <width>47</width>\n            <height>115</height>\n            <unit>mm</unit>\n        </dimensions>\n    </deviceInfo>\n    <eventProps>\n        <entry>\n            <key>Session Length</key>\n            <value>3</value>\n        </entry>\n        <entry>\n            <key>Session Id</key>\n            <value>1644606951</value>\n        </entry>\n    </eventProps><Event>",
      "language": "xml"
    },
    {
      "code": "ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.Session Length,eventProps.Session Id\n20220329140130,Session Concluded,,,[krishna@clevertap.com],Web,14155551234,Krishna,krishna@clevertap.com,,,,,,,Others,,,,,,0,1648542690",
      "language": "text",
      "name": "CSV"
    }
  ]
}
[/block]
### Custom Control Group
The event is raised when a campaign is activated with a control group.
[block:code]
{
  "codes": [
    {
      "code": "{\n  \"ts\": 20220212004500,\n  \"eventName\": \"Control Group\",\n  \"profile\": {\n    \"identity\": \"64e7fc45-c223-487e-a9c7-b6b885712b40,19021994,19021996\",\n    \"all_identities\": [\n      \"64e7fc45-c223-487e-a9c7-b6b885712b40\",\n      \"arnab@clevertap.com\",\n      \"19021994\",\n      \"19021996\",\n      \"arnab+3@clevertap.com\"\n    ],\n    \"platform\": \"Android\",\n    \"name\": \"Arnab3\",\n    \"email\": \"arnab@clevertap.com\",\n    \"phone\": 917907527139\n  },\n  \"deviceInfo\": {\n    \"make\": \"samsung\",\n    \"model\": \"SM-G781B\",\n    \"appVersion\": \"4.3.0.0-prod-android12\",\n    \"sdkVersion\": \"40300\",\n    \"osVersion\": \"Others\",\n    \"dpi\": 480,\n    \"dimensions\": {\n      \"width\": 47,\n      \"height\": 115,\n      \"unit\": \"mm\"\n    }\n  },\n  \"eventProps\": {\n    \"Campaign id\": \"1638189364\",\n    \"Campaign name\": \"EMAIL OLD\",\n    \"Campaign type\": \"Email\"\n  }\n}",
      "language": "json"
    },
    {
      "code": "<?xml version='1.0' encoding='UTF-8'?>\n<root>\n<Event>\n    <ts>20220212004500</ts>\n    <eventName>Control Group</eventName>\n    <profile>\n        <identity>64e7fc45-c223-487e-a9c7-b6b885712b40,19021994,19021996</identity>\n        <all_identities>64e7fc45-c223-487e-a9c7-b6b885712b40</all_identities>\n        <all_identities>arnab@clevertap.com</all_identities>\n        <all_identities>19021994</all_identities>\n        <all_identities>19021996</all_identities>\n        <all_identities>arnab+3@clevertap.com</all_identities>\n        <platform>Android</platform>\n        <name>Arnab3</name>\n        <email>arnab@clevertap.com</email>\n        <phone>917907527139</phone>\n    </profile>\n    <deviceInfo>\n        <make>samsung</make>\n        <model>SM-G781B</model>\n        <appVersion>4.3.0.0-prod-android12</appVersion>\n        <sdkVersion>40300</sdkVersion>\n        <osVersion>Others</osVersion>\n        <dpi>480</dpi>\n        <dimensions>\n            <width>47</width>\n            <height>115</height>\n            <unit>mm</unit>\n        </dimensions>\n    </deviceInfo>\n    <eventProps>\n        <entry>\n            <key>Campaign id</key>\n            <value>1638189364</value>\n        </entry>\n        <entry>\n            <key>Campaign name</key>\n            <value>EMAIL OLD</value>\n        </entry>\n        <entry>\n            <key>Campaign type</key>\n            <value>Email</value>\n        </entry>\n    </eventProps></root>",
      "language": "xml"
    },
    {
      "code": "ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.CT Source,eventProps.wzrk_id,eventProps.wzrk_pivot,eventProps.Campaign id,eventProps.Campaign name,eventProps.Campaign type\n20220310145900,Control Group,,,,Chrome,14155551234,,,,,,,,,,,,,,,,,,1646904532,My New WhatsApp Message Campaign,",
      "language": "text",
      "name": "CSV"
    }
  ]
}
[/block]
### System Control Group
The event is raised when a campaign is activated with a control group.
[block:code]
{
  "codes": [
    {
      "code": "",
      "language": "text"
    }
  ]
}
[/block]