---
title: Branded Domain
excerpt: >-
  Learn how to configure system and custom domains to generate branded tracking
  links to boost engagement.
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

Branded Domains in CleverTap help you apply your brand to tracking across Email, SMS, WhatsApp, and RCS campaigns.

* For **SMS**, **WhatsApp**, and **RCS** campaigns, branded domains are used to generate short, trackable links.
* For **Email**, branded domains are used to track email open-tracking pixel.

Using branded domains improves user trust and can boost engagement rates.

# Domain Types

CleverTap supports two types of branded domains:

* **System Domain**: Provided by CleverTap, where you can customize the system-generated short links with your brand's prefix for easy integration without the need for DNS configuration.
* **Custom Domain**: Enables you to use your own subdomain for complete control over your branding and tracking. To use a custom domain, you will need to configure DNS records with your domain provider for proper verification and campaign tracking.

Both options allow you to define specific settings, such as the URL structure and 404 error page, ensuring your branded domain is set up to suit your needs.

# Add Domain

This section provides information about creating a branded system and a custom domain for your campaigns. Branded domain behavior varies by channel as follows:

| Channel                  | Supported Domain Types  | What Gets Branded                     |
| ------------------------ | ----------------------- | ------------------------------------- |
| **Email**                | Custom Domain only      | Tracked links and open-tracking pixel |
| **SMS / WhatsApp / RCS** | System or Custom Domain | Short tracking links                  |

## Add System Domain

You can create a system domain to quickly start using branded links in your WhatsApp camapigns without DNS configuration. To add a system domain, perform the following steps:

1. Go to _Settings_ > _Set Up_ > _Branded Domain_.

2. Click **Add Domain**, select _WhatsApp_, and click **Continue**. The _Add Domain_ page opens.

3. Enter the following details:

   <Image align="center" alt="System Domain Creation" border={true} caption="Add System Domain" src="https://files.readme.io/ca255b39acc146166fcf684f36a410fa508fc0c33d442e82d50fb7beeb0d07f0-Add_System_Domain.png" />

   <br />

   <Table align={["left","left"]}>
     <thead>
       <tr>
         <th>
           Field
         </th>

         <th>
           Description
         </th>
       </tr>
     </thead>

     <tbody>
       <tr>
         <td>
           Nickname
         </td>

         <td>
           Provide a name to identify the domain (for example, "Sales Campaign").
         </td>
       </tr>

       <tr>
         <td>
           Channel
         </td>

         <td>
           The channel where this branded domain will be used.

           * **Email**: Used for branded links and open-tracking pixels.

           * **WhatsApp/SMS & RCS**: Used for branded click-tracking links in messages.

           **Note**: Email campaigns support only Custom Domains.
         </td>
       </tr>

       <tr>
         <td>
           Domain Type
         </td>

         <td>
           The type of branded domain you’re adding.

           * **System Domain**: A CleverTap-provided domain that can be customized with your brand prefix. No DNS setup required.
           * **Custom Domain**: Your own subdomain (for example, links.yourbrand.com) that requires DNS configuration.
         </td>
       </tr>

       <tr>
         <td>
           Domain
         </td>

         <td>
           The base domain used for branding and tracking.

           * For **System Domains**, this is auto-filled based on your account region. For more information, refer to System Domain and Region Mapping below the table.
           * For **Custom Domains**, enter your own subdomain.
         </td>
       </tr>

       <tr>
         <td>
           Branded URL Schema
         </td>

         <td>
           Defines how the branded tracking URL is structured:

           URL Structure: `domain/adjoiner/Shortkey`

           This includes the following:

           * **Domain**:
           * **Adjoiner**: A brand-specific path separator that connects the Domain and Shortkey, helping personalize and group URLs. (@Shreejith/Jithendra: removed validation rules, as they will be shown to the users on the dashboard.)
           * **Shortkey**: A unique, auto-generated code added to the branded domain, helping track clicks on links within campaigns.

           For example, `ct3.io/clevertap/abc123`
         </td>
       </tr>

       <tr>
         <td>
           Error Page
         </td>

         <td>
           The page users see if a tracking link is invalid or has expired. You can use CleverTap’s system error page or provide a custom URL to maintain brand consistency even in error scenarios. Click _Preview Error Page_ to view and verify the error before the domain becomes active.
         </td>
       </tr>
     </tbody>
   </Table>

   <br />

4. Click **Save**. The domain status is set to **Active** immediately.

