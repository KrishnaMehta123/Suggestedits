---
title: FAQs
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
## Overview

This section covers FAQs related to the SMS messaging channel.

# FAQs

## How do we unsubscribe a user from receiving SMS promotions?

The [Subscribe API](https://developer.clevertap.com/docs/subscribe-api) provides the ability to set a phone number as subscribed or unsubscribed. This is important so that you do not send an SMS to a phone number accidentally unless they have explicitly opted for it. 

## What is a *Profile not reachable* error?

The error Profile not reachable occurs whenever the qualified device is not reachable via the selected communication channel.

For SMS, the scenario is that the profile does not have a phone number.

## What is a *Duplicate Profile for the channel* error?

This error indicates two different profiles have the same phone number. The engagement is sent for one profile and an error is raised for the second profile.

## Why do some emojis and characters not display in my SMS body?

Check that your service provider supports sending special characters/emojis in an SMS.
