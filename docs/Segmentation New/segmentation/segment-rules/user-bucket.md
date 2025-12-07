---
title: User Bucket
excerpt: >-
  Understand User Bucket numbers in CleverTap and how they are used for
  segmenting and testing campaign effectiveness.
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

When a new user profile is created in CleverTap, a random bucket number between 0 and 999 is automatically assigned. This unique system user property allows you to create uniformly distributed segments of random users, effective for testing the long-term impact of various campaigns on groups of users over time. By evaluating the results from these segments over multiple campaigns, you can determine whether to retain the same bucket numbers for future campaigns or adjust your strategy based on the insights gained. This approach ensures a balanced assessment of your campaign's effectiveness over time, enabling continuous optimization and improvement.

> 📘 Private Beta
> 
> Currently, this feature is a Private Beta Release. If you want access to this feature, contact your Account Manager.

# Use Cases

Here are some use cases where CleverTap's random bucket number assignment can be helpful:

- **Phased Feature Rollout**: Gradually release new features to random user segments. Assess user feedback and performance before a full-scale release, minimizing risk and ensuring quality.
- **Campaign Optimization**: A company wants to test the impact of different promotional offers on user engagement. They would create segments based on random bucket numbers (for example, 0-100, 101-200) and apply different offers to each segment. Then, they can compare engagement metrics to determine which offer performs best.
- **Personalization Strategies**: A retailer wants to test various personalized recommendations to improve sales. The retailer would segment users using bucket numbers and deliver different recommendation algorithms to each segment. The retailer would then measure the effectiveness of each algorithm in terms of conversion rates and sales.
- **Cross-Channel Campaign Testing**: A company is running a multi-channel marketing campaign and wants to evaluate the impact of each channel. They would randomly segment users and expose each segment to different channels (for example, email, push notifications, social media). They would then measure the effectiveness of each channel in driving conversions and engagement.

Thus, you gain actionable insights into what works best by applying distinct strategies to these segments and measuring their performance. These insights guide future decisions and strategy adjustments, allowing you to refine and enhance your campaigns based on experimental data and user behavior.

# Segment Users Based on User Buckets

When creating a segment, add the User Bucket filter. Then, you can specify a number or range of numbers to include in your segment.  
For example, create a segment of users who _Added to Cart_ but did not do a _Charged_ event in the _last 30 days_ and belong to user buckets from 0 to 100.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d3ef701-Random_User_Buckets.png",
        "",
        "Segmenting on Random Bucket Users"
      ],
      "align": "center",
      "border": true,
      "caption": "Segmenting on Random Bucket Users"
    }
  ]
}
[/block]


You can now include these types of segments if you want to run multiple variants of your campaigns. After running these campaigns for the required period, you can use the campaign statistics to decide whether to continue using the same bucket numbers or adjust your segmentation to optimize performance.

> 📘 Note
> 
> Because the assignment is random, the performance of a particular segment in one campaign does not predict how it will perform in future campaigns. Due to the random nature of the buckets, each campaign could yield different results.