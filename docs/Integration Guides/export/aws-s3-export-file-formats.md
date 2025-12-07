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

```text
<export request id>-<timestamp of the export run>-<event name>-<yyyymmdd>-<file index>-<database-id>.<file format>.gz
```

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

```json
{
  "ts": 20220212004131,
  "eventName": "App Launched",
  "profile": {
    "platform": "Android",
    "push_token": "fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf"
  },
  "deviceInfo": {
    "make": "samsung",
    "model": "SM-G781B",
    "appVersion": "4.3.0.0-prod-android12",
    "sdkVersion": "40300",
    "osVersion": "Others",
    "browser": "MobileApp",
    "dpi": 480,
    "dimensions": {
      "width": 47,
      "height": 115,
      "unit": "mm"
    }
  },
  "eventProps": {
    "CT Network Carrier": "airtel",
    "CT Source": "Mobile",
    "CT OS Version": "12",
    "CT SDK Version": 40300,
    "CT Session Id": 1644606691,
    "CT App Version": "4.3.0.0-prod-android12"
  }
}
```
```xml
<root>
<Event>
    <ts>20220212004131</ts>
    <eventName>App Launched</eventName>
    <profile>
        <platform>Android</platform>
        <push_token>fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf</push_token>
    </profile>
    <deviceInfo>
        <make>samsung</make>
        <model>SM-G781B</model>
        <appVersion>4.3.0.0-prod-android12</appVersion>
        <sdkVersion>40300</sdkVersion>
        <osVersion>Others</osVersion>
        <browser>MobileApp</browser>
        <dpi>480</dpi>
        <dimensions>
            <width>47</width>
            <height>115</height>
            <unit>mm</unit>
        </dimensions>
    </deviceInfo>
    <eventProps>
        <entry>
            <key>CT Network Carrier</key>
            <value>airtel</value>
        </entry>
        <entry>
            <key>CT Source</key>
            <value>Mobile</value>
        </entry>
        <entry>
            <key>CT OS Version</key>
            <value>12</value>
        </entry>
        <entry>
            <key>CT SDK Version</key>
            <value>40300</value>
        </entry>
        <entry>
            <key>CT Session Id</key>
            <value>1644606691</value>
        </entry>
        <entry>
            <key>CT App Version</key>
            <value>4.3.0.0-prod-android12</value>
        </entry>
    </eventProps></root>
```
```text CSV
ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.CT Network Carrier,eventProps.CT Source,eventProps.ct_app_version,eventProps.CT Bluetooth Version,eventProps.Keyword,eventProps.CT SDK Version,eventProps.CT Bluetooth Enabled,eventProps.CT OS Version,eventProps.CT Network Type,eventProps.Model,eventProps.CT Longitude,eventProps.CT Latitude,eventProps.CT Connected To WiFi,eventProps.CT Session Id,eventProps.CT App Version
20220307124926,App Launched,,,,Android,,,,fcm:eNf3g3l_RKmYURl-z4psKo:APA91bEKaXMYxVwHWoi8C-sxWyEmhC3fWWRtqGjehfY6sKUx5HARzIe4rors5jouDZdX8gIaQ1C_DKbCMIgKhYD23XmCnpWPyzJIOusZnjtwJjtNrOa0oqSHzJIJ4g-Gsk8AYL3O7Clo,google,sdk_gphone_x86,1.0,40400,11,MobileApp,420,65,104,mm,,Android,Mobile,,,,40400,,11,,,,,,1646637566,1.0
```

### App Installed

This event is recorded when the user launches the app for the first time.

```json
{
  "ts": 20220212004131,
  "eventName": "App Installed",
  "profile": {
    "platform": "Android",
    "push_token": "fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf"
  },
  "deviceInfo": {
    "make": "samsung",
    "model": "SM-G781B",
    "appVersion": "4.3.0.0-prod-android12",
    "sdkVersion": "40300",
    "osVersion": "Others",
    "browser": "MobileApp",
    "dpi": 480,
    "dimensions": {
      "width": 47,
      "height": 115,
      "unit": "mm"
    }
  },
  "eventProps": {
    "ct_app_version": "4.3.0.0-prod-android12",
    "CT Source": "Mobile"
  }
}
```
```xml
<?xml version='1.0' encoding='UTF-8'?>
<root>
<Event>
    <ts>20220212004131</ts>
    <eventName>App Installed</eventName>
    <profile>
        <platform>Android</platform>
        <push_token>fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf</push_token>
    </profile>
    <deviceInfo>
        <make>samsung</make>
        <model>SM-G781B</model>
        <appVersion>4.3.0.0-prod-android12</appVersion>
        <sdkVersion>40300</sdkVersion>
        <osVersion>Others</osVersion>
        <browser>MobileApp</browser>
        <dpi>480</dpi>
        <dimensions>
            <width>47</width>
            <height>115</height>
            <unit>mm</unit>
        </dimensions>
    </deviceInfo>
    <eventProps>
        <entry>
            <key>ct_app_version</key>
            <value>4.3.0.0-prod-android12</value>
        </entry>
        <entry>
            <key>CT Source</key>
            <value>Mobile</value>
        </entry>
    </eventProps></root>
```
```text
ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.ct_app_version,eventProps.CT Source,eventProps.ct_latitude,eventProps.ct_longitude
20220330171124,App Installed,,,,Android,,,,,google,Android SDK built for x86,1.0,40400,10,MobileApp,420,65,108,mm,,1.0,Mobile,,
20220330143803,App Installed,,,,Android,,,,,samsung,SM-M307F,1.0,40400,11,MobileApp,420,65,128,mm,,1.0,Mobile,,
```

