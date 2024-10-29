## Service Bus

- Fire but don't forget (The publisher needs to recieved and acknowledgement whether the message was handled) 
- A message broker which allows for one-to-many communications (pub-sub)
- A publisher sends a message with a topic
- A message can be routed to many subscription. 
- Ideal for decoupled system where reciever and publisher dosen't need to know about one another.
- Messages are stored in queues
- Support message size of 256KB (Standard Tier) and 100MB (premimum tier)
- Has more advance feature over Azure Queue Storage (More expensive)
- Has ordering capabilities (FIFO) which is not avaliable with Queue Storage

# Message Mechanisim
- Queues: These are used for one-to-one communication. A message sent to a queue is received and processed by a single consumer. This is ideal for scenarios where you need to ensure that each message is processed only once.
- Topics and Subscriptions: These enable one-to-many communication. A message sent to a topic can be received by multiple subscribers through their subscriptions. This is useful for scenarios where multiple consumers need to receive the same message.
