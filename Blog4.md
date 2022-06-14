# Call Microsoft Graph API in Power Automate using custom connector.

![images](https://user-images.githubusercontent.com/58803999/173579046-d9c28aa8-9795-4ae5-bbd3-d65968ceb470.jpg)

Credits- http://m.alnafsy.com/

Now that one is well acquainted with power apps and creating a microsoft graph custom connector in it, let us familiarize ourselves with the following terms once so that we can proceed to call Microsoft graph API in Power Automate using custome connectors for which we will require to set the criteria in authentication.

## Azure API Management Gateway
Custom connectors are supported by Microsoft Azure API Management infrastructure. When a connection to the underlying API is created, the API Management gateway stores the API credentials or tokens, depending on the type of authentication used, on a per-connection basis in a token store. This solution enables authentication at the connection level. 


![index](https://user-images.githubusercontent.com/58803999/173577717-0f94b26b-30ff-403b-9d68-65a909bd7680.png)

Credits- https://commons.wikimedia.org/wiki/File:Crypto_key.svg

## Azure API Authentication
Before using any connector in Azure Logic Apps, Power Automate, or Power Apps, the user needs to create a connection by authenticating to the network service. There are different types of authentication. 
1. No authentication- No further information is required. 
2. Basic authentication- The user will provide the user name and password to create the connection. 
3. API Key- Used by web services. Make sure that you define- Parameter label, Parameter name, Parameter location
4. OAuth 2.0 authentication- Available for online connectors. Provides implementations for specific services and prebuilt identity provider templates, when selected, fill in many of the fields that are required by OAuth 2.0.
5. Windows authentication- Available only for connections that use on-premises data gateway, when the Connect via on-premises data gateway check box is set on the General tab. When a new connection is created, the user will need to provide Windows credentials for the service and then select one of the installed on-premises gateways.

## Azure AD Authentication

![Presentation2](https://user-images.githubusercontent.com/58803999/173578298-28c17b34-e341-46b8-bb66-563d862d2f13.png)

## Prerequisites
An account on [Power Apps Portal](https://make.powerapps.com/), [Graph Explorer](https://developer.microsoft.com/en-us/graph/graph-explorer), [Microsoft Azure](portal.azure.com).

## Let's get started!

**Step 1:** Create a new solution.
1. Go to [Power Apps maker portal](https://make.powerapps.com/) and make sure to be in the correct environment.
2. Select Solutions > + New solution and enter the following details. 
3. Don't navigate away from this page after selecting 'Create'.

![img2](https://user-images.githubusercontent.com/58803999/172056163-171285f5-e10a-4a32-bc91-77672dc5b370.png)

**Step 2:** Use Graph Explorer to test the API.
1. Sign in to the [Graph Explorer](https://developer.microsoft.com/en-us/graph/graph-explorer) and use it to test the API. Read the permissions and continue if you agree.
2. Make sure that GET is selected for the verb, add /insights/used to the URL, and then select Run query.
3. You should get a 403 error indicating that Graph Explorer lacks your permission to perform this action.
4. Select the Modify permissions tab to grant Graph Explorer permission > Select Sites.Read.All > Consent.
5. Read the requested permissions, continue if you agree and select Run query again. 

![img3](https://user-images.githubusercontent.com/58803999/172056304-734b0bd3-64ff-4910-9f24-e46dc6184ebc.png)

6. Start a new browser session tab. Sign in to [OneDrive Personal Cloud Storage](https://www.microsoft.com/en-us/microsoft-365/onedrive/online-cloud-storage).
7. Select + New and select Word document. 

![igm4](https://user-images.githubusercontent.com/58803999/172056308-ea37b87a-24cd-497e-9594-365e6500e991.png)

8. Enter some test text in the Word file. The document will be saved automatically for you.
9. Go back to the Graph Explorer and run the same query again.
10. You should now get a response with values. Select the response JSON, right-click, select Copy, and then save it.

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
8. Select Overview, copy the Application (Client) ID and save it on a notepad. You'll use this client ID when creating the connector.

![img12](https://user-images.githubusercontent.com/58803999/172057048-83c4cacd-65fa-47db-823d-ac299f9f7a2d.png)

**Step 4:** Create a custom connector.
1. Make sure to sign in and be in the right environment in the [Power Apps Admin Portal](https://make.powerapps.com/home/).
2. Select Solutions and then select to open the Contoso graph solution that you created in 'Step 1: Create a new solution'.
3. Select + New > Other > Custom connector.
4. Enter Contoso graph for Connector name, scroll down, enter graph.microsoft.com for Host and /v1.0 for Base URL and select Security.

![img13](https://user-images.githubusercontent.com/58803999/172057226-d41ce5b9-8a91-4b04-8fd0-822e5d706610.png)

5. Select OAuth 2.0 for Authentication and Azure Active Directory for Identity Provider.
6. Paste the ID that you copied from Azure in the Client id field and then paste the Value that you copied from Azure in the Client secret field.
7. Enter https://graph.microsoft.com for Resource URL and then select Create connector. Don't navigate away from the page.

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
3. Select Refresh connections and Test operation. You should see a 200 status, and the response should look like the image.

![response-status](https://user-images.githubusercontent.com/58803999/173576351-34136c2c-e24f-458f-a23a-98921fe56177.png)

## Summary
**Congratulations!** You have now created an environment to call Microsoft Graph API in Power Automate and can proceed to learn more in this area. Do leave your feedback in the comments below. Our next blog will on how to [connect Power BI to Microsoft Graph](https://github.com/viviana2419/Dev.To-blog-series-/blob/main/blog5.md). Stay tuned!

## Next Steps
[More info on overview of Microsoft Graph](https://docs.microsoft.com/en-us/graph/overview)

[Basics of Power BI](https://docs.microsoft.com/en-us/power-platform/admin/use-power-bi)

![Pic Credits](https://cdn.pixabay.com/photo/2014/07/15/19/55/thank-you-394180_1280.png)

Credits- https://cdn.pixabay.com/photo/2014/07/15/19/55/thank-you-394180_1280.png
