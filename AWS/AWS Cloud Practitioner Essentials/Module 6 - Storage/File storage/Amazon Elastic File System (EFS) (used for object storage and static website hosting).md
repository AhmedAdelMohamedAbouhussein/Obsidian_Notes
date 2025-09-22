Amazon EFS is a fully managed, scalable file storage service for use with AWS cloud services and on-premises resources. It operates using the _Linux Network File System (NFS) protocol_, and _automatically scales_ to petabytes as you add or remove files without disrupting applications. EFS is designed to support a wide variety of workloads and can be accessed by _multiple EC2 instances simultaneously_.

![[Pasted image 20250917163806.png]]

With EFS, you can keep existing file systems in place while AWS does all the heavy lifting of the scaling and the replication. EFS makes it possible for you to have multiple instances accessing the data in EFS at the same time. It scales up and down as needed without you having to do anything to make that scaling happen.

When you create an EFS filesystem, it comes with pre-configured lifecycle policies that help keep your cloud data cost-optimized. EFS automatically moves data between storage classes based on access patterns, but you have the option to customize the lifecycle policies to fit your storage needs.

![[Pasted image 20250917164023.png]]


Amazon EFS storage classes

With Amazon EFS, you can create and configure file systems quickly without any minimum fee or setup cost. You pay only for the storage used and you can choose from a range of storage classes designed to fit your use case.

1. _EFS Standard_ and EFS Standard-Infrequent Access (Standard-IA)

The _EFS Standard_ and _EFS Standard-Infrequent Access (Standard-IA)_ storage classes offer Multi-AZ resilience and the highest levels of durability and availability. They have a higher cost associated with them due to higher availability and durability.

2. _EFS One Zone_ and _EFS One Zone-Infrequent Access (EFS One Zone-IA)_

The _EFS One Zone_ and _EFS One Zone-Infrequent Access (EFS One Zone-IA)_ provide additional savings by saving your data in a single Availability Zone. By using just one Availability Zone, you can reduce your storage costs when compared to the Standard EFS storage classes.

3.  _EFS Archive_ storage Class

The _EFS Archive_ storage class is cost-optimized for data that is accessed only a few times a year or less and that does not need the sub-millisecond latencies of EFS Standard. EFS Archive offers a storage price up to 50% lower compared to EFS Infrequent Access, providing a more cost-optimized experience for cold, rarely-accessed data.


Amazon EFS data lifecycle

You can further optimize Amazon EFS storage costs by automatically moving data between storage classes based on usage patterns. You can create lifecycle policies that determine when and how files transition between different storage tiers. These automated policies help ensure your data resides in the most cost-effective storage class without manual intervention.

![[Pasted image 20250917164404.png]]
![[Pasted image 20250917164412.png]]
![[Pasted image 20250917164418.png]]