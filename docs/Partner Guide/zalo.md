---
title: Zalo
excerpt: Understand how to integrate Zalo with CleverTap.
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: index
next:
  description: ''
---
# Overview

[Zalo](https://zalo.me/pc) is a popular messaging app in Vietnam that provides users with fast, stable, convenient, and private connections anytime, anywhere. Integrating Zalo and CleverTap allows you to enhance user engagement, marketing efforts, or analytics for businesses using both platforms.

Zalo's Official Account (OA) supports various reply actions. Below is a detailed view of each capability.

* Text
* Image
* Attachment
* Buttons
* Quick Replies

# Prerequisites For Integration

The table below lists the prerequisites for Zalo and CleverTap integration: 

<Table align={["left","left"]}>
  <thead>
    <tr>
      <th>
        Requirements
      </th>

      <th>
        Description
      </th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>
        **[Zalo App](https://developers.zalo.me/createapp)**
      </td>

      <td>
        The Zalo App contains the settings for your OA.
      </td>
    </tr>

    <tr>
      <td>
        **[Zalo Official Account (OA)](https://oa.zalo.me/manage/oa?option=create)**
      </td>

      <td>
        A Zalo OA is used as your bot's identity. People who chat with your app see the OA name and the OA profile picture.
      </td>
    </tr>

    <tr>
      <td>
        **User ID**
      </td>

      <td>
        You must have a **user\_id** to send messages on OA. Once a user interacts and subscribes to OA, a **user\_id** is created. This user\_id can be sent to CleverTap as a custom user property in string format.  

        For more information, refer to the following links:  

        * [https://developers.zalo.me/docs/api/official-account-api/quan-ly-thong-tin-official-account/lay-danh-sach-nguoi-quan-tam-post-5133](https://developers.zalo.me/docs/api/official-account-api/quan-ly-thong-tin-official-account/lay-danh-sach-nguoi-quan-tam-post-5133)  
        * [https://developers.zalo.me/docs/api/official-account-api/quan-ly-thong-tin-official-account/lay-thong-tin-nguoi-quan-tam-post-5129](https://developers.zalo.me/docs/api/official-account-api/quan-ly-thong-tin-official-account/lay-thong-tin-nguoi-quan-tam-post-5129)
      </td>
    </tr>

    <tr>
      <td>
        **[OA Access Token](https://developers.zalo.me/docs/api/official-account-api/phu-luc/official-account-access-token-post-4307)**
      </td>

      <td>
        These access tokens provide permission to APIs that read, write, or modify the data belonging to an OA. You must obtain a user access token and **manage\_pagespermission** to obtain a page access token. Once you have the user access token, you get the page access token via the Graph API.
      </td>
    </tr>

    <tr>
      <td>
        **[App Review and Approval](https://oa.zalo.me/home/faq/chinh-sach-ve-official-account-list7)**
      </td>

      <td>
        When ready to release your OA to the public, you must submit it to Zalo for review and approval. This review process lets you ensure your OA abides by the policies and functions as expected before making it available to everyone on Zalo.
      </td>
    </tr>
  </tbody>
</Table>

# Integrate Zalo with CleverTap

This process involves the following three steps:

1. [Configure Zalo Official Account](https://staging.docs.user.clevertap.net/docs/zalo#configure-zalo-official-account).
2. [Set Up Webhook in CleverTap Dashboard](https://staging.docs.user.clevertap.net/docs/zalo#set-up-webhook-in-clevertap-dashboard).
3. [Preview and Test Your Zalo Campaign with Webhook](https://staging.docs.user.clevertap.net/docs/zalo#preview-and-test-your-zalo-campaign-with-webhook).

## Configure Zalo Official Account

This section describes the steps to configure your Zalo Official Account: 

1. [Collect Your User ID](https://staging.docs.user.clevertap.net/docs/zalo#collect-your-user-id)
2. [Send User ID to Clevertap as a Custom User Property](https://staging.docs.user.clevertap.net/docs/zalo#send-user-id-to-clevertap-as-a-custom-user-property)

### Collect Your User ID

To send messages on Zalo OA, you must collect your *user\_id*. It identifies your users and interacts with them consistently. Zalo OA creates an identifier any time you message a follower or when a customer messages you.

When a user sends a message or follows your Official Account (OA), their user ID is included in the *sender.id*/*follower.id* property of the webhook event. This helps your OA identify who performed the action.

**Message Event**

```json
{
    "app_id": "360846524940903967",
    "sender": {
        "id": "246845883529197922"
    },
    "user_id_by_app": "552177279717587730",
    "recipient": {
        "id": "388613280878808645"
    },
    "event_name": "user_send_text",
    "message": {
        "text": "message",
        "msg_id": "96d3cdf3af150460909"
    },
    "timestamp": "154390853474"
}
```

| Parameters        | Description |
| :---------------- | :---------- |
| app\_id           |             |
| sender            |             |
| id                |             |
| user\_id\_by\_app |             |
| recipient         |             |
| event\_name       |             |
| message           |             |
| text              |             |
| msg\_id           |             |
| timestamop        |             |

**Follow Event**

```json
{
  "oa_id": "388613280879808645",
  "follower": {
    "id": "24684588352919792"
  },
  "user_id_by_app": "552172779717587730",
  "event_name": "follow",
  "source": "oa_profile",
  "app_id": "36084652489903967",
  "timestamp": "154397978274"
}

```

| Parameters        | Description |
| :---------------- | :---------- |
| oa\_id            |             |
| follower          |             |
| id                |             |
| user\_id\_by\_app |             |
| event\_name       |             |
| source            |             |
| app\_id           |             |
| timestamp         |             |

Whenever you send a message, their *user\_id* is included in the *recipient.id* property of the request to identify who should receive the message.

Once you are confident that you are receiving the *user\_id*, send it to CleverTap as a custom attribute.

### Send User ID to CleverTap as a Custom User Property

Coordinate and share this with your developer to send the `user_id` to CleverTap as a [custom user property](https://developer.clevertap.com/docs/concepts-user-profiles). The `user_id` is a string that you can access by making an API call.

## Set Up Webhook in CleverTap Dashboard

To set up your first CleverTap webhook:

1. Navigate to **Settings** > **Engage** > **Channels** > **Webhooks**.
2. Click **+ Add Webhook**.

   <Image title="Set up a Webhook from CleverTap dashboard" alt={2858} align="center" className="border" border={true} src="https://files.readme.io/1967920-Add_Webhook.png" />
3. Configure the webhook template by adding the following details: 

   <Image align="center" className="border" width="95% " border={true} src="https://files.readme.io/0b2ae19-CreateWebhook.jpg" />

   | Field               | Description                                                                                                                                                                       |
   | :------------------ | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | Name                | Enter the nickname for your webhook to identify the webhook uniquely.                                                                                                             |
   | Destination URL     | Enter the Zalo URL. Check [Step 4](https://staging.docs.user.clevertap.net/docs/zalo#:~:text=To%20get%20a%20destination%20URL%20for%20sending%20Zalo%20messages%20to%20users%3A). |
   | Method              | Select the *POST* method from the dropdown.                                                                                                                                       |
   | Basic Authorization | Enable this option.                                                                                                                                                               |
   | Username            | @Parth: What will be the username?                                                                                                                                                |
   | Password            | Enter the password as \<API Token>\. To obtain the API token, refer to [Generating a new API token](https://support.zendesk.com/hc/en-us/articles/4408889192858).                 |
4. To get a destination URL for sending Zalo messages to users: 

   1. Navigate to [Zalo API Explorer](https://developers.zalo.me/tools/explorer/1800875745710821035).
   2. Select an application associated with your OA and use the dropdown to generate access tokens for your OA.

      <Image align="center" className="border" width="95% " border={true} src="https://files.readme.io/b59205f-APIExplorer.jpg" />
   3. Copy the destination URL and paste it under the **Destination URL** on the CleverTap dashboard.

      <Image align="center" className="border" width="95% " border={true} src="https://files.readme.io/0b2ae19-CreateWebhook.jpg" />
5. Click **Create**. 

## Preview and Test Your Zalo Campaign with Webhook

To preview and test your Zalo campaign with webhook: 

1. Go to *Channels* > *Webhook*. 
2. Under *Type*, select **One time**.
3. Under *When*, select the following and click **Continue**: 
   * *Message type* as **One time** and 
   * *Webhook start date and time* as **Now**.  
4. Under *Who*, select the existing segment or create your new segment. Click **Continue**.
5. Filter the users by common properties. For example, the *user\_id* user property is set as *2525951653789073307*. Click **Continue**. 
6. Under *What*, copy and paste the custom JSON snippet in *Custom Body*.  [@Parth: Could you provide the custom JSON snippet used here?]
7. Click **Deploy Webhook**. 
8. Enter a campaign name and click **Save**. 
9. Under Webhook stats, you can check the conversion.