### App Uninstalled

This event is recorded when a user uninstalls your application.

```json
{
  "ts": 20220212000212,
  "eventName": "App Uninstalled",
  "profile": {
    "platform": "Web"
  },
  "deviceInfo": {
    "browser": "Others"
  },
  "eventProps": {
    "clevertapId": "__g3c83c420053a4bb8a27b665f10aa1677",
    "CT Source": "API",
    "source": "REALTIME_FIREBASE"
  }
}
```
```xml
<?xml version='1.0' encoding='UTF-8'?>
<root>
<Event>
    <ts>20220212041124</ts>
    <eventName>App Uninstalled</eventName>
    <profile>
        <platform>Web</platform>
    </profile>
    <deviceInfo>
        <browser>Others</browser>
    </deviceInfo>
    <eventProps>
        <entry>
            <key>clevertapId</key>
            <value>__g577b9e571268456aa8168894f12b0ae2</value>
        </entry>
        <entry>
            <key>CT Source</key>
            <value>API</value>
        </entry>
        <entry>
            <key>source</key>
            <value>REALTIME_FIREBASE</value>
        </entry>
    </eventProps></root>
```
```text CSV
ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.CT Network Carrier,eventProps.CT Source,eventProps.ct_app_version,eventProps.CT Bluetooth Version,eventProps.Keyword,eventProps.CT SDK Version,eventProps.CT Bluetooth Enabled,eventProps.CT OS Version,eventProps.CT Network Type,eventProps.Model,eventProps.CT Longitude,eventProps.CT Latitude,eventProps.CT Connected To WiFi,eventProps.CT Session Id,eventProps.CT App Version
20220307124926,App Launched,,,,Android,,,,fcm:eNf3g3l_RKmYURl-z4psKo:APA91bEKaXMYxVwHWoi8C-sxWyEmhC3fWWRtqGjehfY6sKUx5HARzIe4rors5jouDZdX8gIaQ1C_DKbCMIgKhYD23XmCnpWPyzJIOusZnjtwJjtNrOa0oqSHzJIJ4g-Gsk8AYL3O7Clo,google,sdk_gphone_x86,1.0,40400,11,MobileApp,420,65,104,mm,,Android,Mobile,,,,40400,,11,,,,,,1646637566,1.0
```

### UTM Visited

This event is tracked when a user clicks on a link from a marketing campaign with a UTM parameter defined. This event is also tracked when a CleverTap-integrated attribution platform, such as Branch or Apsalar, sends this information to CleverTap.

```json
{
  "ts": 20220212004131,
  "eventName": "UTM Visited",
  "profile": {
    "platform": "Android",
    "push_token": "fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf"
  },
  "deviceInfo": {
    "make": "samsung",
    "model": "SM-G781B",
    "appVersion": "4.3.0.0-prod-android12",
    "sdkVersion": "40300",
    "osVersion": "Others",
    "browser": "MobileApp",
    "dpi": 480,
    "dimensions": {
      "width": 47,
      "height": 115,
      "unit": "mm"
    }
  },
  "eventProps": {
    "Install": "y"
  },
  "session_props": {
    "session_referrer": "wzrk://track?install=true&utm_source=google-play&utm_medium=organic",
    "utm_medium": "organic",
    "session_source": "Others",
    "utm_source": "google-play"
  }
}
```
```xml
<?xml version='1.0' encoding='UTF-8'?>
<root>
<Event>
    <ts>20220212004131</ts>
    <eventName>UTM Visited</eventName>
    <profile>
        <platform>Android</platform>
        <push_token>fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf</push_token>
    </profile>
    <deviceInfo>
        <make>samsung</make>
        <model>SM-G781B</model>
        <appVersion>4.3.0.0-prod-android12</appVersion>
        <sdkVersion>40300</sdkVersion>
        <osVersion>Others</osVersion>
        <browser>MobileApp</browser>
        <dpi>480</dpi>
        <dimensions>
            <width>47</width>
            <height>115</height>
            <unit>mm</unit>
        </dimensions>
    </deviceInfo>
    <eventProps>
        <entry>
            <key>Install</key>
            <value>y</value>
        </entry>
    </eventProps>
    <sessionProps>
        <entry>
            <key>session_referrer</key>
            <value>wzrk://track?install=true&amp;utm_source=google-play&amp;utm_medium=organic</value>
        </entry>
        <entry>
            <key>utm_medium</key>
            <value>organic</value>
        </entry>
        <entry>
            <key>session_source</key>
            <value>Others</value>
        </entry>
        <entry>
            <key>utm_source</key>
            <value>google-play</value>
        </entry>
    </sessionProps>
</Event>
</root>
```
```text CSV
ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.wzrk_cts,eventProps.firstname,eventProps.CT Source,eventProps.wzrk_push_amp,eventProps.wzrk_ck,eventProps.utm_medium,eventProps.ltmpl,eventProps.wzrk_sound,eventProps.wzrk_ttl_s,eventProps.UTM,eventProps.wzrk_c2a,eventProps.feature,eventProps.provider,eventProps.wzrk_pid,eventProps.continue,eventProps.Campaign id,eventProps.browser,eventProps.action,eventProps.CT Latitude,eventProps.Install,eventProps.Campaign type,eventProps.CT App Version,eventProps.wzrk_acct_id,eventProps.utm_campaign,eventProps.wzrk_pivot,eventProps.wzrk_dl,eventProps.wzrk_cid,eventProps.wzrk_bi,eventProps.wzrk_bc,eventProps.wzrk_rnv,eventProps.wzrk_pn,eventProps.RAW_STRING,eventProps.passive,eventProps.lastname,eventProps.0,eventProps.1,eventProps.followup,eventProps.2,eventProps.time_continue,eventProps.wzrk_id,eventProps.wzrk_ttl,eventProps.v,eventProps.service,eventProps.CT Longitude,eventProps.wzrk_animated,eventProps.wzrk_bp,eventProps.wzrk_dt,eventProps.utm_source,sessionProps.utm_campaign,sessionProps.session_referrer,sessionProps.utm_medium,sessionProps.session_source,sessionProps.utm_source
20220307124926,UTM Visited,,,,Android,,,,fcm:eNf3g3l_RKmYURl-z4psKo:APA91bEKaXMYxVwHWoi8C-sxWyEmhC3fWWRtqGjehfY6sKUx5HARzIe4rors5jouDZdX8gIaQ1C_DKbCMIgKhYD23XmCnpWPyzJIOusZnjtwJjtNrOa0oqSHzJIJ4g-Gsk8AYL3O7Clo,google,sdk_gphone_x86,1.0,40400,11,MobileApp,420,65,104,mm,,,,,,,,,,,,,,,,,,,,,y,,,,,,,,,,,,,,,,,,,,,,,,,,,,,,wzrk://track?install=true&utm_source=google-play&utm_medium=organic,organic,Others,google-play
```

