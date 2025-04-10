# Huawei eNSP Lab Exercises

This repository contains my hands-on lab exercises for learning Huawei networking technologies using the eNSP emulator.Each lab focuses on fundamental networking concepts and includes objectives, topology diagrams,configuration steps (with screenshots planned), and verification procedures. This is a record of my ongoing journey to build practical networking skills.

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

- **Table of Contents**: Click any lab in the list above to jump right to that section.
- **Objectives**: Each lab starts with a brief list of what I aimed to learn.
- **Topology Diagrams**: Get a quick visual overview of the network setup for each exercise.
- **Configuration Steps**: Follow the commands and (soon) add screenshots that show how each lab is set up.
- **Verification**: Check how I confirmed the lab worked—through tests like ping results and routing tables.
- **Personal Notes**: I've added my own notes and observations as I progressed.
- **Resources**: Find extra documentation and guides in the Resources section at the end.

---

This layout reflects my ongoing journey with Huawei eNSP. Enjoy exploring and learning along with me!
## Lab 1: IPv4 Addressing and Routing

### Objectives

- Learn how to configure an IPv4 address on an interface
- Understand the functions and meanings of loopback interfaces
- Understand how direct routes are generated
- Learn how to configure static routes and understand the conditions for the static routes to take effect
- Learn how to test the connectivity of the network layer by using the ping tool
- Learn how to configure static routes and understand their application scenarios  

### Topology
![Lab 1 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images/1.%20Lab%201%20IPv4%20Addressing%20and%20Routing/TOPO.IPV4%20ADDRESSING%20AND%20ROUTING%20CONFIG.png)

### Configuration Screenshots
- screenshots of configuration outputs and command tables COMING SOON

### Verification
- screenshots of ping results, routing tables, and any relevant packet captures.COMING SOON.

---

## Lab 2: OSPF Routing

### Objectives

- Learn the basic commands of OSPF
- Learn how to check the OSPF running status
- Learn how to control OSPF route selection using costs
- Understand the advertisement of default routes in OSPF
- Learn how to configure OSPF authentication  
### Topology
![Lab 2 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images/2.%20Lab%202%20OSPF%20Routing/topo.ospf%20routing.png)

### Configuration Screenshots
-  screenshots of OSPF configuration and command outputs COMING SOON.

### Verification
- Include screenshots showing OSPF neighbor relationships, routing tables, and traceroute outputs.

---

## Lab 3.1: Ethernet Basics and VLAN Configuration

### Objectives

- Understand the fundamentals of Ethernet switching
- Configure basic Ethernet settings and VLANs on network devices
- Verify VLAN membership and connectivity between devices



### Topology
![Lab 3.1 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images/3.1%20Lab%203.1%20Ethernet%20Basics%20and%20VLAN%20Configuration/topo.ethernet%20Basics%20and%20Vlan%20Config.png)

### Configuration Screenshots
- screenshots of VLAN configurations and Ethernet interface settings COMING SOON

### Verification
-  screenshots of VLAN membership, ping tests, and any Wireshark captures.

---

## Lab 3.2: Spanning Tree Configuration

### Objectives

- Understand the operation of the Spanning Tree Protocol (STP)
- Configure STP parameters on network switches
- Verify and troubleshoot STP settings, including identifying root bridges and port roles

### Topology
![Lab 3.2 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images/3.2%20Lab%203.2%20Spanning%20Tree%20Configuration/topo.%20spanning%20tree%20configuration.png)

### Configuration Screenshots
-  screenshots of spanning tree configurations and port roles COMING SOON.

### Verification
- Include screenshots showing STP status and traceroute or ping results.

---
## Lab 3.3: Ethernet Link Aggregation

### Objectives

- Learn how to manually configure link aggregation
- Learn how to configure link aggregation in static LACP mode
- Learn how to determine active links in static LACP mode
- Learn how to configure some static LACP features
  
  ### Topology
![Lab 3.3 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images/3.3%20Lab%203.3%20Ethernet%20Link%20Aggregation/topo.ethernet%20link%20aggregation.png)

### Configuration Screenshots
-  screenshots of configuration and command outputs here.
### Verification
- screenshots of ping results etc. COMING SOON

---
## Lab 4.0: Inter-VLAN Communication

### Objectives

- Learn how to use Dot1q termination subinterfaces to implement inter-VLAN 
communication
- Learn how to use VLANIF interfaces to implement inter-VLAN communication
- Understand the forwarding process of inter-VLAN communication

### Topology
![Lab 4.0 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images/4.0%20Lab%204%20Inter-VLAN%20Communication/topo.Inter-VLAN-Communication.png)


