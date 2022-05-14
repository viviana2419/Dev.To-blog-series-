# Access User Data from Microsoft Graph

In the previous blog post, you have learnt about the basics of PowerPlatform and Microsoft Graph. In this one, we will elaborate more on Graph specifically and provide examples in the field of education regarding how to access user data. After reading this, you will get an idea about how to use Graph to work with users in MS 365 including the required permissions.

## Objectives and Prerequisites
Users are the core of most operations in Microsoft 365. Microsoft Graph enables developers full control over the lifecycle of users in Microsoft 365 including creating, updating, and deleting users and to listing users in the organization. 

Thus, are you interested in... 
* How to get a list of users?
* How to get details, including multi-media, of a user?
* how to manage the lifecycle of a user from creation to deletion?

In order to get those objectives, you should have...
* Basic knowledge of REST services & APIs
* Basic knowledge of Microsoft Graph
* Ability to develop with NET Core at the intermediate level
* Experience using Visual Studio Code at the beginner level
* Access to a Microsoft 365 tenant

However, you don't have to check all those boxes! Your interest and willingness to learn is the key. Once we go through the following demonstration process, there are [additional resources](https://docs.microsoft.com/en-gb/learn/paths/m365-msgraph-associate/) for you to practice and learn more. So, let's go!

## Why integrate with education scenarios?
Imagine a teacher went to a conference and got excited about certain great applications. After she came back, the first thing she need to do is to load the list of students into the app. It doesn't sound like a fun task to do, right? It can also be kind of a barrer to entry at times when there is a large class or a lot of details needed. This screnario don't only happen to teacher, but to students or education software developers who may find key pieces of information are typically locked away inside a school Student Information System (SIS). Any time teachers bring a new application into their classroom, they spend time manually importing roster data into the app. Time-consuming, isn't it? And here is where Graph could come in and help. 

## What can you do with the Microsoft Graph user resource?
The user resource is the gateway to resources related to a user. The user can be the currently signed-in user, or another user if your identity and application has been granted the necessary permissions.

Following are some examples of things you can do with Graph user resource:
* Manage your organization by creating new users in your organization or update the resources and relationships for existing users. E.g. Create or delete users in your Azure AD organization, Upload or retrieve a photo for the user, etc
* Work with calendars and tasks through viewing, querying and updating user calendar. E.g. Find free meeting times for a set of users, get a list of reminders set on a user's calendar, etc
* Administer mail and handle contacts by configuring user mail settings and send mail on a user's behalf. E.g. List mail messages and send new mail, retrieve and update mailbox folders and settings, etc
* Gather user insights. E.g. Return documents recently viewed and modified by a user, return documents and sites trending around a user's activity, etc

## How to access users through Microsoft Graph?
There are two ways you can do it:
1. Access the signed-in user through the "me" alias at https://graph.microsoft.com/v1.0/me. This alias maps to the same endpoint as /users/{signed-in user's id}.

      To access a specific user, use either their ID or their userPrincipalName. For example:
      * https://graph.microsoft/com/v1.0/users/{user's ID}
      * https://graph.microsoft/com/v1.0/users/{userPrincipalName}

2. Microsoft Graph also enables developers to get a list of users. The /users endpoint will return all users in the organization using the Microsoft Graph API. The following code will do the same thing using the Microsoft Graph .NET SDK:

      GraphServiceClient graphClient = GetAuthenticatedGraphClient(...);
      var users = graphClient.Users.Request().GetAsync().Result;
      
## Back to the case
So now after you have a basic idea about Graph's functionality, let's go back to the scenario and see how to get a class of student info from Graph. There are two ways, build a Graph application or access from the Graph webpage. 

To begin with, if you haven't used Graph before, developing Microsoft Graph apps requires a Microsoft 365 tenant. You can follow the instructions on the [Microsoft 365 Developer Program](https://developer.microsoft.com/microsoft-365/dev-program) site for obtaining a developer tenant if you don't currently have a Microsoft 365 account. Then, you'll create an Azure AD application, a .NET Core console application, then finally display the currently signed in user's details. For specific demo video and documentation, please check it out [here](https://docs.microsoft.com/en-gb/learn/modules/msgraph-access-user-data/3-exercise-reading-users).

Moreover, if you already have an account set up and have some experience with Graph. You can access from Graph Explore. For example, if you log in as a teach account, you can have a look a the list of classes. by using this query: 

      GET /education/me/classes
      GET /education/users/{id}/classes
      
Then, it'll return a list of classes like below. 
![image](https://user-images.githubusercontent.com/49314681/168429511-5298b328-e5c7-4a8a-966a-ad38ea8f7dd9.png)

From there, you can find descriptions of the classes codes for the class you taught and other details. Then, you can copy the class ID of one of those. In ther search query, put 

      GET https://graph.microsoft.com/v1.0/education/classes/{class-id}/members

Then, you'll get a list of members of that specific class.
![image](https://user-images.githubusercontent.com/49314681/168430376-c6b5303c-797f-4b44-842d-0b7b211dc2a4.png)

As a result, you'll get information about students and whose data are always updated since it sync with school's back-end system. Pretty cool right?
## Next Steps
Interested in learning more about Graph? We saw this ahead and prepared the following resources for you to explore:

* [MS-Learn: Build apps with Microsoft Graph – Associate](https://docs.microsoft.com/en-gb/learn/paths/m365-msgraph-associate/)
* [MS Doc: Overview of Microsoft Graph](https://docs.microsoft.com/en-us/graph/overview)
* [MS Doc: Graph Education API overview](https://docs.microsoft.com/en-us/graph/education-concept-overview)

## Summary
Good job in reading so far! In this post, we learned what can you do with the Microsoft Graph user resource, how to access user data through Microsoft Graph in different ways, and how to use Graph solve problems in the realm of education. How's it going with you? Please comment below! Our next blog will talk about how to connect Microsoft Graph with Power Apps. Stay tuned!


