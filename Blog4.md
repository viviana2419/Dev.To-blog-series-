# Call Microsoft Graph API in Power Automate using custom connector.

## Configure custom connectors with authenticated APIs in Power Automate

* Azure API Management Gateway
Custom connectors are supported by Microsoft Azure API Management infrastructure. When a connection to the underlying API is created, the API Management gateway stores the API credentials or tokens, depending on the type of authentication used, on a per-connection basis in a token store. This solution enables authentication at the connection level. 

* Azure API Authentication
Before using any connector in Azure Logic Apps, Power Automate, or Power Apps, the user needs to create a connection by authenticating to the network service. 
1. No authentication- No further information is required. 
2. Basic authentication- The user will provide the user name and password to create the connection. 
3. API Key- Used by web services. Make sure that you define- Parameter label, Parameter name, Parameter location
4. OAuth 2.0 authentication- Available for online connectors. Provides implementations for specific services and prebuilt identity provider templates, when selected, fill in many of the fields that are required by OAuth 2.0.
5. Windows authentication- Available only for connections that use on-premises data gateway, when the Connect via on-premises data gateway check box is set on the General tab. When a new connection is created, the user will need to provide Windows credentials for the service and then select one of the installed on-premises gateways.

* Azure AD Authentication
1. Select the Authentication/Authorization blade.
2. Enable the App Service Authentication.
3. Set the default action on unauthorized access.
4. Configure and register the app in Azure Active Directory.

Follow these steps to set up and configure connectors with Azure AD:
Register two Azure AD apps:
1. One to identify and protect API service
2. One to identify and protect your connector
3. Delegate permissions. Allow your connector's registered app to make "on-behalf" calls to your service's identity.
4. Define your connector by providing the client ID, secret, and resource URL information.
5. Add redirect URLs to the connector app registration.
If your service is set up with the Cross-Origin Resource Sharing (CORS) scheme, allow list Azure API Management domains (usually azure-apim.net) for CORS on your service.
