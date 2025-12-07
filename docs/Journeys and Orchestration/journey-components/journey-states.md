---
title: Journey States
excerpt: >-
  Learn about different Journey States in CleverTap, which provide insights into
  user engagement and behavior throughout their interaction with your
  application.
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

Journey States in CleverTap refer to the distinct phases a user experiences within an automated Journey. Each state is defined by unique characteristics determining how and when users enter, progress through, or exit the Journey. These states offer valuable insights into user behavior, enabling marketers to monitor engagement and optimize workflow efficiency.

The following illustration and table give a quick overview of key aspects for each journey state:

- User Entry
- User Movement
- Possible Next Actions
- Possible Next States

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/00c2a2b32dc91b10ab38ae01e2438ec3a5dd20f43d29a2452d28d63059eeff59-Journey_states_flow.png",
        "",
        "Journey States"
      ],
      "align": "center",
      "sizing": "90% ",
      "border": true,
      "caption": "Journey States"
    }
  ]
}
[/block]


| State Name | User Entry                                                             | User Movement                                                     | Possible Next Actions      | Possible Next States        |
| :--------- | :--------------------------------------------------------------------- | :---------------------------------------------------------------- | :------------------------- | :-------------------------- |
| Draft      | Not Applicable                                                         | Not Applicable                                                    | Edit, Save, Publish, Clone | Scheduled, Running          |
| Scheduled  | Not Applicable                                                         | Not Applicable                                                    | Edit, Clone, Pause, Stop   | Running, Paused, Stopped    |
| Running    | Users enter the Journey as per the entry criteria                      | Users move ahead in the Journey as per the flow after qualifying. | Edit, Clone, Pause, Stop   | Paused, Stopped, Completed  |
| Paused     | User entry is paused                                                   | Users keep moving inside the journey                              | Edit, Clone, Resume, Stop  | Running, Stopped, Completed |
| Completed  | User entry is marked completed, and users can no longer qualify        | Users keep moving inside the journey                              | Clone, Stop                | Stopped                     |
| Stopped    | User entry is stopped, and users can no longer qualify for the Journey | Users no longer move inside the Journey                           | Clone                      | None                        |

 The current status of the Journey is displayed under the _Journeys_ list page. After the Journey is published, you can modify the following: the _What_ section, the Email or SMS provider, and the user distribution for the IntelliNODE journey split in manual mode. Let us understand these states in detail.

# Draft State

The Draft State in CleverTap refers to a Journey created but not published. Any unsaved changes in this state may be lost unless explicitly saved. If you have an existing unsaved Journey in the cache and choose to create a new Journey, CleverTap provides the option to either start a fresh Journey or restore the cached Journey for further editing.

If you restore the cached Journey, the most recent version saved in your browser cache loads, enabling you to continue editing from where you stopped. The cache is specific to each user and depends on the web browser, ensuring that only the user who created the Journey can access it while preventing accidental data loss.

The _Created By_ and _Published By_ columns on the Journeys List page identify the users responsible for creating and publishing the Journey. The _Created By_ column identifies the user who creates the Journey; however, the _Published By_ column denotes the user who publishes it, transitioning the Journey from _Draft_ to _Scheduled_ or _Running_.

# Scheduled State

The _Scheduled_ state indicates that the journey is set to go live in the future but is not currently editable except for the _What_ section. The following table describes the key difference between the Past Behavior and Live Behavior Journeys in the Scheduled state:

| **Feature**                | **Past Behavior Setup**                                                                                        | **Live Behavior Setup**                                                                                     |
| -------------------------- | -------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| **Qualification Criteria** | Based on **past actions** or **custom lists**.                                                                 | Based on **real-time user actions** or **inactivity**.                                                      |
| **Entry Timing**           | **At a fixed time**.                                                                                           | **At a fixed time**.                                                                                        |
| **Trigger Type**           | Static triggers based on predefined events.                                                                    | Dynamic triggers that act as soon as criteria are met.                                                      |
| **Use Case Focus**         | Re-engagement or follow-ups based on past activities. For example, targeting users who checked out last month. | Real-time engagement or retention campaigns. For example, sending a cart abandonment reminder in real-time. |

In this state, users start to qualify for the journey on publish or at a scheduled time. As a result, no user will qualify for the journey. If the Journey is stopped in the _Scheduled_ state, it will not start at the scheduled time, and no users will qualify for the journey.

# Running State

The _Running_ state indicates that the journey is active and the users execute actions as defined. In this state, users enter the Journey as they qualify and move ahead in the Journey as per the flow after qualifying (refer to the following GIF).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5aa5ea778cb2e4c2a73b283535a56b64413f776a1ca3379792ba2b4766364f3b-Running.gif",
        "",
        "Running State"
      ],
      "align": "center",
      "border": true,
      "caption": "User Entry and Movement in Running State"
    }
  ]
}
[/block]


As users move through the Journey nodes (for example, receiving a message, meeting a condition, or dropping off), the stats are updated immediately in the dashboard. The date range selection in the calendar widget directly influences the Node stats. Consider an example where the Journey running from Jan 1–Jan 10 sends push notifications to users. On Jan 5, you use the calendar widget to filter data for Jan 1–Jan 4. The Node stats update to reflect only the number of users who entered, dropped off, or converted during that time frame. Always ensure you are analyzing the correct time frame. For nodes with scheduled actions (for example, if a campaign is scheduled to run after two days), stats are updated only when those actions are triggered.

# Paused State

The _Paused_ state indicates that the already qualified users or the users who have entered the journey continue to advance in the journey. However, no new users qualify for the journey until it resumes (refer to the following GIF). For example, consider a Journey targeting users who abandon their cart without completing a purchase within 30 minutes. If you pause the Journey, users already qualified continue to progress and receive the notifications as per the Journey setup, such as receiving a discount after 24 hours, while new users who meet the criteria during the pause do not enter. Once the Journey resumes, new users qualify again based on the cart abandonment trigger. Existing user progress remains unaffected by the paused period.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/8f53f43f6d2bf593957d3fd51ab66753c3d0a36009497ab9f6a31af58422c7c9-Paused.gif",
        "",
        "Paused State"
      ],
      "align": "center",
      "border": true,
      "caption": "User Entry and Movement in Paused State"
    }
  ]
}
[/block]


# Stopped State

The _Stopped_ state indicates that the journey has been permanently deactivated. Users in the journey do not progress further, and their entry is halted (refer to the following GIF). The users systematically exit from the journey over a period of 30 days. The journey cannot be edited once stopped.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d37e56e4b883fcc1cbf6eaf85b1ba34bb3f4c462b274b7f6528058564920684b-Stopped.gif",
        "",
        "Stopped State"
      ],
      "align": "center",
      "border": true,
      "caption": "User Entry and Movement in Stopped State"
    }
  ]
}
[/block]


# Completed State

The _Completed_ state signifies that the user entry is marked complete. The already qualified users continue to move ahead and move out of the journey once they all get timed out (refer to the following GIF).

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/854ba478e8cd88e48cda04e1e449cbf26cf26ebb353e680b83dbebbf24a8125e-Completed.gif",
        "",
        "User Enter and Movement in Completed State "
      ],
      "align": "center",
      "border": true,
      "caption": "User Entry and Movement in Completed State "
    }
  ]
}
[/block]