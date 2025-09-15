
Define cloud computing in AWS.
	on demand delivery of IT resources over the internet with pay as you go pricing


Describe and differentiate between cloud deployment types.
	You can deploy cloud resources in multiple ways: cloud, on-premises, and hybrid. Each type offers unique benefits and considerations, and exploring these options can help you make informed decisions about your cloud strategy.
	
1. <span style="font-size:16px; color:green;">Cloud</span>:
	In a cloud-based deployment model, you have the flexibility to migrate your existing resources to the cloud, design and build new applications within the cloud environment, or use a combination of both.
	
	for instance, a company might migrate data resources to the cloud, then develop an application comprised of virtual servers, databases, and networking components entirely hosted in the cloud.
	
2. <span style="font-size:16px; color:green;">On Premise</span>:
	Deploying resources on premises using virtualization and resource management tools does not provide many of the benefits of cloud computing. However, it is sometimes sought for its ability to provide dedicated resources and low latency.
	
	In most cases this deployment model is the same as legacy IT infrastructure while using application management and virtualization technologies to try increasing resource utilization.
	
3. <span style="font-size:16px; color:green;">Hybrid</span>:
	In a hybrid deployment, cloud-based resources and on-premises infrastructure work together. This approach is ideal for situations where legacy applications must remain on premises due to maintenance preferences or regulatory requirements.
	
	For instance, a company might choose to retain certain regulated legacy applications on-premises while using cloud services for advanced data processing and analytics.
	
	Multi-cloud deployments can also be considered _hybrid deployments_.


## **1. AWS Cloud**

💡 _Everything is hosted on Amazon Web Services (AWS), and you consume resources over the internet as needed._

### ✅ Pros

- **Scalability:** Instantly scale up/down resources.
- **Lower upfront cost:** No need to buy servers or networking gear.
- **Managed services:** AWS handles updates, security patches, backups.
- **Global availability:** Deploy apps in multiple regions worldwide.
- **Pay-as-you-go:** Only pay for what you use.

### ❌ Cons

- **Recurring cost:** Can become expensive over time if not optimized.
- **Vendor lock-in:** Hard to migrate once heavily invested.
- **Internet dependency:** Service availability relies on internet connectivity.

---

## **2. On-Premise (Traditional IT)**

💡 _You own and manage physical servers, storage, and networking in your data center._

### ✅ Pros

- **Full control:** You own the infrastructure, security, and compliance.
- **Customization:** Tailor hardware/software to specific business needs.
- **No internet dependency:** Local workloads continue running even if internet goes down.
- **Data sovereignty:** Keep sensitive data on-site (important in some industries).

### ❌ Cons

- **High upfront cost:** Expensive to buy servers, cooling, power, licenses.
- **Maintenance burden:** You manage updates, hardware failures, and scaling.
- **Scalability limits:** Scaling requires buying more hardware (slow and costly).
- **Disaster recovery:** Complex and expensive unless carefully planned.
    

---

## **3. Hybrid Cloud**

💡 _Mix of on-premise infrastructure and cloud (e.g., AWS Outposts, VPN/Direct Connect)._

### ✅ Pros

- **Flexibility:** Run sensitive workloads on-prem while using AWS for scalability.
- **Cost optimization:** Move workloads dynamically based on demand.
- **Business continuity:** Cloud as backup for disaster recovery.
- **Regulatory compliance:** Store regulated data on-prem, other workloads in cloud.

### ❌ Cons

- **Complexity:** Requires expertise to manage and integrate both environments.
- **Higher costs:** Maintaining both on-prem and cloud can be expensive.
- **Security challenges:** Need consistent security across both environments.

---

## **When to Use Each**

- **AWS Cloud:** Startups, fast-growing apps, global services, unpredictable workloads.
- **On-Premise:** Industries with strict data regulations (banks, healthcare, defense).
- **Hybrid Cloud:** Enterprises modernizing legacy systems, gradual migration, or balancing sensitive + scalable workloads.