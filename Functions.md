## Azure functions

- A small piece of code that's triggered by an event (serverless or service on demand)
- Commonly triggered via a HTTP, database changes or messages from queue
- Can only be triggered only to a single event
- Has optional input and output bindings
- 

## Durable functions
- Is an extension to azure function
- Unlinke azure functions it maintain states (state is preserve after a restart or pause)
- Durable function maintain state by (Check-point, orchestration history, Durable task framework, Azure storage)
