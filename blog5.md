# Connecting Power BI to Microsoft Graph 
**Hey well done!**
![Well done!1](https://user-images.githubusercontent.com/64436573/173185282-79710678-f10d-44c2-9a5e-bf3248b0c161.png)
 You are almost near to achieve your goal of becoming Microsoft Power Platform expert. Till now we expect that you have read all the previous blogs and this is our fifth blog. Let have a top-level view of previous blogs.
 
In first blog we have learned the basic concepts of Power Platform and have learned the introduction of each component of Power Platform. In first blog we have introduction of each and every component of Microsoft Power Platform along with some features of Microsoft Power Platform. Then from blog two to blog five we have Microsoft Graph focused content. In these blogs we have learned how to access data from Graph API and how to connect Graph API to various components of Power Automate. So, it was a nice journey of how to work with a huge amount of data and how to handle the data with the help of Microsoft Graph API.

So now in this blog we are continuing the concepts of Graph API and now we are **“connecting Power BI to Microsoft Graph”**. As we already have an introduction about these two components and now, we will focus more on the implementation rather the learning the concepts.

Microsoft Power BI is a data analyzing and data visualizing tool which gives the insights of data through reports and dashboards. And with the help of this analyzed data one can make proper decisions.

On the other hand, Microsoft graph is a data accessing API with the help of which we can access data from Microsoft cloud services like Active directory, SharePoint, OneDrive and much more. So now we will play with these two technologies to meet our business solutions. We will learn how to import data in Microsoft Power BI with the help of Microsoft Graph then visualize and analyze that data in Power BI. 

**So, let’s do it!**
![Well done!](https://user-images.githubusercontent.com/64436573/173185740-ac43f443-5016-4d4e-b6b3-d1df81e5f6c5.png)

We can connect Graph API with Power BI using custom connectors for Power BI. Graph API have many important functionalities and one of the most important benefits of Graph API is that it has single endpoint as compared to other Microsoft Graph API’s. The Graph API data source can be used in the Power BI Desktop where we can publish the model to Microsoft Power BI service.

Now let’s see the steps of connecting Power BI with Graph API. The steps are given below:

Login to Power BI Desktop using Microsoft Credentials. Click on Get Data and select OData feed. In simple clicks, you will be able to import the data to Microsoft Power BI Desktop easily. 

![Power BI OData feed](https://user-images.githubusercontent.com/64436573/173185896-8474c764-5fbd-4a0d-a56f-7144cdd9fa06.png)

Just copy the API URL https://graph.microsoft.com/beta/users from the Graph Explorer that can be pasted in the OData feed as shown in the image above. You must login to Graph Explorer before inmporting data.

Next, import the data shown in your dashboard and then it’s good to go.

The URL given here is used to find the users connected with me. We can also run this as a query in Graph Explorer, just paste the link in Graph explorer search bar and hit run query to see the output as shown below

![1](https://user-images.githubusercontent.com/64436573/173186007-02af2e07-52ea-4817-9b24-4fade530b4ce.png)

**Note:** here the output is hidden due to privacy issues.

There is also modify permissions (preview) tab where we can change and modify permissions for our queries.

![2](https://user-images.githubusercontent.com/64436573/173186067-3606bab9-2362-4e5b-90f8-e6f2b9668a08.png)

Graph explorer has two versions beta and v1.0 and I founded beta as the best versions so it’s recommended to use beta version.

On the left side are sample queries which we can use for testing and learning purposes.

So it was the short and precise overview of Graph API, we can further explore it using Microsoft docs and Microsoft learn platform.

Further learning materials:

[Microsoft Graph Documentation](https://docs.microsoft.com/en-us/graph/)

[Overview of Microsoft Graph](https://docs.microsoft.com/en-us/graph/overview)

[Videos on Microsoft Graph](https://developer.microsoft.com/en-us/graph/gallery/?filterBy=Podcasts,Videos)

