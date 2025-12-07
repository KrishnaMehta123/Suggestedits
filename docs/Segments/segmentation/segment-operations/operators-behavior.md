---
title: System Events Properties and Operator Behavior
excerpt: >-
  Learn how to use system event properties and supported operators to filter
  campaign-tracking events for precise audience segmentation.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

When users receive or interact with campaigns, CleverTap generates system events such as Notification Delivered, Clicked, Viewed, Sent, Failed, and so on. Each of these events captures system properties, structured fields that help you understand how a message performed and how users engaged with it.

You can use these properties in Segment Builder to create audience segments based on message behavior. While building segments, you can apply logical operators to match values precisely or partially.

## Supported Operators

Use the following operators to define how Segment Builder matches values when you filter users by system properties:

* `equals` – Match an exact value\
  For example: Delivery Status equals Delivered
* `not equals` – Exclude a specific value\
   For example: Delivery Status not equals Delivered
* `contains` – Match any value that includes a substring\
  For example: Clicked URL contains /offers

## Use Cases

The following use cases show how you can use system properties and operators in Segment Builder to create targeted user segments based on message behavior:

* Retarget users who clicked a specific link\
  → Notification Clicked > Clicked URL > contains > /promo
* Find users who didn’t receive a transactional email\
  → Notification Delivered > Delivery Status > not equals > Delivered

# System Events and Properties

CleverTap automatically tracks the campaign events, each of which logs one or more system properties, such as the delivery status, clicked URL, reply text, and more. These properties vary by event type. You can use these properties in segmentation filters to analyze message outcomes, re-engage users, or troubleshoot delivery issues.

* [Notification Delivered](doc:operators-behavior#notification-delivered)
* [Notification Clicked](doc:operators-behavior#notification-clicked)
* [Notification Viewed](<doc: operators-behavior#notification-viewed>)
* [Notification Replied](operators-behavior#notification-replied)
* [Notification Sent](doc:operators-behavior#notification-sent)
* [Notification Failed](doc:operators-behavior#notification-failed)

### Notification Delivered

The following table lists the event properties and supported operators for the `Notification Delivered` event:

| Property Name | Supported Operators          | Example Usage                    |
| ------------- | ---------------------------- | -------------------------------- |
| CT Source     | equals, not equals           | CT Source equals API             |
| wzrk\_id      | equals, not equals           | wzrk\_id equals 1699991234\_1001 |
| Campaign type | equals, not equals, contains | Campaign type equals recurring   |
| Variant       | equals, not equals           | Variant equals B                 |
| skipTCM       | equals                       | skipTCM equals true              |

### Notification Clicked

The following table lists the event properties and supported operators for the `Notification Clicked` event:

| Property Name          | Supported Operators          | Example Usage                                 |
| ---------------------- | ---------------------------- | --------------------------------------------- |
| wzrk\_id               | equals, not equals           | wzrk\_id equals 1699991234\_1001              |
| Campaign type          | equals, not equals, contains | Campaign type contains onboarding             |
| Campaign id            | equals, not equals           | Campaign id equals 1681430001\_2025           |
| Variant                | equals, not equals           | Variant not equals B                          |
| wzrk\_c2a              | equals, not equals           | wzrk\_c2a equals checkout\_cta                |
| wzrk\_click\_innerText | equals, not equals, contains | wzrk\_click\_innerText contains “Start Trial” |
| wzrk\_click\_c2a       | equals, not equals           | wzrk\_click\_c2a equals buy\_now              |
| User Agent             | contains                     | User Agent contains iPhone                    |
| button\_id             | equals                       | button\_id equals pay\_later                  |

### Notification Viewed

The following table lists the event properties and supported operators for the `Notification Viewed` event:

| Property Name           | Supported Operators          | Example Usage                       |
| ----------------------- | ---------------------------- | ----------------------------------- |
| Campaign id             | equals, not equals           | Campaign id equals 1699991234       |
| wzrk\_id                | equals, not equals           | wzrk\_id equals wzrk-delivery-id    |
| Campaign type           | equals, not equals, contains | Campaign type contains reactivation |
| CT Source               | equals                       | CT Source equals dashboard          |
| Variant                 | equals, not equals           | Variant equals B                    |
| CT Session Id           | equals                       | CT Session Id equals 9fa9-session   |
| browser                 | equals, not equals           | browser equals Firefox              |
| User Agent              | contains                     | User Agent contains Android         |
| ct\_sdk\_version        | equals                       | ct\_sdk\_version equals 4.6.2       |
| ct\_os\_version         | equals                       | ct\_os\_version equals 14.2.1       |
| ct\_app\_version        | equals                       | ct\_app\_version equals 3.0.0       |
| ct\_connected\_to\_wifi | equals                       | ct\_connected\_to\_wifi equals true |
| ct\_network\_carrier    | equals                       | ct\_network\_carrier equals Airtel  |
| ct\_longitude           | equals                       | ct\_longitude equals 77.5946        |
| ct\_latitude            | equals                       | ct\_latitude equals 12.9716         |
| wzrk\_c2a               | equals                       | wzrk\_c2a equals buy\_now           |
| skipTCM                 | equals                       | skipTCM equals true                 |

### Notification Replied

The following table lists the event properties and supported operators for the `Notification Replied` event:

| Property Name           | Supported Operators          | Example Usage                                                                 |
| ----------------------- | ---------------------------- | ----------------------------------------------------------------------------- |
| Campaign id             | equals, not equals           | Campaign id equals 1699980001\_abc                                            |
| wzrk\_id                | equals, not equals           | wzrk\_id equals wzrk-abc-1234                                                 |
| Incoming text           | equals, not equals, contains | Incoming text contains “stop”                                                 |
| Incoming message type   | equals                       | Incoming message type equals text                                             |
| Source WABA number      | equals                       | Source WABA number equals +14150001234                                        |
| Destination WABA number | —                            | — \{@meenakshi, if there are no supported operators then why is it mentinoed} |
| Variant                 | equals, not equals           | Variant equals B                                                              |
| CT Source               | equals                       | CT Source equals dashboard                                                    |
| Campaign type           | equals, not equals, contains | Campaign type equals recurring                                                |
| QR Payload              | equals                       | QR Payload equals offer2025                                                   |

### Notification Sent

The following table lists the event properties and supported operators for the `Notification Sent` event:

| Property Name | Supported Operators          | Example Usage                 |
| ------------- | ---------------------------- | ----------------------------- |
| Campaign type | equals, not equals, contains | Campaign type equals one-time |
| Labels        | equals, not equals           | Labels equals flash-sale      |
| Variant       | equals, not equals           | Variant equals A              |

### Notification Failed

The following table lists the event properties and supported operators for the `Notification Failed` event:

| Property Name | Supported Operators          | Example Usage                      |
| ------------- | ---------------------------- | ---------------------------------- |
| Error         | equals, not equals, contains | Error contains “Invalid token”     |
| Variant       | equals, not equals           | Variant equals A                   |
| Labels        | equals, not equals           | Labels equals promo-bulk           |
| Campaign type | equals, not equals, contains | Campaign type equals transactional |
| Campaign id   | equals, not equals           | Campaign id equals 1699989999      |
