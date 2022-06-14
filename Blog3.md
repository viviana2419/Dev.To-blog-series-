# Creating Microsoft Graph custom connector in Power Apps.

## What are Power Apps?
* Power Apps is a **suite of apps, services, connectors, and a data platform**, that provides a rapid development environment to build custom apps for business needs. 
* Using Power Apps, one can quickly **build custom business apps that connect to data stored** either **in the underlying data platform** (Microsoft Dataverse) or in various **online and on-premises data sources** (such as SharePoint, Microsoft 365, Dynamics 365, SQL Server). 
* One can **create three types of apps** using this service: canvas, model-driven, and portal. 

## What are Microsoft Graphs?
* Microsoft Graph is the gateway to data and intelligence in Microsoft 365. It **provides a unified programmability model** that you can use to access the tremendous amount of data in Microsoft 365, Windows, and Enterprise Mobility + Security.
* The Microsoft Graph API **offers a single endpoint** to provide access to rich, people-centric data and insights in the Microsoft cloud.
* Microsoft Graph connectors work in the incoming direction, delivering data external to the Microsoft cloud into Microsoft Graph services and applications to enhance Microsoft 365 experiences such as Microsoft Search.
* Microsoft Graph Data Connect provides a set of **tools to streamline secure and scalable delivery of Microsoft Graph data** to popular Azure data stores. The cached data serves as data sources for Azure development tools that you can use to build intelligent applications.

![Credits](https://docs.microsoft.com/en-us/graph/images/microsoft-graph.png)

Credits- https://docs.microsoft.com/en-us/graph/images/microsoft-graph.png

## What are the uses of Microsoft Graph?
One can use Microsoft Graph to:
* Look at the next meeting and prepare for it by providing profile information for attendees, as well as information about the latest documents they're working on, and people they're collaborating with.
* Scans one’s calendar, and suggests the best times for the next team meeting and subscribe to changes in the calendar, send an alert when one spending too much time in meetings, and provide recommendations for the ones one can miss or delegate based on how relevant the attendees are to you.
* Help one sort out personal and work information on a phone. For example, by categorizing pictures that should go to your personal OneDrive and business receipts that should go to your OneDrive for Business and bring custom business data into Microsoft Graph, indexing it to make it searchable along with data from Microsoft 365 services.

## What are custom connectors?
Connectors help make it easier for app and flow makers to connect to other apps, data, and devices in the cloud in the following ways:
* Connection is done in a consistent, repeatable way that is discoverable by makers.
* Connectors have actions that allow makers to control when an operation is performed.
* Connectors can have triggers that allow automation to start when the triggering event occurs.

![Presentation1](https://user-images.githubusercontent.com/58803999/173576451-fdc44814-9960-4fd1-b02e-1a208749e625.png)

## Prerequisites
An account on ![Power Apps Portal](https://make.powerapps.com/).

## Let's get started!

**Step 1:** Create a new solution.
1. Go to [Power Apps maker portal](https://make.powerapps.com/) and make sure to be in the correct environment.
2. Select Solutions > + New solution and enter the following details. 
3. Don't navigate away from this page after selecting 'Create'.

![Img1](https://user-images.githubusercontent.com/58803999/172183894-ace14d0e-8283-4d03-b0d2-9b9cd52826e8.png)

**Step 2:** Create a custom connector.
1. Go to [Power Apps admin portal](https://make.powerapps.com/) and make sure that you are in the correct environment.
2. Select Solutions and then select to open the Microsoft Graph solution that you created in Task 1: Create a new solution.
3. Select + New > Automation > Custom connector.
4. Enter Microsoft graph for Connector name.
5. Scroll down, enter graph.microsoft.com for Host and /v1.0 for Base URL.

![Img2](https://user-images.githubusercontent.com/58803999/172184483-39298b7d-4e31-4bc5-90e1-74ce1521759a.png)

6. Go to the Security option. Since we are just creating a custom connection, you can choose "No authentication" else any other type of authentication as per your needs.

![Img4](https://user-images.githubusercontent.com/58803999/172185436-b5293f9f-4754-4aeb-965d-ae33d2531875.png)

7. Go to the Definition option. You can leave it as it is and move to the Code (Preview) option.

![Img5](https://user-images.githubusercontent.com/58803999/172186091-85c88a0a-25e8-4f5d-93ab-8958acce6d8f.png)

8. You can leave it as it is and click on "Create Connector".

![Screenshot (6)](https://user-images.githubusercontent.com/58803999/172186743-3f2b25fb-6187-454d-aa08-a98184a469e9.png)

![Img7](https://user-images.githubusercontent.com/58803999/172187284-6c7d0416-0f20-40fa-b1c6-9658351936dd.png)

## Summary
**Congratulations!** You have created a Microsft Graph custom connector in Power App and can proceed to learn more in this area. Do leave your feedback in the comments below. Our next blog will on how to [call Microsoft Graph API in Power Automate using custom connector](https://github.com/viviana2419/Dev.To-blog-series-/blob/main/Blog4.md). Stay tuned!

## Next Steps
[More info on overview of Microsoft Graph](https://docs.microsoft.com/en-us/graph/overview)

[List used for building a Microsoft connector](https://docs.microsoft.com/en-us/graph/api/insights-list-used/)

![Pic Credits](https://cdn.pixabay.com/photo/2014/07/15/19/55/thank-you-394180_1280.png)
Credits- https://cdn.pixabay.com/photo/2014/07/15/19/55/thank-you-394180_1280.png
