---
title: Webhooks Stats
excerpt: View stats for your webhooks.
deprecated: false
hidden: false
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# View Statistics

You can view the statistics of your webhook from the *Campaign* list page.

<Image alt="Analyse Webhook Statistics" align="center" border={true} src="https://files.readme.io/444c57110eaa0b3a10df5c302430e3036788ca4c4372104e820cd1524e0f0be0-Webhooks_Trends.png">
  Analyse Webhook Statistics
</Image>

* **Webhooks streamed**  - Represents the total webhooks streamed to an endpoint.
* **Message Trend** - Represents performance trend for total webhooks streamed over a specific period of time (for example, daily, weekly, monthly) in a campaign. 

<Image alt="Webhook Streamed Errors" align="center" border={true} src="https://files.readme.io/b611a189acf231aad7f7e02531a5745d53354fcb4075ffb2fd09f09680ae2a98-Webhooks_Errors.png">
  Webhook Streamed Errors
</Image>

* **Errors**: It represents the count and reason for the webhooks that were not exported due to errors.

The following table lists the errors that may occur while delivering the webhook campaign:

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Error
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        Webhook dispatch error
      </td>

      <td>
        This error means that the webhook payload failed to deliver or dispatch to the specified target URL. This error occurs when CleverTap attempts to send the data to the webhook endpoint, but the delivery process encounters an issue, preventing successful transmission. The cause could be various reasons, such as:  

        <ul><li> Server unavailability </li><li> Incorrect URL </li><li> Network connectivity issues </li><li> Problems with the receiving server </li></ul>
      </td>
    </tr>

    <tr>
      <td>
        Invalid Webhook URL
      </td>

      <td>
        The provided URL for the webhook is not valid or properly formatted. When configuring a webhook in CleverTap, you must provide a correct and complete URL specifying the endpoint where the data should be delivered. If the URL is missing essential components, contains errors, or is not in the expected format, CleverTap cannot deliver the webhook payload.
      </td>
    </tr>
  </tbody>
</Table>
