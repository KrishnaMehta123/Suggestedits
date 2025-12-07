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
You can choose eMandate via Netbanking as the preferred payment method when creating a *CleverTap Basic* account or update it later.

You need to register for eMandate by entering the following details:
* Account Number 
* IFSC code
* Account Holder Name
* Account Type
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ce52215-Multiple_Payment_Methods.png",
        "Multiple Payment Methods.png",
        808,
        1534,
        "#f2f4fa"
      ],
      "border": true,
      "sizing": "80"
    }
  ]
}
[/block]
The setup requires one-time authorization via NetBanking for enabling future transactions. The authentication can take up to 1-2 banking days, depending upon the respective bank. After the *eMandate via NetBanking* payment method is authorized, you will receive a confirmation email about the same. The subsequent payments do not require any customer intervention. 

It is recommended to inform your customer about the deduction of ₹1 or ₹2 during the authorization. This amount will be refunded to your customer in 5-7 banking days.

If there is an issue in registering the eMandate via NetBanking payment method, you must update your payment details on the CleverTap dashboard to avoid loss of access.

The following table lists the Turn Around Time (TAT) for authorization of different banks:
[block:parameters]
{
  "data": {
    "h-0": "Bank Name",
    "h-1": "Turn Around Time for Authorization",
    "0-0": "All Banks via NPCI",
    "0-1": "Real-time",
    "1-0": "ICICI and Axis",
    "1-1": "Real-time",
    "2-0": "HDFC and State Bank of India",
    "2-1": "T + 1 working days"
  },
  "cols": 2,
  "rows": 3
}
[/block]
After registering successfully, CleverTap automatically debits the billing amount from your registered account. The payment processing can take up to 1-2 banking days. However, the payment processing time varies from bank to bank. The following table provides information about the TAT for different banks:
[block:parameters]
{
  "data": {
    "h-0": "Bank Name",
    "h-1": "Turn Around Time for Payment Processing",
    "0-0": "ICICI",
    "1-0": "Axis",
    "2-0": "HDFC",
    "3-0": "State Bank of India",
    "4-0": "Other Banks",
    "4-1": "Same day",
    "0-1": "Real-time",
    "1-1": "Same day",
    "2-1": "Same day",
    "3-1": "T + 1 working days"
  },
  "cols": 2,
  "rows": 5
}
[/block]
# Registration Failure
If the eMandate via NetBanking registration fails, try again by visiting the dashboard or choosing a different payment method such as a Credit/Debit Card.

# Payment Failure in eMandate via NetBanking
If the payment fails, CleverTap notifies you immediately. To resolve the payment failure, you need to re-enter the account details. You can also change your payment method to a Credit/Debit Card.