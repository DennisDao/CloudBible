## APIM

- API gateway or reverse proxy service provided by Microsoft
- APIM provides several ways to secure access
  - Subscription key
  - Client certficate 
  - Restriction by Ip address
  - Oauth 2 Protocol, Validate JWT bearer token
- Used to secure backend service
- Backend can be Rest APIs, Azure Logics apps
- Polices are a collection of statement executed sequentially
   - Front-end -> Inbound -> Backend -> Outbound

## Contract Management 
APIM provicdes a management plan (interface) that allows you to manage and secure APIs and products.
The management plan allows you to perform the following
- Exposing APIs to internal or external users
- Rate Limiting and throttling by subscription
- Monitoring and Analytics (gain insight into how your APIs is being used)
- Access Control - Ensuring only authorized users can access APIS often via Oauth 2.0 or other authentication methods.
- Allow you to version different APIs. 


