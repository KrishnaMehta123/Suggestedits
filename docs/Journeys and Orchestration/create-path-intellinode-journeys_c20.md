---
title: Create an IntelliNode Journey
excerpt: >-
  Understand how to create variations in journeys using IntelliNode goals and
  paths.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
---
# Overview
IntelliNode is an experiment that uses two or more variations of a journey; statistical analysis is used to determine which path works better for the desired conversion goal. You can test different paths for user journeys, to test which performs well, and repeat it for any future engagements.
As a marketer, you can let the CleverTap Decision Making systems find the best path or manually go through each stat to arrive at a conclusion.

# IntelliNode

1. Create a Journey. 
2. Drag and drop the **IntelliNode** under *Controllers* in the left pane to the canvas. 
3. Click **IntelliNode** in the canvas to begin charting paths for the journeys.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/6d409bd-Click_A_B.jpg",
        "Click_A_B.jpg",
        1280,
        585,
        "#f5f8f8"
      ],
      "border": true,
      "sizing": "80"
    }
  ]
}
[/block]
4. Give your IntelliNode a name and select whether you want the tests to be configured manually or automatically.
Automatic Mode allows the CleverTap intelligent decision-making system to kick in, where the initial distribution across all setup paths would be equal but change based on individual path performance. The system will automatically assign a higher distribution to better-performing paths by reevaluating performance for each path every few minutes. 
Manual Mode gives the driving wheel to the Marketer, where you can choose the distribution across paths at any given point in time.
5. Click *+Path* to add paths to a user journey.
You may set up to 7 different paths for the user journeys, either in the automated or the manual mode.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/1d83a47-A_B_Test_path.jpg",
        "A_B_Test_path.jpg",
        746,
        573,
        "#f6f7f3"
      ],
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]
##IntelliNode Goals
You may define the IntelliNode goals and align them to the different paths, you've created.
1. Enter the **IntelliNode goal name**.
2. Edit the events for which you have defined the goals. 
 a. Click *New segment* to configure more than one segment for a goal.
3. Click **+IntelliNode Goal** to add more goals.
4. Click *Save & Close*
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/ef7f3c3-A_B_Goal.jpg",
        "A_B_Goal.jpg",
        367,
        315,
        "#f7f7fb"
      ],
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]
##Configure Paths
1. Click the path you want to configure
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/331c8f7-Click_Paths.jpg",
        "Click_Paths.jpg",
        454,
        241,
        "#f1f6ef"
      ],
      "sizing": "80",
      "border": true
    }
  ]
}
[/block]
2. Configure the path including the sleep time, and delay, if required.
Delay is the time delay between an event occurrence and the path action.
Sleep time is the time taken for subsequent path actions.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/0c3a709-Configure_path.jpg",
        "Configure_path.jpg",
        522,
        240,
        "#e8f4ef"
      ],
      "border": true
    }
  ]
}
[/block]
##Publish
Click **Publish**. This makes the journey live.