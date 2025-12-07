---
title: Signed Call™ Custom Implementation
excerpt: Learn about the custom implementation in Signed Call™.
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

This document helps existing CleverTap customers who have integrated the Signed Call™ Web SDK for their web applications and are seeking to implement a custom UI.

CleverTap provides a suite of call functions designed to enhance Signed Call management. These callback functions help you manage the lifecycle of calls. 

You need to pass these callback functions in the **cb** object within the payload while initializing the Signed Call Web SDK as follows:

```javascript
let SignedCallClient

initSignedCall(
  {
    accountId: <string>,
    apikey: <string>,
    cuid: <string>,
    clevertap: <clevertap sdk instance>,
    name: <string / optional>,
    ringtone: <string / optional>
    cb: <object>   // Required incase of custom UI Implementation.
  }
).then(client => SignedCallClient = client).catch(err => console.log(err))
```

```javascript
// Register callback functions for custom UI
cb: {
    incoming (data): <function>,
    receiverAnswered (): <function>,
    missed (data): <function>,
    answered (data): <function>,
    cancelled (): <function>,
    hangup (): <function>,
    timer: <string>,
    callStatus: <string>
}
```

CleverTap offers the following list of callback functions to manage the call in case of custom UI implementation:

| Callback functions | Description                                                                                                                                     | Returns                                                |
| :----------------- | :---------------------------------------------------------------------------------------------------------------------------------------------- | :----------------------------------------------------- |
| incoming(data)     | This function is triggered to inform the SDK of an incoming call with a context                                                                 | Call context string. (For example - **Food Delivery**) |
| receiverAnswered() | This function is executed on the **initiator's** side when the receiver answers the call using signedCallClient.answer().                       | Void.                                                  |
| missed(data)       | This function is triggered to inform that a call was missed.                                                                                    | Call context string.                                   |
| answered(data)     | This function is triggered when a call is successfully answered using signedCallClient.answer().                                                | True / False (boolean).                                |
| cancelled():       | This function is triggered to inform the receiver of the incoming call that the initiator has canceled it.                                      | Void.                                                  |
| hangup():          | This function is triggered when the call is terminated via signedCallClient.hangup(). It can be called by either the initiator or the receiver. | Void.                                                  |

## Callback Properties

Following are the properties required for custom UI implementation to display the time and status of call in the call screen:

| Property name | Description                                                                                                  |
| :------------ | :----------------------------------------------------------------------------------------------------------- |
| timer         | HTML element ID from the DOM in which the call duration timer will be displayed, e.g., 00:01:15 (hh:mm:ss).  |
| callStatus    | HTML element ID for showing the different call states, e.g., Outgoing, Incoming, Ongoing, Reconnecting, etc. |

## SDK Actions

Following are the set of actions supported by SignedCall Web SDK

| SDK Action         | Description                               |
| :----------------- | :---------------------------------------- |
| answer()           | To answer when receiving an incoming call |
| decline()          | To decline an incoming call               |
| toggleMuteUnmute() | To toggle mute and unmute while on call   |
| hangup()           | To end an active ongoing call             |
| dialCancel()       | When you make a call and want to cancel.  |