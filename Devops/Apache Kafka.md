## 1. Introduction to Apache Kafka

**Apache Kafka** is a **distributed event-streaming platform** used for:

- High-throughput
- Fault-tolerant
- Real-time data streaming

Kafka was originally developed by **LinkedIn** and later open-sourced under the **Apache Software Foundation**.

### What Kafka Solves

Kafka is designed to handle:

- Massive volumes of data
- Real-time data pipelines
- Event-driven architectures
- Asynchronous communication between systems

Kafka does **not handle request–response for every message**; it **stores messages in partitions**, and consumers **pull them asynchronously** whenever they want.

---

## 2. Core Use Cases of Kafka

- Real-time log aggregation
- Messaging systems
- Event-driven microservices
- Data streaming and analytics
- Monitoring and metrics pipelines
- Data integration between systems

---

## 3. Kafka Architecture Overview

Kafka follows a **distributed, publish–subscribe model**.

### High-level Architecture

![[Pasted image 20251218151929.png]]`

Kafka is composed of several **services and components**, each with a specific responsibility.

---

# 4. Kafka Core Components

---

## 4.1 Kafka Broker

### Definition

A **broker** is a Kafka server that:

- Stores data
- Serves producers and consumers
- Handles replication and fault tolerance

### Key Points

- A Kafka cluster consists of **multiple brokers**
- Each broker has a unique **broker ID**
- Brokers store data on disk (persistent storage)

### Responsibilities

- Receive messages from producers
- Store messages in partitions (A **distributed, persistent log**)
- Serve messages to consumers
- Replicate data to other brokers

---

## 4.2 Kafka Topic

### Definition

A **topic** is a **logical channel** where messages are published.

### Characteristics

- Topics are split into **partitions**
- Topics are immutable (messages cannot be changed)
- Topics can have **retention policies**

Example:

`topic: user-events`

---

## 4.3 Kafka Partition

### Definition

A **partition** is an ordered, immutable sequence of records.

### Why Partitions Exist

- Enable **parallelism**
- Improve scalability
- Distribute load across brokers

### Important Rules

- Order is guaranteed **only within a partition**
- Each partition is stored on one broker (leader)
- Replicas exist on other brokers

---

## 4.4 Kafka Record (Message)

A Kafka message consists of:

- **Key** (optional)
- **Value** (actual data)
- **Timestamp**
- **Headers**

Example:

`(key, value) (userId, "UserLoggedIn")`

---

## 4.5 Offset

### Definition

An **offset** is a unique, sequential ID assigned to each record **within a partition**.

### Key Concepts

- Offset identifies a message’s position
- Offsets are **per partition**
- Consumers track offsets to know what they have read

Example:

`Partition 0 → offsets: 0, 1, 2, 3`

---

# 5. Kafka Producers

---

## 5.1 Kafka Producer

### Definition

A **producer** is an application that **publishes messages** to Kafka topics.

### Responsibilities

- Serialize data
- Choose topic and partition
- Send records to brokers

---

## 5.2 Message Routing

Kafka decides partition assignment using:

1. Message key (hash-based)
2. Round-robin (if no key)
3. Custom partitioner

### Key-based Ordering

- Same key → same partition
- Preserves order for that key

---

## 5.3 Producer Acknowledgements (acks)

| acks | Meaning                                    |
| ---- | ------------------------------------------ |
| 0    | No confirmation                            |
| 1    | Leader broker confirms                     |
| all  | All replicas confirm (strongest guarantee) |


---

## 5.4 Producer Reliability Features

- Retries
- Idempotent producers
- Exactly-once semantics (with transactions)

---

# 6. Kafka Consumers

---

## 6.1 Kafka Consumer

### Definition

A **consumer** reads messages from Kafka topics.

### Characteristics

- Pull-based model
- Can read at its own pace
- Tracks offsets

---

## 6.2 Consumer Groups

### Definition

A **consumer group** is a set of consumers that cooperate to read a topic.

### Rules

- Each partition is read by **only one consumer per group**
- Multiple consumer groups can read the same topic independently

Example:

`Topic with 3 partitions Consumer Group A → 3 consumers Consumer Group B → 1 consumer`

---

## 6.3 Offset Management

Offsets can be:

- Automatically committed
- Manually committed

Stored in:

`__consumer_offsets topic`

---

## 6.4 Rebalancing

Occurs when:

- A consumer joins or leaves
- Topic partitions change

Kafka redistributes partitions among consumers.

---

# 7. Kafka Replication & Fault Tolerance

---

## 7.1 Leader and Followers

- Each partition has:
    
    - **1 leader**
    - **Multiple followers (replicas)**

### Leader

- Handles reads and writes

### Followers

- Replicate data
- Take over if leader fails

---

## 7.2 In-Sync Replicas (ISR)

- Replicas fully caught up with the leader
- Only ISR replicas are eligible for leader election

---

## 7.3 Fault Tolerance

Kafka survives:

- Broker failures
- Network failures
- Consumer crashes

---

# 8. Kafka Storage Model

---

## 8.1 Log Segments

- Each partition is stored as a **log**
- Logs are split into **segments**
- Segments are immutable

---

## 8.2 Retention Policies

Kafka does **not delete data immediately after consumption**.

Retention can be based on:

- Time (e.g., 7 days)
- Size (e.g., 10GB)
- Compaction (latest value per key)

---

## 8.3 Log Compaction

Keeps:

- Latest record per key  
    Deletes:
- Older records with same key

Used for:

- State storage
- Configuration topics

---

# 9. Kafka Services & Ecosystem

---

## 9.1 Apache ZooKeeper (Legacy)

### Role (Before Kafka 3.x)

- Broker metadata
- Leader election
- Cluster coordination
    

### Status

⚠️ Being phased out

---

## 9.2 Kafka KRaft (Modern)

### Definition

**KRaft (Kafka Raft)** replaces ZooKeeper.

### Responsibilities

- Metadata management
- Leader election
- Cluster coordination

### Benefits

- Simpler architecture
- Better performance
- Easier operations

---

## 9.3 Kafka Connect

### Definition

Kafka Connect is a **data integration service**.

### Purpose

- Move data **into Kafka** (Source Connectors)
- Move data **out of Kafka** (Sink Connectors)

### Examples

- MySQL → Kafka
- Kafka → Elasticsearch
- Kafka → S3

### Key Features

- Scalable
- Fault-tolerant
- Config-driven (no code)

---

## 9.4 Kafka Streams

### Definition

Kafka Streams is a **stream-processing library**.

### Purpose

- Real-time transformations
- Aggregations
- Joins

### Characteristics

- Runs inside your application
- Uses Kafka topics as input/output
- Exactly-once processing support

---

## 9.5 Schema Registry (Confluent)

### Definition

Manages schemas for Kafka messages.

### Supported Formats

- Avro
- Protobuf
- JSON Schema

### Benefits

- Data compatibility
- Schema evolution
- Strong typing

---

# 10. Kafka Delivery Semantics

|Mode|Description|
|---|---|
|At most once|Messages may be lost|
|At least once|Messages may be duplicated|
|Exactly once|No loss, no duplicates|

---

# 11. Kafka Security

Kafka supports:

- SSL/TLS (encryption)
- SASL (authentication)
- ACLs (authorization)

---

# 12. Kafka Performance Characteristics

- High throughput (millions of messages/sec)
- Low latency
- Disk-based (sequential writes)
- Zero-copy transfer

---

# 13. Kafka vs Traditional Messaging Systems

|Feature|Kafka|Traditional MQ|
|---|---|---|
|Data retention|Yes|No|
|Replay messages|Yes|No|
|Scalability|Very high|Limited|
|Ordering|Per partition|Global|

---

# 14. Kafka in Microservices

Kafka is commonly used as:

- Event backbone
- Async communication layer
- Event sourcing system
- CQRS architecture support

---

# 15. Summary

Apache Kafka is:

- A distributed event-streaming platform
- Highly scalable and fault-tolerant
- Suitable for real-time and big data systems

It consists of:

- Brokers
- Topics & partitions
- Producers & consumers
- Connect, Streams, Schema Registry
- ZooKeeper (legacy) / KRaft (modern)

---

## 📌 One-Line Exam Summary

> Apache Kafka is a distributed, fault-tolerant event streaming platform used for real-time data pipelines and event-driven architectures.
