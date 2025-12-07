---
title: Release Notes (COPY)
excerpt: >-
  Explore CleverTap’s newest capabilities, designed to optimize engagement and
  retention at scale.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
Stay up to date with CleverTap's latest feature releases, cutting-edge feature enhancements, and performance enhancements to help you make the most of your experience.

View previous updates in [What's New: 2024](https://docs.clevertap.com/docs/whats-new).

<SdkCard />

# Release Type Legend

<details>

<summary>Expand to learn how to interpret CleverTap's release tags.
  <hr>

</summary>

<TypesOfProductReleases />

<br />

</details>

<br />

[block:html]
{
  "html": "<div class=\"filters\">\n  <h1>Filter By Feature</h1>\n\n <div style=\"\n  background-color: #f8f9fc;\n  border: 1px solid #e2e8f0;\n  border-radius: 8px;\n  padding: 24px 32px;\n  margin: 40px 0;\n  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.04);\n\">\n   \n  <div class=\"filter-options\">\n    <label class=\"filter-option\">\n      <input type=\"checkbox\" id=\"filter-campaigns\">\n      <span class=\"campaign\">\n        <img src=\"https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg\" alt=\"Campaigns\" />\n        Campaigns\n      </span>\n    </label>\n\n    <label class=\"filter-option\">\n      <input type=\"checkbox\" id=\"filter-analytics\">\n      <span class=\"analytics\">\n        <img src=\"https://files.readme.io/f57aa9f8ef374b2652d21d86c7251de0e10d2f8661a4828202bcced4cb299d5f-Analytics.svg\" alt=\"Analytics\" />\n        Analytics\n      </span>\n    </label>\n\n    <label class=\"filter-option\">\n      <input type=\"checkbox\" id=\"filter-segments\">\n      <span class=\"segments\">\n        <img src=\"https://files.readme.io/04fe24c1114cef41af4a4e0224cab88f5be4c31160eca491d67942c689cb79c0-Segmentation.svg\" alt=\"Segments\" />\n        Segments\n      </span>\n    </label>\n\n    <label class=\"filter-option\">\n      <input type=\"checkbox\" id=\"filter-journeys\">\n      <span class=\"journeys\">\n        <img src=\"https://files.readme.io/51dc269788d03bb7bc0482fbc020414bedd96b6c778ac37b71884095493b93c8-Journeys.svg\" alt=\"Journeys\" />\n        Journeys\n      </span>\n    </label>\n\n    <label class=\"filter-option\">\n      <input type=\"checkbox\" id=\"filter-signed-call\">\n      <span class=\"signed-call\">\n        <img src=\"https://files.readme.io/90161cf9015e0e768441c7cefb5a62fb938b438ef6c4ce007cb705542234e2d8-Vector_1.svg\" alt=\"Signed Call\" />\n        Signed Call\n      </span>\n    </label>\n\n    <label class=\"filter-option\">\n      <input type=\"checkbox\" id=\"filter-product-experiences\">\n      <span class=\"product-experiences\">\n        <img src=\"https://files.readme.io/d7de531a1060998537a4e71a078198cf28076d99e1aed3e3c1bdcb5509e29d95-Product_experiences.svg\" alt=\"Product Experiences\" />\n        Product Experiences\n      </span>\n    </label>\n\n    <label class=\"filter-option\">\n      <input type=\"checkbox\" id=\"filter-content-manager\">\n      <span class=\"content-manager\">\n        <img src=\"https://files.readme.io/0ed57ff4730974458d74d2a34ec4cf285aa5e84f59075a6b32550b9d1fd60ae8-Content_Manager.svg\" alt=\"Content Manager\" />\n        Content Manager\n      </span>\n    </label>\n  </div>\n</div>\n"
}
[/block]


# 2025

## March

[block:html]
{
  "html": "<div class=\"release-note article\" data-category=\"campaigns\" id=\"Event-Personalization-Beyond-24-Hours\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#Event-Personalization-Beyond-24-Hours\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg\" alt=\"Campaigns\" class=\"release-note-heading-icon\"/>\n    </div>\n      <h3 class=\"release-note-heading\">Introducing Event Personalization Beyond 24 Hours for Live Behavior Campaigns</h3>\n    <div class=\"badge enhancement\">ENHANCEMENT</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>You can now apply Event Personalization to Live Action and Date-time campaigns with a delay of more than 24 hours. You can create highly personalized push campaigns based on event properties to create custom-tailored notifications, driving better targeting and relevance. It also extends the reach of event-triggered communications hours to increase engagement rates and conversions.</p>\n    <p>For example, streaming applications can now engage users with personalized messages, even days after their last session, ensuring continued engagement.</p>\n    <p>As a result, you can analyze and refine your messaging strategies effectively. For more information, see <a href=\"https://docs.clevertap.com/docs/campaign-reports#subscribe-to-reports\" target=\"_blank\">Subscribe to Reports.</a></p>\n  </div>\n  <hr/>\n</div>"
}
[/block]


## February

[block:html]
{
  "html": "<div class=\"release-note article\" data-category=\"campaigns\" id=\"Group-Campaign-Reports-by-Tags-for-Deeper-Insights\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#Group-Campaign-Reports-by-Tags-for-Deeper-Insights\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/370216d2a5ec47fd419bc47a95762d51295730db345b40f825b3de7115e6e667-Campaigns.svg\" alt=\"Campaigns\"/>\n    </div>\n    <div>\n      <h3 class=\"release-note-heading\">Group Campaign Reports by Tags for Deeper Insights</h3>\n    </div>\n    <div class=\"badge enhancement\">ENHANCEMENT</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>CleverTap now provides Tag Group-wise campaign reports. This is available for Push, Web Push, Email, SMS, and WhatsApp campaigns sent via the Target Users by Identity API. With this enhancement, you can:</p>\n    <p>\n    \t<ul>\n        <li>Get granular insights with reports broken down by tag groups.</li>\n        <li>Optimize campaign strategies by identifying high-performing tag groups.</li>\n    \t</ul>\n    </p>\n    <p>For more information, refer to For more information, refer to <a href=\"#\" target=\"_blank\"> Message Archiving</a></p>\n  </div>\n  <hr/>\n</div>\n"
}
[/block]


[block:html]
{
  "html": "<div class=\"release-note article\" data-category=\"product-experiences\" id=\"Message-Archiving with-Multi-Cloud-Support\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#Message-Archiving-with-Multi-Cloud-Support\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/d7de531a1060998537a4e71a078198cf28076d99e1aed3e3c1bdcb5509e29d95-Product_experiences.svg\" alt=\"Product Experiences\"/>\n    </div>\n    <div>\n      <h3 class=\"release-note-heading\">Message Archiving with Multi-Cloud Support</h3>\n    </div>\n    <div class=\"badge new-feature\">NEW FEATURE</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>The Message Archiving feature now fully supports <b>Google Cloud Platform (GCP), Azure Blob, and AWS S3 buckets</b>. Customers can store copies of outgoing messages across various channels in real-time. This allows seamless integration with multiple cloud storage platforms, offering flexibility and improved data management.</p>\n    <p>\n    \t<ul>\n        <li><b>Google Cloud Platform (GCP) Bucket:</b> Archive outgoing messages directly to your GCP bucket in real-time.</li>\n        <li><b>Azure Blob:</b> Effortlessly store message copies in Azure Blob storage.</li>\n        <li><b>AWS S3 Bucket:</b> Store message archives reliably in your AWS S3 bucket.</li>\n      </ul>\n    </p>\n  <p>\n  <img src=\"https://files.readme.io/3d75303d9e616a48d15b807b985744b75ea2449478cd5efd137f3a716c9f43e2-FebBanner1.jpg\"/>\n  </p>\n  <p>This feature is available as a paid add-on. For more details, refer to <a href=\"https://docs.clevertap.com/docs/message-archiving\" target=\"_blank\">Message Archiving.</a></p>\n  </div>\n  <hr/>\n</div>\n"
}
[/block]


[block:html]
{
  "html": "<div class=\"release-note article\" data-category=\"product-experiences\" id=\"Email-Delivery-Tracking-Enhanced-Campaign-Insights\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#Email-Delivery-Tracking-Enhanced-Campaign-Insights\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/d7de531a1060998537a4e71a078198cf28076d99e1aed3e3c1bdcb5509e29d95-Product_experiences.svg\" alt=\"Product Experiences\"/>\n    </div>\n    <div>\n      <h3 class=\"release-note-heading\">Email Delivery Tracking: Enhanced Campaign Insights</h3>\n    </div>\n    <div class=\"badge private-beta\">BETA</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>CleverTap now offers Email Delivery Tracking, providing deeper visibility into campaign performance beyond just sent emails. With this enhancement, you can now track actual deliveries to users' inboxes, measure delivery rates, analyze engagement based on delivered emails, and gain insights into errors affecting end user delivery. This feature is currently in Private Beta for customers using SendGrid and Infobip (Advanced Email) providers.</p>\n    <p>For more details, refer to <a href=\"https://docs.clevertap.com/docs/email-campaign-stats-delivered\" target=\"_blank\">Campaign Stats</a> and <a href=\"https://docs.clevertap.com/docs/email-provider-operations-delivered\" target=\"_blank\">Provider Stats.</a></p>\n  </div>\n  <hr/>\n</div>\n"
}
[/block]


[block:html]
{
  "html": "<div class=\"release-note article\" data-category=\"analytics\" id=\"Emoji-Support-for-Web-Push-Notification\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#Emoji-Support-for-Web-Push-Notification\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/f57aa9f8ef374b2652d21d86c7251de0e10d2f8661a4828202bcced4cb299d5f-Analytics.svg\" alt=\"Analytics\"/>\n    </div>\n    <div>\n      <h3 class=\"release-note-heading\">Emoji Support for Web Push Notification</h3>\n    </div>\n    <div class=\"badge enhancement\">ENHANCEMENT</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>You can now personalize your notifications and make them fun by adding emojis in the improved Web Push Editor. All message customization options, such as Scribe, Personalization, and Emojis, are accessible below the text fields, making it easier to create engaging notifications.</p>\n    <p>\n      <img src=\"https://files.readme.io/595c35b5641d8ff95ca11c924bcc80ef3fb65bb47b6cb1d5870f24c7fe6d50e7-d6d84e856b1b3fbbb667311ee22af4a6f8cea0fef43525fed5f35a416cee59da-image.png\"/>\n    </p>\n    <p>\n      For more information, refer to <a href=\"https://docs.clevertap.com/docs/create-message-web-push#web-push-editor\" target=\"_blank\"> Web Push Editor.</a></p>\n  </div>\n  <hr/>\n</div>\n"
}
[/block]


[block:html]
{
  "html": "<div class=\"release-note article\" data-category=\"journeys\" id=\"Scribe-for-Web-Push-Emotionally-Intelligent-Campaigns-Made-Easy\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#Scribe-for-Web-Push-Emotionally-Intelligent-Campaigns-Made-Easy\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/51dc269788d03bb7bc0482fbc020414bedd96b6c778ac37b71884095493b93c8-Journeys.svg\" alt=\"Journeys\"/>\n    </div>\n    <div>\n      <h3 class=\"release-note-heading\">Scribe for Web Push: Emotionally Intelligent Campaigns Made Easy</h3>\n    </div>\n    <div class=\"badge enhancement\">ENHANCEMENT</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>Scribe for CleverTap Web Push is here to transform your campaign messaging. With Scribe, you can easily and quickly create emotionally resonant web push messages. You can also analyze and refine their tone to better connect with your audience and test multiple variations to maximize campaign effectiveness. This feature is now available to all customers with access to Scribe as part of their Billing Plan.</p>\n    <p>For more information, refer to <a href=\"https://docs.clevertap.com/docs/scribe#create-a-web-push-notification-using-scribe\" target=\"_blank\">Scribe</a></p>\n  </div>\n  <hr/>\n</div>\n"
}
[/block]


[block:html]
{
  "html": "<div class=\"release-note article\" data-category=\"journeys\" id=\"Adding-Descriptions-for-Journey\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#Adding-Descriptions-for-Journey\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/51dc269788d03bb7bc0482fbc020414bedd96b6c778ac37b71884095493b93c8-Journeys.svg\" alt=\"Journeys\"/>\n    </div>\n    <div>\n      <h3 class=\"release-note-heading\">Adding Descriptions for Journey</h3>\n    </div>\n    <div class=\"badge new-feature\">NEW FEATURE</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>We are excited to announce that you can now add a description or summary while publishing a journey. This new feature allows you to provide additional context and insights to your internal users</p>\n    <p><img src=\"https://files.readme.io/6606e37749febb003bc2e1df1f618aa26654884baaf53ecb5d9ededceceaa829-Add_Journey_Description.gif\"/></p>\n    <p>You can update this description only when editing the published journey.</p>\n    <p>For more information, refer to <a href=\"https://docs.clevertap.com/docs/add-a-journey-description#publish-journeys\" target=\"_blank\">Publish journeys</a></p>\n  </div>\n  <hr/>\n</div>\n"
}
[/block]


## January

[block:html]
{
  "html": "<div class=\"release-note article\" data-category=\"signed-call\" id=\"Email-Add-on-for-CleverTap-Essentials-Plan\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#Email-Add-on-for-CleverTap-Essentials-Plan\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/90161cf9015e0e768441c7cefb5a62fb938b438ef6c4ce007cb705542234e2d8-Vector_1.svg\" alt=\"Signed call\"/>\n    </div>\n    <div>\n      <h3 class=\"release-note-heading\">Email Add-on for CleverTap Essentials Plan</h3>\n    </div>\n    <div class=\"badge private-beta\">PRIVATE BETA</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>The Email Add-on is now available with the CleverTap Essentials Plan. With this add-on, you can use CleverTap as your Email Service Provider (ESP), eliminating the need for third-party integrations.</p>\n    <p>To enable the Email add-on from the CleverTap dashboard, purchase the add-on, set up your email preferences, and warm up your dedicated IP to ensure the best possible deliverability.</p>\n    <p><img src=\"https://files.readme.io/8d30f945a8be7b21496ffed03e25b4dbb4f14e0f6ebbe14d23238770e2b9c7a8-Add_Journey_Description.gif\" />\n    </p>\n    <p>For more information, refer to <a href=\"https://docs.clevertap.com/docs/email-add-on-for-clevertap-essentials-plan\" target=\"_blank\">Email Add-on.</a></p>\n  </div>\n  <hr/>\n</div>\n"
}
[/block]


# 2024

## December

[block:html]
{
  "html": "<div class=\"release-note article\" data-category=\"segments\" id=\"Introducing-Reusable-Content-Blocks-for-greater-efficiency\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#Introducing-Reusable-Content-Blocks-for-greater-efficiency\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/04fe24c1114cef41af4a4e0224cab88f5be4c31160eca491d67942c689cb79c0-Segmentation.svg\" alt=\"Segmentation\"/>\n    </div>\n    <div>\n      <h3 class=\"release-note-heading\">Introducing Reusable Content Blocks for greater efficiency</h3>\n    </div>\n    <div class=\"badge private-beta\">PRIVATE BETA</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>We are excited to introduce Content Blocks in CleverTap’s Content Manager. Content Blocks are reusable snippets for standardized elements, such as footers, logos, or disclaimers.</p>\n    <p><img src=\"https://files.readme.io/a8ffbf71088fce311effa670335745e46b493562619202c2509ac6c7fa6ff1ae-Footer_Standardization_with_Content_Blocks.png\" />\n    </p>\n    <p>These blocks are designed to simplify the reuse of content across email campaigns, saving you valuable time. They help you maintain consistent messaging and standardize your brand communication.</p>\n  </div>\n  <hr/>\n</div>\n"
}
[/block]


[block:html]
{
  "html": "<div class=\"release-note article\" data-category=\"content-manager\" id=\"Store-Outgoing-Messages-Using-Message-Archiving\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#Store-Outgoing-Messages-Using-Message-Archiving\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/0ed57ff4730974458d74d2a34ec4cf285aa5e84f59075a6b32550b9d1fd60ae8-Content_Manager.svg\" alt=\"Content Manager\"/>\n    </div>\n    <div>\n      <h3 class=\"release-note-heading\">Store Outgoing Messages Using Message Archiving</h3>\n    </div>\n    <div class=\"badge beta\">BETA</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>Message Archiving now supports Google Cloud Platform (GCP), allowing customers to store copies of outgoing messages across different channels in real-time directly in their GCP bucket. The feature is in Public Beta and available to all CleverTap customers using AWS S3 buckets, Azure Blob, and GCP buckets.</p>\n    <p>For more information, refer to <a href=\"https://docs.clevertap.com/docs/message-archiving\" target=\"_blank\">Message Archiving.</a></p>\n  </div>\n  <hr/>\n</div>\n"
}
[/block]


## November

[block:html]
{
  "html": "<div class=\"release-note article\" data-category=\"analytics\" id=\"AppsFlyer-OneLink-Integration-for-Email\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#AppsFlyer-OneLink-Integration-for-Email\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/f57aa9f8ef374b2652d21d86c7251de0e10d2f8661a4828202bcced4cb299d5f-Analytics.svg\" alt=\"Analytics\"/>\n    </div>\n    <div>\n      <h3 class=\"release-note-heading\">AppsFlyer OneLink Integration for Email</h3>\n    </div>\n    <div class=\"badge private-beta\">PRIAVTE BETA</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>Introducing the updated AppsFlyer OneLink integration for Email. This new version makes it easier for users to set up and track clicks by managing everything from the AppsFlyer dashboard. You no longer need to configure anything on the CleverTap dashboard. The setup is now fully managed from the AppsFlyer dashboard itself, removing the need for configuration on CleverTap.</p>\n    <p>The older integration is no longer available, so you must switch to the new setup to keep using it. Currently, this integration supports Sendgrid ESP only. To enable it, contact AppsFlyer support.</p>\n    <p>For more information, refer to <a href=\"https://docs.clevertap.com/docs/appsflyer-onelink#set-up-appsflyer-onelinks\" target=\"_blank\">AppsFlyer OneLink Integration.</a></p>\n  </div>\n  <hr/>\n</div>\n"
}
[/block]


## October

[block:html]
{
  "html": "<div class=\"release-note article\" data-category=\"analytics\" id=\"Notification-Failed-Event-for---Email-Analytics\">\n  <div class=\"release-note-header\">\n    <div class=\"anchor-link-icon\">\n      <a href=\"#Notification-Failed-Event-for---Email-Analytics\"><i class=\"fa-light fa-anchor\"></i></a>\n    </div>\n    <div>\n      <img src=\"https://files.readme.io/f57aa9f8ef374b2652d21d86c7251de0e10d2f8661a4828202bcced4cb299d5f-Analytics.svg\" alt=\"Product Experiences\"/>\n    </div>\n    <div>\n      <h3 class=\"release-note-heading\">Notification Failed Event for Email Analytics</h3>\n    </div>\n    <div class=\"badge private-beta\">PRIAVTE BETA</div>\n  </div>\n  <div class=\"release-note-body\">\n    <p>Announcing a significant enhancement to our Email Analytics: the Notification Failed event that gives you more deeper insights into campaign errors. With this update, CleverTap captures a Notification Failed event, along with the reason for failure, enabling better targeting and resolution.</p>\n    <p>\n      <ul>\n  <li>\n    <b>Improved Targeting:</b> Target users through alternate channels when errors occur. \n    For example, if users encounter soft bounce errors, you can re-target them via other channels.\n  </li>\n  <li>\n    <b>Cleaner Email List:</b> Unsubscribe users with persistent errors to maintain an accurate and engaged subscriber base.\n  </li>\n  <li>\n    <b>Error Analysis:</b> Analyze the root causes of errors to resolve issues and optimize future engagements.\n  </li>\n</ul>\n\n    </p>\n    <p>For more information, refer to <a href=\"https://docs.clevertap.com/docs/events#:~:text=Notification%20Failed,in%20the%20campaign\" target=\"_blank\">Notification Failed Event.</p>\n  </div>\n</div>\n"
}
[/block]


[block:html]
{
  "html": "<style>\n  .release-heading-container {\n    display: flex;\n    align-items: center;\n    gap: 5px;\n  }\n  \n  .release-note-header div {\n    align-self: baseline;\n  }\n \n  .release-note-heading {\n    margin: 0 !important;\n    margin-bottom: 18px !important;\n  }\n  \n  .filters h3 {\n  margin-bottom: 12px;\n  font-size: 20px;\n}\n\n.filter-options {\n  display: flex;\n  flex-wrap: wrap;\n  gap: 20px;\n  align-items: center;\n}\n\n.filter-option {\n  flex: 0 0 calc(33.33% - 14px);\n  display: flex;\n  align-items: center;\n  gap: 10px;\n  font-size: 16px;\n  white-space: nowrap;\n}\n\n.filter-option img {\n  width: 16px;\n  height: 16px;\n}\n\n.content-manager {\n\tdisplay: flex;\n  align-items: center;\n  gap: 8px;\n}\n\n  \n  .badge {\n    font-size: 12px;\n    font-weight: 700;\n    color: white;\n  \tpadding:0px 4px;\n    border-radius: 5px;\n    display: inline-block;\n\t\tmin-width: max-content;\n}\n  \n  .anchor-link-icon {\n  margin-left: -23px;\n  opacity: 0;\n  transition: opacity 0.3s ease;\n}\n\n/* Show the anchor icon on hover */\n.release-note-header:hover .anchor-link-icon {\n  opacity: 1;\n}\n \n .anchor-link-icon{\n  \tmargin-left:-23px;\n  }\n.anchor-link-icon-inline {\n  display: flex;\n  align-items: center;\n  font-size: 1.2em;\n}\n  \n.release-note-header{\n  display:flex;\n  gap:8px;\n  align-items: center;\n }\n  \n.private-beta {\n    background-color: #B0B0B0;\n}\n  \n.beta {\n    background-color: #9E9E9E;\n}\n  \n.new-feature {\n    background-color: #4CAF50;\n}\n  \n.enhancement {\n    background-color: #2962FF;\n}\n  \n.update {\n    background-color: #673AB7;\n}\n  \n/* Hide all articles by default */\n.article {\n  display: none;\n}\n\n/* Show all articles if no filters are checked */\nbody:not(:has(.filters input:checked)) .article {\n  display: block;\n}\n\n/* Show matching articles */\nbody:has(#filter-campaigns:checked) .article[data-category=\"campaigns\"],\nbody:has(#filter-analytics:checked) .article[data-category=\"analytics\"],\nbody:has(#filter-segments:checked) .article[data-category=\"segments\"],\nbody:has(#filter-journeys:checked) .article[data-category=\"journeys\"],\nbody:has(#filter-signed-call:checked) .article[data-category=\"signed-call\"],\nbody:has(#filter-product-experiences:checked) .article[data-category=\"product-experiences\"],\nbody:has(#filter-content-manager:checked) .article[data-category=\"content-manager\"] {\n  display: block;\n}\n\n  \n</style>"
}
[/block]