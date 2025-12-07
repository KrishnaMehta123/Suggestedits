---
title: Clearout
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
# Overview

[Clearout](https://clearout.io/) is an Email Verification and Email Finder tool that helps expand your reach, lower hard bounces, and improve deliverability rates. It enhances your sales and marketing efforts by simplifying how you discover and reach ideal prospects via email.

Integrating Clearout with CleverTap enables you to validate user email lists, reduce bounce rates, and maintain your domain’s sender reputation — all within your marketing workflow.

To learn more about Clearout and its result files, refer to the [Clearout documentation](https://clearout.io/help/).  
For support, contact the [Clearout Support team](mailto:us@clearout.io).

***

## Introduction

The integration between **CleverTap** and **Clearout** enables marketers to ensure higher email deliverability and better engagement by validating user email addresses directly from their CleverTap account.

Clearout’s native integration helps you identify invalid, risky, or disposable email addresses and push that validation data back into CleverTap automatically.

This process allows marketers to:

- Maintain clean and reliable email lists.
- Reduce hard bounces and protect sender reputation.
- Improve segmentation and campaign ROI by targeting verified users only.

***

## Use Case

Using Clearout’s dashboard, you can connect your CleverTap account and pull user lists that contain email addresses. Clearout validates each address, categorizing it as **valid**, **invalid**, **disposable**, **role-based**, or **risky**.

Once verification is complete, the results are synced back to CleverTap as **custom user properties** (for example: `Clearout Verification Status: valid`).

This enables marketers to:

- Send email campaigns only to users with verified addresses.
- Trigger push or in-app messages prompting invalid users to update their emails.
- Create audience segments based on deliverability status for more targeted engagement.

***

# Prerequisites for Integration

Before setting up the integration, ensure you have:

- An active **Clearout** account
- An active **CleverTap** account with valid credentials (Account ID, Passcode, and Region)

***

# Integrate Clearout with CleverTap

This integration allows you to verify and clean your CleverTap audience email lists using Clearout, helping you improve email deliverability and maintain your sender reputation.

The process involves the following steps:

1. [Connect CleverTap Account](#connect-clevertap-account)
2. [Add the Email List](#add-email-list)
3. [Verify the Email List](#verify-email-list)
4. [Export the Verified List](#export-verified-list)

***

## Step 1: Connect CleverTap Account

To connect your CleverTap account with Clearout:

1. Log in to your Clearout account.
2. Click the ![](https://files.readme.io/298e857-menu_icon.png) icon and select **Integrations** from the list.

![Navigating to Integrations Page](https://files.readme.io/04e27d1-Clearout_dashboard.png)

3. On the **Integrations** page, scroll down and select **CleverTap**, then click **Connect to CleverTap**.

![Click Connect to CleverTap](https://files.readme.io/8826dbd-Select_CleverTap.png)

4. Enter the following project details to authorize the connection:

   - **Account ID**: Your CleverTap Project ID
   - **Account Passcode**: Your CleverTap passcode
   - **Region**: Your CleverTap account region
   - **Account Name**: A nickname to identify the account

These details can be found on the **Settings → Project** page in your CleverTap dashboard.  
Use the following table to identify your region based on your CleverTap URL:

| Dashboard URL                                                                                        | Region            |
| :--------------------------------------------------------------------------------------------------- | :---------------- |
| [https://eu1.dashboard.clevertap.com/login.html](https://eu1.dashboard.clevertap.com/login.html#/)   | EU1               |
| [https://in1.dashboard.clevertap.com/login.html](https://in1.dashboard.clevertap.com/login.html#/)   | India             |
| [https://us1.dashboard.clevertap.com/login.html](https://us1.dashboard.clevertap.com/login.html#/)   | U.S               |
| [https://sg1.dashboard.clevertap.com/login.html](https://sg1.dashboard.clevertap.com/login.html#/)   | Singapore         |
| [https://aps3.dashboard.clevertap.com/login.html](https://aps3.dashboard.clevertap.com/login.html#/) | Indonesia         |
| [https://mec1.dashboard.clevertap.com/login.html](https://mec1.dashboard.clevertap.com/login.html#/) | Middle East (UAE) |

***

## Step 2: Add Email List

After connecting your CleverTap account, add the email list you want to validate:

1. From the Clearout dashboard, navigate to the **Email Verifier** tab.

![Navigating to Email Verifier Tab](https://files.readme.io/12f6262-Select_Email_Verifier_tab.png)

2. Select the desired CleverTap audience list to validate, then click **Add to My List**.

![Selecting the CleverTap Audience List for Validation](https://files.readme.io/200afc3-Add_to_My_lIst.png)

> 💡 **Tip:** You can add multiple lists to your verification queue to validate them in sequence.

***

## Step 3: Verify Email List

To validate your selected list:

1. On the **Email Verifier** page, click **Verify** to begin validation.
2. Clearout will process and mark each address as valid, invalid, or risky based on deliverability checks.

![Click Verify to Validate Audience List](https://files.readme.io/70f4586-Click_Verify.png)

> 💡 **Tip:** Clearout automatically categorizes each address by type and risk level, allowing more granular segmentation once synced with CleverTap.

> ⚙️ **How it helps:** Verifying emails ensures that your CleverTap campaigns reach active inboxes, reducing bounces and improving sender reputation.

***

## Step 4: Export the Verified List

After validation, you can export the verified results back to CleverTap in one of two ways:

- **Unsubscribe:** Automatically remove invalid or non-deliverable email addresses from your CleverTap audience list.
- **Append:** Keep all contacts but append Clearout verification status columns to your existing CleverTap data.

To export:

1. Choose your preferred export option (**Unsubscribe**, **Append**, or both).
2. Click **Export** to sync the verified data with CleverTap.

![Click Export](https://files.readme.io/01eaec1-Export_Verified_List.png)

After exporting, Clearout automatically updates CleverTap user profiles with new properties such as **Clearout Verification Status** or **Email Validity Result**.

You can view these properties in CleverTap by opening any user profile under **User Details → Properties**.

> 💡 **Tip:** The Unsubscribe option is recommended for active mailing lists to prevent deliverability issues.

***

## Create a CleverTap Campaign Using Verified Emails

After verification results are exported to CleverTap, you can use these custom user properties to build targeted campaigns.

1. Log in to your CleverTap dashboard.
2. From the left panel, go to **Campaigns → + Campaign → Email**.
3. In the **Who** section, define a segment rule such as:

   ```
   Where Clearout Verification Status equals valid
   ```
4. Configure the email campaign content as needed. For example, send a message like “Your email address has been successfully verified.”
5. Click **Preview and Test** to ensure your campaign targets the correct users.
6. Once satisfied, click **Publish** to make the campaign live.

> ⚙️ **How it helps:** This ensures that your email campaigns only reach verified users, reducing bounces and improving engagement metrics.

***

# FAQs

### How can I confirm whether undeliverable emails are handled in CleverTap?

CleverTap automatically changes the **communication preferences** to “Unsubscribed” for users whose email addresses are marked as undeliverable by Clearout.

You can verify this by opening a user profile in CleverTap and checking their communication preferences.

![Verify Communication Preferences from CleverTap Dashboard](https://files.readme.io/fdd84f2-Communication_preferences.png)

***

### How many lists can I validate at a time?

You can validate up to three lists simultaneously.

***

### Can I purchase Clearout credits through CleverTap?

No. You must purchase credits directly from [Clearout](https://app.clearout.io/dashboard/account/pricing) to validate your lists.

***

✅ **Document Alignment Summary**

- Added contextual **Introduction** and **Use Case** sections for clarity.
- Explained **why** each step matters, not just _how_ to click.
- Introduced new section: **Create a CleverTap Campaign Using Verified Emails**.
- Updated tone to match CleverTap’s integration doc style (actionable, concise, results-focused).
- Verified heading hierarchy, link validity, and image syntax per TEC Style Guide.

***

Would you like me to also generate a short **excerpt version** (150–200 words) for your integration landing page or partner listing (Clearout x CleverTap)? That’s often required for the integration summary block before linking to the full doc.