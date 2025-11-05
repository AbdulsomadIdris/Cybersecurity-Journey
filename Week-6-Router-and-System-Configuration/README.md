# Week 6 – System and Router Configuration

### 🧠 Topics Covered
- Introduction to **Router and System Configuration**
- Understanding how routers manage and direct network traffic
- Basic LAN setup and configuration
- Access Point (AP) setup and management
- IP configuration (static and dynamic)

---

## ⚙️ Router Configuration Overview
A **router** is responsible for directing data between networks (e.g., between a LAN and the Internet).  
It operates mainly at **Layer 3 (Network Layer)** of the OSI model.

### 🔹 Common Functions of a Router
1. **Routing** – Determines the best path for data to travel.  
2. **Network Address Translation (NAT)** – Converts private IPs to public IPs for internet access.  
3. **DHCP (Dynamic Host Configuration Protocol)** – Assigns IP addresses automatically to devices.  
4. **Firewall** – Filters and protects the network from external threats.  
5. **Wireless Access Control** – Allows configuration of SSID, passwords, and Wi-Fi settings.

---

## 🧩 Steps in Basic Router Configuration
1. Connect router via **Ethernet** or **console cable**
2. Access the router interface (e.g., **192.168.1.1**) through a web browser or CLI
3. Log in with default credentials (e.g., *admin/admin*)
4. Configure:
   - Router Name / SSID  
   - IP Address or DHCP settings  
   - Default Gateway  
   - DNS settings  
   - Passwords and security options
5. Save and apply settings

---

## 🧰 Access Point (AP) Configuration
An **Access Point (AP)** allows wireless devices to connect to a wired network.  

### Steps:
1. Connect the AP to the router via LAN cable  
2. Log into the AP interface  
3. Set SSID (Wi-Fi name) and password  
4. Configure **Channel**, **Encryption (WPA2/WPA3)**, and **Mode (2.4GHz / 5GHz)**  
5. Save and test connection using wireless devices  

---

## 💻 System Configuration
### IP Address Configuration
- **Static IP:** Manually assigned to a device; does not change.  
- **Dynamic IP:** Automatically assigned by a DHCP server.

### Steps (Windows Example):
1. Go to **Network & Internet Settings**  
2. Open **Change Adapter Options**  
3. Right-click your Ethernet/Wi-Fi adapter → Properties  
4. Select **Internet Protocol Version 4 (TCP/IPv4)** → Properties  
5. Choose either:
   - **Obtain an IP address automatically** (Dynamic)  
   - **Use the following IP address** (Static)
6. Click **OK** and verify with `ipconfig` command.

---

## 🔌 Tools Used
- **Crimping tool** – For attaching RJ45 connectors  
- **LAN cable tester** – To verify connection integrity  
- **Router interface (GUI/CLI)** – For configuration  
- **Access Point setup** – For wireless connectivity testing  

---

## 🧩 Key Takeaway
System and router configuration are the backbone of real-world networking.  
Knowing how to connect, configure, and troubleshoot both wired and wireless networks is essential for every networking and cybersecurity professional.
