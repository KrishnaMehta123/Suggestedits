---
title: Common Use Cases
excerpt: >-
  Explore a list of consolidated business use cases for Liquid Tags. You can use
  the sample use cases to increase customer engagement.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
<!DOCTYPE html>

<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

```
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 1.5rem;
  max-width: 1000px;
  margin: 2rem auto;
  padding: 1rem;
  justify-content: center;
}

.integration-card {
  display: flex;
  align-items: center;
  padding: 1.25rem 1.5rem;
  background: white;
  border-radius: 12px;
  min-height: 100px;
  border: 1px solid rgba(0, 0, 0, 0.08);
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.04);
  transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
  text-decoration: none;
}

.integration-card:hover {
  box-shadow: 0px 6px 12px rgba(0, 0, 0, 0.08);
  transform: translateY(-2px);
}

.logo-container {
  display: flex;
  align-items: center;
  padding-right: 1rem;
  border-right: 1px solid rgba(0, 0, 0, 0.08);
  margin-right: 1rem;
}

.logo {
  width: 48px;
  height: 48px;
  object-fit: contain;
  border-radius: 5px;
}

.content {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.name {
  font-size: 1rem;
  font-weight: 600;
  color: #000;
  margin-bottom: 0.3rem;
}

.category {
  font-size: 0.8rem;
  color: #666;
}

/* Responsive rules */
@media (max-width: 768px) {
  .grid {
    grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
    padding: 0 1rem;
  }
}

@media (max-width: 480px) {
  .grid {
    grid-template-columns: 1fr;
  }
}
```

  </style>
</head>
<body>

<div class="grid">
  <a href="#e-commerce" class="integration-card">
    <div class="logo-container">
      <img src="https://img.icons8.com/fluency/48/shopping-cart-loaded.png" class="logo" alt="E-Commerce" />
    </div>
    <div class="content">
      <div class="name">E-Commerce</div>
      <div class="category">Personalization & Offers</div>
    </div>
  </a>

  <a href="#job-portal" class="integration-card">
    <div class="logo-container">
      <img src="https://img.icons8.com/color/48/resume.png" class="logo" alt="Job Portal" />
    </div>
    <div class="content">
      <div class="name">Job Portal</div>
      <div class="category">Hiring & Notifications</div>
    </div>
  </a>

  <a href="#ott" class="integration-card">
    <div class="logo-container">
      <img src="https://img.icons8.com/color/48/tv.png" class="logo" alt="OTT" />
    </div>
    <div class="content">
      <div class="name">OTT</div>
      <div class="category">Content & Engagement</div>
    </div>
  </a>

  <a href="#fintech" class="integration-card">
    <div class="logo-container">
      <img src="https://img.icons8.com/color/48/money-bag.png" class="logo" alt="Fintech" />
    </div>
    <div class="content">
      <div class="name">Fintech</div>
      <div class="category">Finance & Portfolios</div>
    </div>
  </a>

  <a href="#food-delivery" class="integration-card">
    <div class="logo-container">
      <img src="https://img.icons8.com/color/48/meal.png" class="logo" alt="Food Delivery" />
    </div>
    <div class="content">
      <div class="name">Food Delivery</div>
      <div class="category">Menu & Recommendations</div>
    </div>
  </a>

  <a href="#gaming" class="integration-card">
    <div class="logo-container">
      <img src="https://img.icons8.com/color/48/controller.png" class="logo" alt="Gaming" />
    </div>
    <div class="content">
      <div class="name">Gaming</div>
      <div class="category">Rewards & Items</div>
    </div>
  </a>
</div>

</body>
</html>

## E-Commerce

#### Dynamic Discount Messaging

```liquid
{% case Profile.tier %}
  {% when "Silver" %}
    Enjoy 5% off on your next purchase!
  {% when "Gold" %}
    Enjoy 10% off and early access!
  {% when "Platinum" %}
    15% off + VIP support for you!
  {% else %}
    Sign up for a membership now for exclusive benefits!
{% endcase %}
```

#### Truncate Item List

```liquid
You viewed a lot of items! Here's a few to revisit:

{% for item in Profile.recently_viewed limit:3 offset:1 %}
- {{ item.name }}
{% endfor %}
```

#### Personalized Welcome Message

```liquid
Hi {{ user.name | default: 'there' }},
Welcome to [Your App Name]!
{% if user.welcome_offer %}
You've received a referral bonus of {{ user.welcome_offer }}!
{% else %}
Start exploring our app today.
{% endif %}
```

#### Abandoned Cart Recovery

```liquid
Hey {{ user.name | default: 'there' }},
We noticed you left item(s) in your cart.
{% if user.vip_status == 'Gold' %}
Here's an exclusive 10% discount for you! Apply code: VIP10 at checkout.
{% else %}
Complete your purchase now before your items sell out!
{% endif %}
```

#### Product Recommendations

