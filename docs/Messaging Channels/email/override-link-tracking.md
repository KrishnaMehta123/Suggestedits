---
title: Override Link Tracking
excerpt: Learn how to override redirection of Email links to the CleverTap server.
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

To track clicks on email links, CleverTap redirects the links of your email body, first to a CleverTap server and then back to your landing page.

If you want to avoid click tracking through CleverTap, set the following tag in your email body:

```html
<a data-track="off" href="donotoverrride"> Your link </a>
```

Setting this tag will ensure that CleverTap does not redirect the links that you have specified in your email body.

> 🚧 Click Tracking
>
> If you set this tag, CleverTap will be unable to track clicks on your email message.

# Add Override Link Tracking

In this section, learn how to use a **Email with drag and drop** template to add override redirection of email links.

1. From the *What* section in the Email builder, click **Go to Editor**. The Email Editor tool displays.
2. Choose **Basic Templates**> **Email with drag and drop** template. 
3. Under the **Content** tab, drag the **HTML** icon to the desired location.
4. In the **Content Properties** section, add the above shared HTML code to override link tracking for specific email links effectively.
