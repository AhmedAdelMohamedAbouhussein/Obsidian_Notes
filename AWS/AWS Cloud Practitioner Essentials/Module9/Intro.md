### Authentication and authorization

_Authentication_ is the process of verifying the identity of a user or entity through credentials like a username and password combination.

- **Use case:** An employee logs in to an employee portal.

_Authorization_ grants users certain access rights and permissions that determine which actions they can perform in a system or application.

- **Use case:** An employee can only access their own employee records inside the employee portal.

![[Pasted image 20250920222435.png]]


![[Pasted image 20250920222213.png]]

![[Pasted image 20250920222230.png]]

![[Pasted image 20250920222302.png]]

![[Pasted image 20250920222733.png]]

### AWS shared responsibility model

Cloud security is a shared responsibility between customers and AWS. Let's examine this relationship using the AWS shared responsibility model.

**Customers: Security _in_ the cloud**  
When using AWS services, customers maintain complete control over their content. As a result, customers are responsible for securing everything they create and manage in the AWS Cloud. This includes the following:

- Managing the security of data, systems, and applications
    
- Deciding what data and workloads to store or run in AWS
    
- Determining which AWS services to use
    
- Controlling who has access to environments and resources
    

**AWS: Security _of_ the cloud**  
AWS is responsible for security _of_ the cloud. AWS operates, manages, and controls the components at all layers of the infrastructure. This includes securing the following:

- The foundational software that powers AWS services
    
- The virtualization layer
    
- The hardware and global infrastructure that supports the data centers from which services operate. This includes protection for AWS Regions, Availability Zones, and edge locations.