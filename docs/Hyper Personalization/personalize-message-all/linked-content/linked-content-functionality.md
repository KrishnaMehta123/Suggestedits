---
title: Linked Content Functionality
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

CleverTap fetches dynamic content from external sources in real-time when delivering personalized messages using Linked Content. The speed and efficiency of this process depend on how the content is personalized and how caching is utilized.

# Response Time and Request Management

CleverTap retrieves content from external APIs to personalize messages. The number of API requests and the time taken can vary based on personalization:

- **Shared Content**: If personalized values are **not used** and the same content applies to multiple users (such as a weather update for all users in Mumbai), CleverTap fetches it once and reuses it. This reduces the number of API calls.
- **Unique Content**: If personalized values **are used** and each user requires different content (such as user-specific location or profile information), CleverTap fetches fresh content for every user. This increases the number of API calls.

So, approximately **460 API calls** can be made per second to fetch Linked Content.

# Caching

To avoid fetching the same content multiple times, CleverTap temporarily stores responses for reuse. This is called caching. Here's how it works:

- If CleverTap receives a valid response it has already seen (based on the API URL and parameters), it reuses it instead of making a new API call.
- This response is stored for up to 5 minutes.
- After 5 minutes, CleverTap will fetch fresh data to ensure it's up to date.
- CleverTap can store up to 1,000 unique combinations of user details per account.

This significantly reduces the API load and speeds up message delivery for campaigns with similar content.

# Timeout

Every request made to fetch Linked Content has a maximum wait time, known as a timeout. The timeout for each API request is **5 seconds**. 

If a request does not complete within 5 seconds, it is considered failed. There is no retry mechanism for failed requests, so ensure that the API you are connecting to is reliable and responsive.

## Example Scenarios

### Example 1: Campaign with 4.5 Million Users

- Suppose you are sending a campaign to 4.5 million users.
- If fully personalized content is needed for each user, and caching is not possible, it could take approximately **2 hours 45 minutes** to fetch all responses.
- If personalization is minimal and caching is effective, the campaign can complete much faster.

### Example 2: Campaign with 10 Million Users

Imagine you want to include weather information based on each user’s region in your email campaign.

- **Best Case (Caching Effective):**  
  If all users are from the same city, Linked Content fetches the weather data once every 5 minutes and reuses it for all users. Emails are sent very quickly.

- **Good Case (Moderate Personalization):**  
  If users are spread across a few cities, Linked Content makes about **10–15 API requests** for different regions. The campaign experiences only a slight delay.

- **Worst Case (Full Personalization):**  
  If every user is from a different region, a **unique API call** is made for each user. This leads to significant delays, depending on third-party API response times.

> 📘 **Key Consideration:**
> 
> Whenever possible, designing campaigns that allow caching (such as grouping users by city or region) will dramatically improve delivery speed and efficiency.