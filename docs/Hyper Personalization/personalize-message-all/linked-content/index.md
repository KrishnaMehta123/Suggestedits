---
title: Linked Content
excerpt: Learn more about dynamic messaging with Linked Content.
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

Linked Content lets you enrich your messages with dynamic, real-time data from sources outside the CleverTap platform. It supports send-time personalization, ensuring each message is contextual with the most relevant data.

For example, if you operate a food delivery service across various geographies, you can tailor offers based on each user's local weather. CleverTap can pull the user's location from profile attributes, while weather details are fetched from a third-party API. If you want to add more information, you can opt to include any source, such as third-party tools and in-house software, in your message.

In a user scenario, you could have three users: one in New York, where it is snowing, one in San Francisco, where it is cloudy, and one in Miami, where it is sunny. You can add conditions in your messages to deliver messages according to the weather and location where the message will be delivered, such as:

* New York user: Since this user is probably staying in a cold region, you can send an offer to order piping hot food. 
* San Francisco user: Since it is the weekend, this user may go out in the evening, so you send an offer for a dinner reservation at a nearby restaurant. 
* Miami user: Since it is always sunny, you send an offer for a nearby barbecue restaurant. 

Personalizing your content can help you better meet the needs of your end users, which can significantly increase your click rates.

> 📘 Note
>
> You can create *Linked Content* using *Liquid Tags.* For more information, refer to [Liquid Tags](https://docs.clevertap.com/docs/liquid-tags) before you begin.

You can use *Linked Content* with the following engagement channels:

* Email
* Mobile Push
* SMS
* Webhooks
* WhatsApp
* Native Display

# Video Tutorial

You can watch the following video to learn more about Linked Content personalization.

<HTMLBlock>{`
<div
              style="
                position: relative;
                padding-bottom: 56.25%;
                height: 0;
                border-radius: 0;
                box-shadow: 0 15px 40px rgba(63,58,79,.3);
                overflow: hidden;
                min-width:320px"><iframe
              src="https://clevertap.portal.trainn.co/share/7TS9XZhkIYJhZzaiEiuq0w/embed?autoplay=false"
              frameborder="0"
              webkitallowfullscreen
              mozallowfullscreen
              allowfullscreen
              allow="autoplay; fullscreen"
              style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;"></iframe></div>
`}</HTMLBlock>

# Create Linked Content API

You can get the data for send-time personalization from different APIs. API names are nicknames that you can assign to the provider APIs. You can call these anywhere in your message so that you do not have to mention the entire API name. For example, if the API fetches the weather information for a particular city. You can shorten the API endpoint URL   `http://api.example.com/weather-management/city-weather`  to just `Weather` as the API name. You can also [personalize the API endpoint URL](doc:linked-content#personalize-linked-content-url).

To. create API names:

1. Select *Settings* > *Setup* > *Linked Content*. The *Linked Content* page displays.
2. Click the **+ Linked Content** button to call a new API. To edit the linked content, click the ellipsis menu, then click the edit icon. 
3. Enter a name for the API. 

<Image title="Create API Names" alt={1163} align="center" width="smart" border={true} src="https://files.readme.io/65c4783-Linked_Content_API_Create.png">
  Create API Names
</Image>

4. Enter all the relevant details, such as the access key and query parameters.
5. Click the **Test Linked Content** link. 
6. Enter the required details to test the API. If the input is correct, you will see a success message. The test response appears in the JSON response box. The response format is always JSON.\
   The following is an example response for the API name you entered:

```json
"request": {
    "type": "City",
    "query": "New York, United States of America",
    "language": "en",
    "unit": "m"
  },
  "location": {
    "name": "New York",
    "country": "United States of America",
    "region": "New York",
    "lat": "40.714",
    "lon": "-74.006",
    "timezone_id": "America/New_York",
    "localtime": "2020-04-22 12:44",
    "localtime_epoch": 1587559440,
    "utc_offset": "-4.0"
  },
  "current": {
    "observation_time": "04:44 PM",
    "temperature": 7,
    "weather_code": 113,
    "weather_icons": [
      "http://cdn.worldweatheronline.com/images/wsymbols01_png_64/wsymbol_0001_sunny.png"
    ],
    "weather_descriptions": [
      "Sunny"
    ],
    "wind_speed": 17,
    "wind_degree": 280,
    "wind_dir": "W",
    "pressure": 1012,
    "precip": 0,
    "humidity": 28,
    "cloudcover": 0,
    "feelslike": 4,
    "uv_index": 6,
    "visibility": 16,
    "is_day": "yes"
  }
}
```

7. You can choose to add each API object manually or click *Auto-fill Objects* with the API response. All the objects are listed with their label names. If required, you can change the label names here. These labels are available at the time of campaign creation.

<Image title="Add API Objects" alt={1192} align="center" width="smart" border={true} src="https://files.readme.io/8174ccf-Dynamic_Content_API.png">
  Add API Objects
</Image>

8. Click **Test and save changes** to save all the API changes. 

> 📘 Encoding Error
>
> * If you encounter encoding errors in your API response due to non-English characters, add the `charset=utf-8` parameter to your endpoint.
>
> <Image align="center" className="border" border={true} src="https://files.readme.io/cc268ec-image.png" />
>
> * If using an internal API endpoint, check internally for the relevant parameters.
> * If you use an external API endpoint, the parameters are available with the provider. For API details, refer to their website or contact their support.

# Use Linked Content in Campaigns

The APIs must be mapped to the campaign from the *What* section. After the APIs are mapped, you can use them in the email body using [liquid tags](https://docs.clevertap.com/docs/liquid-tags). The sample scenario below shows how to create an email campaign using liquid tags and linked content.

1. [Create an Email Campaign](https://docs.clevertap.com/docs/create-message-email).  
2. Select the *New email with rich media* template. 
3. From the [What](https://docs.clevertap.com/docs/email#section-step-4-define-the-what) section, click ![](https://files.readme.io/d946c02-personalization_icon.png) icon. The *Personalization Setup* window displays. 

<Image title="Create Personalized Email" alt={2876} align="center" border={true} src="https://files.readme.io/17bef81-Click_Personalization_icon.png">
  Create Personalized Email
</Image>

4. Select your APIs from the list under the *Linked Content* tab. 

<Image title="Select APIs from Linked Content" alt={1896} align="center" border={true} src="https://files.readme.io/e1a6472-Linked_Content.png">
  Select APIs from Linked Content
</Image>

5. Map the API parameters to the user and event properties, or add custom parameters. Here, we map the query parameter that fetches weather information based on the user location with the help of the profile property *Location*. This means that each user is sent an offer based on their location. 

<Image title="Map Linked Content" alt={1898} align="center" width="smart" border={true} src="https://files.readme.io/6011741-Map_Linked_Content.png">
  Map Linked Content
</Image>

> 📘 Mapping Custom Fields
>
> You can also use liquid tags for personalization when mapping customer properties for an External Trigger Campaign. You can access this feature only if you have External Trigger enabled for your account.
>
> <Image alt="Mapping Custom Fields Using Liquid Tags" align="center" border={true} src="https://files.readme.io/1bcf690-Mapping_Custom_Fields.gif">
>   Mapping Custom Fields Using Liquid Tags
> </Image>

6. Click **Apply** to save the mapping. 

We are now ready to start writing Linked Content. 

# Use Labels to Simplify Personalization

You can write linked content with labels. There are two types of labels that you can use in your linked content. 

* Custom Labels - These are labels you can create yourself. For example, password or authorization key.
* System Labels - These are default labels you can use to analyze API responses. 

## Custom Labels

The API response will provide you with a set of object labels. However, if you want additional personalization, you can create custom labels during the creation and editing of [APIs](https://docs.clevertap.com/docs/linked-content#section-create-edit-namespaces). These will not be part of the API response.  

## System Labels

These are CleverTap labels that are available by default. You can use them to gauge the health of your API and check whether the responses are received correctly or not. 

| System Labels      | Description                                                                                               |
| :----------------- | :-------------------------------------------------------------------------------------------------------- |
| raw                | This is a raw API response.                                                                               |
| JSON               | This is the raw response parsed as JSON.                                                                  |
| http\_status\_code | This is the HTTP status code to identify errors, such as, 404 (not found), 401 (unauthorized), and so on. |
| headers            | These are response headers.                                                                               |

# Handle Arrays in API Responses

The response from an API may have arrays with nested JSON. 

```json Example Response
"restaurants_info": [
    { 
        "id": "16769241",
        "name": "Junior's Restaurant",
        "user_rating": {
            "aggregate_rating": "4.7",
            "rating_text": "Excellent",
            "votes": "538"
     }      
    },
  
    {
        "id": "16763460",
        "name": "Cookshop",
        "user_rating": {
           "aggregate_rating": "4.6",
           "rating_text": "Excellent",
           "votes": "252"
        }
    }
]
```

You can create conditions based on this array. For example, the response above has an array called `restaurants`. This array contains items under it such as id, name, rating. Notice the object `user_rating`. It is a nested object that contains an aggregate rating of the restaurant, rating text from an actual user, number of votes, and so on. You can use the array in the following manner:

```liquid Array list
{% for restaurant in Linked.RestaurantAPI.restaurants_info limit:5%} 
{{restaurant.name}}  {{restaurant.user_rating.rating_text}}
{% endfor %}
```

The output will be something similar to the following text:

```text Output - Array list
Marta has a rating  Excellent
PN Wood Fired Pizza  Excellent
PQR Very Good
&pizza   Good
Leonelli Focacceria e Pasticceria Good
```

# Personalized Campaign Using Linked Content

After you have created and saved the APIs, use the linked content in your campaigns. It is recommended that you familiarize yourself with [Liquid Tags](https://docs.clevertap.com/docs/liquid-tags) before you start writing Linked Content. The syntax for writing linked content is `Linked.APIName.label`. In our previous user scenario, we had three users, one in New York, where it was snowing, one in San Francisco, where it was cloudy, and one in Miami, where it was sunny. You can add conditions in your messages to deliver messages according to the weather and zip code. So, you can plan the following message:

* New York user - Since this user is probably staying in, you send an offer for ordering piping hot food. 
* San Francisco user - Since it is the weekend, this user may go out in the evening, so you send an offer for a dinner reservation at a nearby restaurant. 
* Miami user - Since it is always sunny, you send an offer for a nearby barbecue restaurant. 

The following is what a written personalized linked content for your users may look like:

```liquid
Hi {{ Profile.name | default:"there!" }},

{% if Linked.cityBasedWeather.temp > 30 %}
It is a bright sunny day in {{ Profile.location | default:"your city" }}. How about a barbeque today?


{% elsif Linked.cityBasedWeather.temp < 10 %}
It is indeed cold today in {{ Profile.location | default:"your city" }}!! Time for some hot pizza!
{% else %}
It has  been a while in {{ Profile.location | default:"your city" }}. Order something exotic!
{% endif %}
```

If you want to add a list of the top 5 restaurants in this message, you can add the following in the main message:

```liquid
{% for restaurant in Linked.RestaurantAPI.restaurants_info limit:5%} 
{{restaurant.name}}  {{restaurant.user_rating.rating_text}}
{% endfor %}
```

The final message before you send out the email may look like the following:

```liquid
Hi {{ Profile.name | default:"there!" }},

{% if Linked.cityBasedWeather.temp > 30 %}
It is a bright sunny day in {{ Profile.location | default:"your city" }}. How about a barbeque today?

Use the coupon code (BARBQ).
These are the top 5 restaurants near you:
{% for restaurant in Linked.RestaurantAPI.restaurants_info limit:5%} 
{{restaurant.name}}  {{restaurant.user_rating.rating_text}}
{% endfor %}


{% elsif Linked.cityBasedWeather.temp < 10 %}
It is indeed cold today in {{ Profile.location | default:"your city" }}!! 
Time for some hot pizza!
                                         
Use the coupon code (PIZZA). These are the top 5 restaurants near you:
{% for restaurant in Linked.RestaurantAPI.restaurants_info limit:5%} 
{{restaurant.name}}  {{restaurant.user_rating.rating_text}}
{% endfor %}
                                          
{% else %}
                                          
It has  been a while in {{ Profile.location | default:"your city" }}. 
Order something exotic!
                                          
Use the coupon code (EXOTIC).These are the top 5 restaurants near you:           {% for restaurant in Linked.RestaurantAPI.restaurants_info limit:5%} 
{{restaurant.name}}  {{restaurant.user_rating.rating_text}}
{% endfor %}
                                          
{% endif %}
```

Add some personalizations from our editor, then send out the email. For additional information on how to personalize your email, refer to [Create an Email Campaign](https://docs.clevertap.com/docs/create-message-email). 

<Image title="Create Email Campaign using Linked Content" alt={1107} align="center" width="80% " border={true} src="https://files.readme.io/eebe749-linked_content_email_example_split.png">
  Create an Email Campaign using Linked Content
</Image>

# FAQs

### Do you retry if the linked content API fails to give a successful payload?

We do not retry if the linked content API fails to give a successful payload.

### How much time do you wait to fetch the API response?

We wait **five** seconds to fetch the API response.