```liquid
Hi {{ user.name }},
Based on your recent interest in {{ user.last_browsed_category }}, you might love these:
{% for product in recommendations %}
- {{ product.name }} for {{ product.price }}
{% endfor %}
Check them out before they're gone!
```

#### Subscription Renewal Reminders

```liquid
Hi {{ user.name }},
Your subscription to {{ user.subscription_plan }} expires on {{ user.subscription_end_date }}.
{% if user.auto_renew == false %}
Renew now to continue enjoying uninterrupted service!
{% else %}
No action needed! Your subscription will renew automatically.
{% endif %}
```

#### Personalized Birthday or Anniversary Messages

```liquid
Happy Birthday, {{ user.name }}! 🎉
As a special treat, enjoy a {{ user.birthday_discount }}% discount on your next purchase.
Use code: BDAY{{ user.id }}.
Offer valid until {{ today | date: "+7 days" }}.
```

#### Location-Based Promotions

```liquid
Hey {{ user.name }},
You're near our {{ user.nearest_store }} store! Stop by and enjoy an exclusive {{ user.local_discount }}% off today.
```

***

## Job Portal

#### Job Posting Confirmation with Dynamic Role & City

```liquid
Hi {{ Profile.employer_name | default: "Employer" }},

Your job posting for **{{ Event.job_role }}** in **{{ Event.job_city }}** has been published successfully!

You'll start receiving applications shortly. View applicants here: {{ Event.job_link }}
```

#### Application Alert with Candidate Count

```liquid
Hi {{ Profile.employer_name }},

You have received **{{ Event.new_applications_count }}** new applications for your job post: **{{ Event.job_role }}**.

{% if Event.new_applications_count > 5 %}
You’re trending! Consider shortlisting candidates soon to stay ahead.
{% else %}
You may get more applicants soon. Stay tuned!
{% endif %}
```

#### Candidate Profile Highlight

```liquid
Here are your top shortlisted candidates:

{% tablerow candidate in Event.shortlisted_candidates %}
{{ candidate.name }} - {{ candidate.experience }} years - {{ candidate.location }}
{% endtablerow %}
```

#### Reminder to Complete Profile

```liquid
{% if Profile.company_name == blank %}
  {% abort %}
{% endif %}

Hi {{ Profile.employer_name }},

Complete your profile for better visibility to job seekers. Your company "{{ Profile.company_name }}" deserves a spotlight!
```

#### Multi-City Job Posting Alert

```liquid
You’ve posted jobs in these cities:

{% assign cities = Event.job_cities | split: "," %}
{% for city in cities %}
- {{ city }}
{% endfor %}
```

***

## OTT

#### Content Recommendations by Genre

```liquid
{% assign genres = Profile.favorite_genres | split: "," %}
{% for genre in genres %}
  {% case genre %}
    {% when "Drama" %}
      Try our new emotional dramas!
    {% when "Comedy" %}
      You’ll love these hilarious comedies!
    {% when "Action" %}
      Adrenaline-packed shows waiting for you!
    {% else %}
      Check out trending shows in every genre!
  {% endcase %}
{% endfor %}
```

#### Auto-playlist Generation

```liquid
Your next binge list:

{% for show in Catalog.recommendations limit:3 offset:2 %}
- {{ show.title }} ({{ show.genre }})
{% endfor %}
```

***

## Fintech

#### Portfolio Table View

```liquid
Here's a snapshot of your portfolio:

{% tablerow investment in Profile.investments %}
{{ investment.type }} - ${{ investment.value }}
{% endtablerow %}
```

#### Auto-abort if profile is missing balance info

```liquid
{% if Profile.account_balance == blank %}
  {% abort %}
{% endif %}

Your current balance is ${{ Profile.account_balance }}
```

***

## Food Delivery

#### Menu Listing with Early Exit

```liquid
Available Deals Today:

{% for item in Catalog.daily_deals %}
  {% if item.sold_out %}
    {% break %}
  {% endif %}
  - {{ item.name }} for ${{ item.price }}
{% endfor %}
```

#### Skip Low-rated Restaurants

```liquid
Top Restaurant Picks:

{% for restaurant in Catalog.restaurants %}
  {% if restaurant.rating < 3 %}
    {% continue %}
  {% endif %}
  - {{ restaurant.name }} ({{ restaurant.rating }}⭐)
{% endfor %}
```

***

## Gaming

#### Login Bonus Timer

```liquid
Hi {{ Profile.username }},

You logged in at {{ now }}. Come back in 24 hours for your next reward!
```

#### Item Showcase with Limit

```liquid
Exclusive In-game Items:

{% for item in Catalog.special_items limit:2 %}
- {{ item.name }}: {{ item.power }}
{% endfor %}
```

![](https://files.readme.io/ae813b1dc8324a6534b778731af81d4480700837934250eeb7f9b13358a9a337-Storm_DS_Lquid_tag_1.svg)