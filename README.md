# Huawei eNSP Lab Exercises

This repository contains my lab exercises for learning Huawei networking technologies using the eNSP network simulator.Each lab focuses on basic networking concepts and includes objectives, topology diagrams,configurations, and verifications. 
This layout reflects my ongoing journey with Huawei eNSP. Enjoy exploring and learning along with me!

---

## Table of Contents
1. [Lab 1: IPv4 Addressing and Routing](#lab-1-ipv4-addressing-and-routing)
2. [Lab 2: OSPF Routing](#lab-2-ospf-routing)
3. [Lab 3.1: Ethernet Basics and VLAN Configuration](#lab-31-ethernet-basics-and-vlan-configuration)
4. [Lab 3.2: Spanning Tree Configuration](#lab-32-spanning-tree-configuration)
5. [Lab 3.3: Ethernet Link Aggregation](#lab-33-ethernet-link-aggregation)
6. [Lab 4.0: Inter-VLAN Communication](#lab-40-inter-vlan-communication)
7. [Lab 4.1: ACL Configuration](#lab-41-acl-configuration)
8. [Lab 4.2: Local AAA Configuration](#lab-42-local-aaa-configuration)
9. [Lab 4.3: NAT Configuration](#lab-43-nat-configuration)
10. [Lab 5.1: FTP Configuration](#lab-51-ftp-configuration)
11. [Lab 5.2: DHCP Configuration](#lab-52-dhcp-configuration)
12. [Lab 6: Creating a WLAN](#lab-6-creating-a-wlan)
13. [Lab 7: Creating an IPv6 Network](#lab-7-creating-an-ipv6-network)

---

## Navigating the Repository

- **Table of Contents**: Click a lab in the list above to jump right to that section.
- **Objectives**: Each lab begins with brief objectives.
- **Topology Diagrams**: Get a visual overview of the network setup for each exercise.
- **Configuration Steps**: If you choose to,follow the commands and add screenshots that show how each lab is set up.
- **Verification**: Confirm if the lab works, through ping , tracert and by confirming in the routing tables.
- **Personal Notes**: I've added my own notes and observations as I progressed.
- **Resources**: I have included links to documentation and guides in the Resources section at the end.

---

## Lab 1: IPv4 Addressing and Routing

### Objectives

- Assigning IPv4 addresses to network interfaces.
-  Examine how loopback interfaces function and their role in network testing and management.
- Investigate how direct routing paths are generated and understand the underlying principles.
-  Learn to set up static routes, focusing on the necessary conditions for these routes to become effective.
-  Using tools like ping and tracert to assess the performance and connectivity of the network layer.
- Comparing various static routing scenarios to determine when and why each approach is appropriate. 

### Topology
![Lab 1 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images/1.%20Lab%201%20IPv4%20Addressing%20and%20Routing/TOPO.IPV4%20ADDRESSING%20AND%20ROUTING%20CONFIG.png)


**Key commands**
Below are the key commands , organized by lab and device. Click on each lab to view the commands.

---

<details>
  <summary><strong>Lab 1: IPv4 Addressing and Routing </strong></summary>

| **Device**         | **Command**                                                                                  | **Description**                                                                                                        |
|--------------------|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| **All**            | `display ip interface brief`                                                                 | Displays brief interface IP address and status information.                                                          |
| **All**            | `display ip routing-table`                                                                   | Displays the IP routing table.                                                                                         |
| **R1, R2, R3**     | `interface <interface-type><interface-number>`                                               | Enters the view of a specific physical interface.                                                                     |
| **R1, R2, R3**     | `ip address <ip-address> <mask-length>`                                                      | Assigns an IPv4 address and mask length to an interface.                                                               |
| **R1, R2, R3**     | `interface LoopBack<interface-number>`                                                       | Enters the view of a logical loopback interface.                                                                       |
| **R1, R2, R3**     | `ip route-static <dest-addr> <mask> <next-hop> [preference <value>]`                         | Configures a static IPv4 route, optionally setting a preference for backup.                                            |
| **R1, R2, R3**     | `ping -a <source-ip> <destination-ip>`                                                         | Pings a destination specifying the source IP address.                                                                  |
| **R1, R2, R3**     | `tracert -a <source-ip> <destination-ip>`                                                       | Traces the route to a destination specifying the source IP address.                                                    |
| **R1, R2**         | `shutdown`                                                                                   | Administratively disables an interface (used for testing backup route).                                                |
| **R1, R2**         | `undo shutdown`                                                                              | Re-enables an administratively disabled interface.                                                                     |
| **R1, R2, R3**     | `undo ip route-static <dest-addr> <mask> <next-hop> [preference <value>]`                     | Removes a configured static IPv4 route.                                                                                |
| **R1**             | `ip route-static 0.0.0.0 0 <next-hop-address>`                                               | Configures a default static route.                                                                                     |

</details>

---


### Configuration Screenshots
-  COMING SOON

### Verification
- COMING SOON.

---

## Lab 2: OSPF Routing

### Objectives

- Using OSPF commands to manage and troubleshoot routing configurations.
- Inspecting and verifying the operational status of OSPF .
- Adjusting route costs to manipulate and optimize OSPF route decisions.
- Understanding OSPF’s advertisement of default routes and their impact on network topology.
- Implementing and testing OSPF authentication mechanisms to safeguard routing exchanges from unauthorized access.
  
### Topology
![Lab 2 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images/2.%20Lab%202%20OSPF%20Routing/topo.ospf%20routing.png)


**Key commands**
details>
  <summary><strong>Lab 2: OSPF Routing </strong></summary>

| **Device**         | **Command**                                                                                               | **Description**                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| **R1, R2, R3**     | `ospf [process-id]`                                                                                       | Creates and enters the OSPF process view.                                                               |
| **R1, R2, R3**     | `area <area-id>`                                                                                          | Creates an OSPF area and enters the area view.                                                          |
| **R1, R2, R3**     | `network <network-address> <wildcard-mask>`                                                               | Enables OSPF on interfaces matching the network/wildcard within the area.                               |
| **R1, R2, R3**     | `network <ip-address> 0.0.0.0`                                                                              | Enables OSPF specifically on the interface with the given IP within the area.                           |
| **R1, R2, R3**     | `display ospf peer`<br>`display ospf peer brief`                                                           | Displays OSPF neighbor information (detailed/brief).                                                    |
| **R1, R2, R3**     | `display ip routing-table protocol ospf`                                                                  | Displays only the OSPF routes in the IP routing table.                                                  |
| **R1, R2**         | `ospf authentication-mode md5 <key-id> cipher <password>`                                                  | Configures MD5 authentication on an OSPF interface.                                                     |
| **R3**             | `authentication-mode md5 <key-id> cipher <password>`                                                       | Configures MD5 authentication for an entire OSPF area (within area view).                                 |
| **R1**             | `default-route-advertise [always]`                                                                         | Configures the router to advertise a default route into OSPF.                                           |
| **R1**             | `ospf cost <value>`                                                                                        | Manually sets the OSPF cost for an interface to influence path selection.                               |

</details>

---

### Configuration Screenshots
-  screenshots of OSPF configuration and command outputs COMING SOON.

### Verification
-COMING SOON are screenshots showing OSPF neighbor relationships, routing tables, and traceroute outputs.

---

## Lab 3.1: Ethernet Basics and VLAN Configuration

### Objectives

- Developing a clear understanding of how Ethernet switching operates at the fundamental level.
- Configuring basic ethernet settings and setting up VLANs on network devices to segment traffic effectively.
- Validating VLAN assignments and inter device connectivity for proper functioning of the configurations.



### Topology
![Lab 3.1 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images/3.1%20Lab%203.1%20Ethernet%20Basics%20and%20VLAN%20Configuration/topo.ethernet%20Basics%20and%20Vlan%20Config.png)

**Key commands**
<details>
  <summary><strong>Lab 3.1: Ethernet Basics and VLAN Configuration </strong></summary>

| **Device**         | **Command**                                                                                                  | **Description**                                                                                               |
|--------------------|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| **S1, S2**         | `vlan <vlan-id>`<br>`vlan batch <vlan-list>`                                                                   | Creates one or more VLANs.                                                                                      |
| **S1, S2**         | `interface <interface-type><interface-number>`                                                                | Enters the interface view.                                                                                     |
| **S1, S2**         | `port link-type access`                                                                                        | Sets the interface link type to Access.                                                                        |
| **S1, S2**         | `port default vlan <vlan-id>`                                                                                  | Assigns an access port to a specific VLAN (sets PVID).                                                         |
| **S1, S2**         | `port link-type trunk`                                                                                          | Sets the interface link type to Trunk.                                                                         |
| **S1, S2**         | `port trunk allow-pass vlan <vlan-list>`                                                                        | Specifies which VLANs are allowed on the trunk port.                                                           |
| **S1, S2**         | `undo port trunk allow-pass vlan 1`                                                                             | Removes VLAN 1 from the allowed list on a trunk port (security best practice).                                   |
| **S2**             | `mac-vlan mac-address <mac-address>`                                                                            | Associates a MAC address with the current VLAN (within VLAN view).                                               |
| **S2**             | `port link-type hybrid`                                                                                         | Sets the interface link type to Hybrid.                                                                         |
| **S2**             | `port hybrid untagged vlan <vlan-id>`                                                                            | Configures a hybrid port to send frames for the specified VLAN untagged.                                          |
| **S2**             | `mac-vlan enable`                                                                                               | Enables MAC address-based VLAN assignment on the interface.                                                     |
| **S1, S2**         | `display vlan`<br>`display vlan verbose`                                                                       | Displays VLAN information (summary/detailed).                                                                   |
| **S2**             | `display mac-vlan vlan <vlan-id>`                                                                               | Displays MAC-to-VLAN mappings for a VLAN.                                                                         |
| **S3, S4**         | `undo portswitch`                                                                                               | Changes an interface from Layer 2 to Layer 3 mode (if applicable).                                                |
| **S3, S4**         | `interface Vlanif <vlan-id>`                                                                                     | Creates a Layer 3 VLAN interface (if applicable).                                                                 |
| **R1, R3, S3, S4**  | `ip address <ip-address> <mask-length>`                                                                          | Configures IP addresses (on physical L3 or VLANIF interfaces).                                                    |

</details>

### Configuration Screenshots
- screenshots COMING SOON

### Verification
-  screenshots Soon.

---

## Lab 3.2: Spanning Tree Configuration

### Objectives

- Understanding of how the Spanning Tree Protocol prevents network loops and ensures redundancy.
- Configuring key STP parameters on network switches to optimize network performance.
- Verifying STP operation by identifying root bridges and port roles, and troubleshooting any anomalies in the S.T.P.
### Topology
![Lab 3.2 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images/3.2%20Lab%203.2%20Spanning%20Tree%20Configuration/topo.%20spanning%20tree%20configuration.png)

**Key commands**
<details>
  <summary><strong>Lab 3.2: Spanning Tree Configuration</strong></summary>

| **Device**         | **Command**                                                                                                  | **Description**                                                                                     |
|--------------------|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| **S1, S2, S3, S4**  | `stp enable`                                                                                                  | Enables STP globally (often default).                                                               |
| **S1, S2, S3, S4**  | `stp mode {stp \| rstp \| mstp}`                                                                               | Sets the Spanning Tree mode for the switch.                                                         |
| **S1, S2, S3, S4**  | `display stp`<br>`display stp brief`                                                                          | Displays STP status (detailed/brief).                                                               |
| **S1**             | `stp root primary`                                                                                             | Configures the switch as the primary root bridge (priority 0).                                      |
| **S2**             | `stp root secondary`                                                                                           | Configures the switch as the secondary root bridge (priority 4096).                                 |
| **S4**             | `stp cost <value>`                                                                                             | Manually sets the STP cost on a port to influence path selection.                                   |
| **S3**             | `stp edged-port enable`                                                                                        | Configures a port connected to end devices as an edge port (for faster convergence).                |

</details>

### Configuration Screenshots
-  COMING SOON.

### Verification
- COMING SOON.

---
## Lab 3.3: Ethernet Link Aggregation

### Objectives

- Manually configuring link aggregation to understand its foundational principles.
- Configuring link aggregation using static LACP mode.
- verifying which aggregated links are active during static LACP operations.
- Exploring and applying additional static LACP features to enhance network performance and redundancy.
  
  ### Topology
![Lab 3.3 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images/3.3%20Lab%203.3%20Ethernet%20Link%20Aggregation/topo.ethernet%20link%20aggregation.png)


**Key commands**
<details>
  <summary><strong>Lab 3.3: Ethernet Link Aggregation </strong></summary>

| **Device**         | **Command**                                                                                                  | **Description**                                                                                        |
|--------------------|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| **S1, S2**         | `interface Eth-Trunk <trunk-id>`                                                                               | Creates a logical Eth-Trunk interface.                                                                 |
| **S1, S2**         | `mode manual load-balance`                                                                                     | Sets Eth-Trunk mode to manual (static).                                                                |
| **S1, S2**         | `mode lacp`                                                                                                   | Sets Eth-Trunk mode to LACP.                                                                           |
| **S1, S2**         | `eth-trunk <trunk-id>`                                                                                          | Adds the current physical interface to the specified Eth-Trunk.                                      |
| **S1, S2**         | `trunkport <interface-type> <interface-number> [to <interface-number>]`                                         | Adds member ports to the current Eth-Trunk (entered within Eth-Trunk view).                            |
| **S1, S2**         | `undo trunkport <interface-type> <interface-number> [to <interface-number>]`                                    | Removes member ports from the current Eth-Trunk.                                                     |
| **S1, S2**         | `display eth-trunk <trunk-id>`                                                                                  | Displays the status of the Eth-Trunk.                                                                  |
| **S1**             | `lacp priority <value>`                                                                                         | Sets the LACP system/port priority (lower is better for election/active selection).                    |
| **S1**             | `max active-linknumber <value>`                                                                               | Sets the maximum number of active links in the LACP group.                                             |
| **S1**             | `least active-linknumber <value>`                                                                             | Sets the minimum number of active links required for the LACP group to be UP.                           |
| **S1**             | `lacp preempt enable`                                                                                          | Allows a higher-priority link to become active again after recovery.                                   |
| **S1**             | `load-balance {dst-ip \| src-ip \| ...}`                                                                       | Sets the load balancing algorithm for the Eth-Trunk.                                                 |

</details>
### Configuration Screenshots
-  COMING SOON.
### Verification
- screenshots of ping results etc. COMING SOON

---
## Lab 4.0: Inter-VLAN Communication

### Objectives

- Using Dot1q termination subinterfaces to implement inter-VLAN 
communication
- Using VLANIF interfaces to implement inter-VLAN communication
-Examining the process by which network traffic is routed between VLANs.

### Topology
![Lab 4.0 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images/4.0%20Lab%204%20Inter-VLAN%20Communication/topo.Inter-VLAN-Communication.png)
**Key commands**


### Configuration Screenshots
- screenshots of ACL configuration and command outputs here.

### Verification
-  screenshots COMING SOON


---
 ## Lab 4.1: ACL Configuration

### Objectives

- Mastering ACL Basics for Network Security.
- Configuring ACL rules on Huawei devices.
- Verifying ACL functionality using connectivity tests . 


### Topology
![Lab 4.1 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images/4.1%20Lab%204.1%20ACL%20Configuration/topo.png)
**Key Commands**
### Configuration Screenshots
- COMING SOON screenshots of ACL configuration and command outputs here.

### Verification
- COMING SOON screenshots showing ACL rule listings and ping,traceroute test results.

---

## Lab 4.2: Local AAA Configuration

### Objectives

- Understand the fundamentals of AAA (Authentication, Authorization, and Accounting)
- Configure local AAA settings on Huawei devices
- Verify AAA user authentication and test network access  

### Topology
![Lab 4.2 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images/4.2%20Lab%204.2%20Local%20AAA%20Configuration/topo-AAA-configuration.png)
**Key commands**

### Configuration Screenshots
- COMING SOON 

### Verification
-  screenshots COMING SOON

---

## Lab 4.3: NAT Configuration

### Objectives

- Understanding NAT configuration, its purpose and types.
- Setting up NAT on Huawei devices.
- Validating and Troubleshooting NAT: Verifying translations and resolve issues.


### Topology
![Lab 4.3 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images/4.3%20Lab%204.3%20%20NAT%20Configuration/topogy%20diagram.png)
**Key commands**

### Configuration Screenshots
- COMING SOON.

### Verification
- COMING SOON.

---

## Lab 5.1: FTP Configuration

### Objectives

- Understanding FTP concepts and their use.
- Configuring both FTP server and client.
-  Verifying connectivity and file exchange.

### Topology
![Lab 5.1 Topology](path/to/lab5.1-topology.png)
**Key commands**

### Configuration Screenshots
-  COMING SOON

### Verification
- Coming soon screenshots .

---

## Lab 5.2: DHCP Configuration

### Objectives

- Understanding the operation of Dynamic Host Configuration Protocol (DHCP)
- Configuring DHCP services on Huawei devices
- Verifying DHCP lease assignments and testing client connectivity  


### Topology
![Lab 5.2 Topology](path/to/lab5.2-topology.png)
**Key commands**

### Configuration Screenshots
- screenshots of DHCP server configuration and DHCP lease outputs. Soon.

### Verification
- coming soon

---

## Lab 6: Creating a WLAN

### Objectives

- Learning key WLAN setup principles.
- Configuring WLAN on Huawei Devices.
- Testing and Troubleshooting Connectivity to ensure stable wireless access.

### Topology
![Lab 6 Topology](path/to/lab6-topology.png)
**Key commands**

### Configuration Screenshots
- screenshots of WLAN configuration interfaces and settings,coming soon

### Verification
- COMING SOON

---

## Lab 7: Creating an IPv6 Network

### Objectives
- Understanding IPv6 addressing and routing concepts.
- Configuring IPv6 addresses on devices.
- Testing connectivity and fixing issues.
  
### Topology
![Lab 7 Topology](path/to/lab7-topology.png)
**Key commands**

### Configuration Screenshots
- Coming soon

### Verification
- Coming soon.

---

## Tips

- Always save your configurations and topo to avoid losing progress.
- Use the `display` command to verify configurations on Huawei devices.
- Use question mark incase you forget the full command.

---

## Resources
- [Infosyte: How to Install Huawei eNSP Network Simulator](https://infosyte.com/how-to-install-huawei-ensp-network-simulator/)
- [Wireshark Documentation](https://www.wireshark.org/docs/) 
- [Huawei Talent Learning Portal](https://e.huawei.com/en/talent/learning/#/home) - Explore official Huawei learning and training resources.
- [Basic Networking Cheat Sheet (Community Maintained)](https://github.com/trimstray/the-book-of-secret-knowledge)

---

- Any contributions and suggestions are welcome.
