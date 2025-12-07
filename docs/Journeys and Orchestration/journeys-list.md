---
title: Journeys List
excerpt: >-
  Learn how to understand and optimize your journeys with the Journeys List
  page.
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

The *Journeys List* page on the CleverTap Dashboard provides a comprehensive overview of all the Journeys created on the dashboard with detailed performance statistics. This section also allows you to search for and filter specific Journeys easily.

To access the *Journeys List* page, go to *Journeys* from the CleverTap Dashboard. 

<Image alt="All Journeys" align="center" border={true} src="https://files.readme.io/1a87ef280b5089665cd91d81dc3b344384bb00663cd969c2ab31601ce5c25b67-Journeys_List.png">
  Journeys List
</Image>

The following details are displayed for each journey::

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Field
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Journey Details
      </td>

      <td>
        Displays the Journey name and ID.
      </td>
    </tr>

    <tr>
      <td>
        Start Time
      </td>

      <td>
        Displays the date and time when the Journey state changed to *Running* and users started entering the Journey.
      </td>
    </tr>

    <tr>
      <td>
        Status
      </td>

      <td>
        Displays the current state of the Journey, such as Draft, Running, Paused, Completed, and Stopped. For more information, refer to [Journey States](doc:journey-states).
      </td>
    </tr>

    <tr>
      <td>
        Entry Type
      </td>

      <td>
        Specifies how users qualify for the Journey. They can qualify based on the Past behavior/ Custom list (actions they have performed or have been performing in the past) or Live behavior (as soon as they perform any action).
      </td>
    </tr>

    <tr>
      <td>
        Goals Met
      </td>

      <td>
        Displays the total number of users who completed the Journey goal(s) defined in the Journey, such as purchases, sign-ups, or other tracked events.
      </td>
    </tr>

    <tr>
      <td>
        Entered Users
      </td>

      <td>
        Displays the number of unique users who entered the Journey based on the entry criteria.
      </td>
    </tr>

    <tr>
      <td>
        Timed-Out Users
      </td>

      <td>
        Displays the total number of users who exited the Journey without achieving any defined goals because they exceeded the Journey timelines
      </td>
    </tr>

    <tr>
      <td>
        Rate
      </td>

      <td>
        Indicates the percentage of Goal Met.<li> If the goal exists, it is calculated as [(Number of users who met the goal/Total number of qualified users) * 100].</li><li>If the goal does not exist, it is calculated as \[(Number of users who exited last node/Total number of qualified users) \* 100.</li>  
      </td>
    </tr>

    <tr>
      <td>
        Created By
      </td>

      <td>
        Displays the email ID of the user who created the journey.
      </td>
    </tr>

    <tr>
      <td>
        Created On
      </td>

      <td>
        Displays the date on which the Journey was initially created.
      </td>
    </tr>

    <tr>
      <td>
        Published By
      </td>

      <td>
        Displays the email ID of the user who last published the Journey.
      </td>
    </tr>

    <tr>
      <td>
        Published On
      </td>

      <td>
        Displays the date on which the Journey was last published.
      </td>
    </tr>
  </tbody>
</Table>

# Filter Journeys

You can locate a specific journey from the *All Journeys* page with Journey Filters. By applying these filters, you can refine your search based on the following criteria: 

* Entry type
* Status
* Created by
* [Labels](doc:all-journeys#assign-label-to-journeys)
* IntelliNODE

You can apply quick filters directly from the top of the *All Journeys* page.

<Image alt="Quick Journey Filters" align="center" border={true} src="https://files.readme.io/e3ec5a9bc10fc9f9a62eef2849b3caf7afeaa9c18c4f479f51032b7f556131fb-Quick_Filters.png">
  Quick Journey Filters
</Image>

To filter journeys:

1. Go to *Journeys* from the CleverTap dashboard. The All Journeys page opens.
2. Click ![](https://files.readme.io/5b5d9b72cbf26494288be1890d39e0f976694b8b0694ce4690570d089b8f37ee-Filters_icon.png) icon. The *Filter Journeys* window opens on the right side.
3. Apply the required filters and click **Apply**. For example, if you want to look at the *Running* journeys with Entry type as *Past Behavior*.

<Image alt="Filter Journeys" align="center" border={true} src="https://files.readme.io/784386f188ca5af551ad2af7f35dd4410ac453de3d888d2da87779e4b837cc5e-Journey_Filters.gif">
  Filter Journeys
</Image>

You can also save your frequently used custom filters by clicking **Save Filter** from the *Filter Journeys* window.

# Assign Label to Journeys

Labels help categorize engagements with meaningful names or themes, making organizing, analyzing performance, and understanding user behavior across multiple journeys easier. Here are some of the examples for Journey Labels: 

* Onboarding: Group all Journeys related to new user onboarding.
* Re-engage: Categorize Journeys designed to re-engage users who have become inactive. 

**Key Benefits of Journey Labels**

* **Simplified Organization**: Use labels to group Journeys with similar objectives, themes, or target audiences.
* **Enhanced Analysis**: Leverage labels to track notifications and analyze Journey performance effectively.

To assign labels to the journeys:

1. Select the required journey from the *All Journeys* page.
2. Click ![](https://files.readme.io/88c31ba6baf35d426881cdf01b679b8b674eb6a0cb4c09610d2ecd9eda755e17-Labels_icon.png) icon. The *Add Label* popup opens.
3. Select the label you want to assign from the list and click **Add**.\
   To add a new label, type the desired name, select it, and click **Add**. (refer to the illustration below). 

<Image alt="Assign Journey Label" align="center" border={true} src="https://files.readme.io/a751d30f27d15be2f4f9dc356ee647cdfb896af5d45e19cb8ef91e778389f57f-Apply_Labels.gif">
  Assign Journey Label
</Image>

You can also utilize Journey Labels to analyze Journey performance from the *Analytics* section for the *Notifications Sent* event. This helps track the total number of notifications sent by Journeys tagged with specific labels, thereby gaining deeper insights into user segmentation and Journey effectiveness.

<Image alt="Analyze Journey Performance Using Journey Label" align="center" border={true} src="https://files.readme.io/e98166504d0616ed298894a4941be7406f7e5f2af93c9c05f1b2fdee521f3d92-Analyze_Journey_Performance_Using_Journey_Label.png">
  Analyze Journey Performance Using Journey Label
</Image>

This empowers you to analyze performance data more granularly and refine your Journey strategies based on actionable insights.
