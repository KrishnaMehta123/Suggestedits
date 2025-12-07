---
title: Render Rate PoC FAQs
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
## Customer-facing FAQS

Q1. How to enable fallback on a Campaign?

A1. Create a new Push Campaign or Clone an existing push Campaign. Navigate to “What” and select Advanced options. Under Advanced, toggle and enable the “Notification Fallback” option for Android.

> 📘 Note
>
> This is only available in Old UI during the PoC.

Q2. How to test the fallback option?\
A2. The fallback option is designed to only work in cases where the OEM is not allowing a normal push to render. The best way to recreate such a scenario is to put the device under strict mode.

1. Enable Developer options on your android device.
2. Open Developer options and scroll down to “Background Process Limits”.
3. Set the limit as “No Background process”
4. Long press on App and open App Info
5. Set the App Battery usage to “Restricted” - This can differ in different OEMs. Once the device is ready to be tested, create a Campaign, send a test with “Notification Fallback” switched off and then with switched on. The second notification should be rendered on the device. This process is a way to put the device in a state which adheres to the “Inactive” definition of the OEM.

Q3. How will my custom handling be impacted?\
A3. The Booster SDK does two activities:

* Allows the Core SDK to function properly in bad cases \[described above]
* Renders the push itself if the core SDK failsIn case 1 the Custom Handling functionality will work as expected with a time limit of 4.5 Seconds, but in the second case where nothing seems to be working the SDK will auto render the notification with baseline features - Title, Message, Message Summary, Image, Deeplink, Sound and CTAs.

Q4. How can I see the uplift?\
A4. The Booster SDK can only showcase uplift in the 2nd scenario described above, there is no definitive way to showcase uplift for the 1st scenario as of today. We have a solution around it but is outside the scope of the PoC. The only way to check the uplift would be via an AB test or by running 2 campaigns on the same base, with each Variant having a different state of the toggle. For Users whose notification is rendered when the fallback is enabled, the Push Impression event will have a new key "Fallback Enabled" with the value "True.”

Q5. How do I integrate the Booster SDK?\
A5. The Booster SDK is an additional SDK which requires minimum support of the latest CT Android SDK - 4.6.0. The fallback SDK needs to be added via an AAR dependency and the SDK will be shared on request.

Q6. What is the battery drain on this technique?\
A6. Our internal tests over 60 devices have shown negligible \[\<0.1%] battery usage over a period of 2 months, with 8 notifications sent per device per day.

Q7. What is the size increase?\
A7. The fallback SDK has a size of less than 50Kb.

Q8. How does the fallback work?\
A8. The Booster SDK has higher level permission on the notification control hierarchy, where the control allows the core SDK to run for a longer duration and is of higher importance in ensuring the rendering of notifications.

Q9. Is there a way to disable the Booster SDK?\
A9. CleverTap backend has a flag on an account level which acts like a kill switch for the Booster SDK, all logic done in the Booster SDK is inside the flag which can be controlled by CleverTap backend. This is kept as an option in case the functioning needs to be disabled.