### Notification Sent

This event is tracked when a campaign message is sent to a user. This event is always recorded, even if the user does not open or click on the message. This event is recorded for email, mobile push, SMS, and web push campaigns. The Notification Sent event is available on the Event dashboard, but it is not displayed on the User Profile.

```json
{
  "ts": 20220212210100,
  "eventName": "Notification Sent",
  "profile": {
    "all_identities": [
      "testingmom@gmail.com"
    ],
    "platform": "Android",
    "email": "testingmom@gmail.com",
    "push_token": "fcm:ffvb4LIsf3k:APA91bHtWKK-Zl4Ba-7iJ-Y8v9sAzjGxtHVNN2BZnksiLuFaUOZ7D3plpA2R79Xx-MDv2jdl9OFlI1a1LSagT8bjEUHyaQTBBuEto45ipAFjDHq2RdMS9qgGi0nZFTe5fBLjhznWhBX7"
  },
  "deviceInfo": {
    "make": "Vivo",
    "model": "1716",
    "appVersion": "2.0",
    "sdkVersion": "30701",
    "osVersion": "8.1.0",
    "dpi": 320,
    "dimensions": {
      "width": 68,
      "height": 128,
      "unit": "mm"
    }
  },
  "eventProps": {
    "Campaign id": "1524576510",
    "Campaign name": "Test",
    "Campaign type": "Mobile Push - Android"
  }
}
```
```xml
<?xml version='1.0' encoding='UTF-8'?>
<root>
<Event>
    <ts>20220212210100</ts>
    <eventName>Notification Sent</eventName>
    <profile>
        <all_identities>testingmom@gmail.com</all_identities>
        <platform>Android</platform>
        <email>testingmom@gmail.com</email>
        <push_token>fcm:ffvb4LIsf3k:APA91bHtWKK-Zl4Ba-7iJ-Y8v9sAzjGxtHVNN2BZnksiLuFaUOZ7D3plpA2R79Xx-MDv2jdl9OFlI1a1LSagT8bjEUHyaQTBBuEto45ipAFjDHq2RdMS9qgGi0nZFTe5fBLjhznWhBX7</push_token>
    </profile>
    <deviceInfo>
        <make>Vivo</make>
        <model>1716</model>
        <appVersion>2.0</appVersion>
        <sdkVersion>30701</sdkVersion>
        <osVersion>8.1.0</osVersion>
        <dpi>320</dpi>
        <dimensions>
            <width>68</width>
            <height>128</height>
            <unit>mm</unit>
        </dimensions>
    </deviceInfo>
    <eventProps>
        <entry>
            <key>Campaign id</key>
            <value>1524576510</value>
        </entry>
        <entry>
            <key>Campaign name</key>
            <value>Test</value>
        </entry>
        <entry>
            <key>Campaign type</key>
            <value>Mobile Push - Android</value>
        </entry>
    </eventProps></root>
```
```text CSV
ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.Campaign id,eventProps.Campaign name,eventProps.Campaign type
20220331141100,Notification Sent,,,,Android,,,,,xaomi,mi a2,,30700,9.2,,,,,,,1648716020,Non-Broadcast,Webhook
```

### Notification Viewed

This event is tracked when a user views an email, in-app notification, or a web notification sent from CleverTap.

