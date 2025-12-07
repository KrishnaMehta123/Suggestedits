---
title: Uninstalls View
excerpt: ''
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

The *Uninstall* dashboard presents data on the number of users uninstalling your app, the number of new activations (first-time app launches), and the net number of new installs (new installs and total uninstalls for specific date ranges).

For more information, refer to [Uninstall Tracking](https://developer.clevertap.com/docs/uninstall-tracking).

<Image title="Analytics and Uninstalls View" alt={1719} align="center" border={true} src="https://files.readme.io/2227a783a033e49c5ddf128d5586b9b7819cd88c46964ddd2f7c0fc7cb639c0a-Uninstall.png">
  Activation and Uninstalls Analytics View
</Image>

To get to the uninstall view, navigate to *Boards* > *Uninstall*.

> 📘 Things to Consider
>
> Here are some things to consider: 
>
> * You must explicitly enable *Uninstall* detection feature from your dashboard.
> * Uninstall detection is only available for iOS and Android apps. 
> * Uninstall data is not available for Windows apps.

# Troubleshooting and FAQ

### Q. Why are most of my uninstalls tracked between 2 AM and 4 AM?

CleverTap runs a daily task at 2 AM (local time) to detect the number of uninstalls. You can account for this time to create campaigns and journeys to retain these users.

Check out our [App Uninstall Tracking](https://clevertap.com/blog/uninstall-tracking/) guide for a deeper dive into why tracking uninstalls matters and how to get it right.
