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

## Network Devices <a name="NET"></a> ([Back to Index](#INDEX))

## Hubs

Hubs are multiport physical repeaters that are used to connect end-user workstations. An incoming frame is rebroadcast out __all other ports__ except the port it came in on. They are inexpensive devices that do not create separate broadcast and collision domains

Hubs do not make any forwarding decisions based on MAC address or IP address

A collision domain is a network segment where collisions can occur when frames are sent among the devices on that network segment

If 4 computers are connected to a hub, all 4 share the same bandwidth. Each device can only use a portion of the total bandwidth. Collisions can occur when frames are sent simultaneously by multiple computers attached to the hub

Ethernet devices rely on __Carrier Sense Multiple Access with Collision Detection (CSMA/CD)__ to mitigate collisions

With CSMA/CD a transmitting device listens on the network segment before it attempts to send data. If no transmissions are there, it sends data and listens to determine whether a collision occured. If a collision is detected, each transmitting device waits a random period of time before attempting to retransmit

Collision detection can function only when the devices do not attempt to transmit and receive at the same time.

Hubs are restricted to half-duplex mode meaning they cannot transmit and receive at the same time

## Bridges

Bridges use the MAC address of data recipients to deliver frames. Bridges maintain a forwarding database in which the MAC addresses of the attached hosts are stored.

When a packet is received by a bridge, the sender's MAC address is recorded in the forwarding database. If the address is also stored in the forwarding database, the packet will be sent directly to the recipient. If the address is not in the database, the packet is broadcast out all ports excluding the port it arrived on

Each host receives the packet and uses the MAC address to determine if it is for them

When the intended recipient responds to the packet, the bridge sends the reply directly to the original sender.

Bridges can be used to increase the number of collision domains - each port on a bridge creates a separate collision domain. They do not create separate broadcast domains - all devices connected to a bridge will reside in the same broadcast domain

## Switches

Switches can be used to provide network connectivity to endpoint devices. They can operate at Layer 2 or Layer 3. Layer 2 switches function similiarly to bridges. Layer 3 switches add routing functionality

Switches use information in the __data packet__ headers to forward packets to the correct ports. This results in fewer collisions, improved traffic flow and faster performance

Switches break a large network into smaller networks. Switches perform __microsegmentation__ of collision domains - this creates a separate dedicated network segment for each port

Layer 2 switches use physical addresses known as MAC addresses. They are used to carry out their primary responsibility of switching frames. Switches store known MAC addresses in a special area of memory known as the __Content Addressable Memory (CAM)__ table. The CAM table associates MAC addresses with the physical interface through which those addresses can be reached

When a switch receives a frame, it adds the source MAC to the CAM table. The switch then checks the CAM table to see if the destination MAC address is listed. If it is, it directs the frame to the appropriate port. If not, it broadcasts the frame out all ports except the port it arrived on

If 4 computers are connected to a switch, each computer will reside in its own collision domain. All 4 computers can send data to the switch simultaneously

Because switches forward broadcasts, all devices connected to a Layer 2 switch will reside within a single broadcast domain. Layer 3 switches can use VLANs to separate the broadcast domains

## Routers

Routers are used to forward packets between computer networks. Routers create separate broadcast domains. Devices connected to a router reside in a separate broadcast domain. A broadcast that is sent on one network segment attached to the router will not be forwarded to any other network

Layer 3 switches share many features and capabilities with routers

Routers make path decisions based on logical addresses such as IP addresses. Routers store IP address information in a routing table. The routing table is stored in a special section of memory known as the __Ternary CAM (TCAM) table__. The TCAM table is used to provide wire speed access to data for queries. The TCAM table can provide a non-exact match for a particular query

Routers can implement multiple TCAM tables - commonly used to facilitate the implementation of access control list (ACL) rules, Quality of Service (QoS) rules, etc...

When a router receives a packet, it forwards the packet to the destination network based on information in a routing table. 

If a router receives a packet that is destined for a remote network that is not listed in the table and neither a static default router nor a gateway of last resort has been configured, the packet is dropped and an ICMP Unreachable Error is sent to the interface it was received on

## Servers

Many different types of network servers and various functions associated with them. Servers can either be a specific piece of hardware or a software program - typically set up to provide specific services to a group of other computers on a network

Servers provide a centralized way to control, manage and distribute a variety of technologies - simple data files, applications, security policies, network addresses

Some examples of services include:

Server | Description
------------ | -------------
File Servers | Can configure a file server to allow users to access shared files/folders, used as a central storage location
Domain Servers | Manages resources that are available on the domain, used to configure access and security policies for users
Print Servers | Provides access to a limited number of printers to many computer users rather than a local printer for each PC
DHCP Servers | Automatically provide IP addresses to client computers, clients can connect to the server and automatically get an IP
Web Servers | Allows customers to access your company website, typically contain content that is viewable in a browser
Proxy Servers | Intermediary between browser and internet. When computers connect to the internet, the computer first connects to the proxy server. The proxy performs one of the following actions - forwards traffic, blocks traffic, returns cached webpage

## Endpoints

Endpoints are also known as hosts. Individual computing devices that access the services available on the network - could be a PC, PDA, laptop, thin client or terminal

Endpoints act as the user interface at which the user can access the data or other devices available on a network

## Next-Generation Firewalls and IPS Devices

Firewalls are devices that filter packets inbound from untrusted networks. Typically a firewall filters packets without analysis

Cisco Adaptive Security Appliances (ASAs) are next-generation, multifunction appliances that can provide firewall, virtual private network (VPN), intrusion prevention, and content security services

An IPS is a device that detects and can automatically mitigate network intrusion attempts - can determine whether a given packet might be malicious and can take various actions

## WAPs

WAPs are devices that enable wireless clients to connect to a wireless LAN (WLAN) - using radio frequency (RF) communication

WAPs are available in single-band or dual-band form. WAPs that are designed for modern versions of the IEEE 802.11 standard are typically dual-band WAPs

One band operates at 2.4GHz frequency while the other operates at 5GHz frequency

## Controllers

Controllers manage other network devices - including Cisco DNA Controller and wireless LAN controllers (WLCs)

Cisco DNA is a software-centric network architecture that uses a combination of Application Programming Interfaces (APIs) and a graphical user interface (GUI) to simplify network operations

Cisco DNA Controller is the central component of a Cisco Software-Defined Access (SDA) network - Cisco SDA is a Cisco developed means of building local area networks (LANs) by using policies and automation

Whereas autonomous WLANs required that each AP handle both traffic and management functions, Cisco Unified Wireless Networks use WLCs to centralize security configurations among APs and to provide mobility services at both Layer 2 and Layer 3

WLCs provide user authentication, RF management, security and policy enforcement and QoS to lightweight APs (LAPs). A LAP requires a WLC to function

If WLC becomes unavailable, the LAP will reboot and drop all client association until the WLC becomes available or until another WLC is found on the network

A LAP communicates over Lightweight Access Point Protocol (LWAPP) to establish two tunnels to its associated WLC - one tunnel for data and one tunnel for control traffic. Traffic sent through data tunnel is not encrypted. Traffic sent through control tunnel is encrypted

## Cisco Three-Tier Network Design Model  <a name="THREE"></a> ([Back to Index](#INDEX))

## The Core Layer

The Core Layer provides the fastest switching path in the network. It is commonly referred to as the network backbone and is primarily associated with low latency and high reliability

## The Distribution Layer

The Distribution Layer provides router filtering and interVLAN routing. Management ACLs and IPS filtering is typically implemented at distribution layer. The Distribution layer also serves as an aggregration point for access layer network links

Because the Distribution layer is the intermediary between the Access layer and Core layer, it is an ideal place to enforce security policies and perform tasks that involved packet manipulation. Summarization and next-hope redundancy are performed at this layer

## The Access Layer

The Access layer provides Network Admission Control (NAC) - NAC is a Cisco feature that prevents hosts from accessing the network if they do not comply with organizational requirements

NAC Profiler automates NAC by automatically discovering and inventorying devices attached to the LAN

This layer serves as a media termination point for servers and endpoints. The Access layer is an ideal place to perform user authentication and port security

The Access layer typically consists of OSI Layer 2 switches only - when packets must be routed, it is first sent to a L3 device in the distribution layer. Some designs employ L3 switches in the access layer which moves the demarcation between L2 and L3 switching to the access layer

## Cisco Two-Tier Network Design Model <a name="TWO"></a> ([Back to Index](#INDEX))

This model is sometimes referred to as the Collapsed-Core Network Design Model. The functionality of the core layer is collapsed into the distribution layer. The functionality of the core layer is provided by the distribution layer and a distinct core layer does not exist

The Distribution layer infrastructure must be sufficient to meet the design requirements

## Spine-Leaf Topology <a name="SPINE"></a> ([Back to Index](#INDEX))

Spine-Leaf topologies are generally seen in data centers more than organizations. Spine-Leaf topologies are two-tier, partial-mesh network architectures

Every lower-tier leaf switch connects to every top-tier spine switch. Leafs and spines are not connected to one another

Spine switches connect to the network backbone. If link oversubscription occurs, a new spine switch can be added and connections to every leaf switch can be established. Leaf switches connect to nodes such as servers. When port capacity becomes a problem with addition of new servers, a new leaf can be added and connections to every spine switch can be established

Because spines have connections to every leaf, the scalability of the fabric is limited by the number of ports on the spine node and not by the number of ports on the leaf node

Redundant connections between a spine and leaf pair are unnecessary because the nature of the topology ensures that each leaf has multiple connections to the network fabric - each spine requires only a single connection to each leaf node

Spine and leaf nodes create a scalable network fabric that is optimized for east-west data transfer - typically traffic between an application server and its supporting data services (databases, file servers)

Spine-leaf enables nonlocal traffic to pass from any ingress leaf interface to any egress leaf interface through a single, dynamically selected spine node

Because every traffic flow must pass through no more than two network hops, throughput and latency become much more even and predictable

## WAN Topologies <a name="WAN"></a> ([Back to Index](#INDEX))

A WAN (Wide-Area Network) is a network that covers a large geographical area. A WAN is spread across multiple cities or countries for example the Internet

Geographically dispersed LANs are typically connected together by a WAN. WAN connectivity is generally supplied by a service provider. Customers can connect LANs by tunneling traffic securely over the WAN, often via a site-to-site VPN. ISPs routers and switches are invisible to the customer LAN

Older WAN technologies include T1 and T3 leased lines which provide point-to-point connectivity. Frame Relay and Asynchronous Transfer Mode (ATM) provide point-to-multipoint connectivity

Newer WAN technologies include Multiprotocol Label Switching (MPLS) and Metro Ethernet

## SOHO Topologies <a name="SOHO"></a> ([Back to Index](#INDEX))

SOHO stands for Small Office/Home Office which is a small LAN or WLAN with one or more computers.

LAN or WLAN is connected to a service provider network typically over satellite, Digital Subscriber Line (DSL), cable and fiber to the Internet. Satellite and DSL are older/slower technologies. Cable and fiber are faster technologies

## On-Premises and Cloud Deployment <a name="ONPREM"></a> ([Back to Index](#INDEX))

On-premise deployments involved purchasing, configuring and maintaining the deployment at the local level. The organization has full control over the network but it does increase the costs

Cloud deployments are owned/maintained by cloud hosting providers. The provider has control over both hardware and software. Some of the noted benefits are:

* It has a lower upfront cost
* No hiring or training is required

There are also downsides which include:

* Requires monthly usage fee
* Less likely to offer an organization more customization and control

Cloud deployments have decreased operational costs but can increase risks. When the internet service is interrupted, access to resources is also interrupted and confidential data might be stored on a third-party server

The National Institute of Standards and Technology (NIST) defines three service models:

1. Software as a Service (SaaS)
2. Platform as a Service (PaaS)
3. Infrastructure as a Service (IaaS)

### Software as a Service (SaaS)

SaaS enables a consumer to access applications that are running in cloud infrastructure - it does not enable the consumer to manage the cloud infrastructure or configure the provided apps

SaaS exposes the least amount of consumer's network to the cloud and the least likely to require changes to the consumer's network design. A company uses SaaS when it licenses a service provider's office suite and email service and delivers it to end users through a browser

SaaS providers use an Internet-enabled licensing function, a streaming service, or a web app to provide users with software that could otherwise be used locally

Web-based email clients are examples of Saas including:

* Microsoft Office 365
* Google Drive
* iCloud

### Platform as a Service (PaaS)

PaaS provides a consumer with a bit more freedom than SaaS - it enables the consumer to install and possibly configured provider-supported apps in the cloud infrastructure

Companies that use a provider's deployment tools or API to deploy specific cloud-based applications or services is using PaaS. An organization could use a third party's MySQL database and Apache services to build a cloud-based customer relationship management platform (CRM)

### Infrastructure as a Service (IaaS)

IaaS provides the greatest degree of freedom by enabling a consumer to provision processing, memory, storage, and network resources within the cloud infrastructure. It also enables a consumer to install OSs and applications but cloud infrastructure remains under the control of the service provider

Companies use IaaS when it hires a service provider to deliver cloud-based processing and storage that houses multiple physical or virtual hosts that can be configured in a variety of ways

Suppose a company wants to establish a web server farm by configuring multiple Linux Apache MySQL PHP (LAMP) servers. The company could save hardware costs by virtualizing the farm and using a provider's cloud service to deliver the physical infrastructure and bandwidth for the virtual farm

Control over the operating system, software and server configuration would remain the responsibility of the organization but control of the physical infrastructure and bandwidth would be the responsibility of the service provider

Another example of IaaS is using a third party's infrastructure to host corporate DNS and DHCP servers

## Interfaces and Cabling <a name="INTS"></a> ([Back to Index](#INDEX))

Cisco routers support a variety of physical interfaces. Cisco offers fixed-configuration routers and modular routers. Fixed-configuration routers have limited number of integrated interfaces and do not support additional interfaces - makes them suite for SOHO implementations. Modular routers generally come with a small number of integrated LAN interfaces but offer expansion slots

### Copper Cables

Copper wires are used to transmit data as electrical signals. Ethernet, Token Ring, Copper Distributed Data Interface (CDDI) networks all use copper cabling to transmit data

Most modern Ethernet networks use copper unshielded twisted-pair (UTP) cables. These cables are inexpensive, easy to install and support speeds of up to 1Gbps but should be no more than 100 meters in length. UTP cables are segregated into different category ratings

Minimum rating of Cat3 is required to achieve a data transmission of up to 10Mbps - also known as 10BaseT Ethernet

Minimum rating of Cat5 is required to achieve data of 100Mbps - known as Fast Ethernet or 10BaseTX Ethernet or 1Gbps which is known as Gigabit Ethernet or 1000BaseT Ethernet

Coaxial cables support longer segment runs than UTP cables but most modern networks no longer use coaxial cables

### Connecting UTP with RJ-45

UTP cables contain 4 pairs of colour-coded wires:

1. white/green and green
2. white/blue and blue
3. white/orange and orange
4. white/brown and brown

The 8 wires must be crimped into the 8 pins within an RJ-45 connector. The pins in the RJ-45 connector are arranged in order from left to right

In a typical Ethernet or Fast Ethernet cabling scheme, the wires that are connected to Pins 1 & 2 transmit data and the wires connected to Pins 3 & 6 receive data

Gigabit Ethernet transmits and receives data on all 4 pairs of wires