```json
{
  "ts": 20220212004133,
  "eventName": "Notification Viewed",
  "profile": {
    "platform": "Android",
    "push_token": "fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf"
  },
  "deviceInfo": {
    "make": "samsung",
    "model": "SM-G781B",
    "appVersion": "4.3.0.0-prod-android12",
    "sdkVersion": "40300",
    "osVersion": "Others",
    "browser": "MobileApp",
    "dpi": 480,
    "dimensions": {
      "width": 47,
      "height": 115,
      "unit": "mm"
    }
  },
  "eventProps": {
    "CT Source": "Mobile",
    "wzrk_id": "275227_20220212",
    "wzrk_ttl": 1644779493,
    "wzrk_pivot": "wzrk_default",
    "CT Session Id": 1644606691,
    "CT App Version": "4.3.0.0-prod-android12",
    "Campaign type": "InApp"
  }
}
```
```xml
<?xml version='1.0' encoding='UTF-8'?>
<root>
<Event>
    <ts>20220212004133</ts>
    <eventName>Notification Viewed</eventName>
    <profile>
        <platform>Android</platform>
        <push_token>fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf</push_token>
    </profile>
    <deviceInfo>
        <make>samsung</make>
        <model>SM-G781B</model>
        <appVersion>4.3.0.0-prod-android12</appVersion>
        <sdkVersion>40300</sdkVersion>
        <osVersion>Others</osVersion>
        <browser>MobileApp</browser>
        <dpi>480</dpi>
        <dimensions>
            <width>47</width>
            <height>115</height>
            <unit>mm</unit>
        </dimensions>
    </deviceInfo>
    <eventProps>
        <entry>
            <key>CT Source</key>
            <value>Mobile</value>
        </entry>
        <entry>
            <key>wzrk_id</key>
            <value>275227_20220212</value>
        </entry>
        <entry>
            <key>wzrk_ttl</key>
            <value>1644779493</value>
        </entry>
        <entry>
            <key>wzrk_pivot</key>
            <value>wzrk_default</value>
        </entry>
        <entry>
            <key>CT Session Id</key>
            <value>1644606691</value>
        </entry>
        <entry>
            <key>CT App Version</key>
            <value>4.3.0.0-prod-android12</value>
        </entry>
        <entry>
            <key>Campaign type</key>
            <value>InApp</value>
        </entry>
    </eventProps></root>
```
```text CSV
ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.wzrk_acts,eventProps.CT Source,eventProps.wzrk_cts,eventProps.Client Name,eventProps.wzrk_sound,eventProps.wzrk_c2a,eventProps.wzrk_pid,eventProps.Campaign id,eventProps.browser,eventProps.CT Latitude,eventProps.Campaign type,eventProps.CT App Version,eventProps.wzrk_acct_id,eventProps.wzrk_pivot,eventProps.wzrk_cid,eventProps.wzrk_dl,eventProps.wzrk_bi,eventProps.wzrk_bc,eventProps.wzrk_rnv,eventProps.wzrk_pn,eventProps.User Agent,eventProps.wzrk_id,eventProps.wzrk_ttl,eventProps.CT Longitude,eventProps.wzrk_animated,eventProps.wzrk_bp,eventProps.CT Session Id
20220325131632,Notification Viewed,aks123,,"[adarsh@clevertap.com, aks123]",Chrome,919999594213,Adarsh,adarsh@clevertap.com,,,,,,,Chrome,,,,,,,,,Gmail,,,,,,,Email,,,Variant A,,,,,,,Mozilla/5.0 (Windows NT 5.1; rv:11.0) Gecko Firefox/11.0 (via ggpht.com GoogleImageProxy),1648191410_20220325,,,,,
```

### Push Impressions

This event is tracked when a push notification sent from CleverTap is delivered on a user’s device. The funnels on the Push campaign statistics page reflect the count for this event.

### App Version Changed

This event is raised when a user’s current app version is different from the user’s previous app version.

### Notification Replied

