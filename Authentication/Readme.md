
#### AIMS360 API Authentication
 
Authenticating via OAuth requires the generation of a bearer token. All requests need to include
Header Authorization.

Note: To generate Bearer token, the API access should be enabled in the Company
License.



#### Generating Bearer Token on AIMS360 ERP Application

Step 1: Login to AIMS360 ERP application using the Username and password

Note: The respective logged in Operator must have API permissions enabled to
generate Bearer Token. To get the API permissions enabled, contact your System
Administrator.

Step 2:

Navigate to API tab under User Settings. If the Bearer token/Access token is not
generated earlier, Generate Access token button will be available. Click on
Generate Access token button.

![](media/1161981bb91a28440e45cb67b3dda0fa.png)

Step 3:

Enter the Username and Password on the AIMS360 login window displayed.

![](media/33921651f05aa63fe4d2ac51c14b9f90.png)

Step 4:

After Successful validation of the username and password, the Bearer
token/Access token will be generated and displayed on API tab

![](media/52438300e2a7bd385d96c7791decc685.png)

#### Generating a Bearer token on Swagger

Swagger URL: https://app.swaggerhub.com/apis-docs/AIMS360/AIMS360API/1.0.0

Step 1:

To generate bearer token, the Client ID and Secret key are necessary. Copy
client ID and secret from AIMS360 API tab under System Settings on AIMS360
application.

![](media/ff708d7d5f37ee685ae47ff23867b9ca.png)

Step 2:

On Swagger documentation screen, click on Authorize button

![](media/6294147184ff3d0609e984e275a5637d.png)

Step 3:

On Authorization screen, provide the AIMS360 Operator Username, password, copied
Client ID and secret under Authorization Header. Click on Authorize button.

Note: AIMS360 Operator should be an active API User.

![](media/a540e529f7e7114ac8878b1f39484aee.png)

Step 4:

On successful validation of the provided details, bearer token will be generated
and configured.

![](media/c7c3e58b570c397cadcebdff59d5ec49.png)

Step 5:

After successful authentication, close the Authorization screen and now you are
ready to access the AIMS360 APIs.
