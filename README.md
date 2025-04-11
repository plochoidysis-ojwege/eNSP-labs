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
![Lab 4.1 Topology](path/to/lab4.1-topology.png)

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
![Lab 4.2 Topology](path/to/lab4.2-topology.png)

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
![Lab 4.3 Topology](path/to/lab4.3-topology.png)

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
