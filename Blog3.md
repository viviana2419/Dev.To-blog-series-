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

![img1](https://user-images.githubusercontent.com/58803999/172055576-a3100eea-e65d-4e97-937d-606b5d0f55e1.png)

## What are the uses of Microsoft Graph?
One can use Microsoft Graph to:
* Look at the next meeting and prepare for it by providing profile information for attendees, as well as information about the latest documents they're working on, and people they're collaborating with.
* Scans one’s calendar, and suggests the best times for the next team meeting.
* Fetch the latest sales projection chart from an Excel file in your OneDrive and update the forecast in real time, all from a phone.
* Subscribe to changes in the calendar, send an alert when one spending too much time in meetings, and provide recommendations for the ones one can miss or delegate based on how relevant the attendees are to you.
* Help one sort out personal and work information on a phone. For example, by categorizing pictures that should go to your personal OneDrive and business receipts that should go to your OneDrive for Business.
* Analyze at-scale Microsoft 365 data so that decision makers can unlock valuable insights into time allocation and collaboration patterns that improve business productivity.
* Bring custom business data into Microsoft Graph, indexing it to make it searchable along with data from Microsoft 365 services.

## What are custom connectors?
Connectors help make it easier for app and flow makers to connect to other apps, data, and devices in the cloud in the following ways:
* Connection is done in a consistent, repeatable way that is discoverable by makers.
* Connectors have actions that allow makers to control when an operation is performed.
* Connectors can have triggers that allow automation to start when the triggering event occurs.

## Prerequisites
None except the willingness to learn. This tutorial will be a beginner friendly step by step process. Are you ready? Let's go!

## Create a custom connector
* Check the connector reference to determine if a suitable connector already exists for the API/service.
* Manually edit the connector definition in the maker portal or by importing a definition in a supported format. This process includes identifying the authentication requirements for the API.
* Custom connectors can be used in the same way as built-in connectors. These connectors can also be used in an environment other than the one that you used to create it. The connector definition needs to be exported from the environment where it was created and then imported into any environment that needs it. 
* Custom connectors are only available in environments where their definition exists and are not available to other Microsoft customers. By sharing a custom connector definition as an open source, you make it available on GitHub for other customers to import into their environments. 

**Step 1:** Create a new solution.
1. Go to [Power Apps maker portal](https://make.powerapps.com/) and make sure to be in the correct environment.
2. Select Solutions > + New solution and enter the following details. 
3. Don't navigate away from this page after selecting 'Create'.

![img2](https://user-images.githubusercontent.com/58803999/172056163-171285f5-e10a-4a32-bc91-77672dc5b370.png)

**Step 2:** Use Graph Explorer to test the API.
1. Sign in to the [Graph Explorer](https://developer.microsoft.com/en-us/graph/graph-explorer) and use it to test the API.
2. Read the permissions and continue if you agree.
3. Make sure that GET is selected for the verb, add /insights/used to the URL, and then select Run query.
4. You should get a 403 error indicating that Graph Explorer lacks your permission to perform this action.
5. Select the Modify permissions tab to grant Graph Explorer permission.
6. Select Sites.Read.All and then select Consent.
7. Read the requested permissions and then continue if you agree.
8. Select Run query again. 

![img3](https://user-images.githubusercontent.com/58803999/172056304-734b0bd3-64ff-4910-9f24-e46dc6184ebc.png)

8. Sign in to [OneDrive Personal Cloud Storage](https://www.microsoft.com/en-us/microsoft-365/onedrive/online-cloud-storage)
9. Select + New and select Word document. 

![igm4](https://user-images.githubusercontent.com/58803999/172056308-ea37b87a-24cd-497e-9594-365e6500e991.png)

10. Enter some test text in the Word file. The document will be saved automatically for you.
11. Go back to the Graph Explorer.
12. Run the same query again.
13. You should now get a response with values.
14. Select the response JSON, right-click, select Copy, and then save it.

![img5](https://user-images.githubusercontent.com/58803999/172056314-3d3046c6-96de-407c-ac40-0c4b9a6c0347.png)

**Step 3:** Register a new application and add permissions.
1. Sign in to [Microsoft Azure](portal.azure.com) with your user admin credentials.
2. Select Show portal menu and then select Azure Active Directory.

![img6](https://user-images.githubusercontent.com/58803999/172056722-6d4ee677-4c2e-4c5f-a289-0cdf0a4d2646.png)

3. Enter Learn last used connector for Name, enter https://global.consent.azure-apim.net/redirect for Redirect URI, and then select Register.

![img9](https://user-images.githubusercontent.com/58803999/172056948-79452de0-eb96-4726-ae25-8c21f8936302.png)

4. Select API permissions and then select + Add a permission.

![img8](https://user-images.githubusercontent.com/58803999/172056923-5f15f43f-1151-4869-bcec-f17c5fa7cba6.png)

5. Select Certificates & secrets and + New client secret.
6. Enter Last used connector action for Description, select In 1 year for Expires, and then select Add.
7. Copy the Value and save it for later because it won't be shown again. You will use this user secret when creating the connector.
8. Select Overview.
9. Copy the Application (Client) ID and save it on a notepad. You'll use this client ID when creating the connector.

![img12](https://user-images.githubusercontent.com/58803999/172057048-83c4cacd-65fa-47db-823d-ac299f9f7a2d.png)

**Step 4:** Create a custom connector.
1. Make sure to sign in and be in the right environment in the [Power Apps Admin Portal](https://make.powerapps.com/home/).
2. Select Solutions and then select to open the Contoso graph solution that you created in 'Step 1: Create a new solution'.
3. Select + New > Other > Custom connector.
4. Enter Contoso graph for Connector name.
5. Scroll down, enter graph.microsoft.com for Host and /v1.0 for Base URL and select Security.

![img13](https://user-images.githubusercontent.com/58803999/172057226-d41ce5b9-8a91-4b04-8fd0-822e5d706610.png)

6. Select OAuth 2.0 for Authentication.
7. Select Azure Active Directory for Identity Provider.
8. Paste the ID that you copied from Azure in the Client id field and then paste the Value that you copied from Azure in the Client secret field.
9. Enter https://graph.microsoft.com for Resource URL and then select Create connector. Don't navigate away from the page.

![img14](https://user-images.githubusercontent.com/58803999/172057335-1ddd2a8f-cd97-4eb8-bfed-497876258dc1.png)

**Step 5:** Add the action.
1. Select Definition > + New action.
2. Enter Last used for Summary and LastUsed for Operation ID. Go to the Request section and select + Import from sample.
3. Select Get for the verb, enter /me/insights/used for URL, and then select Import. Scroll down and select the default response.
4. Select + Import from sample. Paste the response that you copied from Graph Explorer in the Body field and then select Import.

![img15](https://user-images.githubusercontent.com/58803999/172057424-df1ae93c-917b-4f06-81ba-a749d3dfd447.png)

5. Select Update connector. Don't navigate away from this page.

**Step 6:** Test the connector.
1. Select the Test tab and then select + New connection.
2. Provide your credentials. Read the requested permissions and continue. 
3. Select Refresh connections and Test operation.
4. You should see a 200 status, and the response should look like the following image.

![img16](https://user-images.githubusercontent.com/58803999/172057496-734122b5-a304-4621-a9d5-7214cf784202.png)

**Congratulations!** You have now created a Microsft Graph custom connector in Power App and can proceed to learn more in this area.

## Next Steps
[More info on overview of Microsoft Graph](https://docs.microsoft.com/en-us/graph/overview)

[Configuration of custom connectors with API](https://docs.microsoft.com/en-us/learn/modules/configure-custom-connectors-api/)
