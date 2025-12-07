---
title: Create an IntelliNODE Journey_WIP
excerpt: >-
  Understand how to create variations in journeys using IntelliNODE goals and
  paths.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
#Overview

You can have multiple variations in an IntelliNODE journey. This allows you to run multiple A/B tests to check the journey's success and test your assumptions. 

# Create an IntelliNODE Journey

To create an IntelliNODE journey:
1. Create a new Journey. 
2. Drag and drop **IntelliNODE** from the *Controllers* section to create an IntelliNODE journey. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f6e2d1d-Intellinode_journey_drag_drop_.gif",
        "Intellinode_journey_drag_drop .gif",
        1392,
        672,
        "#000000"
      ],
      "border": true
    }
  ]
}
[/block]
3. Click **IntelliNODE** in the canvas to set up the experiment.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d3be1aa-InteliNODE_Set_Up.png",
        "InteliNODE Set Up.png",
        1514,
        1218,
        "#000000"
      ],
      "border": true,
      "sizing": "smart"
    }
  ]
}
[/block]
4. Enter a name for the  IntelliNODE and select whether you want the experiments configured manually or automatically. We recommend entering a simple name you can remember, such as *abandoned cart experiment*. 
  * Automated Mode: This mode handles the distribution of qualifying users across all the connected paths. All paths start with equal distribution. However, the system automatically assigns a higher distribution to better-performing paths by re-evaluating the performance of each path every five minutes. The IntellNODE goal is used to determine the performance of each path. 
  * Manual Mode: This mode gives you control over the user distribution for each path. You can monitor the performance of your experiment and then change the distribution percentages of each path in the live journey. 

[block:callout]
{
  "type": "info",
  "title": "Switching between Automated and Manual Modes",
  "body": "You cannot switch modes in an IntelliNODE *after* publishing the journey."
}
[/block]
5. Click **+Path** to add paths to a user journey.
You can add up to seven paths for the user journeys in the automated or manual mode.

##IntelliNODE Goals

An IntelliNODE goal is common for all the paths. The goal is used to calculate the conversion percentage. 

In automated mode, this conversion percentage determines the user distribution. To set up an IntelliNODE goal:

1. Enter the **IntelliNODE goal name**. The goal name must be easy to identify, for example, *cart abandon experiment*.
2. Define the preferred user action by using events and filters.
3. Click **+IntelliNODE Goal** to add more goals. You can add up to 3 goals.
4. Click *Save & Close* to save the goal. 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/5266944-InteliNODE_Goals.png",
        "InteliNODE Goals.png",
        1540,
        2052,
        "#000000"
      ],
      "sizing": "smart",
      "border": true
    }
  ]
}
[/block]
##Publish
Click **Publish** to make the journey live.
[block:callout]
{
  "type": "info",
  "title": "Distribution changes in a manual mode",
  "body": "For manual mode, only the latest ten edit logs are available."
}
[/block]
Monitor the [IntelliNODE stats](https://docs.clevertap.com/docs/intellinode-stats) to check if your journey is progressing as planned.

# Automated vs. Manual IntelliNODE

The automated IntelliNODE does the heavy lifting for you. It verifies the conversion rate every five minutes and adjusts the user distribution accordingly. The user distribution is eventually shifted in favor of the best-performing path. However, the other paths still receive some user distribution to account for seasonality. This way, you are insured against any change in user behavior. You can stop the experiment at any moment by declaring a path as the winner. The winning path is then utilized to engage *all* your users. 

The manual IntelliNODE gives you total control over user distribution. You can monitor the experiment's performance and change the user distribution for each path in a live journey.