**System Domain and Account Region Mapping**

| Dashboard URL                | System Domain | Region      | Example URL   |
| :--------------------------- | :------------ | :---------- | :------------ |
| eu1.dashboard.clevertap.com  | ct1.io        | EU          | ct1.io/25AlJz |
| in1.dashboard.clevertap.com  | ct3.io        | IN          | ct3.io/52KlAz |
| sg1.dashboard.clevertap.com  | ct4.io        | SG          | ct4.io/25ZlAz |
| us1.dashboard.clevertap.com  | ct5.io        | US          | ct5.io/52ZlKa |
| mec1.dashboard.clevertap.com | ct8.io        | Middle East | ct8.io/25ZaJz |
| aps3.dashboard.clevertap.com | ct9.io        | Indonesia   | ct9.io/52KJz  |

## Add Custom Domain

Use your own subdomain (for example, `sales.yourbrand.com`) for maximum brand visibility. This option allows you to fully control the branding and tracking for your campaigns.

<Callout icon="📘" theme="info">
  #### Custom Domain

  You can add up to 5 unique custom domains per account per channel.
</Callout>

### For WhatsApp/SMS & RCS

To add a custom domain, perform the following steps:

1. Repeat steps _1_ through _3_ under Add System Domain. except that select _Domain Type_ as _Custom_.
2. Click **Save & Generate DNS**. The domain status is set to **Pending Verification** immediately and DNS Records are generated to configure it on your Domain provider dashboard.

<Image align="center" alt="Custom Domain Creation" border={true} caption="Custom Domain Creation" src="https://files.readme.io/7915e7432f0a7c1851decf9bff092a9b55eadf127645140bb2aa3ce4b7e2147a-Add_Custom_Domain_for_WhatsAppSMS__RCS.png" />

### For Email

To configure your custom domain, perform the following steps:

1. Go to _Settings_ > _Set Up_ > _Branded Domain_.

2. Click **Add Domain**, select _Email_, and click **Continue**. The _Add Domain_ page opens.

3. Enter the following details:  _Nickname_ and _Domain_.

   <Image align="center" border={true} caption="Add Custom Domain for Email" src="https://files.readme.io/ece7c12d5494a02f09b09dfafe7d7f699078afcbd719d219dc54c92eea6b5147-Add_Custom_Domain_for_Email.png" />

4. Click **Save & Generate DNS**. The domain status is be set to **Pending Verification** immediately and DNS Records will be generated for you to configure with your Domain provider.

<Image align="center" border={true} caption="DNS Records Generated" src="https://files.readme.io/6d90a8eaa27f1d56aae290b66bf962fcd1b1ee164bddfe3bc0779a7a310d4f48-image.png" />

### Verify Custom Domain

(@Shreejith, This applies to Email as well, so adding a cross-reference to this section.)

1. Go to the domain provider dashboard and configure the following DNS records. When configuring DNS records with your domain provider, enter only the prefix part in the Name field. The prefix is the part that precedes the main domain. For example, if the CNAME is `_c58ebcb5c******5f03bb6b174349.short.clevertap.com`, enter `_c58ebcb5c******5f03bb6b174349.short` in the Name field.

| Type  | Description                                               | Key (Name)                                         | Value                                                      |
| ----- | --------------------------------------------------------- | -------------------------------------------------- | :--------------------------------------------------------- |
| CNAME | Used for domain ownership verification.                   | _c58ebcb5c******5f03bb6b174349.short.clevertap.com | _0f8561a2dc*******9ef25e32f6.xl****vlj.acm-validations.aws |
| CNAME | Redirects branded links to CleverTap's short URL service. | short.clevertap.com                                | short-clevertap-com.cltap.com                              |
| TXT   | Verifies domain association with CleverTap.               | _txt-6**-R**-R47Z.short.clevertap.com              | ct0.co=2c1f96426804                                        |

