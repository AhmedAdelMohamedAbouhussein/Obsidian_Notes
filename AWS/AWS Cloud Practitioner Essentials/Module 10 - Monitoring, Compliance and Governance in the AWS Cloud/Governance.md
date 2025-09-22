Governance in the AWS Cloud

In this lesson, you will review the following three AWS services that can help govern and enforce services and accounts to meet your company's requirements:

- **AWS Control Tower**
    
- **AWS Service Catalog**
    
- **AWS License Manager**

![[Pasted image 20250921182933.png]]

> **AWS Control Tower**

AWS Control Tower is a service you can use to enforce and manage governance rules for security, operations, and compliance at scale across all your organizations and accounts in the AWS Cloud.

**Benefits:** AWS Control Tower can help you save time while providing governance. It uses preconfigured controls, which can help you to quickly set up multi-account environments, automation with built-in governance, and integration of third-party software at scale.

**Use cases:** Use AWS Control Tower to quickly deploy applications and provision compliant AWS accounts.

To learn more about AWS Control Tower features, choose each of the four numbered markers.
![[Pasted image 20250921183258.png]]

## Dashboard

The AWS Control Tower dashboard provides continuous oversight to see provisioned accounts across your enterprise. AWS Control Tower also has controls for policy enforcement and can help detect noncompliant resources.

## Account Factory

The AWS Control Tower Account Factory is a configurable account template that standardizes the provisioning of new accounts.

## Controls

Controls, sometimes called guardrails, are high-level rules that provide governance for your overall AWS environment.

## Landing zone

A landing zone is a well-architected multi-account environment that's based on security and compliance best practices. It's the enterprise-wide container that holds all of the organizational units (OUs), accounts, users, and resources you want to regulate for compliance.



Managing employee requests for new AWS services or resources can be time consuming, but you also don't want everyone guessing which type of services and settings should be used. That's where Service Catalog can help.

> **AWS Service Catalog**

With Service Catalog, you can create, share, and organize from a curated catalog of AWS resources. You can deploy baseline networking resources and security tools for new AWS accounts so you can govern consistently.

**Benefits:** Service Catalog saves time by making it quick to find and deploy approved, self-service cloud resources. It also helps you stay agile while improving governance over resources across multiple accounts.

**Use cases:** Use it to provision resources across AWS accounts, apply access controls, and accelerate provisioning of continuous integration and continuous delivery (CI/CD) pipelines.



When companies move from on premises to the cloud, they must decide how to handle their software licenses. With AWS Bring Your Own License model (BYOL), they can use existing software licenses purchased directly from vendors, such as Microsoft, on AWS services like Amazon EC2 Dedicated Hosts and Amazon WorkSpaces. This can result in significant cost savings compared to purchasing licenses directly from AWS. By using BYOL with existing licenses in a cloud environment, you get flexibility and potential optimized costs. The service that helps you manage and govern your software licenses is AWS License Manager.

> **AWS License Manager**

License Manager is a service that helps you manage your software licenses and fine-tune your licensing costs.

**Benefits:** License Manager helps with visibility and control, tracking and managing licenses, and reducing the risk of noncompliance with licenses.

**Use cases:** Use it to streamline license management and to simplify the Microsoft License Mobility through Software Assurance experience. You can also use it to automate the distribution and activation of software entitlements across AWS accounts for end users.

Managing software licenses can be time consuming, costly, and difficult to enforce. License Manager helps reduce the risk of noncompliance by enforcing license usage limits, blocking new launches, and using other controls.

![[Pasted image 20250921183735.png]]