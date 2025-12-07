---
title: Personalize Campaigns with Linked Content URL and Body Personalization
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

You can dynamically generate URLs with parameters based on user preferences or profile data. For instance, if you're using an API to fetch weather information for a specific city, instead of setting up separate Linked Content endpoint URLs for every location, you can configure a single, flexible endpoint by personalizing parts of the URL. In this case, the endpoint URL will be as follows:

```
https://api.example.com/weather-management?location-name={{locname}}&location-weather={{locweather}}
```

In this example, the values of location-name and location-weather are dynamically inserted based on each user’s data.

<Image alt="Example for Linked Content URL Personalization" align="center" border={true} src="https://files.readme.io/7dab31c-Example_for_Linked_Content_URL_Personalization.png">
  Example for Linked Content URL Personalization
</Image>

# Parameters

The endpoint URL consists of the following parameters:

## Path Parameters

These parameters help specify variable parts of the URL path, allowing APIs to target specific resources or actions dynamically based on the values provided within the URL path itself. Path parameter, when present in the endpoint URL, becomes a mandatory parameter. 

You can include the path parameter as shown in the following image:

<Image alt="Path Parameter Example" align="center" border={true} src="https://files.readme.io/1c6e77f-Example_for_Path_Parameters.png">
  Path Parameter Example
</Image>

## Query Parameters

Query parameters are key-value pairs appended to the end of a URL that provides additional information to an API endpoint. They are used to modify the behavior or content returned by the server. Query parameters are separated from the base URL by a question mark (?), and multiple parameters are separated by an ampersand (&). 

If we refer to the following image, the query parameters will be: `articletopic` and `user`.

<Image alt="Query Parameters Example" align="center" border={true} src="https://files.readme.io/70cddc9-image.png">
  Query Parameters Example
</Image>

While the previous example shows personalization in values only, you can also personalize keys in the query parameters. This means both the parameter names and their values can be dynamic. For example, a user is accessing a movie recommendation API, and the API allows for personalized queries based on the user's preferences and location. In this case, the endpoint URL can be: 

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

So, the keys and values change based on user input or data stored in a user profile, allowing the API to deliver personalized recommendations tailored to the individual's genre preference and location.

<Image alt="Personalize Both Keys and Values in Query Parameters" align="center" border={true} src="https://files.readme.io/2fab433-Personalize_Both_Keys_and_Values_in_Query_Parameters.png">
  Personalize Both Keys and Values in Query Parameters
</Image>

<br />

# Linked Content in Body Personalization

In addition to URLs, Linked Content can now be used to dynamically personalize the body of your message content across multiple channels. 

### Supported Channels

Currently, body personalization for Linked Content is available for the following channels:

* Push
* Email
* Web Push
* Webhook
* Native Display

> 📘 Note
>
> * Event personalization returns default value in case of inaction campaigns with delay of more than a day.
> * The following personalization inputs are supported when used inside the Linked Content body:
>   * Profile Properties
>   * Identity
>   * Campaign ID
>   * Event Personalization
>   * External Trigger Properties
>   * Send Test Personalization (in Push)
