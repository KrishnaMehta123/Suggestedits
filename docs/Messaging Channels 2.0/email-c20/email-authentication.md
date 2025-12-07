---
title: Email Authentication_ WIP not be released with campaign 2.0
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
\<\< @PM: THE SECTIONS BELOW UNDER 'EMAIL AUTHENTICATION' WERE COPIED/PASTED FROM [https://docs.google.com/document/d/1LO9-QvAUs8\_Pzt-7G-2wDjo0726ScrU3aNPNsruYJdo/edit](https://docs.google.com/document/d/1LO9-QvAUs8_Pzt-7G-2wDjo0726ScrU3aNPNsruYJdo/edit) CAN EVERYTHING BE SHOWN AS IS? IF SO, DOCS WILL EDIT IT TO ADHERE TO OUR STYLE GUIDE LATER. >>

# Email Authentication

Authentication is the process of attempting to verify the digital identity of the sender of a communication. There are three main types of email authentication: SPF, DKIM, and DMARC (optional).

## SPF Record (Setup by SendGrid)

SPF stands for Sender Policy Framework. SPF is an email authentication method that identifies the mail servers approved to send emails from a specific domain. ISPs use this validation protocol to determine when spammers and phishers are trying to impersonate your brand to send malicious emails from your domain.\
While inbox providers generally don't block email solely based on a missing SPF record, it's one more data point that contributes to your positive sender reputation. Also, it helps protect your brand.

### How to check for the SPF records

1. Log in to your CleverTap account and create a campaign in the Email channel.
2. Send a test mail to your email id.
3. Log in to your email account and navigate to the test email received in your inbox.
4. Open the header content for that particular email. (Follow the steps particular to your mailbox providers such as Google, Yahoo or Hotmail or even the email client you are using such as IBM Lotus Notes or Outlook)
5. Search for the keyword *SPF* in that text, and if you find *spf=pass*, this signifies that the SPF records are correctly in place.

## DKIM Email Signature (Setup by SendGrid)

DomainKeys Identified Mail (DKIM) allows you to publish a key that ISPs use to verify that the email message didn't change in transit, and the sender can take ownership of the content. DKIM defends against malicious modification of messages in transit, and it carries a lot of reputation weight with inbox providers. Messages not signed with a DKIM signature aren't likely to see the inbox.

### How to check for the DKIM records

Log in to your CleverTap account and create a campaign in the Email channel.\
Send a test mail to your email id.\
Log in to your email account and navigate to the test email received in your inbox.\
Open the header content for that particular email. (Follow the steps specific to your mailbox providers such as Google, Yahoo or Hotmail or even the email client you are using such as IBM Lotus Notes or Outlook)\
Search for the keyword *DKIM* in that text, and if you find *dkim=pass*, this signifies that the SPF records are properly in place.

## DMARC Record Publishing (This will be required to be set up at your end)

A Domain-based Message Authentication, Reporting & Conformance (DMARC) record is a protocol that uses SPF and DKIM to determine the authenticity of an email. The protocol allows you to specify how you want ISPs to handle emails that were not authenticated using SPF or DKIM. You can decide to send those emails straight to the junk folder or have them blocked altogether.

## BIMI (This will be required to be set up at your end)

BIMI is an acronym of Brand Indicators for Message Identification. It is an open standard created jointly by several big players in the email market, such as Google and Verizon Media/Yahoo.\
BIMI provides the MBP with a consistent and reliable way of retrieving the correct logo for every email. Brands benefit from BIMI due to the fact that email recipients see the familiar brand logo immediately. Recognizing a logo is much faster than reading and creates a different and additional level of trust. After all; "a picture is worth a thousand words." Open rates of emails should increase after BIMI is implemented. Additionally, due to the way how BIMI is designed, it helps to prevent fraudulent emails.\
BIMI is an open standard, so anyone can implement and use it. BIMI builds upon the well-established standards of SPF, DKIM, and DMARC. Provided these are already in place, BIMI is just a small step away.

These are the main, minimal steps required:\
Implement DMARC as it is required for BIMI.\
DMARC policy has to be set to "reject" or "quarantine."\
Create your logo as a square SVG file without any text.\
Publish your logo on an accessible web-source.\
Create a DNS TXT record for your emails' "From:" address. Something like: default.\_bimi.yourbrand.com IN TXT "v=BIMI1; l=[https://subdomain.yourbrand.com/image/logo.svg](https://subdomain.yourbrand.com/image/logo.svg); a=;"\
OR\
With a Verified Mark Certificate:\
default.\_bimi.yourbrand.com IN TXT "v=BIMI1; l=[https://subdomain.yourbrand.com/image/logo.svg](https://subdomain.yourbrand.com/image/logo.svg); a=cert;[https://subdomain.brand.com/vmc/logo.pem;"](https://subdomain.brand.com/vmc/logo.pem;")
