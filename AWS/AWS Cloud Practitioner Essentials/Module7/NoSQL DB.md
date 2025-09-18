NoSQL databases are sometimes referred to as _non-relational databases_ because their structures are different than relational databases like Amazon RDS. Instead of row and column relationships, NoSQL databases build a structure for the data that they contain using _key-value pairs_ instead. With key-value pairs, data is organized into items identified by unique keys.

Each key has one or more associated attributes, or values, that represent various characteristics of the data. You can think of a key as a word entry in a dictionary, and the value as its associated definition. Not every item in the table has to have the same attributes, and you can add or remove attributes at any time.


Amazon DynamoDB

DynamoDB is a fully managed NoSQL database service that provides fast and predictable performance for both document and key-value data structures. It's a powerful and incredibly fast database option for use cases that require a flexible schema, and is ideal for applications that require high performance and seamless scaling.

DynamoDB seamlessly scales alongside your data without impacting performance, which means that you only pay for the resources that you use. It also includes built-in security features for enhanced protection, and automatically spreads your data across multiple servers to handle your workload.

### Use cases

Some examples of practical use cases for DynamoDB are gaming platforms, financial service applications, and mobile applications with global user bases.

![[Pasted image 20250918142523.png]]

![[Pasted image 20250918142008.png]]

![[Pasted image 20250918142113.png]]

You can even use DynamoDB for globally distributed applications. That particular feature is called DynamoDB global tables. An awesome example of this feature in use is Amazon Prime Day 2024. For those 48 hours, there were tens of trillions of calls to the DynamoDB API. It peaked at 146 million requests per second.