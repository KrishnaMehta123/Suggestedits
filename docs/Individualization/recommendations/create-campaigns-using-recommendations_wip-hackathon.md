---
title: Create Campaigns using Recommendations_WIP hackathon
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

After the recommendations have been published, you can use them in your engagement workflow by creating personalized and contextual recommendations for your users.

# Access Recommendations Within a Campaign

During the campaign creation in the *What* section, access recommendations with the following steps:

1. To personalize your message, type the @ symbol or click the @ symbol in any input field that has personalization available. 
2. Click **Recommendations**.

<Image title="recommendations_@personalization.png" alt={879} className="border" border={true} src="https://files.readme.io/167b2a9-recommendations_personalization.png" />

# Create Recommendation Content

Consider a food delivery app. You can create recommendation content for users based on their last viewed product. We will understand different steps and available options based on the use cases. 

To create recommendation content, perform the following steps:

1. Click the *Personalization* ![Personalization](https://files.readme.io/5d34d91-recommendations_personalization_icon.png) icon in the message.
2. Select one out of five recommendations from a list of *Recommendations* that have already been published.
3. Select the event that you want to trigger for the recommendation. 

For our example, we select "Product Viewed." For a particular user, we know the following:\
a. The last cuisine of the Product viewed by the user - *Burger*\
b. The last user location - *Bayside*\
c. The last restaurant whose product was viewed - *McDonald's* 

> 📘 Event Selection
>
> You can only select events that are mapped to the catalog. For more information, refer to [Create a new Catalog](https://docs.clevertap.com/docs/catalog#create-a-new-catalog).

4. (Optional) Filter recommendations by event, catalog, or location.

You can filter out the products based on different cases using the recommendation filters and offer hyper-personalized recommendations for each user. For example, for our test users, the recommendations without any filter would be as follows: 

![932](https://files.readme.io/87bd0eb-recommendations_all_restaurants.png "recommendations_all_restaurants.png")

a. Filter by event.

  i. Click **+ Filter by event**.\
  ii. Select whether you want to include or exclude recommended items based on the selected event properties. 

For example, if you want to upsell from the same restaurant, you can use this filter to keep only the items from the recommendation list for the selected event property. 

For example, the condition can be -  *include* recommendations where the event property called *Restaurant ID* of the event *Product Viewed* matches the *Restaurant ID* of the recommended items. In this case, all recommendation items will now only have items from McDonald's.

![941](https://files.readme.io/2e0890e-recommendations_only_McDonalds.png "recommendations_only_McDonalds.png")

> 📘 Add up to Five Event Filters
>
> You can add up to five event filters.

> 📘 How the Filter by Event Works
>
> The filter by event takes precedence over recommended items and selected events matching. It provides the capability to include and exclude all recommended items when a column value of an item in the product catalog matches a defined event property.

b. Filter by catalog.\
 i. Click **+ Filter by Catalog**.\
 ii. Select whether you want to include or exclude recommended items based on selected catalog column values. To include items whose rating is greater than 4, keep items from the recommendation list that have the catalog column value *Rating* greater than 5. Rating is a column that was already present in the catalog.

![942](https://files.readme.io/563f7ae-recommendations_MD_rating_4above.png "recommendations_MD_rating_4above.png")

> 📘 Add up to Five Catalog Columns
>
> You can add a total of five catalog filters for a single recommendation.

> 📘 How the Filter by Catalog Works
>
> You can choose to filter out recommended items, based on catalog column values.\
> For example, exclude items that have a promotion running on them, by saying catalog column value "hasPromo" is equal to "true." Here, the catalog has the column "hasPromo" which signifies if a promotion is running on the listed item.

c. Filter by location.

  i. Click **+ Filter by location**.\
  ii. Select a product location catalog and a radius. The location can be within a 1-100 KM/mile radius from the user's last known location. These are the recommendations that are displayed to the user.

![940](https://files.readme.io/448b89e-recommendations_MD_location_within_100.png "recommendations_MD_location_within_100.png")

When the campaign is sent out, the fields will be replaced and the message will contain the personalized fields for each product. The resulting recommendations will be hyper-personalized to suit the user's preferences.

> 📘 How the Filter by Location Works
>
> The filter by location takes precedence over the location of the recommended items that are fetched from the location catalog. Items in a defined range are looked up with the associated product location catalog and matched with the user's last known location to be included in the filter.

5. Decide the sequence of items to be served up to the user out of the list of items that can be recommended. For example, serve up the first item from the list of recommended items.
6. Click **Apply**.

<Image title="recommendations_campaign_dashboard.png" alt={930} className="border" border={true} src="https://files.readme.io/093d80b-recommendations_campaign_dashboard.png" />

# Choose the Fields to Personalize your Message

Now that you have created a recommendation, use the following steps to finalize your content:

1. Choose the particular fields from the catalog that you want to use in your personalized message.
2. Enter your content in the title and message.

When the campaign is sent out, the fields will be replaced and the message will contain the personalized fields for each product. 

> 👍 Video Example
>
> You can send out a recommended video to the user with the video name and thumbnail image based on the last videos a user has watched.

<Image title="recommendations_@personalization.png" alt={879} className="border" border={true} src="https://files.readme.io/167b2a9-recommendations_personalization.png" />

3. Send a test campaign to yourself to see the look and feel of the campaign. The test message will show the first item in the recommendation list.
4. Once you are done testing, publish the campaign.

<Image title="Screenshot 2019-03-01 at 5.28.45 PM.png" alt={328} className="border" border={true} src="https://files.readme.io/4d118f5-Screenshot_2019-03-01_at_5.28.45_PM.png" />

## Email Campaigns with Recommendations

You can create email campaigns with recommended content by invoking recommendations within the email messages. Beyond this part, all the steps are the same as the generic ones described in the sections above. 

You can create emails using:

* New email with rich media
* Templates

But first, you must load your recommendations. 

1. Click **Personalization**.

<Image title="Email with templates.png" alt={1433} className="border" border={true} src="https://files.readme.io/ad9ec52-Email_with_templates.png" />

2. Select *Recommendations*, then click **+ Recommendation**.

![1427](https://files.readme.io/1d7bd8f-1_Add_recommendations.png "1 Add recommendations.png")

3. Select a recommender.

![937](https://files.readme.io/5c28937-2_Select_recommender.png "2 Select recommender.png")

4. Select an event and the filters for your recommendations.

![927](https://files.readme.io/a40527d-3_Select_event_and_filter.png "3 Select event and filter.png")

5. Click **Apply**.

![932](https://files.readme.io/24e8465-4_Click_Apply.png "4 Click Apply.png")

## Recommendations using a New Email with Rich Media

You can create personalized recommendations using a new email with media with the steps below.

### Link with Recommendations

You can add recommendations within links with the following steps:

1. Click on the link icon to add a link to your email message.

<Image title="Link icon.png" alt={1425} className="border" border={true} src="https://files.readme.io/c7701bf-Link_icon.png" />

2. Type the @ symbol or click on the @ symbol to personalize the link using recommendations in the display text and the URL fields.\
   \<Sunil: need help to figure out this step/screenshot. Couldn't figure out where to find this screen in the new UI.>

<Image title="Link pop-up.png" alt={690} className="border" border={true} src="https://files.readme.io/c4eb166-Link_pop-up.png" />

### Image with Recommendations

You can also add recommendations within images with the following steps:

1. Click on the image icon to add an image to your email message.

<Image title="Image icon.png" alt={1424} className="border" border={true} src="https://files.readme.io/c3ec5d4-Image_icon.png" />

2. Type the @ symbol or click on the @ symbol to personalize the link using recommendations in the URL. Click **Recommendations** and select an event.

<Image title="Recommendations for images.png" alt={1425} className="border" border={true} src="https://files.readme.io/c3482ad-Recommendations_for_images.png" />

The remainder of the steps is the same as any other campaigns as explained in the sections above.

## Recommendations in Template Emails

You can create personalized recommendations using template emails with the steps below.

### Links, Images, Deeplinks, and Custom HTML with Recommendations

You can add recommendations within links, images, deeplinks, and custom HTML with the following steps:

1. Drag and drop the *Dynamic Content* block into the content box in the center of the email body.

<Image title="1 Drag and drop.png" alt={1419} className="border" border={true} src="https://files.readme.io/7224658-1_Drag_and_drop.png" />

2. Click on the new content box to display the menu on the right.
3. Click on the **Add options** button to access the dynamic content options. 

<Image title="2 Drag and drop - content box.png" alt={1419} className="border" border={true} src="https://files.readme.io/b862a72-2_Drag_and_drop_-_content_box.png" />

4. When the window pop-up displays, select one of the following options:

* Image
* Deeplink
* Text
* Custom HTML

> 📘 Option Name Required
>
> When you create a dynamic block, the option name is mandatory. Also, these dynamic blocks can be re-used if required.

#### Image with Recommendations

Type the @ symbol or click on the @ symbol to personalize the image content using recommendations in the URL, alternative text, and target URL fields.

<Image title="3 Drag and drop - image.png" alt={879} className="border" border={true} src="https://files.readme.io/8ac24fd-3_Drag_and_drop_-_image.png" />

#### Deeplink with Recommendations

Type the @ symbol or click on the @ symbol to personalize the deeplink content using recommendations in the display text and URL fields.

<Image title="4 Drag and drop - deeplink.png" alt={855} className="border" border={true} src="https://files.readme.io/c99ab69-4_Drag_and_drop_-_deeplink.png" />

#### Text with Recommendations

Type the @ symbol or click on the @ symbol to personalize the text content using recommendations in the text field.

<Image title="5 Drag and drop - text.png" alt={850} className="border" border={true} src="https://files.readme.io/8423040-5_Drag_and_drop_-_text.png" />

#### Custom HTML with recommendations

Type the @ symbol or click on the @ symbol to personalize the custom HTML content using recommendations in the custom HTML code box.

![849](https://files.readme.io/8ccea3d-6_Drag_and_drop_-_custom_HTML.png "6 Drag and drop - custom HTML.png")

### Existing Text Content Type in the Template Containing Deeplinks with Recommendations

You can access recommendations within the existing text content type with the following steps:

1. Drag and drop the *Text* block into the content box in the center of the email body.

<Image title="1 Drag and drop.png" alt={1419} className="border" border={true} src="https://files.readme.io/2d30676-1_Drag_and_drop.png" />

2. Click on the content box to display the menu.
3. Click **More** > **Personalized Deeplink**.

<Image title="2 Drag and drop - Text.png" alt={1425} className="border" border={true} src="https://files.readme.io/56c523d-2_Drag_and_drop_-_Text.png" />

3. Type the @ symbol or click on the @ symbol to personalize the deeplink content using recommendations in the display text and URL fields.

<Image title="3 Drag and drop - Text.png" alt={1408} className="border" border={true} src="https://files.readme.io/3b9c6ee-3_Drag_and_drop_-_Text.png" />
