SQS : Amazon Simple Queue Service
SNS : Amazon Notification Service

Amazon SQS is a message queuing service that facilitates reliable communication between software components. It can send, store, and receive messages at any scale, making sure messages are not lost and that other services don't need to be available for processing. In Amazon SQS, an application places messages into a queue, and a user or service retrieves the message, processes it, and then removes it from the queue.

Payload: Data with in a message
Amazon SQS queues: where messages are placed until they are processed

![[Pasted image 20250914183141.png]]


Amazon SNS is a publish-subscribe service that publishers use to send messages to subscribers through SNS topics. In Amazon SNS, subscribers can include web servers, email addresses, Lambda functions, and various other endpoints. 