`.

2. Once your DNS records are saved, go back to the **Branded Domain** page on the CleverTap dashboard.
3. Click the ![](https://files.readme.io/c637417f8cac230dcf67387780cea85c586b965f8272fea35db6d1d6141c1ecb-Screenshot_2025-12-17_at_9.37.30_PM.png) icon next to your domain. DNS propagation may take up to 24 hours to complete. If verification fails, check your DNS configuration with your domain provider to ensure it is accurate. If the settings are correct, try refreshing after some time.

# Manage Branded Domains

The Domain Listing page allows you to view and manage all your configured domains. You can easily edit domain settings, view DNS records, and make any necessary updates to check if your domains are properly set up and functioning.

Go to _Settings_ > _Set Up_ > _Branded Domains_. You can see a list of all your domains (system or custom), including the following details:

<Image align="center" border={true} caption="Branded Domains Page" src="https://files.readme.io/2fbb49c4e3a18c0744338f8f2db30ae4f28a3babf5c0f3eb1289f175dc099f41-Branded_Domain_Listing_Page.png" />

| Column            | Description                                                                                                                |
| :---------------- | :------------------------------------------------------------------------------------------------------------------------- |
| _Nickname_        | A user-defined name for identifying the domain (for example, "Sales Campaign").                                            |
| _Domain URL_      | The full URL of the domain being used for tracking links (for example, `ct3.io/clevertap/abc123`, `track.yourdomain.com`). |
| _Created By_      | The user who created the domain.                                                                                           |
| _Status_          | The current status of the domain can be **Active** or **Pending Verification**.                                            |
| _Last Updated On_ | The date when the domain settings were last updated.                                                                       |

After adding the domain, you can perform the folloeing operations by hovering over the branded domain:

<Image align="center" border={true} caption="Manage Branded Domains" src="https://files.readme.io/a4ad7fef6b3c58d079a57876f5c3d45be43447b1298499d715bdf28d0e2dbafd-Manage_Branded_Domains.gif" />

* **Set as Default**: You can set any verified domain as the default. This domain is automatically used for wrapping and tracking links in SMS, WhatsApp, RCS, and Email campaigns (including template buttons). You can override it per campaign when creating new ones.

* **Edit**: For each domain (except system defaults), you can set a custom 404 error page. This page is displayed if users click on expired links (older than 7 days).

* **Verify Domain**: You can manually verify the domain by checking the status. If the verification fails, you can click the ![](https://files.readme.io/c5163a3fa40adb8519750791f8de9e7a6736bfe7a28cdbe65c5de3281357911f-Screenshot_2025-12-17_at_9.37.30_PM.png) icon next to the domain to retry.

* **View DNS Records**: You can access and review the DNS settings associated with your domain. This includes details such as CNAME and TXT records, which are essential for domain verification and proper tracking. By viewing these records, you can ensure that the domain is correctly configured with your DNS provider for seamless integration and functionality.

## FAQs

(@Jithendra/Shreejith: IMO, we can remove a few FAQs here as most of it is already covered in the content. We can retain the best Practices & the Link Preview question. Rest is repeated information. I haven't reviewed the FAQs content, though.)

### What is a branded domain, and why should I set it up?

A branded domain is a custom or customized URL that tracks clicks from your SMS, WhatsApp, or RCS campaigns. It helps build brand trust, improves click-through rates, and complies with regulations such as **DLT Whitelisting** (especially in India).

### What’s the difference between a system domain and a custom domain?

* **System Domain**: Provided by CleverTap (for example, `ct3.io`) and ready to use. You can customize the path (`/brand/`) or query parameter (`?key=brand`) to brand it.
* **Custom Domain**: Your own subdomain (for example, `links.yourbrand.com`) that you configure via your domain provider with DNS settings.

### What is an Adjoiner, and why is it needed?

An **Adjoiner** is the part of the URL that appears between the domain and the short key. It adds brand identity and structure to the tracking URL. The adjoiner is required to create a valid branded domain URL.  
Example:

* **Path-based**: `ct3.io/yourbrand/abc123`
* **Query-based**: `ct3.io?key=yourbrand&sk=abc123`

### **Can I use special characters in the adjoiner?**

No. The **Adjoiner** can only contain lowercase letters, numbers, and hyphens. It must not start or end with a hyphen, and cannot contain special characters such as `@`, `#`, `&`, and so on.

### **Can I switch between path-based and query-based adjoiners?**

No, you must choose one format per domain — either **path-based** (`/yourbrand/`) or **query-based** (`?key=yourbrand`). You cannot mix both formats in a single domain configuration.

### **What happens if a user clicks an expired link?**

If a link is older than 7 days, it expires. You can configure a **404 Error Page URL** for each domain, which will be shown to users who click on expired links.

### **What is the default domain and how does it work?**

The **Default Domain** is automatically used to wrap and track links in **SMS**, **RCS**, and **WhatsApp** campaigns (including template buttons). You can override the **Default Domain** per campaign by selecting a different domain from the dropdown when creating new campaigns.

