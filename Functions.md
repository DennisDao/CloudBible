## Azure functions

- A small piece of code that's triggered by an event (serverless or service on demand)
- They are stateless, meaning they do not maintain state between executions
- Commonly triggered via a HTTP, database changes or messages from queue
- Can only be triggered only to a single event
- Has optional input and output bindings
  
## Durable functions
- Is an extension to azure function
- Unlinke azure functions it maintain states (state is preserve after a restart or pause)
- State is mantained by a Orchestrator functions, which is a function that calls other functions
- Durable function maintain state by (Check-point, orchestration history, Durable task framework, Azure storage)
- State can be stored externally using Azure Storage (blob, tables, queue), Azure Cosmos Db, Azure SQL Database
- Event sourcing (history) is used to build up the current state


