Scalability is about a system’s potential to grow over time, whereas elasticity is about the dynamic, on-demand adjustment of resources.

![[Pasted image 20250914170517.png]]

![[Pasted image 20250914170525.png]]

Amazon EC2 Auto Scaling automatically adjusts the number of EC2 instances based on changes in application demand, providing better availability. It offers two approaches. _Dynamic scaling_ adjusts in real time to fluctuations in demand. _Predictive scaling_ preemptively schedules the right number of instances based on anticipated demand.

The way this works technically involves some other AWS services to make it all happen. You need to be collecting data about the performance of the instances, or potentially data around latency and other application metrics. You would use the **Amazon CloudWatch** service to collect and monitor these metrics. This data is then used to determine when scaling needs to happen. And, it happens automatically, right when you need it.

With EC2 Auto Scaling, you maintain the desired amount of compute capacity for your application by dynamically adjusting the number of EC2 instances based on demand. You can create Auto Scaling groups, which are collections of EC2 instances that can scale in or out to meet your application’s needs.
An Auto Scaling group is configured with the following three key settings.

![[Pasted image 20250914180616.png]]
![[Pasted image 20250914180657.png]]
![[Pasted image 20250914180808.png]]
