
Detection and response services

Preventing and protecting against security threats are two methods for securing your AWS resources. You should also be prepared to detect and respond to security incidents that might occur. AWS offers a variety of services you can use to detect and respond to security incidents.


> **Amazon Inspector**

Amazon Inspector helps improve the security and compliance of applications by running automated security assessments for Amazon EC2 instances, containers, and Lambda functions. It checks applications for security vulnerabilities and deviations from security best practices, such as open access to EC2 instances and installations of vulnerable software versions.

You can view completed assessments in the Amazon Inspector console. These assessments include a list of security findings prioritized by severity level. Each identified security issue includes a detailed description and a recommendation for how to fix it. You can also retrieve these findings through an API.


> **Amazon GuardDuty**

Amazon GuardDuty provides intelligent threat detection across your infrastructure and resources. GuardDuty identifies threats by continuously monitoring streams of your account metadata and network activity in your environment. It uses known malicious IP addresses, anomaly detection, and machine learning to identify threats more accurately.

You can review detailed findings about any GuardDuty detected threats in the AWS Management Console. Findings include recommended steps for remediation. You can also configure AWS Lambda functions to perform remediation steps automatically.

![[Pasted image 20250920232350.png]]


> **Amazon Detective**

After a threat has been detected, you can use Amazon Detective to further investigate the root cause. Detective helps you analyze threats with interactive visualizations contained in a unified AWS Management Console view. These visualizations include resource and user interactions over a configurable timeline with recommended steps for remediation.

![[Pasted image 20250920234607.png]]

> **AWS Security Hub**

Security Hub brings multiple security services together into a single place and format. With this service, you can quickly see your security and compliance state in one comprehensive view. Security Hub automatically aggregates security findings from AWS and partner services and organizes them into actionable, meaningful groupings called insights. It can accelerate time to resolution (TTR) with automated remediation.

![[Pasted image 20250920234639.png]]

