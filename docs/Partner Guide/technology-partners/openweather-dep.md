---
title: OpenWeather - dep
excerpt: Contextual Location Partner
deprecated: true
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
(@Krishna: Move this under Contextual Location Partner. This doc should be placed just above PlotProjects - update the description under Contextual Location Partner doc.)

# Overview

[OpenWeather](https://openweathermap.org/) collects precise weather data globally, enabling businesses to integrate with [CleverTap](https://docs.clevertap.com/docs/linked-contenthttps://docs.clevertap.com/docs/linked-content) for targeted campaigns. CleverTap and OpenWeather integration allows you to fetch the user location and weather updates in real-time and send personalized campaigns to your users. For instance, retail companies can send localized notifications recommending weather-appropriate products such as umbrellas during rainy seasons and so on. This document is a comprehensive guide for integrating OpenWeather and CleverTap.

(@Krishna - intro for OpenWeather - should not highlight about integration - it should say what OPen Weather exactly does- data collection across the globe. You can take inspiration from the following pieces:

- Open Weather is a team of IT experts and data scientists that has been practising deep weather data science. For each point on the globe, OpenWeather provides historical, current and forecasted weather data via light-speed APIs.
- OpenWeather, Weather forecasts, nowcasts and history in a fast and elegant way

Krihsna - just fix the intro for Open Weather, rest I have fixed and retained your example as is)

# Prerequisites

You must have the following for this integration:

- An OpenWeather account 
- API key for OpenWeather. For getting the API, contact your Open Weather account manager.
- A CleverTap account 

> 📘 Note
> 
> Ensure that you are tracking user co-ordinates (latitude and longitude) as user attributes on CleverTap.

# Integrate CleverTap with OpenWeather

This process involves the following three major steps:

1. Set Up OpenWeather dashoboard.
2. Set Up CleverTap dashboard.

## Set Up OpenWeather Dashboard

Generate an API key from the OpenWeather dashboard to integrate with CleverTap:

1. Log in to your OpenWeather dahsboard. 
2. Select _My API Keys_ from the dropdown list from your account or you can also select the _API keys_ tab directly. 
3. Enter your _API key name_ under the _Create Key_ field and click **Generate**. OpenWeather also creates a default _API key_ when you log in to the dashbaord for the first time.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/995b8a0-OpenWeather_API_Generate.png",
        "",
        "OpenWeather Generate API"
      ],
      "align": "center",
      "border": true,
      "caption": "Generate OpenWeather API Key"
    }
  ]
}
[/block]


(@Krishna: In the above image, highlight the portion where you want to draw user's attention)

> 📘 API Documentation
> 
> For more information, refer to <https://openweathermap.org/api/one-call-3>

## Set Up CleverTap Dashboard

To set up CleverTap dashabord:

1. Go to _Settings_ > _Setup_ > _Linked Content_ and click **+ Linked Content**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1437fb1-OpenWeather_Clevertap_Linked_Content.png",
        "",
        "Linked Content Setup"
      ],
      "align": "center",
      "border": true,
      "caption": " Set Up Linked Content"
    }
  ]
}
[/block]


2. Enter the following details:

[block:parameters]
{
  "data": {
    "h-0": "Parameters",
    "h-1": "Description",
    "0-0": "API Name",
    "0-1": "Enter the name to uniquely identify your API.",
    "1-0": "Endpoint URL",
    "1-1": "Select **GET** from the dropdown list and use the Open Weather API endpoint URL that most suits your purpose. For our use case, we want to fetch current weather data for user's location, so enter the following endpoint URL: <https://api.openweathermap.org/data/2.5/weather?lat={{latitude}}&lon={{longitude}}&<appid=)&exclude={{part}}>  \n  \nFor more information about OpenWeather available APIs, refer to [Weather API](https://openweathermap.org/api).   \n  \n**Note**: You must update the API URL based on your OpenWeather subscription. We have subscribed to the version 2.5 for demonstration purposes.",
    "2-0": "Parameters",
    "2-1": "Declare the parameters to be fetched from the endpoint as follows:   \n  \n<li> latitude </li> <li> longitude </li> <li> part </li> from the OpenWeather dashboard. \nMark latitude and longitude as mandatory fields."
  },
  "cols": 2,
  "rows": 3,
  "align": [
    "left",
    "left"
  ]
}
[/block]