```xml
<?xml version='1.0' encoding='UTF-8'?>
<root>
<Event>
    <ts>20220330143846</ts>
    <eventName>Notification Replied</eventName>
    <profile>
        <identity>6102608768475532,645676746</identity>
        <all_identities>6102608768475532</all_identities>
        <all_identities>deepak@clevertap.com</all_identities>
        <all_identities>645676746</all_identities>
        <platform>Chrome</platform>
        <name>deepak yadav</name>
        <email>deepak@clevertap.com</email>
        <push_token>d-q28mLIUX4:APA91bHi2UiOaDIs9FUTqLRBO_7vATEIipJwmq2H3q4iGfVfD9wNTZNgKVFmwWZTyjxzzbg6G77AnfrQcSkQFHuDW9bJOso9b-Wo7Mtf2_9dRBy5be5VkYOzn4nRBiRS62wcnZuQvOMQBFMVl_2D2tVwiIeIQrymcsw8ilrDNn9Iv3XBT3Qg66eOUZcgSMg1cvf0yiaGdp7zBW71GQ3Ww2w5TiF4VOcRCKcnkP94EraOCaiHUsllA2DLg</push_token>
        <phone>919930079420</phone>
    </profile>
    <deviceInfo>
        <browser>Chrome</browser>
    </deviceInfo>
    <eventProps/><Event>
    <ts>20220330143906</ts>
    <eventName>Notification Replied</eventName>
    <profile>
        <identity>6102608768475532,645676746</identity>
        <all_identities>6102608768475532</all_identities>
        <all_identities>deepak@clevertap.com</all_identities>
        <all_identities>645676746</all_identities>
        <platform>Chrome</platform>
        <name>deepak yadav</name>
        <email>deepak@clevertap.com</email>
        <push_token>d-q28mLIUX4:APA91bHi2UiOaDIs9FUTqLRBO_7vATEIipJwmq2H3q4iGfVfD9wNTZNgKVFmwWZTyjxzzbg6G77AnfrQcSkQFHuDW9bJOso9b-Wo7Mtf2_9dRBy5be5VkYOzn4nRBiRS62wcnZuQvOMQBFMVl_2D2tVwiIeIQrymcsw8ilrDNn9Iv3XBT3Qg66eOUZcgSMg1cvf0yiaGdp7zBW71GQ3Ww2w5TiF4VOcRCKcnkP94EraOCaiHUsllA2DLg</push_token>
        <phone>919930079420</phone>
    </profile>
    <deviceInfo>
        <browser>Chrome</browser>
    </deviceInfo>
    <eventProps>
        <entry>
            <key>CT Source</key>
            <value>GUPSHUP</value>
        </entry>
        <entry>
            <key>wzrk_id</key>
            <value>1596537111_20220330</value>
        </entry>
        <entry>
            <key>Campaign id</key>
            <value>1596537111</value>
        </entry>
        <entry>
            <key>Campaign type</key>
            <value>WhatsApp</value>
        </entry>
    </eventProps>
    </root>
```
```text CSV
ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.CT Source,eventProps.wzrk_id,eventProps.Campaign id,eventProps.Campaign type
20220330143846,Notification Replied,"6102608768475532,645676746",,"[6102608768475532, deepak@clevertap.com, 645676746]",Chrome,919930079420,deepak yadav,deepak@clevertap.com,d-q28mLIUX4:APA91bHi2UiOaDIs9FUTqLRBO_7vATEIipJwmq2H3q4iGfVfD9wNTZNgKVFmwWZTyjxzzbg6G77AnfrQcSkQFHuDW9bJOso9b-Wo7Mtf2_9dRBy5be5VkYOzn4nRBiRS62wcnZuQvOMQBFMVl_2D2tVwiIeIQrymcsw8ilrDNn9Iv3XBT3Qg66eOUZcgSMg1cvf0yiaGdp7zBW71GQ3Ww2w5TiF4VOcRCKcnkP94EraOCaiHUsllA2DLg,,,,,,Chrome,,,,,,,,,
```

### AB Experiment Stopped

This event is raised when the experiment was stopped.

### AB Experiment Rolled Out

This event is raised when the winner variant is sent to all devices.

### AB Experiment Disqualified

This event is raised when the device is disqualified.

### AB Experiment Rendered

This event indicates that the variant has reached the device.

```json
{
  "ts": 20220212004133,
  "eventName": "AB Experiment Rendered",
  "profile": {
    "platform": "Android",
    "push_token": "fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf"
  },
  "deviceInfo": {
    "make": "samsung",
    "model": "SM-G781B",
    "appVersion": "4.3.0.0-prod-android12",
    "sdkVersion": "40300",
    "osVersion": "Others",
    "browser": "MobileApp",
    "dpi": 480,
    "dimensions": {
      "width": 47,
      "height": 115,
      "unit": "mm"
    }
  },
  "eventProps": {
    "Variant": "Control Variant",
    "Variant Id": 0,
    "CT Source": "Mobile",
    "Version": 1,
    "Experiment Id": 16,
    "Stickiness": "true",
    "Mutually Exclusive": "true"
  }
}
```
```xml
<?xml version='1.0' encoding='UTF-8'?>
<root>
<Event>
    <ts>20220212004133</ts>
    <eventName>AB Experiment Rendered</eventName>
    <profile>
        <platform>Android</platform>
        <push_token>fcm:fAvHbAICJKfckm50uVB_WM:APA91bH7nOLq_el08Rkkferx7k3QLsPZ5QCWbbRvw-OPs5XG1l6FqzJKJkYOKLm0EOy-OjTHna3a9tORIZHWI8xAC4qsHjYt-xItfMUJfsJYIy4O2vrUDUXKUi7OrVxHa7RI9lU_sYnf</push_token>
    </profile>
    <deviceInfo>
        <make>samsung</make>
        <model>SM-G781B</model>
        <appVersion>4.3.0.0-prod-android12</appVersion>
        <sdkVersion>40300</sdkVersion>
        <osVersion>Others</osVersion>
        <browser>MobileApp</browser>
        <dpi>480</dpi>
        <dimensions>
            <width>47</width>
            <height>115</height>
            <unit>mm</unit>
        </dimensions>
    </deviceInfo>
    <eventProps>
        <entry>
            <key>Variant</key>
            <value>Control Variant</value>
        </entry>
        <entry>
            <key>Variant Id</key>
            <value>0</value>
        </entry>
        <entry>
            <key>CT Source</key>
            <value>Mobile</value>
        </entry>
        <entry>
            <key>Version</key>
            <value>1</value>
        </entry>
        <entry>
            <key>Experiment Id</key>
            <value>16</value>
        </entry>
        <entry>
            <key>Stickiness</key>
            <value>true</value>
        </entry>
        <entry>
            <key>Mutually Exclusive</key>
            <value>true</value>
        </entry>
    </eventProps></root>
```
```text CSV
ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.Variant,eventProps.Variant Id,eventProps.CT Source,eventProps.Version,eventProps.Experiment Id,eventProps.Stickiness,eventProps.Mutually Exclusive
20220331151803,AB Experiment Rendered,,,,Android,,,,fcm:eM2qyPvaQb-LiySepSzYKk:APA91bG4ezAYx_achDjcgwy0MM7TC6TsU9bCQ1uWxyY1DnqHP42CqEX1h6hEefsAdwZLOidgPYePpmFoqGHtPdRJvjuwv_ckZ9mVAX5qXwoCeaqhfWRcCe8nuuCRXUS5L8c6d8VcggeD,samsung,SM-G781B,4.3.0.0-prod-android12,40300,12,MobileApp,480,47,115,mm,,Variant A,1,Mobile,1,16,true,true
```

