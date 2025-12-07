---
title: Setup
excerpt: Understand how to set up Web Push as a channel for your marketing campaigns.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Check that the Web Push is set up before creating campaigns. 

From the CleverTap dashboard, navigate to *Settings > Channels > Web push*. 

You can toggle the Web push for every browser that is integrated correctly. All the details are displayed on this page. 

1. [Chrome Browser](https://developer.clevertap.com/docs/web#section-chrome-web-push)

<Image alt="CT Dashboard settings for Chrome" align="center" width="80% " border={true} src="https://files.readme.io/088057131103893b398a4587df82c913056e4f2e09b703fb1748896336ada3e7-image.png">
  CT Dashboard settings for Chrome
</Image>

> 📘 FCM Update: Migrate to HTTP v1 API
>
> We only support VAPID based Web Push notifications. Customers that have FCM based tokens in their account, please note the following:
>
> * Firebase will deprecate its legacy APIs starting June 20, 2023, and discontinue them from June 2024.
> * To avoid disruptions in web push notifications, you must migrate to the new HTTP v1 API by June 20, 2024. For more information, refer to [Integrate FCM and CleverTap](https://developer.clevertap.com/docs/web-push#integrate-fcm-and-clevertap).

2. [Firefox Browser](https://developer.clevertap.com/docs/web#section-firefox-web-push)

<Image alt="CT Dashboard settings for Firefox" align="center" width="80% " border={true} src="https://files.readme.io/2acbfaa52a58b6885477b6eedb1973bfa882d6599223ca8a6249f527e04df9fa-image.png">
  CT Dashboard settings for Firefox
</Image>

3. [Safari Browser](https://developer.clevertap.com/docs/web#section-safari-web-push)

<Image title="Provide APNS details" alt={1080} align="center" width="80%" border={true} src="https://files.readme.io/9a8d528-safari_web_push.png">
  CT Dashboard Settings for Safari
</Image>

4. [Kai OS](https://developer.clevertap.com/docs/kaios)

<Image alt="CT Dashboard Settings for KaiOS" align="center" width="80% " border={true} src="https://files.readme.io/231f7b6c446d06b3ce1e0b67bc2a335b2327d7b625afa039bbbf6c7ba4030aa5-image.png">
  CT Dashboard Settings for KaiOS
</Image>
