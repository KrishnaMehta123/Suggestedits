---
title: Create Campaigns using Recommendations
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
[block:api-header]
{
  "title": "Overview"
}
[/block]
After the recommendations have been published, you can use them in your engagement workflow by creating personalized and contextual recommendations for your users.

#Access Recommendations Within a Campaign
During the campaign creation in the *What* section, access recommendations with the following steps:

1. Type the @ symbol to personalize your message. 
2. Click **+ Create** under *Recommendation Content*.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/167b2a9-recommendations_personalization.png",
        "recommendations_@personalization.png",
        879,
        683,
        "#f7f8fa"
      ],
      "border": true
    }
  ]
}
[/block]
#Create Recommendation Content

Consider a food delivery app. You can create recommendation content for users based on their last viewed product. We will understand different steps and available options based on the use cases. 

To create recommendation content, perform the following steps:


1. Click the *Personalization* ![Personalization](https://files.readme.io/5d34d91-recommendations_personalization_icon.png) icon in the message.
2. Select a recommendation from a list of *Recommendations* that have already been published.
3. Select the event that you want to trigger for the recommendation. For our example, we select "Product Viewed". For a particular user, we know the following: 
a. The last cuisine of the Product viewed by the user - *Burger*
b. The last user location - *Bayside*
c. The last restaurant whose product was viewed - *McDonald's* 
[block:callout]
{
  "type": "info",
  "title": "Event Selection",
  "body": "You can only select events that are mapped to the catalog. For more information, see [create a new catalog](https://docs.clevertap.com/docs/catalog#create-a-new-catalog)."
}
[/block]
4.  (Optional) You can now filter recommendations by event, by catalog, or by location. 
 You can filter out the products based on different cases using the recommendation filters and offer hyper-personalized recommendations for each user. Let's say for our test users, the recommendations without any filter would be as follows: 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/87bd0eb-recommendations_all_restaurants.png",
        "recommendations_all_restaurants.png",
        932,
        260,
        "#ebeceb"
      ],
      "caption": ""
    }
  ]
}
[/block]
a. Filter by event

  i. Click **+ Filter by event**. 
  ii. Select whether you want to *include* or *exclude* recommended items based on the selected event properties. For example, if you would want to upsell from the same restaurant, you can use this filter to keep only the items from the recommendation list for the selected event property. For example, the condition can be -  *include* recommendations where the event property called *Restaurant ID* of the event *Product Viewed* matches the *Restaurant ID* of the recommended items. In this case, all recommendation items will now only have items from McDonald's.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2e0890e-recommendations_only_McDonalds.png",
        "recommendations_only_McDonalds.png",
        941,
        99,
        "#e8ebe9"
      ]
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "body": "You can add up to five event filters.",
  "title": "Add up to Five Event Filters"
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "How the Filter by Event Works?",
  "body": "The filter by event takes precedence over recommended items and selected events matching. It provides the capability to include and exclude all recommended items when a column value of an item in the product catalog matches a defined event property."
}
[/block]
b. Filter by Catalog
 i. Click **+ Filter by Catalog**.
 ii. Select whether you want to include or exclude recommended items based on selected catalog column values. To include items whose rating is greater than 4, keep items from the recommendation list that have the catalog column value *Rating* greater than 5. Rating is a column that was already present in the catalog.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/563f7ae-recommendations_MD_rating_4above.png",
        "recommendations_MD_rating_4above.png",
        942,
        76,
        "#e6eae8"
      ],
      "caption": ""
    }
  ]
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "Add up to Five Catalog Columns",
  "body": "You can add a total of five catalog filters for a single recommendation."
}
[/block]

[block:callout]
{
  "type": "info",
  "title": "How the Filter by Catalog Works?",
  "body": "You can choose to filter out recommended items, based on Catalog Column values. \nFor example, exclude items that have a promotion running on them, by saying catalog column value \"hasPromo\" is equal to \"true\". Here the Catalog has the column \"hasPromo\", which signifies if a promotion is running on the listed item."
}
[/block]
c. Filter by Location
  
i. Click **+ Filter by Location**. 
ii. Select a product location catalog and a radius. The location can be within a 1 - 100 KM/Mile radius from the user's last known location. These are the recommendations that are displayed to the user.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/448b89e-recommendations_MD_location_within_100.png",
        "recommendations_MD_location_within_100.png",
        940,
        61,
        "#e6ebe8"
      ]
    }
  ]
}
[/block]
When the campaign is sent out, the fields will be replaced and the message will contain the personalized fields for each product. The resulting recommendations will be hyper-personalized to suit the user's preferences. 
  
[block:callout]
{
  "type": "info",
  "title": "How the Filter by Location Works?",
  "body": "The filter by location takes precedence over the location of the recommended items that are fetched from the location catalog. Items in a defined range are looked up with the associated product location catalog and matched with the user's last known location to be included in the filter."
}
[/block]
5. Decide the sequence of items to be served up to the user out of the list of items that can be recommended For example, serve up the first item from the list of recommended items.
6. Click **Apply**.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/093d80b-recommendations_campaign_dashboard.png",
        "recommendations_campaign_dashboard.png",
        930,
        765,
        "#f7f8fa"
      ],
      "border": true
    }
  ]
}
[/block]