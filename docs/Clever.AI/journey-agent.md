---
title: Journey Agent
deprecated: false
hidden: false
metadata:
  robots: index
---
Journey Agent allows you to create customer journeys using natural language prompts. Describe your goal, for example, “Create a re-engagement journey for inactive users”, and the system automatically converts it into a structured journey workflow.

<Callout icon="📘" theme="info">
  #### Private Beta

  Currently, this feature is released in Private Beta. To gain access, contact your Customer Success Manager.
</Callout>

Creating a journey using Journey Agent includes the following four key stages:

1. **AskAI**    
   Enter your journey objective in the Build with AI input field. For example, “Create a re-engagement journey for users inactive for 30 days.”
2. **Journey Builder**
   The system interprets your prompt and generates a visual journey with predefined triggers, actions, and conditions. You can modify these elements directly in the builder.
3. **Journey Overview**
   Review the generated journey to confirm the audience reach, key touchpoints, and engagement logic.
4. **Launch Journey**
   Once the workflow looks correct, click Publish to activate your journey. You can monitor its performance later in the Journey Dashboard.

<Image align="center" border={true} caption="Journey Agent" src="https://files.readme.io/f1f588e1e1b372711dd2e462d76616677d404ca2063b6580e19422ca7f2ba1c4-Journey_Using_Prompts_-_Overview.gif" />

# Create Journey Using Prompts

To create a journey using prompts, perform the following steps:

1. Go to _Journeys_ and click **+ Journey**.
2. Select _Build with AI_ if you want to create your journey using text prompts or select _Build Manually_ to create your journey from scratch.
3. In the AskAI prompt input field, enter your journey description. For example, “Create a win-back journey for users who haven’t opened the app in 14 days.” The system will generate a visual flow with:  

   * Entry: the event or condition that starts the journey (for example, Inactivity > 14 days).
   * Actions: Users receive a Push Notification. 

   <Image align="center" border={true} caption="Sample Winback Journey Using Prompts" src="https://files.readme.io/9d48134853b1d30c1845858622a59f759daa8de7d20c4a35ddf545e730fc8ad3-Winback_Journey_using_Prompts.gif" />
4. Edit or rearrange nodes as needed using drag-and-drop. For example, you can build up on this journey by sending a follow-up message to users who do not engage with the Push Notification. And for those who click the notification, they receive a "Welcome Back" message.  

   <Image border={false} />
5. Click **Publish** once you have reviewed your journey and are ready to activate your journey.

<br />
