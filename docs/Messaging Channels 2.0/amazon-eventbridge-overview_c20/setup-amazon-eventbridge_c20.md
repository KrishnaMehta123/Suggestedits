---
title: Setup
excerpt: Learn how to set up Amazon Eventbridge to send event data to Amazon service
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: >-
    Refer to the pages listed below to learn more about the following Amazon
    Eventbridge sections:
  pages:
    - type: link
      title: Create Message
      url: https://docs.clevertap.com/docs/create-message-amazon-eventbridge_c20
    - type: link
      title: Personalize Message
      url: >-
        https://docs.clevertap.com/docs/personalize-message-amazon-eventbridge_c20
    - type: link
      title: Amazon Eventbridge Campaign Stats
      url: https://docs.clevertap.com/docs/stats-for-amazon-eventbridge_c20
---
This process involves adding Amazon Eventbridge details to the CleverTap dashboard. To add the details to the CleverTap dashboard:

1. Log in to your CleverTap account.
2. Navigate to *Settings* > *Partners* > *Exports*. 

<Image title="Amazon unconnected.png" alt={1672} className="border" border={true} src="https://files.readme.io/034dcc7-Amazon_unconnected.png" />

3. Click the **Amazon** icon under the *Unconnected partners* section. The *Amazon* page is displayed.
4. Enter Amazon service details.

<Image title="EB config.png" alt={1180} className="border" border={true} src="https://files.readme.io/32bf8d8-EB_config.png" />

The details can be obtained by navigating to *Amazon EventBridge* > *Amazon EventBridge* Partners and then clicking **Set up** CleverTap partner listing of the Amazon dashboard.

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
        AWS Account ID
      </td>

      <td>
        This user property is used as an identifier when sending events data to Amazon Eventbridge.
      </td>
    </tr>

    <tr>
      <td>
        Region
      </td>

      <td>
        Select the AWS region from the **AWS region** dropdown list to receive events.
      </td>
    </tr>
  </tbody>
</Table>

5. Click **Save**. On clicking, the message "Your Amazon credentials saved successfully" is displayed.\
   Amazon is now displayed under Connected partners when you navigate to *Settings* > *Partners* > *Exports*.

<Image title="Amazon connected.png" alt={1392} className="border" border={true} src="https://files.readme.io/178732a-Amazon_connected.png" />
