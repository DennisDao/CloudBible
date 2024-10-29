## Service Bus

- A message broker which allows for one-to-many communications (pub-sub)
- A publisher sends a message with a topic
- Multiple reciever can recieve a copy of the message via their subscription. 
- Ideal for decoupled system where reciever and publisher dosen't need to know about one another.
- Messages are stored in queues
- Support message size of 256KB (Standard Tier) and 100MB (premimum tier)
- Has more advance feature over Azure Queue Storage (More expensive)
- Has ordering capabilities (FIFO) which is not avaliable with Queue Storage
