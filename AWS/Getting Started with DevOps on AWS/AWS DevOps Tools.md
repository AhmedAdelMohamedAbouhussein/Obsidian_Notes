To successfully practice DevOps, you need effective tools that support your team and your workflows and help you deliver value faster. AWS supports DevOps with a number of services that developers use at every stage of the application lifecycle. As you learn more about the AWS services, remember that your DevOps solution might comprise AWS services and third-party solutions.

![[Pasted image 20250926172400.png]]

### **1. Developer Tools**

- **AWS Cloud9**: A cloud-based IDE for writing, running, and debugging code in a browser.
    
- **AWS Cloud Development Kit (CDK)**: An open-source framework for defining cloud infrastructure using programming languages.
    
- **Amazon Tools and SDKs**: Provide APIs and CLI support for interacting with AWS services.
    

---

### **2. AWS CodeCommit**

A fully managed source control service that hosts secure Git repositories. Developers **check in code** here, acting as the starting point for the pipeline.

---

### **3. AWS CodeBuild**

A fully managed build service that compiles source code, runs unit tests, and produces artifacts ready for deployment.

---

### **4. AWS CodeDeploy**

Automates the deployment of code to various compute services like Amazon EC2, AWS Lambda, or on-premises servers. Ensures smooth rollouts with features like blue/green deployments.

---

### **5. AWS X-Ray**

Helps developers analyze and debug production applications by tracing requests through distributed services. Identifies bottlenecks and performance issues.

---

### **6. Amazon CloudWatch**

Monitors applications and infrastructure in real time, collecting metrics, logs, and events. Enables alarms, dashboards, and automated responses.

---

### **7. AWS CodePipeline**

The orchestration service that automates the build, test, and deploy phases. It integrates CodeCommit, CodeBuild, CodeDeploy, and third-party tools to create a continuous delivery workflow.