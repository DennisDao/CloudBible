## Authentication

- Authorization code flow
  - Used by public clients (application that are client side that cant be trusted to keep application secret)
  - Redirect the user to the identity provider for authentication (Azure AD, Google, Facebook)
  - Once authenticated the user is redirected to a callback URI
  - The callback uri contains the authorization code which can be exchange for an access token
  - involves a user aka user impersonation or requesting information on the user behalf
 
 - Client credential flow
   - Server to server communication (back-end)
   - Authorized the app rather than the user
   - Permissions are granted directly to the application itself by an administrator
   - Can you `client_id` and `client_scecret` (not secure, instead use certficate base authentication)

- Service principal
  - Is a identity created in Azure AD for applcations and hosted services
  - Is objected stored for a single tenant
  - Services principals can be assigned roles and permisson to access certain azure resources (RBAC)
  - You can add the service principal to a azure storage account
