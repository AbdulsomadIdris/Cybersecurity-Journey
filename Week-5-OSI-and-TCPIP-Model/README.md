# Week 5 – OSI & TCP/IP Models and Port Numbers

### 🧠 Topics Covered
- The **OSI (Open Systems Interconnection)** model  
- The **TCP/IP model**  
- Functions of each layer  
- Relationship between OSI and TCP/IP models  
- Common port numbers and their services

---

## 🏗️ OSI Model (7 Layers)
The **OSI model** standardizes how data is transmitted across a network.  
It divides communication into **seven layers**, each with its own role.

| Layer | Name | Function |
|--------|------|-----------|
| 7 | **Application** | Provides network services to end users (e.g., web browsers, email). |
| 6 | **Presentation** | Translates data formats, encryption, and compression. |
| 5 | **Session** | Establishes, manages, and terminates connections. |
| 4 | **Transport** | Ensures reliable data delivery using TCP/UDP. |
| 3 | **Network** | Handles IP addressing and routing (logical addressing). |
| 2 | **Data Link** | Manages MAC addressing and error detection. |
| 1 | **Physical** | Deals with hardware, cables, and electrical signals. |

**Mnemonic to remember:**  
🧠 *"Please Do Not Throw Sausage Pizza Away"* → (Physical, Data Link, Network, Transport, Session, Presentation, Application)

---

## 🌐 TCP/IP Model (4 Layers)

| Layer | Equivalent OSI Layers | Function |
|--------|-----------------------|-----------|
| 4 | Application (7–5) | User applications and protocols (HTTP, FTP, DNS, etc.) |
| 3 | Transport (4) | Communication reliability (TCP/UDP). |
| 2 | Internet (3) | Logical addressing and routing using IP. |
| 1 | Network Access (2–1) | Physical transmission and MAC-level access. |

---

## 🔁 Relationship Between OSI and TCP/IP Models
| OSI Layer | TCP/IP Equivalent | Example Protocols |
|------------|------------------|--------------------|
| Application | Application | HTTP, HTTPS, FTP, SMTP, DNS |
| Presentation | Application | SSL, TLS, JPEG, MPEG |
| Session | Application | NetBIOS, RPC |
| Transport | Transport | TCP, UDP |
| Network | Internet | IP, ICMP |
| Data Link | Network Access | Ethernet, PPP |
| Physical | Network Access | Cables, Hubs, Wi-Fi |

**Key Point:**  
The TCP/IP model is a simplified, practical version of the OSI model used in real-world networking.

---

## ⚙️ Common Port Numbers and Their Services

| Port | Protocol | Service |
|------|-----------|----------|
| 20 / 21 | TCP | FTP (File Transfer Protocol) |
| 22 | TCP | SSH (Secure Shell) |
| 23 | TCP | Telnet (Remote Access) |
| 25 | TCP | SMTP (Mail Sending) |
| 53 | TCP/UDP | DNS (Domain Name System) |
| 67 / 68 | UDP | DHCP (IP Address Assignment) |
| 69 | UDP | TFTP (Trivial File Transfer Protocol) |
| 80 | TCP | HTTP (Web Browsing) |
| 110 | TCP | POP3 (Mail Retrieval) |
| 123 | UDP | NTP (Time Synchronization) |
| 143 | TCP | IMAP (Mail Retrieval) |
| 161 / 162 | UDP | SNMP (Network Management) |
| 389 | TCP/UDP | LDAP (Directory Services) |
| 443 | TCP | HTTPS (Secure Web Browsing) |
| 445 | TCP | SMB (File Sharing / Windows File Transfer) |
| 3389 | TCP | RDP (Remote Desktop Protocol) |

---

## 🧰 Practical Work
- Compared the OSI and TCP/IP models layer-by-layer  
- Matched real protocols (HTTP, DNS, FTP) to their corresponding layers  
- Identified common port numbers using **netstat** and Wireshark tools  
- Understood how TCP ensures reliable data delivery while UDP is faster but unreliable  

---

## 🧩 Key Takeaway
The OSI and TCP/IP models provide the framework for all digital communication.  
Understanding layers and ports allows network professionals to diagnose, secure, and optimize connections effectively.
