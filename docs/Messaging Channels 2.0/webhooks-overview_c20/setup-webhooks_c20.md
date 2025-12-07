---
title: Setup
excerpt: Setup Webhooks
deprecated: false
hidden: true
metadata:
  title: ''
  description: ''
  robots: noindex
next:
  description: ''
  pages:
    - type: link
      title: Create Webhooks
      url: https://docs.clevertap.com/docs/create-message-webhook_c20
    - type: link
      title: Personalize Webhooks
      url: https://docs.clevertap.com/docs/personalize-message-webhooks_c20
    - type: link
      title: Webhook Stats
      url: https://docs.clevertap.com/docs/webhooks-stats_c20
---
Webhooks send an HTTP API request with information about the user i.e event or user properties. 

To set up your first CleverTap webhook:

1. Navigate to **Settings** > *Engage* > **Channels** > **Webhooks**.
2. Click **+ Add Webhook**. 
3. Configure the webhook template.
4. Click **Save**.
5. Once you click *Save*, CleverTap sends the below payload to your configured endpoint. 
[block:code]
{
  "codes": [
    {
      "code": "{\n   \"is_test\":true,\n   \"targetId\":1234,\n   \"key_values\":{\n      \"key\":\"value\"\n   },\n   \"profiles\":[\n      {\n         \"Identity\":\"UserId\",\n         \"Email\":\"User@user.com\",\n         \"push_token\":\"Token\"\n      },\n      {\n         \"Identity\":\"UserId\",\n         \"Email\":\"User@user.com\",\n         \"push_token\":\"Token\"\n      },\n      {\n         \"Identity\":\"UserId\",\n         \"Email\":\"User@user.com\",\n         \"push_token\":\"Token\"\n      },\n      {\n         \"Identity\":\"UserId\",\n         \"Email\":\"User@user.com\",\n         \"push_token\":\"Token\"\n      },\n      {\n         \"Identity\":\"UserId\",\n         \"Email\":\"User@user.com\",\n         \"push_token\":\"Token\"\n      }\n   ]\n}",
      "language": "json"
    }
  ]
}
[/block]
6. Once your endpoint responds with an **HTTP status 200 OK**, CleverTap will save the template.
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c5ed2e7-Campaign_Webhooks_add_webhook_param.png",
        "Campaign_Webhooks_add_webhook_param.png",
        606,
        875,
        "#f6f7f9"
      ],
      "sizing": "smart",
      "border": true
    }
  ]
}
[/block]