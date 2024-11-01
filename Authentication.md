## Authentication

- Authorization code flow
  - Used by public clients (application that are client side that cant be trusted to keep application secret)
  - Redirect the user to the identity provider for authentication (Azure AD, Google, Facebook)
  - Once authenticated the user is redirected to a callback URI
  - The callback uri contains the authorization code which can be exchange for an access token
  - involves a user aka user impersonation or requesting information on the user behalf (Delegated permission - Access API as the signed in user)
 
 - Client credential flow
   - Server to server communication (back-end)
   - Authorized the app rather than the user
   - Permissions are granted directly to the application itself by an administrator
   - It make use of `client_id` and `client_scecret` (not secure, instead use certficate base authentication)
   - Service princpial needs to created in Azure AD

- Service principal
  - Is a identity object created in Azure AD for applcations and hosted services
  - Is object stored for a single tenant in AAD
  - Services principals can be assigned roles and permisson to access certain azure resources (RBAC)
  - You can add the service principal to any azure service like storage account. 

- System assigned Identity
  - Tied to a specfic azure resources
  - When the azure resources is deleted the system assigned identity is also deleted
  - Credentials rotation is managed automatically
  - Authentication happens automatically
  - Quick and easy to set up
    - Create a system identity form a VM
    - Go target resource
    - Grant the access to the resource by specifying the VM identity
   
- User Assigned Identity
  - Standalone identity idependant of the azure resource
  - Can be assigned to multiple resource like VM
  - When the azure resource is deleted the user assigned identity it not deleted
 

## How authentication works

- Managed Identities: Within the Azure ecosystem managed identities is uses as a form of authentication, services can authenticated to one another without needing to store credential in code. 
- Azure Activite Directory (AAD): Service that's not within the Azure ecosystem can authenticate using AAD by using OAuth 2, this is commonly used for webapps, APIs and daemon services that need to interact with Azure resources.
- Connection strings: API Keys and connection string can be used as form of authentication
  
