---
title: Data Setup and Management
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
Integrating the CleverTap SDK with your mobile app or website is the first step to understanding and retaining users while igniting growth.

The Basic plan is a self-serve model where we provide support for integration via the following: 

- [Support Tickets](https://bit.ly/c4sticket): You can raise support tickets, and the support team will revert over the email. You must upgrade to an enterprise plan if you need a specialized onboarding manager.
- [Documentation](https://docs.clevertap.com/docs): A product documentation entailing CleverTap overview for users, platform features & core concepts & developer documentation covering SDK, API & Dev resources to help you get started.
- [Integration Videos](https://eu1.dashboard.clevertap.com/R74-ZWR-R44Z/integration-videos): This can be accessed from the ‘Need Help?’ section to help you tackle integration issues.
- [Integration Checklist](https://eu1.dashboard.clevertap.com/R74-ZWR-R44Z/main): It is available on your CleverTap dashboard to guide you through onboarding and setup. 

> 📘 Integration Time
> 
> The integration time depends on the speed and skills of your software developer. It also depends on the number of metrics you want to track and the mar-tech stack of your business. We have customers who have integrated CleverTap in a week. It’s recommended that you begin with tracking only the most essential metrics for your business.

# Data Setup

[Data Setup](https://docs.clevertap.com/docs/onboarding-setup-data-management) starts with defining the structure for your data, i.e. Schema. Once that is defined and all the required SDKs are integrated, the data flows into the CleveTap dashboard. 

## Schema

 [Schema](https://docs.clevertap.com/docs/schema) is a framework to maintain your data, organize, and structure it. It enforces rules to maintain data integrity so that you can avoid data quality issues later. The schema table stores event and user properties in a pre-defined order to preserve data sanity. 

## User Profile

A CleverTap user profile has a set of default fields, such as email, phone number, and language. You can also extend the default user profile by adding custom fields specific to your business.

A CleverTap user profile consists of three parts:

- **Identifiers**: Each user profile is given a unique CleverTap ID. You can also add other identifiers to recognize the user, including email, phone number, Facebook ID, or your custom identifier. To learn more about how identity works on the CleverTap dashboard, refer to [User Profiles](https://developer.clevertap.com/docs/concepts-user-profiles) documentation.
- **Properties**: These are the user profile properties such as age, gender, device, and location. You can also extend the default user profile by adding custom fields specific to your business.
- **Events**: This is a log of actions a user takes in your app, such as a product viewed, a video watched, or an item added to the cart.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ddc5eb1-image.png",
        "User Properties",
        "User Properties"
      ],
      "align": "center",
      "border": true,
      "caption": "User Properties"
    }
  ]
}
[/block]

### User Profile Types

​​The CleverTap [user profile type](https://docs.clevertap.com/docs/user-profiles#user-profile-types) changes automatically depending on the information set in them. A user profile can only belong to one type: 

- Anonymous/Guest
- Addressable
- Customer

### Update User Profile

 You can [update user profile](https://docs.clevertap.com/docs/user-profiles#updating-a-user-profile) properties via CSV, API, and SFTP Import. Refer to the corresponding documentation below:

- [Uploading User Profiles via API](https://developer.clevertap.com/docs/upload-user-profiles-api)
- [Importing data via SFTP](https://developer.clevertap.com/docs/imports-via-sftp)
- [CSV Upload](https://docs.clevertap.com/docs/csv-upload)

## Events

Events track what individual actions users perform in your app or website. Some examples of events include a user launching an app, viewing a product, listening to a song, sharing a photo, making a purchase, or favoriting an item.

An event could be of four types (click on the titles to understand how these events are tracked in CleverTap):

- [Custom events](https://developer.clevertap.com/docs/events#custom-events): Custom events are events that you can define, edit, remove, and so on. These are your app events that you can fully control.
- [System events](https://developer.clevertap.com/docs/events#system-events): System events are tracked automatically. Some events tracked automatically are app install, the app launched, notification sent, notification viewed, etc.
- [Conversion events](https://docs.clevertap.com/docs/schema#section-conversion-event): These are the events that help you track conversion.
- [Qualifying events](https://docs.clevertap.com/docs/schema#qualifying-event): These are the events that help you track conversion.

# Data Management

You can refer to the following as part of CleverTap for Startups data management:

## Data Retention Policy

The default data retention policy for the CleverTap for Startups plan is one year, which cannot be changed. CleverTap deletes all backups within 60 days of the customer deleting the data. 

The data of CleverTap for Startups customers are stored in the EU region. Currently, there is no provision to store the data in other regions. If you want the data hosted in your country, opt for the Enterprise plans.

If you are keen to change the region of the server/data center based on your preferences, we suggest you opt for the CleverTap Enterprise plan. 

This data can be exported using the Export option or an API. Learn more about exporting data [here](https://docs.clevertap.com/docs/export).

## Privacy

Protecting customer data is always a priority at CleverTap, so we maintain globally-recognised data handling standards, best practices, and adherence to data transfer regulations. Independent, third-party auditors assess compliance. CleverTap complies with GDPR, CCPA, SOC 2 Type II, ISO 27001, and HIPAA. You can read more about how we handle data privacy [here](https://clevertap.com/security).