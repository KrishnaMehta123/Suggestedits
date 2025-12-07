---
title: Setup
excerpt: >-
  Understand how to integrate Facebook Audiences with CleverTap to be able to
  run marketing campaigns
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: >-
    Refer to the pages listed below to learn more about the following Facebook
    Audiences sections:
  pages:
    - type: link
      title: Create Message
      url: https://docs.clevertap.com/docs/create-message-fb-audience_c20
    - type: link
      title: Facebook Audiences Campaign Stats
      url: https://docs.clevertap.com/docs/facebook-audience-stats_c20
---
The benefit of integrating your Facebook Audiences account with CleverTap is getting per-campaign, per-user cost data and the average revenue for users acquired via that campaign. This helps you understand the cost of a campaign versus the revenue earned with it.

# Integrate Facebook Ads Account

> 📘 Admin Access
>
> You must have admin access to FB accounts to connect your Facebook Audiences account with the CleverTap dashboard.

## Get Your Facebook Audiences Account ID

1. Log in to your [Facebook Ads account](https://www.facebook.com/ads/manage/home/).
2. Navigate to *Settings*, and copy the *Account ID* visible under *Account Information*.

## Connect Facebooks Audiences Account

1. Log into your CleverTap Dashboard, and navigate to *Settings* > *Channel* > *Remarketing*. 

> 📘 Users with Multiple CleverTap Accounts
>
> If you have multiple CleverTap accounts, check that you are using the correct account.

<Image title="Faceebook Account Keys.png" alt={2302} className="border" border={true} src="https://files.readme.io/e9635a5-Faceebook_Account_Keys.png" />

2. Paste the *Account ID* you copied in the above step, and click **Connect**.
3. Click **Okay** when prompted by Facebook to give access to CleverTap.

After establishing the connection successfully, the message *Account connected successfully* displays. The initial campaign data will display in two hours and is subsequently updated every two hours.

> 📘 Additional Notes
>
> Check that your Facebook Ad campaign links are tagged with the following parameters for them to show up in the *Campaign* dashboard:
>
> * wzrk\_source=facebook
> * wzrk\_campaign=\<campaign\_name>
