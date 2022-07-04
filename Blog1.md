This blog series introduces the Power platform ecosystem and includes a broad understanding of the Power platform with additional resources for people from different backgrounds no matter as consultant, data analyst, or developer. The blog series aim to empower readers to build solutions easily that normally require developer expertise and to hone the consulting skills regarding business problems!
* [Blog 1: Introduction to Power Platform and Microsoft Graph](https://github.com/viviana2419/Dev.To-blog-series-/blob/main/Blog1.md) 
* [Blog 2: Access User Data from Microsoft Graph](https://github.com/viviana2419/Dev.To-blog-series-/blob/main/blog2.md)
* [Blog 3: Creating Microsoft Graph custom connector in Power Apps](https://github.com/viviana2419/Dev.To-blog-series-/blob/main/Blog3.md)
* [Blog 4: Call Microsoft Graph API in Power Automate using custom connector](https://github.com/viviana2419/Dev.To-blog-series-/blob/main/Blog4.md)
* [Blog 5: Connecting Power BI to Microsoft Graph](https://github.com/viviana2419/Dev.To-blog-series-/blob/main/blog5.md)
* [Blog 6: Bring AI to your life with Power Virtual Agents and Ms Graph](https://github.com/viviana2419/Dev.To-blog-series-/blob/main/Blog6.md)

# Prerequisite:
To learn and build with Power Platform, there are no prerequisite required. We will start from the very basics and will learn the track step by step. In this blog we are going to answer the questions which evolve in every person’s mind who starts with Power Platform in order to hone their business. We will learn this technology in details and will also define its pros and cons.

So we encourage the readers to start learning Power Platform without worrying about the prerequisites for this learning path.

# Expected Outcomes
After leaning this track, you will be able to
* Work with power platform components to create best business solutions.
* Create custom apps using Power apps without having coding skills.
* To automate workflows and repetitive processes using Power Automate.
* Analyze data, visualize data and make decisions using analyzed data with the help of Power BI.
* Work with the most powerful AI oriented technology called Power Virtual Agents.

# Introduction to power platform
![2a51caf5af85acce41a0b9a8444c3ae6](https://user-images.githubusercontent.com/64436573/170357712-80510604-616b-4046-9556-8202bdb01c6c.png)

Power platform is a platform which consists of four components and many underlying technologies that all the applications can use. The four components are:
- Power Apps
- Power Automate
- Power BI
- Power virtual agents

We will discuss all of them one by one.

So, all these apps combinedly forms a powerful platform called Microsoft Power Platform. Microsoft Power Platform is used to provide complex business solutions, analyze the data and make decisions on the basis of analyzed data, visualize the data with the help of graphs, automate a business process and is used to build virtual agents for communication with humans. The most interesting fact about Power Platform is that everyone can use it without having coding skills because it is drag and drop technology and by just dragging and dropping the components, we can build powerful applications. Along with these powerful tools Power Platform also provides other amazing features like AI builder, Microsoft Data verse and connectors which adds more functionalities to these apps. With all these extensions and functionalities Microsoft Power Platform is the leading technology in the low code/no code development.

The Microsoft Power Platform is used by many businesses – both big and small. The following image shows some of the businesses that have chosen to adopt the Microsoft Power Platform to accelerate their business.
![111](https://user-images.githubusercontent.com/64436573/170120738-dc4102eb-6a5f-47bc-9f44-ac40238b33dc.png)

So now its time to dive into details of each component of Power Platform.

## [POWER APPS](https://powerapps.microsoft.com/en-us/)
PowerApps is a drag and drop interface which allow users to create apps with no-code/low code development. And the apps designed through PowerApps can run on Android, iOS, windows and on any internet browser, this feature of PowerApps makes it the leader of other app development platforms. PowerApps also provides other services, connectors and data platforms which are helpful in creating custom apps for business solutions.	 PowerApps can quickly transform any manual business to digital operations by providing interactive interfaces and several functionalities for better performance.

**How to create a PowerApps app?**

First click on this link [click here](https://make.powerapps.com/) and sign in or create account. After signing in below interface will appear which provides various data platforms to import data from and create the app. So we will create an app using excel workbook so I will click on excel
     ![pa1](https://user-images.githubusercontent.com/64436573/170857112-db9510cd-a0db-4dc5-8926-e1394b04d746.png)

After clicking on excel below interface will appear  
![pa2](https://user-images.githubusercontent.com/64436573/170857148-c6b5f964-4aa9-4745-9355-9f17f2ade976.png)
This interface shows the various connections for importing data. I will click on one drive for business for importing excel workbook and then click on create. After clicking on create, select the file as shown below
  ![Background](https://user-images.githubusercontent.com/64436573/170857604-db6f4826-4cc5-4e00-a2d1-346011be660d.png)

After selecting excel file, select table as shown below and then click on connect
     ![pa3](https://user-images.githubusercontent.com/64436573/170857796-1311b929-2e64-449a-8c54-dd98d955d37b.png)

After clicking on connect below interface will appear
     ![pa4](https://user-images.githubusercontent.com/64436573/170857844-101d85e3-5622-4abf-8c06-490c04155721.png)

Based on the data, power apps create default app for us which can be customized by us.

We can now click on icons and can customize them easily. When we click on play button in the top right corner then the interface changes and we can browse our apps and can check it as how it will work after publishing
     ![pa5](https://user-images.githubusercontent.com/64436573/170858024-a8a73e2a-30c8-42ea-8fde-148d31875171.png)

After customizing the app we can use it by selecting file and then click on save as and now we can install it on our phones etc
     
## [POWER AUTOMATE](https://powerautomate.microsoft.com/en-us/)

![download](https://user-images.githubusercontent.com/64436573/170858193-96469cf0-4873-4679-aa38-aee8a25c2de3.png)

As its name suggest, it’s a tool for automation. It helps automate the repetitive processes by designing workflows for automated communications, for automated files synchronization, for automated reminders, for automated data collection and for other tasks automations. Some of the examples of Power automate workflows are given below:

- If we receive an attachment in our email then we can automatically upload it to one drive.
- We can send automated emails on fix date and time.
- We can automatically send monthly salary slips to our clients.
- Automatically add the events to calendar and get alerts of upcoming events.
- Automatically schedule events.
- Get automated notifications of tasks to do.

So these are some of the functions which Power automate can do. Power automate can connect to various data sources and API’s for improved automation.  

**How to create our first workflow with Power automate?**

   i. Sign in to [Microsoft 365 account](https://www.office.com/).
   
   ii. From apps select Power automate and click on it.
   
   iii. After clicking on Power automate below interface will appear.
       ![11](https://user-images.githubusercontent.com/64436573/173186915-bbb94445-eb9f-42a6-a8f9-90f389899eed.png)
       
   iv. On the left panel various functionalities are available like data, monitor and AI builder which can be used for advance features of workflows.
   ![22](https://user-images.githubusercontent.com/64436573/173187027-10f13fae-6bdb-429e-b99d-d567feb6dcb3.png)

   v. We will create a simple workflow by clicking on “get a push notification when a new file is added in OneDrive for business”.
   ![11](https://user-images.githubusercontent.com/64436573/173187147-419ef843-9aec-4c2c-9aa4-e1f48bf0ba3d.png)

   vi. After clicking on “get a push notification when a new file is added in OneDrive for business” the below interface will appear. Here we need to login to our OneDrive for business account and click on create for notifications tab. 
   ![11](https://user-images.githubusercontent.com/64436573/173187245-aada14a4-16ab-4ca1-8d83-f2652aba2777.png)
  
  vii. After above step below interface will appear, here select the folder which we need to monitor for files upload and select the desired settings for push notifications as shown below. 
  ![33](https://user-images.githubusercontent.com/64436573/173187338-1a10c315-1b02-4180-a7e6-0261762a5476.png)
  
Settings for push notifications

![44](https://user-images.githubusercontent.com/64436573/173187378-20f0af1b-2901-45b4-aa4e-4b04e8c87fac.png)

viii. Now click on save in the top right corner to save the workflow. After saving the workflow below notification will appear on the top. We can also test our workflow by clicking on “test” button.
![55](https://user-images.githubusercontent.com/64436573/173187431-f2c5d187-405e-4281-b9f2-12b31e82d77f.png)

## [Power BI](https://powerbi.microsoft.com/en-us/)

Power BI is all about data visualization and dashboarding. It is useful for visualizing the complex data and convert the complex numbers into interactive graphs and visuals. As visuals are more understandable than numbers, so Power BI can transform the number and calculations into immersive visuals which can be easily understood by non-technical peoples.

**How to work with Power BI?**

i. We can start working with Power BI by using online web portal or install Power BI Desktop app.

ii. [Sign up](https://powerbi.microsoft.com/en-au/) head over to this link and sign up, after sign up we can use either the web-based version or can also install the Desktop app.

iii. In this tutorial we will use the online web-based version. After signing in to the online Power BI website we will have the below interface
![66](https://user-images.githubusercontent.com/64436573/173187628-f8eb8715-65a1-44be-976b-95aff3fae8fe.png)

iv.On the left panel is create button, click on it and then select “pick a published dataset” as shown below.
![77](https://user-images.githubusercontent.com/64436573/173187668-bbfe5f41-2424-4b81-9517-81d2ed7bde57.png)

v. As I have already a published dataset so I will select a dataset named “time table”. We can add data manually or by copying and pasting data in the online web portal. We can add more data sources in Desktop app but can’t add data sources in the web-based version. 
so after selecting dataset click on create then below interface will appear.
![11](https://user-images.githubusercontent.com/64436573/173187774-6a988cbf-3eb4-4b0f-b22d-4014244c3adc.png)

vi.Here we can create our visuals and dashboards. Various panels are present where we can select our desired options. On the most right panel we have our data where we will select only the desired columns for visualization then on second are the types of graphs we can use then on the third panel are the data fields and filters for customization. So here can drag and drop our data and can easily visualize our data as shown below
![11](https://user-images.githubusercontent.com/64436573/173187813-2bfd50dc-bfc1-4853-b320-eeaa8b9a36b8.png)

Here we can add further customizations depending on the technicality of designer. 

## [Power virtual agents](https://powervirtualagents.microsoft.com/en-us/)

Power virtual agent is that component of Power Platform which is used to create chat bots for automatic communication. It is drag and drop interface where no code is required and there is no need of data scientists or developers for designing powerful chatbots.

**So, what are chatbots?**

Basically, if we have company and we are selling software’s then on daily basis we can have thousands of customers who may face problems while using our software’s or some customers want to know about our company then a single person can’t handle all these customers at a time so what we can do is that we can create a chat bot with the help of Power virtual agents where we will populate all the information and general questions & answers related to our software’s and company, so when ever a customer visits our site and he/she want to communicate with us then a chatbot will be initiated for conversation and based on the selected problem the solution will be provided by the chatbot.

We can start our chatbot creation journey by clicking on this link [Microsoft Power Virtual Agents](https://powervirtualagents.microsoft.com/en-us/) after clicking on this link create a free account and start working with chatbots creation. Free account is for limited time but we can practice with chatbot creation for such limited time.   

Below is the interface of power virtual agents chatbot creation.
![content-image-1](https://user-images.githubusercontent.com/64436573/173188122-f4443240-0c53-42e8-8aa2-255d15c22aa7.png)

## Features of Power Platform

Power platform has some other powerful features which increase the customization and capabilities of Power platform. Due to these features Power platform provides robust solutions to almost any kind of business. So the detail of these features is given below:

 * [AI BUILDER](https://docs.microsoft.com/en-us/ai-builder/):

  This feature of Power platform allows users to add AI capabilities to their Power apps and Power automate. This feature makes Power platform intelligent and can make predictions for better business solutions. 
To add AI capabilities to our workflows and apps we can locate its button on the left panel in Power automate and in Power apps.

* [Microsoft data verse](https://docs.microsoft.com/en-us/power-apps/maker/data-platform/data-platform-intro):

As its name suggests that it’s a platform for data storage and data integration with Power platforms components. It facilitates the user to add data from multiple resources and integrate it with power platform for usage. As we need data for every component of Power platform to make it functional and that data is stored and manipulated in Microsoft Data verse.

* [Connectors](https://docs.microsoft.com/en-us/connectors/):

Connectors help us to connect apps, data and devices for cohesive actions and functionalities. 
Let say we have data stored in our Dropbox account and we want to use it in our Power app then we will use the Dropbox connector for importing that data in Power apps platform. We can use the connectors functionalities by locating it on the left panel in Power apps and in Power automate. There are various options available for connecting various connectors, examples of popular connectors include Salesforce, Office 365, Twitter, Dropbox, Google services, and more.

## [Introduction to Microsoft graph](https://developer.microsoft.com/en-us/graph)

Microsoft graph is an API which is used to connect to various services of Microsoft 365 and we can also use it to access data in Microsoft 365, Windows, and Enterprise Mobility + Security. It can add intelligence and security to our apps which will interact with millions of users. It can automate our tasks and can make decisions for us based on the data provided.

We can start our initial journey with Microsoft graph by exploring the “[Graph explorer]([url](https://developer.microsoft.com/en-us/graph/graph-explorer))”.

Graph explorer provides samples for creating Microsoft Graph REST API requests. It contains some common scenarios to work with Microsoft graph API. We can use the samples codes for using Microsoft graph API in our apps and the sample queries are also present which can be utilized in our apps for accessing different services of Microsoft graph.

Graph Explorer includes the following elements:
   
1. HTTP verb drop-down list
2.	API version drop-down list
3.	Request query address bar
4.	Sample query
5.	Documentation link for the sample query

![1111](https://user-images.githubusercontent.com/64436573/173229513-0918ae55-c3d5-44dd-a2f8-9c082d787670.png)

## Next Steps
if you are interested to further learn these technologies then below are some useful resources 
* [Introduction to Microsoft Power Platform](https://docs.microsoft.com/en-us/learn/modules/introduction-power-platform/)
* [PL-900: Microsoft Power Platform Fundamentals](https://docs.microsoft.com/en-us/learn/paths/power-plat-fundamentals/)
* [Microsoft Power Platform documentation](https://docs.microsoft.com/en-us/power-platform/)
* [Microsoft Certified: Power Platform Fundamentals](https://docs.microsoft.com/en-us/learn/certifications/power-platform-fundamentals/)
* [Overview of Microsoft Graph](https://docs.microsoft.com/en-us/graph/overview)
* [Microsoft Graph documentation](https://docs.microsoft.com/en-us/graph/)
* [Explore Microsoft Graph](https://docs.microsoft.com/en-us/learn/modules/microsoft-graph/)

## Summary:

In this first blog of blog series, we have just given the introduction to various components of Microsoft Power platform. We have introduced each component and also shown that how can we get started with each of these components. In the last section of this blog we have a little introduction to Microsoft Graph API which is a powerful tool for connecting to a tremendous amount of data and which can also add intelligence capabilities to our business solution.  






