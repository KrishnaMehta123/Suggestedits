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

```json
{
   "is_test":true,
   "targetId":1234,
   "key_values":{
      "key":"value"
   },
   "profiles":[
      {
         "Identity":"UserId",
         "Email":"User@user.com",
         "push_token":"Token"
      },
      {
         "Identity":"UserId",
         "Email":"User@user.com",
         "push_token":"Token"
      },
      {
         "Identity":"UserId",
         "Email":"User@user.com",
         "push_token":"Token"
      },
      {
         "Identity":"UserId",
         "Email":"User@user.com",
         "push_token":"Token"
      },
      {
         "Identity":"UserId",
         "Email":"User@user.com",
         "push_token":"Token"
      }
   ]
}
```

6. Once your endpoint responds with an **HTTP status 200 OK**, CleverTap will save the template.

<Image title="Campaign_Webhooks_add_webhook_param.png" alt={606} className="border" width="smart" border={true} src="https://files.readme.io/c5ed2e7-Campaign_Webhooks_add_webhook_param.png" />
