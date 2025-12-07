---
title: Unusually High Email Opens and Clicks
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
A well-designed email campaign can help you get more reach and conversions. However, you may sometimes observe unusually high email open and click counts for a set of campaigns or users (for example, B2B domains). It can be due to a variety of reasons. 

# Unusually High Opens

Multiple opens means that the recipient opened your email numerous times.  However, there may be instances where the email *opens* exceeds expectation, or *opens* for a recipient are registered multiple times in quick succession. It can be due to the following reasons:

* Email Clients - Many email clients, such as (Outlook or Apple Mail) have a preview pane as part of the inbox view. A recipient scrolling over your email in their inbox (even passively) can trigger an email open notification. Industry-wide opens are tracked using images. When an image is displayed, the email is counted as open. The email client controls this display and is not distinguishable from human opens. 

* Email Forwards - The forwarded email is an exact copy of the original email. Forwarded emails can also add to the *open* count.  The open is attributed to the original recipient, even if the recipient of the forwarded email opens the email. 

* Virus Scanners - These scanners sometimes preview emails to determine whether they are spam. However, there is no way to distinguish between machine and human opens.

* Email Groups - If a user signs up for your service with a group address, all the opens are attributed to a single profile or email address qualifying for the email campaign.

* CC/BCC Recipients - If you add CC/BCC recipients to your email campaigns, all the opens by the CC/BCC recipients are attributed to the main recipients who qualify for the campaign. This feature is released in Private Beta. You can [add CC/BCC recipients](doc:create-message-email#ccbcc) in emails for the following providers: SendGrid, Amazon SES, and Generic SMTP setup. If you want to access this feature, contact your Customer Success Manager.

# Unusually High Clicks

* Email Forwards - CleverTap adds unique tracking info to each URL in an email campaign. The forwarded email is an exact copy of the original email. All the clicks are attributed to the original recipient, even if the recipient of the email forwarded clicks the email. There is no way to distinguish between the original recipient and the forwarded email recipient.

* Spam Filters - A spam filter may click the links in your emails. Aggressive spam filters click links in emails to check for malicious activity before delivering them to the recipients. Unfortunately, there is no way to verify if a spam filter or your intended recipient clicked a link. However, if you see unusually high clicks from a single domain, it will likely be a spam filter.

* CC/BCC Recipients - If you add CC/BCC recipients to your email campaigns, all the email clicks by the CC/BCC recipients are attributed to the main recipients who qualify for the campaign. This feature is released in Private Beta. You can [add CC/BCC recipients](doc:create-message-email#ccbcc) in emails for the following providers: SendGrid, Amazon SES, and Generic SMTP setup. If you want to access this feature, contact your Customer Success Manager.
