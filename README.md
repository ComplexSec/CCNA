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

## Application Layer

The Application Layer determines whether adequate resources exist for communication. It manages communications between apps and then directs data to the correct program

This layer is also responsible for converting data into a format that is usable by apps and directing data to the proper app window. If multiple instances exist, the layer will ensure that data is delivered to the corect app instance

Protocols used by the Application Layer include:

Protocol | Description
------------ | -------------
HyperText Transfer Protocol (HTTP) | Transfer web pages over the internet
File Transfer Protocol (FTP) | Transfer files over a network
Trivial File Transfer Protocol (TFTP) | Transfer files over a network
Dynamic Host Configuration Protocol (DHCP) | Assign IP addressing information to clients
Domain Name System (DNS) | Translate host names to IPs
Simple Mail Transfer Protocol (SMTP) | Send email messages
Post Office Protocol (POP3) | Receive email messages
Telnet | Create terminal connection to remote devices
Secure Shell (SSH) | Create a secure remote terminal connection to networked device

## Presentation Layer

The Presentation Layer is responsible for converting and representing the payload in different formats - eg. data-based, character-based, image-based, audio-based, video-based and more

Compression and encryption are often handled by this layer

Some formats used by the Presentation Layer include:

* Graphics Interchange Format (GIF)
* Joint Photographic Experts Group (JPEG)
* Motion Picture Experts Group (MPEG)
* QuickTime

## Session Layer

The Session Layer is responsible for establishing, maintaining and terminating data communications between apps or devices

Sessions are made up of requests and responses. The Session Layer identifies the data as belonging to a particular session and ensures that the requests and responses are sent back and forth between the two parties

Protocols that operate at the Session Layer include:

Protocol | Description
------------ | -------------
Password Authentication Protocol (PAP) | Authentication protocol that uses a simple user and password pair
Remote Procedure Call (RPC) | Allows clients to initiate a process that is executed on a remote server

## Transport Layer

The Transport Layer is responsible for error-free delivery of information between devices. It is also repsonsible for flow control and sequencing. The information traversing the Transport Layer is called a __segment__

Protocols that operate at the Transport Layer include:

Protocol | Description
------------ | -------------
User Datagram Protocol (UDP) | Provides connectionless, unreliable data transfer between networked computers
Transmission Control Protocol (TCP) | Provides connection-oriented, reliable data transfer between networked computers

## Network Layer

The Network Layer is responsible for logical addressing and routing on a network. Logical addressing methods include those defined by IPv4 and IPv6. The information traversing the Network layer is called a __packet__

Examples of protocols that are used at this layer include:

Protocol | Description
------------ | -------------
IPv4 | Used to uniquely identify devices on a network
IPv6 | Used to uniquely identify devices on a network
Open Shortest Path First | Link State-Routing Protocol
Enhanced Interior Gateway Routing Protocol (EIGRP) | Cisco created hybrid routing protocol

## Data Link Layer

The Data Link layer defines how devices communicate over a network. It is responsible for managing physical addressing and switching on a network. Physical (MAC) addresses are handled here. Information traversing the Data Link layer is called a __frame__

Data Link layer devices include switches and bridges

Switching is handled at the Data Link layer because switches use physical addresses to forward packets to the correct port

Some portions of the 802.11 wireless standard function at the Data Link layer and some portions at the Physical Layer

Protocols that operate at the Data Link layer include:

* Ethernet
* Frame Relay
* Point-to-Point Protocol (PPP)
* Cisco Discovery Protocol (CDP)

## Physical Layer

The Physical Layer defines how bits are passed over a medium. They can be passed electronically, mechanically, optically or by radio signals

Media can include:

* Coaxial cable
* Twisted-pair copper cable
* Fiber-optic cable

Physical layer includes the connectors used to connect the cables to the devices that operate at this layer. This layer passes bits between the Data Link layer and physical devices on a network

Examples of devices that operate at this layer are:

* Network Interface Cards (NIC)
* Hubs
* Repeaters

The devices that operate at the Physical Layer receive and forward bits to other devices without making any path determination about the bits. The devices simply forward the bits to the next hop in the network

Protocols that operate at the Physical Layer include:

* Ethernet
* Universal Serial Bus (USB)
* Asynchronous Digital Subscriber Line (ADSL)