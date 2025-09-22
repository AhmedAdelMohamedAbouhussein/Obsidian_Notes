
Relational databases store data in a way that relates it to other pieces of data, and they use structured query language, or SQL, to manage and query data. This approach stores data in an easily understandable, consistent, and scalable way that works great for applications requiring structured data management.

AWS offers fully managed relational database solutions that remove the burden of database administration while maintaining high availability and security. AWS relational databases support popular database engines like MySQL, PostgreSQL, and Oracle, making it easier to migrate existing databases to AWS.


![[Pasted image 20250918140523.png]]


Amazon Relational Database Service (Amazon RDS)

Amazon RDS is a _managed_ relational database service that handles routine database tasks such as backups, patching, and hardware provisioning. Amazon RDS supports multiple database instance class types that optimize for memory, performance, or input/output (I/O).

To improve data resilience, Amazon RDS offers Multi-AZ deployment and automated backups, but you can also manually create backups using DB snapshots. These are full backups of your entire database instance, which can be useful for specific point-in-time recovery or long-term data archiving purposes. Amazon RDS offers security features including network isolation, encryption in transit, and encryption at rest. You can readily scale database resources vertically or horizontally as needed.

### Supported database engines

Amazon RDS supports different database engines, including Amazon Aurora, MySQL, PostgreSQL, Microsoft SQL Server, MariaDB, and Oracle Database.

### Use cases

Some examples of practical use cases for Amazon RDS are web applications, enterprise workloads, and product inventories for e-commerce platforms.

![[Pasted image 20250918140735.png]]


Amazon Aurora

Aurora is a managed relational database designed to help reduce unnecessary I/O operations. It's compatible with MySQL and PostgreSQL, provides high performance and availability, and automatically scales alongside your workloads. Aurora replicates data across multiple Availability Zones for enhanced durability and fault tolerance, and features automated backups, encryption at rest, and continuous monitoring.

Aurora provides a high-performance, highly available storage architecture that offers up to five times the throughput of standard MySQL.
### Use cases

Some examples of practical use cases for Aurora are gaming applications, media and content management, and real-time analytics.

### Benefits
![[Pasted image 20250918141135.png]]

![[Pasted image 20250918140928.png]]

AWS Database Migration Service

a fully managed service that helps you migrate databases to AWS **quickly, securely, and with minimal downtime**. It supports both **homogeneous migrations** (e.g., Oracle → Oracle, MySQL → MySQL) and **heterogeneous migrations** (e.g., Oracle → PostgreSQL, SQL Server → Amazon Aurora).