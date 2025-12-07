---
title: Messaging Frequency Caps
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
# Overview

Frequency caps help you control the number of messages your users receive. It is common to run multiple messaging campaigns simultaneously or close to one another. The same user may qualify for more than one of these campaigns and be subject to receiving several messages in short succession. 

Alternatively, for a recurring or triggered campaign, the same user may re-qualify for this campaign and receive the same message more than once. Frequency caps provide the capability to ensure your users do not receive too many messages. 

CleverTap has two types of frequency caps, including:
  * *Global Frequency Caps* control the maximum messages a user can get across campaigns for a particular communication channel.
  * *Message-level Frequency Caps* define how often messages can be sent to a particular user for a particular campaign.

When a frequency cap applies to a user, CleverTap does not deliver the associated message. The dropped messages are accounted for in the campaign report error table.

# Global Frequency Caps
Global frequency caps operate on a per-channel basis and let you specify the message cadence, dwell time between messages, and throttle limits (delivery rates).

## Maximum Messages per Channel

You can define the maximum number of messages a user can get across campaigns for a specific communication channel.
[block:callout]
{
  "type": "success",
  "title": "Cadence Example",
  "body": "You can define a cadence of three push notifications in seven days. Cadence ensures that users only receive three push messages in seven days."
}
[/block]
## Dwell Time Between Messages
You can define the minimum time gap between messages across campaigns for a communication channel. 

For example, you can set a minimum gap of at least four hours between messages with a range of:
  * Minimum gap: Five minutes.
  * Maximum gap: Seven days.

## Throttle
You can control the rate at which CleverTap sends notifications. The control rate is defined as the number of messages every five minutes.

### Example
Sending no more than 15,000 messages every five minutes throttles the rate at which all campaigns go out. Throttle limits are typically applicable to large, one-time campaigns. 

For example, you want to send a message to your entire base or a large subset of your base by including a link that leads to a call-to-action. When your users receive this message and click the link, they get directed to the call-to-action resource that you included. Depending on your campaign size, you may want to set a throttle limit to ensure that your notifications are not all delivered at once and redirect too many users simultaneously to the same resource.

# Message-level Frequency Caps

Message-level caps let you control the number of times a particular ongoing campaign gets delivered to the same user. 
[block:callout]
{
  "type": "warning",
  "body": "Message-level and global frequency caps work together when applied simultaneously. A user may be subject to either or both frequency cap limits.",
  "title": "Message Level and Global Frequency Caps"
}
[/block]
These caps are important for recurring or triggered campaigns where the same user may re-qualify multiple times to receive a message.

##Control Options
The control options include:
  * Send every time the user qualifies (default): This sends a message every time the user qualifies (can choose to respect global caps).
  * Send with a minimum gap of: This sets a minimum gap between subsequent messages. The minimum gap allowed is five minutes and the maximum gap allowed is 30 days.