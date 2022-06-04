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

## What are the uses of Microsoft Graph?
One can use Microsoft Graph to:
* Look at the next meeting and prepare for it by providing profile information for attendees, as well as information about the latest documents they're working on, and people they're collaborating with.
* Scans one’s calendar, and suggests the best times for the next team meeting.
* Fetch the latest sales projection chart from an Excel file in your OneDrive and update the forecast in real time, all from a phone.
* Subscribe to changes in the calendar, send an alert when one spending too much time in meetings, and provide recommendations for the ones one can miss or delegate based on how relevant the attendees are to you.
* Help one sort out personal and work information on a phone. For example, by categorizing pictures that should go to your personal OneDrive and business receipts that should go to your OneDrive for Business.
* Analyze at-scale Microsoft 365 data so that decision makers can unlock valuable insights into time allocation and collaboration patterns that improve business productivity.
* Bring custom business data into Microsoft Graph, indexing it to make it searchable along with data from Microsoft 365 services.
![image](https://www.google.com/imgres?imgurl=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fgraph%2Fimages%2Fmicrosoft-graph.png&imgrefurl=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fgraph%2Foverview&tbnid=1PndKlb1wQifLM&vet=12ahUKEwinirmWgJT4AhXGBbcAHZEQDDYQMygBegUIARDWAQ..i&docid=hj85DluW4sQHYM&w=800&h=391&q=microsoft%20graph&client=firefox-b-d&ved=2ahUKEwinirmWgJT4AhXGBbcAHZEQDDYQMygBegUIARDWAQ)

## What are custom connectors?
Connectors help make it easier for app and flow makers to connect to other apps, data, and devices in the cloud in the following ways:
* Connection is done in a consistent, repeatable way that is discoverable by makers.
* Connectors have actions that allow makers to control when an operation is performed.
* Connectors can have triggers that allow automation to start when the triggering event occurs.

## Prerequisites
None except the willingness to learn. This tutorial will be a beginner friendly step by step process. Are you ready? Let's go!

## Procedure
## * Create a custom connector
1. Check the connector reference to determine if a suitable connector already exists for the API/service.

2. Manually edit the connector definition in the maker portal or by importing a definition in a supported format. This process includes identifying the authentication requirements for the API.

3. Custom connectors can be used in the same way as built-in connectors. These connectors can also be used in an environment other than the one that you used to create it. The connector definition needs to be exported from the environment where it was created and then imported into any environment that needs it. 

4. Custom connectors are only available in environments where their definition exists and are not available to other Microsoft customers. By sharing a custom connector definition as an open source, you make it available on GitHub for other customers to import into their environments. 

## * Configure custom connectors with authenticated APIs in Power Automate

* Azure API Management Gateway
1. Custom connectors are supported by Microsoft Azure API Management infrastructure.
2. When a connection to the underlying API is created, the API Management gateway stores the API credentials or tokens, depending on the type of authentication used, on a per-connection basis in a token store. Because only an authenticated user can create a connection, the connections are always authenticated. This solution enables authentication at the connection level. 

* Azure API Authentication
1. Before using any connector in Azure Logic Apps, Power Automate, or Power Apps, the user needs to create a connection by authenticating to the network service. 
2. When the No authentication option is selected, no further information is required. The user won't need authentication to create a connection to the custom connector, and any anonymous user can use the connector.
3. The simplest type of authentication is Basic authentication, where the user will provide the user name and password to create the connection. The values that you enter under the Parameter label column aren't the actual user name or password; they're labels for these fields that the user will see while creating the connection.
4. API Key is a popular authentication scheme that is used by web services. Make sure that you define the following values:
Parameter label
Parameter name
Parameter location
5. The OAuth 2.0 authentication scheme is only available for online connectors. Other than providing support for Generic OAuth 2.0, the platform provides implementations for specific services, including Azure Active Directory (Azure AD), GitHub, Microsoft account, and more. Prebuilt identity provider templates, when selected, fill in many of the fields that are required by OAuth 2.0.
6. The Windows authentication option is available only for connections that use on-premises data gateway, when the Connect via on-premises data gateway check box is set on the General tab. When a new connection is created, the user will need to provide Windows credentials for the service and then select one of the installed on-premises gateways.
