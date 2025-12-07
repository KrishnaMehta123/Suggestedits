---
title: Deeplinking with AppsFlyer
excerpt: Open mobile application using deep-link without rerouting
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
#Overview
We have improved our deep linking with AppsFlyer for email. Marketers can now directly route users to the app from an email, bypassing the web browser. Deeplinking ensures a seamless user experience and solves the double redirection problem as users get a redirection to the app or an app store.
[block:callout]
{
  "type": "info",
  "body": "This integration works only for clients who have an AppsFlyer account.",
  "title": "Who?"
}
[/block]
#Steps to Enable Deeplinks

1. Navigate to *Settings* > *Channel* > *Email* and click **Setup** on the CleverTap dashboard.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/75139db-Deeplinking_Navigation.png",
        "Deeplinking Navigation.png",
        900,
        472,
        "#f5f6f8"
      ],
      "border": true,
      "sizing": "smart"
    }
  ]
}
[/block]
2. Click **Appsflyer domain deeplink** and the dropdown window displays.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/4d4b75c-Appsflyer_domain_deeplink.png",
        "Appsflyer domain deeplink.png",
        662,
        123,
        "#f8f8fa"
      ],
      "border": true,
      "sizing": "smart"
    }
  ]
}
[/block]
3. Enter the domain name you want to add as a deep link and click **Add**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/559920c-Adding_a_domain.png",
        "Adding a domain.png",
        609,
        279,
        "#f8f8fb"
      ],
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "warning",
  "body": "You can add multiple domains here, but not an invalid domain name.",
  "title": "Adding an Invalid Domain"
}
[/block]

4. Click **Save** to add multiple domains.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6e878e0-Save_domain.png",
        "Save domain.png",
        600,
        260,
        "#f6f7fa"
      ],
      "border": true
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "body": "To delete a domain, click the 'X' button and click **Save** to store the changes.",
  "title": "Deleting a Domain"
}
[/block]
#Impact
This change allows users to add a list of domains, allowing email clicks to directly open an app whenever the user clicks on that link.

Deeplinking prevents multiple redirections that a user faces, improves overall UX, and increases user retention.