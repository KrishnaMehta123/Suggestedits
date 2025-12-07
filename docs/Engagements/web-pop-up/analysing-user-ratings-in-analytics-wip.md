---
title: Analysing User Ratings in Analytics (WIP)
excerpt: Understand how you can analyze user ratings for accurate data analysis
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
## Tracking Events

Whenever a user submits the feedback form, the **Rating Submitted** event is triggered. This event includes properties such as *User Rating, Input Type, Comment*.\
Refer to the table below for a better understanding of the event properties.

<Table align={["left","left","left","left","left"]}>
  <thead>
    <tr>
      <th style={{ textAlign: "left" }}>
        Event Name
      </th>

      <th style={{ textAlign: "left" }}>
        Properties
      </th>

      <th style={{ textAlign: "left" }}>
        Data Type
      </th>

      <th style={{ textAlign: "left" }}>
        Sample Value
      </th>

      <th style={{ textAlign: "left" }}>
        Comments
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td style={{ textAlign: "left" }}>
        Rating Submitted
      </td>

      <td style={{ textAlign: "left" }}>
        User Rating
      </td>

      <td style={{ textAlign: "left" }}>
        Number
      </td>

      <td style={{ textAlign: "left" }}>
        3
      </td>

      <td style={{ textAlign: "left" }}>

      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>

      </td>

      <td style={{ textAlign: "left" }}>
        Input Type
      </td>

      <td style={{ textAlign: "left" }}>
        String
      </td>

      <td style={{ textAlign: "left" }}>
        Rating/NPS
      </td>

      <td style={{ textAlign: "left" }}>

      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>

      </td>

      <td style={{ textAlign: "left" }}>
        Comment
      </td>

      <td style={{ textAlign: "left" }}>
        String
      </td>

      <td style={{ textAlign: "left" }}>
        Awesome product
      </td>

      <td style={{ textAlign: "left" }}>
        512 characters limit
      </td>
    </tr>

    <tr>
      <td style={{ textAlign: "left" }}>

      </td>

      <td style={{ textAlign: "left" }}>
        Campaign Id
      </td>

      <td style={{ textAlign: "left" }}>
        String
      </td>

      <td style={{ textAlign: "left" }}>
        17654
      </td>

      <td style={{ textAlign: "left" }}>

      </td>
    </tr>
  </tbody>
</Table>

The event details can then be tracked from the Analytics dashboard.

## Analysis of Data Captured using Ratings Template

1. When a user submits a rating by clicking the Submit button on the Web popup, a *Rating Submitted* event is triggered.
2. This event is available across the CleverTap platform. It helps in creating targeted segments for users to engage them on various channels based on their rating feedback. 
3. This event can also be used in Analytics for the analysis of data captured through the **Ratings** campaigns. 

Listed below are the steps to perform analysis for some of the key metrics:

### View Ratings Trend

To view the *Trend* for the number of ratings submitted and Frequency histogram:\
   i. Navigate to *Analytics > Events*.\
   ii. From the event dropdown, search for *Rating Submitted* event and click on **View details**.\
   iii. Under the *Trends & Properties* tab, one can view the trend for the number of ratings submitted on a Daily, Weekly, and Monthly basis.\
  iv. Select Event property as *Ratings* to get a histogram view of the rating scale.

### Analyze Average Rating Trends

To analyze the Average Rating trends:\
  i. Navigate to *Analytics > Trends*\
  ii. Select the *Rating Submitted event* > *+Summarize by* “User Rating” property and click on **View Trend**\
  iii. Navigate to the *Properties* tab and select *Average of property value* from the *View* dropdown.\
  iv. You can also analyze the trend of Average Rating on a Daily, Weekly, and Monthly basis.

> 📘 Pinning Reports to Dashboards
>
> One can also pin the reports or specific trend charts to a custom dashboard using the pin icon available at the extreme right for monitoring the data at regular intervals.

### Analyze Comments

To view and analyze the Comments received:

   i. Navigate to *Analytics* > *Events*\
   ii. Select the *Rating Submitted event*\
   iii. To filter the data at a campaign level, add the *Campaign id* filter as show below:

<Image title="campaign id.png" alt={2544} border={true} src="https://files.readme.io/edf2849-campaign_id.png">
  Rating Submitted Data
</Image>

iv. Click *View details*.\
v. Navigate to *Trend & Properties*\
vi. From the Event property dropdown, select *Comment*\
vii. Select the grid view to view all the comments received in tabular format.

<Image title="comments received.png" alt={2164} className="border" border={true} src="https://files.readme.io/466a94a-comments_received.png" />

viii. To download the comments, Click **Export as CSV** button available below the grid icon.
