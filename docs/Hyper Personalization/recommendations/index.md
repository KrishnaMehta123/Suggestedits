---
title: Recommendations
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
# Overview

The recommendations feature helps marketers engage and retain their customer base as it provides the capability to create personalized content for each user based on their unique historical data.

Using recommendations in campaigns and journeys will boost overall engagement throughout the user’s lifecycle across multiple channels such as in-apps, batch campaigns, or push notifications. Powered by a scalable architecture, this feature can cater to the millions of users you are trying to reach.

# How it Works

The following demonstrates how recommendations work:

* Once a catalog is uploaded into CleverTap, after 24 hours, the relationships among catalog items are used to form the basis of generating recommendations for a particular event. The catalog can also pick items to serve up recommendations.

* Then, you can create a recommendation by defining certain rules that indicate which catalog you want to use, the catalog value, the event on the basis of which the recommendation is to be generated, the lookback window, and any specific filtering criteria.

* While building a campaign or journey, use recommendations to personalize each interaction with each one of your users to create a delightful experience.

* Once the recommendation is built into a campaign or journey, your users will receive personalized recommendations based on their past history of interaction with other products.

* **Triggered Campaigns**  
  In the case of triggered campaigns, if the user performs the event defined for the last action under recommendations in the last 60 days and also performs the qualifying event, they will receive the campaigns.

  **Example**  
  Consider the example where the Charged event is the event defined for the last action under recommendations, and Added to cart is the qualifying event.

  * **Scenario 1: Receive the Campaign**  
    If the user performs the Charged event on the same day at 6 p.m., they will receive the campaign as soon as they perform the Added to cart event next.
  * **Scenario 2: Did not Receive the Campaign**  
    If the user has not performed the Charged event in the last 60 days and performs the Added to cart event on a certain date at 4 p.m., they will not receive the campaign.

* **PBS Campaigns**  
  In the case of PBS campaigns, if the user performs the qualifying event and has also performed the event defined for the last action performed under recommendations in the last 60 days, they will receive the campaign.

  **Example**  
  Consider the example where the Charged event is the event defined for the last action under recommendations, and the Product Viewed in the last 30 days is the segment definition. If 100 users qualify for the segment definition and only 80 users have performed the Charged event in the last 60 days, only 80 users will receive the campaign along with recommendations.

* CleverTap sends recommendations based on the last three user actions; thereby ensuring accurate and relevant suggestions. **(@Abhinav: Now that we are saying that the recommendations consider last three actions - will that impact the above two bullets as well?)**

* CleverTap allows you to automatically update your recommendations at set intervals, which can be adjusted based on your business needs. To customize this setting, contact your Customer Success Manager. The recommendations will be automatically refreshed in the following situations:

  * **Scenario 1**: If you have set the auto-refresh for recommendations to 7 days, and the time difference between the current date and the last refresh is 7 days or more, the recommendations will be refreshed. For example, if today is February 29, 2024, and the last refresh was on February 22, 2024 (a 7-day difference), the recommendations will update automatically.
  * **Scenario 2**: If the auto-refresh is set to 7 days, recommendations will be refreshed when the following two conditions are met: (i) the time difference between the current date and the last refresh is half the auto-refresh duration (7 days), and (ii) the last refresh happened before the catalog was last updated. For instance, if today is February 29, 2024, the last refresh was on February 22, 2024, and the catalog was last updated on February 26, both conditions are met, and the recommendations will be auto-refreshed.

# Examples

Below are some examples showing how recommendations can be used:

* John receives relevant and timely recommendations to purchase soccer merchandise as he recently added a pair of soccer shoes to his shopping cart. His list of recommendations would be based on what other people interested in purchasing soccer shoes have been doing around this time of the year.
* Jane has just watched _Game of Thrones_. Next, she receives an instant, in-app recommendation that suggests she watch similar English drama series and other titles that are often viewed by viewers who also watch _Game of Thrones_. These recommendations are also sensitive to recent trends and patterns.

# Recommendation Errors and Troubleshooting

If CleverTap cannot generate valid recommendations, the campaign is not sent. This prevents incorrect recommendations from reaching users.

Common reasons for recommendation errors include the following:

* Insufficient interaction data
* Recommender not refreshed after a catalogue update
* Over-restrictive filters during campaign creation
* User has not performed the selected last action in the past 60 days
* Item from the user’s last action is missing from the catalogue or has no associations

To avoid errors, target users who have performed the required action in the past 60 days and ensure catalogues and recommenders are kept in sync.

# Best Practices

The following best practices help ensure accurate recommendations and a successful campaign delivery:

* Map the correct event property to the Identity column
* Use separate catalogues for different recommendation use cases
* Validate interaction data before launching campaigns
* Refresh recommenders when the catalogue structure or item count changes
* Use recommender filters sparingly and prefer campaign-level filters for dynamic attributes
