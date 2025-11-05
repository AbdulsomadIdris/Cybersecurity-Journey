# Week 7 – Cisco Packet Tracer Practical

### 🧠 Topics Covered
- Introduction to Cisco Packet Tracer
- Creating and simulating network topologies
- Assigning IP addresses to devices
- Configuring through both GUI and CLI
- Testing connectivity using the ping command
- Observing data flow and troubleshooting network errors

---

## 💻 What Is Cisco Packet Tracer?
**Cisco Packet Tracer** is a powerful network simulation tool developed by Cisco Systems.  
It allows students and professionals to design, configure, and troubleshoot virtual networks without needing physical hardware.

---

## ⚙️ Configuration Methods
There are **two main configuration methods** in Cisco Packet Tracer:
1. **Graphical User Interface (GUI)**
2. **Command Line Interface (CLI)**

---

## 🖱️ GUI (Graphical User Interface) Configuration
The **GUI** is a visual interface that allows you to configure devices by clicking through menus and options rather than typing commands.

### Steps:
1. Click on a device (e.g., PC, router, or switch).  
2. Go to the **Desktop** or **Config** tab.  
3. Under **IP Configuration**, enter:
   - IP Address  
   - Subnet Mask  
   - Default Gateway  
4. For Routers and Switches:
   - Go to the **Config** tab.  
   - Select the interface (e.g., GigabitEthernet0/0).  
   - Assign IP addresses and enable the interface.  
5. Save and close the window.

**Example (PC GUI Configuration):**
```
IP Address: 192.168.1.2
Subnet Mask: 255.255.255.0
Default Gateway: 192.168.1.1
```

**Example (Router GUI Configuration):**
- Interface: GigabitEthernet0/0  
- IP Address: 192.168.1.1  
- Subnet Mask: 255.255.255.0  
- Status: On (No Shutdown)

---

## 💻 CLI (Command Line Interface) Configuration
The **CLI** is used for more advanced setup using Cisco IOS commands.  
It provides better control and simulates how real Cisco devices are configured.

### Example 1 – Basic Router Configuration
```
Router> enable
Router# configure terminal
Router(config)# hostname R1
R1(config)# interface g0/0
R1(config-if)# ip address 192.168.1.1 255.255.255.0
R1(config-if)# no shutdown
R1(config-if)# exit
R1(config)# interface g0/1
R1(config-if)# ip address 10.0.0.1 255.255.255.0
R1(config-if)# no shutdown
R1(config)# exit
R1# write
```

### Example 2 – Basic Switch Configuration
```
Switch> enable
Switch# configure terminal
Switch(config)# hostname SW1
SW1(config)# interface vlan 1
SW1(config-if)# ip address 192.168.1.3 255.255.255.0
SW1(config-if)# no shutdown
SW1(config-if)# exit
SW1(config)# enable secret cisco123
SW1(config)# line console 0
SW1(config-line)# password admin
SW1(config-line)# login
SW1(config-line)# exit
SW1# write
```

---

## 🌐 Connecting Devices
1. **Select Devices:** PCs, Routers, Switches, Access Points, Servers.  
2. **Connect Devices Using Proper Cables:**
   - Straight-through → PC ↔ Switch or Router ↔ Switch  
   - Crossover → Switch ↔ Switch or Router ↔ Router  
3. **Assign IP Addresses:** via GUI or CLI.  
4. **Set Default Gateways:** on PCs for internet connectivity.

---

## 🧪 Testing Connectivity
1. On any PC → go to **Desktop > Command Prompt**.  
2. Type the `ping` command to test:
   ```
   ping 192.168.1.3
   ```
3. If the connection is successful, replies will show up as:
   ```
   Reply from 192.168.1.3: bytes=32 time<1ms TTL=128
   ```
4. You can also switch to **Simulation Mode** to visually track packet movement between devices.

---

## 🧰 Practical Tasks Performed
- Created and simulated topologies (Star, Bus, Hybrid).  
- Configured routers, switches, and PCs using GUI and CLI.  
- Assigned static IP addresses and subnet masks.  
- Tested connectivity using the ping command.  
- Visualized data transfer in Simulation Mode.  
- Configured an access point for wireless connection.

---

## 🧩 Key Takeaways
- The **GUI** simplifies configuration and is great for beginners.  
- The **CLI** builds real-world Cisco skills and offers deeper control.  
- **Packet Tracer** helps you visualize, test, and understand how networks actually operate.  
Together, GUI + CLI give you a full hands-on understanding of networking operations.

---
