---
title: Popular Recemmendations
excerpt: >-
  Learn how to set up and manage Popular Recommendations in CleverTap to
  showcase top-performing products or content automatically.
deprecated: false
hidden: false
metadata:
  robots: index
---
# Overview

The Popular Recommendations feature allows marketers and product teams to deliver relevant, high-performing product suggestions to end-users. This guide explains how to configure, manage, and use the Popular Recommendations setup within the CleverTap platform.

Popular Recommendations are automatically generated based on real user engagement data such as views, purchases, or other tracked interactions over a configurable time window.

## Advantages

* Accelerated time to market, prebuilt out-of-the-box (OOB) recommendation types make setup fast.
* Consistency and accuracy, shared guardrails, and uniform recommendation logic ensure predictable results.
* Scalability, recommendations are cached, low latency, and suitable for high-traffic campaigns.

## Supported Use Cases

Popular Recommendations are best suited for the following verticals:

* E-commerce, show trending or best-selling items in a category.
* OTT and Media, display most-watched or recently popular content.

# Prerequisites

Before setting up Popular Recommendations, ensure the following:

* You have the necessary access permissions for Recommendations Setup.
* A product catalog is configured and synced with relevant item attributes.
* Event tracking is set up for key user interactions such as product views, add-to-cart, purchases, or video watches.
* Your account has OOB recommendation types enabled.

# Setting Up a Popular Recommendation

Follow these steps to create and configure a Popular Recommendation setup for your account.  

1. Select the Recommendation Type
2. Configure Setup Parameters
3. Publish and Monitor Status

## Select the Recommendation Type

From the Recommendations Setup dashboard:

1. Click Create New Setup.
2. Choose Type: Popular from the available OOB recommendation types.

Each account can have multiple active Popular setups.

## Configure Setup Parameters

| Parameter       | Description                                                                                                              | Editable | Extended at Invocation |
| --------------- | ------------------------------------------------------------------------------------------------------------------------ | -------- | ---------------------- |
| Catalog         | Choose one or more product catalogs. Recommendations will be generated only from these catalogs.                         | No       | No                     |
| Time Duration   | Specify the time window (for example, 7 days or 30 days) to evaluate item popularity.                                    | Yes      | No                     |
| Interactions    | Select which user events count toward popularity (for example, product viewed, added to cart, purchased).                | Yes      | No                     |
| Scope           | Define how items are grouped (for example, by Category or Brand).                                                        | Yes      | Yes                    |
| Segment         | Restrict recommendations to a specific audience segment, if needed.                                                      | Yes      | No                     |
| Guardrails      | Rules that exclude or include certain catalog items when generating recommendations (for example, exclude out-of-stock). | Yes      | No                     |
| Rules           | Rules that apply when serving recommendations (for example, exclude blacklisted products).                               | Yes      | Yes                    |
| Fallback Rules  | Define default or backup items to display if generated results are fewer than requested.                                 | Yes      | Yes                    |
| Count           | Number of items to recommend.                                                                                            | Yes      | Yes                    |
| Product Details | Choose which product attributes appear in the recommendation response.                                                   | Yes      | Yes                    |

## Publish and Monitor Status

Once the setup is saved and published:

* The internal Recommendation Generator runs according to the defined frequency, such as daily, weekly, or monthly.
* Status values indicate generation progress:

  * Processing, setup is running.
  * Ready to Serve, recommendations successfully generated.
  * Error, generation failed.
  * Ready to Serve (Partial), generated fewer items than expected.

# Using the Popular Recommendations API

Once configured, you can invoke Popular Recommendations through a unified API endpoint.

### Endpoint

```bash
GET /getRecommendations
```

### Parameters

| Parameter | Type    | Description                                               |
| --------- | ------- | --------------------------------------------------------- |
| reco_type | string  | Recommendation type such as popular_by_category.          |
| category  | string  | Category name or ID, mandatory for category-based setups. |
| count     | integer | Number of items requested.                                |
| cursor    | string  | Used for pagination.                                      |
| rules     | object  | Optional serving rules, such as exclude blacklisted=true. |

### Example Request

```bash
GET /getRecommendations?reco_type=popular_by_category&category=Shoes&count=10
```

### Example Response

```json
{
  "status": "success",
  "items": [
    {
      "id": "12345",
      "name": "AirZoom Running Shoes",
      "price": 89.99,
      "image_url": "https://example.com/item12345.jpg"
    }
  ]
}
```

### Error Codes

| Error Code               | Description                                           |
| ------------------------ | ----------------------------------------------------- |
| UNKNOWN_RECO_TYPE        | Invalid or disabled recommendation type.              |
| MISSING_MANDATORY_FILTER | Required parameter missing, such as category.         |
| INVALID_FILTER           | Provided filter value is invalid.                     |
| CURSOR_INVALIDATED       | Pagination request invalidated due to dataset change. |
| NO_CONTENT               | No items found for given parameters.                  |

# Personalization

If personalization is enabled, you can pass the CleverTap user identity with the API request. The system applies user-specific context, for example preferences or exclusions, and tailors recommendations by attributes such as gender, language, or size.

# Troubleshooting

| Issue                        | Possible Cause                         | Solution                                          |
| ---------------------------- | -------------------------------------- | ------------------------------------------------- |
| No results returned          | Missing or incorrect filters           | Verify category, scope, or event mapping          |
| Recommendations not updating | Generator not scheduled or setup error | Re-publish setup, check generator logs            |
| API latency                  | High traffic or cache miss             | Retry after interval, contact support if persists |

# FAQs

### How are Popular Recommendations different from Trending Recommendations

Popular rankings are based on cumulative interactions within a set window, while Trending weighs recent velocity and changes in engagement.

### Can I override default recommendation rules?

Yes, overwrites and extensions are allowed for rules, fallback rules, and counts at invocation.

### What happens if there are fewer recommendations than requested?

The system fills missing items using fallback rules or default items.
