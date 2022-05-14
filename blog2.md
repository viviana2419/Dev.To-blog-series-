# Access User Data from Microsoft Graph

In the previous blog post, you have learnt about the basics of PowerPlatform and Microsoft Graph. In this one, we will elaborate more on Graph specifically and provide examples in the field of education regarding how to access user data. After reading this, you will get an idea about how to use Graph to work with users in MS 365 including the required permissions.

## Objectives and Prerequisites
Users are the core of most operations in Microsoft 365. Microsoft Graph enables developers full control over the lifecycle of users in Microsoft 365 including creating, updating, and deleting users and to listing users in the organization. 

Thus, we are interested in 
* How to get a list of users?
* How to get details, including multi-media, of a user?
* how to manage the lifecycle of a user from creation to deletion?

In order to get those objectives, you need to have...
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