[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f23f0dd-Set_up_Linked_Content.png",
        "",
        "Linked Content Parameters"
      ],
      "align": "center",
      "border": true,
      "caption": "Linked Content Parameters"
    }
  ]
}
[/block]


(@Krishna: Update the screenshot to show all three parameters here and highlight them.)

2. Click **Test Linked Content** after you set up the parameters.  
   Add relevant values for the set parameters and click **Send Request**. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d83e67d-Linked_Content_enter_values_.png",
        "",
        "Enter Values for Request Parameters"
      ],
      "align": "center",
      "sizing": "70% ",
      "border": true,
      "caption": "Enter Values for Request Parameters"
    }
  ]
}
[/block]


4. Click **Auto-Fill Objects with Responses** after the response code is populated in the Response field and click **Test & save changes**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/19f08d0-auto-fill_objects_with_response.png",
        "",
        "Auto-Fill Objects with Response"
      ],
      "align": "center",
      "border": true,
      "caption": "Auto-Fill Objects with Response"
    }
  ]
}
[/block]


Here is an example of the response: 

```json JSON
{
  "coord": {
    "lon": -94.04,
    "lat": 33.33
  },
  "weather": [
    {
      "id": 803,
      "main": "Clouds",
      "description": "broken clouds",
      "icon": "04d"
    }
  ],
  "base": "stations",
  "main": {
    "temp": 305.36,
    "feels_like": 311.36,
    "temp_min": 303.15,
    "temp_max": 305.36,
    "pressure": 1014,
    "humidity": 62,
    "sea_level": 1014,
    "grnd_level": 1003
  },
  "visibility": 10000,
  "wind": {
    "speed": 1.54,
    "deg": 340
  },
  "clouds": {
    "all": 75
  },
  "dt": 1720188172,
  "sys": {
    "type": 1,
    "id": 6094,
    "country": "US",
    "sunrise": 1720177934,
    "sunset": 1720229345
  },
  "timezone": -18000,
  "id": 4736096,
  "name": "Texarkana",
  "cod": 200
}
```

# Create a Campaign on CleverTap

Once you set up the Linked Content on CleverTap, you can now run personalized campaigns from the CleverTap dashboard. In our case, the retail company wants to send personalized email campaign recommending weather-appropriate products such as umbrellas during rainy seasons and so on. To do so:

1. Go to _Campaigns_ and click **+ Campaigns**.
2. Select _Emails_ from the list of messaging channels. 
3. Click **Go To Editor** from the What section and select _Email with Rich Media_ template to create an email campaign. 
4. Click the ![](https://files.readme.io/c486f61-Personalization_icon.png) icon and select the _Linked Content_ tab. 
5. Slect the _API_ you configured while setting up the CleverTap dashboard.
6. Map the API Parameters to attributes in the users' profile and click **Apply**.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9d4a3c1-image_7.png",
        "",
        "Personalization Set up"
      ],
      "align": "center",
      "border": true,
      "caption": "Personalization Set up"
    }
  ]
}
[/block]


7. Create the campaign message using the Linked Content as shown in the following image: 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/22151a3-image_6.png",
        "",
        "Map Linked Content to create an Email"
      ],
      "align": "center",
      "border": true,
      "caption": "Create a Personalized Email Campaign Using Linked Content"
    }
  ]
}
[/block]


```json
{% if Linked.OpenWeather-Demo.weather[0].main == "Clouds"%}
  Hey! it looks cloudy, are you ready for the monsoons? Avail 50% off on all monsoon gear.
{% else %}
   Avail early bird discounts on all monsoon gear.
{% endif %}
```

8. Define all the campaign sections and click **Publish**. You can also sent test campaigns before publishing the campaigns to borader audience.