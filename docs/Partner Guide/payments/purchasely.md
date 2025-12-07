---
title: Purchasely
excerpt: Payment Partner
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

[Purchasely](https://www.purchasely.com/) is a mobile in-app purchase platform that allows businesses to monetize their apps by offering in-app purchases. After integrating with CleverTap, Purchasely automatically sends all the events related to customer subscriptions from your app to CleverTap. You can then trigger messaging campaigns based on those events to engage, upsell, and retain customers. In addition, you can analyze events and monitor revenue from your app seamlessly.

The Purchasely model offers the following benefits:

* Manage your products, pricing, and subscriptions
* Analyze your in-app purchase data to track revenue, conversion rates, and user behavior

# Prerequisites for Integration

Before setting up Purchasely with CleverTap, there are a few prerequisites that you must have in place. These include:

* **Purchasely account:** You must have a Purchasely account with all the required setup and configurations to send events to the CleverTap dashboard.
* **CleverTap account:** You must have an active CleverTap account with access to the CleverTap dashboard.
* **Purchasely SDK integration:** You need to have integrated the Purchasely SDK into your mobile app to enable in-app purchases.
* **In-app purchases enabled:** In-app purchases must be enabled in your mobile app to allow users to make purchases.
* **API and secret keys:** You must have the API and secret keys for your Purchasely account. These are required to connect your Purchasely account with your CleverTap account.

# Integrate Purchasely with CleverTap

This section describes how to integrate Purchasely with CleverTap. This integration allows you to associate user events with user data in CleverTap, which can help you analyze user behavior and personalize user experiences. This process involves the following three steps:

1. [Associate Purchasely Events to CleverTap Users](https://docs.clevertap.com/docs/purchasely#associate-purchasely-events-to-clevertap-users)
2. [Find CleverTap Project Details](https://docs.clevertap.com/docs/purchasely#find-clevertap-project-details)
3. [Set Up CleverTap in Purchasely Dashboard](https://docs.clevertap.com/docs/purchasely#set-up-clevertap-in-purchasely-dashboard)

## Associate Purchasely Events with CleverTap Users

In the CleverTap SDK, you can set the [CleverTap ID](https://developer.clevertap.com/docs/concepts-user-profiles#section-identifying-a-user) as an attribute for the Purchasely SDK. Purchasely can use the CleverTap ID as a user identity to associate the subscription events to CleverTap. This ensures that user events sent from Purchasely SDK are associated with the CleverTap user.

OR (@Parth: Please check the different version)

To associate the events with CleverTap users, you need to initialize the CleverTap SDK in your application and retrieve the user's [CleverTap ID](https://developer.clevertap.com/docs/concepts-user-profiles#section-identifying-a-user). Then, you need to set the CleverTap ID as an attribute in the Purchasely SDK. This allows Purchasely to associate the user with events in CleverTap.

Following is the syntax to retrieve the CleverTap ID from CleverTap SDK:

```swift
CleverTap.autoIntegrate()
if let clevertapId = CleverTap.sharedInstance()?.profileGetID() {
    Purchasely.setAttribute(.clevertapId, value: clevertapId)
}
```
```kotlin
val cleverTap = CleverTapAPI.getDefaultInstance(applicationContext)
cleverTap?.cleverTapID?.let {
    Purchasely.setAttribute(Attribute.CLEVER_TAP_ID, it)
}
```
```java
CleverTapAPI cleverTap = CleverTapAPI.getDefaultInstance(getApplicationContext());
if(cleverTap.getCleverTapID() != null) {
    Purchasely.setAttribute(Attribute.CLEVER_TAP_ID, cleverTap.getCleverTapID());
}
```
```Text React Native
CleverTap.getCleverTapID((err, res) => {
    Purchasely.setAttribute(Attributes.CLEVER_TAP_ID, res);
});
```

## Find CleverTap Project Details

Find the following project details to authorize the Purchasely connection with the CleverTap dashboard:

* Project ID
* Passcode
* Region

These details are obtained by navigating to the *Settings* > *Project* page of the CleverTap dashboard:

<Image alt="CleverTap Project Details" align="center" border={true} src="https://files.readme.io/c15acc7-Project_Details.png">
  CleverTap Project Details
</Image>

To identify the region of your account, check the URL of your CleverTap account. 

Refer to the following table to identify the region for your account:

| Region                  | API Endpoint           | CleverTap Dashboard URL                                                                            |
| :---------------------- | :--------------------- | :------------------------------------------------------------------------------------------------- |
| India                   | in1.api.clevertap.com  | [https://in1.dashboard.clevertap.com/login.html](https://in1.dashboard.clevertap.com/login.html)   |
| Singapore               | sg1.api.clevertap.com  | [https://sg1.dashboard.clevertap.com/login.html](https://sg1.dashboard.clevertap.com/login.html)   |
| United States           | us1.api.clevertap.com  | [https://us1.dashboard.clevertap.com/login.html](https://us1.dashboard.clevertap.com/login.html)   |
| Indonesia               | aps3.api.clevertap.com | [https://aps3.dashboard.clevertap.com/login.html](https://aps3.dashboard.clevertap.com/login.html) |
| Middle East (UAE)       | mec1.api.clevertap.com | [https://mec1.dashboard.clevertap.com/login.html](https://mec1.dashboard.clevertap.com/login.html) |
| Europe (default region) | api.clevertap.com      | [https://eu1.dashboard.clevertap.com/login.html](https://eu1.dashboard.clevertap.com/login.html)   |

## Set Up CleverTap in Purchasely Dashboard

To set up CleverTap in Purchasely dashboard:

1. Navigate to *Settings* > *Integrations* from the Purchasely dashboard. The *External Integrations* page opens.
2. Click the ellipsis ![](https://files.readme.io/f1bcbe8-Ellipsis.png) icon on the *CleverTap* tile.

<Image align="center" className="border" border={true} src="https://files.readme.io/c8687c9-CleverTap.png" />

The CleverTap Integration form opens.

3. From the *Account Parameters* tab, enable the integration, and enter your CleverTap Account *Region*, *Account ID*, and *Passcode*.

<Image align="center" className="border" border={true} src="https://files.readme.io/bbb8788-Account_Parameters.png" />

To find these details, refer to [CleverTap Project Details](https://docs.clevertap.com/docs/purchasely#2-find-clevertap-project-details).

4. Click **Next**.
5. Enable the events you want to be sent to CleverTap.

<Image align="center" className="border" border={true} src="https://files.readme.io/f98c6ba-Server_Events.png" />

6. Click *Save*.

> 📘 Renaming Events
>
> You can orverride the names of events sent to CleverTap when setting up the integration.

# Subscription Events

The following are the main subscription events that can be sent to CleverTap by Purchasely. To view the full list, refer to [Subscription Events](https://docs.purchasely.com/analytics/events/webhook-events/subscription-events).

| Event                           | Description                                                                                                              |
| :------------------------------ | :----------------------------------------------------------------------------------------------------------------------- |
| SUBSCRIPTION\_STARTED           | Sent when the user purchases a product whether it is the start of a trial or a regular purchase of a consumable product. |
| SUBSCRIPTION\_RENEWED           | Sent when a subscription renews                                                                                          |
| SUBSCRIPTION\_EXPIRED           | Sent when the subscription actually ends                                                                                 |
| SUBSCRIPTION\_REACTIVATED       | Sent when an expired subscription is reactivated. This event is particularly useful for win-back & retargeting campaigns |
| SUBSCRIPTION\_REFUNDED\_REVOKED | Sent when the subscription actually ends                                                                                 |
| RENEWAL\_DISABLED               | Sent when the user deactivates the renewal of a subscription wether it is in trial period or not.                        |
| RENEWAL\_ENABLED                | Sent when the user reactivates                                                                                           |
| TRIAL\_STARTED                  | Sent when a trial starts                                                                                                 |
| TRIAL\_CONVERTED                | Sent when a user converts from a free trial to a normal paid-period                                                      |
| TRIAL\_NOT\_CONVERTED           | Sent when a user finishes it's trial period without renewing to a paid-period                                            |

# Use Cases for Customer Engagements

Purchasely and CleverTap are two powerful tools that can be integrated to help businesses improve their user acquisition, engagement, and retention strategies. After integrating Purchasely with CleverTap businesses can solve use cases like:

* **Personalized in-app purchase offers:** With Purchasely and CleverTap integration, businesses can offer personalized in-app purchase offers to their users based on their past purchase behavior and user data. This can increase the chances of converting users into paying customers.
* **Automated subscription management:** Purchasely offers a subscription management system that can be integrated with CleverTap to automate subscription renewals, cancellations, and upgrades. This can help businesses reduce churn rates and increase revenue.
* **Targeted push notifications:** With CleverTap's advanced segmentation capabilities, businesses can target specific user segments with personalized push notifications that promote Purchasely offers and promotions. This can increase user engagement and revenue.
* **User behavior tracking:** CleverTap can track user behavior within the app, such as which features they use the most, and which Purchasely offers they respond to. This data can be used to optimize future Purchasely offers and improve the overall user experience.
* **A/B testing:** With CleverTap, businesses can conduct A/B tests to compare different Purchasely offers and pricing strategies to see which ones generate the most revenue and conversions.

Overall, integrating Purchasely with CleverTap can help businesses improve their in-app purchase strategies, increase revenue, and improve user engagement and retention.

\<\<@Parth please confirm if the above-documented uses cases are feasible with Purchasely+CT integration>>
