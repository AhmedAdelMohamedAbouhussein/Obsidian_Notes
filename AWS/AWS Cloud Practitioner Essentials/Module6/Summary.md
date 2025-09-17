All right so to recap, Amazon S3 excels at scalable object storage for web assets backups and more. Amazon EBS provides block level storage needed for EC2 instances and databases. And Amazon EFS offers managed shared file systems from workloads that require rapid simultaneous access to files.

## Amazon EC2 Storage

- **[Amazon EC2 Instance Store User Guide]**
    - Temporary storage option directly attached to the host computer of an EC2 instance.
    - High-performance but **non-persistent** storage.

## Amazon Elastic Block Store (EBS)

- **[Amazon Elastic Block Store (Amazon EBS)]**
    - Scalable block storage service.
    - Persistent, high-performance volumes attachable to EC2 instances.
        
- **[Amazon Elastic Block Store (Amazon EBS) FAQ]**
    - Frequently asked questions about EBS.
        
- **[Amazon EBS Snapshots User Guide]**
    - Point-in-time backups of EBS volumes.
    - Enables data protection and restoration.
        
- **[Amazon Data Lifecycle Manager User Guide]**
    - Automates creation, retention, and deletion of EBS snapshots.

## Amazon Simple Storage Service (S3)

- **[Amazon Simple Storage Service (Amazon S3)]**
    - Scalable cloud storage for storing and retrieving data from anywhere.
        
- **[Amazon Simple Storage Service (Amazon S3) FAQ]**
    - Frequently asked questions about S3.
        
- **[Amazon S3 Storage Classes]**
    - Multiple storage classes tailored for performance vs. cost.
    - Options include frequent access, infrequent access, and archival.
        
- **[Amazon S3 Versioning User Guide]**
    - Keeps multiple versions of objects.
    - Provides recovery from accidental deletions or overwrites.
        
- **[Amazon S3 Buckets User Guide]**
    - Buckets act as containers for securely storing and managing data.

## Amazon Elastic File System (EFS)

- **[Amazon Elastic File System (Amazon EFS)]**
    - Fully-managed, scalable file storage.
    - Shared data access for multiple AWS resources without capacity planning.
        
- **[Amazon Elastic File System (Amazon EFS) FAQ]**
    - Frequently asked questions about EFS.

## Amazon FSx

- **[Amazon FSx]**
    - Fully managed file storage service.
    - Supports Windows File Server, Lustre, NetApp ONTAP, and OpenZFS.
        
- **[Amazon FSx for Windows File Server]**
    
    - Reliable, high-performance file storage compatible with Windows apps.
        
- **[Amazon FSx for NetApp ONTAP]**
    
    - Advanced data management with Windows + Linux workload compatibility.
        
- **[Amazon FSx for OpenZFS]**
    
    - High-performance, scalable storage using ZFS.
        
- **[Amazon FSx for Lustre]**
    
    - Fast data access for compute-intensive workloads.

## AWS Storage Gateway

- **[AWS Storage Gateway]**
    - Hybrid cloud storage integrating on-premises and AWS services.
        
- **[Amazon S3 File Gateway]**
    - Provides local file access to S3 objects.
    - Caches frequently accessed data for faster retrieval.
        
- **[Tape Gateway]**
    - For backup data to S3.
    - Maintains compatibility with existing tape-based backup systems.
        
- **[Volume Gateway]**
    - Provides iSCSI block storage volumes.
    - Supports **cached mode** and **stored mode**.