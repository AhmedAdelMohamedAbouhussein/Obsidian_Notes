
Network and application attacks

Network and application protection is another vital component of a secure environment on AWS. In the previous video, you learned about denial of service attacks that might be used against your enterprise.

Let's review how these denial of service attacks work.

### DoS attacks

In a denial of service attack, an attacker floods a web application with excessive network traffic. Legitimate customer requests are denied if the web application becomes overloaded and can no longer respond.

### DDoS attacks

In a distributed denial of service (DDoS) attack, an attacker can use multiple infected computers (called _zombie bots_) to unknowingly send excessive traffic to a web application.

### UDP flood

A UDP flood is a type of DDoS attack where attackers send massive amounts of UDP packets to random or specific ports. This overloads the target’s network and CPU resources, making it unable to respond to legitimate requests.
![[Pasted image 20250920230319.png]]


AWS protection through services

AWS also offers the following services to help protect your network and applications.


> **AWS Shield**

_AWS Shield Standard_ is designed to automatically protect AWS customers from the most common, frequently occurring types of DDoS attacks at no cost. It uses a variety of analysis techniques to detect and mitigate incoming malicious network traffic in real time.

_AWS Shield Advanced_ is a paid service that provides detailed attack diagnostics and the ability to detect and mitigate sophisticated DDoS attacks. It also integrates with other services, such as Amazon CloudFront, Amazon Route 53, and ELB.

Additionally, you can integrate AWS Shield with AWS WAF by writing custom rules to mitigate complex DDoS attacks.


> **AWS WAF**

AWS WAF is a web application firewall that monitors network requests that come into your web applications. When a request comes into AWS WAF, it checks the IP address against a web access control list (web ACL). If the request comes from a blocked IP address on the web ACL, AWS WAF denies access. Legitimate requests are allowed access.