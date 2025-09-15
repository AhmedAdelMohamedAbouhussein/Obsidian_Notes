### Containers and VMs

A container packages your application with everything it needs to run, so it works the same on any computer. This helps to move, update, and manage. Containers are faster and lighter than virtual machines (VMs) because they share the host computer’s operating system. VMs use a hypervisor to run full, separate operating systems, which makes them less resource-efficient and have longer startup times.

![[Pasted image 20250915162250.png]]
![[Pasted image 20250915162318.png]]


Container orchestration services manage the lifecycle of containers, including starting, stopping, and running them across a cluster. These orchestration services automatically scale containers out when traffic increases—and scale back in when things calm down. This way, your application can handle spikes in demand without breaking a sweat. They also handle recovery from failure, monitoring, and updates, saving you tons of time and effort.

![[Pasted image 20250915162336.png]]

On AWS, we have two main container orchestration options: Amazon ECS and Amazon EKS.

Amazon ECS stands for Amazon Elastic Container Service. It’s ideal if you want something streamlined and integrated, but you can still define your application’s container images and resources, such as EC2 instance types and load balancers. ECS automatically manages the containers and their infrastructure based on the parameters you set.

![[Pasted image 20250915161734.png]]

On the other hand, you have Amazon EKS, or Amazon Elastic Kubernetes Service. Kubernetes is an open source platform that automates containerized application deployment, scaling, and management. EKS makes it convenient to run Kubernetes clusters on AWS. It offers a lot of control and flexibility, especially for large-scale or hybrid deployments.


![[Pasted image 20250915161853.png]]

Now, orchestration services need somewhere to get their containers from. That’s where Amazon Elastic Container Registry, or Amazon ECR, comes in. ECR is a fully managed container registry that stores your container images. You build your containers that have your application and all of its dependencies bundled together. From there, a container orchestration tool can pull the container image and deploy it.
Amazon Elastic Container Registry (Amazon ECR) is where you can store, manage, and deploy container images. It supports container images that follow the Open Container Initiative (OCI) standards. You can push, pull, and manage images in your Amazon ECR repositories using standard container tooling and command line interfaces (CLIs).

![[Pasted image 20250915162019.png]]

So, you’ve got your container image, and you've chosen an orchestration service. Now, let’s focus on where your containers will actually run. AWS offers two main options for this: Amazon EC2 and AWS Fargate.

With EC2, you manage the virtual machines that run your containers. With this option, you have full control, but you need to manage the underlying infrastructure.

On the other hand, Fargate is serverless and offers efficiency and convenience. With Fargate, AWS manages the servers, and you only need to worry about your containers. No need to manage a fleet for these containers to run on.

![[Pasted image 20250915162157.png]]

![[Pasted image 20250915162600.png]]