### **Will old campaigns use the new branded domain?**

No. Campaigns created before you set up a branded domain will continue using the **System Domain** unless you manually edit or recreate them with the new branded domain.

### **How long does domain verification take?**

Custom domains require **DNS record configuration**. While CleverTap fetches DNS updates automatically, it may take up to **24 hours** for DNS changes to propagate globally. You can click the **refresh** icon to retry verification.

### **I configured the DNS records, but my domain has still not been verified. What should I do?**

Check the following:

* **DNS records** are entered exactly as shown in the CleverTap dashboard.
* You’ve entered only the required prefix in the **Key** field (for example, short, not short.clevertap.com)
* Wait up to 24 hours, then try refreshing again

### What are the best practices for adding a branded domain in CleverTap?

Here are some tips to ensure your branded domain setup is effective and compliant:

* **For System Domains** (like `ct3.io/yourbrand/abc123`):
  * Choose a short and meaningful **Adjoiner** that clearly represents your brand or campaign type.
  * Use lowercase letters and hyphens (`-`) if needed (for example, `/clevertap/`, `/new-user/`, `/sale2024/`).
  * Keep it concise: Aim for 5–8 characters in the **Adjoiner** (excluding the slashes) to avoid long URLs in **SMS** or **WhatsApp** messages.
  * Avoid vague terms like `/track/` or `/link/` — use something unique to your brand.
* **For Custom Domains** (like `links.yourbrand.com`):
  * Use a subdomain such as **links.**, **click.**, or **promo.** (for example,`links.yourbrand.com`, `click.yourbrand.com`).
  * Keep the **Subdomain** short, relevant, and easy to remember.
  * Avoid complex words, long phrases, or special characters in the **Subdomain** name.
  * Ensure you configure **DNS records** exactly as shown after setup to avoid delays in verification.

**Avoid**:

* Using more than 20 characters in the **Adjoiner** or **Subdomain**
* Starting or ending **Adjoiners** with hyphens
* Using non-brand-specific generic terms

> 📘 Pro Tip: Buy a new short domain for campaigns
>
> If your existing domain is long or complex, consider purchasing a new, short domain for marketing messages. Ideally, the domain must be 5–8 characters long and phonetically similar to your brand name. This improves:
>
> * Link trustworthiness
> * User recall and voice-based sharing (for example, over phone or radio)
> * Visual clarity in messages and notifications
>
> **Examples**:
>
> * If your brand is **MobiKart**, consider domains like **mobkt.in**, **mobik.in**, or **mkrt.co**.
> * If your brand is **FreshBite**, try **frsbt.com**, **frbite.in**, etc.

### When will a link preview be shown for my branded domain link?

A link preview is generated when the messaging platform (such as SMS, WhatsApp, or RCS) scans the URL included in your message and detects the required Open Graph metadata on the destination page. The following tags must be present and properly configured in the page’s HTML:

* `<meta property="og:title" content="...">`
* `<meta property="og:description" content="...">`
* `<meta property="og:image" content="...">`

If these tags are available and valid, the platform may display a visual preview containing a title, description, and image. A preview may not be shown in the following cases:

* The Open Graph tags are missing or incorrectly implemented
* The domain is blocked by `robots.txt` or firewalls
* The page is inaccessible to external crawlers

To validate whether your Open Graph metadata is implemented correctly, use any metadata testing tool or Open Graph debugger.

### How do link previews work on iOS devices, and why might they not appear?

iOS devices running version 10 or above support link previews in the native Messages application. These previews may still appear for SMS-based messages, but several conditions must be met for reliable rendering.

**Preview requirements**

* Only one link should be included in the message. Messages with multiple links will not generate a preview.
* The link must be the final element in the message. No text, punctuation, or symbols should follow the link.
* The domain must be served over HTTPS and use a valid SSL certificate. Self-signed, expired, or incomplete certificates will block preview generation.
* The recipient must tap _Tap to Load Preview_ for metadata to be fetched.

**iOS-specific behaviors and limitations**

* iOS delays metadata fetching until after the message is delivered, and in some cases, until the user interacts with the message.
* Devices may display cached metadata even after updates have been made to the page’s Open Graph tags.
* Certain third-party messaging apps may block previews by default unless explicitly enabled in settings.

These constraints can lead to inconsistent preview rendering on iOS devices even when metadata is correctly configured.
