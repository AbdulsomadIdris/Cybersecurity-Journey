# Week 4 – IP Addressing and Subnetting

### 🧠 Topics Covered
- Concept of **IP Address** and **Protocols**
- Difference between **IPv4** and **IPv6**
- Classes of IP addresses (A, B, C, D, E)
- Public vs Private, Static vs Dynamic IPs
- Subnetting and network segmentation
- Calculation of Network, Broadcast, and Host addresses

---

## 🌐 What Is an IP Address?
An **IP Address (Internet Protocol Address)** is a unique identifier assigned to each device connected to a network.  
It acts like a digital home address, ensuring data sent across the internet reaches the correct destination.

**Versions:**
- **IPv4** – 32-bit address written as 4 decimal numbers (e.g., 192.168.1.1)
- **IPv6** – 128-bit address written in hexadecimal (e.g., 2001:0db8::7334)

---

## 📦 IP Address Classes

| Class  |           Range             | Default Subnet Mask | Example     | Usage               |
|------- |          --------           |---------------------|----------   |--------             |
| A      | 1.0.0.0 – 126.255.255.255   | 255.0.0.0           | 10.0.0.1    | Very large networks |
| B      | 128.0.0.0 – 191.255.255.255 | 255.255.0.0         | 172.16.0.1  | Medium networks     |
| C      | 192.0.0.0 – 223.255.255.255 | 255.255.255.0       | 192.168.1.1 | Small networks      |
| D      | 224.0.0.0 – 239.255.255.255 | —                   | —           | Multicast           |
| E      | 240.0.0.0 – 255.255.255.255 | —                   | —           | Experimental        |

---

## 🔒 Private vs Public IPs

| Type    | Range                         | Use Case             |
|------   |--------                       |-----------           |
| Private | 10.0.0.0 – 10.255.255.255     | Local networks       |
| Private | 172.16.0.0 – 172.31.255.255   | Local networks       |
| Private | 192.168.0.0 – 192.168.255.255 | Home/office networks |
| Public  | Outside these ranges          | Used on the Internet |

---

## ⚙️ Subnetting
**Subnetting** is the process of dividing a large network into smaller, manageable sub-networks (subnets).  
It helps improve efficiency, security, and control.

### 🎯 Advantages:
- Efficient IP usage  
- Reduced broadcast traffic  
- Easier troubleshooting  
- Better network organization  

---

## 🧮 Subnetting Formulas

| Task                             | Rule                                                                      |
|------                            |------                                                                     |
| **1. Network IP Address**        | Change all bits in the host portion to **0**                              |
| **2. Broadcast IP Address**      | Change all bits in the host portion to **1**                              |
| **3. First Host IP**             | Change all bits in the host portion to **0**, except the **last bit = 1** |
| **4. Last Host IP**              | Change all bits in the host portion to **1**, except the **last bit = 0** |
| **5. Number of Segments**        | `2^n` → where *n* = number of bits borrowed from host portion             |
| **6. Number of Devices (Hosts)** | `2^n - 2` → where *n* = number of bits left for host portion              |

---

## 💡 Example:
Given IP: `192.168.10.0/26`

| Parameter          | Calculation       | Result         |
|------------        |--------------     |---------       |
| Subnet Mask        | 255.255.255.192   | —              |
| Network Address    | All host bits = 0 | 192.168.10.0   |
| Broadcast Address  | All host bits = 1 | 192.168.10.63  |
| First Host         | Network + 1       | 192.168.10.1   |
| Last Host          | Broadcast - 1     | 192.168.10.62  |
| Number of Segments | 2^(2)             | 4              |
| Number of Devices  | 2^(6) - 2         | 62             |

---

## 🧰 Practical Work
- Subnetted Class C networks manually  
- Calculated Network, Broadcast, First and Last Host IPs  
- Determined Number of Segments and Devices  
- Configured IP addressing in simulation environments  

---

## 🧩 Key Takeaway
Subnetting is at the heart of IP management.  
It improves performance, enhances control, and ensures efficient use of address space — a core skill for every network and cybersecurity professional.
