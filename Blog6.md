# Bring AI to your life with Power Virtual Agents and Graph
Ever wondered **how to bring AI to your day-to-day work?** Our last post will focus on Power Virtual Agents, particularly how to build conversational BOTs with Microsoft Graph. We are going to return user's calendar meeting information through BOT interaction. Some extending ideas could be getting Planner or important email data. This post serves as **a foundation and an inspiration**. So **let's go** ahead and get into the content!

![image](https://user-images.githubusercontent.com/49314681/168832267-420be9e9-606c-494f-98d2-979b5277ca99.png)
(from https://www.youtube.com/watch?v=M_uiW2bjLxA)

## Objectives and Prerequisites
So why this content is important? I am sure much like myself, most of you are **inundated with a lot of information**, which is **spread across many services** like Email, Calendar, SharePoint, etc. In order to find the right focus from the disparate data, we can **bring this information together** by using **Power Virtual Agents** and **Graph**. 

Thus, our goal is to...
* **Introducing bots**, explaining where they are being used, and providing an overview of how Power Virtual Agents can be used to create bots
* **Reviewing the process for creating a bot** and how to work with the Power Virtual Agents user interface
* **Illustrating the process of publishing a bot** and successfully solving our problem

In order to get those objectives, **you should have**...
* Access to Power Virtual Agents
* Relevant [permissions](https://docs.microsoft.com/en-us/graph/api/calendar-list-events?view=graph-rest-1.0&tabs=http) including enabled delegation to access user calendar 

## Why Microsoft Power Virtual Agents in Education?
Microsoft Power Virtual Agents empowers teams to create powerful bots through a **guided, no-code graphical interface**. With Power Virtual Agents, we can **eliminate the gap between the subject matter experts and development teams** that are building the bots, and can reduce latency between teams recognizing an issue and updating the bot to address the issue. 

Each one of us wears **multiple hats at work** sometimes. For example, a university professor may be a lecturer, a researcher and a faculty staff for one semester! Hence, there could be a lot of different meetings and projects. **To efficiently and interactively navigate through information**, our chatbot would come to the field. It can **help to show a list and give suggestions**, just **like a personal assistant**. 

![image](https://user-images.githubusercontent.com/49314681/171876104-e8758ff1-1243-49ec-88e7-dd6133d3bce0.png)

(from https://iconscout.com/illustration/virtual-assistant-2130746)

Moreover, it includes the **following features to enhance your bot's functionality** to make it even **more powerful**:
* Initiate Microsoft Power Automate flows, which is being used in our following demo
* Pass conversations to live agents. Bots can be configured to pass conversations, including the context to live agents
* Automate topic creation. You can extract content from existing support pages, such as Frequently Asked Questions (FAQs)

## How to get started?
The first time that you **sign in** to Power Virtual Agents and create a new bot, a default environment is created. Unless specified otherwise, any additional bots will **be created in the default environment**. If additional environments are needed, such as for different regions, organizational needs, or other circumstances, they can be added through the [Microsoft Power Platform admin center.](https://docs.microsoft.com/en-us/power-platform/admin/create-environment/)

When in the admin center, you can **add environments by going to the Environments tab** and **selecting New** to open the new environment panel.

![image](https://user-images.githubusercontent.com/49314681/168820736-a8f205b3-b6fd-4a24-95d9-72f0750a36ee.png)

You can **create bots by selecting the bot icon** in the Power Virtual Agents interface. 

![image](https://user-images.githubusercontent.com/49314681/168820950-8396720a-d346-429c-98b4-c3c0c968f36c.png)

In the Create a new bot dialog box, **enter a name** for your bot. **Select Create to begin the bot-building process**, which can take up to **15 minutes** for the first bot that you create in an environment. 

![image](https://user-images.githubusercontent.com/49314681/168821078-fa692361-d82e-42c6-9ddb-d58b168fa038.png)

You will **define any additional topics by selecting Topics** in the side navigation pane and then selecting New topic at the top of the page. Each topic that you define should include some trigger phrases. Trigger phrases are examples of text such as questions or utterances that teach the bot when to respond with this dialog. 

![image](https://user-images.githubusercontent.com/49314681/168821351-1c63ce98-f93c-4e8c-bf2d-a5181617f128.png)

After you have **saved your topic**, you can define how customers are guided through their conversational interaction with the topic. You can define the path by selecting Go to authoring canvas. The **authoring canvas** is a graphical dialog tree editor that allows you to define bot responses and the overall bot conversation. When the canvas loads, the c**onversation will consist of two nodes**:
* The trigger phrases that will initiate the topic.
* The initial message that will be provided to the user.

![image](https://user-images.githubusercontent.com/49314681/168821699-1efbf2a1-955f-4c0f-8b83-bd025e862a70.png)

**Conversation nodes help define the path that the conversation will take**. Conversation nodes can display messages, ask questions, or run actions. You can add these nodes by selecting the plus sign (+) below the node. For example, if you want to provide store hours based on where the customer lives, you would add an Ask a question node to identify which store location that they want the hours for.

The following image shows the Ask a question node being used to ask the customer which store location they want the hours for. In addition, the customers are provided with two multiple-choice options to choose from: Seattle and Bellevue.

![image](https://user-images.githubusercontent.com/49314681/168821918-bdd43992-d367-4dbe-9d75-1aec35e5a461.png)

You can **test your bot in real time** by using the test bot panel, which you can enable by selecting Test your bot at the bottom of the side navigation pane.

![image](https://user-images.githubusercontent.com/49314681/168822385-f958cf82-2e1e-4931-bf0d-c9a067f96c68.png)

By **testing your bots often** throughout the creation process, you can ensure that the conversation flows as anticipated. If the dialog does not reflect your intention, you can change the dialog and save it. The **latest content will be pushed** into the test bot, and you can try it out again.

When you are ready to publish your bot, **select the Publish tab** on the side navigation pane. During the publishing process, the bot will **be checked for errors**. Bot publishing typically takes a few minutes. When the publish is successful, the top of the page will display a green banner indicating that everything worked correctly. If errors are detected, you will be notified through a message that is displayed in the application.

![image](https://user-images.githubusercontent.com/49314681/168822651-b16a0fb7-467f-48d9-9a4a-604dccdfde46.png)

After a bot is deployed and customers are interacting with it, **statistics that are related to the bot will become available**. You can access this information through the **Analytics tab** in the side navigation pane. This pane provides key performance indicators (KPIs) that show the volume of sessions that your bot has handled, how effectively your bot was able to engage users and resolve issues, escalation rates to human agents, and abandonment rates during conversations.

![image](https://user-images.githubusercontent.com/49314681/168822772-628603d6-ba34-4cde-830e-99cfffa1641c.png)

For step by step exercise to create a bot, **please check out** [this learn module](https://docs.microsoft.com/en-us/learn/modules/power-virtual-agents-bots/6b-exercise). 

## How to connect my BOT with Graph?
It is not hard to connect with Graph with your Bot. However, we'll involve Power Automate as well. For our solution Architecture, we are going to use **Power Virtual Agent Triger**, **HTTP Action** to connect Office 365 **Graph API**, and then do some **data processing** to break it down and **pull only the information we need**. Lastly, we will send them back through the **PVA Return Values** action by using markdown. 

For specific steps and final demo, **please check out** [this video](https://www.youtube.com/watch?v=M_uiW2bjLxA)! 

## Next Steps
Interested in learning more about Power Virtual Agent? Here are some **resources** for you to explore:
* [MS Learn: Create bots with Power Virtual Agents](https://docs.microsoft.com/en-us/learn/paths/work-power-virtual-agents/)
* [MS Doc: Graph Connector Agent](https://docs.microsoft.com/en-us/microsoftsearch/graph-connector-agent)

## Final Note
**Great work** if you read till the end! We learned **what is Power Virtual Agent and where they are being used**. We walked through **how to create bot and connect it with Graph API**. **Let us know** if this post is helpful. **Thank you for reading and we are proud of your learning mindset!**

![image](https://user-images.githubusercontent.com/49314681/171876404-948597bf-7d79-4919-958b-c1ed30576ffa.png)

