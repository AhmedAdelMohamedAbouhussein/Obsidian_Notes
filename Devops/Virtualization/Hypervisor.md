A **hypervisor** is the technology that makes virtualization possible—it’s the software (or firmware) that lets you run **multiple operating systems on the same physical machine** at the same time.

Think of it as a **manager** that controls virtual machines.

---

### **Types of Hypervisors**

1. **Type 1 (Bare-metal)**
    
    - Runs **directly on the physical hardware**.
        
    - No host OS needed.
        
    - Examples: VMware ESXi, Microsoft Hyper-V, Xen.
        
    - Pros: High performance, used in data centers.
        
2. **Type 2 (Hosted)**
    
    - Runs **on top of a host operating system**.
        
    - Example: Oracle VirtualBox, VMware Workstation.
        
    - Pros: Easy to use on your personal computer, good for learning/testing.
        
    - Cons: Slightly slower than Type 1 because it goes through the host OS.
        

---

### **How It Works**

- The hypervisor **allocates resources** (CPU, RAM, disk) to each virtual machine.
    
- Each VM thinks it’s running on its **own physical machine**, even though it shares the real hardware with other VMs.
    

---

In short:

- **VirtualBox is a Type 2 hypervisor** because it runs on top of your existing OS.
    
- A hypervisor is basically the **software layer that creates and manages virtual computers**.