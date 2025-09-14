A load balancer takes in requests and routes them to instances. There are many off-the-shelf load balancers that work great on AWS
However, if you would like AWS to handle all of that, and you just configure it once, check out Elastic Load Balancing, or ELB. ELB is designed to distribute network traffic to improve application scalability. The word _elastic_ refers to its ability to scale up or down based on traffic, without adding to your hourly costs. ELB can manage both internal and external traffic to AWS. It offers different routing strategies to ensure efficient traffic management and thusly optimal application performance.

Elastic Load Balancing (ELB) automatically distributes incoming application traffic across multiple resources, such as EC2 instances, to optimize performance and reliability. A load balancer serves as the single point of contact for all incoming web traffic to an Auto Scaling group. As the number of EC2 instances fluctuates in response to traffic demands, incoming requests are first directed to the load balancer. From there, the traffic is distributed evenly across the available instances.

Although ELB and Amazon EC2 Auto Scaling are distinct services, they work in tandem to enhance application performance and ensure high availability. Together, they enable applications running on Amazon EC2 to scale effectively while maintaining consistent performance.

![[Pasted image 20250914182047.png]]

![[Pasted image 20250914182134.png]]

