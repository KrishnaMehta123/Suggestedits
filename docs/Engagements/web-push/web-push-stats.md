---
title: Web Push Stats
excerpt: >-
  Understand all the statistical information available for your Web Push
  campaign
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Viewing Web Push Campaign Stats

Once the campaign has been published, you can view the statistics from the dashboard. Click on **Campaigns** > select the specific campaign from the campaign list. A Stats page opens up where you can view the total Views, Clicks, Conversions, CTR, and Conversion Performance.

<Image title="Trends and Stats" alt={2768} align="center" border={true} src="https://files.readme.io/cefa7ba-web_push_stats_final.png">
  Web Push Campaign Stats
</Image>

<Image alt="Web Push Conversion Performance Stats" align="center" border={true} src="https://files.readme.io/ca4dc9cb6c0f6ec7e0c4c6cffa7b592e484c274073d2a12180aef09804b02a90-image.png">
  Web Push Conversion Performance Stats
</Image>

<br />

* **Sent**: Represents the count of total Web Push notifications sent to the end-users.
* **Views**: Represents the number of times a Web Push notification is viewed.
* **Clicks**: Represents the number of times users have clicked on the Web Push notification.
* **CTR**:  Represents the ratio of Clicks to Views. (CTR = Clicks/Views \* 100).
* **Trend charts**: Represents trends of *Sent*, *Viewed*, and *Clicked* events for this campaign over a specific period of time (for example daily, weekly, monthly).

# Errors

You can view Web Push campaign errors from the Stats > Errors tab.

<Image alt="Web Push Errors Stats" align="center" border={true} src="https://files.readme.io/8258b9c45b9ab558688a950d0f24d8ef781e5db8c314de50fb4296c02390ffe8-image_10.png">
  Web Push Errors Stats
</Image>

## APNS Errors

Apple Push Notification Service (APNS) errors indicate issues with push notification delivery to iOS devices. Refer to the following table for error codes. 

| Error Code                 | Description                                  |
| -------------------------- | -------------------------------------------- |
| apns\_auth\_error          | Invalid APNS certificate.                    |
| apns\_toomany\_same\_token | Too many requests for the same device token. |
| apns\_unknown              | General APNS error.                          |
| apns\_token\_format        | APNS token format is invalid.                |
| apns\_temp\_blacklist      | APNS account temporarily blacklisted.        |
| apns\_empty\_payload       | APNS payload is empty.                       |

## VAPID Errors

VAPID (Voluntary Application Server Identification) errors occur during web push notification delivery. Refer to the error codes categorized below based on their associated platform.

### Safari, Firefox, Kaios Web Push dispatch errors

| Error Code            | Description                                                                  |
| :-------------------- | :--------------------------------------------------------------------------- |
| bad\_params           | One or more of the parameters specified is invalid.                          |
| bad\_auth             | The authorization header is invalid or missing, causing invalid credentials. |
| end\_point\_invalid   | The URL specified is invalid.                                                |
| token\_invalid        | Invalid Token.                                                               |
| server\_issue         | An internal error has occurred within the Push Server.                       |
| browser\_unsubscribed | The user has unsubscribed.                                                   |
| dispatch\_failed      | Dispatch error.                                                              |
| payload\_too\_large   | The payload used is too large.                                               |

### Chrome VAPID

| Error Code            | Description                  |
| :-------------------- | :--------------------------- |
| gcm\_ia               | Invalid FCM key.             |
| push\_unreg           | Push Unregistered (Android). |
| browser\_unsubscribed | The user has unsubscribed.   |

### Chrome FCM

| Error Code                   | Description                           |
| :--------------------------- | :------------------------------------ |
| gcm\_others                  | Unknown Error for FCM.                |
| fcm\_invalid\_argument       | The FCM argument is invalid.          |
| fcm\_sending\_rate\_exceeded | The sending rate for FCM is exceeded. |
| fcm\_oauth2\_token\_expired  | FCM OAuth2 Token Expired.             |
| gcm\_msi                     | Wrong FCM API key.                    |
| push\_unreg                  | Push Unregistered (Android).          |
| fcm\_internal\_server\_error | FCM internal server error.            |

# FAQs

### What are the timeouts and retry limits for Web Push Notifications?

The following are the timeout and retry limits for web push notifications:

| Channel | Timeout (ConnectionRequest)                  | Retry Limits |
| :------ | :------------------------------------------- | :----------- |
| Chrome  | 10 Seconds                                   | 6            |
| Firefox | 10 Seconds                                   | 3            |
| KaiOS   | 10 Seconds                                   | 3            |
| Safari  | 10 Seconds (Read and Connect), 30 Sec (Read) | 3            |

For more information, refer to the [Channel-Specific Timeouts and Retries](doc:platform-considerations#channel-specific-timeouts-and-retries).

Understanding how users interact with your web experience is crucial for optimizing engagement. Learn more about analyzing key [Customer Engagement Metrics](https://clevertap.com/blog/customer-engagement-metrics/) to refine your web strategy to drive better conversions.
