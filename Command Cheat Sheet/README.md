# Cisco Commands Cheat Sheet

## List of common Cisco CCNA IOS Commands

# Table of Contents <a name="INDEX"></a>

1. [Basic Configuration Commands](#BASIC)
2. [Troubleshooting Commands](#TROUBLESHOOT)
3. [Routing and VLAN Commands](#ROUTEVLAN)
4. [DHCP Commands](#DHCP)
5. [Security Commands](#SECURITY)
6. [Monitoring and Logging Commands](#LOGGING)

![](/images/network5.jpg)

## Basic Configuration Commands <a name="BASIC"></a> ([Back to Index](#INDEX))

Command | Purpose
------------ | -------------
enable | Logs into enable/user exec/privileged mode
configure terminal | logs you into configuration mode
interface fastethernet/number | enters interface configuration mode for specified interface
reload | exec mode command that reboots
hostname `<name>` | sets hostname for device
copy `<from> <to>` | enable mode command that copies files from one location to another
copy running-config startup-config | enable mode command that saves active config to startup
copy startup-config running-config | enable mode command that merges startup config with current active config in RAM
write erase & erase startup config | enable mode command that deletes startup config
ip address `<ip> <mask` | assigns IP address and subnet mask
shutdown & no shutdown | interface config mode command that shutdowns or brings up interface
ip default-gateway `<ip>` | sets default gateway
show running-config | enable mode command that displays current configuration
description `<string>` | config interface command to describe the interface
show running-config `<interface>` | enable mode command to display running config for interface
show ip interface `<number>` | displays usability status of interfaces configured for IP
ip name-server `<serverIP>` | configure mode command that sets IP address of DNS servers

## Troubleshooting Commands <a name="TROUBLESHOOT"></a> ([Back to Index](#INDEX))

Command | Purpose
------------ | -------------
ping `<hostname>/<system-address>` | used in enable mode to diagnose basic connectivity
speed `<10/100/1000/auto>`  | interface mode command to manually set the speed
duplex `<auto/full/half>` | interface mode command to manually set duplex
cdp run & no cdp run | configuration mode command that enables or disables CDP
show mac address-table | displays MAC address table
show cdp | shows whether CDP is enabled globally
show cdp neighbors | lists summary information about each neighbour
show interfaces | displays detailed information about interface status, settings and counters
show interface status | displays interface line status
show interfaces switchport | displays config settings and current operationl status including VLAN trunking details
show interfaces trunk | lists information about current trunks and VLANs supported
show vlan & show vlan brief | lists each vlan and all interfaces assigned to that VLAN
show vtp status | lists current VTP status including current mode

## Routing and VLAN Commands <a name="ROUTEVLAN"></a> ([Back to Index](#INDEX))

Command | Purpose
------------ | -------------
ip route `<network> <mask>` | sets a static route in the IP routing table
router rip | enables RIP and places you in router config mode
network `<ip>` | in router config mode, associates a network with a RRIP routing process
version 2 | in router config mode, disables automatic summarization
no auto-summary | in router config mode, disables automatic summarization
passive-interface `<int>` | in router config mode, sets the interface to passive RIP mode
show ip rip database | displays content of RIP routing database
ip nat `<inside/outside>` | interface config mode command to designate that traffic originating from/destined to the interface is subject to NAT
ip nat inside source `<list/interface/overload>` | config mode command to establish dynamic source translation
ip nat inside source static `<localip/globalip>` | config mode command to establish a static translation between an inside local and inside global address
vlan | creates a VLAN and enters VLAN configuration mode
switchport access vlan | sets the VLAn that the interface belongs to
switchport trunk & encapsulation dot1q | specifies 802.1Q encapsulation on trunk link
switchport access | assigns this port to a VLAN 
vlan & vlan-id `<name>` | configures a specific VLAN name
switchport mode `<access/trunk>` | configure VLAN membership mode of a port
switchport trunk `<encapsulation dot1q>` | sets trunk characteristics when interface in trunking mode
encapsulation dot1q vlan-id | config mode command that defines matching criteria to map 802.1Q frames ingress on an interface

## DHCP Commands <a name="DHCP"></a> ([Back to Index](#INDEX))

Command | Purpose
------------ | -------------
ip address dhcp | config mode command to acquire an IP address via DHCP
ip dhcp pool name | config mode command to configure a DHCP address pool on a DHCP server
domain-name `<domain>` | DHCP pool config mode to specify domain name for DHCP client
network `<network-number> <mask>` | used in DHCP pool config mode to configure network number and mask for pool
ip dhcp excluded-address `<ip> <lastip>` | config mode command to specify IP addresses to not assign
ip helper-address `<address>` | interface config mode command to enable forwarding of UDP broadcasts 
default-router `<address>` | used in DHCP pool config mode to specify default router list for a client

## Security Commands <a name="SECURITY"></a> ([Back to Index](#INDEX))

Command | Purpose
------------ | -------------
password `<pass>` | lists password that is required if login is configured
username `<name>` password `<pass>` | global command that defines one username and password
enable password `<pass>` | config mode command that defines password
enable secret `<pass>` | config mode command that sets password for enable mode
service password-encryption | config mode command that encrypts all passwords
ip domain-name `<name>` | configures DNS domain name
crypto key generate rsa | config mode command that creates/stores keys for SSH
transport input `<telnet/ssh>` | used in vty line config mode and defines whether Telnet/SSH is allowed
access-list `<acl-number>` deny/permit source `<wildcard>` | config mode command that defines a standard IP access list
access-class | restricts incoming and outgoing connections between particular vty 
ip access-list `<standard/extended>` `<acl-name/acl-number>` | config mode command that defines an IP acess by name or number
permit source `<source/wildcard>` | used in ACL config mode to set conditions to allow packets to pass
deny source `source/wildcard>` | used in ACL config mode to set conditions to deny packets
ntp peer `<ip>` | used in global config mode to configure software clock to synchronize a peer
switchport port-security | used in interface config mode to enable port security
switchport port-security maximum maximum | insed in interface config mode to set maximum number of secure MAC addresses
switchport port-security mac-address `<mac>` | used in interface config mode to add a MAC to the list of secure MAC addresses
switchport port-security violation `<shutdown/restrict/protect>` | used in interface config mode to set action to be taken 
show port security `<interface>` | displays information about security options configured on interface

## Monitoring and Logging Commands <a name="LOGGING"></a> ([Back to Index](#INDEX))

Command | Purpose
------------ | -------------
logging `<ip>` | configures IP address of host that receives syslog messages
logging trap level | used in config mode to limit mesages that are logged to syslog servers
show logging | enable mode command that displays state of syslog 
terminal monitor | used in interface config mode to enable port security 
switchport port-security maximum maximum | enable mode command to send copy of all syslog messages to user who issues the command
