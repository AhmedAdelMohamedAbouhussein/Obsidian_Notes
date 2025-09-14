AWS Global Infrastructure consists of physical locations around the world that contain groups of data centers. 

1. AWS Regions are physical locations around the world that contain groups of data centers. These groups of data centers are called Availability Zones. Each AWS Region consists of a minimum of three physically separate Availability Zones within a geographic area.
2. An Availability Zone consists of one or more data centers with redundant power, networking, and connectivity. Regions and Availability Zones are designed to provide low-latency, fault-tolerant access to services for users within a given area.

![[Pasted image 20250912203543.png]]

## Achieving high availability with AWS Global Infrastructure

AWS infrastructure is designed with high availability and fault tolerance in mind. Availability Zones (AZs) are configured as isolated resources, and they are each equipped with independent power, networking, and connectivity.

It's recommended to distribute your resources across multiple AZs. That way, if one AZ encounters an outage, your business applications will continue to operate without interruption. With this approach of redundancy and resource isolation, AWS customers can achieve the benefits of high availability and fault tolerance.