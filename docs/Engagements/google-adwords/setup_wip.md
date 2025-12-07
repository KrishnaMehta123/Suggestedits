---
title: Setup_WIP
excerpt: >-
  Understand how to integrate Google Ads with CleverTap to run marketing
  campaigns.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
You must integrate Google Ads, and CleverTap accounts to segment users in CleverTap and automatically upload those users to the Google Ads account. The integration enables you to easily run remarketing campaigns where you show ads to specific segments of your users across Google Search Network, YouTube, and Gmail.

## Connect Google Ads Account
Connect the Google Ads account to your CleverTap account. The *Google ads account ID *is available at the top right on your Google Dashboard. For more information about finding your Ads Customer ID, refer to [Google Support](https://support.google.com/ads/express/answer/6083253).

The process involves adding Google Ads Customer ID to the CleverTap dashboard. To do so: 

1. Log in to the [CleverTap Dashboard](https://dashboard.clevertap.com/). 
2. Navigate to *Settings* > *Channels* > *Remarketing*.
3. Enter the *Google ads account ID*, and then click **Connect**.
4. (Optional) Enter your Manager account ID for a linked [Manager Account](https://ads.google.com/intl/en_in/home/tools/manager-accounts/).
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/b74ffb0-google_ads_manager_id.png",
        "google_ads_manager_id.png",
        1600,
        1092,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "Admin User",
  "body": "The user with Admin rights on Google Ads Platform can integrate Google Ads and CleverTap accounts."
}
[/block]
5. Click **Continue** when prompted by Google to give access to CleverTap.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/944d50f-google_ads_allow_r.png",
        "google_ads_allow_r.png",
        400,
        544,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "warning",
  "body": "If you have multiple CleverTap accounts, check that you are using the correct account. Similarly, if you have multiple Ads accounts, verify it is the correct account.",
  "title": "Verify Credentials"
}
[/block]