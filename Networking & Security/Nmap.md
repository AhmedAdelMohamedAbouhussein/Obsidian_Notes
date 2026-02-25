## 1️⃣ Definition

**Nmap** (Network Mapper) is an **open-source network scanning and security auditing tool**.

- Used to **discover hosts, services, and open ports** on a network
    
- Can detect **OS types, versions, and running services**
    
- Works on **Linux, Windows, macOS, and Unix systems**
    
- Essential tool in **network administration, penetration testing, and security auditing**
    

---

## 2️⃣ Key Features

|Feature|Description|
|---|---|
|Host discovery|Identify live hosts on a network|
|Port scanning|Detect open, closed, or filtered ports|
|Service version detection|Determine software and versions running on ports|
|OS fingerprinting|Identify operating system and hardware|
|Scriptable interaction|Nmap Scripting Engine (NSE) for vulnerability scanning, automation|
|Flexible scanning techniques|TCP SYN scan, UDP scan, ACK scan, etc.|
|Output formats|Plain text, XML, grepable, JSON|

---

## 3️⃣ Installation

### Linux

	sudo apt update  
	sudo apt install nmap  
	nmap --version

### Windows / macOS

- Download from [https://nmap.org/download.html](https://nmap.org/download.html)
    
- GUI version: **Zenmap**
    

---

## 4️⃣ Basic Usage

### Scan a single host

nmap 192.168.1.1

- Default scan: **TCP SYN scan on 1000 common ports**
    

### Scan multiple hosts

	nmap 192.168.1.1 192.168.1.5 192.168.1.10  
	nmap 192.168.1.0/24  # Scan entire subnet

### Scan specific ports

	nmap -p 22,80,443 192.168.1.1

---

## 5️⃣ Advanced Scanning

### Service Version Detection

nmap -sV 192.168.1.1

- `-sV` → detect version of services running on open ports
    

### OS Detection

nmap -O 192.168.1.1

- `-O` → OS fingerprinting
    

### Aggressive Scan

nmap -A 192.168.1.1

- `-A` → combines **OS detection, version detection, script scanning, and traceroute**
    

---

## 6️⃣ Nmap Scan Types

|Scan Type|Description|
|---|---|
|TCP SYN scan `-sS`|Most common, stealthy, sends SYN packets|
|TCP Connect `-sT`|Full TCP handshake, less stealthy|
|UDP scan `-sU`|Scan UDP ports, slower|
|ACK scan `-sA`|Map firewall rules|
|FIN / Xmas / Null|Evade IDS / firewall detection|

---

## 7️⃣ Nmap Scripting Engine (NSE)

- Powerful scripting system for **automation, vulnerability scanning, and info gathering**
    
- Scripts located in `/usr/share/nmap/scripts` (Linux)
    
- Run scripts:
    

nmap --script=vuln 192.168.1.1

- Examples:
    
    - `http-vuln-cve2017-5638` → checks for Apache Struts vulnerability
        
    - `ssl-heartbleed` → detect Heartbleed vulnerability
        
    - `ftp-anon` → check for anonymous FTP access
        

---

## 8️⃣ Output Options

|Option|Description|
|---|---|
|`-oN <file>`|Normal text output|
|`-oX <file>`|XML output|
|`-oG <file>`|Grepable output|
|`-oA <prefix>`|Save all formats with prefix|

---

## 9️⃣ Advantages

- **Versatile** → host discovery, port scanning, OS/service detection
    
- **Open source and cross-platform**
    
- **Scriptable** → automation and vulnerability detection
    
- **Powerful for security audits** and penetration testing
    

---

## 🔟 Limitations

- Scans may be **detected by IDS/IPS**
    
- Aggressive scans may **trigger alerts or block access**
    
- Requires **network knowledge** to interpret results accurately
    
- Large network scans can be **slow** without optimization
    

---

## 11️⃣ Common Use Cases

1. **Network inventory** → find hosts and services
    
2. **Security auditing** → identify vulnerabilities and open ports
    
3. **Penetration testing** → reconnaissance phase
    
4. **Firewall testing** → map filtered ports and rules
    
5. **Compliance verification** → check open ports vs security policy
    

---

## 12️⃣ Key Exam / Interview Points

- **Nmap = network scanning & security tool**
    
- Supports **host discovery, port scanning, OS detection, service version detection**
    
- **NSE scripts** allow vulnerability scanning and automation
    
- Scan types: **TCP SYN, TCP Connect, UDP, ACK, FIN/Xmas/Null**
    
- Output can be saved in **text, XML, grepable, JSON**
    
- Common flag: `nmap -A target` → aggressive scan with OS/service detection