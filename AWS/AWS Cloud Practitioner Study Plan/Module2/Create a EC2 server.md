### **Steps to Create an EC2 Instance**

- **Go to EC2 Console**
    
    - Access via “Recently visited,” shortcuts, or search.
    - Select **Launch Instance**.
        
- **Choose Instance Name**
    
    - Helps you identify it later.
        
- **Select AMI (Amazon Machine Image)**
    
    - Template with OS + pre-installed apps.
    - Choose **Amazon Linux AMI** (general-purpose, free-tier friendly).
        
- **Choose Instance Type**
    
    - Defines compute resources.
    - Select **t2.micro** (1 vCPU, 1 GB memory, Free Tier eligible).
        
- **Choose Key Pair**
    
    - Used for SSH login.
    - **Public key** injected into instance.
    - **Private key** kept by you.
    - Either create new or use existing.
        
- **Configure Network Settings**
    
    - Allow **HTTP traffic from the internet**.
    - Required for a web server.
        
- **Set Storage Options**
    
    - **8 GB gp3 EBS volume** (Elastic Block Store).

- **Add User Data (Advanced Details)**
    
    - Paste startup script in **User Data**.
    - Installs and enables **Nginx web server** automatically.
        
- **Launch Instance**
    
    - Review configurations.
    - Click **Launch Instance**.
        
- **Access Instance**
    
    - Copy **public IP address**.
    - Open in browser → see running web server.