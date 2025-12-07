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
# Overview

We have improved our deep linking with AppsFlyer for email. Marketers can now directly route users to the app from an email, bypassing the web browser. Deeplinking ensures a seamless user experience and solves the double redirection problem as users get a redirection to the app or an app store.

> 📘 Who?
>
> This integration works only for clients who have an AppsFlyer account.

# Steps to Enable Deeplinks

1. Navigate to *Settings* > *Channel* > *Email* and click **Setup** on the CleverTap dashboard.

<Image title="Deeplinking Navigation.png" alt={900} className="border" width="smart" border={true} src="https://files.readme.io/75139db-Deeplinking_Navigation.png" />

2. Click **Appsflyer domain deeplink** and the dropdown window displays.

<Image title="Appsflyer domain deeplink.png" alt={662} className="border" width="smart" border={true} src="https://files.readme.io/4d4b75c-Appsflyer_domain_deeplink.png" />

3. Enter the domain name you want to add as a deep link and click **Add**.

<Image title="Adding a domain.png" alt={609} className="border" border={true} src="https://files.readme.io/559920c-Adding_a_domain.png" />

> 🚧 Adding an Invalid Domain
>
> You can add multiple domains here, but not an invalid domain name.

4. Click **Save** to add multiple domains.

<Image title="Save domain.png" alt={600} className="border" border={true} src="https://files.readme.io/6e878e0-Save_domain.png" />

> 📘 Deleting a Domain
>
> To delete a domain, click the 'X' button and click **Save** to store the changes.

# Impact

This change allows users to add a list of domains, allowing email clicks to directly open an app whenever the user clicks on that link.

Deeplinking prevents multiple redirections that a user faces, improves overall UX, and increases user retention.
