# Message Queues (MQ)

### Meaning

A **Message Queue** is a **communication method between applications or services** where messages are **stored in a queue** until the recipient is ready to process them.

- Enables **asynchronous communication**.
- Common in **distributed systems and microservices**.

---

## 1. How Message Queues Work

1. **Producer** sends a message to the queue    
2. **Queue** stores messages in order (FIFO — first in, first out).
3. **Consumer** retrieves and processes the messages.

**Key feature:** Producer and consumer **do not need to interact at the same time**.

---

## 2. Benefits

- **Decoupling:** Producer and consumer can work independently.    
- **Scalability:** Multiple consumers can process messages in parallel.
- **Reliability:** Messages can be persisted if the consumer is offline.
- **Load leveling:** Smooths out bursts of messages.

---

## 3. Common Patterns

1. **Point-to-Point (Queue)**
    
    - One producer → One consumer        
    - Example: Job processing queue
    
2. **Publish-Subscribe (Topic)**
    
    - One producer → Multiple consumers    
    - Example: Notifications, chat messages
        
---

## 4. Popular Message Queue Systems

- **RabbitMQ**
- **Apache Kafka**
- **Amazon SQS**
- **ActiveMQ**

---

## 5. Memory Hook

- Think: **“Mailbox for programs”**    
- Producer drops a message → Consumer picks it up → decoupled communication

---

## 6. One-Line Exam Answer

> A message queue is a system that stores messages sent by producers until consumers can process them, enabling asynchronous and decoupled communication between applications.