# Call Microsoft Graph API in Power Automate using custom connector.

## Configuring custom connectors with authenticated APIs in Power Automate

* Azure API Management Gateway
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
[Create Microsoft Graph custom connector](https://github.com/viviana2419/Dev.To-blog-series-/blob/main/Blog3.md) first.

## Call Microsoft Graph API in Power Automate using custom connector.

**Step 1:** Register a new application and add permissions.
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

**Step 6:** Test the connector.
1. Select the Test tab and then select + New connection.
2. Provide your credentials. Read the requested permissions and continue. 
3. Select Refresh connections and Test operation.
4. You should see a 200 status, and the response should look like the following image.

![img16](https://user-images.githubusercontent.com/58803999/172057496-734122b5-a304-4621-a9d5-7214cf784202.png)
