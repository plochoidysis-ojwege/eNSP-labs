
# Repository Moved! 🚧

**This repository has been moved to a new location to continue development and updates.**

All future content, fixes, and contributions for the eNSP Lab Exercises will be available at:

### New Repository Location:
[**plochoidysis-ojwege/eNSP-lab-exercises**](https://github.com/plochoidysis-ojwege/eNSP-lab-exercises)

**Please update your bookmarks, clones, and any references you may have to this repository.**

---


This repository will no longer be updated.
Thank you for your understanding!


---

# Huawei eNSP Lab Exercises

This repository contains lab exercises for learning Huawei networking technologies using the eNSP network simulator.Each lab focuses on basic networking concepts and includes objectives, topology diagrams,configurations, and verifications. 
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
- **Generated Audio overviews**: Below the topology diagram of each lab,is an MP4 audio overview .Incase an audio fail to play, just re-sync or refresh your browser(This is a common issue ,especially after playing an audio, the next could fail).
- **Key Commands**: Just below the generated audio overview, click on each lab key commands,they are on collapsible sections
- **Configuration Steps**: If you choose to,follow the commands and add screenshots that show how each lab is set up. I have added some verications in collasible sections, but it's a journey ,soon all sections will be updated.
- **Verification**: Confirm if the lab works, through ping , tracert and by confirming in the routing tables.
- **Personal Notes**: I've added my own notes and observations as I progressed.
- **Resources**: I have included links to documentation and guides in the Resources section at the end.


---


https://github.com/user-attachments/assets/9c5b449d-a37e-4062-be6d-fa604b7c1d06




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
![Lab 1 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/1.%20Lab%201%20IPv4%20Addressing%20and%20Routing/TOPO.IPV4%20ADDRESSING%20AND%20ROUTING%20CONFIG.png)




https://github.com/user-attachments/assets/36ceffa7-4059-4c88-a59e-a5474b8fd791





**Key commands**


Below are the key commands , organized by lab and device. Click on thelab to view the commands.

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



### Verification/ configuration screenshots
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
![Lab 2 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/2.%20Lab%202%20OSPF%20Routing/topo.ospf%20routing.png)






https://github.com/user-attachments/assets/42ac10f7-c961-474f-80b1-2970678cc545



**Key commands**

<details>
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
![Lab 3.1 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/3.1%20Lab%203.1%20Ethernet%20Basics%20and%20VLAN%20Configuration/topo.ethernet%20Basics%20and%20Vlan%20Config.png)



https://github.com/user-attachments/assets/ef2bdf4b-fad4-48ab-9f40-c4a91d3d8e6c



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



### Verification/configuration screenshots
-  screenshots of OSPF neighbor relationships, routing tables, and traceroute outputs COMING SOON.

---

## Lab 3.2: Spanning Tree Configuration

### Objectives

- Understanding of how the Spanning Tree Protocol prevents network loops and ensures redundancy.
- Configuring key STP parameters on network switches to optimize network performance.
- Verifying STP operation by identifying root bridges and port roles, and troubleshooting any anomalies in the S.T.P.
### Topology
![Lab 3.2 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/3.2%20Lab%203.2%20Spanning%20Tree%20Configuration/topo.%20spanning%20tree%20configuration.png)




https://github.com/user-attachments/assets/3b47bd3c-90e0-4ff9-aadf-8a6b10dd4679



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




### Verification / configuration screenshots

- <details>
  <summary>Verification Screenshots</summary>
  
  ![3.2 STP data capture before any configurations](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/3.2%20Lab%203.2%20Spanning%20Tree%20Configuration/3.2%20Stp%20data%20capture%20before%20any%20configurations.jpeg)
  
  ![3.2 Data capture](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/3.2%20Lab%203.2%20Spanning%20Tree%20Configuration/3.2%20data%20capture%2C%20i%20dont%20know%20which%20one.jpeg)
  
  ![3.2 display stp brief S1](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/3.2%20Lab%203.2%20Spanning%20Tree%20Configuration/3.2%20disp%20stp%20brief%20S1.jpeg)
  
  ![3.2 display stp brief S2](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/3.2%20Lab%203.2%20Spanning%20Tree%20Configuration/3.2%20disp%20stp%20brief%20S2.jpeg)
  
  ![3.2 display stp brief S3](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/3.2%20Lab%203.2%20Spanning%20Tree%20Configuration/3.2%20disp%20stp%20brief%20S3.jpeg)
  
  ![3.2 display stp brief S4](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/3.2%20Lab%203.2%20Spanning%20Tree%20Configuration/3.2%20disp%20stp%20brief%20S4.jpeg)
  
  ![3.2 displaying stp for S1](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/3.2%20Lab%203.2%20Spanning%20Tree%20Configuration/3.2%20displaying%20stp%20for%20S1.jpeg)
  
  ![3.2 the bridge id of that particular bridge](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/3.2%20Lab%203.2%20Spanning%20Tree%20Configuration/3.2%20the%20bridge%20id%20of%20that%20particular%20bridge.jpeg)
  
</details>



---
## Lab 3.3: Ethernet Link Aggregation

### Objectives

- Manually configuring link aggregation to understand its foundational principles.
- Configuring link aggregation using static LACP mode.
- verifying which aggregated links are active during static LACP operations.
- Exploring and applying additional static LACP features to enhance network performance and redundancy.
  
  ### Topology
![Lab 3.3 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/3.3%20Lab%203.3%20Ethernet%20Link%20Aggregation/topo.ethernet%20link%20aggregation.png)




https://github.com/user-attachments/assets/9f59783b-f3c4-4dea-bb44-0399cd09255c




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


### Verification/ configuration screenshots
- screenshots of ping results etc. COMING SOON

---
## Lab 4.0: Inter-VLAN Communication

### Objectives

- Using Dot1q termination subinterfaces to implement inter-VLAN 
communication
- Using VLANIF interfaces to implement inter-VLAN communication
-Examining the process by which network traffic is routed between VLANs.

### Topology
![Lab 4.0 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.0%20Lab%204%20Inter-VLAN%20Communication/topo.Inter-VLAN-Communication.png)




https://github.com/user-attachments/assets/9eb75b4b-6a27-45b7-9e32-530b126bc161




**Key commands**
<details>
  <summary><strong>Lab 4.0: Inter-VLAN Communication</strong></summary>

### Method 1: Router-on-a-Stick (Dot1q Subinterfaces)

| **Device**    | **Command**                                                                                | **Description**                                                                                         |
|---------------|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| **S1**        | `interface GigabitEthernet0/0/1`                                                             | Enters the interface view connected to the router.                                                    |
| **S1**        | `port link-type trunk`                                                                      | Sets the port connected to the router as a trunk.                                                     |
| **S1**        | `port trunk allow-pass vlan 2 3`                                                             | Allows necessary VLANs on the trunk link to the router.                                               |
| **R1**        | `interface GigabitEthernet0/0/1.<subinterface-number>`                                     | Creates a logical subinterface.                                                                       |
| **R1**        | `dot1q termination vid <vlan-id>`                                                           | Associates the subinterface with a specific VLAN ID.                                                  |
| **R1**        | `arp broadcast enable`                                                                      | Allows ARP broadcasts on the subinterface (may be default).                                           |
| **R1**        | `ip address <gateway-ip> <mask-length>`                                                     | Assigns the gateway IP address for the VLAN to the subinterface.                                      |
| **R2, R3**    | `ip route-static 0.0.0.0 0 <gateway-ip>`                                                    | Configures the default gateway on end devices.                                                        |

### Method 2: Layer 3 Switch (VLANIF Interfaces)

| **Device**    | **Command**                                                                                | **Description**                                                                                         |
|---------------|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| **S1**        | `interface Vlanif <vlan-id>`                                                                 | Creates a Layer 3 VLAN interface.                                                                       |
| **S1**        | `ip address <gateway-ip> <mask-length>`                                                     | Assigns the gateway IP address for the VLAN to the VLANIF interface.                                    |
| **S1**        | `interface GigabitEthernet0/0/2`<br>`interface GigabitEthernet0/0/3`                             | Enters interface view for ports connected to end devices.                                             |
| **S1**        | `port link-type access`                                                                      | Sets ports connected to end devices as access ports.                                                  |
| **S1**        | `port default vlan <vlan-id>`                                                                 | Assigns access ports to their respective VLANs.                                                       |
| **R2, R3**    | `ip route-static 0.0.0.0 0 <gateway-ip>`                                                    | Configures the default gateway on end devices.                                                        |

</details>



### Verification/ configuration screenshots

- <details>
  <summary>Verification Screenshots</summary>
  
  ![Before trunkport creation](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.0%20Lab%204%20Inter-VLAN%20Communication/b4-trunkport-must-be-created-first-before-allowing-pass-vlan-2and3%7BWASnotIncludedINtheMANUAL%7D.png)
  
  ![Connectivity between VLANs after configurations](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.0%20Lab%204%20Inter-VLAN%20Communication/connectivityBTNvlansAFTERconfigurations.png)
  
  ![Different VLANs R2 & R3 cannot communicate](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.0%20Lab%204%20Inter-VLAN%20Communication/different-vlans-R2-R3%20cannot-communicate.png)
  
  ![Interface VLANIF view](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.0%20Lab%204%20Inter-VLAN%20Communication/interface-vlanif.png)
  
  ![Ping results before configuring the switch](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.0%20Lab%204%20Inter-VLAN%20Communication/ping-results-before-configuring-the-switch_R3-cannot-reach-R2%20and-vice-varsa.png)
  
  ![Ping and tracert results after VLANIF](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.0%20Lab%204%20Inter-VLAN%20Communication/pingANDtracert-results-after-vlanif.png)
  
</details>

---
 ## Lab 4.1: ACL Configuration

### Objectives

- Mastering ACL Basics for Network Security.
- Configuring ACL rules on Huawei devices.
- Verifying ACL functionality using connectivity tests . 


### Topology
![Lab 4.1 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.1%20Lab%204.1%20ACL%20Configuration/topo.png)






https://github.com/user-attachments/assets/b059e532-4c7c-4f1b-8c18-85dfea7a3619



**Key Commands**
<details>
  <summary><strong>Lab 4.1: ACL Configuration</strong></summary>

| **Device**         | **Command**                                                                                                     | **Description**                                                                                                 |
|--------------------|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| **R1, R2, R3**     | *OSPF Configuration (Refer to Lab 2.2 commands to ensure basic connectivity first)*                             |                                                                                                               |
| **R3**             | `telnet server enable`                                                                                          | Enables the Telnet server service.                                                                              |
| **R3**             | `user-interface vty 0 4`                                                                                         | Enters VTY line view.                                                                                           |
| **R3**             | `authentication-mode password`                                                                                  | Sets VTY authentication to use a local password.                                                                |
| **R3**             | `set authentication password cipher <password>`                                                                | Sets the VTY login password (encrypted).                                                                        |
| **R3**             | `user privilege level <level>`                                                                                   | Sets the privilege level for VTY users.                                                                         |
| **R3/R2**         | `acl <acl-number>`                                                                                               | Creates an ACL (e.g., 3000).                                                                                      |
| **R3/R2**         | `rule <id> {permit\|deny} tcp source <ip> <wc> destination <ip> <wc> [destination-port eq <port>]`               | Defines ACL rules to permit/deny specific TCP traffic (e.g., Telnet port 23).                                    |
| **R3**             | `acl <acl-number> inbound`                                                                                       | Applies ACL to filter incoming VTY connections (Method 1).                                                      |
| **R2**             | `interface GigabitEthernet0/0/3`                                                                                 | Enters interface view (Method 2).                                                                                 |
| **R2**             | `traffic-filter inbound acl <acl-number>`                                                                        | Applies ACL to filter incoming traffic on the interface (Method 2).                                               |
| **R3/R2**         | `display acl <acl-number>`                                                                                       | Displays the ACL configuration and match counts.                                                                |
| **R1**             | `telnet -a <source-ip> <destination-ip>`                                                                         | Initiates Telnet specifying the source IP for testing ACL rules.                                                  |

</details>
### Configuration Screenshots
- COMING SOON screenshots of ACL configuration and command outputs here.

### Verification/ configuration screenshots

### Configuration Screenshots
- <details>
  <summary>Configuration Screenshots</summary>
  
  ![ACL configured on R2](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.1%20Lab%204.1%20ACL%20Configuration/ACL-configured-on-R2.png)
  
  ![Filtering traffic on R2 GE0.0.3 of R3 and displaying ACL](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.1%20Lab%204.1%20ACL%20Configuration/Filtering-traffic-on-R2%20GE0.0.3%20of%20R3-and-displaying-ACL.png)
  
  ![R1](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.1%20Lab%204.1%20ACL%20Configuration/R1.png)
  
  ![R3 configured as server](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.1%20Lab%204.1%20ACL%20Configuration/R3-configured-as-server..png)
  
</details>

### Verification/ configuration screenshots
- <details>
  <summary>Verification Screenshots</summary>
  
  ![Verification: Telnetting R3 = SUCCESSFUL on R1](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.1%20Lab%204.1%20ACL%20Configuration/VERIFICATION-telnetting-R3%3DSUCCESSFULL-ON-R1.png)
  
  ![Display ACL config after configuring](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.1%20Lab%204.1%20ACL%20Configuration/disp-ACL-config(after-configuring).png)
  
  ![Displaying ACL config](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.1%20Lab%204.1%20ACL%20Configuration/displaying-acl-config.png)
  
  ![Ping on R3 just after config](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.1%20Lab%204.1%20ACL%20Configuration/ping-on-R3-jus-after-config..png)
  
</details>


---

## Lab 4.2: Local AAA Configuration

### Objectives

- Understand the fundamentals of AAA (Authentication, Authorization, and Accounting)
- Configure local AAA settings on Huawei devices
- Verify AAA user authentication and test network access  


### Topology
![Lab 4.2 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.2%20Lab%204.2%20Local%20AAA%20Configuration/topo-AAA-configuration.png)



https://github.com/user-attachments/assets/47df12d2-3889-4478-b6e1-38151c1dd29c



**Key commands**
<details>
  <summary><strong>Lab 4.2: Local AAA Configuration (Section 4.2)</strong></summary>

| **Device**         | **Command**                                                                                                     | **Description**                                                                                                      |
|--------------------|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **R1, R2**         | *IP Address Configuration to ensure basic connectivity between devices*                                        |                                                                                                                      |
| **R2**             | `aaa`                                                                                                           | Enters AAA configuration view.                                                                                       |
| **R2**             | `authentication-scheme <name>`                                                                                  | Creates an authentication scheme.                                                                                    |
| **R2**             | `authentication-mode local`                                                                                     | Sets the authentication method to local within the scheme.                                                           |
| **R2**             | `authorization-scheme <name>`                                                                                   | Creates an authorization scheme.                                                                                     |
| **R2**             | `authorization-mode local`                                                                                      | Sets the authorization method to local within the scheme.                                                            |
| **R2**             | `domain <name>`                                                                                                 | Creates a user domain.                                                                                               |
| **R2**             | `authentication-scheme <name>`                                                                                  | Applies an authentication scheme to the domain.                                                                      |
| **R2**             | `authorization-scheme <name>`                                                                                   | Applies an authorization scheme to the domain.                                                                       |
| **R2**             | `local-user <user>[@<domain>] password {cipher\|irreversible-cipher} <pass>`                                      | Creates a local user, optionally in a domain, with a password.                                                       |
| **R2**             | `local-user <user>[@<domain>] service-type telnet`                                                               | Allows the user to access via Telnet.                                                                                |
| **R2**             | `local-user <user>[@<domain>] privilege level <level>`                                                           | Sets the user's command privilege level.                                                                             |
| **R2**             | `telnet server enable`                                                                                          | Enables the Telnet server.                                                                                           |
| **R2**             | `user-interface vty 0 4`                                                                                         | Enters VTY line view.                                                                                                |
| **R2**             | `authentication-mode aaa`                                                                                        | Configures VTY lines to use AAA for authentication.                                                                  |
| **R1**             | `telnet <R2-ip-address>`                                                                                         | Initiates a Telnet connection (prompts for username@domain and password).                                             |
| **R2**             | `display users`                                                                                                 | Displays currently logged-in users.      |

</details>


### Verification/ configuration screenshots


---

## Lab 4.3: NAT Configuration

### Objectives

- Understanding NAT configuration, its purpose and types.
- Setting up NAT on Huawei devices.
- Validating and Troubleshooting NAT: Verifying translations and resolve issues.


### Topology
![Lab 4.3 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.3%20Lab%204.3%20%20NAT%20Configuration/topogy%20diagram.png)



https://github.com/user-attachments/assets/17d213cc-0f9c-475e-8ddf-fc3e2fe45edf



**Key commands**

<details>
  <summary><strong>Lab 4.3: NAT Configuration </strong></summary>

| **Device**         | **Command**                                                                                                     | **Description**                                                                                                  |
|--------------------|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| **R1, R2, R3**     | *IP Address & Routing Configuration to ensure basic connectivity and necessary static/default routes*           |                                                                                                                  |
| **R1, R3**         | *Telnet Server/User Configuration for testing (Refer to Lab 4.1/4.2)*                                             |                                                                                                                  |
| **R2**             | `nat address-group <index> <start-ip> <end-ip>`                                                                    | Defines a pool of public IP addresses for dynamic NAT.                                                            |
| **R2**             | `acl <number>`<br>`rule <id> permit source <private-net> <wildcard>`                                               | Creates an ACL to identify private source traffic needing translation.                                             |
| **R2**             | `interface <public-interface>`                                                                                    | Enters the view of the public-facing interface.                                                                   |
| **R2**             | `nat outbound <acl-num> address-group <index> [no-pat]`                                                             | Applies dynamic NAT using the address pool for traffic matching the ACL.                                             |
| **R2**             | `nat outbound <acl-num>`                                                                                           | Applies Easy IP NAT (uses interface IP) for traffic matching the ACL.                                               |
| **R2**             | `nat server protocol tcp global current-interface <pub-port> inside <priv-ip> <priv-port>`                           | Configures NAT Server (port forwarding) for a specific internal service (e.g., Telnet).                                 |
| **R1**             | `ping <public-ip>`<br>`telnet <public-ip>`                                                                        | Tests outbound NAT connectivity from the private network.                                                          |
| **R2**             | `display nat session all`                                                                                         | Displays the active NAT translation table.                                                                         |
| **R3**             | `telnet <R2-public-ip> <public-port>`                                                                              | Tests inbound NAT Server access from the public network.                                                           |

</details>


### Verification/ configuration screenshots

### Verification/ configuration screenshots
- <details>
  <summary>Verification Screenshots</summary>
  
  ![Display interfaces on R3](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.3%20Lab%204.3%20%20NAT%20Configuration/4.3-disp-int-br-R3.png)
  
  ![Source IP ping at R2 int G.0.0.2](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.3%20Lab%204.3%20%20NAT%20Configuration/DATA-CAPTURED-WITH-THE-SOURCE-IP-PING-AT-R2-INT-G.0.0.2.png)
  
  ![Easy IP Configuration](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.3%20Lab%204.3%20%20NAT%20Configuration/EASY-IP-CONFIGURATION.png)
  
  ![Just one source IP address Easy IP](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.3%20Lab%204.3%20%20NAT%20Configuration/JUST-ONE-SOURCE-IP-ADDRESS-EASY-IP.png)
  
  ![NAT Config on R2](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.3%20Lab%204.3%20%20NAT%20Configuration/NAT-CONFIG-ON-R2.png)
  
  ![NAT Server at Work](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.3%20Lab%204.3%20%20NAT%20Configuration/NAT-SERVER-AT-WORK.png)
  
  ![NAT Session Confirms Mapping](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.3%20Lab%204.3%20%20NAT%20Configuration/NAT-SESSION-CONFIRMS-MAPPING.png)
  
  ![Ping after NAT configuration successful](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.3%20Lab%204.3%20%20NAT%20Configuration/PING-AFTER-NAT-CONFIG%3DSUCCESSFULL.png)
  
  ![R3 cannot reach R1; telnet protects private IPs](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.3%20Lab%204.3%20%20NAT%20Configuration/R3-Cannot-reach-R1-telnetting-protects-the-private-ips.png)
  
  ![Ping R3 from R1 fails as NAT not yet configured on R2](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.3%20Lab%204.3%20%20NAT%20Configuration/ping-R3-FROM-R1-CANNOT-BE-SUCCESSFULL-BCS-NAT-IS-NOT-YET-CONFIG-ON-R2.png)
  
  ![Pinging R2 on R3](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.3%20Lab%204.3%20%20NAT%20Configuration/pinging-R2-ON-R3.png)
  
  ![Pinging gateway on R1](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.3%20Lab%204.3%20%20NAT%20Configuration/pinging-gateway-on-R1.png)
  
  ![Telnetting R1 from R3 after NAT server configured successfully](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.3%20Lab%204.3%20%20NAT%20Configuration/telnetting-R1-FROM-R3-after-configuring-NAT-server-now%3Dsuccessfull-from-the-public-network.png)
  
  ![Telnetting R3](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/4.3%20Lab%204.3%20%20NAT%20Configuration/telnetting-R3.png)
  
</details>
---

## Lab 5.1: FTP Configuration

### Objectives

- Understanding FTP concepts and their use.
- Configuring both FTP server and client.
-  Verifying connectivity and file exchange.

### Topology
![Lab 5.1 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/5.1%20Lab%205.1%20FTP%20Configuration/topo-FTP.png)



https://github.com/user-attachments/assets/9ad83413-da80-4603-87ad-1a4a29b6e910



**Key commands**
<details>
  <summary><strong>Lab 5.1: FTP Configuration (Section 5.1)</strong></summary>

| **Device**         | **Command**                                                                                                      | **Description**                                                                                       |
|--------------------|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| **R1, R2**         | *IP Address Configuration to ensure basic IP connectivity*                                                       |                                                                                                       |
| **R1, R2**         | `save <filename.cfg>`                                                                                            | Saves the current configuration to a file (for transfer).                                           |
| **R1, R2**         | `dir`                                                                                                            | Lists files in the local storage (flash:/).                                                          |
| **R2**             | `ftp server enable`                                                                                              | Enables the FTP server function.                                                                     |
| **R2**             | `aaa`                                                                                                            | Enters AAA view.                                                                                       |
| **R2**             | `local-user <user> password ...`                                                                                 | Creates a local user for FTP.                                                                          |
| **R2**             | `local-user <user> service-type ftp`                                                                             | Allows the user FTP access.                                                                            |
| **R2**             | `local-user <user> privilege level <level>`                                                                      | Sets user privilege (>=3 needed).                                                                      |
| **R2**             | `local-user <user> ftp-directory <directory>`                                                                    | Sets the user's home directory (e.g., `flash:/`).                                                      |
| **R1**             | `ftp <R2-ip-address>`                                                                                             | Connects to the FTP server from the client.                                                          |
| **R1**             | `ascii` / `binary`                                                                                               | Sets FTP transfer mode (within the FTP session).                                                     |
| **R1**             | `get <remote-file> [<local-file>]`                                                                               | Downloads a file from the server.                                                                      |
| **R1**             | `put <local-file> [<remote-file>]`                                                                               | Uploads a file to the server.                                                                          |
| **R1**             | `delete <remote-file>`                                                                                           | Deletes a file on the server.                                                                          |
| **R1**             | `bye` / `quit`                                                                                                   | Disconnects from the FTP server.                                                                       |

</details>



### Verification/ configuration screenshots

### Verification/ configuration screenshots
- <details>
  <summary>Verification Screenshots</summary>
  
  ![After exiting ftp a copy of test 2 is seen because it was downloaded](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/5.1%20Lab%205.1%20FTP%20Configuration/After%20exiting%20ftp%20a%20copy%20of%20test%202%20is%20seen%20because%20it%20was%20downloaded.png)
  
  ![Also on R1 NO TEST 2 CFG](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/5.1%20Lab%205.1%20FTP%20Configuration/Also%20on%20R1%20NO%20TEST%202%20CFG.png)
  
  ![DOWNLOADING](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/5.1%20Lab%205.1%20FTP%20Configuration/DOWNLOADING.png)
  
  ![MORE CMD DISPLAYS MORE](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/5.1%20Lab%205.1%20FTP%20Configuration/MORE-CMD-DISPLAYS-MORE.png)
  
  ![NO R2 AFTER DELETION](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/5.1%20Lab%205.1%20FTP%20Configuration/NO%20R2%20AFTER%20DELETION.png)
  
  ![NO TEST 2 ANYMORE ON R2](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/5.1%20Lab%205.1%20FTP%20Configuration/NO%20TEST%202%20ANYMORE%20ON%20R2.png)
  
  ![STPING INTO R2](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/5.1%20Lab%205.1%20FTP%20Configuration/STPING%20INTO%20R2.png)
  
  ![Before saving = no-test one file](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/5.1%20Lab%205.1%20FTP%20Configuration/b4-saving%3Dno-test-one-file.png)
  
  ![Now after saving](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/5.1%20Lab%205.1%20FTP%20Configuration/now-after-saving.png)
  
  ![stp-ing into R2](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/5.1%20Lab%205.1%20FTP%20Configuration/stp-ing%20into-R2.png)
  
</details>
---

## Lab 5.2: DHCP Configuration

### Objectives

- Understanding the operation of Dynamic Host Configuration Protocol (DHCP)
- Configuring DHCP services on Huawei devices
- Verifying DHCP lease assignments and testing client connectivity  


### Topology
![Lab 5.2 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/5.2%20Lab%205.2%20DHCP%20Configuration/topo%20DHCP.png)



https://github.com/user-attachments/assets/3ed0d22c-913e-4655-b407-48c86f796aa5



**Key commands**
<details>
  <summary><strong>Lab 5.2: DHCP Configuration</strong></summary>

| **Device**         | **Command**                                                                                                      | **Description**                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| **R2**             | *IP Address Configuration on server interfaces (typically static)*                                               |                                                                                                              |
| **R1, R2, R3**     | `dhcp enable`                                                                                                    | Enables DHCP service globally.                                                                               |
| **R2**             | `interface <server-interface-for-R1>`                                                                             | Enters interface view (for interface pool).                                                                  |
| **R2**             | `dhcp select interface`                                                                                          | Configures the interface to use an interface-specific pool.                                                  |
| **R2**             | `dhcp server dns-list <dns-ip>`                                                                                  | Sets DNS server for the interface pool.                                                                      |
| **R2**             | `ip pool <pool-name>`                                                                                            | Creates a global DHCP pool (e.g., for R3).                                                                     |
| **R2**             | `network <network-addr> mask <mask-len>`                                                                           | Defines the address range for the global pool.                                                               |
| **R2**             | `gateway-list <gateway-ip>`                                                                                      | Sets the default gateway for the global pool.                                                                |
| **R2**             | `dns-list <dns-ip>`                                                                                              | Sets DNS server for the global pool.                                                                         |
| **R2**             | `lease day <d> hour <h>`                                                                                         | Sets the lease duration for the global pool.                                                                 |
| **R2**             | `static-bind ip-address <ip> mac-address <mac>`                                                                   | Creates a static IP reservation within the global pool.                                                      |
| **R2**             | `interface <server-interface-for-R3>`                                                                             | Enters interface view (for the global pool assignment).                                                      |
| **R2**             | `dhcp select global`                                                                                             | Configures the interface to assign addresses from the matching global pool.                                  |
| **R1, R3**         | `interface <client-interface>`                                                                                   | Enters client interface view.                                                                                |
| **R1, R3**         | `ip address dhcp-alloc`                                                                                          | Configures the client interface to obtain an IP address via DHCP.                                              |
| **R1, R3**         | `display ip interface brief`<br>`display dns server`<br>`display ip routing-table`                           | Verifies IP, DNS, and route acquisition on the clients.                                                      |
| **R2**             | `display ip pool name <pool-name>`<br>`display ip pool interface <interface-name>`                               | Displays DHCP pool status and usage on the server.                                                           |

</details>


### Verification/ configuration screenshots

<details>
![disp ip pool name- globalpool](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/5.2%20Lab%205.2%20DHCP%20Configuration/disp%20ip%20pool%20name-%20globalpool.png)
  
</details>

---

## Lab 6: Creating a WLAN

### Objectives

- Learning key WLAN setup principles.
- Configuring WLAN on Huawei Devices.
- Testing and Troubleshooting Connectivity to ensure stable wireless access.

### Topology
![Lab 6.1 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/6.1%20Lab%206.1%20Creating%20a%20WLAN/topo.WLAN.png)




https://github.com/user-attachments/assets/175ae9d0-b4b2-4151-b619-39378161920f



**Key commands**
<details>
  <summary><strong>Lab 6: Creating a WLAN</strong></summary>

| **Device**         | **Command**                                                                                                      | **Description**                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| **S1, AC, S3, S4** | *VLAN & Trunk Configuration (ensure VLANs 100, 101 are created and trunks are set as in Lab 3.1)*                 |                                                                                                              |
| **S3, S4**         | `poe enable`                                                                                                     | Enables PoE on ports connected to APs (often default).                                                       |
| **S1, AC**         | `interface Vlanif <vlan-id>`<br>`ip address ...`                                                                | Configures Layer 3 interfaces for STA gateway (S1) and AP management (AC).                                    |
| **S1, AC**         | *DHCP Server Configuration (refer to Lab 5.2 for DHCP pool settings)*                                            |                                                                                                              |
| **AC**             | `wlan`                                                                                                           | Enters WLAN view.                                                                                            |
| **AC**             | `ap-group name <group-name>`                                                                                     | Creates an AP group.                                                                                         |
| **AC**             | `regulatory-domain-profile name default & country-code cn`                                                       | (Optional) Configures the country code if the default CN is acceptable.                                        |
| **AC**             | `regulatory-domain-profile default`                                                                              | Binds the regulatory profile to the AP group (within the AP-group view).                                       |
| **AC**             | `capwap source interface Vlanif <mgmt-vlan-id>`                                                                   | Sets the source interface for AC-AP communication.                                                           |
| **AC**             | `ap auth-mode mac-auth`                                                                                          | Sets the AP authentication mode (default is MAC).                                                            |
| **AC**             | `ap-id <id> ap-mac <mac>`                                                                                          | Adds/authenticates an AP by its MAC address.                                                                 |
| **AC**             | `ap-name <name>`                                                                                                 | Assigns a name to the AP (within the AP-id view).                                                              |
| **AC**             | `ap-group <group-name>`                                                                                          | Assigns the AP to a group (within the AP-id view).                                                             |
| **AC**             | `display ap all`                                                                                                 | Displays the status of configured APs.                                                                       |
| **AC**             | `security-profile name <name>`                                                                                   | Creates a security profile.                                                                                    |
| **AC**             | `security wpa-wpa2 psk pass-phrase <password> aes`                                                               | Configures WPA2-PSK security.                                                                                  |
| **AC**             | `ssid-profile name <name>`                                                                                       | Creates an SSID profile.                                                                                       |
| **AC**             | `ssid <ssid-name>`                                                                                               | Sets the WLAN network name (SSID).                                                                             |
| **AC**             | `vap-profile name <name>`                                                                                        | Creates a Virtual AP (VAP) profile.                                                                            |
| **AC**             | `forward-mode direct-forward`                                                                                    | Sets the data forwarding mode (typically default).                                                           |
| **AC**             | `service-vlan vlan-id <vlan-id>`                                                                                  | Maps the VAP to a service VLAN.                                                                                |
| **AC**             | `security-profile <name>`                                                                                        | Binds the security profile to the VAP profile.                                                                 |
| **AC**             | `ssid-profile <name>`                                                                                            | Binds the SSID profile to the VAP profile.                                                                     |
| **AC**             | `vap-profile <name> wlan <wlan-id> radio all`                                                                    | Binds the VAP profile to AP radios within the AP group, enabling the WLAN.                                      |
| **STA**            | *Connect to the WLAN using the device’s Wi-Fi settings with the specified SSID and password.*                      |                                                                                                              |
| **AC**             | `display station all`                                                                                            | Displays connected wireless clients (STAs).                                                                    |

</details>


### Verification/ configuration screenshots

### Verification/ configuration screenshots
- <details>
  <summary>Verification Screenshots for Lab 6: Creating a WLAN</summary>
  
  ![AP1 system information](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/6.1%20Lab%206.1%20Creating%20a%20WLAN/AP%201%20system%20info.png)
  
  ![AP2 system information](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/6.1%20Lab%206.1%20Creating%20a%20WLAN/AP2%20sys%20info.png)
  
  ![AP configuration brought online](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/6.1%20Lab%206.1%20Creating%20a%20WLAN/Configuring%20the%20APs%20to%20bring%20them%20online-AP2%20%20shown-AP1%20done%20the%20same%20way.png)
  
  ![VLAN configuration verified on S4](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/6.1%20Lab%206.1%20Creating%20a%20WLAN/Confirming%20VLAN%20is%20configured%20correctly%20on%20S4.png)
  
  ![Station connecting to Wi‑Fi](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/6.1%20Lab%206.1%20Creating%20a%20WLAN/Connecting%20a%20station%20to%20Wi-Fi.png)
  
  ![DHCP configuration on S1](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/6.1%20Lab%206.1%20Creating%20a%20WLAN/DHCP%20configured%20on%20%20S1.png)
  
  ![DHCP setup verified on AC](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/6.1%20Lab%206.1%20Creating%20a%20WLAN/DHCP%20configured%20on%20AC.png)
  
  ![Data capture at S3 confirms AP1 success](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/6.1%20Lab%206.1%20Creating%20a%20WLAN/Data%20Capture%20at%20%5BS3%5D%20g%200%200%201%20is%20successfull%20hence%20AP1%20is%20successful.png)
  
  ![Data capture at S4 confirms AP2 success](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/6.1%20Lab%206.1%20Creating%20a%20WLAN/Data%20Capture%20at%20%5BS4%5D%20g%200%200%201%20is%20successfull%20hence%20AP2%20is%20successful.png)
  
  ![Guide to retrieve AP MAC addresses](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/6.1%20Lab%206.1%20Creating%20a%20WLAN/How%20to%20get%20the%20MAC%20address%20for%20the%20APs.png)
  
  ![VLAN successfully created on AC](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/6.1%20Lab%206.1%20Creating%20a%20WLAN/VLAN%20created%20successfully%20on%20AC.png)
  
  ![VLAN configuration on S1](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/6.1%20Lab%206.1%20Creating%20a%20WLAN/VLAN%20on%20S1.png)
  
  ![AP statuses displayed successfully](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/6.1%20Lab%206.1%20Creating%20a%20WLAN/diisplaying%20AP1%20and%20AP2%20%3Dsuccessful.png)
  
  ![Station 1 connected to Wi‑Fi verified](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/6.1%20Lab%206.1%20Creating%20a%20WLAN/verified%20successfully-station%201%20connected%20to%20Wi-Fi.png)
  
  ![Pinging S1 (aggregation switch) successful](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/6.1%20Lab%206.1%20Creating%20a%20WLAN/verified-pinging%20S1(the%20aggregation%20switch)%3Dsuccessfull.png)
  
  ![Station 2 Wi‑Fi connection verified](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/6.1%20Lab%206.1%20Creating%20a%20WLAN/verified-station%202%20successfully%20connected.png)
  
  ![All stations successfully connected](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/6.1%20Lab%206.1%20Creating%20a%20WLAN/verified-the%20Stations%20successfullyconnected.png-)
  
</details>


---

## Lab 7: Creating an IPv6 Network

### Objectives
- Understanding IPv6 addressing and routing concepts.
- Configuring IPv6 addresses on devices.
- Testing connectivity and fixing issues.
  
### Topology
![Lab 7 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/7.%20Lab%207%20creating%20an%20IPv6%20Network/topo.creating%20an%20IPv6.png)




https://github.com/user-attachments/assets/1fb7509b-ea7e-44cb-833e-85e83a645461



**Key commands**
<details>
  <summary><strong>Lab 7: Creating an IPv6 Network</strong></summary>

| **Device**         | **Command**                                                                                                      | **Description**                                                                                                  |
|--------------------|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| **R1, R2, R3**     | `ipv6`                                                                                                           | Enables IPv6 forwarding globally.                                                                              |
| **R1, R2, R3**     | `interface <interface>`<br>`ipv6 enable`                                                                          | Enters interface view and enables IPv6 on it.                                                                    |
| **R1, R2, R3**     | `ipv6 address auto link-local`                                                                                   | Automatically generates a link-local (FE80::) address.                                                            |
| **R1, R2, R3**     | `display ipv6 interface <interface>`                                                                             | Displays IPv6 interface status and addresses.                                                                    |
| **R1**             | `ping ipv6 <link-local-addr> -i <interface>`                                                                       | Pings a link-local address, specifying the outbound interface.                                                   |
| **R2**             | `ipv6 address <ipv6-addr>/<prefix-len>`                                                                            | Manually configures a static global IPv6 address.                                                               |
| **R2, R3**         | `dhcp enable`                                                                                                    | Enables DHCP service globally (for DHCPv6).                                                                      |
| **R2**             | `dhcpv6 pool <pool-name>`                                                                                        | Creates a DHCPv6 pool.                                                                                           |
| **R2**             | `address prefix <prefix>/<len>`                                                                                  | Defines the address prefix for the DHCPv6 pool.                                                                  |
| **R2**             | `dns-server <ipv6-dns-addr>`                                                                                       | Sets the DNS server address for the DHCPv6 pool.                                                                 |
| **R2**             | `interface <server-interface> & dhcpv6 server <pool-name>`                                                         | Applies the DHCPv6 pool to the server interface.                                                                 |
| **R3**             | `interface <client-interface> & ipv6 address auto dhcp`                                                            | Configures the client interface for stateful DHCPv6 address acquisition.                                           |
| **R2**             | `interface <server-interface> & undo ipv6 nd ra halt`                                                              | Enables Router Advertisement (RA) sending on the server interface.                                               |
| **R2**             | `ipv6 nd autoconfig managed-address-flag`                                                                          | Sets the M flag in RAs (indicating stateful address configuration).                                               |
| **R2**             | `ipv6 nd autoconfig other-flag`                                                                                    | Sets the O flag in RAs (indicating stateful configuration for other parameters, e.g., DNS).                         |
| **R3**             | `interface <client-interface> & ipv6 address auto global default`                                                  | Configures the client to learn the default gateway via RAs.                                                      |
| **R1**             | `interface <client-interface> & ipv6 address auto global`                                                          | Configures the client interface for stateless address autoconfiguration (SLAAC).                                    |
| **R1**             | `ipv6 route-static <dest-prefix>/<len> <next-hop-ipv6>`                                                            | Configures a static IPv6 route.                                                                                  |
| **R1, R3**         | `display ipv6 routing-table`                                                                                       | Displays the IPv6 routing table.                                                                                  |
| **R1**             | `display ipv6 neighbors`                                                                                           | Displays the IPv6 neighbor cache.                                                                                 |

</details>


### Verification/ configuration screenshots

### Verification/ configuration screenshots

- <details>
  <summary>Verification Screenshots for Lab 7: Creating an IPv6 Network</summary>
  
  ![DHCPv6 server allocates gateway address to clients](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/7.%20Lab%207%20creating%20an%20IPv6%20Network/Configuring%20DHCPv6%20server%20to%20allocate%20the%20gateway%20address%20to%20clients..png)
  
  ![Static IPv6 addresses configured on R2](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/7.%20Lab%207%20creating%20an%20IPv6%20Network/Configuring%20static%20IPv6%20addresses%20on%20R2.%20.png)
  
  ![DHCPv6 client function configured](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/7.%20Lab%207%20creating%20an%20IPv6%20Network/Configuring%20the%20DHCPv6%20client%20function.%20.png)
  
  ![DHCPv6 server function configured](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/7.%20Lab%207%20creating%20an%20IPv6%20Network/Configuring%20the%20DHCPv6%20server%20function..png)
  
  ![IPv6 neighbor information displayed](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/7.%20Lab%207%20creating%20an%20IPv6%20Network/Displaying%20the%20IPv6%20neighbor%20information..png)
  
  ![Client address and DNS server information displayed](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/7.%20Lab%207%20creating%20an%20IPv6%20Network/Displaying%20the%20client%20address%20and%20DNS%20server%20information..png)
  
  ![Routes of R3 displayed](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/7.%20Lab%207%20creating%20an%20IPv6%20Network/Displaying%20the%20routes%20of%20R3.png)
  
  ![Enabling RA on R2 before R1 config](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/7.%20Lab%207%20creating%20an%20IPv6%20Network/Enabling%20RA%20on%20GigabitEthernet0.0.0%20of%20R2.%20just%20b4%20Configuring%20R1%20to%20obtain%20an%20IPv6%20address%20in%20stateless%20mode.png)
  
  ![First 3 steps on R1](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/7.%20Lab%207%20creating%20an%20IPv6%20Network/First%203%20steps%20on%20R1.png)
  
  ![First 3 steps on R2](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/7.%20Lab%207%20creating%20an%20IPv6%20Network/First%203%20steps%20on%20R2.png)
  
  ![First 3 steps on R3](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/7.%20Lab%207%20creating%20an%20IPv6%20Network/First%203%20steps%20on%20R3.png)
  
  ![IPv6 configuration on R1](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/7.%20Lab%207%20creating%20an%20IPv6%20Network/Ipv6%20on%20R1.png)
  
  ![Testing connectivity](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/7.%20Lab%207%20creating%20an%20IPv6%20Network/Testing%20connectivity..png)
  
  ![Pinging R2 from R3](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images%20and%20audios%20of%20the%20labs/7.%20Lab%207%20creating%20an%20IPv6%20Network/pinging%20R2%20from%20R3.png)
  
</details>

---

## Tips

- Always save your configurations and topo to avoid losing progress.
- Use the `display` command to verify configurations on Huawei devices.
- Use question mark incase you forget the full command.

---

## Resources
- [How to install eNSP](https://www.youtube.com/watch?v=gLEQx5JJYA0)
- [prerequisite](https://github.com/plochoidysis-ojwege/eNSP-labs/tree/main/Prerequisites/Real%20Notes)
- [Wireshark Documentation](https://www.wireshark.org/docs/) 
- [Huawei Talent Learning Portal](https://e.huawei.com/en/talent/learning/#/home)
- [Basic Networking Cheat Sheet (Community Maintained)](https://github.com/trimstray/the-book-of-secret-knowledge)

---

- Any contributions and suggestions are welcome.


---
