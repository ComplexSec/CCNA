# CCNA 200-301 Resources

## Refresh your networking and CCNA knowledge

<details><summary>Module 1 - Networking Fundamentals</summary>
<p>	

# Table of Contents <a name="INDEX"></a>

1. [The OSI Model](#OSI)
2. [Network Devices](#NET)
3. [Cisco Three-Tier Network Design Model](#THREE)
4. [Cisco Two-Tier Network Design Model](#TWO)
5. [Spine-Leaf Topology](#SPINE)
6. [WAN Topologies](#WAN)
7. [SOHO Topologies](#SOHO)
8. [On-Premises and Cloud Deployments](#ONPREM)
9. [Interfaces and Cabling](#INTS)
10. [Troubleshooting Interfaces and Cabling](#TROUBLE)
11. [Review Question and Answers](#REV1)

![](/images/network1.jpg)

## The OSI Model <a name="OSI"></a> ([Back to Index](#INDEX))

## Quick Summary

<ins>Layer 7 - The Application Layer</ins>

* Delivers appropriately formatted payloads to the correct instance of an application
* Includes protocols such as HTTP, SMTP and DNS
* Information is called __data__

<ins>Layer 6 - Presentation Layer</ins>

* Converts data into different formats
* Compression and encryption handled here
* Includes formats such as MP3, JPEG and GIF
* Information is called __data__

<ins>Layer 5 - Session Layer</ins>

* Establishes and maintains communications
* Includes protocols such as PAP and RPC
* Uses requests and responses
* Information is called __data__

<ins>Layer 4 - Transport Layer</ins>

* Applies flow control and error detection and sequencing
* Includes protocols such as TCP and UDP
* Information is called __segments__

<ins>Layer 3 - Network Layer</ins>

* Responsible for logical addressing and routing
* Includes devices such as routers and Layer 3 switches
* Includes protocols such as IPv4, IPv6, IPX, OSPF and EIGRP
* Information is called __packets__

<ins>Layer 2 - Data Link Layer</ins>

* Defines how devices communicate over a network
* Responsible for managing physical addressing and switching (MAC addresses)
* Includes devices such as switches and bridges
* Includes protocols such as Ethernet, Frame Relay, Token Ring, PPP and CDP
* Information is called __frames__

<ins>Layer 1 - Physical Layer</ins>

* Defines how bits are passed over a medium
* Can be passed electronically, mechanically, optically or by radio signals
* Media includes coaxial cable, twisted-pair copper cable and fiber-optic cable
* Includes the connectors used to connect the cables to the devices
* Devices include NICs, hubs and repeaters
* Forward bits to the next hop in the network
* Inlcudes protocols such as Ethernet, USB and ADSL
* Information is called __bits__