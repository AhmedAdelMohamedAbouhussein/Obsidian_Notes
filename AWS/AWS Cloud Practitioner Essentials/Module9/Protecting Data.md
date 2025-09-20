Encryption is a key component of data protection. Let's review how data encryption works.

### Encryption basics

Data encryption works like a lock and key mechanism. If you have the right key, you can access the encrypted data. Otherwise, you cannot access the data. For example, let's say you are protecting a customer's profile. An encryption key is used to turn the profile information into a randomized set of characters. A decryption key is used to access the customer's information, such as their name, only when it's needed by your application.
![[Pasted image 20250920231719.png]]


### Types of data encryption

Data encryption comes in the following two forms: 

- **Data encryption at rest**: The data is idle and not moving, like when it's stored in a database.
    
- **Data encryption in transit:** The data is moving between locations, like when it's being sent from a database to an application. SSL/TLS certificates are used to establish encrypted network connections from one system to another.

![[Pasted image 20250920231738.png]]


AWS data protection

AWS has a variety of methods for protecting data. They include built-in data protection for storage options and services specifically designed for enhanced data protection.

Let's review some of the data protection methods.

![[Pasted image 20250920231823.png]]


AWS data protection services

> **AWS Key Management Service (AWS KMS)**

You can use AWS KMS to create and manage cryptographic keys. These keys can then be used to encrypt and decrypt your data. You can also control the use of keys across a wide range of services and in your applications. For example, you can specify which IAM users and roles can manage keys. Your keys never leave AWS KMS, and you can temporarily disable them so they can no longer be used.

> _A_ **_cryptographic key_** _is a random string of digits used for locking (encrypting) and unlocking (decrypting) data._

> **Amazon Macie**

With Amazon Macie, you can monitor your sensitive data at rest to make sure it's safe. Macie uses machine learning (ML) and automation to discover sensitive data stored in Amazon S3. You can use Macie to assess your security posture, which is especially helpful for meeting compliance requirements.

> **AWS Certificate Manager (ACM)**

ACM centralizes the management of your SSL/TLS certificates that provide data encryption in transit. It can be used to protect various AWS services and your connected on-premises resources.

> **_SSL/TLS certificates_** _are used to establish encrypted network connections from one system to another._
