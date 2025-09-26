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


ELB with Amazon EC2 Auto Scaling

Additionally, the ELB service integrates seamlessly with Amazon EC2 Auto Scaling. As soon as a new EC2 instance is added to or removed from the Amazon EC2 Auto Scaling group, ELB is notified. However, before ELB can send traffic to a new EC2 instance, it needs to validate that the application running on the EC2 instance is available.  
  
This validation is done by way of the ELB health checks feature you learned about in the previous lesson. 


Configure Amazon EC2 Auto Scaling components

There are three main components of Amazon EC2 Auto Scaling. Each of these components addresses one main question as follows:

- •
    
    **Launch template or configuration:** Which resources should be automatically scaled?
    
- •
    
    **Amazon EC2 Auto Scaling groups:** Where should the resources be deployed?
    
- •
    
    **Scaling policies:** When should the resources be added or removed?
    

### 

Launch templates and configurations

Multiple parameters are required to create EC2 instances—Amazon Machine Image (AMI) ID, instance type, security group, additional Amazon EBS volumes, and more. All this information is also required by Amazon EC2 Auto Scaling to create the EC2 instance on your behalf when there is a need to scale. This information is stored in a launch template.  
  
You can use a launch template to manually launch an EC2 instance or for use with Amazon EC2 Auto Scaling. It also supports versioning, which can be used for quickly rolling back if there's an issue or a need to specify a default version of the template. This way, while iterating on a new version, other users can continue launching EC2 instances using the default version until you make the necessary changes.