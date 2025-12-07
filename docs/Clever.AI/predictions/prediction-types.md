---
title: 'Predictions: Types and Statuses'
excerpt: >-
  Explore the Predictions Dashboard to understand prediction types and their
  states.
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

This guide will help you navigate and master CleverTap’s Predictions feature. By understanding the different types of predictions and their statuses, you will gain crucial insights to manage your prediction models effectively.

# Types of Predictions

Let us begin by exploring the types of Predictions you encounter on your dashboard, each offering unique capabilities to enhance your decision-making process.

- [System Predictions](doc:prediction-types#system-predictions) 
- [Custom Predictions](doc:prediction-types#custom-predictions) 

## System Predictions

System predictions are ready-to-use predictions that we have created for use. They require minimal input and can be started right away. They estimate the likelihood of different outcomes or actions within a specified timeframe, such as retention, conversion, or app uninstall rates, with set goals. 

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/565d2c64e39cb744da5f8a869c515c9bb6a017b97ccceef673409dd1000fc61d-System_Predictions.png",
        "",
        "System Predictions"
      ],
      "align": "center",
      "border": true,
      "caption": "System Predictions"
    }
  ]
}
[/block]


The following four system predictions are available for your CleverTap account:

| Name                   | Description                                                                                           | Prediction on                                                            | Goal                              |
| :--------------------- | :---------------------------------------------------------------------------------------------------- | :----------------------------------------------------------------------- | :-------------------------------- |
| **Conversions**        | Use this to predict users who have a High likelihood to perform conversion events.                    | Active users in the last 60 days                                         | Account level conversion event    |
| **New User Retention** | Use this to predict users that have a High likelihood to engage with the app soon after installation. | Install the app or visited the website for the first time in last 7 days | App Launch or Web Session Started |
| **Retention**          | Use this to predict users likely to engage with the app over time.                                    | Active in the last 180 days                                              | App Launch or Web Session Started |
| **Uninstalls**         | Use this to predict users who have High likelihood to uninstall the app.                              | Active in the last 90 days                                               | Uninstalled Event                 |

## Custom Predictions

Custom predictions allow you to create Predictions based on specific goals and criteria relevant to your business needs. Unlike system-generated predictions, custom predictions allow you to define the target audience, set unique goal events, and specify the period for the prediction. These predictions focus on user behaviors or outcomes that matter most to your business, giving you more control and flexibility in forecasting future actions. 

You can identify custom predictions on the _Predictions_ page by their grayed-out icons, as shown below:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/f7c316d80e7e94a026c0d4ad84b5f5b1b709973d13753cd53e1acfe90401266b-Custom_Predictions.png",
        "",
        "Custom Predictions"
      ],
      "align": "center",
      "border": true,
      "caption": "Custom Predictions"
    }
  ]
}
[/block]


# Prediction Status

Prediction Status refers to the current state or progress of a prediction within the system. It helps understand whether the prediction is still being processed, active, etc. A Prediction has the following statuses:

[block:parameters]
{
  "data": {
    "h-0": "Status",
    "h-1": "Description",
    "0-0": "**Available**",
    "0-1": "The prediction is created and visible on the dashboard but not yet running. To begin generating insights, you need to click _Activate_. Once activated, the prediction moves to the _Processing_ status.",
    "1-0": "**Processing**",
    "1-1": "The prediction is currently running and being calculated. When you initiate the _ Activate _ action, it moves to the _Processing_ state and stays in that state until the system finishes processing the data.",
    "2-0": "**Active**",
    "2-1": "The prediction has finished processing and is now live, actively monitoring user behavior or events. It will remain in this state until manually stopped or the defined prediction period ends.",
    "3-0": "**Stopped**",
    "3-1": "The user has stopped the prediction. The prediction can transition to this state from the _Active_ state.  \n  \n**Note**: Once you stop a custom prediction, you cannot restart it."
  },
  "cols": 2,
  "rows": 4,
  "align": [
    "left",
    "left"
  ]
}
[/block]