# Step 1 - Setup Application Registrations

## Pre-requisites
1. Create your own Azure AD B2C tenant following [Tutorial: Create an Azure Active Directory B2C tenant](https://learn.microsoft.com/en-us/azure/active-directory-b2c/tutorial-create-tenant)
2. Create your own Azure AD B2C sign up and sign in user flow by following [Tutorial: Create user flows and custom policies in Azure Active Directory B2C ](https://learn.microsoft.com/en-us/azure/active-directory-b2c/tutorial-create-user-flows?pivots=b2c-user-flow)

## Create your Azure AD B2C application registrations
To complete this demo you will need to create multiple application registrations in your Azure AD B2C tenant and note their client id's , secrets, etc.

### 1. Register **insomnia_authcode_demo**

This application registraiton will reprsent a client app which uses the Authorization Code flow + client secrets to authenticate to Azure B2C

1. Sign in to the Azure portal.
2. If you have access to multiple tenants, select the Settings icon in the top menu to **switch to your Azure AD B2C tenant from the Directories + subscriptions menu.**
3. In the Azure portal, search for, then select **Azure AD B2C.**
4. Select App registrations, and then select New registration.
5. Enter a Name for the application for this demo use **insomnia_authcode_demo** as the name
6. Under Supported account types, select** Accounts in any identity provider or organizational directory (for authenticating users with user flows)**.
7. Under Redirect URI, select **Web**, and then enter ```https://oidcdebugger.com/debug``` in the URL text box
8. Select **Register**

   ![image](https://github.com/user-attachments/assets/62db0244-5606-42e5-a997-5808936d2f11)

9. From the **Overview** blade of this new app registration.  Notate and record the **Application (client) ID** in your notes
10. Choose **Certificates & secrets** menu and under Client Secrets, choose **New client secret**
11. Give this secret a name and an expiration date in the future and choose **Add**
12. Use the **copy** button next to the **Value** of the newly generated secret and Record this value in your notes

   ![image](https://github.com/user-attachments/assets/59fe6da3-247b-4318-b19b-08b9ba067352)

13. In your notes you should now have the following saved:

   ```
   insomnia_authcode_demo:
   client_id = <client_id from step 9 above>
   client_secret = <secret value from step 12 above>
   ```

### 2. Register **insomnia_authcodepkce_demo**

This application registration will represent a single page application (SPA) client app which uses the Authorization Code + PKCE flow to authenticate to Azure B2C

1. Sign in to the Azure portal.
2. If you have access to multiple tenants, select the Settings icon in the top menu to **switch to your Azure AD B2C tenant from the Directories + subscriptions menu.**
3. In the Azure portal, search for, then select **Azure AD B2C.**
4. Select App registrations, and then select New registration.
5. Enter a Name for the application for this demo use **insomnia_authcodepkce_demo** as the name
6. Under Supported account types, select** Accounts in any identity provider or organizational directory (for authenticating users with user flows)**.
7. Under Redirect URI, select **Singlepage application (SPA)**, and then enter ```https://oidcdebugger.com/debug``` in the URL text box
8. Select **Register**
9. From the **Overview** blade of this new app registration.  Notate and record the **Application (client) ID** in your notes

   ![image](https://github.com/user-attachments/assets/2b6fe29d-8b89-41a0-8c8b-5555a3b969f8)

10. In your notes you should now have the following saved

    ```
    insomnia_authcode_demo:
    client_id = <client_id>
    client_secret = <secret value>
    
    insomnia_authcodepkce_demo:
    client_id = <client_id from step 9 above>

    ```

### 3. Register **insomnia_implicitflow_demo**

This application registration will represent a client app which uses the Implicit flow to authenticate to Azure B2C

1. Sign in to the Azure portal.
2. If you have access to multiple tenants, select the Settings icon in the top menu to **switch to your Azure AD B2C tenant from the Directories + subscriptions menu.**
3. In the Azure portal, search for, then select **Azure AD B2C.**
4. Select App registrations, and then select New registration.
5. Enter a Name for the application for this demo use **insomnia_implicitflow_demo** as the name
6. Under Supported account types, select** Accounts in any identity provider or organizational directory (for authenticating users with user flows)**.
7. Under Redirect URI, select **Web**, and then enter ```https://jwt.ms``` in the URL text box
8. Select **Register**

   ![image](https://github.com/user-attachments/assets/21a1d41a-ad32-42b4-a339-c6dcd578e389)


9. From the **Overview** blade of this new app registration.  Notate and record the **Application (client) ID** in your notes
10. Choose the **Authentication** menu for this new app registration
11. Locate and enable the options for **Access tokens (used for implicit flows)** and **ID tokens (used for implicit and hybrid flows)**

   ![image](https://github.com/user-attachments/assets/9665a90e-f70d-46c7-9b4f-ed7262bebcda)

12. Save this setting
13. In your notes you should now have the following saved:

    ```
    insomnia_authcode_demo:
    client_id = <client_id>
    client_secret = <secret value>

    insomnia_authcodepkce_demo:
    client_id = <client_id>
    
    insomnia_implicitflow_demo:
    client_id = <client_id from step 9 above>
    ```

### 4. Register **insomnia_webapi_demo**

This application will represent a web api that uses Oauth2 authorization scopes and Azure B2C to emit access tokens 

1. Sign in to the Azure portal.
2. If you have access to multiple tenants, select the Settings icon in the top menu to **switch to your Azure AD B2C tenant from the Directories + subscriptions menu.**
3. In the Azure portal, search for, then select **Azure AD B2C.**
4. Select App registrations, and then select New registration.
5. Enter a Name for the application for this demo use **insomnia_webapi_demo** as the name
6. Under Supported account types, select** Accounts in any identity provider or organizational directory (for authenticating users with user flows)**.
7. Under Redirect URI, select **Web**, and then enter ```https://jwt.ms``` in the URL text box
8. Select **Register**
9. From the **Overview** blade of this new app registration.  Notate and record the **Application (client) ID** in your notes
10. From this new application registration, visit the **Expose an API** menu
11. Next to **Application ID URI** choose Add and then choose **Save** to add the default Application ID URI value

   ![image](https://github.com/user-attachments/assets/b02cdbb6-2080-4c4d-9f72-95d92c390f72)

12. Selectd **Add a scope** and under the name , admin consent display name, and description populate the value ```demoscope``` and choose **Add scope**

   ![image](https://github.com/user-attachments/assets/2f63031d-cd6c-4952-8acd-d9d1eca7bc29)

13. Next to the newly created scope copy and paste the full scope name using the copy button ,  add this to your notes

   ![image](https://github.com/user-attachments/assets/d5d26a9f-eab1-46b9-9cbc-b232dd1b994a)

14. In your notes you should now have the following saved:

    ```
    insomnia_authcode_demo:
    client_id = <client_id>
    client_secret = <secret value>
    
    insomnia_implicitflow_demo:
    client_id = <client_id>

    insomnia_authcodepkce_demo:
    client_id = <client_id from step 9 above>
    
    insomnia_webapi_demo:
    client_id = <client_id from step 9 above>
    demo scope name = <full scope from step 13 above>
    ```

### 5. Add your demoscope api permission to each of your client apps

In order for your three client apps to be able to request an access token for your web api demoscope, you must add this API permission to each of your three client apps using the following steps

1. Sign in to the Azure portal.
2. If you have access to multiple tenants, select the Settings icon in the top menu to **switch to your Azure AD B2C tenant from the Directories + subscriptions menu.**
3. In the Azure portal, search for, then select **Azure AD B2C.**
4. Select App registrations
5. Locate your first app registration **insomnia_authcodepkce_demo**
6. From the **API permissions** blade choose **Add a permission**
7. From the **APIs my organization uses** tab search for your previously registered api name `insomnia_webapi_demo' and select this API

   ![image](https://github.com/user-attachments/assets/480f52fb-9dcf-4545-97b2-cdc393655898)

8. Under **Delegated permissions** select the **demoscope** permission and choose **Add permissions**

   ![image](https://github.com/user-attachments/assets/7ea8b70e-0b3d-4b80-8165-aad87b651fc0)

9. Once added, select the **Grant admin consent** button to grant consent to this application in your directory

   ![image](https://github.com/user-attachments/assets/5c25319c-d829-416d-b691-152f5b319e60)

10.  Now you will need to follow the same steps 1-9 but for your other two client apps `insomnia_authcodepkce_demo` and `insomnia_implicitflow_demo`

