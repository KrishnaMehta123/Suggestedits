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
2. Click **Set up** under the CleverTap partner listing. The *Set up event source* page opens.
3. Click **Copy** to copy your AWS account number to your clipboard and save it. You will require these details for configuring the CleverTap dashboard.

## Configure CleverTap Event Source

To configure CleverTap Event Source:

1. Log in to your CleverTap account and navigate to the *Settings* > *Partners* page.

<Image title="Navigate to Partners page.png" alt={2854} className="border" border={true} src="https://files.readme.io/2685d0f-Navigate_to_Partners_page.png" />

2. Hover on the *Amazon EventBridge* icon and click **Integrate**. The *Integrate raw data partner - Amazon EventBridge* popup opens on the right side of the screen.

<Image title="Click Integrate.png" alt={2400} className="border" border={true} src="https://files.readme.io/a1bb7e6-Click_Integrate.png" />

3. Enter the following Amazon service details and click **Integrate**:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        <p>Field</p>
      </th>

      <th>
        <p>Description</p>
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        <p>Partner Nickname</p>
      </td>

      <td>
        <p>Enter the <em>Nickname</em> for your integration.</p>
      </td>
    </tr>

    <tr>
      <td>
        <p>AWS Account ID</p>
      </td>

      <td>
        <ul><li>Enter the AWS account number obtained in <em>Step 3</em> of <a href="">Find Amazon EventBridge Event Source Details</a>.</li><li>This user property is used as an identifier when sending event data to Amazon EventBridge.</li></ul>
      </td>
    </tr>

    <tr>
      <td>
        Region
      </td>

      <td>
        The AWS account region. The events are sent to the selected region.
      </td>
    </tr>
  </tbody>
</Table>

<Image title="Integrate raw data partner - Amazon EventBridge.png" alt={2394} className="border" border={true} src="https://files.readme.io/d374259-Integrate_raw_data_partner_-_Amazon_EventBridge.png" />

After successful integration, the *Integrated* tag displays against *Amazon EventBridge* on the *Partners List* page.

<Image title="Integrated tag.png" alt={2852} className="border" border={true} src="https://files.readme.io/32b704a-Integrated_tag.png" />

## Associate Event Source with Designated Event Bus in AWS Console

To establish an event connection to Amazon EventBridge, your CleverTap event source must be associated with the event bus in Amazon EventBridge. You can now see the CleverTap event source, created in *Step 3* of [Configure CleverTap Event Source](doc:setup_pe_2-1#configure-clevertap-event-source),\
under the *Partner* events sources on the Amazon EventBridge dashboard. To associate the event source with the designated event bus in the AWS console:

1. Select the event source name and associate it with an event bus. 
2. After establishing the connection, set your rules and targets for Amazon EventBridge to redirect events to an AWS service. For more information, refer to the [Amazon EventBridge documentation](https://docs.aws.amazon.com/eventbridge/index.html).