### GeoCluster Exited

The event is only applicable if you have enabled the geofence feature. This event is recorded to mark when a device exits a geofence.

### GeoCluster Entered

The event is only applicable if you have enabled the geofence feature. This event is recorded to mark when a device enters a geofence.

### Channel Unsubscribed

This event is raised when an email is not acknowledged.

```json
{
  "ts": 20220214175719,
  "eventName": "Channel Unsubscribed",
  "profile": {
    "all_identities": [
      "shweta.chile+38814Campaigns@clevertap.com",
      "shweta.chile+38814campaigns@clevertap.com"
    ],
    "platform": "Android",
    "email": "shweta.chile+38814campaigns@clevertap.com",
    "phone": 918879382967
  },
  "deviceInfo": {
    "make": "samsung",
    "appVersion": "2.4.1.2",
    "sdkVersion": "30800",
    "osVersion": "9",
    "browser": "MobileApp",
    "dpi": 380,
    "dimensions": {
      "width": 68,
      "height": 121,
      "unit": "mm"
    }
  },
  "eventProps": {
    "Resubscribed": "false",
    "Variant": "wzrk_default",
    "Group": "all",
    "Type": "unsubscribe",
    "Campaign id": 1644841452,
    "Subscription Type": "Account Level",
    "Identity": "shweta.chile@clevertap.com",
    "Campaign type": "email"
  }
}
```
```xml
<?xml version='1.0' encoding='UTF-8'?>
<root>
<Event>
    <ts>20220217100621</ts>
    <eventName>Channel Unsubscribed</eventName>
    <profile>
        <identity>13bbf7943e584-0885c2531-5c793977-3e8000-13bbf7943e609553768</identity>
        <all_identities>testnew553768@gmail.com</all_identities>
        <all_identities>13bbf7943e584-0885c2531-5c793977-3e8000-13bbf7943e609553768</all_identities>
        <platform>Web</platform>
        <email>testnew553768@gmail.com</email>
    </profile>
    <deviceInfo>
        <browser>Others</browser>
    </deviceInfo>
    <eventProps>
        <entry>
            <key>Resubscribed</key>
            <value>false</value>
        </entry>
        <entry>
            <key>Variant</key>
            <value>wzrk_default</value>
        </entry>
        <entry>
            <key>Group</key>
            <value>all</value>
        </entry>
        <entry>
            <key>Type</key>
            <value>unsubscribe</value>
        </entry>
        <entry>
            <key>Campaign id</key>
            <value>1645072550</value>
        </entry>
        <entry>
            <key>Subscription Type</key>
            <value>Account Level</value>
        </entry>
        <entry>
            <key>Identity</key>
            <value>rahul.agarwal@clevertap.com</value>
        </entry>
        <entry>
            <key>Campaign type</key>
            <value>email</value>
        </entry>
    </eventProps><Event>
```
```text CSV
ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.Variant,eventProps.Resubscribed,eventProps.Group,eventProps.Type,eventProps.Campaign id,eventProps.Subscription Type,eventProps.Identity,eventProps.Reason,eventProps.Campaign type
20220303175015,Channel Unsubscribed,664454,,[664454],Web,,,,,,,,,,Others,,,,,,wzrk_default,false,all,bounced,35024,Account Level,pragya@clevertap.com,,email
```

### Reply Sent

This is an event raised only for WhatsApp. This event is recorded when an agent (CleverTap user) replies to a WhatsApp message from the end-user.