### Configuration Screenshots
- Add screenshots of ACL configuration and command outputs here.

### Verification
-  screenshots COMING SOON


---
 ## Lab 4.1: ACL Configuration

### Objectives

- Understand Access Control List (ACL) concepts and their role in network security
- Configure ACL rules on Huawei devices
- Verify ACL functionality using connectivity tests  


### Topology
![Lab 4.1 Topology](path/to/lab4.1-topology.png)

### Configuration Screenshots
- COMING SOON screenshots of ACL configuration and command outputs here.

### Verification
- COMING SOON screenshots showing ACL rule listings and ping or traceroute test results.

---

## Lab 4.2: Local AAA Configuration

### Objectives

- Understand the fundamentals of AAA (Authentication, Authorization, and Accounting)
- Configure local AAA settings on Huawei devices
- Verify AAA user authentication and test network access  

### Topology
![Lab 4.2 Topology](path/to/lab4.2-topology.png)

### Configuration Screenshots
- COMING SOON screenshots of AAA configuration details and user authentication setups.

### Verification
-  screenshots showing successful AAA authentication tests and relevant command outputs.COMING SOON

---

## Lab 4.3: NAT Configuration

### Objectives

- Understand the purpose and types of Network Address Translation (NAT)
- Configure NAT settings on Huawei devices
- Verify NAT translations and troubleshoot related issues  


### Topology
![Lab 4.3 Topology](path/to/lab4.3-topology.png)

### Configuration Screenshots
- Add screenshots of NAT configuration commands and NAT translation outputs.

### Verification
- Include screenshots showing NAT translation tables, ping tests, and any packet captures.COMING SOON.

---

## Lab 5.1: FTP Configuration

### Objectives

- Understand the fundamentals of File Transfer Protocol (FTP)
- Configure FTP servers and clients on Huawei devices
- Verify FTP connectivity and perform file transfers  


### Topology
![Lab 5.1 Topology](path/to/lab5.1-topology.png)

### Configuration Screenshots
-  screenshots of FTP configuration and command outputs here.COMING SOON

### Verification
- Coming soon screenshots showing successful FTP connections and file transfer logs.

---

## Lab 5.2: DHCP Configuration

### Objectives

- Understand the operation of Dynamic Host Configuration Protocol (DHCP)
- Configure DHCP services on Huawei devices
- Verify DHCP lease assignments and test client connectivity  


### Topology
![Lab 5.2 Topology](path/to/lab5.2-topology.png)

### Configuration Screenshots
- screenshots of DHCP server configuration and DHCP lease outputs. Soon.

### Verification
- Include screenshots showing DHCP bindings, ping tests, and routing verification.coming soon

---

## Lab 6: Creating a WLAN

### Objectives

- Understand the principles of WLAN configuration
- Configure WLAN parameters and settings on Huawei devices
- Verify wireless connectivity and troubleshoot WLAN issues  


### Topology
![Lab 6 Topology](path/to/lab6-topology.png)

### Configuration Screenshots
- screenshots of WLAN configuration interfaces and settings,coming soon

### Verification
- Include screenshots showing WLAN connectivity tests and wireless signal verification.COMING SOON

---

## Lab 7: Creating an IPv6 Network

### Objectives

- Understand IPv6 addressing and routing concepts
- Configure IPv6 addresses on network interfaces
- Verify IPv6 connectivity and troubleshoot IPv6-related issues  

### Topology
![Lab 7 Topology](path/to/lab7-topology.png)

### Configuration Screenshots
- Add screenshots of IPv6 configuration commands and outputs here.Coming soon

### Verification
-  screenshots showing IPv6 neighbor discovery, ping results, and any Wireshark captures.Coming soon.

---

## Tips

- Always save your configurations to avoid losing progress.
- Use the `display` command to verify configurations on Huawei devices.
- Refer to the official Huawei eNSP documentation for troubleshooting.

---

## Resources
- [Infosyte: How to Install Huawei eNSP Network Simulator](https://infosyte.com/how-to-install-huawei-ensp-network-simulator/)
- [Wireshark Documentation](https://www.wireshark.org/docs/) 
 - [Huawei Talent Learning Portal](https://e.huawei.com/en/talent/learning/#/home) - Explore official Huawei learning and training resources.
-  [Huawei eNSP Pro Full Guide](https://forum.huawei.com/enterprise/intl/en/thread/Huawei-eNSP-Pro-Full-Guide-Part1/856124796711411712?blogId=856124796711411712) - A detailed guide from the Huawei forum.

---

- Any contributions and suggestions are welcome.
