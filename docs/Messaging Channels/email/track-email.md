---
title: Track Email
excerpt: Learn how to track your emails
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
# Overview

CleverTap allows you to track emails and analyze data such as links, attachments, and open rates of emails. You can boost your user engagement by tracking your emails.

# Track Client Names

Get insights for your email campaign such as the *Client name (*&#x73;uch as Gmail) and *User Agent* (such as Mozilla Firefox). If some clients cannot be identified, they are saved as *Unidentified* clients. 

## Analyze Client Names

You can analyze the client names to check the efficiency of your campaign and if the message is received correctly by the target audience. 

Clients are tracked with the Notification Viewed event. You can use the event properties *Client Name* and *User Agent* to analyze your campaign.\
Follow the steps to analyze the client information:

1. Click Analytics > Events from the dashboard.
2. Select the event *Notification Viewed*.
3. Filter by the *Campaign Type* as *Email* event property. 
4. Click View Details. 
5. Click the Trend & Properties tab to view the event trend.
6. Scroll down to *Event property* section.  
7. Select the *Client Name* property from the list to view the clients. 

![1160](https://files.readme.io/43d4f02-Email_client_name_property.png "Email_client_name_property.png")

8. Select the event *User Agent* to view the client by the user agent.

<Image title="Email_user_agent_property.png" alt={1165} className="border" border={true} src="https://files.readme.io/6d35e3f-Email_user_agent_property.png" />

9. Toggle between the views by clicking the ![event property view](https://files.readme.io/2d94b48-Analytics_Event_Property_view_toolbar.png) toolbar.
10. Scroll down to see a Frequency histogram.
