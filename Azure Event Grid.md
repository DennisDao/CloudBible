## Azure Event Grid

- Another pub-sub service, Fire and Forget
- Main purpose is for routing events 
- Azure Event Grid, Event Hub and Service Bus are somewhat similar with overlapping functionalities.
- An event can be viewed as a lightweight notification of a condition or a state change
- The publisher has no expectation on what the consumer do.
- Charge by 64KB increment for instance a message size of 65KB would be charge as two seperate events.
- Events can be filtered
- Custom events
- System events built-in (blob changed, azure resource change) 
  ## Building block
  - Event - What happend.
  - Source - What trigged the event
  - Topic - End-point where publisher sends the event
     - Topic Name: `ecommerce-orders`
     - Event Type: `OrderCreated` `OrderShipped` `OrderDelivered`
  - Subscription - any endpoint that can handle HTTP Request such as Azure Functions, Logic Apps
       - `az eventgrid event-subscription create \
        --resource-group myResourceGroup \
        --topic-name myCustomTopic \
        --name mySubscription \
        --endpoint https://myendpoint.com/api/events`
   - Handler - the app or services that react to the event
