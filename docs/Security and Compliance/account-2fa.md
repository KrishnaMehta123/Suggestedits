---
title: Two-Factor Authentication (2FA)
excerpt: Understand how 2FA configuration works on the CleverTap dashboard
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

Keeping your data safe is of utmost importance. Two-Factor Authentication (2FA) adds extra security because it requires CleverTap Dashboard users to provide a unique verification code from an authenticator app in addition to their sign-in credentials when they log into the CleverTap. 

[block:callout]
{
  "type": "info",
  "body": "From December 01, 2022, all CleverTap projects will have mandatory Two-Factor Authentication enabled except for the projects that use Single-Sign On (SSO). For any questions, refer to [FAQs](doc:account-2fa#faqs)",
  "title": "Important"
}
[/block]

2FA is a critical security measure that adds a second layer of protection in addition to your password and requires CleverTap Dashboard users to provide a unique verification code from an authenticator app in addition to their sign-in credentials. 

# Set up 2FA

Once 2FA is enabled, CleverTap will generate a unique QR code for each user trying to log in.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2d998cc-2fa_QR.png",
        "2fa QR.png",
        738,
        1022,
        "#000000"
      ],
      "border": true,
      "sizing": "smart",
      "caption": "Set-up Two factor Authentication"
    }
  ]
}
[/block]
You need to:
1. Download the Google Authenticator app from [Google Play Store](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&hl=en_IN&gl=US&pli=1) or the Apple [App store](https://apps.apple.com/us/app/google-authenticator/id388497605).
2. Scan the QR code.
3. Enter the verification code generated on the Authenticator app and click *Authenticate*.

After this setup, for all the subsequent logins, you will need to enter the 2FA verification code from the *Authenticator* app as shown below.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/120ef9c-2_step_ver.png",
        "2 step ver.png",
        710,
        748,
        "#000000"
      ],
      "border": true,
      "sizing": "smart",
      "caption": "Two Step Verification Screen11"
    }
  ]
}
[/block]
# How to Reset the 2FA Key

If a user cannot provide a verification code during log-in, either due to losing access to the Google Authenticator app or losing the device itself, a dashboard admin must be asked to reset the respective user's 2FA key from the dashboard.

To do so, the admin needs to:

1. Navigate to *Settings* > *Security* > *Two-Factor Authentication*. This will display the list of all user email addresses with 2FA enabled.

2. Click the reset icon adjacent to the user project for which you need to reset the 2FA key.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f2a82b5-2FA_N2.png",
        "2FA N2.png",
        1212,
        1164,
        "#e9ecf3"
      ],
      "border": true,
      "caption": "Reset 2FA View"
    }
  ]
}
[/block]
After an administrator resets a key for a project, the user is asked to set up Two-Factor Authentication on their next login.

If none of the administrators can access the dashboard, raise a support ticket via [Help Center](https://help.clevertap.com/)

#FAQs

##What should I do if I do not have a verification code?
Contact an admin in your project to reset your 2FA key. After resetting, you should be able to set up the 2FA authentication on your desired device.

##I lost my device that had 2FA configured. What should I do?
Contact an admin in your project to reset your 2FA key. After resetting, you should be able to set up the 2FA authentication on your desired device.

##Why am I not able to toggle the project level 2FA?
Two-Factor Authentication is mandatory for security reasons. If you are facing any issues, raise a support ticket from your CleverTap dashboard or reach out to your Customer Success Manager.

##Is 2FA applicable for SSO users?
SSO supersedes 2FA. A user will not be asked for a 2FA verification code if SSO is enabled for their project.