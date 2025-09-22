## 

Transferring data to and from the AWS Cloud

**Online data transfer**

Several AWS services facilitate online data transfer to the AWS Cloud. In the last lesson, you learned that AWS Database Migration Service (AWS DMS) transfers the database and its data to the AWS Cloud. In this lesson, you will identify services that can help with the considerations of online transfer for other types of data and files.

In this lesson, you will review three services:

- AWS DataSync
    
- AWS Transfer Family
    
- AWS Direct Connect

When you migrate data to the AWS Cloud, there are a few considerations to keep in mind. You need to ensure security (will it get there safely), data validation (will it get there in one piece), scheduling (when is the best time). You would also confirm bandwidth requirements. For the majority of data migration workloads, AWS DataSync will do the job.


> **AWS DataSync**

AWS DataSync is specifically designed for automating and accelerating data transfer. DataSync simplifies and accelerates moving large amounts of data between on-premises storage and AWS storage services like Amazon Simple Storage Service (Amazon S3). It automates many aspects of the transfer process, including running instances, encryption, and network optimization.

**Benefits:** The benefits include streamlining and accelerating secure data migrations. DataSync manages data movement workloads with bandwidth throttling, migration scheduling, task filtering, and task reporting. It also provides rapid data replication.

**Use cases:** You can use DataSync to migrate your data, archive your cold data, and manage hybrid data workflows.

The next service provides fully managed support for file transfers into and out of Amazon S3. It supports many different transfer protocols. A transfer protocol is a set of rules or standards that govern the way data is moved from one location to another.


> **AWS Transfer Family**

The AWS Transfer Family makes it possible to seamlessly manage and share data with simple, secure, and scalable file transfers. This service provides fully managed support for secure file transfers over FTP, Secure File Transfer Protocol (SFTP), File Transfer Protocol Secure (FTPS), and other protocols. It helps you transfer files directly into and out of AWS storage services like Amazon S3 and Amazon EFS.

**Benefits:** The benefits include simplifying the process of setting up and managing file transfers and reducing the need for complex infrastructure management. The Transfer Family provides secure data transfer with encryption and authentication, to ensure data integrity and confidentiality. It is built to scale and streamline workflows.

**Use cases:** You can use the Transfer Family to modernize and manage your file transfers, simplify data sharing with your workforce and partners, and integrate transactional business data into a unified data lake.

You might remember Direct Connect from the networking module. With the bandwidth of a dedicated connection, it is also a great solution for moving your data online to the AWS Cloud when migrating.


> **Direct Connect**

AWS Direct Connect is a service that makes it possible for you to establish a dedicated private connection between your network and virtual private cloud (VPC) in the AWS Cloud. Because it is your dedicated connection, it is a fast, reliable, and secure way to transfer your data or files.

**Benefits:** Direct Connect helps reduce network costs and increase amount of bandwidth.