```json
{
  "ts": 20220330144227,
  "eventName": "Reply Sent",
  "profile": {
    "identity": "6102608768475532,645676746",
    "all_identities": [
      "6102608768475532",
      "deepak@clevertap.com",
      "645676746"
    ],
    "platform": "Chrome",
    "name": "deepak yadav",
    "email": "deepak@clevertap.com",
    "push_token": "d-q28mLIUX4:APA91bHi2UiOaDIs9FUTqLRBO_7vATEIipJwmq2H3q4iGfVfD9wNTZNgKVFmwWZTyjxzzbg6G77AnfrQcSkQFHuDW9bJOso9b-Wo7Mtf2_9dRBy5be5VkYOzn4nRBiRS62wcnZuQvOMQBFMVl_2D2tVwiIeIQrymcsw8ilrDNn9Iv3XBT3Qg66eOUZcgSMg1cvf0yiaGdp7zBW71GQ3Ww2w5TiF4VOcRCKcnkP94EraOCaiHUsllA2DLg",
    "phone": 919930079420
  },
  "deviceInfo": {
    "browser": "Chrome"
  },
  "eventProps": {
    "CT Source": "System",
    "Campaign id": 1596537111,
    "Campaign type": "WhatsApp"
  }
}
```
```xml
<?xml version='1.0' encoding='UTF-8'?>
<root>
<Event>
    <ts>20220330144227</ts>
    <eventName>Reply Sent</eventName>
    <profile>
        <identity>6102608768475532,645676746</identity>
        <all_identities>6102608768475532</all_identities>
        <all_identities>deepak@clevertap.com</all_identities>
        <all_identities>645676746</all_identities>
        <platform>Chrome</platform>
        <name>deepak yadav</name>
        <email>deepak@clevertap.com</email>
        <push_token>d-q28mLIUX4:APA91bHi2UiOaDIs9FUTqLRBO_7vATEIipJwmq2H3q4iGfVfD9wNTZNgKVFmwWZTyjxzzbg6G77AnfrQcSkQFHuDW9bJOso9b-Wo7Mtf2_9dRBy5be5VkYOzn4nRBiRS62wcnZuQvOMQBFMVl_2D2tVwiIeIQrymcsw8ilrDNn9Iv3XBT3Qg66eOUZcgSMg1cvf0yiaGdp7zBW71GQ3Ww2w5TiF4VOcRCKcnkP94EraOCaiHUsllA2DLg</push_token>
        <phone>919930079420</phone>
    </profile>
    <deviceInfo>
        <browser>Chrome</browser>
    </deviceInfo>
    <eventProps>
        <entry>
            <key>CT Source</key>
            <value>System</value>
        </entry>
        <entry>
            <key>Campaign id</key>
            <value>1596537111</value>
        </entry>
        <entry>
            <key>Campaign type</key>
            <value>WhatsApp</value>
        </entry>
    </eventProps><Event>
```
```text CSV
ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.CT Source,eventProps.Campaign id,eventProps.Campaign type
20220330144227,Reply Sent,"6102608768475532,645676746",,"[6102608768475532, deepak@clevertap.com, 645676746]",Chrome,919930079420,deepak yadav,deepak@clevertap.com,d-q28mLIUX4:APA91bHi2UiOaDIs9FUTqLRBO_7vATEIipJwmq2H3q4iGfVfD9wNTZNgKVFmwWZTyjxzzbg6G77AnfrQcSkQFHuDW9bJOso9b-Wo7Mtf2_9dRBy5be5VkYOzn4nRBiRS62wcnZuQvOMQBFMVl_2D2tVwiIeIQrymcsw8ilrDNn9Iv3XBT3Qg66eOUZcgSMg1cvf0yiaGdp7zBW71GQ3Ww2w5TiF4VOcRCKcnkP94EraOCaiHUsllA2DLg,,,,,,Chrome,,,,,,System,1596537111,WhatsApp
```

### Webhook Delivered

This event is recorded when a Webhook campaign is delivered successfully.

```text CSV
ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.ContentName,eventProps.CT Source,eventProps.ct_app_version,eventProps.ct_latitude,eventProps.all_identities,eventProps.ct_longitude,eventProps.session_props | session_source,eventProps.Campaign Id,eventProps.mp_processing_time_ms,eventProps.ts
20220331141127,Webhook Delivered,,,[t1@t.com],Chrome,,,t1@t.com,,,,,,,Chrome,,,,,,,System,,,,,,1648716020,,
```

### State Transitioned

This event is recorded for the lifecycle optimizer when a user transitions from one stage to another.

```json
{
  "ts": 20220213235900,
  "eventName": "State Transitioned",
  "profile": {
    "platform": "Android"
  },
  "deviceInfo": {
    "make": "oneplus",
    "model": "GM1901",
    "appVersion": "2.0",
    "sdkVersion": "30702",
    "osVersion": "10",
    "browser": "MobileApp",
    "dpi": 420,
    "dimensions": {
      "width": 68,
      "height": 139,
      "unit": "mm"
    }
  },
  "eventProps": {
    "Destination": 0,
    "Type": "retention",
    "Model": 1591889096,
    "Source": 1
  }
}
```
```xml
<?xml version='1.0' encoding='UTF-8'?>
<root>
<Event>
    <ts>20220213235900</ts>
    <eventName>State Transitioned</eventName>
    <profile>
        <platform>Android</platform>
    </profile>
    <deviceInfo>
        <make>oneplus</make>
        <model>HD1901</model>
        <appVersion>2.0</appVersion>
        <sdkVersion>30702</sdkVersion>
        <osVersion>10</osVersion>
        <browser>MobileApp</browser>
        <dpi>420</dpi>
        <dimensions>
            <width>68</width>
            <height>138</height>
            <unit>mm</unit>
        </dimensions>
    </deviceInfo>
    <eventProps>
        <entry>
            <key>Destination</key>
            <value>0</value>
        </entry>
        <entry>
            <key>Type</key>
            <value>retention</value>
        </entry>
        <entry>
            <key>Model</key>
            <value>1591889096</value>
        </entry>
        <entry>
            <key>Source</key>
            <value>1</value>
        </entry>
    </eventProps></root>
```
```text CSV
ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.Destination,eventProps.Type,eventProps.Model,eventProps.Source
20220313235900,State Transitioned,,,[piyush1234dutta@gmail.com],Web,,Sachin gupta,piyush1234dutta@gmail.com,,,,,,,Others,,,,,,0,retention,1591889096,1
```

### Session Concluded

