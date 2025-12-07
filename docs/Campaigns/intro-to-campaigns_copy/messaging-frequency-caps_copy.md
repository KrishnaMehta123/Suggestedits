---
title: Messaging Frequency Caps
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

Frequency caps help you control the number of messages your users receive. It is common to run multiple messaging campaigns simultaneously or in close proximity to one another. The same user may qualify for more than one of these campaigns and be subject to receiving several messages in short succession. 

Alternatively, for a recurring or triggered campaign, the same user may re-qualify for this campaign and receive the same message more than once. Frequency caps provide the capability to ensure your users do not receive too many messages. 

CleverTap has two types of frequency caps, including:

- _Global Frequency Caps_ control the maximum messages a user can get across campaigns for a particular channel of communication.
- _Message-level Frequency Caps_ define how often messages can be sent to a particular user for a particular campaign.

When a frequency cap applies to a user, CleverTap will not deliver the associated message. The dropped messages will be accounted for in the campaign report error table.

# Global Frequency Caps

Global frequency caps operate on a per-channel basis and let you specify the message cadence, dwell time between messages, and throttle limits (delivery rates).

## Maximum Messages per Channel

You can define the maximum number of messages a user can get for a specific channel of communication across campaigns.

> 👍 Cadence Example
> 
> You can define a cadence of three push notifications in seven days. This ensures that users only receive three push messages in seven days.

## Dwell Time Between Messages

For a communication channel, you can define the minimum time gap between messages across campaigns. 

For example, you can set a minimum gap of at least four hours between messages with a range of:

- Minimum gap: Five minutes.
- Maximum gap: Seven days.

## Throttle

You can control the rate at which notifications are sent out of CleverTap. The control rate is defined as the number of messages every five minutes.

### Example

Send no more than 15,000 messages every five minutes. This will throttle the rate at which all campaigns go out. Throttle limits are typically applicable to large, one-time campaigns. 

For example, you want to send a message out to your entire base or a large subset of your base by including a link that leads to a call-to-action in the message. When your users receive this message and click the link, they are directed to the call-to-action resource that you included. Depending on your campaign size, you may want to set a throttle limit to ensure that your notifications are not all delivered at once and redirect a large number of users simultaneously to the same resource.

# Message-level Frequency Caps

Message-level caps let you to control the number of times a particular ongoing campaign is delivered to the same user. 

> 🚧 Message Level and Global Frequency Caps
> 
> Message-level and global frequency caps work together when applied simultaneously. A user may be subject to either or both frequency cap limits.

These caps are important for recurring campaigns or triggered campaigns where the same user may re-qualify multiple times to receive a message.

## Control Options

The control options include:

- Send every time the user qualifies (default): This sends a message every time the user qualifies (can choose to respect global caps).
- Send with a minimum gap of: This sets a minimum gap between subsequent messages. The minimum gap allowed is five minutes and the maximum gap allowed is 30 days.

# FAQs

### Q. How does the User DND Set error occur?

A. The _User DND Set_ error occurs when you qualify users for a campaign despite unsubscribing on the target device. This error informs you that these users have been passed into the error bucket.

### Q. What is the Frequency Caps Exceed error?

A. The _Global Frequency_ feature limits the total number of messages that can be scheduled per day for a user, taking into account all active devices and across different communication channels.

Navigate to _Settings_ > _Engage_ > _Setup_ > _Campaign limits_ to cap the frequency for various channels. 

From the _Campaigns limits_ page, you can define the number of messages you want to send to each user in X number of days. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/55bab17-New_final_Previous_Campaigns_global_frequency_v1.png",
        "New final Previous Campaigns_global_frequency v1.png",
        975
      ],
      "align": "center",
      "sizing": "100",
      "border": true
    }
  ]
}
[/block]


You can also specify the following:

- _Dwell time_ is the gap you want to keep between messages.
- _Throttle_ controls the flow of your messages. 

For more information on dwell time, refer to [Dwell Time Between Messages](https://docs.clevertap.com/docs/messaging-frequency-caps#section-dwell-time-between-messages).

For more information on throttling, refer to [Throttle](https://docs.clevertap.com/docs/messaging-frequency-caps#section-throttle).

Now, when you create a campaign, and you want to disable the _Global frequency limit_, clear the _Global Campaign Limit_ option under the _Who_ section. The _Global Campaign Limit_ is enabled by default.