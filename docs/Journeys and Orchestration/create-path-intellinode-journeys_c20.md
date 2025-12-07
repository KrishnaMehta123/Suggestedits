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

IntelliNode is an experiment that uses two or more variations of a journey; statistical analysis is used to determine which path works better for the desired conversion goal. You can test different paths for user journeys, to test which performs well, and repeat it for any future engagements.\
As a marketer, you can let the CleverTap Decision Making systems find the best path or manually go through each stat to arrive at a conclusion.

# IntelliNode

1. Create a Journey. 
2. Drag and drop the **IntelliNode** under *Controllers* in the left pane to the canvas. 
3. Click **IntelliNode** in the canvas to begin charting paths for the journeys.

<Image title="Click_A_B.jpg" alt={1280} className="border" width="80%" border={true} src="https://files.readme.io/6d409bd-Click_A_B.jpg" />

4. Give your IntelliNode a name and select whether you want the tests to be configured manually or automatically.\
   Automatic Mode allows the CleverTap intelligent decision-making system to kick in, where the initial distribution across all setup paths would be equal but change based on individual path performance. The system will automatically assign a higher distribution to better-performing paths by reevaluating performance for each path every few minutes.\
   Manual Mode gives the driving wheel to the Marketer, where you can choose the distribution across paths at any given point in time.
5. Click *+Path* to add paths to a user journey.\
   You may set up to 7 different paths for the user journeys, either in the automated or the manual mode.

<Image title="A_B_Test_path.jpg" alt={746} className="border" width="80%" border={true} src="https://files.readme.io/1d83a47-A_B_Test_path.jpg" />

## IntelliNode Goals

You may define the IntelliNode goals and align them to the different paths, you've created.

1. Enter the **IntelliNode goal name**.
2. Edit the events for which you have defined the goals.\
   a. Click *New segment* to configure more than one segment for a goal.
3. Click **+IntelliNode Goal** to add more goals.
4. Click *Save & Close*

<Image title="A_B_Goal.jpg" alt={367} className="border" width="80%" border={true} src="https://files.readme.io/ef7f3c3-A_B_Goal.jpg" />

## Configure Paths

1. Click the path you want to configure

<Image title="Click_Paths.jpg" alt={454} className="border" width="80%" border={true} src="https://files.readme.io/331c8f7-Click_Paths.jpg" />

2. Configure the path including the sleep time, and delay, if required.\
   Delay is the time delay between an event occurrence and the path action.\
   Sleep time is the time taken for subsequent path actions.

<Image title="Configure_path.jpg" alt={522} className="border" border={true} src="https://files.readme.io/0c3a709-Configure_path.jpg" />

## Publish

Click **Publish**. This makes the journey live.
