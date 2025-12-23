---
title: Linked Content URL and Request Body Personalization
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
# Linked Content URL Personalization

You can dynamically generate URLs with parameters based on user preferences or profile data. For instance, if you are using an API to fetch weather information for a specific city, instead of setting up separate Linked Content endpoint URLs for every location, you can configure a single, flexible endpoint by personalizing parts of the URL. In this case, the endpoint URL will be as follows:

```
https://api.example.com/weather-management?location-name={{locname}}&location-weather={{locweather}}
```

In this example, the values of location-name and location-weather are dynamically inserted based on each user’s data.

<Image align="center" alt="Example for Linked Content URL Personalization" border={true} caption="Example for Linked Content URL Personalization" src="https://files.readme.io/7dab31c-Example_for_Linked_Content_URL_Personalization.png" />

The endpoint URL consists of the following parameters:

### Path Parameters

These parameters help specify variable parts of the URL path, allowing APIs to target specific resources or actions dynamically based on the values provided within the URL path itself. Path parameter, when present in the endpoint URL, becomes a mandatory parameter.

You can include the path parameter as shown in the following image:

<Image align="center" alt="Path Parameter Example" border={true} caption="Path Parameter Example" src="https://files.readme.io/1c6e77f-Example_for_Path_Parameters.png" />

### Query Parameters

Query parameters are key-value pairs appended to the end of a URL that provide additional information to an API endpoint. They are used to modify the behavior or content returned by the server. Query parameters are separated from the base URL by a question mark (?), and multiple parameters are separated by an ampersand (&). 

If we refer to the following image, the query parameters will be: `articletopic` and `user`.

<Image align="center" alt="Query Parameters Example" border={true} caption="Query Parameters Example" src="https://files.readme.io/70cddc9-image.png" />

While the previous example shows personalization in values only, you can also personalize keys in the query parameters. This means both the parameter names and their values can be dynamic. For example, a user accesses a movie recommendation API that allows for personalized queries based on the user's preferences and location. In this case, the endpoint URL can be:

```
<https://movie-recommendation-api.com/recommendations?{{genrename}}={{genre}}&{{location}}={{place}}>
```

Here:

* `genrename` and `place` are dynamic keys.
* `genre` and `location` are dynamic values from the user profile.

This allows for a fully personalized query structure driven by user profile data. So, one user might send:

```
https://movie-recommendation-api.com/recommendations?favGenre=Comedy&region=California
```

While another user might send:

```
https://movie-recommendation-api.com/recommendations?preferredGenre=Action&area=Texas
```

The keys and values change based on user input or data stored in a user profile, allowing the API to deliver personalized recommendations tailored to the individual's genre preferences and location.

<Image align="center" alt="Personalize Both Keys and Values in Query Parameters" border={true} caption="Personalize Both Keys and Values in Query Parameters" src="https://files.readme.io/2fab433-Personalize_Both_Keys_and_Values_in_Query_Parameters.png" />

# Linked Content Request Body Personalization

In addition to personalizing URLs, Linked Content also supports dynamic personalization of the request body. This is especially useful for POST APIs that require user-specific details, such as identity, eligibility, or category, to be sent as part of the payload.

Currently, body personalization for Linked Content is available for the following channels: Push, Email, Web Push, Webhook, and Native Display.

### Example

Consider an OTT platform wants to fetch personalized content recommendations based on:

* The user’s region and language (passed in the URL), and
* The user’s subscription plan and viewing preferences (passed in the request body).

**Linked Content Endpoint URL**

```
[https://movie-recommendation-api.com/recommendations?\{\{genrename}}=\{\{genre}}&\{\{location}}=\{\{place}}](https://movie-recommendation-api.com/recommendations?\{\{genrename}}=\{\{genre}}&\{\{location}}=\{\{place}})
```

**Request Body with Linked Content Placeholders**

```json
{
  "userId": "{{identity}}",
  "subscriptionPlan": "{{Profile.plan_type}}",
  "preferredGenre": "{{Profile.favorite_genre}}"
}
```

When the request is sent, Linked Content automatically replaces these placeholders with real user data. The OTT recommendation service then uses this personalized payload to return content that is relevant to each viewer.

<Callout icon="📘" theme="info">
  #### Note

  * Event personalization returns default value in case of inaction campaigns with delay of more than a day.
  * The following personalization inputs are supported when used inside the Linked Content body:
    * Profile Properties
    * Identity
    * Campaign ID
    * Event Personalization
    * External Trigger Properties
    * Send Test Personalization (in Push)
</Callout>