This event is recorded to mark the end of a session. Session tracking must be enabled for the event to be tracked.

```json
{
  "ts": 20220212195454,
  "eventName": "Session Concluded",
  "profile": {
    "identity": "coinsidentity",
    "all_identities": [
      "harsh+coinsph@clevertap.com",
      "coinsidentity"
    ],
    "platform": "Web",
    "email": "harsh@clevertap.com"
  },
  "deviceInfo": {
    "browser": "Others"
  },
  "eventProps": {
    "Session Length": 0,
    "Session Id": 1644675894
  }
}
```
```xml
<?xml version='1.0' encoding='UTF-8'?>
<root>
<Event>
    <ts>20220212004554</ts>
    <eventName>Session Concluded</eventName>
    <profile>
        <all_identities>arnabtest@clevertap.com</all_identities>
        <platform>Android</platform>
        <name>Arnab</name>
        <email>arnabtest@clevertap.com</email>
    </profile>
    <deviceInfo>
        <make>samsung</make>
        <model>SM-G781B</model>
        <appVersion>4.3.0.0-prod-android12</appVersion>
        <sdkVersion>0</sdkVersion>
        <osVersion>Others</osVersion>
        <browser>MobileApp</browser>
        <dpi>480</dpi>
        <dimensions>
            <width>47</width>
            <height>115</height>
            <unit>mm</unit>
        </dimensions>
    </deviceInfo>
    <eventProps>
        <entry>
            <key>Session Length</key>
            <value>3</value>
        </entry>
        <entry>
            <key>Session Id</key>
            <value>1644606951</value>
        </entry>
    </eventProps><Event>
```
```text CSV
ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.Session Length,eventProps.Session Id
20220329140130,Session Concluded,,,[krishna@clevertap.com],Web,14155551234,Krishna,krishna@clevertap.com,,,,,,,Others,,,,,,0,1648542690
```

### Custom Control Group

The event is raised when a campaign is activated with a control group.

```json
{
  "ts": 20220212004500,
  "eventName": "Control Group",
  "profile": {
    "identity": "64e7fc45-c223-487e-a9c7-b6b885712b40,19021994,19021996",
    "all_identities": [
      "64e7fc45-c223-487e-a9c7-b6b885712b40",
      "arnab@clevertap.com",
      "19021994",
      "19021996",
      "arnab+3@clevertap.com"
    ],
    "platform": "Android",
    "name": "Arnab3",
    "email": "arnab@clevertap.com",
    "phone": 917907527139
  },
  "deviceInfo": {
    "make": "samsung",
    "model": "SM-G781B",
    "appVersion": "4.3.0.0-prod-android12",
    "sdkVersion": "40300",
    "osVersion": "Others",
    "dpi": 480,
    "dimensions": {
      "width": 47,
      "height": 115,
      "unit": "mm"
    }
  },
  "eventProps": {
    "Campaign id": "1638189364",
    "Campaign name": "EMAIL OLD",
    "Campaign type": "Email"
  }
}
```
```xml
<?xml version='1.0' encoding='UTF-8'?>
<root>
<Event>
    <ts>20220212004500</ts>
    <eventName>Control Group</eventName>
    <profile>
        <identity>64e7fc45-c223-487e-a9c7-b6b885712b40,19021994,19021996</identity>
        <all_identities>64e7fc45-c223-487e-a9c7-b6b885712b40</all_identities>
        <all_identities>arnab@clevertap.com</all_identities>
        <all_identities>19021994</all_identities>
        <all_identities>19021996</all_identities>
        <all_identities>arnab+3@clevertap.com</all_identities>
        <platform>Android</platform>
        <name>Arnab3</name>
        <email>arnab@clevertap.com</email>
        <phone>917907527139</phone>
    </profile>
    <deviceInfo>
        <make>samsung</make>
        <model>SM-G781B</model>
        <appVersion>4.3.0.0-prod-android12</appVersion>
        <sdkVersion>40300</sdkVersion>
        <osVersion>Others</osVersion>
        <dpi>480</dpi>
        <dimensions>
            <width>47</width>
            <height>115</height>
            <unit>mm</unit>
        </dimensions>
    </deviceInfo>
    <eventProps>
        <entry>
            <key>Campaign id</key>
            <value>1638189364</value>
        </entry>
        <entry>
            <key>Campaign name</key>
            <value>EMAIL OLD</value>
        </entry>
        <entry>
            <key>Campaign type</key>
            <value>Email</value>
        </entry>
    </eventProps></root>
```
```text CSV
ts,eventName,profile.identity,profile.objectId,profile.all_identities,profile.platform,profile.phone,profile.name,profile.email,profile.push_token,deviceInfo.make,deviceInfo.model,deviceInfo.appVersion,deviceInfo.sdkVersion,deviceInfo.osVersion,deviceInfo.browser,deviceInfo.dpi,deviceInfo.dimensions.width,deviceInfo.dimensions.height,deviceInfo.dimensions.unit,controlGroupName,eventProps.CT Source,eventProps.wzrk_id,eventProps.wzrk_pivot,eventProps.Campaign id,eventProps.Campaign name,eventProps.Campaign type
20220310145900,Control Group,,,,Chrome,14155551234,,,,,,,,,,,,,,,,,,1646904532,My New WhatsApp Message Campaign,
```

### System Control Group

The event is raised when a campaign is activated with a control group.
