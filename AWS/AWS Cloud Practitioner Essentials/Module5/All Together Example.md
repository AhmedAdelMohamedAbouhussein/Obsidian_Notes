
![[Pasted image 20250917132553.png]]

 let's take a look at how that works. Starting with a user, they access the company's website using a custom domain, the request is then sent to a Route 53 DNS record. Route 53 uses a routing policy to determine which Region is closest to the user and then directs them to the appropriate CloudFront edge location.  The edge location then fetches the content from the designated origin server in the chosen Region. Notice how we're showing an architecture with multiple AWS Regions, and multiple VPCs!