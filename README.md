# Enterprise Multi-Branch Network

> A professionally documented enterprise network built using Cisco Packet Tracer.

![Overview](images/overview.png)

---

# Overview

This project simulates a modern enterprise network consisting of four interconnected locations:

- Headquarters (Kuala Lumpur)
- Penang Branch
- Johor Bahru Branch
- Kota Kinabalu Branch

Originally developed as a university project, this network has evolved into **Project Zero** — an enterprise-grade networking portfolio focused on security hardening, scalable routing, standardized infrastructure, and realistic enterprise network design.

---

# Current Release

**Latest Stable Release:** `v0.5.0`

Current development is focused on **v0.6.0**, introducing branch security standardization, enterprise optimization, and infrastructure enhancements.

---

# Features

- Multi-site enterprise topology
- Department-based VLAN segmentation
- Layer 3 inter-VLAN routing
- Dynamic routing using OSPF
- Secure SSH device management
- Management access restricted using ACLs
- Department-based Access Control Lists (ACLs)
- Wireless network isolation
- IoT network isolation
- Port Security on access ports
- BPDU Guard protection
- Native VLAN hardening
- Parking VLAN for unused ports
- Disabled Dynamic Trunking Protocol (DTP)
- Standardized enterprise naming conventions
- Version-controlled development using Git & GitHub
- Private IPv4 addressing
- Centralized DHCP services
- Centralized DNS services
- Centralized Syslog logging
- Centralized NTP time synchronization
- Centralized TFTP configuration backups

---

# Security Features

- SSH Version 2 management
- Local administrator authentication
- Encrypted device passwords
- Management-plane protection using VTY ACLs
- Department isolation using Extended ACLs
- Wireless client isolation
- IoT network isolation
- Port Security with Sticky MAC learning
- BPDU Guard on user access ports
- Dedicated Parking VLAN for unused interfaces
- Native VLAN hardening
- Disabled Dynamic Trunking Protocol (DTP)
- Dynamic routing with OSPF replacing static routing

---

# Enterprise Services

- DHCP
- DNS
- Syslog
- NTP
- HTTP
- TFTP

---

# Network Overview

## Enterprise WAN

![Enterprise Overview](images/overview.png)

---

## Headquarters

![Headquarters](images/headquarters.png)

---

## Penang Branch

![Penang](images/penang.png)

---

## Johor Bahru Branch

![Johor](images/johor.png)

---

## Kota Kinabalu Branch

![Kota Kinabalu](images/kota.png)

---

# Project Structure

```text
enterprise-multi-branch-network/

├── images/
│   ├── overview.png
│   ├── headquarters.png
│   ├── penang.png
│   ├── johor.png
│   └── kota.png
│
├── packet-tracer/
│   ├── enterprise-network-v1.0-original.pkt
│   └── enterprise-network-v0.5.0.pkt
│
└── README.md
```

---

# Technologies

- Cisco Packet Tracer 9
- Cisco IOS
- VLANs
- IEEE 802.1Q Trunking
- Inter-VLAN Routing
- OSPF
- Extended ACLs
- SSH
- DHCP
- DNS
- Syslog
- NTP
- TFTP
- Spanning Tree Protocol (STP)
- Port Security
- Git
- GitHub

---

# Development Roadmap

## ✅ v0.1.0

- Enterprise topology redesign
- Professional branch layouts
- Standardized device naming
- Improved visual consistency
- GitHub repository
- Project documentation

---

## ✅ v0.2.0

- Headquarters security hardening
- SSH management
- Local user authentication
- Port Security
- BPDU Guard
- Parking VLAN implementation
- Native VLAN hardening
- Disabled Dynamic Trunking Protocol (DTP)

---

## ✅ v0.3.0

- Private IPv4 addressing
- Centralized DHCP deployment
- DNS deployment
- Syslog deployment
- NTP deployment
- HTTP server
- TFTP backup server
- Enterprise infrastructure services

---

## ✅ v0.4.0

- Enterprise-wide OSPF deployment
- Migration from static routing to dynamic routing
- Dynamic route advertisement between all sites
- OSPF Area 0 backbone implementation
- Automatic route learning across the WAN
- Removal of legacy enterprise static routes
- Full enterprise WAN connectivity validation

---

## ✅ v0.5.0

- Enterprise-wide Access Control Lists (ACLs)
- Department isolation policies
- Wireless network isolation
- IoT network isolation
- Secure SSH deployment across all Layer 3 devices
- Management access restricted to IT and Management VLANs
- Standardized router and Layer 3 switch security baseline
- Enterprise credential standardization
- Full enterprise security validation

---

## 🚧 Planned (v0.6.0+)

- Branch security hardening
- Infrastructure optimization
- Enterprise monitoring improvements
- Configuration cleanup and optimization
- Additional ACL enhancements
- High availability features
- Final enterprise validation

---

# Version History

| Version | Description |
|----------|-------------|
| v0.1.0 | Enterprise topology redesign |
| v0.2.0 | Headquarters security hardening |
| v0.3.0 | Enterprise infrastructure services deployment |
| v0.4.0 | Migrated enterprise WAN from static routing to OSPF |
| v0.5.0 | Enterprise security hardening with ACLs and secure SSH management |

---

# Author

**Cezar Abou Al Mouna**

Cybersecurity Student

GitHub: https://github.com/CezarSecurity