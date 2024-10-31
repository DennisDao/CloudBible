## Service Bus

- A pull model, message needs to be pulled
- Fire but don't forget (The publisher needs to recieved and acknowledgement whether the message was handled) `await args.CompleteMessageAsync(args.Message)`
- A message broker which allows for one-to-many communications (pub-sub)
- A publisher sends a message with a topic
- A message can be routed to many subscription. 
- Ideal for decoupled system where reciever and publisher dosen't need to know about one another.
- Messages are stored in queues
- Support message size of 256KB (Standard Tier) and 100MB (premimum tier)
- Has more advance feature over Azure Queue Storage (More expensive)
- Has ordering capabilities using Queue (FIFO) which is not avaliable with Queue Storage
- Message has a TTL (Time to live)
- You can locked a message (this pause the TTL)
- Supported dead letter queue for undelivered messages (user can view the content of the message)
- Messages can be filter using SQL Filter, Boolean Filter and Correlation Filter.
- 

# Message Methods
- Queues: These are used for one-to-one communication. A message sent to a queue is received and processed by a single consumer. This is ideal for scenarios where you need to ensure that each message is processed only once.
  - An example of a queue is customers at a supermarket, where the first customer to reach the cashier gets served, and the rest needs wait in line
  - The benefits of queue is that sender and reciever operates at different pace
- Topics and Subscriptions: These enable one-to-many communication. A message sent to a topic can be received by multiple subscribers through their subscriptions. This is useful for scenarios where multiple consumers need to receive the same message.
  - Topics are ideal for parallel processing, for instance a online shopping website, for example a customer places an order and the message is sent to multiple consumers, there might be multiple consumer that is intrested in the event for instance a shipping process, a delievery process, a invetory process etc.. 
