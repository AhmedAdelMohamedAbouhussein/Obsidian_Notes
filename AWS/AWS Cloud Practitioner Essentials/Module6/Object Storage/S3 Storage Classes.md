Amazon S3 offers various storage classes to suit a variety of workloads with specific performance, access, resiliency, and cost requirements. They're also designed to address data residency requirements, unpredictable access patterns, archival storage needs, and offer the most cost-effective options for different access patterns.

1.   S3 Standard

S3 Standard is considered general-purpose storage for cloud applications, dynamic websites, content distribution, mobile and gaming applications, and big data analytics. When you upload an object to Amazon S3 without specifying a storage class, the object is added to S3 Standard by default.

2. S3 Intelligent-Tiering

This tier is useful if your data has unknown or changing access patterns. S3 Intelligent-Tiering stores objects in three tiers: a frequent access tier, an infrequent access tier, and an archive instant access tier. Amazon S3 monitors access patterns of your data and automatically moves your data to the most cost-effective storage tier based on frequency of access.

3. S3 Standard Infrequent Access (Standard-IA)

S3 Standard-Infrequent Access (S3 Standard-IA) is for data that is accessed less frequently but requires rapid access when needed. S3 Standard-IA offers the high durability, high throughput, and low latency of S3 Standard, with a low per-GiB storage price and per-GiB retrieval fee. This storage tier is ideal if you want to store long-term backups, disaster recovery files, and so on.

4.  S3 One Zone Infrequent Access (One Zone-IA)

S3 One Zone-Infrequent Access (S3 One Zone-IA) stores data in a single Availability Zone, reducing costs compared to S3 Standard-IA, which uses three zones. This storage class suits customers seeking affordable storage for infrequently accessed data without high availability needs. It's perfect for storing secondary backups or easily recreatable data.

5. S3 Express One Zone

S3 Express One Zone stores data in a single Availability Zone. It was purpose-built to deliver consistent single-digit millisecond data access for your most frequently accessed data and latency-sensitive applications. S3 Express One Zone delivers data access speed up to 10x faster and request costs up to 80% lower than S3 Standard.

6.   S3 Glacier Instant Retrieval

Use S3 Glacier Instant Retrieval for archiving data that is rarely accessed and requires millisecond retrieval. Data stored in this storage class offers a cost savings of up to 68 percent compared to the S3 Standard-IA storage class, with the same latency and throughput performance.

7. S3 Glacier Flexible Retrieval

S3 Glacier Flexible Retrieval offers low-cost storage for archived data that is accessed 1–2 times per year. With S3 Glacier Flexible Retrieval, your data can be accessed in as little as 1–5 minutes using an expedited retrieval. You can also request bulk retrievals in up to 5–12 hours at no additional cost. It's an ideal solution for backup, disaster recovery, offsite data storage needs, and for when some data occasionally must be retrieved in minutes.

8. S3 Glacier Deep Archive

S3 Glacier Deep Archive is the lowest-cost Amazon S3 storage class. It supports long-term retention and digital preservation for data that might be accessed once or twice per year. Data stored in the S3 Glacier Deep Archive storage class has a default retrieval time of 12 hours. It is designed for customers that retain data sets for 7–10 years or longer, to meet regulatory compliance requirements. Examples include those in highly regulated industries, such as financial services, healthcare, and public sectors.

9.   S3 Outposts

Amazon S3 Outposts delivers object storage to your on-premises AWS Outposts environment using Amazon S3 APIs and features, and serves workloads with local data residency requirements. It also helps maintain optimal performance when data must remain in close proximity to on-premises applications.