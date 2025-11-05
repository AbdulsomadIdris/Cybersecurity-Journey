# Week 7 – Cisco Packet Tracer Practical

### 🧠 Topics Covered
- Introduction to **Cisco Packet Tracer**
- Creating and simulating network topologies
- Assigning IP addresses to devices (using both GUI and CLI)
- Configuring routers and switches
- Testing connectivity using **ping** and **traceroute**
- Observing packet flow in **Simulation Mode**
- Troubleshooting network errors

---

## 💻 What Is Cisco Packet Tracer?
**Cisco Packet Tracer** is a powerful network simulation software developed by Cisco Systems.  
It allows users to visually design, configure, and test network setups without needing real hardware.

It’s widely used for:
- Practicing Cisco commands (CLI)
- Testing different network topologies
- Understanding data flow between devices
- Building confidence before real-world networking

---

## ⚙️ Network Setup Overview
In this practical, we built and configured networks using:
- **Routers**
- **Switches**
- **PCs**
- **Access Points**
- **Cables** (Straight-through, Crossover, Fiber)

We configured devices using **two methods**:
1. **Graphical User Interface (GUI)**
2. **Command Line Interface (CLI)**

---

## 🧩 1. Configuration Using GUI (Graphical User Interface)

### 🖥️ PC Configuration (GUI)
1. Click the **PC** → open the **Desktop tab** → select **IP Configuration**.  
2. Enter the following:
   - **IP Address:** e.g., `192.168.1.2`
   - **Subnet Mask:** `255.255.255.0`
   - **Default Gateway:** `192.168.1.1`
3. Close the window.  
4. Test connection by opening the **Command Prompt** on the PC and typing:
ping 192.168.1.3


---

### 📡 Router Configuration (GUI)
1. Click the **Router** → open the **Config tab**.  
2. Select **Interface (e.g., GigabitEthernet0/0)** → turn it **ON**.  
3. Assign:
- **IP Address:** `192.168.1.1`
- **Subnet Mask:** `255.255.255.0`
4. Repeat for additional interfaces if connecting multiple networks.
5. Save the configuration.

---

### 🔌 Switch Configuration (GUI)
1. Click the **Switch** → go to **Config tab** → select **VLAN 1**.  
2. Assign:
- **IP Address:** `192.168.1.10`
- **Subnet Mask:** `255.255.255.0`
- **Default Gateway:** `192.168.1.1`
3. Turn the interface **ON** and save.

---

## 🧠 2. Configuration Using CLI (Command Line Interface)

### 🖧 Router CLI Configuration
Router> enable
Router# configure terminal
Router(config)# hostname R1
R1(config)# enable secret myStrongPass

! Configure interface GigabitEthernet0/0
R1(config)# interface g0/0
R1(config-if)# ip address 192.168.1.1 255.255.255.0
R1(config-if)# no shutdown
R1(config-if)# exit

! Configure interface GigabitEthernet0/1
R1(config)# interface g0/1
R1(config-if)# ip address 10.0.0.1 255.255.255.0
R1(config-if)# no shutdown
R1(config-if)# exit

! Secure VTY lines (remote access)
R1(config)# line vty 0 4
R1(config-line)# password cisco
R1(config-line)# login
R1(config-line)# exit

! Save configuration
R1# write memory


---

### 🖥️ Switch CLI Configuration
Switch> enable
Switch# configure terminal
Switch(config)# hostname S1

! Assign management IP to VLAN 1
S1(config)# interface vlan 1
S1(config-if)# ip address 192.168.1.10 255.255.255.0
S1(config-if)# no shutdown
S1(config-if)# exit

! Set default gateway for switch management
S1(config)# ip default-gateway 192.168.1.1

! Secure VTY lines
S1(config)# line vty 0 4
S1(config-line)# password admin
S1(config-line)# login
S1(config-line)# exit


---

## 🔍 Verification and Testing

### ✅ Basic Verification Commands
| Command | Description |
|----------|--------------|
| `show ip interface brief` | Displays interface status and assigned IPs |
| `show running-config` | Displays current configuration |
| `show ip route` | Displays routing table (router only) |
| `ping <IP>` | Tests connectivity between devices |
| `traceroute <IP>` | Traces the path packets take to destination |

### ✅ PC Command Prompt
On any PC (Desktop → Command Prompt):
ping 192.168.1.3
tracert 192.168.1.3

---

## 🧮 Example Network Scenario
**Two LANs connected via a router:**

| Device | Interface | IP Address | Subnet Mask |
|---------|------------|-------------|--------------|
| Router R1 | G0/0 | 192.168.1.1 | 255.255.255.0 |
| Router R1 | G0/1 | 192.168.2.1 | 255.255.255.0 |
| PC1 | NIC | 192.168.1.2 | 255.255.255.0 |
| PC2 | NIC | 192.168.2.2 | 255.255.255.0 |

**Test:**
From PC1 → `ping 192.168.2.2`  
✅ If replies are successful, routing works properly.

---

## 🧰 Practical Tasks Performed
- Created and connected network devices using correct cables  
- Configured PCs, Routers, and Switches using both GUI and CLI  
- Assigned static IPs and gateways  
- Used `ping` and `traceroute` to test communication  
- Observed data flow in **Simulation Mode**  
- Saved configurations using `write memory` and `copy run start`  

---

## 🧩 Key Takeaway
Mastering **both GUI and CLI** in Packet Tracer gives you the flexibility to design, configure, and troubleshoot networks effectively.  
The GUI helps visualize setups easily, while the CLI builds real-world Cisco configuration skills crucial for advanced networking and cybersecurity.

Finalized Week 7 (GUI + CLI)
