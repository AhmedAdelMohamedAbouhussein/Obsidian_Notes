Built a multi-Region CI/CD pipeline using AWS DevOps tools. Provisioned EC2 environments with CloudFormation, using parameters, tags, and UserData for automation. Managed source code in CodeCommit and developed via Cloud9. Configured CodeDeploy for application rollout across regions. Orchestrated pipeline stages with CodePipeline, adding CloudWatch triggers, approval gates, and a Lambda readiness check to ensure secure, automated deployments.

### **1. Environment Provisioning (Outside the Pipeline)**

- **AWS CloudFormation** used to define infrastructure as code.
    
- Provisioned **EC2 instances** and **security groups** in **Region 1 (US West, Oregon)** and **Region 2 (US East, N. Virginia)**.
    
- Used **Parameters, Tags (Name=My-Demo-Web-App)**, and **UserData** to configure instances and install **CodeDeploy agent**.
    

---

### **2. Source Control & Development**

- **AWS CodeCommit** → Git-based repository where developers push code.
    
- **AWS Cloud9** → Cloud IDE for editing, uploading files, and running Git commands (`clone`, `add`, `commit`, `push`).
    
- Application: EC2 user-data script creates a static web page showing instance metadata.
    

---

### **3. Continuous Deployment Setup**

- **AWS CodeDeploy**: Defines deployment application and groups (`CodeDeploy-Web-App-Group-Region1`, `CodeDeploy-Web-App-Group-Region2`).
    
- Target EC2 instances identified by **Tags**.
    
- Configured without load balancer for simplicity.
    

---

### **4. CI/CD Pipeline Orchestration**

- **AWS CodePipeline** automates flow:
    
    - **Source Stage** → CodeCommit (triggered by CloudWatch Events on code push).
        
    - **Deploy Stage** → CodeDeploy to Region 1.
        
- Enhanced pipeline with:
    
    - **Manual Approval Gate** before deploying to Region 2.
        
    - Later replaced with an **automated Lambda function check** (`Region-approval-test`) to validate readiness.
        

---

### **5. Monitoring & Control**

- Deployment logs/status tracked in CodePipeline and CodeDeploy.
    
- Application validated by refreshing deployed web page across regions.
    

---

✅ **Core AWS Services Covered**:

- AWS CloudFormation (IaC), EC2, Security Groups, IAM, Cloud9, CodeCommit, CodeDeploy, CodePipeline, CloudWatch Events, Lambda.