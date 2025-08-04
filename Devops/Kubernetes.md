**Kubernetes** (often abbreviated as **K8s**) is an **open-source container orchestration platform** developed by Google and now maintained by the Cloud Native Computing Foundation (CNCF). It is used to **automate deployment, scaling, and management of containerized applications**.

### Why Kubernetes?
When you deploy applications in **containers** (like Docker), managing a few containers is easy. But when you have **hundreds or thousands**, doing it manually becomes impossible. Kubernetes helps manage this at scale.

### Key Features of Kubernetes:

1. **Container Orchestration**  
    It schedules and runs containers across a cluster of machines, making sure your app is always running.
2. **Scaling**  
    You can **automatically scale** your application up or down based on traffic (horizontal scaling).
3. **Load Balancing**  
    It distributes incoming traffic to ensure no container gets overwhelmed.
4. **Self-Healing**  
    If a container crashes, Kubernetes **automatically restarts or replaces** it.
5. **Service Discovery and DNS**  
    Kubernetes automatically assigns IPs and DNS names to services and handles communication.
6. **Rolling Updates and Rollbacks**  
    Deploy new versions of your app **without downtime**. You can also revert back if something goes wrong.
7. **Storage Orchestration**  
    Automatically mounts the storage system of your choice (local, AWS EBS, Google Cloud Persistent Disk, etc.) to containers.

![[Pasted image 20250803182124.png]]
![[Pasted image 20250803182146.png]]

