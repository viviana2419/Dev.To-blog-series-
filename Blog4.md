# Call Microsoft Graph API in Power Automate using custom connector.

## Azure API Management Gateway
Custom connectors are supported by Microsoft Azure API Management infrastructure. When a connection to the underlying API is created, the API Management gateway stores the API credentials or tokens, depending on the type of authentication used, on a per-connection basis in a token store. This solution enables authentication at the connection level. 

## Azure API Authentication
Before using any connector in Azure Logic Apps, Power Automate, or Power Apps, the user needs to create a connection by authenticating to the network service. 
1. No authentication- No further information is required. 
2. Basic authentication- The user will provide the user name and password to create the connection. 
3. API Key- Used by web services. Make sure that you define- Parameter label, Parameter name, Parameter location
4. OAuth 2.0 authentication- Available for online connectors. Provides implementations for specific services and prebuilt identity provider templates, when selected, fill in many of the fields that are required by OAuth 2.0.
5. Windows authentication- Available only for connections that use on-premises data gateway, when the Connect via on-premises data gateway check box is set on the General tab. When a new connection is created, the user will need to provide Windows credentials for the service and then select one of the installed on-premises gateways.

## Azure AD Authentication
1. Select the Authentication/Authorization blade.
2. Enable the App Service Authentication.
3. Set the default action on unauthorized access.
4. Configure and register the app in Azure Active Directory.

## Prerequisites
Go through [Creating Microsoft Graph custom connector in Power Apps](https://github.com/viviana2419/Dev.To-blog-series-/blob/main/Blog3.md).

## Call Microsoft Graph API in Power Automate using custom connector.

**Step 1:** Use Graph Explorer to test the API.
1. Sign in to the [Graph Explorer](https://developer.microsoft.com/en-us/graph/graph-explorer) and use it to test the API.
2. Read the permissions and continue if you agree.
3. Make sure that GET is selected for the verb, add /insights/used to the URL, and then select Run query.
4. You should get a 403 error indicating that Graph Explorer lacks your permission to perform this action.
5. Select the Modify permissions tab to grant Graph Explorer permission.
6. Select Sites.Read.All and then select Consent.
7. Read the requested permissions and then continue if you agree.
8. Select Run query again. 

![img3](https://user-images.githubusercontent.com/58803999/172056304-734b0bd3-64ff-4910-9f24-e46dc6184ebc.png)

8. Start a new browser session tab. Sign in to [OneDrive Personal Cloud Storage](https://www.microsoft.com/en-us/microsoft-365/onedrive/online-cloud-storage)
9. Select + New and select Word document. 

![igm4](https://user-images.githubusercontent.com/58803999/172056308-ea37b87a-24cd-497e-9594-365e6500e991.png)

10. Enter some test text in the Word file. The document will be saved automatically for you.
11. Go back to the Graph Explorer.
12. Run the same query again.
13. You should now get a response with values.
14. Select the response JSON, right-click, select Copy, and then save it.

![img5](https://user-images.githubusercontent.com/58803999/172056314-3d3046c6-96de-407c-ac40-0c4b9a6c0347.png)

**Step 2:** Register a new application and add permissions.
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

## Summary
**Congratulations!** You have now created an environment to call Microsoft Graph API in Power Automate and can proceed to learn more in this area. Do leave your feedback in the comments below. Our next blog will on how to **[connect Power BI to Microsoft Graph]**(https://github.com/viviana2419/Dev.To-blog-series-/blob/main/blog5.md). Stay tuned!

## Next Steps
[More info on overview of Microsoft Graph](https://docs.microsoft.com/en-us/graph/overview)

[Basics of Power BI](https://docs.microsoft.com/en-us/power-platform/admin/use-power-bi)

