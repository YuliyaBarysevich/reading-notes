# Class 14

**Resources:**

- [Amazon SQS](https://aws.amazon.com/about-aws/whats-new/2016/11/amazon-sqs-introduces-fifo-queues-with-exactly-once-processing-and-lower-prices-for-standard-queues/#:~:text=FIFO%20queues%20have%20essentially%20the,being%20received%20by%20message%20consumers/)
- [Tutorials Point](https://www.tutorialspoint.com/design_pattern/observer_pattern.htm)

## Review, Research, and Discussion

1. What’s the difference between a FIFO and a standard queue?
    - FIFO queues have essentially the same features as standard queues, but provide the added benefits of supporting ordering and exactly-once processing. FIFO queues provide additional features that help prevent unintentional duplicates from being sent by message producers or from being received by message consumers.
2. How can the server be assured a message was properly received?
    - Send a response status
3. What classic design pattern is best represented by event driven programming?
    - Observer pattern. It is used when there is one-to-many relationship between objects such as if one object is modified, its depenedent objects are to be notified automatically. 
4. How do you test an event driven system?
    - unit tests, service tests, and end-to-end tests

## Vocabulary Terms


1. [FIFO Queue](https://queue-it.com/queue-first-in-first-out/)
    - A FIFO queue is a queue that operates on a first-in, first-out (FIFO) principle. This means that the request (like a customer in a store or a print job sent to a printer) is processed in the order in which it arrives. A first-come, first-served line is the most common type of queue that we join in our everyday lives and is generally accepted as the fairest way to operate a queue.
2. [Pub/Sub](https://ably.com/topic/pub-sub)
    - Publish Subscribe Design Pattern. It provides a framework for exchanging messages between publishers and subscribers. This pattern involves the publisher and the subscriber relying on a message broker that relays messages from the publisher to the subscribers. The host (publisher) publishes messages (events) to a channel that subscribers can then sign up to.