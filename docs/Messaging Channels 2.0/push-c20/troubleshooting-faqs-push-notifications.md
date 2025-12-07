---
title: Troubleshooting & FAQs
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
# FAQ
## Q. How do I analyze the CTA button for a push campaign?
To track the number of clicks on the click to action (CTA) buttons of the push notification, navigate to:
*Analytics* > *Events*.
Search for the *Notification Clicked* event filtered by the campaign. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a1eeb55-Analyze_CTA_1.png",
        "Analyze_CTA_1.png",
        1232,
        625,
        "#f5f6f9"
      ],
      "border": true
    }
  ]
}
[/block]
On the result, go to *Trend & Properties*, then scroll down to the *Event property* table and filter in the dropdown by *wzrk_c2a* to see a distribution of clicks across the various buttons on that respective campaign.

<<@dk, need a good screen here>>
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9d5e8c1-Analyze_CTA_2.png",
        "Analyze_CTA_2.png",
        1046,
        566,
        "#e1e9f0"
      ],
      "border": true
    }
  ]
}
[/block]
##Q. Why does the push notification image not render for Android?
Rendering of the image in a push notification is dependent on three factors:
* Image size - The image size must be less than 40Kb.
* User's internet connection: The OS (Android and iOS) tries to download the image for ~10 seconds. If it cannot download the image within this time, the push is rendered only with the title and message without the image.
* CDN(Content Delivery Network) throughput: Because the OS downloads the image every time a push is sent to a user, the CDN you are using to host images must also be scalable. Say the notification is sent to 5 million users. The OS tries to download the image from the CDN for all these users. The CDN must be scalable for such a base.



## Q. why do images not render for the push notifications? Primarily for  Chinese OEMs such as OnePlus?

Chinese handsets have tweaked the OS to enhance battery life. Battery optimization plays a vital role in preventing image rendering in a push notification. This behavior is prominent across makes like Oppo, OnePlus, and so on. Because of the battery optimization layer, the app sometimes kills the background services, preventing the notification from rendering. This behavior varies by user and device based on the app's usage pattern and device usage and timings. Additionally, if the notification is clicked as soon as received, the app might open irrespective of the settings. However, if the notifications stay in the user's tray for a specific time (the threshold varies from device to device), the app does not open on clicking the notification.
Please find the further details as follows:
Based on our observations, in OnePlus Devices: 
* Under*Settings* >*Recent App Management*, you have two options available, that is, Normal Clear* and*Deep Clear*. Generally, if *Deep clear* is selected, clicking on a notification does not open the app.
* Along with*Recent App Management*, there is battery optimization, which has two options under*Advanced optimization* >*Deep optimization* &*Sleep standby optimization*.
This option also prevents opening the app after clicking the notification.
This behavior varies from user to user using a OnePlus device basis the app's usage pattern.

## Q. What is the recommended image dimension in push notifications with CTA? 
* Aspect ratio: 16:9 and Recommended Size - 533.33 X 300 pixels minimum.
* Supported file types are PNG, JPG, JPEG
* Max size: 40Kb
We would recommend maintaining an Aspect ratio of 16:9. Adjust the dimensions accordingly. You can calculate the aspect ratio from websites such as https://calculateaspectratio.com.

## Q. If I send a push notification to my users, but their device is inactive, then when they open it again, does the notification appear for them? 

## Q. Does a push notification appear for an inactive device after it becomes active?
The user device may be inactive if the user's internet service is unavailable or if the phone is switched off or out of the network/coverage area. The user does not receive any notification. However, a notification is delivered basis the TTL period when the user gets connectivity later.  


## Q. My application infrastructure can only support handling 100K users in a given time duration. How do I achieve this rate-limiting from CleverTap while sending push notifications?
This can be achieved by throttling campaigns. The push campaign adheres to the throttle limit set for push notifications in the *Campaign Limits* under *Account Settings*.
This can then be enabled or disabled during the setup of campaign creation. For more information, refer to [Throttling](https://docs.clevertap.com/docs/setup-push-notification#push-campaign-throttling).