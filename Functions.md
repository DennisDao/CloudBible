## Azure functions

- A small piece of code that's triggered by an event (serverless or service on demand)
- They are stateless, meaning they do not maintain state between executions
- Commonly triggered via a HTTP, database changes or messages from queue
- Can only be triggered only to a single event
- Has optional input and output bindings
  
## Durable functions
- Is an extension to azure function
- Unlinke azure functions it maintain states (state is preserve after a restart or pause)
- State is mantained by a Orchestrator functions, which is a function that calls other functions or in other words used to cordinates the entire workflow
- Durable function maintain state by (Check-point, orchestration history, Durable task framework, Azure storage)
- State can be stored externally using Azure Storage (blob, tables, queue), Azure Cosmos Db, Azure SQL Database
- Event sourcing (history) is used to build up the current state
- `InstanceId` is assigned to each orchestration instance and it's used to build up the current state and it's a vital bit of information, At runtime the `InstanceId` is used to get the event history table
- `[FunctionName("GetOrchestrationHistory")]
    public static async Task<IActionResult> Run(
        [HttpTrigger(AuthorizationLevel.Function, "get", Route = "orchestrations/{instanceId}")] HttpRequest req,
        [DurableClient] IDurableOrchestrationClient client,
        string instanceId,
        ILogger log)
    {
        var status = await client.GetStatusAsync(instanceId, showHistory: true, showHistoryOutput: true);
        return new OkObjectResult(status);
    }`
- There are four patterns
   - Function Chaining: Executing a sequence of functions in a specific order. Each function’s output is the input for the next.
   - Fan-out/Fan-in: Running multiple functions in parallel and then aggregating their results.
   - Async HTTP APIs: Managing long-running HTTP requests by breaking them into smaller, manageable tasks.
   - Human Interaction: Pausing workflows until an external event, like user input, occurs.

