---
title: Track Push Impression_BIL-2151
excerpt: ''
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

The Push Impression event is tracked when a push notification sent from CleverTap is delivered to a user’s device. After the toggle for Push Impressions is turned on, the CleverTap SDK starts recording an event whenever a push notification sent via CleverTap is delivered to the user’s device. The **Push Impression** event has 25 event properties, and users can Identify and configure the non-required event properties to optimize the cost. 

To do so:

1. Navigate to *Settings* > *Schema* > *Events* from the CleverTap dashboard.
2. Select the *Push Impressions* event from the *System events* tab.
3. Click the ![](https://files.readme.io/fb90f6a-Ellipsis.png) icon and then select *Setup push impressions* from the list.
4. Turn ON the **Mobile Push** toggle and click **Save**. The *Push impressions tracking enables* message displays on the screen.

<Image alt="Enable Tracking Push Impressions Event" align="center" border={true} src="https://files.readme.io/0e8a8e4-Enable_Tracking_Push_Impressions_Event.gif">
  Enable Tracking Push Impressions Event
</Image>

### Enable Event Property Tracking

The users can enable or disable the tracking of some of the *Push Impression* event properties from the CleverTap dashboard. There are a few Push Impression event properties for which you do not have the option to enable or disable the tracking, which are listed as follows:

* `wzrk_ttl_s`
* `wzrk_st`
* `wzrk_rnv`
* `Campaign type`
* `wzrk_cid`
* `wzrk_dl`
* `wzrk_bc`
* `wzrk_bi`
* `wzrk_bp`
* `wzrk_nms`
* `wzrk_ck`
* `wzrk_mutable_content`
* `wzrk_ttl`
* `wzrk_pn_s`

To enable the tracking of Push Impression event properties:

1. Navigate to *Settings* > *Schema* > *Events* from the CleverTap dashboard.
2. Select the *Push Impression*  from the *System events* tab.
3. Click the hyperlink under the *Properties* column. The Push Impression properties list opens. (@bajrang, this is not the latest screenshot)

<Image alt="Push Impressions Properties List" align="center" border={true} src="https://files.readme.io/6c0b851-image.png">
  Push Impressions Properties List
</Image>

4. Select the configurable property, click the ![](https://files.readme.io/fb90f6a-Ellipsis.png) icon, and select *Enable property variant* from the list. The *Enable property tracking* popup opens.\
   (@bajrang: pls add a screenshot here.)
5. Click **Enable** to confirm your action. The *Property tracking successfully enabled* message displays on the screen. The status of the event property changes to *Active*. Once enabled, if you want to disable the tracking later, you can do so by clicking the ![](https://files.readme.io/fb90f6a-Ellipsis.png) icon and selecting **Disable property variant** from the list. 

> 📘 Key Points to Remember
>
> The following are some of the points to consider when configuring the *Push Impressions* event:
>
> * The event property tracking feature is not available for required properties.
> * The **Status** is always *Active* for mandatory properties.
> * The tracking of configurable properties is disabled by default for new (new users of CleverTap dashboard) or returning users (existing users who turned off push impression feature) of push impression feature. 
> * For existing users, the tracking of event properties remains as is, however, they have the additional capability to enable/disable tracking for the same.

The following table lists the Push Impression event properties:

| Property               | Property Description                                                                                                        | Mandatory |
| :--------------------- | :-------------------------------------------------------------------------------------------------------------------------- | :-------- |
| `wzrk_ttl_s`           | Server-side time to live                                                                                                    | No        |
| `wzrk_st`              | Subtitle entered in the [What](https://docs.clevertap.com/docs/create-message-push#push-editor) section of the campaign.    | No        |
| `wzrk_rnv`             | Render Notification viewed (used by SDK to raise PUSH impressions)                                                          | No        |
| `wzrk_push_amp`        | Push amplification flag                                                                                                     | Yes       |
| `wzrk_pn`              | The flag to check if the Push is from CleverTap or not.                                                                     | Yes       |
| `CT Source`            | CleverTap Source                                                                                                            | Yes       |
| `Campaign type`        | Campaign Channel                                                                                                            | No        |
| `wzrk_id`              | The ID of the campaign.                                                                                                     | Yes       |
| `wzrk_pid`             | Unique push notification ID                                                                                                 | Yes       |
| `wzrk_pivot`           | Variant                                                                                                                     | Yes       |
| `wzrk_acct_id`         | CleverTap Account ID                                                                                                        | Yes       |
| `CT App Version`       | CleverTap App Version                                                                                                       | Yes       |
| `wzrk_cid`             | The ID of the channel.                                                                                                      | No        |
| `wzrk_dl`              | Deep link entered in the [What](https://docs.clevertap.com/docs/create-message-push#push-editor) section of the campaign    | No        |
| `wzrk_bc`              | Badge count entered in the [What](https://docs.clevertap.com/docs/create-message-push#push-editor) section of the campaign. | No        |
| `wzrk_bi`              | Badge information                                                                                                           | No        |
| `wzrk_bp`              | Big picture                                                                                                                 | No        |
| `wzrk_nms`             | Notification message summary                                                                                                | No        |
| `wzrk_dt`              | Delivery type                                                                                                               | Yes       |
| `wzrk_ck`              | Collapse key                                                                                                                | No        |
| `wzrk_mutable_content` | iOS                                                                                                                         | No        |
| `wzrk_acts`            | CTA button                                                                                                                  | Yes       |
| `wzrk_ttl`             | SDK side time to live                                                                                                       | No        |
| `wzrk_pn_h`            | RenderMax health state                                                                                                      | Yes       |
| `wzrk_fallback`        | RenderMax activation key                                                                                                    | No        |
| `wzrk_pn_s`            | Silent notification key                                                                                                     | No        |

(@Sanskriti: We are coming up with a page where we are listing all the events and event properties along with their description. Let me know if you want to see this document, I can show it to you and then we can decide on this. In this document, we can just list down the properties that cannot be configured.)  --(@amrita- sure, lets keep the mandatory ones here with their description)

(@bajrang, the last column should be mandatory or configurable?)
