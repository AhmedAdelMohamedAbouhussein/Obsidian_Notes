## 1️⃣ Definition

**Tailscale** is a **VPN service built on WireGuard** that creates a **secure private network** between your devices.

- Simplifies network connectivity **without manually configuring firewalls, NAT, or port forwarding**
    
- Works on multiple platforms: **Windows, macOS, Linux, iOS, Android**
    
- Uses **peer-to-peer connections** with **automatic NAT traversal**
    

---

## 2️⃣ Core Concept

Tailscale builds a **mesh VPN**:

1. Each device runs a **Tailscale client**
    
2. Devices authenticate via **OAuth / SSO / Identity Provider**
    
3. Tailscale assigns a **private IP address** to each device (100.x.x.x)
    
4. Devices communicate securely over **WireGuard tunnels**
    
5. Uses **DERP relay servers** if direct peer-to-peer connection fails
    

Key points:

- **No central VPN server required**
    
- **Automatic key management**
    
- **End-to-end encryption**
    

---

## 3️⃣ How Tailscale Works

1. **Authentication**: Login via Google, Microsoft, or GitHub
    
2. **Device registration**: Client gets a **private IP** and public keys
    
3. **Key distribution**: Each device shares its public keys with others
    
4. **Mesh creation**: Devices form direct **WireGuard connections**
    
5. **DERP fallback**: If NAT prevents direct connection, traffic routes via **Tailscale relay server**
    

---

## 4️⃣ Features

|Feature|Description|
|---|---|
|Built on WireGuard|Fast, modern VPN encryption|
|Mesh Networking|Every device can reach every other device|
|NAT Traversal|Works behind firewalls and home routers|
|Identity-Based Access|Uses SSO for authentication|
|Split Tunnels|Route some traffic over Tailscale, some over regular network|
|ACLs / Access Control|Control which devices can communicate|
|Cross-Platform|Windows, macOS, Linux, Android, iOS|

---

## 5️⃣ Tailscale vs Traditional VPN

|Feature|Traditional VPN|Tailscale|
|---|---|---|
|Server|Required|Optional (mesh P2P)|
|NAT Traversal|Manual port forwarding|Automatic|
|Key Management|Manual|Automatic|
|Setup Complexity|High|Very Low|
|Scalability|Limited by server|Mesh, scales easily|
|Security|Centralized|End-to-end encrypted|

---

## 6️⃣ Typical Use Cases

1. **Remote Work** → Access home/office devices securely
    
2. **Cloud Management** → Connect servers in different regions
    
3. **IoT Devices** → Securely manage devices behind NAT/firewalls
    
4. **Private Networking** → Connect team devices without VPN servers
    

---

## 7️⃣ Quick Example (Linux / CLI)

![[{77219774-82A3-44EA-97E1-286E7FF274E7}.png]]

- After `tailscale up`, each device gets a **100.x.x.x IP**
    
- Devices communicate **directly (WireGuard)** or via **DERP relay**
    

---

## 8️⃣ Advantages

- **Easy setup** → no VPN servers
    
- **Secure** → WireGuard + automatic key rotation
    
- **Works behind NAT/firewalls** → seamless mesh network
    
- **Cross-platform & scalable** → laptops, phones, servers
    

---

## 9️⃣ Limitations

- Depends on **Tailscale coordination servers** for key exchange
    
- Free tier has **device limits**
    
- Mostly optimized for **team or personal private networks**, not large enterprise VPN infrastructure
    

---

## 🔟 Key Exam / Interview Points

- Tailscale = **WireGuard + mesh networking + identity management**
    
- Devices get **private 100.x.x.x IPs** → communicate securely
    
- Uses **DERP relay** if peer-to-peer connection fails
    
- Eliminates need for **manual VPN server setup**
    
- **Access control & SSO integration** make it enterprise-friendly