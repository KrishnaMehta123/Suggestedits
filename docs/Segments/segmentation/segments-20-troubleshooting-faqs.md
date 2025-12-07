---
title: 'Segments 2.0: Troubleshooting & FAQs'
excerpt: This page covers the FAQs for Segments 2.0.
deprecated: true
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
(@Meenal: As discussed, let's move this to under the FAQ section of <https://docs.clevertap.com/docs/troubleshooting-faqs-push-notifications> document.)

### Why do I see an increase in the number of errors after migrating to the enhanced segment builder?

After migrating to the enhanced segment builder, you may notice an increase in errors. This is due to a fundamental change in how user properties are evaluated.

Previously, filters in the _Who_ section were evaluated during campaign user qualification. With the enhanced Segment Builder, this evaluation now happens during campaign dispatch. Here is how it works:

Consider an example where a campaign is triggered on user action and includes filters such as region = India or gender = M. 

- **During the qualification phase**, all user profiles performing the specified event qualify for the campaign, regardless of the user property. 
- **During the dispatching phase**: 
  - Profiles without tokens are marked as unreachable, as their User Properties cannot be evaluated.
  - Profiles with tokens are evaluated:
    - Those matching the filters (for example, Region = India and Gender = M) receive the campaign notification.
    - Those not matching the filters are silently dropped from the campaign.

While silently dropped profiles are excluded from the campaign, they can still be identified using the [Find People/Segments](https://staging.docs.user.clevertap.net/docs/find-people) page from the CleverTap dashboard. For more information on user profile properties and events, refer to [User Profiles ](doc:user-profiles)and [Events](doc:events).