---
title: Setup
excerpt: Understand how to set up Push as a channel for your marketing campaigns.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Mobile Push Setup

Set up your mobile push notifications from the CleverTap dashboard.  
Navigate to _Settings > Channels > Mobile push_. 

# Android

Set up and enter credentials for all the platforms that your application supports:  
\<Xiaomi is not available in the DB?>

1. [FCM](https://developer.clevertap.com/docs/android-push#find-your-fcm-sender-id--fcm-server-api-key)
2. [Xiaomi](https://developer.clevertap.com/docs/xiaomi-push-notifications#section-get-the-apps-package-name-app-id-app-key-app-secret)
3. [Baidu](https://developer.clevertap.com/docs/baidu-push-notifications#section-get-the-apps-api-key-secret-key)
4. [Huwaei](https://developer.clevertap.com/docs/clevertap-huawei-push-integration#section-get-the-apps-app-id-app-secret)

## Enable Notification Channels

For Android 8.0 and above, you can create a group of channels for your users. The users can then turn on or off the subscription to these channels. You can create and choose from a list of these channels in campaign creation. 

<Give more info>

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/3ea1e3dd77383905a539a9257ccf9a110155faaf43c61058c109a809bc600351-image.png",
        null,
        ""
      ],
      "align": "center",
      "sizing": "5060px",
      "border": true
    }
  ]
}
[/block]


<br />

# iOS

You can either create and upload: 

- [APNs Auth Key](https://developer.clevertap.com/docs/how-to-create-an-ios-apns-auth-key)
- [APNs Push Certificate](https://developer.clevertap.com/docs/how-to-create-an-ios-apns-certificate)

> 📘 Our Recommendation
> 
> We recommend that you create and upload an APNs Auth Key.

# Raising Events

CleverTap SDK tracks data based on the integration setup. Refer to [CleverTap SDKs](https://developer.clevertap.com/docs/clevertap-sdks) for more information. 

The following system events can be enabled manually:

## Raising Push Impression Event

You can raise and record push notifications delivered to your users’ Android devices.

\<not for iOS devices?>

1. Navigate to _Settings_ > _Schema_ > _Events_.
2. From the _System Events \_tab, search for \_Push Impressions_, then click on the vertical ellipsis menu.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1f68258-push_set_push_impression.png",
        "Setup Push Impressions for Android from the Schema",
        1171
      ],
      "align": "center",
      "border": true,
      "caption": "Setup Push Impressions"
    }
  ]
}
[/block]


3. Click on **Setup push impressions**. A new window displays.
4. Turn on the _Mobile Push_ toggle. 
5. Click on **Save** to enable the option.

After the toggle is on, all the push notifications delivered are recorded under the _Push Impressions_ event. The viewed and conversion count from this event is also available under _Analytics_ > _Events_.

> 🚧 SDK Considerations
> 
> Some things to consider include:
> 
> 1. The push event can only be raised for CleverTap SDK version 3.5.1 and above for Android and version 3.5.0 and above for iOS.
> 2. If the notification channel is incorrect, the push notification is not delivered on the device and therefore, no event is raised for the push impression.

## Raising Notification Viewed Event for iOS

To raise the _Notification Viewed_ event for iOS, it is mandatory to enable the _Mutable Content_ under the iOS section of the campaign creation.

\<not for Android?>

For more information on how to enable _Notification Viewed_ for your account, refer to our [developer documentation](https://developer.clevertap.com/docs/push-notifications-ios#push-impressions). 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2bd5135-campaign_iOS.png",
        "Select the Mutable Content Checkbox",
        1251
      ],
      "align": "center",
      "sizing": "80",
      "border": true,
      "caption": "Setup Push Impressions for iOS"
    }
  ]
}
[/block]


## Optimize Push Impressions

CleverTap SDK raises the _Push Impression_ event when the end user's device displays a push notification. This is important because a push successfully sent might not be delivered or displayed on the user's device due to various reasons such as:

- The device's battery optimization killed the app's background activity and suppressed the push notification. Hence, it could not be displayed. This is observed in most Android devices.
- The user is offline, and the push was delivered after the TTL duration. Hence, the push notification was not displayed. The user unsubscribes the notification channel ID used for the push notification in the Android app settings, and hence the push was dismissed by the Operating System (OS).
- If the user is in an unstable network, Push Impression might not be sent but counted as sent. Also, users may have unsubscribed push notifications from the app on the device level, which causes low CTR too.
- When a push is sent from CleverTap, it is delivered to the end user through Firebase. Chinese OEMs usually suppress push notifications for battery optimization, thereby reducing deliveries.

**To increase reachability, CleverTap provides the following options:**

- _Pull Notification_: For more information about optimizing delivery using pull notifications, refer to [Optimize Delivery via Pull Notification](https://docs.clevertap.com/docs/push-optimize-delivery#optimize-delivery-via-pull-notification).
- _Push + App Inbox Campaigns_: The message from push would be sent to the App Inbox when a user launches the app. Integrating with other push notification providers to increase reach and deliverability. For more information, refer to the following documentation: 
  - [Xiaomi Push Integration](https://developer.clevertap.com/docs/xiaomi-push-notifications)
  - [Huawei Push Integration](https://developer.clevertap.com/docs/clevertap-huawei-push-integration)
  - [Baidu Push Integration](https://developer.clevertap.com/docs/baidu-push-notifications)
- Also, if your application is custom-handling the push notification in Android, you must raise the Push Impression event in your Push Handling code. For more information, refer to the [Android SDK](https://developer.clevertap.com/docs/android) documentation. 
- For both (Android and iOS), you must upgrade your respective application with CleverTap SDK version 3.5.1 or above to track the Push Impression. Ensuring the Push Impression is implemented correctly might help increase the Push Impression numbers marked on CleverTap.
- If your application displays the push notification using your custom code and not through CleverTap SDK, then you must raise the _Notification Clicked_ event through your code by calling the following code:
  ```
  1CleverTapAPI.getDefaultInstance(application).pushNotificationClickedEvent(activity.getIntent().getExtras());
  ```

# Push Campaign Throttling

You can throttle the rate at which CleverTap delivers push notifications under _Settings_ > _Setup_ > _Campaign Limits_. If your user base is large and all users receive and click on a push notification at roughly the same time to open the app, you could experience a significant, unwanted load on your systems.

By using push campaign throttling, you can meter how quickly CleverTap delivers your notifications.

> 👍 Push Campaign Throttling Example
> 
> If your reachable audience for a campaign is 500,000 users and your back-end systems can only support up to 20% of them, you can set a throttle limit to 100,000 notifications per 15-minute interval. The entire campaign will then deliver in 1 hour 15 minutes.

For more information refer to this [overview of push notifications](https://clevertap.com/blog/what-are-push-notifications/) which explains what they are, how they work, and why they are crucial for effective user communication.

To ensure your push notifications are engaging and effective, explore our guide on [Push Notification: Best Practices](https://clevertap.com/blog/push-notification-best-practices/) for expert tips on timing, content, and personalization.

\<Can we write settings for ANdroid and iOS separately?>