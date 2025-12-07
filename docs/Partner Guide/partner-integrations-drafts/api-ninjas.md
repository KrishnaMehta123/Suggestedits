---
title: API Ninjas
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

[API Ninjas](https://api-ninjas.com/) offers a comprehensive suite of APIs providing real-time data across multiple domains. The **Weather API** within the suite delivers detailed, real-time weather information, including temperature, humidity, wind speed, and more, for any city or geographic location worldwide.

With the CleverTap and API Ninjas integration, you can enrich your marketing campaigns with real-time weather insights as follows:

* Trigger promotions when the temperature crosses a certain threshold.
* Deliver weather-relevant offers such as raincoats during rainy days or sunscreen during sunny weather.
* Engage users contextually based on real-time environmental data.

# Prerequisites for Integration

To integrate API Ninjas with CleverTap, ensure the following prerequisites are met:

* You have an **API Ninjas account** and an active [API Key](https://api-ninjas.com/profile).
* You have an active CleverTap account.
* User location details (latitude and longitude or city) are stored in CleverTap user profiles as properties.

# Integrating API Ninjas with CleverTap

The integration process involves the following three key steps:

1. [Locate API Ninjas API Key](doc:api-ninjas#locate-api-ninjas-api-key)
2. [Configure Linked Content API](doc:api-ninjas#configure-linked-content-api)
3. [Create Personalized Campaign](doc:api-ninjas#create-personalized-campaign)

## Locate API Ninjas API Key

To complete the integration process, you need your API Ninjas API Key. Follow these steps to locate it:

1. Log in to your [API Ninjas Dashboard](https://api-ninjas.com/profile).
2. Copy your **API Key** under the API section; this will be used for Linked Content authentication.

<Image alt="API Ninjas API Key" align="center" width="65% " border={true} src="https://files.readme.io/0d446bdc62e082872bf9223a7128b9249e5a9fb0d991e5054ece01d40d9dc12c-image.png">
  API Ninjas API Key
</Image>

## Configure Linked Content API

Integrate API Ninjas Weather API with CleverTap by setting up Linked Content. To do so, perform the following steps:

1. Go to *Settings* > *Setup* > *Linked Content* from the CleverTap dashboard.
2. Click **+ Linked Content** and enter the following:

| Field        | Value                                                                                              |
| ------------ | -------------------------------------------------------------------------------------------------- |
| Name         | Provide a name for the Linked Content. For example: `WeatherAPI`                                   |
| Request Type | Select `GET` method.                                                                               |
| Endpoint URL | Enter the following endpoint URL: `https://api.api-ninjas.com/v1/weather?lat={{lat}}&lon={{long}}` |

This endpoint uses the following three parameters:

* `Latitude` and `Longitude` pulled from user profile (custom properties)
* `place:` chain name to search near the user (for example, `Starbucks`)

<Image alt="Linked Content Setup" align="center" width="75% " border={true} src="https://files.readme.io/7a7ddb097948e125943746070af9f1c72ee4797e55df3d2d6979b2239efc02df-image.png">
  Linked Content Setup
</Image>

3. Under *Headers*, add the following key-value pair:
   * Key: `X-Api-Key`
   * Value: `<Your_API_Ninjas_Key>`

<Image alt="Header Setup" align="center" width="75% " border={true} src="https://files.readme.io/1a63647e2912b938296166fd85a6e93661480c9dbb779de0cc6ed2ae87130d90-image.png">
  Header Setup
</Image>

4. Click **Test the Linked Content** using sample values. The following is a sample API response:

```json
{
  "temp": 28,
  "humidity": 75,
  "wind_speed": 4.5,
  "sunrise": 1615616341,
  "sunset": 1615658463
}
```

5. Click **Auto-Fill Objects with Response** to automatically handle responses and populate objects.

<Image alt="Auto-Fill Objects with Response" align="center" width="65% " border={true} src="https://files.readme.io/f38b951f29ff730be27ec068b083b5332984b5a1701df40f0b01676cfbd4f763-image.png">
  Auto-Fill Objects with Response
</Image>

6. Click **Test and save changes** to complete the setup.

<Image alt="Test And Save" align="center" width="35% " border={true} src="https://files.readme.io/34ed47fcd4270fe6aa081bc6218294b4d2c932458d59052e1c9912dde4e19eb0-image.png">
  Test And Save
</Image>

## Create Personalized Campaign

Once the API Ninjas Weather API is integrated, you can use it in a CleverTap push notification campaign to personalize messages based on current weather conditions. To do so, perform the following steps:

1. Go to the *Campaigns* page, click **+ Campaign**, and select *Push Notification* from the list of messaging channels.
2. Click **Go to Editor** under the *What* section.
   1. Click **Personalization**.
   2. Select the Linked Content configured under [Configure Linked Content API](doc:api-ninjas#configure-linked-content-api) and click **Apply**.
   3. Map parameters to personalize the message dynamically:
      * **Latitude** → `{{ Profile.lat }}`
      * **Longitude** → `{{ Profile.long }}`

<Image alt="Personalization Setup" align="center" width="75% " border={true} src="https://files.readme.io/627da66a02eb948399c743d99aabd0587460e1cd68d8efe86bedfb4c9633d830-image.png">
  Personalization Setup
</Image>

3. Use [Liquid tags](doc:personalize-message-all#liquid-tags) to personalize the campaign message. For example:

```liquid
It's currently {{ Linked["WeatherAPI"].temp | default: "N/A" }}°C where you are.
{% if Linked["WeatherAPI"].temp < 20 %}
❄️ Brr! Stay warm with 20% off on our winter collection!
{% elsif Linked["WeatherAPI"].temp >= 20 and Linked["WeatherAPI"].temp < 35 %}
🌤️ Perfect weather for a stroll! Enjoy 15% off our casual wear!
{% elsif Linked["WeatherAPI"].temp >= 35 %}
☀️ Beat the heat with 20% off our summer essentials!
{% else %}
🛍️ Enjoy shopping with us today!
{% endif %}
```

<Image alt="Example Personalize Message" align="center" width="65% " border={true} src="https://files.readme.io/e2898162452f4e8739e538227a57d77e00cbc2389414d368b22b007a6f831399-image.png">
  Example Personalize Message
</Image>

4. Click **Preview and Publish** to test and launch the campaign.

<Image alt="Push Notification Preview" align="center" width="35% " border={true} src="https://files.readme.io/f9f9e88cc9e7ed90c57e2e8ba98bfd76fe94d6b4fd8eafcd9f48df5649807979-image.png">
  Push Notification Preview
</Image>

By combining API Ninjas' real-time weather data with CleverTap’s personalization engine, you can deliver timely, weather-aware campaigns that boost engagement and conversion.
