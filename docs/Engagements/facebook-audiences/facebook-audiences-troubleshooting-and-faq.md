---
title: 'Facebook: Troubleshooting & FAQs'
excerpt: Explore troubleshooting tips and FAQs for Facebook Audiences
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Here’s a concise guide of troubleshooting tips and frequently asked questions to help you address common issues with Facebook Audiences.

### What happens if I open an old draft or clone an older Facebook campaign?

When you open an old draft or clone an older Facebook campaign, certain sections will be reset to ensure compatibility with the updated payload structure:

* **Setup**, **What**, and **Who** sections will be reset.
* The **Who** section will retain the previous user query, but the **Control Group** checkbox will be cleared by default.
* You must reconfigure the updated sections before proceeding.

### Can I publish a campaign that uses the old Facebook campaign structure?

No, you cannot publish campaigns using the old structure. Before it can be published, you must update it to align with the new format.

### What happens when I open an older Facebook campaign in Completed, Scheduled, or Recurring state?

CleverTap maintains legacy compatibility for viewing data from older campaigns, but editing limitations apply.

* The *Campaign Overview* page will continue to display as expected.
* The *Stats* page will display data using the old structure for consistency and historical accuracy.
* No edits can be published unless the campaign is updated to the new structure.

### Can I use an old Facebook campaign node in a Journey?

No. You cannot publish a Journey that includes a Facebook campaign node built using the old structure. The system will block the publish action until the node is updated to the new structure.

> 📘 Note
>
> To check if a Facebook campaign node is using an outdated structure, try opening it in the Journey builder. If the node requires an update, the interface will prompt you to reconfigure it before proceeding.

### What happens to the Facebook campaign node in Journeys that use the old structure?

The **Facebook Node** in the **What** section of the Journey will be reset. You must reconfigure it using the latest campaign structure to proceed.

### Why am I seeing the error "Connect to Business Manager to create this audience"?

This error occurs when your Facebook account is not properly linked to a Facebook Business Manager or does not have the required permissions to create a Custom Audience.

To resolve the issue:

* Ensure your Facebook account is associated with a valid **Facebook Business Manager**.
* The Business Manager must be connected to the correct **Facebook Ad Account**.
* You must have the necessary permissions to create and manage audiences.

For a detailed walkthrough and additional troubleshooting tips, refer to the official guide:\
[Connect to Business Manager to create this audience – Troubleshooting](https://gitbook.toneden.io/advertising-platform/facebook-advertising/facebook-ads-troubleshooting-and-faqs/connect-to-business-manager-to-create-this-audience)
