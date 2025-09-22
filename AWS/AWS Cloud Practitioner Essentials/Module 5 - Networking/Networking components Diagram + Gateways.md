![[Pasted image 20250915185222.png]]

The **AWS Cloud** is the outermost box in most diagrams.

**Region** is the next box. AWS Regions are separate geographic areas. You choose your Region based on your users' geographic location for lower latency, compliance and data residency requirements, available services, and cost.

**Amazon VPC** is a solid box, and it represents your isolated, logically segmented network within AWS. A VPC helps you to control your network resources and security.

**Availability Zones** are shown as separate boxes across a region. AZs consist of one or more discrete data centers, each with redundant power, networking, and connectivity, and housed in separate facilities. Using multiple AZs can protect your applications from the failure of a single location in the Region.

**Subnets** are essentially segments of your VPC, allowing you to divide your VPC into smaller, manageable sections. A subnet is a range of IP addresses in your VPC.

**Private subnets** are designed to isolate resources that shouldn't be directly exposed to the public internet. In diagrams, they are illustrated with solid boxes.

**Public subnets** are designed to provide direct internet access to resources placed inside them. To allow access, they are connected with an internet gateway.. In diagrams, public subnets are drawn with dashed boxes.


![[Pasted image 20250915185909.png]]

to allow traffic from the public internet to flow into and out of your VPC, you must attach what is called an internet gateway to your VPC. An internet gateway is like a doorway that is open to the public. Without it, no one can reach the resources placed inside of your VPC.

![[Pasted image 20250915190330.png]]
VPN creates a connection that is more like a secure tunnel through the internet. Using encryption, it hides and protects everything you send and receive from outside eyes. A virtual private gateway is the component in the AWS Cloud that makes it possible for you to connect this protected traffic to enter the VPC. With a VPN connection, your data travels privately and safely, hidden from others using the same route.

With a virtual private gateway, you can establish a VPN connection between your VPC and a private network, such as an on-premises data center or internal corporate network. A virtual private gateway allows traffic into the VPC only if it is coming from an approved network.


**Virtual private network**

A VPN encrypts your internet traffic, helping protect it from anyone who might try to intercept or monitor it.


A virtual private gateway is the virtual private network (VPN) endpoint on the AWS side. It provides a way for you to establish a secure, encrypted connection between your on-premises network and your virtual private cloud (VPC).