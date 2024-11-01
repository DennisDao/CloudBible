## Where to store Json Payload in Azure 
- You can store JSON file in blob storage
- You can store JSON data in ComsmosDb if you need to query of fetch the data
- You can store the data in Azure SQL Database as JSON string

## How to retire a azure functions 
- You can disable or retire an azure function using the azure portal
- You can disable a azure function locally using `local.settings.json` ` "AzureWebJobs.QueueTrigger.Disabled": true`

## Question 
- Constant vs Readonly
  - Constant defined at compiled time and cannot be change thereafter
  - Constant Are implicity static members
  - Can be declared at the time of decleration or via constructor and cannot be changed at runtime or after intialize
 
- Yield operator
  - The yield keyword in C# helps you create a sequence of values that you can iterate over, one at a time

- IEnumerable vs IQueryable
  - IEnumerable - Designed for iterating over in-memory collections like arrays, lists, etc
  - IQueryable - Designed for querying out-of-memory data sources, such as databases

- IDisposable
  - Release unmanaged resources like file handles, database connections, or network connections when they are no longer needed
  - Works outside of the garbage collection cycle
  - Can be used in a using statement.
    
- DI lifecycles 
   - Scoped - created once per request, same instance is shared throughout the process
   - Singleton - There will only be 1 instance ever
   - Transient - The object will be created whenever it's requested, for instance at the controller layer a new instance is created and at the service layer a new instance is created.

- Git Commands 
   - https://www.freecodecamp.org/news/10-important-git-commands-that-every-developer-should-know/
 
- Middleware
  - Middleware are code embed into the request pipeline, once the code or delgated is invoked it passes the excution to the next one.
  - Authentication and authoization are middleware

- Database normizaltion
   - Is the process of organizing data in a relational database to redundancy and improve data integrity, this is achieve with Normal forms which is used to safeguard the database from update and delete annomalies. 
  
