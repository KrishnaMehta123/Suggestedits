---
title: Setup
excerpt: >-
  Understand how to integrate Facebook Audiences with CleverTap to be able to
  run marketing campaigns
deprecated: true
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: >-
    Refer to the pages listed below to learn more about the following Facebook
    Audiences sections:
---
The benefit of integrating your Facebook Audiences account with CleverTap is getting per-campaign, per-user cost data and the average revenue for users acquired via that campaign. It helps you understand the cost of a campaign against its revenue.

# Integrate Facebook Ads Account

> 📘 Admin Access
> 
> You must have admin access to FB accounts to connect your Facebook Audiences account with the CleverTap dashboard.

## Get Your Facebook Audiences Account ID

1. Log in to your [Facebook Ads account](https://www.facebook.com/ads/manage/home/).
2. Navigate to _Settings_, and copy the _Account ID_ visible under _Account Information_.

## Connect Facebooks Audiences Account

1. Log into your CleverTap Dashboard, and navigate to _Settings_ > _Channel_ > _Remarketing_. 

> 📘 Users with Multiple CleverTap Accounts
> 
> If you have multiple CleverTap accounts, check that you are using the correct account.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e9635a5-Faceebook_Account_Keys.png",
        "Integrate Facebook and Google Ads Account Keys",
        2302
      ],
      "align": "center",
      "border": true,
      "caption": "Integrate Facebook and Google Ads Network to Enable Remarking Messages"
    }
  ]
}
[/block]



2. Paste the _Account ID_ you copied in the above step, and click **Connect**.
3. Click **Okay** when prompted by Facebook to give access to CleverTap.

After establishing the connection successfully, the message _Account connected successfully_ displays. The initial campaign data will display in two hours and is subsequently updated every two hours.

> 📘 Additional Notes
> 
> Check that your Facebook Ad campaign links are tagged with the following parameters for them to show up in the _Campaign_ dashboard:
> 
> - wzrk_source=facebook
> - wzrk_campaign=\<campaign_name>