There are 2 different Telecommunications Industry Association (TIA) wire termination standards for an RJ-45 connector - T568A & T568B

The T568A standard is compatible with Integrated Services Digital Network (ISDN) cabling standards

The T568B standard is compatible with a standard established by AT&T

Wires used for transmit and receive in one standard are inverse in the other

The T568A Standard:

* uses the white/green and green wires for Pins 1 & 2
* uses the white/orange and orange wires for Pins 3 & 6

The T568B Standard:

* uses white/orange and orange wires for Pins 1 & 2
* uses white/green and green wires for Pins 3 & 6

The white/blue and blue and white/brown and brown wires are typically connected to the same pin regardless of standard

### Understanding Straight-Through and Crossover Cables

There are times when you should use T568A on one side and T568B on the other side. A crossover cable uses a different standard at each end - used to connect two workstations, two switches, two routers over the same cable or any of the same two devices

Dissimiliar Ethernet devices such as router and switch, switch and workstation must be connected with a straight-through Ethernet cable - uses the same pinout standard at each end

If two dissimiliar devices are connected with a straight-through, the transmit pair on one end is connected to the receive pair on the other. If two similiar devices are connected with a straight-through, the transmit pins on one end are connected to the transmit pins on the other which means no communication

Because Gigabit Ethernet uses all 8 wires of a UTP cable, the crossover pinout for a cable that is to be used over a Gigabit connection is slightly more complex than an inverse T568-standard

In addition to inverting the transmit/receive wires, the white/blue and blue wires on one end should be inverse to the white/brown and brown wires on the other end

### Serial Cables

Serial cables are also copper cables but are not commonly used anymore. Most service provider equipment has transitioned to Ethernet and fibre-optic cables

Cisco devices support five types of serial cables. Most commonly used serial cable is a 25-pin EIA/TIA-232 cable with a DB-25 conenctor at the end.

One end of a serial cable is the Data Communications Equipment (DCE) end and the other is the Data Terminal Equipment (DTE) end. The DCE end provides clocking to the DTE end - if clock rate is not configured on the DTE end, physical connectivity cannot be established

### Fibre-Optic Cables

Fibre-optic cables transmit data as pulses of light. These cables are not susceptible to radio frequency interference (RFI) or electromagnetic interference (EMI)

Implementing fibre-optic cables can be useful in buildings that contain sources of electrical or magnetic interferences. Fibre-optic cables are also useful for connecting buildings that are electrically compatible

Fibre-optic supports greater bandwidth and longer segment distances - commonly used for network backbones and high-speed data transfer. They can be used to create Fibre Distributed Data Interface (FDDI) LANs - 100Mbps dual-ring LANs

Cisco devices do not require fibre-optic cable connections to communicate with each other

Fibre-optic cost a lot more than copper UTP, shielded twisted-pair (STP) or coaxial cables

### Fibre-Optic Cable Types

There are two main types of Fibre-Optic cables:

1. Multimode Fibre (MMF)
2. Single-Mode Fibre (SMF)

<ins>__MultiMode Fibre__</ins>

MMF can use a 62.5 micron core and wavelength of 850 nanometers. They are typically used for distances less than 2km

When light is transmitted through a fibre-optic cable, light is only propogated by the fibre core at certain angles or modes. The light transmitted into the core of an MMF cable is typically in the 850-nm or 1300-nm frequency range

Because MMF has a relatively large core that permits many different angles of light, the signal becomes dispersed over great distances - this dispersion effectively limits the usable distance of MMF to 2km

MMF is typically used in campus designs that require at least 1Gbps of bandwidth and network runs that are less than 2km

<ins>__Single-Mode Fibre__</ins>

SMF typically uses a 9-micron core. Light transmitted into the core is typically in the 1310nm or 1350nm frequency range

Because SMF has a small core that permits very few angles of light, the signal does not become very dispersed over great distances - enables network runs of 80km or more

Typically used in campus designs that require at least 10Gbps of bandwidth and network runs that are greater than 2km

### Fibre-Optic Cable Connections

Older cables use ST and SC connectors. Older ST connector is round, spring-loaded connector. SC connector is square-shaped that snaps into its receptacle. SC is available in both single and duplex variables

Newer fibre-optic cables can also use LC or MT-RJ connectors

LC connectors are small form factor connectors that are available in both single and duplex varieties. They snap into their receptacle and are half the size of SC connectors

MT-RJ connectors look like miniature RJ-45 Ethernet copper connectors. They provide duplex interface in a single connector

### PoE

PoE provides in-line power for connected IP phones and WAPs over the same cable that varries voice and data traffic. PoE eases VoIP and WLAN implementations because you are not limited to installing devices next to existing power sources - as long as there is a network jack, the device can draw power from the network cable

A Cisco Catalyst switch can provide power to both Cisco and non-Cisco devices that support either IEEE 802.3af standard, the IEEE 802.3at standard or the Cisco prestandard method

For a Catalyst switch to succesfully provide power, both the switch and device must support the same PoE method. After a common PoE method is determined, CDP messages are sent between Catalyst switches and Cisco devices can further refine the amount of allocated power

802.3af standard divides power requirements into the following classes:

* Class 0: 0.44 - 12.94W
* Class 1: 0.44 - 3.83W
* Class 2: 3.84 - 6.49W
* Class 3: 6.49 - 12.95W

Class 0 is the default PoE level - devices classified as such will draw as much power as they need

The 802.3at PoE Plus standard adds a fourth class, Class 4, which is used for high-power PoE devices - class 4 provides 12.95W to 25.50W of power

Cisco Catalyst switches monitor and police PoE ports. If a device attempts to draw more power than a port is configured to provide, a syslog message is issued and port shutdown and enters the error-disabled state

## Troubleshooting Interfaces and Cabling <a name="TROUBLE"></a> ([Back to Index](#INDEX))

### Excessive Noise

Excessive Noise is a problem that can cause tranmissions errors. Noise errors are caused by a physical media problem. A damaged cable or wrong cable type could cause excessive noise errors to occur

Excessive noise errors are detectable by viewing output from the __show interfaces__ command - a high number of Cyclic Redundancy Check (CRC) errors along with a low number of collisions can indicate noise issues

NOTE: INSERT IMAGES

### Collisions

Too many collisions can cause network congestion due to packets being retransmitted as a result of the collisions

Malfunctioning NICs in hosts can cause jabber on the network which causes collisions. Too many devices on one network can also cause collisions and duplex mismatch errors between devices can cause collisions

Resolving collision errors may involve:

* Replacing NICs in client computers
* Creating additional network segments
* Reconfigurating duplex settings

Number of collisions that occur on an interface can be viewed using the __show interfaces__ command - high number of collisions could indicate transmission problems on the network

NOTE: INSERT IMAGES

### Late Collisions

A late collision is a collision that occurs after the 512th bit (64th byte) of a frame that has been transmitted. The amount of time it takes to sends the first 512 bits of a frame is dependent on the network technology:

* 51.2 microseconds to send 512 bits over a 10-Mbps Ethernet segment
* 5.12 microseconds to send 512 bits over a 100-Mbps Ethernet segment

Late collisions can occur as a result of:

* Duplex mismatch errors
* Network segment that extends farther than the cable length supports

Number of late collisions that occur on an interface can be viewed via __show interfaces__ command - show under the late collisions counter

NOTE: INSERT IMAGES

### Duplex Mismatch

Duplex mismatch errors can cause a number of problems:

* Intermittent connectivity
* Performance problems
* High number of collisions
* Late collisions

Duplex mismatch occurs when the ends of a network link are configured with different duplex settings - both ends need to be configured with the same duplex setting

One symptom of mismatch is the half-duplex side will report late collisions. The full duplex side will report runts, frame check sequences (FCS) and alignment errors

Duplex mismatches can sometimes be difficult to diagnose. If you suspect that a duplex mismatch error is causing network problems, use the __status__ parameter of the __show interfaces__ command - this verifies the duplex settings for all interfaces on a device

NOTE: INSERT IMAGES

The __a-__ indicates autonegotiation. Autonegotiation is a method of electrical signaling between interfaces to enable the automatic configuration of speed and duplex settings on an interface

If one side of the link is statically configured, the autonegotiation-enabled side will attempt to operate at the fastest speed supported - the speed field for autonegotiated port will display auto

Setting autonegotiation on only one side of a link can cause configuration problems on the link - it is not possible to statically configured the duplex settings of a port unless the port speed is statically configured first

### Speed Mismatch

Speed mismatch errors can prevent an interface from sending and receiving traffic. A speed mismatch occurs when one end of a network link is configured to use a different speed than the other end - the link between the two would not be able to be established and remain in a down state

You can explicitly configure the speed setting on an interface or autonegotiate it - you are allowed to have one end autonegotiate and one statically configured

In the case where one is static and one is autonegotiated, the autonegotiating port can identify the other port link's speed by the eletrical signal sent by the port

Prevent a speed mismatch from occuring by ensuring that at least one end of a link is configured to autonegotiate the speed settings

NOTE: INSERT IMAGES

### Understanding the OSI Model to Troubleshoot Networks

There are 3 main techniques for troubleshooting using the OSI Model:

1. Bottom Up 
2. Top Down
3. Divide and Conquer

### Bottom Up Troubleshooting Technique

The Bottom Up Technique starts at the Physical layer of the OSI model and works through each layer upward. Typically start troubleshooting by checking the cable is plugged in correctly then check and verify the network card, then IP address, etc...

### Top Dowm Troubleshooting Technique

The Top Down Technique starts at the Application layer of the OSI model and works through each layer downward. Typically start troubleshooting by examining or restarting the network apps

### Divide and Conquer Technique

The Divide and Conquer Technique starts at the Network layer and works either up or down the model depending on the outcome of different tests

NOTE: INSERT IMAGES

### Troubleshooting Physical Layer Connectivity

To troubleshoot the Physical layer, begin by verifying that physical connectivity exists between the router and ISP. There are several ways to verify physical connectivity:

* First, simply examine the cable
* Second, connect to the router and issue the __show interfaces__ command

When issued without parameters, the __show interfaces__ command displays information about each of the interfaces. An interface status of up indicates that the physical interface is working properly. An interface status of down indicates the presence of a Layer 1 issue

Examples of Layer 1 issues include:

* A faulty interface
* A broken cable
* An incorrect cable

You should use a crossover cable to connect the Ethernet interfaces of two similiar devices
You should use a straight through cable to connect two dissimiliar devices

If the interface is in the administrative down state, issue the __no shut__ command

The __show interfaces__ command provides stats that can help diagnose other Layer 1 problems. Many CRC errors on an interface could be indicative of a bad cable. A high number of input/output queue drops could indicate that the router hardware is unable to efficiently process the volume of traffic being sent to the router

Some Cisco configuration mistakes can create Physical layer problems. The DCE end of a serial connection provides clocking information to the DTE end. If the correct clock rate is not set on the DTE interface, physical connectivity cannot be established. You can use the __show controllers serial__ command to determine which end

Ethernet interfaces require that the duplex configuration matches on each end of the link - either full-duplex or half-duplex. Full Duplex means data is being sent from one pair of wires and received by using a different pair of wires which prevents collisions from occuring and enables both ends of a link to transmit and receive information simultaneously

Most modern devices automatically negotiate the duplex settings for Ethernet, FastEthernet and GigabitEthernet interfaces. Duplex mismatches can still occur if the duplex command is manually configured with different nodes on each end. If a high number of collisions are displayed in the output of the __show interfaces__ command, a duplex mismatch could be it

The speed of an interface is also automatically negotiated on modern devices - a Full Duplex Gig interface that is connected to a Full Duplex Fast interface will negotiate a speed of 100Mbps. If the speed command is issued on each side of the link and the speeds do not match, no link is established

A Fast interface that is manually configured to a speed of 100Mbps will not link with a Gig interface that is manually configured to a speed of 1000Mbps

Cisco recommends manually configuring speed and duplex settings on links to devices that are not likely to change or be moved. For most devices automatic negotiation of speed and duplex should be allowed to occur

### Troubleshooting Data Link Layer Connectivity

The __show interfaces__ command is also good for verifying the Data Link Layer components. A Layer 2 protocol is required to transmit information from one interface to another. Protocols that operate at the Data Link layer include:

* Ethernet
* PPP
* High-Level Data Link Control
* Frame Relay


The Line Protocol which is the Data Link layer protocol is in the up state. The Layer 2 protocol must match on each end of a link for connectivity to be established

An interface status of up combined with a line protocol status of down indicates the presence of a Layer 2 problem

Some examples of Data Link layer problems include:

* Mismatched encapsulation between linked serial interfaces
* Clocking errors
* Lack of keepalive messages

Verify the Layer 2 encapsulation method by examining the __show interfaces__ command. By default, a Cisco serial interface is configured to use HDLC encapsulation

The __show interfaces__ command is useful for verifying maximum transmission unit (MTU) configured on an interface. The MTU is the largest frame a device can transmit - sometimes also used to describe the largest packet that a router can forward

The default MTU for an Ethernet frame is 1500 bytes. Because an IP packet has a 20 byte header, the largest IP payload that can be carried in an Ethernet frame is 1480 bytes

If a frame exceeds the MTU of a link, the frame will be fragmented if possible or discarded if the DO-NOT-FRAGMENT bit is set

### Troubleshooting Network Layer Connectivity

Troubleshooting Layer 3 is the most involved task in troubleshooting router connectivity. Network Layer troubleshooting requires the verification of correct IPv4 and IPv6 network addressing - must understand IPv4 and VLSM and IPv6 addressing

Network Layer troubleshooting might involve the examination of routing tables and routing protocol configurations or default gateway configurations

## Review Questions <a name="REV1"></a> ([Back to Index](#INDEX))

<ins>Review Question 1</ins>

How do spines and leafs connect in a spine-leaf topology?

1. Each leaf must connect to every spine
2. Each leaf must connect to at least two spines
3. Each spine must connect to every other spine
4. Each leaf must connect to every other leaf

<details><summary>Review Question 1 Answer</summary>
<p>
	
The answer is __1__

Explanation:

In a spine-leaf topology, each leaf must connect to every spine. In addition, each spine must connect toe very leaf. A spine-leaf topology is a two-tier network architecture in which every lower-tier leaf switch connects to every top-tier spine switch. However, leafs and spines are not connected to each other

</p>
</details>

<ins>Review Question 2</ins>

Which of the following cloud computing service models provides the least management control to the consumer?

1. IaaS
2. PaaS
3. SaaS

<details><summary>Review Question 2 Answer</summary>
<p>
	
The answer is __3__

Explanation:

SaaS is the cloud computing service model that provides the least management control to the consumer. It enables a consumer to access applications that are running in the cloud infrastructure but does not enable the consumer to manage the cloud infrastructure or configure the provided applications
	
</p>
</details>

<ins>Review Question 3</ins>

An interface has a status of up combined with a line protocol status of down. At which of the following layers does the problem most likely exist?

1. at the Physical Layer
2. at the Data Link Layer
3. at the Network Layer
4. at the Transport Layer


<details><summary>Review Question 1 Answer</summary>
<p>
	
The answer is __2__

Explanation:

An interface status of up combined with a line protocol of down most likely indicates the presence of a L2 problem. Examples of L2 problems include mismatched, encapsulation between serial links, clocking errors, lack of keepalive messages. 
	
</p>
</details>

</p>
</details>

<details><summary>Module 2 - Network Addressing and Transport</summary>
<p>	

