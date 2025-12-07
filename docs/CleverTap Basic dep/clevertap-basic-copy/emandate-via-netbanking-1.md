---
title: eMandate via NetBanking
excerpt: >-
  Understand how eMandate via NetBanking complies with new RBI guidelines
  established for recurring payments. This is a new payment method introduced
  for our Indian customers paying in INR.
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

eMandate, a payment service initiated by RBI and the National Payments Corporation of India (NPCI) in October 2021, provides infrastructure for businesses to collect recurring payments in India. It allows you to schedule automatic transfers from your bank account for recurring payments. CleverTap has introduced this payment method to provide flexibility to our customers paying in INR. 

# eMandate via NetBanking Registration

You can choose eMandate via Netbanking as the preferred payment method when creating a *CleverTap Basic* or *Essentials* account or update it later.

You need to register for eMandate by entering the following details:

* Account Number 
* IFSC code
* Account Holder Name
* Account Type

<Image alt="eMandate via NetBanking Registration" align="center" width="70% " border={true} src="https://files.readme.io/9fd44e8-image.png">
  eMandate via NetBanking Registration
</Image>

The setup requires one-time authorization via NetBanking for enabling future transactions. The authentication can take up to 1-2 banking days, depending upon the respective bank. After the *eMandate via NetBanking* payment method is authorized, you will receive a confirmation email about the same. The subsequent payments do not require any customer intervention. 

It is recommended to inform your customer about the deduction of ₹1 or ₹2 during the authorization. This amount will be refunded to your customer in 5-7 banking days.

If there is an issue in registering the eMandate via NetBanking payment method, you must update your payment details on the CleverTap dashboard to avoid loss of access.

The following table lists the Turn Around Time (TAT) for authorization of different banks:

| Bank Name                    | Turn Around Time for Authorization |
| :--------------------------- | :--------------------------------- |
| All Banks via NPCI           | Real-time                          |
| ICICI and Axis               | Real-time                          |
| HDFC and State Bank of India | T + 1 working days                 |

After registering successfully, CleverTap automatically debits the billing amount from your registered account. The payment processing can take up to 1-2 banking days. However, the payment processing time varies from bank to bank. The following table provides information about the TAT for different banks:

| Bank Name           | Turn Around Time for Payment Processing |
| :------------------ | :-------------------------------------- |
| ICICI               | Real-time                               |
| Axis                | Same day                                |
| HDFC                | Same day                                |
| State Bank of India | T + 1 working days                      |
| Other Banks         | Same day                                |

# Registration Failure

If the eMandate via NetBanking registration fails, try again by visiting the dashboard or choosing a different payment method such as a Credit/Debit Card.

# Payment Failure in eMandate via NetBanking

If the payment fails, CleverTap notifies you immediately. To resolve the payment failure, you need to re-enter the account details. You can also change your payment method to a Credit/Debit Card.
