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
hostname <name> | sets hostname for device
copy <from> <to> | enable mode command that copies files from one location to another
copy running-config startup-config | enable mode command that saves active config to startup
copy startup-config running-config | enable mode command that merges startup config with current active config in RAM
write erase & erase startup config | enable mode command that deletes startup config
ip address <ip> <mask> | assigns IP address and subnet mask
shutdown & no shutdown | interface config mode command that shutdowns or brings up interface
ip default-gateway <ip> | sets default gateway
show running-config | enable mode command that displays current configuration
description <string> | config interface command to describe the interface
show running-config <interface> | enable mode command to display running config for interface
show ip interface <number> | displays usability status of interfaces configured for IP
ip name-server <serverIP> | configure mode command that sets IP address of DNS servers