## NOTE: This module skips over some subnetting information as it is assumed you know it by now. If you need a refresher, please click [here](https://www.google.com)

# Table of Contents <a name="INDEX2"></a>

1. [Summary](#SUMMARY)
2. [Layer 2 Addressing](#L2ADD)
3. [Layer 3 Addressing](#L3ADD)
4. [Differences Between IPv4 and IPv6](#DIFF46)
5. [Differences Between IPv4 and IPv6 Headers](#DIFFHEADERS)
6. [IPv6 Address Composition](#IPV6COMP)
7. [IPv6 Prefixes](#IPV6PREFIX)
8. [IPv6 Address Types](#IPV6TYPES)
9. [Global Unicast Addresses and Route Aggregration](#GLOBUNI)
10. [EUI-64 Interface IDs](#EUI64ID)
11. [Stateful and Stateless Address Configuration](#STATEADD)
12. [Using IPv6 in an IPv4 World](#IPV4WORLD)
13. [Verifying Layer 3 Addressing](#VERL3)
14. [Layer 4 Addressing](#L4ADDRESSING)
15. [Review Questions](#REV2)

![](/images/network2.jpg)

## Summary <a name="SUMMARY"></a> ([Back to Index](#INDEX2))

Addresses are used to send messages between communicating devices at Layer 2, Layer 3 and Layer 4 of the OSI model. Communication on Ethernet networks use 48-bit MAC addresses at Layer 2. MAC addresses are assigned by manufacturer and cannot typically be changed.

IPv4 and IPv6 are predominantly used on Ethernet networks at Layer 3. IPv4 addresses have 32 bits and IPv6 addresses have 128 bits

UDP and TCP port numbers are used to determine services at Layer 4. UDP is a connectionless protocol while TCP is a connection-oriented protocol

## Layer 2 Addressing <a name="L2ADD"></a> ([Back to Index](#INDEX2))

Layer 2 addresses are created and assigned to devices when the device is manufactured. They have a combination of a manufacturing code assigned by the IEEE and a unique code to each unit.

The addresses are encoded in the hardware of each device commonly referred to as Burned In Addresses (BIA) and cannot be changed. Many devices allow the user to configure an alternate address in addition to the BIA. The Layer 2 address is part of each physical device

### Ethernet Overview

When two devices send data simultaneously, a collision occur - both devices wait a random amount of time before attempting to resend,  When many devices are connected to one or more hubs to form a large collision domain, collisions are more likely to occur. Switches divide collision domains so collisions are less likely to occur

Full-duplex Ethernet networks do not use any method to control media access - devices configured for full-duplex operation can simultaneously send and receive data. Because Full-duplex devices can send data as soon as they are ready, CSMA/CD is not required

Switches are capable of full or half duplex operations while hubs can only operate in half duplex mode

### Ethernet Frames

An Ethernet Frame typically consists of seven fields in the following order:

1. A 7-byte preamble field
2. A 1-byte start-of-frame (SOF) field
3. A 6-byte destination address field
4. A 6-byte source address field
5. A 2-byte type field
6. A data field in the range from 46 through 1500 bytes
7. A 4-byte Frame Check Sequence (FCS) field

The first 5 fields are known as the __Ethernet Header__

* The __Preamble__ field is used to notify receiving hosts that a frame is being sent
* The __SOF__ field is used for synchronization with other hosts on the LAN
* The __Destination Address__ field contains the MAC address of the host which the data is intended for
* The __Source Address__ field contains the MAC address of the host sending the data

The major difference between an Ethernet header and an 802.3 header is the 2-byte field that ends each header. An Ethernet header contains a 2-byte length field that stores the number of bytes that are contained in the frame's data field. An 802.3 header uses a type field to indicate the protocol that is intended to receive the frame's data after processing

In both Ethernet and 802.3 frame formats, a __payload__ field of a size in the range from 46 to 1500 bytes follow the header. An 802.3 frame stores both an 802.2 header and its payload in that field. An Ethernet frame contains only the payload in the equivalent field

Both 802.3 and Ethernet frames end with an FCS field. The FCS field is a 4-byte cyclic redundancy check (CRC) that is intended to enable a frame's receiver to determine whether the frame has been corrupted in transit - the FCS is calculated based on the value of every other field in the frame

### MAC Addresses

MAC addresses are written in hexadecimal format. A MAC address is composed of six 8-bit octets or bytes for a total of 48 bits of data in the entire address.

The most significant bytes are at the beginning and are transmitted first. Bytes decrease in significance as you move through the address to the least significant octet at the end.

The first three octets represent the Organizationally Unique Identifier (OUI) which is assigned by the IEEE to identify the manufacturer. The last three octets represent the unique NIC-specific identifier assigned to the device

The significance of each octet follows the same rule of the overall address - most significant bit on the left, least significant bit on the right. When transmitted, a bit differs from a byte in that the least significant bit of a byte is transmitted first

The two least significant bits of the most significant byte of a MAC address are used as indicator flags. The least significant bit of the most significant byte is where a MAC address is designated as __unicast__ or __multicast__ - 0 means unicast and 1 means multicast

The second least significant bit is used to designate whether the MAC address is globally administered by IEEE and carries an OUI or is locally administered - O means OUI and 1 means Locally Administered

## Layer 3 Addressing <a name="L3ADD"></a> ([Back to Index](#INDEX2))

Layer 3 addresses are assigned to devices that use IP to exchange data on a network. IP is a route protocol

Routed protocols define the way information is packaged and sent from one network to another. They do not determine the path from source to destination - that is handled by routing protocols. Routed protocols simply address the packet of information and allow the routing protocols to determine the path

The purpose of Layer 3 addresses is to pinpoint the location of a device in the network. Layer 3 addresses assigned by network administrators to a particular device. Addresses can be reused when a device is upgraded or removed

There are two categories of IP addresses:

* Public
* Private

Public IPs are globally unique addresses that are assigned by IANA to large companies and ISPs. Private IPs are locally unique addresses that are not routable over public networks but are used in internal networks

### IPv4 Overview

IPv4 supports:

* Unicast
* Multicast
* Broadcast

A basic IPv4 header without options is 20 octets - 20 bytes or 160 bits. The header contains the following:

* Version - 4 bit field specifying IP version (v6 or v4)
* IP Header Length (IHL) - 4 bit field specifying number of 32-bit sections (words) in the header
* Type of Service - 9 bit field indicating the importance of a packet by specifying the quality of service desired
* Total Length - 16 bit field indicating number of bytes/octets in entire IP packet
* Identification - 16 bit field identifying the current packet and used to reassemble packet fragments
* Flags - 3 bit field used to control fragmentation
* Fragment Offset - 13 bit field indicating the position of data in a fragmented paccket so reassembled correctly
* Time To Live (TTL) - 8 bit field acting as countdown timer and discarded when it reaches zero
* Protocol - 8 bit field specifying upper-layer protocol that should process the packet after IP processing
* Header Checksum - 16 bit field used to verify the integrity of the IP header
* Source Address - 32 bit field specifying source IP
* Destination Address - 32 bit field specifying destination IP
* Options - variable length field that specifies other assorted IP options such as security and source routing parameters

Data is part of the IP packet but not part of the header

Because an IP is a 32 bit number, the range of possible values is limited to 2^32 unique addresses - some IP ranges are set aside for specific purposes

<ins>Loopback Addresses</ins>

All addresses in the 127.0.0.0/8 network are reserved for testing purposes

<ins>Private IP Addresses</ins>

10.0.0.0/8, 172.16.0.0/12 and 192.168.0.0/16 are not routable across the Internet but NAT can be used to translate private IPs to public IPs

<ins>Automatic Private IP Addresses (APIPA)</ins>

169.254.0.0/16 addresses are __link-local__ private addresses randomly generated when client cannot obtain IP via DHCP

<ins>Multicast Addresses</ins>

224.0.0.0/4 addresses are used to send a single stream of data to multiple devices
224.0.0.1 multicast address is the all hosts address (sends multicast to all hosts on a subnet)

<ins>Global Broadcast Address</ins>

255.255.255.255 is used to send data to every computer on a network or subnet

### Classful Networks

Classes A, B and C are available for commercial use
Class D addresses are used for multicast traffic
Class E addresses are reserved for experimental purposes only

IP addresses consist of two parts:

* Network portion
* Host portion

1. Class A - start with 0, first octet ranges from 1 through 127
2. Class B - start with 10, first octet ranges from 128 through 191
3. Class C - start with 110, first octet ranges from 192 through 223
4. Class D - start with 1110, first octet ranges from 224 through 239
5. Class E - start with 1111, first octet ranges from 240 through 255

The following are valid IP addresses in each of the classes available for commercial use as defined by RFC 1918:

* Class A 10.0.0.0 through 10.255.255.255
* Class B 172.16.0.0 through 172.31.255.255
* Class C 192.168.0.0 through 192.168.255.255

### Subnetting

Subnetting is a technique used to divide a network into smaller subnets. All devices on a network that belong to a given subnet have a common number in the network portion and a unique host.

The following list displays the most commonly used subnet mask conversions

* /8 = 255.0.0.0
* /16 = 255.255.0.0
* /17 = 255.255.128.0
* /18 = 255.255.192.0
* /19 = 255.255.224.0
* /20 = 255.255.240.0
* /21 = 255.255.248.0
* /22 = 255.255.252.0
* /23 = 255.255.254.0
* /24 = 255.255.255.0
* /25 = 255.255.255.128
* /26 = 255.255.255.192
* /27 = 255.255.255.224
* /28 = 255.255.255.240
* /29 = 255.255.255.248
* /30 = 255.255.255.252

Subnetting and route summarization can work together so that a network can efficiently use registered IP addresses and so that the routers are able to minimize routing table information and routing update traffic

Route summarization enables a router to advertise multiple contiguous subnets as a single larger subnet. Summarization combines several smaller subnets into one large subnet

Route summarization is most efficient when subnets can be summarized within a single subnet boundary and are contiguous - all of the subnets are consecutive

For example, if a router is connected to:

* 123.45.67.64/30
* 123.45.67.68/30
* 123.45.67.72/30
* 123.45.67.76/30

This can be summarized as a contiguous network and advertised as the 123.45.67.64/28 subnet

### Automatic IP Address Configuration

IPv4 addresses and subnet masks can be:

* Manually configured
* Automatically assigned by a DHCP server
* Automatically assigned to a host by itself

Very small networks can be easily managed by an administrator who manually allocates IP addresses to devices as needed but DHCP configuration makes more sense for networks in which manual assignment could produce significant admin overhead

## Differences Between IPv4 and IPv6 <a name="DIFF46"></a> ([Back to Index](#INDEX2))

IPv6 offers several improvements over IPv4:

* Simplified header
* Native IP Security protocol support 
* Improved route aggregration

IPv6 offers all of the following features:

* Uses a 128 bit address space (more unique addresses for future expansion)
* Automatically configures addresses usign ICMPv6 or DHCPv6
* Does not require NAT and PAT in order to converse addresses
* Native implements IPSec
* Relies on Transport layer protocols instead of header checksums for data integrity
* More efficient route aggregration by using multiple prefixes

## Differences Between IPv4 and IPv6 Headers <a name="DIFFHEADERS"></a> ([Back to Index](#INDEX2))

An IPv4 header contains the following fields:

* Version - 4 bit field specifying IP version (v6 or v4)
* IP Header Length (IHL) - 4 bit field specifying number of 32-bit sections (words) in the header
* Type of Service - 9 bit field indicating the importance of a packet by specifying the quality of service desired
* Total Length - 16 bit field indicating number of bytes/octets in entire IP packet
* Identification - 16 bit field identifying the current packet and used to reassemble packet fragments
* Flags - 3 bit field used to control fragmentation
* Fragment Offset - 13 bit field indicating the position of data in a fragmented paccket so reassembled correctly
* Time To Live (TTL) - 8 bit field acting as countdown timer and discarded when it reaches zero
* Protocol - 8 bit field specifying upper-layer protocol that should process the packet after IP processing
* Header Checksum - 16 bit field used to verify the integrity of the IP header
* Source Address - 32 bit field specifying source IP
* Destination Address - 32 bit field specifying destination IP
* Options - variable length field that specifies other assorted IP options such as security and source routing parameters

An IPv6 header exists in two forms:

* Main Header (similiar to IPv4 header)
* Extensions Header

The IPv6 Main Header contains the following fields:

* Version - same name and function as IPv4 header field
* Traffic Class - functions the same as the IPv4 Type of Service field
* Flow Label - new IPv6 Main Header field used to label packets for special handling
* Payload Length - functions the same as the IPv4 Total Length field
* Next Header - functions the same as the IPv4 Protocol field
* Hop Limit - functions the same as the IPv4 TTL field
* Source Address - same as IPv4 header
* Destination Address - same as IPv4 header

## IPv6 Address Composition <a name="IPV6COMP"></a> ([Back to Index](#INDEX2))

IPv6 address consists of 32 hexadecimal characters representing a 128 bit binary value. IPv6 addresses can be separated into eight 4 character quartets separated by colons

Each hexadecimal character in a quartet represents a 4 bit binary value and each quartet in an IPv6 address could be expressed as 16 binary digits

### Abbreviating IPv6 Addresses

You can omit the leading zeroes in each quartet of an IPv6 address. For example:

	The address 0001:0003:0003:0040:0050:0066:0777:0ABC can become 1:2:3:40:50:66:777:ABC

However, you cannot remove trailing zeroees as that would change the value of the quartet

You can also abbreviate IPv6 addresses by representing either a single quartet or consecutive quartets of all zeroes as a double colon. For example:

	The address 1234:5678:0000:0000:0000:0000:0000:9ABC can become 1234:5678::9ABC

You can only use the double colon abbreviation once in an IPv6 address -if multiple sets of zeroes are present the longest set should be replaced

## IPv6 Prefixes <a name="IPV6PREFIX"></a> ([Back to Index](#INDEX2))

IPv6 addresses consist of two distinct segments:

* Prefix
* Interface ID

The Prefix is the __network portion__ of the address
The Interface ID is the  __host portion__ of the address

Because IPv6 is large, some IPv6 prefixes can contain multiple subprefixes which are similiar to IPv4 subnets - subprefixes can make route aggregration simpler

Route Aggregration is the process of grouping routes with common addresses together under a single prefix to minimize the size of a routing table and increase router efficiency

## IPv6 Address Types <a name="IPV6TYPES"></a> ([Back to Index](#INDEX2))

IPv4 uses three types of address:

* Unicast
* Multicast
* Broadcast

IPv6 also uses unicast and multicast and work similiar but IPv6 does not use broadcast addresses

IPv6 uses __Anycast__ addresses which are not available in IPv4. Functions that were performed by broadcast in IPv4 are performed by multicast and anycast in IPv6

Multicast addresses in IPv6 work similiarly to IPv4 - they are used to send packets to multiple devices that are configured with that multicast address

The following table shows common IPv4 multicast addresses and their respective IPv6 multicast addresses:

Multicast Address | IPv4 | IPv6
------------ | ------------- | -------------
All Hosts | 224.0.0.1 | FF02:0:0:0:0:0:0:1
All Routers | 224.0.0.2 | FF02:0:0:0:0:0:0:2
All OSPF Routers | 224.0.0.5 | FF02:0:0:0:0:0:0:5
All OSPF DRs | 224.0.0.6 | FF02:0:0:0:0:0:0:5
All RIP Routers (except RIPv1) | 224.0.0.9 | FF02:0:0:0:0:0:0:9
All EIGRP Routers | 224.0.0.10 | FF02:0:0:0:0:0:0:A

Anycast addresses are used to send packets to the closest device that is configured with the anycast address. The closest device is selected by the routing protocol used by the router and is ideal for load balancing

A single interface can be configured with multiple unicast, multicast and anycast addresses. Each type of address uses a distinct type of prefix:

Address Type | Address or Prefix
------------ | -------------
Global Unicast | 2000::/3 (starts with 2 or 3)
Unique Local Unicast | FC00::/7 (starts with FC or FD)
Link-Local Unicast | FE80::/10 (starts with FE8, FE9, FEA or FEB)
Multicast | FF00::/8 (starts with FF)
Reserved | Various prefixes
Unspecified Address | ::
Loopback Address | ::1

There are three types of IPv6 Unicast Addresses:

* Global Unicast
* Unique Local Unicast
* Link-Local Unicast

<ins>Global Unicast</ins>

IPv6 global unicast addresses are __globally routable__. They are assigned by ICANN to the RIRs which distributed the addresses to ISPs. The ISPs then distribute the address ranges to organizations. IPv6 global unicast addresses always begin with 2 or 3

<ins>Unique Local Unicast</ins>

IPv6 unique local addresses are assigned by a local administrator and must be __unique__ only within an organization. These addresses always begin with FC or FD and required a randomly generated prefix to ensure that they are unique. These addresses are not aggregrable and cannot be summarized

<ins>Link-Local Unicast</ins>

IPv6 link-local unicast addresses are used for communication over a single link. Routers do not forward traffic sent to a link-local address; they stay on the local link. These addresses are often used for neighbour discovery and typically begin with FE8 although could begin with FE9, FEA or FEB

On Cisco devices, link-local addresses can be manually assigned by using FE8, FE9, FEA or FEB. Link-local addresses that are automatically generated by using EUI-64 always begin with FE8

<ins>Multicast</ins>

IPv6 multicast addresses are similiar to IPv4 multicast addresses and always begin with __FF__

<ins>Anycast</ins>

IPv6 anycast addresses use the same address space as IPv6 global unicast addresses. An anycast address will look the same as a global unicast address

There are two special IPv6 address:

* Unspecified Address
* Loopback Address

<ins>Unspecified Address</ins>

The Unspecified Address is 0:0:0:0:0:0:0:0 and is typically written as __::__. This address is used by a device when requesting an IPv6 address from DHCPv6 server

<ins>Loopback Address</ins>

The Loopback Address is 0:0:0:0:0:0:0:1 and is typically written as __::1__. This address is similiar to IPv4 127.0.0.1 and used for testing purposes 

## Global Unicast Addresses and Route Aggregration <a name="GLOBUNI"></a> ([Back to Index](#INDEX2))

Global unicast addresses are used to send packets to and from a single interface across globally routable networks. There are five components of a global unicast address and each component represents a separate tier of ownership of the IPv6 address space

The five components are:

* The Registry Prefix - 32 bit prefix assigned to a specific RIR by the ICANN. RIRs manage the allocation of blocks of IPv6 addresses to ISPs in specific geographical regions. This prefix is located at the top of the hierarchy

* The ISP Prefix - 9 bit prefix that is assigned to an ISP by an RIR. ISPs manage the allocation of blocks of IPv6 addresses from their ISP prefix range to their customers. This prefix is second in the hierarchy

* The Site Prefix - 16 bit prefix assigned to an organization by an ISP. A site admin can subnet it. This prefix is third in the hierarchy

* The Subnet Prefix - 16 bit prefix that represents a specific subnet of IPv6 addresses within the organization address range. This prefix is fourth in the hierarchy

* The Interface ID - represents the destination host that uses the remaining 64 bits. This prefix is the final tier of the hierarchy

Route Aggregration reduces the number of routes that must be advertised to a network - combines smaller networks into a large subnet

Aggregrate routes get larger as you move up the global unicast address hierarchy. The hierarchy enables routers to maintain smaller routing tables - they only need to know the range allocated to the RIR, ISP or organization

* The __subnet prefix__ is an aggregrate route to the interface IDs within the subnet
* The __site prefix__ is an aggregrate route to the subnets that are within the site
* The __ISP prefix__ is an aggregrate route to the blocks of addresses that an ISP has distributed to orgs
* The __registry prefix__ is an aggregrate route to the networks that an RIR has distributed to ISPs

## EUI-64 Interface IDs <a name="EUI64ID"></a> ([Back to Index](#INDEX2))

Each IPv6 host on a network must have a unique address to it. Hosts can use the MAC address assigned to them during manufacturing as part of the Interface ID portion of the address - known as the EUI-64 Interface ID

The EUI-64 Interface ID is added to the IPv6 prefix to create a full IPv6 address. An interface ID in EUI-64 format is created by taking the OUI of the MAC address, appending the hex bynber FFFE and then appending the serial identifier

The seventh binary bit is then set to 0 if the IPv6 address is locally unique or set to 1 if the IPv6 is globally unique - this might change the value of the second hex character which consists of the 4,5,6,7 bits

The MAC address 00:13:03:28:C7:A4 can be separated into:

* OUI of 00:13:02
* Serial ID of 38:C7:A4

To create an EUI-64 Interface ID, insert FFFE between the OUI and serial ID. Segregrating the 16 characters into four IPv6 quartets results in the ID 0013:02FF:FE38:C7A4

The second hex character is 0 - written as 0000 in binary

The seventh bit is set to 0, so the address would be a locally unique EUI-64 Interface ID

To make the EUI-64 Interface ID globally unique, you must convert the seventh bit to a 1, thereby changing the binary value to 0010 which equals 2 in hexadecimal - the globally unique EUI-64 Interface ID would be 0213:02FF:FE38:C7A4

## Stateful and Stateless Address Configuration <a name="STATEADD"></a> ([Back to Index](#INDEX2))

Dynamic address configuration of IPv6 devices can be performed by using one of two methods:

* Stateful
* Stateless

Stateful configuration requires a DHCPv6 server. Stateless configuration allows the client to generate its own address by using IPv6 network prefix and EUI-64 interface ID

<ins>Stateful Configuration</ins>

Using DHCPv6 works similiary to DHCPv4. DHCPv6 uses multicast messages instead of broadcast messages.

An interface that requires an IPv6 address will start out with the unspecified address (__::__). The client will send router solicitation messages by using Neighbour Discovery Protocol (NDP) to discover neighbour routers. Routers will reply with a router advertisement that lets the client known whether DHCPv6 servers are available.

If DHCPv6 servers are available or if the client does not receive any router advertisements, the client will send multicast packets to FF02::1:2 (all DHCP agents address). The DHCPv6 server will configure the client with IPv6 address information such as the client's leased IPv6 address, the IPv6 network prefix, the IPv6 address of the default router, the domain name, and IPv6 address of one or more DNS servers

<ins>Stateless Configuration</ins>

Assigns an IPv6 address to an interface without the need for a DHCPv6 server. A client will send router solicitation messages to discover a router and routers will reply with router advertisements. If router advertisements state that no DHCPv6 server is available, the router advertisements will include thhe IPv6 prefix used on the network as well as the IPv6 address of the default router

The client will combine the IPv6 prefix with the EUI-64 interface ID to create a unique IPv6 adress

Although a DHCP server is not required for stateless configuration, a DHCPv6 server is required in order to configure a client with the domain name and IPv6 addresses of DNS servers - this info is not provided with router advertisements

## Using IPv6 in an IPv4 World <a name="IPV4WORLD"></a> ([Back to Index](#INDEX2))

It is important to be able to migrate to IPv6 while maintaining the ability to send data over the existing IPv4 infrastructure

Several mechanisms exist that provide interoperability between IPv4 and IPv6:

* Dual Stack
* Network Address Translation-Protocol Translation (NAT-PT)
* Tunneling

<ins>Dual Stack</ins>

Dual Stack enables a host or router to communicate over both IPv4 and IPv6. Dual Stack devices are configured with an IPv4 and IPv6 address. The version of IP that is used is determined by the destination address of that packet

<ins>Network Address Translation-Protocol Translation</ins>

NAT-PT is used to enable communication between IPv6-only hosts and IPv4-only hosts. It translates IPv6 packets to IPv4 packets and vice versa

Because NAT-PT relies on address translation, a NAT-PT router must manage address mappings so that the router can correctly translate IPv4 and IPv6 addresses - address mappings can be created statically or dynamically

<ins>Tunneling</ins>

Tunneling is used to pass IPv6 traffic over an IPv4-only network. There are several methods for tunneling IPv6 traffic over IPv4 or vice versa:

* 6to4
* 4to6
* Intra-Site Automatic Tunneling Addressing Protocol (ISATAP)
* Teredo

To pass IPv6 traffic over a network that supports only IPv4, 6to4 tunneling is often used. 6to4 tunneling __encapsulates__ an IPv6 packet inside an IPv4 header. Each IPv6 network border router that acts as a tunnel endpoint must be configured with both IPv4 and IPv6 stack

Routers on the IPv4 only network recognize only the IPv4 header information - IPv6 packet is simply carried as the data payload of the IPv4 packet. Automatic 6to4 tunneling establishes point-to-multipoint links to remote IPv6 networks over a shared IPv4 network. Manually configured tunnels are typically point-to-point

4to6 tunneling method is the reverse of the 6to4 tunneling method. Routers on the IPv6 only network recognize only the IPv6 header information. IPv4 packets must be encapsulated inside an IPv6 header so they can pass over the IPv6-only network

ISATAP tunneling works similiarly to 6to4 tunneling but does not support IPv4 NAT on the tunnel endpoints

Teredo tunneling creates the tunneling endpoints on dual-stack hosts instead of on the routers. The host itself will create the IPv6 packet and encapsulate it inside an IPv4 packet

## Verifying Layer 3 Addressing <a name="VERL3"></a> ([Back to Index](#INDEX2))

<ins>Windows 10 Verification</ins>

To determine IP addressing information on a computer running Windows 10 by using the GUI, use the following steps:

1. Go to Settings
2. Select Network & Internet
3. On the left-hand pane, select Wi-Fi or Ethernet
4. Scroll down to Properties

To achieve the same using the CLI, simply type __ipconfig__ into the Command Prompt

<ins>Linux Verification</ins>

The GUI for each Linux disto can differ. You can usually find IP addressing information on the Network tab in the Settings menu

You can determine IP addressing information on a computer running Linux by issuing any of the following commands:

* hostname -I
* ip addr
* ifconfig

<ins>MacOS Verification</ins>

To determine IP addressing information on a computer running MacOS by using GUI, use the following steps:

1. From the Apple menu, pull down System Preferences
2. Click on the Network preference pane
3. Select the interface on the left

To achieve the same using the CLI, enter any of the following commands in the CLI:

* ifconfig | grep inet
* ipconfig getifaddr en0 (usually for Ethernet)
* ipconfig getifaddr en1 (usually for Wi-Fi)

## Layer 4 Addressing <a name="L4ADDRESSING"></a> ([Back to Index](#INDEX2))

Packet addressing at Layer 4 focuses on port numbers - they are assigned by IANA

A port is the communication channel used by computers on networks to move data from one computer to another. Well-known port numbers are assigned to enable unknown clients to communicate with one another

The IANA has designated three ranges of port numbers:

* Well known port numbers from 0 to 1023
* Registered port numbers from 1024 to 49151
* Dynamic and/or private ports from 49152 to 65535

A packet's IP address may be appended with a port number and the combined address creates what is called the __socket address__

On the Transport Layer, data is directed to its corresponding application process on a computer as indicated by the port number. The socket address is extracted by the OS, and the headers are removed before the data packets are delivered to the appropriate application

<ins>UDP</ins>

The User Datagram Protocol (UDP) is a Transport layer protocol that is used for unreliable, connectionless datagram transfer. UDP does not establish a communication session before sending data

UDP is considered unreliable because it does not provide error correction or flow control and because a computer does not send an ACK that the data was received

Because there is no sequencing information contained in the UDP ehader, datagrams can arrive out of sequence. It is the responsibility of the application receiving the datagrams to either rearrange them or discard them without notice

The following fields are contained in a UDP header:

* Source Port - 16 bit field that indicates the upper-layer service used on the source device
* Destination Port - 16 bit field that indicates the upper-layer service that will use the data on the destination device
* Length - 16 bit field that specifies the length of the UDP segment
* Checksum - 16 bit field that is used to verify the integrity of the UDP segment to ensure that it was not modified or corrupted in transit

Examples of Application Layer Protocols that rely on UDP for transport include the following:

* DHCP - used to assign IP addressing information to clients and uses UDP ports 67/68
* SNMP - used to monitor and manage network devices and uses UDP ports 161/162
* TFTP - used to transfer files over a network and uses UDP port 69
* NTP - used to synchronize system clock settings and uses UDP port 123
* RADIUS - used in Authentication, Authorization and Accounting and uses UDP ports 1812/1813

<ins>TCP</ins>

The Transmission Control Protocol (TCP) is used for reliable, connection-oriented transfer of data between networked computers. When a computer wants to communicate over TCP, a three-way handshake is performed between source and destination computers

TCP is considered reliable because it offers features such as:

* Error Detection and Correction
* Flow Control
* Sequencing
* Acknowledgements

Data sent by TCP is ordered and checked for errors and any lost packets are retransmitted

The fields that provide the reliability feature can be seen in the TCP header. A TCP header is much longer than a UDP header

The following fields are contained in a TCP header:

* Source Port - 16 bit field that indicates the upper-layer service used on the source device
* Destination Port - 16 bit field that indicates the upper-layer service that will use the data on the destination device
* Sequence Number - 32 bit field that specifies the number given to the first byte of data in the segment and used to reassemble segments
* Acknowledgement Number - 32 bit field that specifies the sequence number of the next byte of data that the sender expects to receive
* Data Offset - 4 bit field that indicates the number of 32 bit sections (words) in the TCP header
* Reserved - 6 bit field that is reserved for future use and should currently be set to zero
* Flags - 6 bit field that is used to activate control flags such as SYN and ACK for establishing connections and FIN for terminating
* Window - 16 bit field that specifies the size of the sender's receive window, which is used to buffer incoming data
* Checksum - 16 bit field that is used to verify the integrity of the TCP segment to ensure that it was NOT modified/corrupted
* Urgent Pointer - 16 bit field indicates the first urgent data byte in the segment
* Options - variable-length field that specifies other assorted TCP options; zeroes are appended to pad the end of the options field so the header ends and data begins on a 32 bit boundary

Examples of Application Layer Protocols that rely on TCP for transport include the following:

* FTP - used to transfer files over a network and use TCP ports 20/21
* HTTP - used to transfer web pages over the internet and uses TCP port 80
* SMTP - used to send email messages and uses TCP port 25
* POP3 - used to receive email messages and uses TCP port 110
* Telnet - used for device management and uses TCP port 23
## Review Questions <a name="REV2"></a> ([Back to Index](#INDEX2))

<ins>Review Question 1</ins>

Which of the following is the OUI in the MAC address 22:44:66:88:AA:CC?

1. 22:44:66
2. 44:66:88
3. 66:88:AA
4. 88:AA:CC

<details><summary>Review Question 1 Answer</summary>
<p>
	
The answer is __1__

Explanation:

The OUI in the MAC address 22:44:66:88:AA:CC is 22:44:66. MAC addresses are 48 bit addresses that are written in hexadecimal format. The first three octets represent the OUI

</p>
</details>

<ins>Review Question 2</ins>

Which of the following is an IPv4 address that can be routed over the Internet?

1. 10.16.1.1
2. 10.32.1.1
3. 172.16.1.1
4. 172.32.1.1
5. 192.168.16.1
6. 192.168.32.1

<details><summary>Review Question 2 Answer</summary>
<p>
	
The answer is __4__

Explanation:

The address 172.32.1.1 is an IPv4 address that can be routed over the Internet. The following ranges are used for private IPv4 addressing:

10.0.0.0 through 10.255.255.255
172.16.0.0 through 172.31.255.255
192.168.0.0 through 192.168.255.255
	
</p>
</details>

<ins>Review Question 3</ins>

Which of the following IPv6 prefixes is used for unique local unicast addresses?

1. 2000::/3
2. FC00::/7
3. FE80::/10
4. FF00::/8

<details><summary>Review Question 3 Answer</summary>
<p>
	
The answer is __2__

Explanation:

The FC00::/7 prefix includes IPv6 addresses that begin with FC or FD. Unique local unicast addresses are similiar to IPv4 private addresses. The IPv6 prefix 2000::/3 is used for global unicast addresses - beginning with 2 or 3. The IPv6 prefix FE80::/10 is used for link local unicast addresses - beginning with FE8, FE9, FEA or FEB. IPv6 prefix FF00::/8 is used for multicast addresses - beginning with FF

</p>
</details>

<ins>Review Question 4</ins>


Which of the following protocols use TCP (select 3 choices)?

1. DHCP
2. FTP
3. HTTP
4. SMTP
5. SNMP
6. TFTP

<details><summary>Review Question 4 Answers</summary>
<p>
	
The answer is __2,3 and 4__

Explanation:

FTP, HTTP and SMTP use TCP. TCP is a Transport Layer protocol that is used for reliable, connection-oriented transfer of data

</p>
</details>

</p>
</details>

<details><summary>Module 3 - Wireless Networks</summary>
<p>

# Table of Contents <a name="INDEX3"></a>

1. [Summary](#SUMWIFI)
2. [Radio Frequency](#RADIOF)
3. [WLAN Topologies](#WLAN)
4. [Wireless Bands and Channels](#BANCHAN)
5. [Wireless Standards](#WSTANS)
6. [Associating with an AP](#ASSAP)
7. [802.11 MAC Frames](#MACFRA)
8. [Review Questions](#REV3)

![](/images/network4.jpg)

## Summary <a name="SUMWIFI"></a> ([Back to Index](#INDEX3))

Wireless communications occur over RF signals. Wireless devices communicate using an IBSS, BSS or ESS wireless topology

WLAN communication occurs over two wireless bands - 2.4GHz and 5GHz. The 2.4GHz band has overlapping channels whereas the 5GHz band has non-overlapping channels

IEEE introduced several wireless standards

* 802.11-1997
* 802.11b
* 802.11a
* 802.11g
* 802.11n
* 802.11ac
* 802.11ax

Each successive standard introduced efficiency and data-rate improvements over previous standards

Wireless clients must associated with an AP in order to communicate on a WLAN. To associate with an AP, the client must be configured with the SSID, appropriate security method and correct authentication key

## Radio Frequency <a name="RADIOF"></a> ([Back to Index](#INDEX3))

WLANs differen from LANs in several ways. Commmunication between devices on a wireless network occurs through the use of radio frequency (RF) signals which are electrical signals sent over the air

RF signals are typically received by radio antennas and can be used to transmit video, audo and data

In WLANs, hosts connect to APs which provide hosts with access to the rest of the network. In medium-to-large Cisco networks, a wireless LAN controller (WLC) can be used along with Lightweight Access Point Protocol (LWAPP) to manage APs

WLCs allow an administrator to centralize security configurations among APs and provide mobility services at Layer 2/3 of the OSI model

RF networks are susceptible to electrical interference. Electrical devices in your office building could cause interference to occur. Wireless devices that are close to the source of the interference could experience a disruption in wireless connectivity - sources can include microwaves, cordless phones, high-power electric lines. Metal shelves, cabinet and machinery can also block a wireless signal

Ensure devices do not lose connectivity by installing multiple APs on the networ. RF networks are also susceptible to noise from other devices operating on the same radio frequency or channel. More devices on the same channel, more likely interference occurs

## WLAN Topologies <a name="WLAN"></a> ([Back to Index](#INDEX3))

<ins>IBSS</ins>

Independent Basic Service Set (IBSS) is an IEEE 802.11 standard WLAN topology consisting of individual peers sometimes referred to as ad-hoc mode

Nodes in ad-hoc mode communicate directly without the use of an AP

Because IBSS networks lack an authentication server, clients are limited in the authentication methods that are available. Lack of available methods makes communications between IBSS devices difficult to secure

<ins>BSS</ins>

Basic Service Set (BSS) is an IEEE 802.11 standard WLAN topology consisting of wireless clients that connect to a single AP. In a BSS, the AP connects to a wired network and provides clients with access to the wired network

Wireless networks that use one or more APs to communicate run in infrastructure mode. Most WLANs operate in infrastructure mode

<ins>ESS</ins>

Extended Service Set (ESS)  is an IEEE 802.11 standard WLAn toplogy consisting of multiple APs on the same subnet. ESS consists of two or more BSSs that are linked by a wired/wireless backbone

Overlapping area between APs ensures that devices can roam from one AP to another without losing connection - coverage overlap of 10-15% is considered optimal

Coverage areas between neighbouring APs should overlap. Neighbouring APs should use wireless channels that do not overlap - ensure APs do not intefere with one another

## Wireless Bands and Channels <a name="BANCHAN"></a> ([Back to Index](#INDEX3))

WLAN communication typically occurs over two wireless bands:

* 2.4GHz
* 5GHz

The 2.4GHz band is divided into 14 channels which are each 24MHz wide

Channel | Range (GHz)
------------ | -------------
1 | 2.401 - 2.423
2 | 2.406 - 2.428
3 | 2.411 - 2.433
4 | 2.416 - 2.438
5 | 2.421 - 2.443
6 | 2.426 - 2.448
7 | 2.431 - 2.453 
8 | 2.436 - 2.458
9 | 2.441 - 2.463
10 | 2.446 - 2.468
11 | 2.451 - 2.473
12 | 2.456 - 2.478
13 | 2.461 - 2.483
14 | 2.473 - 2.495

The channels available for wireless transmission can be limited by local regulatory agencies. Only channels 1-11 are allowed in the US

The channels in the 2.4GHz band have overlapping ranges. Channels that overlap can intefere with one another

A device communication on channel 2 can intefere with a device communicating on channel 5. It is recommended to use nonoverlapping channels. There are three non overlapping channels in the US - 1, 6 and 11. Channels 12 and 13 can be used in most of the world and Channel 14 can only be used in Japan

The 5GHz spectrum is divided into four bands. Each band contains several nonoverlapping channels and each channel is 20MHz wide

Band | Range (GHz) | Channel List
------------ | ------------- | -------------
U-NII-1 | 5.150 - 5.250 | 36 40 44 48
U-NII-2 | 5.250 - 5.350 | 52 56 60 64
U-NII-2 Extended | 5.470 - 5.725 | 100 104 108 112 116 120 124 128 132 136 140
U-NII-3 | 5.725 0 5.825 | 149 153 157 161

Gaps between these ranges are allocated for other purposes. Works is underway to repurpose some frequency ranges and add them to the usable wireless spectrum

Unlike chanels in the 2.4GHz band, channels in the 5GHz band do not intefere with each other. More devices use the 2.4GHz band than a 5GHz band. A device that uses 5GHz band is less likely to encounter interference than a device using 2.4GHz band

## Wireless Standards <a name="WSTANS"></a> ([Back to Index](#INDEX3))

The original 802.11-1997 WLAN standard was released by IEEE in 1997. It operates at 2.4GHz band and has a maximum data throughput of 2Mbps

The 802.11b, 802.11a, 802.11g, 802.11n and 802.11ac WLAN standards are amendments to the original. They were subsequently released by the IEEE. The 802.11ax specification is expected to become standard in late 2020

802.11a and 802.11b standards were both introduced in 1999. The 802.11a standard operates in 5GHz band and has a maximum data throughput of 54Mbps. The 802.11b standard operates in 2.4GHz band and has a maximum data throughput of 11Mbps. Although 802.11a transmits data more efficiently than 802.11b, the 802.11b standard was more widely accepted

The 802.11g standard was introduced in 2003. It operates in the 2.4GHz band and can coexist with 802.11b devices. It transmits data at speeds similiar to 802.11a

The 802.11n standard was introduced in 2009. It operates in both the 2.4GHz band and the 5GHz band. It has added support for Multiple Input, Multiple Output (MIMO) and channel bonding

MIMO uses multiple antennas in concert to increase transmission speeds whereas Channel Bonding increases transmission speeds by allowing multiple interfaces to work together. Both technologies boost the maximum data rate of 802.11n to 600Mbps

The 802.11ac was introduced in 2013. It operates in the 5GHz band and has added support for multi-user MIMO (MU-MIMO) and extended channel bonding. It also increases the transmission speeds to 6.93Gbps

The 802.11ax draft specification operates in 2.4GHz and 5GHz bands at four times the data transmission rate of 802.11ac. It applies improved power-control methods to control interference and reduce power consumption. Typically labelled as Wi-Fi 6

## Associating with an AP <a name="ASSAP"></a> ([Back to Index](#INDEX3))

Wireless clients must associate with an AP before the AP will allow communication. The wireless client must be configured with the appropriate Service Set Identifier (SSID) for the network - the SSID identifies the name of the wireless network to which a device belongs

You should never use the default SSID when you configure an AP and you should also change the default administrative password

You can configure an AP to broadcast the SSID within beacon frames and can disable SSID broadcasts to hide the SSID

When SSID broadcasts are disabled, you must manually configure each wireless client with the correct SSID. The wireless client must use the same SSID to communicate with the AP

In order to associate with an AP, the wireless client must also be configured with the appropriate security protocol and authentication. If wireless AP is configured to encrypt traffic by using WPA, the client must also use WPA

<ins>Open Authentication and WEP</ins>

The original 802.11 standard included two authentication methods:

* Open Authentication
* Wired Equivalent Privacy (WEP)

WEP is extremely weak encryption method that uses RC4 algorithm. WEP keys are easily cracked due to a short 24-0bit initialization vector (IV)

The IV value is added to a 40-bit WEP key to provide 64-bit encryption and is added to a 104-bit WEP key to provide 128-bit encryption

Because IV is sent as clear text, the IV can be intercepted and used to decrypt packets or used for IV replay attacks

WEP is also subject to bit-flipping attacks which exploit a weakness in the Integrity Check Value (ICV). WEP supports only static, preshared keys

<ins>WPA</ins>

Wi-Fi Alliance developed WPA to address significant security weaknesses in the WEP protocol. WPA was only intended as an interim solution until the IEEE 802.11i standard was certified and implemented

WPA uses Temporal Key Integrity Protocol (TKIP) for encryption. Stronger encryption algorithm than WEP. TKIP provides security features such as:

* Key Hashing
* Messages Integrity Check
* Long IV

Keys used by TKIP can change dynamically which increase wireless network security. TKIP provides 128-bit encryption

WPA supports 802.1x and Extensible Authentication Protocol (EAP) based authentication methods. EAP is an authentication framework that can be used for point-to-point connections and for wired/wireless links

<ins>WPA2</ins>

WPA2 was created by the Wi-Fi Alliance as an improvement to the original WPA standard. It fully implements the 802.11i standard

WPA2 uses Advanced Encryption Standard (AES) Counter Mode with Cipher Block Chaining Message Authentication Code Protocol (CCMP) for data encryption. AES-CCMP provides much stronger encryption and supports key length of up to 256 bits. WPA2 supports 802.1x and EAP-based authentication methods

<ins>WPA3</ins>

WPA3 was introduced in 2018 to address weaknesses in WPA2. WPA3 improves encryption by introducing support for AES-Galois/Counter Mode Protocl (AES-GCMP). WPA3-Personal Mode still supports using AES-CCMP at a minimum

WPA3 standard introduces support for Protected Management Frames (PMF) which secures management frame communication between AP and clients

WPA3 also supports 802.1x and EAP-based authentication protocols

<ins>802.1x</ins>

802.1x is a port-based authentication standard that defines the roles and procedures used to authenticate devices. 802.1x uses EAP to provide authentication services for devices requesting network access

802.1x defines the three roles that constitute the authentication framework:

* Supplicant
* Authenticator
* Authentication Server

The Supplicant is an EAP-compatible wireless client that requests access to a network. Before access is granted, the supplicant must provide valid credentials to the authenticator

The Authenticator is an EAP-compatible AP or switch that forwards the credentials to an authentication server for approval

The Authentication server is an Authentication, Authorization and Accounting (AAA) enabled computer such as Remote Authentication Dial-In User Service (RADIUS) that possesses a database of users approved for network access and their applicable permission levels

Once authentication server has verified the identity of the the supplicant, the server informs the authenticator whether access is granted or denied

## 802.11 MAC Frames <a name="MACFRA"></a> ([Back to Index](#INDEX3))

An IEEE 802.11 MAC frame is generally compromised of nine fields:

* Frame Control
* Duration
* ADD1, ADD2, ADD3, ADD4
* Sequence
* Data
* Frame Check Sequence

<ins>Frame Control (FC)</ins>

FC is used to identify the type of 802.11 frame and its 2 bytes of data are subdivided into 11 related fields of information - such as wireless protocol, frame type, frame subtype

<ins>Duration (DUR)</ins>

DUR is a 2 byte field that is used mainly by control frames to indicate transmission timers. It is also used by the Power Save (PS) Poll control frame to indicate the associaton identity (AID) of a client

<ins>ADD1, ADD2, ADD3 and ADD4</ins>

These are 6 byte fields used to convey MAC addresses and Basic Service Set Identifier (BSSID) information. What information resides in which address field is dependent on the type of frame.

ADD1, ADD2 and ADD3 typically contain a source MAC address, destination MAC address, and BSSID with the order being dependent on whether the frame is entering the distribution system (DS), leaving the DS or passing directly between ad-hoc wireless devices

<ins>Sequence (SEQ)</ins>

2 byte field that is subdivided to store two related pieces of information of each frame - fragment number and sequence number

<ins>Data</ins>

The Data field varies in size and contains the frame's payload. For data frames, the payload is user data. For other frames such as management frames, it might contain information such as supported data rates and cipher suites

<ins>Frame Check Sequence (FCS)</ins>

The FCS is a 4 byte cyclic redundancy check (CRC) value calculated from all the 802.11 header fields including data portion of the frame

The value is used by receiving station to determine whether the frame was corrupted during transit 

## Review Questions <a name="REV3"></a> ([Back to Index](#INDEX3))

<ins>Review Question 1</ins>

Which of the following channels in the 2.4GHz band should you use within the United States?

1. 1, 2 and 3
2. 1, 6 and 11
3. 1, 7 and 13
4. 2, 7 and 12

<details><summary>Review Question 1 Answer</summary>
<p>
	
The answer is __2__

Explanation:

You should use channels 1, 6 and 11 in the 2.4GHz band within the US. Although there are 14 channels, only three nonoverlapping channels can be used - 1, 6, and 11. Channels 12, 13 and 14 CANNOT be used within the US

</p>
</details>

<ins>Review Question 2</ins>

Which of the following wireless standards operates in the 2.4GHz range at speeds of up to 54Mbps?

1. 802.11a
2. 802.11b
3. 802.11g 
4. 802.11n

<details><summary>Review Question 2 Answer</summary>
<p>
	
The answer is __3__

Explanation:

The 802.11g standard classifies devices that operate in the 2.4GHz range with a max data throughput rate of 54 Mbps. 802.11a has a max data throughput of 54Mbps but only operates in 5GHz. 802.11b standard operates in 2.4GHz range but has max data throughpu8t rate of 11Mbps. 802.11n standard supports 2.4GHz and 5GHz and has max data throughput of 600Mbps

</p>
</details>

<ins>Review Question 3</ins>

Which of the following wireless security methods supports AES-GCMP for encryption?

1. WEP
2. WPA
3. WPA2
4. WPA3

<details><summary>Review Question 3 Answer</summary>
<p>
	
The answer is __4__

Explanation:

WPA3 supports AES-GCMP for encryption. WPA3-Personal supports AES-CCMP as a minimum level of encryption

</p>
</details>

</p>
</details>

<details><summary>Module 4 - Virtualization Fundamentals</summary>
<p>

# Table of Contents <a name="INDEX4"></a>

1. [Summary](#SUMVIRT)
2. [Understanding Virtualization](#VIRTUALIZE)
3. [Device Virtualization](#DEVVIRT)
4. [Network Virtualization](#NETVIRT)
5. [Container-Based Virtualization](#CONBAS)
6. [Review Questions](#REV4)

![](/images/network3.png)

## Summary <a name="SUMVIRT"></a> ([Back to Index](#INDEX4))

Virtualization provides several advantages over traditional network:

* Partitioning
* Isolation
* Encapsulation
* Hardware Independence

Hypervisor responsible for facilitating the interaction between physical and virtualized hardware. There are two main types of hypervisors - Type 1 and Type 2

* Type 1 Hypervisors - implemented directory on the physical hardware without the need for an underlying OS
* Type 2 Hypervisors - run as privileged applications on the underlying OS

VM is typically stored as a small number of files - VM config, virtual hard drive, possibly VM snapshots

vSwitches are commonly used to connect VMs to each other and to the external network. vSwitches are managed by hypervisors and can interact with physical hardware only through hypervisors

A container bundles binary files and libraries necessary to run its main applications. A container shares operating kernel with the rest of processes on the host - it is more efficient and lightweight than a VM

## Understanding Virtualization <a name="VIRTUALIZE"></a> ([Back to Index](#INDEX4))

In organizations that conform to a traditional network structure, the specific processes or applications required by that organization are allocated dedicated physical resources

An example inlcude your organization requiring a web server, network management system (NMS), centralized network file sharing and a database server.

In a typical networking environment, these apps and services would be implemented on dedicated physical hardware. Four separate physical servers would be required to fill those organizational requirements. If your organization's business model required redundancy, additional physical hardware would likely be implemented

Using dedicated hardware has the advantage of enhancing security by isolating the apps and services from each other. Such a configuration enables the organization to control interactions between and access to the apps/services but it does not scale well

A network configuration that relies exclusively on physical resources is not efficient with regard to:

* Rack space
* Cooling requirements
* Energy requirements
* Resource utilization

If a web server uses 10% of the resources available on its hardware platform, those unused resources cannot be reallocated

Virtualization solves many of the inefficiencies of traditional networking by creating a virtual environment where processes and services can be deployed and resources can be allocated more efficiently

Some of the processes/services in the previous example could be deployed to virtual servers - share physical resources of a single physical server yet remain isolated as though they existed on separate hardware

## Device Virtualization <a name="DEVVIRT"></a> ([Back to Index](#INDEX4))

Device virtualization relies on the deployment of a VM which emulates the physical hardware of a host computer. An OS can be installed on a VM as though it were a physical host. Applications and services can be installed on and configured for that VM

Depending on the device virtualization mechanism, the OS may require minimal modification through installation of specific drivers

The VM itself is typically stored as a small number of files that include:

* VM configuration
* Virtual hard drive
* Possible VM snapshots - save the state of a VM

VMs provide several advantages over traditional network environments

Partitioning enables a single host to run multiple different OS simultaneously and allocate resources among them

Isolation contains VMs in their virtual environments thereby preventing those VMs from discovering any others

Encapsulation allows VMs to easily migrate between hosts

Hardware independence ensures that a VM can migrate to any physical host with appropriate resources

<ins>The Hypervisor</ins>

A Hypervisor is software that is capable of virtualizing the physical components of computer hardware. A Hypervisor is responsible for facilitating the interaction between physical hardware and virtualized hardware

Two main types of Hypervisors:

* Type 1
* Type 2

Type 1 Hypervisors are implemented directly on the physical hardware without the need for an underlying OS whereas Type 2 Hypervisors run as privileged applications running on underlying OS

A Type 1 Hypervisor runs directly on physical hardware. Because there is no underlying OS separating the hypervisor from physical hardware, Type 1 hypervisors are highly performant. Type 1 hypervisors are specialized to the requirements of the VMs that they will host.

Type 1 Hypervisors offer a limited subset of capabilities beyond the functionality necessary to configure, provision and manage VMs. VMWare ESXi and Microsoft Hyper-V are examples of Type 1 hypervisors

Type 2 Hypervisors run as privileged applications on an underlying OS. Additional layer of software prevents Type 2 hypervisors from being as performant as Type 1. Typically, the host OS does not support virtualization capabilities of the hypervisor by default - admins can install additional drivers to support the hypervisor and its virtualized resources

Because a host running Type 2 is also running a complete OS, the host can provide additional processes and services beyond VM management. Oracle VirtualBox and VMware Fusion are examples of Type 2 hypervisors

## Network Virtualization <a name="NETVIRT"></a> ([Back to Index](#INDEX4))

Network Virtualization can be used to emulate physical devices (switches, routers) in a topology. It can also be used to create new topologies by using network resources of an existing physical topology

Virtual Switches (vSwitches) are used to interconnect VMs to each other and to devices outside their host

Network Functions Virtualization (NFV) is used to create appliances such as firewalls and IDS that can perform the functions of their physical counterparts without being confined to a dedicated hardware platform

Virtual LANs (VLANs), Virtual Routing and Forwarding (VRF) and Virtual Private Networks (VPNs) are all forms of network virtualization that use existing network topologies to create new virtual topologies

<ins>Virtual Switches</ins>

A vSwitch is a virtualized switch that emulates a physical Layer 2 switch. vSwitches are commonly used to connect VMs to each other and to the external, physical network

vSwitches are similiar to VMs in that they are managed by a hypervisor and can interact with physical hardware only through capabilities of the hypervisor

Common vSwitches are:

* Cisco Nexu 1000VE
* VMware vSphere Switch
* Open vSwitch (OVS)

<ins>Virtual Network Intefcaces vs Physical Network Interfaces</ins>

A virtual NIC (vNIC) in a VM can be configured by the hypervisor to connect to a vSwitch. The vSwitch can then be connected to a physical NICE (pNIC) on the host to provide a connection to the physical network

Although vSwitches can be connected to the vNICs of VMs without restriction, a vSwitch cannot share a connection to a pNIC with another vSwitch nor can two vSwitches be directly interconnected

<ins>Network Function Virtualization</ins>

NFV is a European Telecommunications Standard Institute (ETSI) standard architecture that recommends decoupling network functions from physical hardware devices by implementing software-based appliances similiar to VMs that are highly specific to their NFs

A virtual network function (VNF) - virtualized NF - is implemented by an appliance and managed by a hypervisor

Load balancers, intrusion detection systems, firewalls, wide area network optimizing and caching appliances are the most common VNFs

Cisco offers a variety of VNFs including:

* Cisco Cloud services Router 1000V (CSR 1000V)
* Cisco NextGen Firewall Virtual Appliance (NGFWv)

<ins>VLANs</ins>

VLAN is a network virtualization mechanism that enables a single Layer 2 switch to function as multiple virtual switches

Traffic within one VLAN is isolated from traffic in all other VLANs. For traffic to pass from one VLAN to another, a router is required or the switch must support interVLAN routing capabilities

<ins>VRFs</ins>

VRF is a network virtualization mechanism that enables a single Layer 3 router to function as multiple virtual routers. When you implement VRFs on a Cisco router, the router interfaces and routing tables associated with each VRF are isolated from other VRFs that have been configured on the router

VRFs are conceptually similiar to VLANs in how they segment traffic on a physical deice into multiple virtual domains. When a VRF is implemented, the same IP addressing scheme can be appied to different routing tables on the same router

VRFs can be used to create multiple network implementations that will use the same infrastructure and the same addressing scheme without causing addressing issues among the other instances

<ins>VPNs</ins>

VPN is a network virtualization mechanism that can create an overlay network on an existing network infrastructure. A VPN can be created to provide secure communications over an unsecure network such as Internet

Because of the almost universal availability of low-cost, high-speed Internet connectivity, VPNs that use Internet for transport are often used to replace dedicated WAN services such as Frame Relay and point-to-point leased lines

IPSec and SSL can be used to encrypt data over a VPN tunnel

## Container-Based Virtualization <a name="CONBAS"></a> ([Back to Index](#INDEX4))

Container-Based Virtualization is an application virtualization mechanism that is similiar to a VM. Containers rely on a containerization engine - similiar to hypervisor - to configure/provision the virtual environment. A container bundles the binary files and libraries necessary to run the main app

Additional resources such as config data and storage resources can be mapped into the container at runtime. Containers share the operating kernel with the rest of the processes on the host - the container itself is isolated

## Review Questions <a name="REV4"></a> ([Back to Index](#INDEX4))

<ins>Review Question 1</ins>

Which of the following hypervisors can run without an underlying OS?

1. Only Type 1
2. Only Type 2
3. Both Type 1 and Type 2
4. Neither Type 1 and Type 2

<details><summary>Review Question 1 Answer</summary>
<p>
	
The answer is __1__

Explanation:

Hypervisor is responsible for facilitating the interaction between physical and virtualized hardware. T1 are implemented directly on the physical hardware without an OS. T2 runs as a privilege app on an underlying OS

</p>
</details>

<ins>Review Question 2</ins>

Which of the following is a network virtualization technology that enables a router to create multiple, distinct routing tables?

1. vSwitch
2. VRF
3. VLAN
4. VPN

<details><summary>Review Question 2 Answer</summary>
<p>
	
The answer is __2__

Explanation:

VPN Routing and Forwarding (VRF) is a network virtualization mechanism that is used to maintain multiple independent routing tables on a single router. When VRF is used, the same IP addressing scheme can be applied to different routing tables on the same router. VRF can be used to create numerous VPNs that will use the same infrastructure and same addressing scheme without causing interference among other instances

</p>
</details>

<ins>Review Question 3</ins>

Which of the following statements is correct regarding containers and VMs?

1. VMs are isolated from one another whereas containers are not
2. VMs require a hypervisor whereas containers do not
3. VMs share bins and libraries whereas containers do not
4. VMs can have dedicated resources whereas containers cannot

<details><summary>Review Question 3 Answer</summary>
<p>
	
The answer is __2__

Explanation:

VMs require a hypervisor. A hypervisor is computer software, firmware or hardware that runs one or more VMs

</p>
</details>

</p>
</details>

<details><summary>Module 5 - Switching and Network Access</summary>
<p>

# Table of Contents <a name="INDEX5"></a>

1. [Summary](#SUMSWITCH)
2. [Understanding Switching Fundamentals](#SWITCHFUN)
3. [Layer 2 Switches](#L2SWITCH)
4. [Layer 2 Frame Forwarding](#L2FORWARD)
5. [Multilayer Switch Forwarding](#MUTLIFORWARD)
6. [Switch Physical Interface Configuration](#SPIG)
7. [Access Ports](#ACCPORTS)
8. [Trunk Ports](#TRUNKPORTS)
9. [Understanding and Configuring DTP](#CONFDTP)
10. [Understanding VLANs](#UNDVLAN)
11. [Understanding the Voice VLAN](#VOICEV)

![](/images/network6.jpg)

## Summary <a name="SUMSWITCH"></a> ([Back to Index](#INDEX5))

![](/images/Module%205/96.png)

Switches are responsible for switching frames by using a MAC address. When a switch receives a frame, the switch adds the source MAC to the CAM table if the address does not already exist so the switch knows to the port which frames are destined for that address should be sent. Then, the switch will check the CAM table to determine whether the destination MAC address is listed. If yes, the switch directs the frame to the appropriate port. If not, the switch broadcasts the frame out all ports except the ingress port

When a switch is used to connected endpoint devices to a network, all devices connected to the switch are members of the same broadcast domain, but each port represents a different collision domain

VLANs can be configured to segment a network into multiple broadcast domains. VLANs can be local to a switch or they can extend throughout the topology by using features such as VTP and 802.1Q trunking

CDP and LLDP are supported on most Cisco devices and can be used to gather information about neighbouring devices. Some devices such as IP Phones can use CDP and LLDP to negotiate power delivery through mechanisms such as PoE

Switches also provide the ability to prevent loops by using a protocol such as STP and RSTP. Cisco's implementations of STP and RSTP offer performance optimization and reduced convergence times

In addition, Cisco enhancements to STP such as PortFast and BPDUGuard offer additional capabilities that can further reduce convergence times

EtherChannel can be used to bundle multiple physical interfaces into a single logical link. EtherChannel is typically used to increase the usable bandwidth between two devices, such as an access switch and a distribution switch and to provide redundancy

## Understanding Switching Fundamentals <a name="SWITCHFUN"></a> ([Back to Index](#INDEX5)) 

Both hubs and switches can be used to connect endpoint devices to a network. However, there are some major differences between how hubs and switches function

When a hub is used to connect endpoint devices to a network, all devices connected to the hub are members of the same broadcast domain, same collision domain and share the same bandwidth. When one device sends a packet, it affects the bandwidth that is available to all other devices. If more than one device sends a packet, collisions can occur and the packets will need to be re-sent

Hubs do NOT use processor logic to perform path determination or packet switching. When a hub receives data, it transmits it out all ports except the received port

When a switch is used to connect endpoint devices, all devices connected to the switch are members of the same broadcast domain but each port represents a different collision domain and receives a dedicated amount of bandwidth

Because each port represents a separate collision domain, multiple devices can send traffic at the same time without causing collisions. Switches also support full-duplex operation - data can be sent and received at the same time

When full-duplex mode is configured, data is sent from one pair of wires and received by a different pair of wires - this prevents collisions from occurring. By contrast, hubs support ONLY half-duplex operation meaning they cannot send and receive data at the same time

Switches are responsible for switching frames by using MAC addresses which are a physical address. When a switch receives the frame, the switch adds the source MAC to the switching table if it does not already exist. Then, the switch checks the table to determine whether the destination MAC is listed

If the destination MAC is listed, the switch will direct the frame to the appropriate port. If it is not listed, the switch will broadcast the frame out all ports except the port it was received on

Switches also have increased security options - they can filter traffic, limit the number of users who can access the switch, and create a logical segmentation of groups of hosts.

Switches also provide the ability to prevent loops by using a protocol such as STP or RSTP. There can be only one active path at any given time between any two endpoints on an Ethernet network. If multiple paths between the same two endpoints exist at the same time, switching loops can occur

STP activates and deactivates links dynamically to allow the network to respond to and reroute traffic around a failed link

## Layer 2 Switches <a name="L2SWITCH"></a> ([Back to Index](#INDEX5))

A Layer 2 switch operates at the Data Link Layer of the OSI model - equivalent to the Network Access Layer of the TCP/IP model. When a device is described as operating at a particular layer of a networking model, it should be understood that the device actually operates at the specified layer and all lower layers

When a switch receives a stream of bits from the Physical Layer, it can verify that the entire data unit has arrived safely. In an Ethernet environment, a data unit at this level is referred to as a __FRAME__. If the entire frame has arrived, the switch can check the integrity of the data by performing a calculation on the received data and comparing the result to the __Frame Check Sequence__ included in the data - if the result does NOT match the FCS, the received data is considered corrupt and is discarded

If the frame has been verified, the switch can make a forwarding decision based on the destination MAC address contained in the frame's header. The switch first searches its __Content Addressable Memory (CAM)__ for an entry that matches - the CAM table provides a list of known hardware addresses and their associated ports on the switch

If the frame's destination MAC adderss is NOT FOUND, the switch forwards the frame out all ports except the ingress port.  If the frame's destination MAC address IS FOUND, the switch forwards the frame to the appropriate port. If the source MAC address does not have an entry, it will be recorded in the CAM table

When a device operates at a particular level of the TCP/IP model, it has access to the protocol information stored in the header and possibly the trailer of the received data unit. In the case of a Data Link Layer device, the device uses the data to make forwarding decisions and to verify the integrity but does not alter the frame

![](/images/Module%205/1.png)

## Layer 2 Frame Forwarding <a name="L2FORWARD"></a> ([Back to Index](#INDEX5))

When a Layer 2 switch forwards a network frame, it effectively copies the frame from a memory location on the ingress port to a memory location on the appropriate egress port - these memory locations are referred to as __QUEUES__

Every port is allocated a portion of system memory that is used for transmit and receive queues. Although frames are typically described as passing through a switch, in reality the data from the frame is COPIED from one memory location to another and then converted into the appropriate signal type for the tranmission media involved

For example, HostA constructs a network frame with its own MAC address as the source and the MAC of HostB as the destination. HostA then transmits the frame to a Layer 2 switch

When the switch receives the frame from HostA, it examines the source MAC to ensure that HostA is associated with the port on which the frame received the frame. The switch then examines the destination MAC of the frame to make a forwarding decision

If the destination MAC address is unknown, the switch forwards the frame out every other port effectively creating a copy of the frame in the transmit queue of every other egress port. When HostB responds with a frame for HostA, the switch associates the MAC of HostB with the port and copies the frame directly to the transmit queue of the port attached to HostA

![](/images/Module%205/2.png)

<ins>The CAM Table</ins>

The CAM Table is allocated from a designated portion of system memory in a Layer 2 switch - system memory is faster than other types of memory such as NVRAM so it can facilitate rapid searches and rapid manipulation

Because the CAM table is allocated a fixed amount of system memory, attempting to store more data than it can hold causes adverse behaviour

The CAM table is constructed dynamically as the switch receives frames from the network. It associates source MAC addresses from network frames with the ports it was received on. An entry is created for each source MAC address, its associated ingress port and the VLAN ID with the port

![](/images/Module%205/3.png)

<ins>Using the CAM Table</ins>

When a Layer 2 switch receives a frame on a port, the switch examines the source MAC address and creates an entry in its CAM table - an entry is retained in the CAM table for a period known as the AGING TIME

When the amount of time an entry has resided in the CAM table exceeds the aging time, the entry is marked as STALE - stale entries are ignored and ultimately removed from the CAM table if the switch does not receive another frame with the same source MAC, port ID and VLAN ID

A Layer 2 switch uses its CAM table to determine the appropriate egress interface for a network frame - the CAM table is indexed by the destination MAC address

A switch examines the destination MAC address of a received frame and searches the CAM table for a corresponding entry. If a matching entry is found, the switch forwards the frame to the corresponding port in the CAM table - the VLAN ID of the source and destination port MUST MATCH otherwise the switch does not directly forward it. If an entry is not found, the switch will flood the frame to all ports within the VLAN identified by the source port

![](/images/Module%205/4.png)

<ins>Configuring the CAM Table</ins>

You can issue the __show mac-address-table aging-time__ command to examine the value of the cam aging time - the default aging time depends on the hardware platform eg. the 3750 switch indicates a default aging time of 300 seconds

![](/images/Module%205/5.png)

You can issue the __mac-address-table aging-time__ command to modify the CAM table aging for every VLAN on a switch - the aging time of 0 disables the aging timer altogether meaning they become static and do NOT get removed from the table

You can use the __vlan__ keyword to modify the aging time for a specific vlan

You can use the __show mac-address-table__ command to examine the contents of the CAM table

![](/images/Module%205/6.png)

Alternatively, you can display specific information from the CAM table:

* __show mac-address-table interface__ displays MAC addresses learned on a specific interface
* __show mac-address-table vlan__ displays MAC addresses learned on ports with a specified VLAN
* __show mac-address-table address__ queries the CAM table for an entry matching a specific MAC 

![](/images/Module%205/7.png)

<ins>The TCAM Table</ins>

Cisco switches use TCAM tables to facilitate the processing of ACLs and QoS parameters. Like the CAM table, the TCAM table uses fast, system memory to mitigate delay caused by table queries. In addition, queries can be executed in parallel to further mitigate query-related delays to frame forwarding due to multiple TCAM tables

Unlike CAM tables, the TCAM table space is divided into application-centric and protocol-centric regions - the regions enabled the TCAM table space to store variable-length fields that are optimized for the data being stored

TCAM table regions also facilitate additional match options such as longest-match and first-match queries

![](/images/Module%205/8.png)

<ins>Modifying the CAM and TCAM Tables</ins>

On Workgroup Class Switches, CAM and TCAM table parameters CANNOT be diretly modified - these switches provide SDM templates to reallocate system resources in predefined configurations

SDM templates are designed to optimize the allocation of system resources for common workgroup switch use cases - recommended that admins explore design changes before considering the use of SDM templates to reconfigure CAM and TCAM resources beyond their defaults

![](/images/Module%205/9.png)

<ins>Switching Modes</ins>

There are four main types of switching modes:

1. Store-and-forward switching
2. Cut-through switching
3. Adaptive cut-through switching
4. FragmentFree switching

__Store-And-Forward Switching__

The switch receives the entire frame before forwarding the frame - the switch verifies that no cyclic redundancy check (CRC) errors are present in the frame. This helps prevent the forwarding of frames with errors. If a CRC error is detected, the frame is discarded or if the frame contains less than 64 bytes, the frame is also discarded - referred to as a RUNT

Because the entire frame MUST be received before it can be forwarded, it has a higher latency than other methods. Multilayer switches MUST use the store-and-forward method because the switch MUST receive the entire frame before Network Layer operations can be performed

![](/images/Module%205/10.png)

__Cut-Through Switching__

This method begins forwarding a frame AFTER the first six bytes - as soon as the frame's destination is received. The switch begins forwarding the frame before the frame is fully received which helps reduce latency

With this method, the frame is NOT checked for errors prior to being forwarded and frames containing errors will be forwarded

![](/images/Module%205/11.png)

__Adaptive Cut-Through Switching__

This method provides a balance between store-and-forward and cut-through switching. When this method is used, an ERROR THRESHOLD can be configured that enables the switch to take advantage of the low latency provided by cut-through switching until the configured error threshold is reached - at that point, the switch begins using the higher latency store-and-forward method

When the error rate falls below the configured threshold, the switch reverts to using the cut-through switching method

![](/images/Module%205/12.png)

__FragmentFree Switching__

Similiar to the cut-through switching method in that the switch does NOT have to receive the entire frame before forwarding. However, it waits until at least 64 bytes of the frame have been received before deciding whether to forward the frame - this allows the switch to check for collision fragments which should be detectable within the first 64 bytes

If the frame is NOT a collision fragment, the switch begins forwarding the frame to the destination

![](/images/Module%205/13.png)

## Multilayer Switch Forwarding <a name="MUTLIFORWARD"></a> ([Back to Index](#INDEX5))

A multilayer switch forwards network frames in a manner similiar to a Layer 2 switch. However, when a frame is received with a MAC that belongs to the switch, the switch uses its Routing Information Base (RIB) to make a Layer 3 forwarding decision based on the header fields of the packet encapsulated by the received frame

<ins>Example</ins>

Suppose HostA needs to send a packet to HostB. HostA will construct an IP packet with its own IP as the source and the IP of HostB as the destination. Because HostB is NOT in the same subnet, HostA MUST send the packet to its default gateway.

HostA will construct a network frame to encapsulate the IP packet. The network frame will use the MAC of HostA as the source and MAC of default gateway (DSW1) as the destination.

HostA transmits the frame to DSW1 which is a Layer 3 switch. Because the frame is addressed to DSW1, the switch de-encapsulates the IP packet and examines the destination IP. DSW1 will consult its RIB to make a forwarding decision

In this secnario, DSW1 will forward the packet to DSW2. DSW1 will construct a network frame with its own MAC as the source and the MAC of DSW2 as the destination. It will encapsulate the IP packet within that frame before forwarding the frame to DSW2

When DSW2 receives the frame, it will follow the same procedure that DSW1 followed. Because the frame is addressed to DSW2, it will de-encapsulate the IP packet and examine the destination IP. DSW2 will consult its RIB to make a forwarding decision. 

HostB is directly connected to DSW2 so DSW2 will encapsulate the packet in a new frame with its own MAC as the source and the MAC of HostB as the destination

![](/images/Module%205/14.png)

<ins>How Multilayer Switches Process Frames</ins>

When a multilayer switch processes frames (either L2 or L3), it MUST examine the integrity of the frame before making a forwarding decision

Network frames typically have some form of integrity check to ensure that they arrive uncorrupted after transmission. Ethernet frames use a CHECKSUM value stored in the FRAME TRAILER - the checksum value is calculated by using several input values including source and destination MAC addresses

If either the source MAC or destination MAC must be changed in the frame header before forwarding, the checksum MUST be recalculated. Changing frame header or trailer fields is commonly referred to as FRAME REWRITING and is necessary when a multilayer switch processes frames that require Layer 3 forwarding

On a multilayer switch, the Layer 3 forwarding process follows a series of simple steps. These steps are typically implemented in Application-Specific Integrated Circuits (ASICs) to minimize the processing delay

First, the Layer 2 checksum is calculated for the received frame and the value is compared to the checksum field in the frame trailer. If they match, the frame is considered intact and the Layer 3 checksum can be calculated

The Layer 3 checksum is calculated by using the source and destination address in the header. In the case of IP packets, the Layer 3 checksum calculation includes the source and destination IP addresses in the packet header. If the calculated checksum value is equal to the checksum value in the packet header, the switch considers the packet intact and uses the packet header information to make a forwarding decision

Once a forwarding decision is made, the multilayer switch performs a FRAME REWRITE. The switch decrements the packet TTL value by one and then encapsulates the packet in a new network frame. The new frame header uses the MAC address of the switch as the source MAC and the MAC of the next hop as destination

The switch then recalculates the frame checksum based on the new addressing and places this value in the checksum field in the frame trailer. The frame is then placed in the transmit queue of the appropriate egress port and sent to the next hop

![](/images/Module%205/15.png)

<ins>Layer 3 Switch Planes of Operation</ins>

Cisco routers and switches are divided into three logical planes of operation:

1. The Management Plane
2. The Control Plane
3. The Data Plane

__The Management Plane__

The management plane is responsible for processing packets that are destined to the Layer 3 address of the device such as SSH, SNMPv3 and Syslog traffic

__The Control Plane__

The control plane is responsible for the creation and maintenance of structures related to routing and forwarding. These functions are heavily dependent on the CPU and memory availability. Control plane traffic is generated by dynamic routing protocols, VTP and STP

__The Data Plane__

The data plane is responsible for traffic passing through the device. Traffic from the data plane consists primarily of user-generated traffic that is forwarded from one interface to another - referred to as transit traffic

In most network designs, data plane traffic makes up the majority of network traffic during normal operation - router and switch hardware such as SWITCHING FABRIC, ROUTE PROCESSOR MODULES and ASICs are optimized for the processing of data plane traffic

![](/images/Module%205/16.png)

## Switch Physical Interface Configuration <a name="SPIG"></a> ([Back to Index](#INDEX5))

A switch interface can operate in either full-duplex or half-duplex mode. Full-duplex devices can simultaneously send and receive data whereas half-duplex cannot transmit and receive at the same time

Sometimes, the type of device that is connected to a switch dictates the duplex mode that should be configured. If a __HUB__ is connected to a switch interface, that interface should be configured to operate in half-duplex mode. If a __HOST__ or __SWITCH__ is connected to a switch interface, that interface should be configured in full-duplex mode

To configure the duplex mode on an interface, you should issue the `duplex <full | half | auto>` command

Duplex mismatches can cause intermittent connectivity problems between devices. There are three main ways to avoid duplex mismatches:

1. Configure both sides of the connection to full-duplex mode
2. Configure both sides of the connection to half-duplex mode
3. Configure both sides of the connection to auto-negotiate

The duplex-auto command configures the interface to autonegotiate the duplex settings. Auto-negotiation is available only for devices that support either the IEEE 802.3u standard or the 802.3z standard

The 802.3u standard allows compliant devices to automatically communicate port speed and duplex capabilities over a 10Mb or 100Mb connection. The 802.3z standard allows gigabit devices to automatically communicate similiar information

![](/images/Module%205/21.png)

<ins>Configuring Interface Speed</ins>

Cisco switch interfaces support multiple interface speeds:

* 10Mbps
* 100Mbps
* 1000Mbps

To configure the speed on an interface, use the `speed` command. The syntax of the speed command is `speed <10 | 100 | 1000 | auto>`. The speed values are measured in Mbps

When a switch port is configured for a speed or a duplex mode that the connected NIC cannot support, the NIC will lose connectivity

![](/images/Module%205/18.png)

<ins>Verifying Basic Switch Configuration</ins>

After configuring a switch, you can verify the configuration by using a combination of show commands

__The show interfaces Command__

You can issue the __show interfaces__ command to view infomation about the interfaces that are configured on a switch. The types of information that can be viewed by issuing the show interfaces command include:

* Status of interfaces
* IP address assigned to interfaces
* Speed configured on interfaces
* How many packets have been sent and received

Additionally, you can view counts of how many times certain errors such as CRC errors have occurred on the interface

The syntax of the show interfaces command is `show interfaces <type-number>` - the type and number parameters are optional. Using this syntax, you should issue the show interfaces f0/1 command to view information about interface FastEthernet0/1

![](/images/Module%205/19.png)

__The show running-config Command__

The __show running-config__ command is a useful tool for verifying and troubleshooting configurations. You can issue the __show running-config__ command on a switch to view information about the current running-config. It will show:

* Configuration information for all interfaces on the switch
* Other configurable options such as VLAN info, access restrictions, banner messages and host name information

![](/images/Module%205/20.png)

## Access Ports <a name="ACCPORTS"></a> ([Back to Index](#INDEX5))

An access port carries traffic for only ONE VLAN. An access port is usually connected to a single workstation or server. If an IP Phone is connected, you can configure an access port to carry traffic from one DATA VLAN and one VOICE VLAN

![](/images/Module%205/22.png)

<ins>Configuring Access Ports</ins>

To configure a switch port as an access port, you should issue the `switchport mode access` command

All access ports belong to VLAN 1 by default. To configure an access port to belong to a different VLAN, issue the `switchport access vlan <number>` command

A VLAN Management Policy Server (VPS) can be used to dynamically map MAC addresses to VLANs. To configure a switch to use a VMPS, issue the `switchport access vlan dynamic` command

![](/images/Module%205/23.png)

<ins>Verifying Access Ports</ins>

To verify whether a port is an access port or a trunk port, issue the `show interfaces <int> switchport` command. In the following example, the F0/1 interface is configured for dynamic auto mode and has negotiated to become an access port

![](/images/Module%205/24.png)

The port on the other end MUST be configured for dynamic auto or access mode. If the port at the other end of the link were set to dynamic desirable or trunk mode, F0/1 would become a trunk port

<ins>Verifying VLAN Membership</ins>

Use the `show vlan` command or the `show vlan brief` command to verify access ports belong to VLANs. In the sample below, the F0/1 port belongs to VLAN1, F0/2 and F0/3 belong to VLAN2 and no ports are in VLAN3

![](/images/Module%205/25.png)

## Trunk Ports <a name="TRUNKPORTS"></a> ([Back to Index](#INDEX5))

To enable a switch port to carry traffic from multiple VLANs, you MUST enable trunking on tthe port. A trunk port typically carries traffic between switches or between a switch and a router. When trunking is enabled on a port, the trunk port carries traffic from ALL VLANs by default

![](/images/Module%205/26.png)

<ins>Trunk Encapsulation Methods</ins>

To identify the VLAN to which a frame belongs, a TAG is added to the frame by using a trunk encapsulation method. There are two encapsulation methods that can be used to TAG VLAN traffic:

1. Inter-Switch Link (ISL)
2. 802.1Q

#### Inter-Switch Link

ISL is a Cisco proprietary trunking protocol that encapsulates each frame inside a 26-byte ISL header and a 4 byte CRC header. ISL is NOT supported on some of the newer Cisco switches - they support only 802.1Q standard. ISL encapsulation extends the maximum length of an Ethernet frame from 1518 bytes to 1548 bytes

#### 802.1Q

802.1Q is a standard-based trunking protocol developed by the IEEE. Rather than encapsulate each frame inside an 802.1Q header and trailer, 802.1Q inserts a 4-byte VLAN field into the frame's existing Ethernet header and does NOT encapsulate the original frame. 802.1Q encapsulation extends the maximum length of an Ethernet frame from 1518 bytes to 1522 bytes

In addition, 802.1Q does provide support for a native VLAN whereas ISL does NOT. Each 802.1Q trunk port has exactly one native VLAN - by default, 802.1Q trunk ports use VLAN 1 as the native VLAN

-----------------------------------------------------------------------------------

Traffic from the native VLAN is NOT tagged. A switch will NOT insert the VLAN field into the Ethernet header of frames that belong to the native VLAN. The destination switch will recognize that any untagged frames belong to the native VLAN. Because native VLAN frames are NOT tagged, these frames can also be understood by devices that do not support 802.1Q trunking

The 802.1Q encapsulation type can support multiple spanning trees and supports up to 4096 individual VLANs

When configuring VLANs across multiple switches, it is important that the same VLAN ID be configured as the native VLAN for each switch in the topology. Configuring different native VLANs on switches in the same topology can result in a native VLAN mismatch when untagged traffic from one switch is sent to another

A native VLAN mismatch can cause traffic that is intended for the native VLAN to be sent to an incorrect native VLAN on another switch or can cause CDP errors on switch ports

In addition, all of the following MUST MATCH on each end of a trunk link:

* The native VLAN ID
* The trunking mode
* The trunking encapsulation method
* The VLAN IDs that are allowed on the trunk


![](/images/Module%205/27.png)

<ins>Configuring Trunk Ports</ins>

Modern Cisco devices and modern versions of IOS allow the configuration of trunk ports on:

* Ethernet
* FastEthernet
* GigabitEthernet

The availability of some trunking features can depend on the device model. Some older devices might not support trunking over 10Mbps links

To configure a switch port as a trunk port, you MUST first set the __trunk encapsulation method__ by issuing the `switchport trunk encapsulation <dot1q | isl | negotiate>` command

The negotiate keyword configures the switch to negotiate the trunking method with the switch at the other end of the trunk link. The trunking methods MUST be the same on both ends of the trunk link

After you have configured the trunk encapsulation method, you can configure the switch port for trunking. To configure a switch port as a permanent trunking port, issue the `switchport mode trunk` command

You can change the native VLAN for an 802.1Q trunk port by issuing the `switchport trunk native vlan <number>` command. Native VLAN MUST match on both sides of the trunk link or spanning tree loops can occur

![](/images/Module%205/28.png)

<ins>Verifying Trunk Ports</ins>

In the sample output below, the F0/1 interface is configured for dynamic desirable mode and has negotiated to become a trunk. The port at the other end MUST be configured for dynamic auto, dynamic desirable or trunk mode. If the port at the other end was set to access mode, F0/1 would become an access port

In addition, the F0/1 interface has negotiated to use IEEE 802.1Q encapsulation. If the other end had been configured for ISL, F0/1 would also have used ISL. If the other end had been configured to negotiate encapsulation, each switch would negotiate to use the default for that model

![](/images/Module%205/29.png)

Can also verify that a port has been configured for trunking via issuing the `show interfaces <interface> trunk` command. This command displays information similiar to that displayed via the `show interfaces switchport` command but it also displays the VLANs that are allowed on the trunk. By default, traffic from ALL VLANs are allowed

![](/images/Module%205/30.png)

## Understanding and Configuring DTP <a name="CONFDTP"></a> ([Back to Index](#INDEX5))

You can configure a switch port to use Dynamic Trunking Protocol (DTP) to negotiate whether the port should become access or trunk

The `switchport mode <access | trunk | dynamic desirable | dynamic auto>` command configures the DTP mode for a switch port. There are two dynamic modes of operation for a switch port:

1. `auto` - operates in access mode unless the neighbouring interface actively negotiates to operate as a trunk
2. `desirable` - operates in access mode unless it can actively negotiate a trunk connection with a neighbouring interface

Because a switch port in AUTO mode does NOT actively negotiate to operate in trunk mode, it will form a trunk link only if negotiations are initiated by the neighbouring interface. A neighbouring interface will initiate negotiations ONLY if it is configured to operate in trunk mode or desirable mode

By contrast, a switch port in desirable mode will actively negotiate to operate in trunk mode and will form a trunk link with a neighbouring port that is configured to operate in trunk, desirable or auto mode

The default dynamic mode is dependent on the hardware platform. In general, departmental switches default to auto mode whereas backbone level switches default to desirable mode

You can statically configure a port to operate in access mode or trunk mode. Issuing the `switchport mode access` command will place the switch into PERMANENT access mode - it will never become a trunk port. Issuing the `switchport mode trunk` command will place the switch into PERMANENT trunk mode - if the other end is configured as a trunk port or dynamic auto/desirable, it will become a trunk link

Issuing the `switchport nonegotiate` command will disable DTP for the port. A port set to nonegotiate will NOT participate in DTP negotiation, nor will the port send DTP frames

Cisco recommends that you set BOTH SIDES of a trunk link to dynamic desirable when using DTP. When trunking to a non-Cisco device, you should MANUALLY configure the switch port for trunk mode

![](/images/Module%205/31.png)

## Understanding VLANs <a name="UNDVLAN"></a> ([Back to Index](#INDEX5))

To understand the usefulness of VLANs, you need to know how a LAN works. A __LAN__ is a set of devices in a single broadcast domain. A broadcast domain is a network segment where ALL devices receive a copy of a broadcast sent out. If a broadcast domain contains 100 devices, all 100 devices will receive a copy of the broadcast

Routers, which separrate one LAN from another, do NOT forward broadcasts. Each interface of a router is a separate broadcast domain. If a device that is connected to one of the router's interfaces sends a broadcast packet, it does NOT get forwarded

You do NOT have to use a router to separate broadcast domains - you can also use a switch to separate broadcast domains

Switches do NOT separate broadcast domains by default. All ports on the switch are part of the same broadcast domain. When a switch receives a broadcast, it forwards the broadcast out ALL ports except the port that originated the broadcast. To separate broadcast domains using a switch, you MUST use VLANs

VLANs are used to create separate LANs on the same switch. This means the switch maintains a separate bridging table for each VLAN

For example, the switches on the LAN below are located in separate buildings. Instead of segmenting the network by building, you can segment the network by department - put all Sales PCs into VLAN10 and all Admin PCs into VLAN20

![](/images/Module%205/32.png)

Broadcasts from a VLAN remain on that VLAN. Broadcasts are NOT forwarded to any other VLANs that are configured on the switch. There are two broadcast domains - VLAN 10 and VLAN 20

<ins>What Do VLANs Do?</ins>

VLANs provide many benefits. Network segmentation allows you to separate hosts into logical groups for easier administration and troubleshooting. VLANs also reduce the number of broadcasts that are sent and received across the network - reduces overhead for all devices because fewer broadcasts must be processed by switches/hosts

Traffic remains local to the VLAN unless routed by a router or Layer 3 switch which increases security. You can prevent traffic from passing from one VLAN to another by implementing ACLs or by preventing routing between the two VLANs - routing between two VLANs is called interVLAN routing

Some Cisco switches support the creation of VOICE VLANs which are used to keep voice traffic separate from data traffic. Additionally, different Quality of Service (QoS) and security policies can be maintained for each VLAN, giving administrators more granular control over the network

![](/images/Module%205/33.png)

<ins>VLANs and IP Addressing</ins>

In the diagram below, all of the devices within the network on the left reside in the same subnet. When VLANs are used, as shown in the network on the right, you should allocate an IP subnet for EACH VLAN

![](/images/Module%205/34.png)

To allow VLANs to communicate with one another, a router MUST use the same method it uses to allow two LANs to communicate with one another - it MUST route the packets between the networks

As stated earlier, routing packets between VLANs is called interVLAN routing. InterVLAN routing is performed by a router or a Layer 3 switch. This can be done by creating static routes or by using a dynamic routing protocol such as OSPF or EIGRP

There are additional design considerations that you should take into account when you need to allocate IP ranges. To facilitate route summarization, the subnets used by the VLANs should be contiguous. If you plan to use a routing protocol that does NOT support VLSM, you should ensure that the subnet masks are similiar

<ins>Creating and Configuring VLANs</ins>

To create a VLAN on a switch, issue the `vlan <number>` command. The number parameter can be from 1 to 4094. VLANs 1002 through 1005 are RESERVED for Token Ring and Fiber Distributed Data Interface (FDDI)

Two hidden VLANs (0 and 4095) are RESERVED for system use - these cannot be seen or deleted

Issuing the `vlan <number>` command will place the switch into VLAN config mode. VLAN config commands are executed immediately in VLAN config mode. However, the configuration changes do NOT take effect until the user exist VLAN config mode

A newly created VLAN will be given the name VLANxxxx where xxxx is the four digit number. To change the VLAN name, issue the `name <name>` command. The name of the VLAN can be up to 32 characters in length

To remove a VLAN from the VLAN database, issue the `no vlan <number>` command

You can assign an IP address to a VLAN which allows devices on the VLAN to be able to ping the switch. In addition, you can manage the switch by connecting to this IP over Telnet or SSH

To configure a VLAN with an IP, first enter interface configuration mode for the VLAN - done via `interface vlan <id>` command. Then, you can configure the VLAN interface with an IP similiar to a normal interface

You can verify the IP has been assigned to the VLAN via the `show interfaces vlan <id>` command

![](/images/Module%205/35.png)

<ins>Verifying LANs</ins>

To display information about ALL VLANs configured on a switch, issue the `show vlan` command - displays VLAN name, status, ports that belong to each VLAN and several VLAN parameters

To verify the creation of a new VLAN, issue the `do show vlan` command from ANY configuration mode

To display a brief summary of VLANs configured on the switch, issue the `show vlan brief` command - displays VLAN name, status, ports that belong to each VLAN but does NOT display VLAN parameters

To display information about a specific VLAN, issue the `show vlan id <id>` command. Alternatively, specify the VLAN by name by issuing the `show vlan name <name>` command

![](/images/Module%205/36.png)

## Understanding the Voice VLAN <a name="VOICEV"></a> ([Back to Index](#INDEX5))

For performance purposes, voice traffic is typically separated from data traffic on a LAN. Newer Cisco switches support the creation of a voice-specific VLAN that is preconfigured to support comms with Cisco IP Phones over a voice network

Voice traffic from an IP phone transits a VLAN with a default Layer 3 IP precedence value of 5 and an IEEE 802.1Q priority of 5. Several other characteristics of the voice VLAN that make it unique in its configuration

CDP MUST be enabled on the interface that is being configured on the voice VLAN - it is enabled by default. If CDP is disabled, the switch will NOT be able to send configuration information to the Cisco IP Phone connected to the port

The voice VLAN should be configured ONLY on access ports. Trunk ports CAN be configured with the voice VLAN but the configuration is NOT supported and will NOT produce results

When the voice VLAN is configured on a port, PortFast is automatically enabled for the port. Removing the voice VLAN does NOT automatically disabled PortFast - you might need to manually disable PortFast if you repurpose the port

Cisco recommends enabling QoS on the switch voice VLAN port if auto QoS is NOT operating on the switch. You can enable QoS on a switch port by issuing the trust device cisco-phone command

Ports that are configured to operate on a voice VLAN can support BOTH port security and 802.1X authentication. If port security is enabled on the switch's access VLAN, dynamic port security will automatically become enabled on the voice VLAN

You cannot statically configure secure MAC addresses on a voice port. Cisco recommends configuring a maximum of TWO allowed MAC addresses on a voice port. Both IP phone and any device that is connected to the access port on the IP phone have MAC addresses

<ins>Configuring the Voice VLAN</ins>

If QoS and CDP are enabled on a switch port, there are only TWO commands that are required to enable the voice VLAN - `switchport mode access` and `switchport voice vlan`

The `switchport mode access` command puts the port into STATIC ACCESS mode. The effect of the `switchport voice vlan` command depends on the value or keyword that follows the vlan keyword - syntax of the command is `switchport voice vlan <id | dot1p | none | untagged>`

If you configure the ID value when you issue the switchport voice vlan command, traffic from the connected IP phone will be forwarded on 802.1Q frames that are tagged with the VLAN ID

It is possible to configure the switchport voice vlan command so that voice traffic is placed in the access VLAN instead. Issuing the `switchport voice vlan dot1p` command causes the IP phone to use 802.1p tagging with a priority of 5 instead of 802.1Q - this causes voice traffic to transit the native VLAN

Configuring the `switchport voice vlan none` command on a switch port causes the IP phone to behave as if it were NOT connected to a Cisco switch. IP Phone does NOT download its configuration from the switch and uses its own configuration. Traffic from the IP phone traverses the access VLAN

Configuring the `switchport voice vlan untagged` command on a switch port causes the IP phone to send untagged voice traffic which traverse the access VLAN. The same behaviour occurs if the switchport voice vlan command is NOT configured on the port. Same method that the IP phone would use if the switchport voice vlan command were NOT configured

























