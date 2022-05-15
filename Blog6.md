# Bring AI to your life with Power Virtual Agents and Ms Graph
Ever wondered how to bring AI to your day-to-day work? Our last post will focus on Power Virtual Agents, particularly how to build conversational BOTs with Microsoft Graph. We are going to return user's calender meeting information through BOT interaction. Some extending ideas could be get Planner or important email data. This post serves as a fundation and an inspiration. So let's go ahead and get into the content!

## Objectives and Prerequisites
So why this content is important? I am sure much like myself, most of you are inundated with a lot of information, which is spread across many services like Email, Calendar, SharePoint, etc. In order to find the right focus from the disparated data, we can bring this information together by using Power Virtual Agents and Ms Graph. 

Thus, our goal is to...
* Introducing bots, explaining where they are being used, and providing an overview of how Power Virtual Agents can be used to create bots
* Reviewing the process for creating a bot and how to work with the Power Virtual Agents user interface
* Illustrating the process of publishing a bot and successfully solve our problem

In order to get those objectives, you should have...
* Access to Power Virtual Agents
* Relevant [permissions](https://docs.microsoft.com/en-us/graph/api/calendar-list-events?view=graph-rest-1.0&tabs=http) including enabled delegation to access user calendar 

## Why Microsoft Power Virtual Agents in Education?
Microsoft Power Virtual Agents empowers teams to create powerful bots through a guided, no-code graphical interface. With Power Virtual Agents, we can eliminate the gap between the subject matter experts and development teams that are building the bots, and can reduce latency between teams recognizing an issue and updating the bot to address the issue. 

Each one of one wear mutiple hats in work sometimes. For example, an university professor may be lecturer, researcher and faculty staff during one semester! Hence, there could be a lot of different meetings and projects. To efficiently and interactively navigate through information, our chat bot would come to the field. It can help to show list and give suggestions, just like a personal assistant. 

Moreover, it includes the following features to enhance your bot's functionality to make it even more powerful:
* Initiate Microsoft Power Automate flows, which is being used in our following demo
* Pass conversations to live agents. Bots can be configured to pass conversations, including the context to live agents
* Automate topic creation. You can extract content from existing support pages, such as Frequently Asked Questions (FAQs)

