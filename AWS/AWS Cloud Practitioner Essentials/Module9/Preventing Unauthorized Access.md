AWS Identity and Access Management (IAM) 

**Securely manage identities and access to AWS services and resources.**

One of the best ways to prevent security incidents before they happen is through proper permission and access management. With IAM, by default, all actions are denied. You must explicitly grant permission to someone before they can perform any actions in your account.

When you grant permissions, you should provide access only on a need-to-have basis. This concept is called the principle of least privilege.

## AWS account root user

All AWS accounts are given an AWS account root user. The root user is the account owner and has permission to do anything inside the AWS account. You should associate a strong password with this powerful account and turn on multi-factor authentication (MFA), which requires at least two verification methods to log in. To handle daily tasks, you should create other IAM identities, such as IAM users.
![[Pasted image 20250920223032.png]]

> _The_ **_principle of least privilege_** _dictates that you should only give people and systems access to what they need and nothing else._
![[Pasted image 20250920223230.png]]

IAM provides users, groups, and roles so you can configure access based on your company’s specific operational and security needs. IAM policies define the needed access for these identities.

## IAM users

An IAM user represents a person or application that interacts with AWS services and resources. It consists of a name and credentials. AWS recommends creating individual IAM users for each person who needs to access the AWS account, so they have their own unique set of security credentials.

## IAM groups

An IAM group is a collection of IAM users. When you assign permissions to a group, all users in the group inherit the permissions. For example, you might assign standard access permissions to a group called **employees** so all your employees receive the same generic access.

## IAM roles

An IAM role is an identity you can assume to gain temporary access to permissions. For example, an employee might need to work as a barista in the morning and a cashier in the afternoon. When someone assumes an IAM role, they abandon all previous permissions they had under a previous role and assume the permissions of the new role.
![[Pasted image 20250920223512.png]]
## IAM policies

An IAM policy is a JSON document that allows or denies permission to access AWS services and resources. IAM policies can also define the level of access to resources. For example, you can allow employees to access all the Amazon S3 buckets in your AWS account or only a specific bucket.

IAM Policy example:
![[Pasted image 20250920223347.png]]

  
> **AWS IAM Identity Center**

IAM Identity Center centralizes identity and access management across AWS accounts and applications. IAM Identity Center can also connect to an existing identity source and provide your workforce with single sign-on access to all your connected AWS services and accounts. This is called federated identity management.

> **_Federated identity management_** _is a system that allows users to access multiple applications, services, or domains using a single set of credentials._


> **AWS Secrets Manager**

Secrets Manager provides a secure way to manage, rotate, and retrieve database credentials, API keys, and other secrets throughout their lifecycle. This helps keep your applications, services, and IT resources safe.

> **_Secrets_** _are confidential or private information intended to be known only to specific individuals or groups. Examples include passwords, database credentials, and API keys._


> **AWS Systems Manager**

Systems Manager provides a centralized view of nodes across your organization’s accounts and Regions and multi-cloud and hybrid environments. With this service, you can quickly access node information, such as ID and operating system details, and automate registry edits, user management, and security patching.

> **_Nodes_** _are connection points in a network, system, or structure_**_._**