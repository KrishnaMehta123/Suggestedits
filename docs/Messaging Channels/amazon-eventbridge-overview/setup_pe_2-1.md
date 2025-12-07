---
title: Setup_PE_2
excerpt: Learn how to set up Amazon Eventbridge to send event data to Amazon service
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Integrate EventBridge with CleverTap

This process involves the following three steps:

1. [Find Amazon EventBridge Event Source Details](doc:setup_pe_2-1#find-amazon-eventbridge-event-source-details).
2. [Configure CleverTap Event Source](doc:setup_pe_2-1#configure-clevertap-event-source).
3. [Associate Event Source with Designated Event Bus in AWS Console](doc:setup_pe_2-1#associate-event-source-with-designated-event-bus-in-aws-console).

## Find Amazon EventBridge Event Source Details

To find the event source details:

1. Navigate to Amazon EventBridge Partners from the Amazon EventBridge dashboard.
2. Click **Set up** under the CleverTap partner listing. The _Set up event source_ page opens.
3. Click **Copy** to copy your AWS account number to your clipboard and save it. You will require these details for configuring the CleverTap dashboard.

## Configure CleverTap Event Source

To configure CleverTap Event Source:

1. Log in to your CleverTap account and navigate to the _Settings_ > _Partners_ page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/2685d0f-Navigate_to_Partners_page.png",
        "Navigate to Partners page.png",
        2854
      ],
      "border": true
    }
  ]
}
[/block]

2. Hover on the _Amazon EventBridge_ icon and click **Integrate**. The _Integrate raw data partner - Amazon EventBridge_ popup opens on the right side of the screen.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/a1bb7e6-Click_Integrate.png",
        "Click Integrate.png",
        2400
      ],
      "border": true
    }
  ]
}
[/block]

3. Enter the following Amazon service details and click **Integrate**:

| <p>Field</p>            | <p>Description</p>                                                                                                                                                                                                                            |
| :---------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Partner Nickname</p> | <p>Enter the <em>Nickname</em> for your integration.</p>                                                                                                                                                                                      |
| <p>AWS Account ID</p>   | <ul><li>Enter the AWS account number obtained in <em>Step 3</em> of <a href="">Find Amazon EventBridge Event Source Details</a>.</li><li>This user property is used as an identifier when sending event data to Amazon EventBridge.</li></ul> |
| Region                  | The AWS account region. The events are sent to the selected region.                                                                                                                                                                           |

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d374259-Integrate_raw_data_partner_-_Amazon_EventBridge.png",
        "Integrate raw data partner - Amazon EventBridge.png",
        2394
      ],
      "border": true
    }
  ]
}
[/block]

After successful integration, the _Integrated_ tag displays against _Amazon EventBridge_ on the _Partners List_ page.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/32b704a-Integrated_tag.png",
        "Integrated tag.png",
        2852
      ],
      "border": true
    }
  ]
}
[/block]

## Associate Event Source with Designated Event Bus in AWS Console

To establish an event connection to Amazon EventBridge, your CleverTap event source must be associated with the event bus in Amazon EventBridge. You can now see the CleverTap event source, created in _Step 3_ of [Configure CleverTap Event Source](doc:setup_pe_2-1#configure-clevertap-event-source),  
under the _Partner_ events sources on the Amazon EventBridge dashboard. To associate the event source with the designated event bus in the AWS console:

1. Select the event source name and associate it with an event bus. 
2. After establishing the connection, set your rules and targets for Amazon EventBridge to redirect events to an AWS service. For more information, refer to the [Amazon EventBridge documentation](https://docs.aws.amazon.com/eventbridge/index.html).