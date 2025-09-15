**IaC (Infrastructure as Code)** = Managing and provisioning cloud resources using code instead of manual clicks in the console.

### 🔑 Key Points about IaC:

- **Automation**: Write code (YAML, JSON, HCL) to define infrastructure like servers, networks, databases.
    
- **Consistency**: Same code = same infrastructure everywhere (dev, staging, prod).
    
- **Version Control**: Store infra code in GitHub/GitLab, track changes, roll back if needed.
    
- **Scalability**: Deploy hundreds of resources in minutes.
    
- **Repeatability**: Reuse templates/modules across projects.
    
- **Collaboration**: Teams can review infra changes just like app code.
    

### ⚡ Common IaC Tools:

- **AWS CloudFormation** → AWS-native IaC (YAML/JSON).
    
- **Terraform** → Multi-cloud IaC (HCL).
    
- **Pulumi** → IaC with real programming languages (Python, TypeScript, Go, etc.).
    
- **Ansible** → Often used for configuration + provisioning.

👉 In short: IaC makes your **infrastructure behave like software** — codified, testable, and repeatable.