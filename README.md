# Huawei eNSP Lab Exercises

This repository contains basic configurations on Huawei eNSP. Each configuration includes objectives, topology images, screenshots of configurations, and verification steps.As I learn basic networking concepts, I'm updating this repository with each lab I complete daily to build my understanding and practical skills. This documentation reflects my ongoing learning journey.

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

## How to Use This README


1. **Navigate the Table of Contents**:
   - Use the Table of Contents at the top to quickly jump to the lab you want to work on.

2. **Understand the Objectives**:
   - Each lab starts with a list of objectives to help you understand what you will learn and accomplish.

3. **Review the Topology**:
   - Refer to the topology diagrams to understand the network setup for each lab.

4. **Follow the Configuration Steps**:
   - Use the configuration screenshots and commands provided to set up the lab environment.

5. **Verify Your Work**:
   - Check the verification section for each lab to ensure your configuration is correct. This includes ping tests, routing tables, and other outputs.

6. **Add Your Own Notes**:
   - Feel free to add screenshots, notes, or additional details to the README as you complete the labs.

7. **Use the Resources**:
   - Refer to the resources section at the end of the README for additional documentation and tools.

---

By following these steps, you can effectively complete the lab exercises and gain hands-on experience with Huawei eNSP.
---

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
- screenshots of configuration outputs and command tables are to be added here

### Verification
- screenshots of ping results, routing tables, and any relevant packet captures.

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
- Add screenshots of OSPF configuration and command outputs here.

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
- Add screenshots of VLAN configurations and Ethernet interface settings here.

### Verification
- Include screenshots of VLAN membership, ping tests, and any Wireshark captures.

---

## Lab 3.2: Spanning Tree Configuration

### Objectives

- Understand the operation of the Spanning Tree Protocol (STP)
- Configure STP parameters on network switches
- Verify and troubleshoot STP settings, including identifying root bridges and port roles

### Topology
![Lab 3.2 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images/3.2%20Lab%203.2%20Spanning%20Tree%20Configuration/topo.%20spanning%20tree%20configuration.png)

### Configuration Screenshots
- Add screenshots of spanning tree configurations and port roles here.

### Verification
- Include screenshots showing STP status and traceroute or ping results.

---
## Lab 3.3: Ethernet Link Aggregation

### Objectives

● Learn how to manually configure link aggregation
● Learn how to configure link aggregation in static LACP mode
● Learn how to determine active links in static LACP mode
● Learn how to configure some static LACP features
  
  ### Topology
![Lab 3.3 Topology](https://github.com/plochoidysis-ojwege/eNSP-labs/blob/main/Images/3.3%20Lab%203.3%20Ethernet%20Link%20Aggregation/topo.ethernet%20link%20aggregation.png)

### Configuration Screenshots
-  screenshots of configuration and command outputs here.
### Verification
- screenshots of ping results etc

---

## Lab 4.0:  Inter-VLAN Communication

### Objectives

- Learn how to use Dot1q termination subinterfaces to implement inter-VLAN 
communication
- Learn how to use VLANIF interfaces to implement inter-VLAN communication
- Understand the forwarding process of inter-VLAN communication

### Topology
![Lab 4.0 Topology](path/to/lab4.1-topology.png)


### Configuration Screenshots
- Add screenshots of ACL configuration and command outputs here.

### Verification
- Include screenshots showing ACL rule listings and ping or traceroute test results.



---
 ## Lab 4.1: ACL Configuration

### Objectives

- Understand Access Control List (ACL) concepts and their role in network security
- Configure ACL rules on Huawei devices
- Verify ACL functionality using connectivity tests  


### Topology
![Lab 4.1 Topology](path/to/lab4.1-topology.png)

### Configuration Screenshots
- Add screenshots of ACL configuration and command outputs here.

### Verification
- Include screenshots showing ACL rule listings and ping or traceroute test results.

---

## Lab 4.2: Local AAA Configuration

### Objectives

- Understand the fundamentals of AAA (Authentication, Authorization, and Accounting)
- Configure local AAA settings on Huawei devices
- Verify AAA user authentication and test network access  

### Topology
![Lab 4.2 Topology](path/to/lab4.2-topology.png)

### Configuration Screenshots
- Add screenshots of AAA configuration details and user authentication setups.

### Verification
- Include screenshots showing successful AAA authentication tests and relevant command outputs.

---

## Lab 4.3: NAT Configuration

### Objectives

- Understand the purpose and types of Network Address Translation (NAT)
- Configure NAT settings on Huawei devices
- Verify NAT translations and troubleshoot related issues  
:contentReference[oaicite:4]{index=4}

### Topology
![Lab 4.3 Topology](path/to/lab4.3-topology.png)

### Configuration Screenshots
- Add screenshots of NAT configuration commands and NAT translation outputs.

### Verification
- Include screenshots showing NAT translation tables, ping tests, and any packet captures.

---

## Lab 5.1: FTP Configuration

### Objectives

- Understand the fundamentals of File Transfer Protocol (FTP)
- Configure FTP servers and clients on Huawei devices
- Verify FTP connectivity and perform file transfers  
:contentReference[oaicite:5]{index=5}

### Topology
![Lab 5.1 Topology](path/to/lab5.1-topology.png)

### Configuration Screenshots
- Add screenshots of FTP configuration and command outputs here.

### Verification
- Include screenshots showing successful FTP connections and file transfer logs.

---

## Lab 5.2: DHCP Configuration

### Objectives

- Understand the operation of Dynamic Host Configuration Protocol (DHCP)
- Configure DHCP services on Huawei devices
- Verify DHCP lease assignments and test client connectivity  
:contentReference[oaicite:6]{index=6}

### Topology
![Lab 5.2 Topology](path/to/lab5.2-topology.png)

### Configuration Screenshots
- Add screenshots of DHCP server configuration and DHCP lease outputs.

### Verification
- Include screenshots showing DHCP bindings, ping tests, and routing verification.

---

## Lab 6: Creating a WLAN

### Objectives

- Understand the principles of WLAN configuration
- Configure WLAN parameters and settings on Huawei devices
- Verify wireless connectivity and troubleshoot WLAN issues  
:contentReference[oaicite:7]{index=7}

### Topology
![Lab 6 Topology](path/to/lab6-topology.png)

### Configuration Screenshots
- Add screenshots of WLAN configuration interfaces and settings.

### Verification
- Include screenshots showing WLAN connectivity tests and wireless signal verification.

---

## Lab 7: Creating an IPv6 Network

### Objectives

- Understand IPv6 addressing and routing concepts
- Configure IPv6 addresses on network interfaces
- Verify IPv6 connectivity and troubleshoot IPv6-related issues  
:contentReference[oaicite:8]{index=8}

### Topology
![Lab 7 Topology](path/to/lab7-topology.png)

### Configuration Screenshots
- Add screenshots of IPv6 configuration commands and outputs here.

### Verification
- Include screenshots showing IPv6 neighbor discovery, ping results, and any Wireshark captures.

---

## Tips for Writing a Good README
1. **Keep it organized:** Use clear headings and subheadings to structure your content.
2. **Use visuals:** Include images and screenshots to make the instructions easier to follow.
3. **Be concise:** Write clear and concise descriptions for each section.
4. **Use Markdown formatting:** Leverage Markdown syntax to make your README visually appealing.

---

## Resources
- [Markdown Guide](https://www.markdownguide.org/)  
- [Wireshark Documentation](https://www.wireshark.org/docs/)  
- [Huawei eNSP Documentation](https://support.huawei.com/enterprise/en/ensp)

---

- Any contribution is welcome.
