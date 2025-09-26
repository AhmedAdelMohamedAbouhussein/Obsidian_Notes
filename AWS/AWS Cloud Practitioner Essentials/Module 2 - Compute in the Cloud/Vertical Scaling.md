**Increase the instance size.** If too many requests are sent to a single active-passive system, the active server will become unavailable and, hopefully, fail over to the passive server. But this doesn’t solve anything.  
  
With active-passive systems, you need vertical scaling. This means increasing the size of the server. With EC2 instances, you select either a larger type or a different instance type. This can be done only while the instance is in a stopped state. In this scenario, the following steps occur:

1. **Stop the passive instance.** This doesn’t impact the application because it’s not taking any traffic.
2. **Change the instance size or type,** and then start the instance again.
3. **Shift the traffic** to the passive instance, turning it active.
4. **Stop, change the size, and start** the previous active instance because both instances should match.

When the number of requests reduces, you must do the same operation. Even though there aren’t that many steps involved, it’s actually a lot of manual work. Another disadvantage is that a server can only scale vertically up to a certain limit. When that limit is reached, the only option is to create another active-passive system and split the requests and functionalities across them. This can require massive application rewriting.  
  
This is where the active-active system can help. When there are too many requests, you can scale this system horizontally by adding more servers.

![[Pasted image 20250926162515.png]]