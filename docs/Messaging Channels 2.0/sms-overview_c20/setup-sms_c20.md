---
title: Setup
excerpt: ''
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: >-
    Refer to the pages listed below to learn more about the following SMS
    sections:
  pages:
    - type: link
      title: Create Message
      url: https://docs.clevertap.com/docs/create-message-sms_c20
    - type: link
      title: Personalize Message
      url: https://docs.clevertap.com/docs/personalize-message-sms_c20
    - type: link
      title: SMS Regulations
      url: https://docs.clevertap.com/docs/sms-regulations_c20
    - type: link
      title: Regulation Impact
      url: https://docs.clevertap.com/docs/regulation-impact_c20
    - type: link
      title: FAQs
      url: https://docs.clevertap.com/docs/sms-faqs_c20
---
# Add a New Provider

To add a new SMS provider, perform the following steps:

1. From the dashboard, navigate to *Settings* > *Channels* > *SMS*.
2. Click **+ Add Provider**.

<Image title="1 Add Provider dashbboard.png" alt={1074} className="border" border={true} src="https://files.readme.io/ea1f1a5-1_Add_Provider_dashbboard.png" />

3. Enter all the required information.
4. Click **Save**. 

Once the phone number is validated by the SMS service provider, you can send a test SMS to test the integration before you start creating SMS campaigns and journeys.

<Image title="SMS provider.png" alt={1070} className="border" border={true} src="https://files.readme.io/9617fec-SMS_provider.png" />

To learn more about integrating specific SMS service providers with CleverTap, refer to this [document](https://docs.clevertap.com/docs/sms-partners). 

# Edit Provider Details

To edit a *Provider*, perform the following steps:

1. Click the ellipsis next to the required provider from the *Providers* tab. 
2. Click **Edit settings** to update the provider details. 

You can also mark a provider as default by selecting *Mark as Default* option available in the ellipsis next to a particular provider.

# Add a Provider Group

The failure of an SMS provider may affect your SMS campaigns, so it is always better to have another SMS provider. By grouping providers, you can provide your users with a seamless experience.

You can assign a preferred provider to send a message. A provider group is used based on its assigned priority for each message. If provider 1 is unavailable, then we attempt the message with provider 2, and so on. In the end, this ensures higher message deliverability for your campaigns.

> 📘 Provider Group Maximum
>
> Each provider group can have a maximum of 10 providers.

To create a provider group, perform the following steps:

1. From the dashboard, navigate to *Settings* > *SMS* > *Provider Groups* tab. 
2. Click **+ Add Provider Group**.

<Image title="3 Provider Group dashboard.png" alt={1064} className="border" border={true} src="https://files.readme.io/a9f0479-3_Provider_Group_dashboard.png" />

2. Enter a group name.
3. Select the providers by priority.
4. Click **Save Provider Group**.

<Image title="SMS_provider_group_create.png" alt={576} className="border" border={true} src="https://files.readme.io/663186b-SMS_provider_group_create.png" />

## Edit a Provider Group

To edit a provider group, perform the following steps:

1. Click the ellipsis next to the required provider from the *Provider Groups* tab. 
2. Click **Edit settings** to add or remove providers or change the priority for any providers. 

You can also mark a provider group as default by selecting the *Mark as Default* option available in the ellipsis next to a particular provider group.

<Image title="4 Edit Provider Group.png" alt={1062} className="border" border={true} src="https://files.readme.io/72b25cf-4_Edit_Provider_Group.png" />
