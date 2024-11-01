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
