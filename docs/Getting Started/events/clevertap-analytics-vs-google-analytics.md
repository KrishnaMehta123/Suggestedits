---
title: CleverTap Analytics vs. Google Analytics
excerpt: Learn why the Event Data between CleverTap and Google does not match.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

Variations in event data between CleverTap Analytics and Google Analytics are not uncommon due to differences in data collection methods, sampling, processing, aggregation, attribution models, and platform-specific limitations. 

This documentation aims to provide information on the top factors contributing to the difference in event data between these two analytics platforms, that is, Google Analytics and CleverTap Analytics. The following are the main factors due to which the event data between CleverTap and Google differ:

## Data Collection Methods

CleverTap Analytics and Google Analytics employ different data collection methods, which can lead to variations in event data. The following factors contribute to these differences:

- **SDK Integration**: CleverTap and Google Analytics provide their respective SDKs, which developers integrate into mobile or web applications. Differences in SDK implementation, event tagging, or parameter mapping can result in variations in event data collection. It is crucial to ensure consistent implementation across both platforms to minimize discrepancies.
- **Tracking Mechanisms:** CleverTap Analytics and Google Analytics may use different tracking mechanisms, such as cookies, unique identifiers, or custom tracking codes. These mechanisms can vary in their accuracy and reliability, potentially leading to differences in event data.

## Data Sampling

Data sampling involves selecting a subset of the data for analysis and extrapolating insights from that subset. CleverTap Analytics and Google Analytics may employ different data sampling techniques to manage and process large volumes of event data, resulting in variations in the reported event data. 

## Data Processing and Aggregation

CleverTap Analytics and Google Analytics use different algorithms and methodologies for data processing and aggregation, which can contribute to differences in event data. The following factors affect data processing and aggregation:

- **Time Zones:** CleverTap Analytics and Google Analytics may operate in different time zones, which can affect how events are categorized and reported, especially for events occurring close to time zone boundaries. Time zone differences can lead to variations in event timestamps and their subsequent analysis.
- **Event Deduplication:** The techniques used to detect and remove duplicate events may vary between CleverTap Analytics and Google Analytics. These differences can impact event counts and metrics, resulting in variations in the reported data.

## Event Attribution Models

Event attribution models determine how credit is assigned to various touchpoints leading to a specific event. CleverTap Analytics and Google Analytics may employ different attribution models, such as first-touch, last-touch, or multi-touch attribution. These models can allocate credit differently, causing variations in the reported event data. Understanding the attribution models used by each platform is crucial when comparing event data.

## Platform-Specific Limitations

Each analytics platform has its own limitations or constraints that can affect event data collection and reporting. These limitations arise from platform-specific factors, including:

- **Device and OS Compatibility:** Differences in a device or operating system compatibility can impact data collection accuracy, leading to variations in event data. It is important to ensure that the platforms are compatible with the target devices and operating systems to minimize discrepancies.
- **Network Connectivity:** Network issues or unreliable connections during data transmission can result in missing or delayed event data, causing discrepancies between CleverTap Analytics and Google Analytics. Ensuring a stable network connection is essential for accurate data collection.

## Session Timeout

 A session is a series of user interactions with the website or application within a given time period. Google Analytics and CleverTap utilize session-based tracking to analyze user interactions. Google Analytics sets its session timeout duration to 30 minutes by default, meaning that if a user is inactive for more than 30 minutes, a new session is triggered upon their next interaction. On the other hand, CleverTap employs a session timeout duration of 20 minutes. This discrepancy in session timeout durations can result in differences in analytics counts, especially for user engagements spanning longer durations. It is essential to consider this variation when comparing event data between CleverTap and Google Analytics.

## Unique User Identification

Unique user identification is crucial for accurately tracking user behavior and engagement metrics in analytics platforms. CleverTap employs the `onUserLogin` method, which triggers whenever a user logs into the application. This method establishes and maintains a unique user identity within the CleverTap system. It triggers whenever a user logs into the application, ensuring accurate tracking of user behavior and engagement metrics. This method is superior as it tracks actual logins, eliminating noise and providing precise user identification.

However, Google Analytics does not utilize a similar method for user identification. Instead, Google relies on a combination of unique identifiers, such as cookies or device IDs, to track and distinguish individual users. The absence of a specific `onUserLogin` method in Google Analytics may lead to differences in how unique users are identified and tracked compared to CleverTap. This distinction highlights CleverTap's advantage in providing more accurate and reliable user-level metrics.

# Conclusion

Users of these analytics platforms other than CleverTap must carefully consider the above-mentioned factors when analyzing and comparing event data, taking into account the specific context and requirements of their applications. Implementing consistent event tracking and understanding the underlying mechanisms can help minimize discrepancies and improve data accuracy across both platforms.