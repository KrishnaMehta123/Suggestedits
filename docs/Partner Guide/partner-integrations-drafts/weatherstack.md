---
title: WeatherStack
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

[WeatherStack](https://weatherstack.com/) provides real-time and historical weather data through a powerful API that includes temperature, humidity, air quality, UV index, sunrise/sunset, and detailed weather descriptions for any location worldwide.

With the CleverTap and Weatherstack integration, you can enhance your marketing campaigns with dynamic weather insights and deliver personalized, context-aware messages to your users. For example:

* Promote indoor products when thunderstorms are reported in the user’s area.
* Offer cooling products or beverages during hot weather.
* Recommend air purifiers or masks when pollution levels are high.

# Prerequisites for Integration

Before setting up the integration, ensure the following:

* You have a **Weatherstack account** and access to your [API Key](https://weatherstack.com/dashboard).
* You have access to the [Weatherstack API documentation](https://weatherstack.com/documentation).
* You have an active CleverTap account with Linked Content enabled.

# Integrating Weatherstack with CleverTap

The integration process involves three main steps:

1. [Get Weatherstack API Key](#get-weatherstack-api-key)
2. [Configure Linked Content API](#configure-linked-content-api)
3. [Create Personalized Campaign](#create-personalized-campaign)

## Get Weatherstack API Key

Before configuring CleverTap, you need to retrieve your Weatherstack API Key, which is required to authenticate all requests to the API. Follow these steps to locate it:

1. Log in to your [Weatherstack Dashboard](https://weatherstack.com/dashboard).
2. Copy your **API Key** listed in the account overview.

<Image alt="Weatherstack API Key" align="center" width="65% " border={true} src="https://files.readme.io/5ed115ab68c0d72440b8df3e4bc8e4e4366af5630b5b1a489e68ff7dcf70f674-image.png">
  Weatherstack API Key
</Image>

### Supported Location Inputs

The Weatherstack API allows for flexible ways to specify a user’s location. These options can be used in the query string of your API call:

| **Method**        | **Example**              | **Description**                                   |
| ----------------- | ------------------------ | ------------------------------------------------- |
| **Location Name** | `query=New York`         | Standard format using a city name.                |
| **ZIP Code**      | `query=99501`            | Works for the US, Canada, and UK.                 |
| **Coordinates**   | `query=40.7831,-73.9712` | Use latitude and longitude to specify a location. |
| **IP Address**    | `query=153.65.8.20`      | Detect location from a specific IP address.       |
| **Auto-Fetch IP** | `query=fetch:ip`         | Automatically detect requester IP and location.   |

## Configure Linked Content API

Set up Linked Content in CleverTap to dynamically fetch live weather data from Weatherstack. To do so, perform the following steps:

1. Go to *Settings* > *Setup* > *Linked Content* from the CleverTap dashboard.
2. Click **+ Linked Content** and enter the following:

| **Field**        | **Value**                                                                                                                                                                    |
| ---------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**         | Provide a name for the Linked Content. For example: `Weatherstack_Current_Weather`                                                                                           |
| **Request Type** | Select `GET` method.                                                                                                                                                         |
| **Endpoint URL** | Enter the following endpoint URL: `http://api.weatherstack.com/current?access_key=<YOUR_API_KEY>&query={{city}}` Replace `<YOUR_API_KEY>` with your actual Weatherstack key. |

> 📘 Note
>
> The `{{city}}` parameter dynamically pulls the user’s city from their CleverTap profile. See [Supported Location Inputs](#supported-location-inputs) for alternate location formats.

<Image alt="Linked Content Setup" align="center" width="65% " border={true} src="https://files.readme.io/17a21e60a9a0dd89732f981a365e7b8c9c2857ca44673c5dda5b7d0cb227fbb8-image.png">
  Linked Content Setup
</Image>

3. Click **Test Linked Content** to verify the connection. A successful response will look similar to the following sample:

```json
{
  "request": {
    "query": "Thanesar, India"
  },
  "location": {
    "name": "Thanesar",
    "country": "India",
    "region": "Haryana"
  },
  "current": {
    "temperature": 28,
    "weather_descriptions": ["Thundery outbreaks in nearby"],
    "weather_icons": [
      "https://cdn.worldweatheronline.com/images/wsymbols01_png_64/wsymbol_0016_thundery_showers.png"
    ]
  }
}
```

4. Click **Auto-Fill Objects with Response** to automatically map the JSON keys.

<Image alt="Auto-Fill Objects with Response" align="center" width="55% " border={true} src="https://files.readme.io/10c305982396d65187fa3d5b33a92095417e03635c2fd482f624c20bc6457cfa-image.png">
  Auto-Fill Objects with Response
</Image>

5. Click **Test and Save** to complete your Linked Content configuration.

<Image alt="Test and Save" align="center" width="35% " border={true} src="https://files.readme.io/3402fb23a998b25fd1aaee63d16c5ea1f0f39e0ecd8d0095bb5f33980d5a6302-image.png">
  Test and Save
</Image>

## Create Personalized Campaign

Once Linked Content is configured, you can use Weatherstack data to create personalized campaigns in CleverTap. You can personalize campaigns based on real-time weather data in a Push Notification campaign or any other campaign type that supports Linked Content. To do so, perform the following steps:

1. Go to the *Campaigns* page, click **+ Campaign**, and select *Push Notification* from the list of messaging channels.
2. Click **Go to Editor** under the *What* section.

   1. Click **Personalization** in the top-right corner.
   2. Select the Linked Content configured in [Configure Linked Content API](doc:weatherstack#configure-linked-content-api).
   3. Map the `{{city}}` parameter to the user's city attribute.

<Image alt="Personalization Setup" align="center" width="65% " border={true} src="https://files.readme.io/8c9c63a41b446c215d0a95474a3e8a26ce0e220b0049454eae7e6547e3e8d46d-image.png">
  Personalization Setup
</Image>

3. Use [Liquid tags](doc:personalize-message-all#liquid-tags) to personalize your message dynamically. For example:

```liquid
{% if Linked.weatherstack.temperature < 10 %}
❄️ **Brr... It's freezing outside!**  
Stay cozy with our **Winter Collection** and get **30% OFF** using code **COZY30**.  
🧥 Shop warm jackets & sweaters now
{% elsif Linked.weatherstack.temperature >= 10 and Linked.weatherstack.temperature < 18 %}
🧣 **Chilly weather alert!**  
Layer up in style with our **Sweaters & Hoodies** – **25% OFF** with code **WARM25**.  
👕 Shop here
{% elsif Linked.weatherstack.temperature >= 18 and Linked.weatherstack.temperature < 25 %}
🌤️ **Perfect weather for casuals!**  
Check out our **Lightweight Tees & Denim** – **20% OFF** with code **COOL20**.  
👖 Browse now
{% elsif Linked.weatherstack.temperature >= 25 and Linked.weatherstack.temperature < 32 %}
☀️ **Sunny vibes are here!**  
Beat the heat with our **Summer Essentials** – **15% OFF** with code **SUNNY15**.  
🩳 Shop shorts, cotton tees & more
{% else %}
🔥 **Scorching hot!**  
Stay cool with our **Breezy Linen Collection** – **10% OFF** with code **BREEZE10**.  
🌴 Shop now
{% endif %}
```

<Image alt="Example Personalized Message" align="center" width="65% " border={true} src="https://files.readme.io/ff1a9833e42a4a98a538421aae57d6c77976902e18c8802fde1da0735716259e-image.png">
  Example Personalized Message
</Image>

4. Click **Preview and Publish** to test and launch your campaign.

Users will now receive weather-personalized push notifications based on real-time data from Weatherstack and their current location.

<Image alt="Push Notification Preview" align="center" width="25% " border={true} src="https://files.readme.io/d70c6055172c608922b1483bfaa1b21598c2e90b48e49094e2bc3ab2e9326e78-image.png">
  Push Notification Preview
</Image>

By combining Weatherstack’s live weather intelligence with CleverTap’s personalization engine, you can create truly contextual campaigns that engage users in the moment and drive measurable business results.
