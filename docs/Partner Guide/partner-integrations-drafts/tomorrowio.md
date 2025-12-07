---
title: Tomorrow.io
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

[Tomorrow.io](https://www.tomorrow.io/) offers hyper-local, real-time weather data via a robust API. It provides detailed metrics such as temperature, humidity, precipitation intensity, wind speed, UV index, and more for any location across the globe.

With the CleverTap and Tomorrow\.io integration, you can power real-time personalization by delivering messaging based on live weather conditions, tailored to each user’s geographic context. For example:

* Send winter product promotions when temperatures drop.
* Recommend sunscreen or summer wear on hot, sunny days.
* Promote rain gear or umbrellas when rain is forecasted.

# Prerequisites for Integration

Before setting up the integration, ensure the following:

* You have a **Tomorrow\.io account**.
* You have your **Tomorrow\.io API Key** (available in the [Tomorrow.io dashboard](https://app.tomorrow.io/)).
* You have access to the [Tomorrow.io Realtime Weather API documentation](https://docs.tomorrow.io/).
* You have an active CleverTap account with Linked Content enabled.

# Integrating Tomorrow\.io with CleverTap

The integration process involves three main steps:

1. [Get Tomorrow.io API Key](#get-tomorrowio-api-key)
2. [Configure Linked Content API](#configure-linked-content-api)
3. [Create Personalized Campaign](#create-personalized-campaign)

# Get Tomorrow\.io API Key

Before you begin configuration, retrieve your Tomorrow\.io API Key. This will be used to authenticate your API requests in CleverTap. Follow these steps to locate it:

1. Log in to your [Tomorrow.io Dashboard](https://app.tomorrow.io/).
2. On the *Home* page, locate your *Your API Key*.
3. Copy *Your API Key*, it will be needed to configure Linked Content in CleverTap.

<Image alt="Tomorrow.io API Key" align="center" width="65% " border={true} src="https://files.readme.io/f618a6a9df03580611b2376d4051b127bdffc7fb9fc9ebb7660caf61776e6c32-image.png">
  Tomorrow\.io API Key
</Image>

### Supported Location Inputs

Tomorrow\.io supports various input formats for specifying user location in API calls:

| **Input Type**           | **Example**                 | **Description**                                        |
| ------------------------ | --------------------------- | ------------------------------------------------------ |
| **City Name**            | `location=new york`         | Standard city name format.                             |
| **Latitude & Longitude** | `location=42.3478,-71.0466` | Decimal degree coordinates for precise targeting.      |
| **US ZIP Code**          | `location=10001 US`         | ZIP code with 2-letter country code based on ISO-3166. |
| **UK Postcode**          | `location=SW1`              | UK postal code support.                                |

> 📘 Note
>
> When using `{{city}}` in the Linked Content URL, CleverTap dynamically inserts the user’s city attribute from their profile.

## Configure Linked Content API

Set up Linked Content in CleverTap to dynamically fetch live weather data from Tomorrow\.io. To do so, perform the following steps:

1. Go to *Settings* > *Setup* > *Linked Content* from the CleverTap dashboard.
2. Click **+ Linked Content** and enter the following:

| **Field**        | **Value**                                                                                                                                                                           |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Name**         | Provide a name for the Linked Content. For example: `TomorrowIO_Current_Weather`                                                                                                    |
| **Request Type** | Select `GET` method.                                                                                                                                                                |
| **Endpoint URL** | Enter the following endpoint URL: `https://api.tomorrow.io/v4/weather/realtime?location={{city}}&apikey=<YOUR_API_KEY>` Replace `<YOUR_API_KEY>` with your actual Tomorrow\.io key. |

> 📘 Note
>
> The `{{city}}` parameter pulls the user’s city from their CleverTap profile. See [Supported Location Inputs](doc:tomorrowio#supported-location-inputs) for alternate formats.

<Image alt="Linked Content Setup" align="center" width="65% " border={true} src="https://files.readme.io/ce37875371854b254d9aeb3ef9fab40654a477a173a1e612bb33d0114d8ddb84-image.png">
  Linked Content Setup
</Image>

3. Click **Test Linked Content** to verify the connection. A successful response will look similar to the following sample:

```json
{
  "data": {
    "time": "2023-01-26T07:48:00Z",
    "values": {
      "temperature": 1.88,
      "humidity": 96,
      "precipitationProbability": 0,
      "windSpeed": 4.3,
      "uvIndex": 2,
      "weatherCode": 1001
    }
  }
}
```

4. Click **Auto-Fill Objects with Response** to automatically map the JSON keys.

<Image alt="Auto-Fill Objects with Response" align="center" width="55% " border={true} src="https://files.readme.io/1bfec3cb362a2879e3d6bad0812924a4c3285be0929b5f7f5646d6894dea32d1-0164c761-dd8e-41e0-b603-8449b59f699c.png">
  Auto-Fill Objects with Response
</Image>

5. Click **Test and Save** to complete your Linked Content configuration.

<Image alt="Test and Save" align="center" width="35% " border={true} src="https://files.readme.io/3402fb23a998b25fd1aaee63d16c5ea1f0f39e0ecd8d0095bb5f33980d5a6302-image.png">
  Test and Save
</Image>

# Create Personalized Campaign

Once Linked Content is configured, you can use Tomorrow\.io data to create personalized campaigns in CleverTap. You can personalize campaigns based on real-time weather data in a Push Notification campaign or any other campaign type that supports Linked Content. To do so, perform the following steps:

1. Go to the *Campaigns* page, click **+ Campaign**, and select *Push Notification* from the list of messaging channels.
2. Click **Go to Editor** under the *What* section.

   1. Click **Personalization** in the top-right corner.
   2. Select the Linked Content configured in [Configure Linked Content API](doc:tomorrowio#configure-linked-content-api).
   3. Map the `{{city}}` parameter to the user's city attribute.

<Image alt="Personalization Setup" align="center" width="65% " border={true} src="https://files.readme.io/9ec0c78d8ef935cccc5c81d03f29d48d422b81343bc86b510ee9c5be171a2bb6-9b5f5333-12d5-4221-bdc3-f213ba3d6e78.png">
  Personalization Setup
</Image>

3. Use [Liquid tags](doc:personalize-message-all#liquid-tags) to personalize your message dynamically. For example:

```liquid
{% if Linked.Tomorrow.temperature < 18 %}
❄️ Feeling the chill? Stay warm with our **Winter Collection**!  
Use code **WINTER20** to get **20% OFF** today!  
🧥 Shop now
{% else %}
☀️ It's a pleasant day ahead!  
Check out our **new arrivals** for all-season comfort.  
👕 Explore now
{% endif %}
```

<Image alt="Example Personalized Message" align="center" width="65% " border={true} src="https://files.readme.io/4350ed84e748fa13d2cf0125637d548f70d39b73fce8f4e76d9234dff4c7733c-a0b910ce-b353-4177-9b20-ed54f6f808e9.png">
  Example Personalized Message
</Image>

4. Click **Preview and Publish** to test and launch your campaign.

Your campaign will now deliver personalized, weather-aware notifications to users based on real-time data from their location.

<Image alt="Push Notification Preview" align="center" width="25% " border={true} src="https://files.readme.io/a162ac3d1c1689ca94c3859878eda473762f6cb01c47c27e86b91fefc9da5514-ac48828e-0956-419b-9d8f-05bf100688a4.png">
  Push Notification Preview
</Image>

By integrating Tomorrow\.io’s hyper-local weather insights with CleverTap’s campaign personalization tools, you can create timely, relevant user experiences that increase engagement and drive conversions, automatically adapting to your users’ environment in real time.
