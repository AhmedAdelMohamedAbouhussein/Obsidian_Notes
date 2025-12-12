# **1. CPU Usage + CPU Temperature**

### **Linux**

![[Pasted image 20251128173933.png]]

**macOS**

![[Pasted image 20251128173948.png]]

**Windows (WSL or Git Bash)**

Windows **does not expose temps** via bash.  
You must call PowerShell:
![[Pasted image 20251128174041.png]]

# ✅ **2. GPU Usage + Temperature**

### **NVIDIA (Linux + Windows + WSL)**

![[Pasted image 20251128174125.png]]

**AMD (Linux only)**
![[Pasted image 20251128174136.png]]

**Intel iGPU (Linux)**

intel_gpu_top -J  # From intel-gpu-tools

