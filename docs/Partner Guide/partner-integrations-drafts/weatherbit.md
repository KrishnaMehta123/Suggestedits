---
title: Weatherbit
excerpt: Contextual Location Partner
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

[Weatherbit](https://www.weatherbit.io/) provides real-time and historical weather data through a robust suite of APIs. The Weatherbit Current Weather API offers detailed insights such as temperature, humidity, precipitation, wind speed, air quality, and more for any city or geographic location worldwide.

With the CleverTap and Weatherbit integration, you can enhance your marketing campaigns with live weather insights to deliver personalized, context-aware messages. For example:

* Trigger campaigns based on current weather conditions (such as, rain, sunshine, or humidity levels).
* Offer weather-appropriate promotions such as rainwear discounts on rainy days or sunscreen offers on sunny days.
* Engage users more effectively by tailoring your messaging to their local environmental context.

# Prerequisites for Integration

Before setting up the integration, ensure the following prerequisites are met:

* You have a **Weatherbit account** and an active [API Key](https://www.weatherbit.io/account/dashboard).
* You have an active CleverTap account with Linked Content enabled.

# Integrating Weatherbit with CleverTap

The integration process involves three main steps:

1. [Get Weatherbit API Key](doc:weatherbit#get-weatherbit-api-key)
2. [Configure Linked Content API](doc:weatherbit#configure-linked-content-api)
3. [Create Personalized Campaign](doc:weatherbit#create-personalized-campaign)

## Get Weatherbit API Key

To complete the integration process, you need your Weatherbit API Key. Follow these steps to locate it:

1. Log in to your [Weatherbit Dashboard](https://www.weatherbit.io/account/dashboard).
2. Copy your **API Key** located under your account details. This key will be used to authenticate your Linked Content setup.

<Image alt="Weatherbit API Key" align="center" width="65% " border={true} src="https://files.readme.io/a4b1d30a45ad434e12c1b98a601a4dfcecabf410a8723d8f4870a87fd3e0f3fd-image.png">
  Weatherbit API Key
</Image>

## Configure Linked Content API

Set up Linked Content in CleverTap to dynamically fetch live weather data from Weatherbit. To do so, perform the following steps:

1. Go to *Settings* > *Setup* > *Linked Content* from the CleverTap dashboard.
2. Click **+ Linked Content** and enter the following:

| Field            | Value                                                                                                                                                              |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Name**         | Provide a name for the Linked Content. For example: `Weatherbit_Current_Weather`                                                                                   |
| **Request Type** | Select `GET` method.                                                                                                                                               |
| **Endpoint URL** | Enter the following endpoint URL: `https://api.weatherbit.io/v2.0/current?city={{city}}&key=<YOUR_API_KEY>` Replace `<YOUR_API_KEY>` with your Weatherbit API key. |

> 📘 Note
>
> The parameter `{{city}}` dynamically pulls the user's city from their CleverTap profile.

<Image alt="Linked Content Setup" align="center" width="65% " border={true} src="https://files.readme.io/77b49285455e1eb8443247cf8f790fa7d031785082467ead79485d4633bfc846-image.png">
  Linked Content Setup
</Image>

3. Click **Test Linked Content** to verify the connection. A successful response will look similar to the following sample:

```json
{
  "count": 1,
  "data": [
    {
      "city_name": "Maradi",
      "temp": 25.9,
      "humidity": 85,
      "precip": 0,
      "wind_spd": 2.5,
      "weather": {
        "description": "Clear sky",
        "icon": "c01d"
      }
    }
  ]
}
```

4. Click **Auto-Fill Objects with Response** to automatically map the JSON keys within CleverTap.
5. Click **Test and Save** to complete your Linked Content configuration.

<Image alt="Test and Save" align="center" width="35% " border={true} src="https://files.readme.io/3402fb23a998b25fd1aaee63d16c5ea1f0f39e0ecd8d0095bb5f33980d5a6302-image.png">
  Test and Save
</Image>

## Create Personalized Campaign

Once your Weatherbit Linked Content is configured in CleverTap, you can personalize campaigns based on real-time weather data in a Push Notification campaign or any other campaign type that supports Linked Content. To do so, perform the following steps:

1. Go to the *Campaigns* page, click **+ Campaign**, and select *Push Notification* from the list of messaging channels.
2. Click **Go to Editor** under the *What* section.

   1. Click **Personalization** in the top-right corner.
   2. Select the Linked Content configured in [Configure Linked Content API](doc:weatherbit#configure-linked-content-api).
   3. Map the `{{city}}` parameter to the user's city attribute.

<Image alt="Personalization Setup" align="center" width="65% " border={true} src="https://files.readme.io/8e6ced808f40691bd2e8529a3fa4566de3e99d064a6a91eefef7b096d7f16611-image.png">
  Personalization Setup
</Image>

3. Use [Liquid tags](doc:personalize-message-all#liquid-tags) to personalize your message dynamically. For example:

```liquid
{% if Linked["Weatherbit_Current_Weather"].json.data[0].weather.description == "Drizzle" %}
☔ Stay prepared for the rain!  
Enjoy **20% off** on all **rain essentials** today.  
Use code: **RAIN20**
{% elsif Linked["Weatherbit_Current_Weather"].json.data[0].weather.description == "Sunny" %}
☀️ Perfect day to step out in style!  
Get **15% off** on our **summer wear collection**.  
Use code: **STYLE15**
{% else %}
🌤️ Enjoy shopping with us today!  
Discover our latest arrivals!
{% endif %}
```

<Image alt="Example Personalized Message" align="center" border={true} src="https://files.readme.io/99694a5b9b703cb5d0a0b6180699b38094b785f6701a3a756b386a8668843aba-image.png">
  Example Personalized Message
</Image>

4. Click **Preview and Publish** to test and launch your campaign.

<Image alt="Push Notification Preview" align="center" width="25% " border={true} src="https://files.readme.io/c610bb7d2693f11d9c6bf8bb09a3b19fa414d09f21124ce37adaec47db4fc023-image.png">
  Push Notification Preview
</Image>

By combining Weatherbit’s real-time weather insights with CleverTap’s personalization capabilities, you can deliver timely, contextually relevant campaigns that boost engagement, improve customer experience, and increase conversions.
