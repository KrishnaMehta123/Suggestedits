---
title: Email Sender Authentication
excerpt: >-
  Understand why Еmail sender authentication is mandatory and learn about the
  different email authentication protocols - SPF, DKIM, and DMARC
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

**Еmail sender authentication** is how you prove to inbox providers that CleverTap is authorised to send emails on your behalf. Having proper sender authentication is mandatory for the successful deliverability of your emails in all inbox providers (Gmail; Yahoo; MSN; etc). It helps distinguish between legitimate senders, such as those sending transaction updates or promotional offers, and potential spammers or scammers attempting to flood users' inboxes with unsolicited or malicious emails. Inbox providers utilise email authentication protocols to achieve verified sender identity when emails arrive at their receiving mail servers. 

To set up sender authentication, you must incorporate a set of Domain Name System (DNS) records into your domain’s hosting service. A DNS translates or resolves a hostname (e.g. [www.clevertap.com](www.clevertap.com)) into a language of numbers that a computer can understand (e.g. an IP address). These DNS records associate your sending domain with CleverTap. Consequently, when an inbox provider processes your email, they refer to your domain instead of CleverTap's ESP (Sendgrid).

# Authentication Record Protocols

Email authenticators such as SPF, DKIM, and DMARC are essential protocols to verify email authenticity and prevent spoofing and phishing attacks. SPF specifies the IP addresses authorised to send emails on behalf of a domain; DKIM adds digital signatures to emails to verify their integrity, and DMARC provides policies for handling emails that fail SPF and DKIM checks, thus enhancing email security.

## Sender Policy Framework (SPF)

SPF is an open standard to prevent sender address forgery. It validates that the IP address used to send an email is authorised to send messages on behalf of the domain listed in the email's Envelope From or Return-path. Without SPF or similar authentication records, a malicious actor can readily assume a sender's identity, deceiving the recipient into engaging in actions or disclosing information they would otherwise refrain from.

*In the postal mail analogy, you would contact the sender to verify if the postman can be trusted to deliver their letter.*

**MOVE SPF IMAGE HERE**

## DomainKeys Identified Mail (DKIM)

DKIM is a validation method designed to help Internet Service Providers (ISP’s) detect and prevent malicious email delivery.

DKIM uses public-key cryptography to sign email message headers - optionally, the message body may also be signed. This signature allows receiving email servers to determine whether a message was sent by a domain owner and whether the message was altered in transit.

*In the postal mail analogy, this means that the envelope has a stamped seal that proves that the letter inside was not altered by anyone who could have had access to the envelope, and the stamp can be verified to be from the sender on the envelope (not the sender mentioned in the letter, this is a big difference).*

**MOVE DKIM IMAGE HERE**

## Domain-based Message Authentication, Reporting, and Conformance (DMARC)

 DMARC is an additional layer atop SPF and DKIM. It validates SPF and DKIM outcomes and verifies if the Header From domain aligns with those used in the SPF and DKIM checks. The *Header From* address represents the sender's email address and is visible to recipients in their email clients.

When SPF and DKIM validations fail or are incongruent with the *Header From* address, the recipient server must adhere to the DMARC policy. This can involve actions such as quarantining (p=quarantine), rejecting (p=reject), or disregarding the results and delivering the email (p=none). 

Visualise your email server as a vigilant individual managing your incoming messages. Without SPF, DKIM, and DMARC implementation, this individual accepts envelopes from any source, opens them, and places the content on your desk without verification. Consequently, discerning the trustworthiness of the sender's identity becomes challenging.

*For an analogy, let’s say you are working at a government office and require two ID proofs for someone to receive a document. If someone brings only one proof, or if someone’s ID fails in some way (such as the addresses on the IDs not matching), you would halt the process and either ask for additional information or refuse to hand over the document.*

For more details on DMARC, refer to [DMARC Resources ](https://dmarc.org/resources/) or [Google's Help Center](https://support.google.com/a/answer/2466563?hl=en\&ref_topic=2759254).

> 👍 Compliance
>
> * As of February 2024, Gmail and  Yahoo have enforced new sending requirements, which require email marketing senders with volumes greater than 5,000 a day to have a valid SPF, DKIM, and DMARC record.
> * For CleverTap clients with Advanced Email (an email sending service integrated with CleverTap) SPF, DKIM and as of recently DMARC have been configured at the time of Еmail onboarding with CleverTap.
