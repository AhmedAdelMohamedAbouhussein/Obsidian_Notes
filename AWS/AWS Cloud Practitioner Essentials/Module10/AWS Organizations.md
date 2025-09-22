As companies grow and scale, the management and governance of disparate AWS accounts can be a challenge. That's where AWS Organizations can help.

> **AWS Organizations**

Organizations helps you centrally manage and govern your environment as you grow and scale your AWS resources. It helps you manage policies for groups of accounts and automate account creation.

**Benefits:** Organizations provides several benefits like quickly scaling your environment by programmatically creating new AWS accounts for resources and teams. It also helps by simplifying permission management through SCPs and managing and optimizing costs across your AWS accounts and resources.

**Use cases:** It can be used for automating AWS account creation, providing tools and access for your security teams, controlling user access to designated services, and sharing common resources across accounts.

![[Pasted image 20250921182524.png]]

**Key concepts of Organizations**

An organization is a collection of AWS accounts that you can manage centrally and organize into a hierarchical, tree-like structure with a root at the top and organizational units (OUs) nested under the root. Each account can be located directly in the root or placed in one of the OUs in the hierarchy.

To learn more about how AWS Organizations works, choose each of the following four numbered markers.

![[Pasted image 20250921182043.png]]

## AWS Organizations

AWS Organizations is used to consolidate and manage multiple AWS accounts within a central location. When you create an organization, it automatically creates a root, which is the parent container for all the accounts in your organization.

## Management account

The management account is the central AWS account that creates and manages the organization. It's responsible for overall control and governance.

## Organizational unit (OU)

An organizational unit (OU) is a logical grouping of accounts in an AWS Organization. OUs can contain member accounts or nested OUs.

## Service control policies (SCP)

An SCP is a policy that lets you place restrictions on the AWS services, resources, and individual API actions that users and roles in each account can access. SCPs can be applied to either OUs or individual member accounts.

In AWS Organizations, you can apply SCPs to the organization root, an individual member account, or an OU. An SCP affects all IAM users, groups, and roles within an account, including the AWS account root user.

You can apply IAM policies to IAM users, groups, or roles. You cannot apply an IAM policy to the AWS account root user.

## Member account not in an OU

If you have a member account that has unique requirements that do not overlap with those of an organizational unit, you can add them to the organization. They do not have to be placed under an OU. This account can still take advantage of benefits such as consolidated billing.