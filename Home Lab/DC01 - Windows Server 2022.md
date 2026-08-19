# DC01 - Windows Server 2022

## Purpose
DC01 is the main infrastructure server for the home lab. It provides centralized identity, DNS, and DHCP services for the simulated small office network.

## Roles Installed
- [[Active Directory Domain Services]]
- [[DNS Server]]
- [[DHCP Server]]

## Network Configuration
- Hostname: DC01
- Domain: [[corp.local]]
- IP Address: 192.168.88.10
- Subnet Mask: 255.255.255.0
- Default Gateway: None
- Preferred DNS: 192.168.88.10

## Why This Server Uses a Static IP
DC01 provides core network services. If its IP address changed, clients may fail to locate DNS, the domain controller, or DHCP services.

## Why DNS Points to Itself
Active Directory depends heavily on DNS. Since DC01 hosts DNS for the domain, it uses itself as the preferred DNS server.

## Connected Network
- [[VMnet2 - Office LAN]]
  
  
  [[Projects and Learning]]

- 