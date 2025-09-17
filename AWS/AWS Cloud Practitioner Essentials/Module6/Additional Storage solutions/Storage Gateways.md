## 

AWS Storage Gateway

Storage Gateway is a hybrid cloud storage service that makes it possible to seamlessly integrate on-premises environments with AWS Cloud storage. You can use it to extend your local storage to the cloud while maintaining low-latency access to frequently used data.

You can use Storage Gateway to streamline storage management and reduce costs for practical hybrid cloud storage use cases. These include moving backups to the cloud, using on-premises file shares backed by cloud storage, and providing low-latency access to data in AWS for on-premises applications.

![[Pasted image 20250917165834.png]]

## 

Gateway types

Storage Gateway offers three distinct types of gateways to meet different hybrid storage needs. Each gateway type is designed to address specific use cases and workload requirements.

1.  Amazon S3 File Gateway

Amazon S3 File Gateway bridges your local environment with Amazon S3. It provides on-premises applications with access to virtually unlimited cloud storage through familiar file protocols. S3 File Gateway makes it possible to store and retrieve cloud objects using familiar file operations.

When you deploy an S3 File Gateway, it appears to your local systems as a standard file server. Files written to this server are automatically uploaded to Amazon S3 while maintaining local access to recently used data through intelligent caching. This means your applications can continue working with files as they always have while the actual data is securely stored in the AWS Cloud.

2.  Volume Gateway

With Volume Gateway, you create virtual storage volumes while maintaining local access to your data. It essentially functions as a bridge between your on-premises infrastructure and AWS Cloud storage by presenting your cloud data as iSCSI volumes that can be mounted by your existing applications.

Volume Gateway operates in two main configurations:

- _Cached volume mode_ stores primary data in the cloud while frequently accessed data is cached locally for low-latency access.
    
- _Stored volume mode_ locally keeps your complete dataset while asynchronously backing it up to the cloud as EBS snapshots.

3.  Tape Gateway

Tape Gateway makes it possible to replace physical tape infrastructure with virtual tape capabilities while benefitting from the durability and scalability of AWS Cloud storage. Tape Gateway provides an interface that works with existing tape backup software, making the transition from physical tapes to cloud storage seamless.

When you deploy a Tape Gateway, it presents itself to your backup applications as standard tape hardware. Your backup software writes data to these virtual tapes just as it would to physical tapes and stored in Amazon S3. You can also configure Tape Gateway to automatically transition less frequently accessed data to a more cost-effective storage class for long-term retention.