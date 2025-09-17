## 🌐 AWS Networking & Connectivity – Key Resources

### 🏗 Core VPC Components

- **Amazon VPC** → Isolated virtual network in AWS for launching resources.
    
- **Subnet** → Sub-division of a VPC (public or private). Organizes resources.
    
- **Internet Gateway (IGW)** → Connects VPC to the internet (for public subnets).
    
- **Virtual Private Gateway (VGW)** → Secure entry point into a VPC from an approved private network (e.g., via VPN).
    

---

### 🔒 Secure Connectivity Options

- **AWS Client VPN** → Fully managed, elastic VPN for **remote workers** and on-premises users. Scales automatically.
    
- **AWS Site-to-Site VPN** → Encrypted tunnel between **data centers/branch offices** and AWS.
    
- **AWS PrivateLink** → Private access to AWS services or partner services **as if in your VPC**.
    
- **AWS Direct Connect** → Dedicated, private, high-bandwidth connection between on-premises and AWS.
    

---

### 🔐 Security Controls

- **Network ACLs (NACLs)** → Stateless traffic filter at **subnet level**.
    
- **Security Groups (SGs)** → Stateful traffic filter at **instance level**.
    

---

### 🌍 DNS & Traffic Management

- **DNS** → Translates human-friendly domain names to IP addresses.
    
- **Amazon Route 53** → Managed DNS + domain registration + health checks + traffic routing.
    
- **Amazon CloudFront** → CDN service delivering content via edge locations for low latency.
    
- **AWS Global Accelerator** → Improves app performance & availability for **global users** by routing via AWS global network.
    

---

### 🔗 Advanced Networking

- **Amazon Transit Gateway (TGW)** → Hub for interconnecting multiple VPCs and on-premises networks.
    
- **NAT Gateway** → Allows **private subnet instances** to access internet services (outbound only).
    
- **Amazon API Gateway** → Service for building, publishing, and securing APIs at scale.
    

---

✅ **Quick Exam Hints**

- _Client VPN_ → Remote **users**.
    
- _Site-to-Site VPN_ → Remote **offices**.
    
- _PrivateLink_ → Private **service-to-service** access.
    
- _Direct Connect_ → **Dedicated line**, high bandwidth.
    
- _NACLs_ → Subnet level, stateless.
    
- _SGs_ → Instance level, stateful.