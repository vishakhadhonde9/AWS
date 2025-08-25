# SNS (Simple Notification Service) -
- Amazon SNS is a fully managed messaging service in AWS that is used to send messages or notifications.
- It works on a Publish–Subscribe model.

## Terminologies -
### Topic:
- A logical channel where publishers send messages. All subscribers to the topic get the same message.

### Publisher:
- Entity (app, AWS service, or script) that sends messages to a topic.

### Subscriber:
- Endpoint that receives messages (SQS, Lambda, Email, SMS, HTTP/S, etc.).


## SNS Works in two ways:

# Application to Application (A2A)
- Messages go from one system to another.
- Example: When an order is placed, SNS can notify Lambda (to process order) and SQS (to queue billing).

# Application to Person (A2P)
- Messages go directly to people.
- Example: OTP via SMS, email alerts, or mobile push notifications.


# SQS 
- Simple Queue Service is a fully managed message queuing service provided by AWS.
- It is used when you want applications or services to send, store, and receive messages in a safe and reliable way without depending on each other directly.

## Working -
- A Producer (application/service) sends a message to the queue.
- The message stays safely in the queue until someone takes it.
- A Consumer (another application/service) picks up the message from the queue and processes it.
- This way, even if the consumer is slow or temporarily unavailable, the message will not be lost.

## Types of Queues-
### Standard Queue:
- High throughput (can process unlimited messages).
- Messages may arrive out of order.
- Messages may be delivered more than once.

### FIFO Queue (First-In-First-Out):
- Messages are processed in the exact order they were sent.
- Each message is delivered exactly once.
- Lower throughput compared to Standard queue.
