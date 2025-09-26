AWS Backup streamlines data protection across various AWS resources and on-premises deployments by providing a single dashboard for monitoring and managing backups. It eliminates the complexity of managing multiple backup strategies by supporting multiple storage types, including Amazon Elastic Block Store (Amazon EBS) volumes, Amazon Elastic File System (Amazon EFS) file systems, and various databases.

AWS Backup centralizes and automates data protection processes, improving consistency and reducing administrative overhead. It offers flexible scheduling options, encryption capabilities, and cross-Region backup support for enhanced disaster recovery.

### Use cases

Some examples of practical use cases for AWS Backup are centralized disaster recovery, consistent backup policies for compliance requirements, and consolidating multiple backup processes through a single interface.

![[Pasted image 20250918144938.png]]



Automated backups are turned on by default. This backs up your entire DB instance (not just individual databases on the instance) and your transaction logs. When you create your DB instance, you set a backup window that is the period of time that automatic backups occur. Typically, you want to set the window during a time when your database experiences little activity because it can cause increased latency and downtime.  
  
**Retaining backups:** Automated backups are retained between 0 and 35 days. You might ask yourself, “Why set automated backups for 0 days?” The 0 days setting stops automated backups from happening. If you set it to 0, it will also delete all existing automated backups. This is not ideal. The benefit of automated backups that you can do point-in-time recovery.


**Point-in-time recovery:** This creates a new DB instance using data restored from a specific point in time. This restoration method provides more granularity by restoring the full backup and rolling back transactions up to the specified time range.
![[Pasted image 20250926161826.png]]

If you want to keep your automated backups longer than 35 days, use manual snapshots. Manual snapshots are similar to taking Amazon EBS snapshots, except you manage them in the Amazon RDS console. These are backups that you can initiate at any time. They exist until you delete them. For example, to meet a compliance requirement that mandates you to keep database backups for a year, you need to use manual snapshots. If you restore data from a manual snapshot, it creates a new DB instance using the data from the snapshot.
![[Pasted image 20250926161833.png]]