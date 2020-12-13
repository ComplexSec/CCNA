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

