# 💽 SATA (Serial ATA)

## 📖 Definition
**SATA (Serial Advanced Technology Attachment)** is a standard interface used to connect **storage devices** (like HDDs, SSDs, and optical drives) to the **motherboard** of a computer.

It replaced the older **PATA (Parallel ATA)** interface, offering faster data transfer speeds and simpler cabling.

---

## ⚙️ Key Features
- **Serial communication** → Transfers data one bit at a time (simpler and faster than parallel).
- **Hot-swappable** → Drives can be connected or disconnected while the system is powered on (if supported by the OS).
- **Slim connectors and cables** → Improves airflow and reduces clutter inside the case.

---

## 🔢 SATA Versions

| Version | Max Speed | Approx. Data Rate | Common Use |
|----------|------------|------------------|-------------|
| **SATA I (1.5 Gbps)** | ~150 MB/s | Old HDDs |
| **SATA II (3.0 Gbps)** | ~300 MB/s | Standard HDDs |
| **SATA III (6.0 Gbps)** | ~600 MB/s | SSDs and modern drives |

Most modern systems use **SATA III**.

---

## 🔌 SATA Connectors

| Connector | Description |
|------------|--------------|
| **SATA Data Cable** | Thin 7-pin cable that transfers data between the drive and motherboard. |
| **SATA Power Cable** | 15-pin cable from the power supply that provides power to the drive. |

🧠 Both cables are required for SATA drives to function.

---

## ⚙️ SATA Modes in BIOS

| Mode | Description | Recommended |
|------|--------------|-------------|
| **AHCI (Advanced Host Controller Interface)** | Modern standard; supports TRIM and NCQ for SSDs. | ✅ Use this |
| **IDE (Legacy)** | Compatibility mode for old systems. | ❌ Outdated |
| **RAID** | Combines multiple drives into one array. | ⚙️ Advanced use only |

---

## 💡 Notes
- SATA SSDs are much **faster than HDDs** but **slower than NVMe (PCIe)** drives.  
- Most desktop motherboards include **4–6 SATA ports** for multiple drives.  
- External drives often use **SATA-to-USB adapters**.

---
