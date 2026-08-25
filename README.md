# Enterprise Multi-Branch Network

> A professionally designed enterprise network built using Cisco Packet Tracer, demonstrating secure multi-site connectivity, Layer 3 switching, dynamic routing, and centralized infrastructure services.

![Version](https://img.shields.io/badge/Version-v0.7.0-blue)
![Cisco Packet Tracer](https://img.shields.io/badge/Cisco-Packet%20Tracer-9.x-green)
![Routing](https://img.shields.io/badge/Routing-OSPF-success)
![License](https://img.shields.io/badge/License-MIT-orange)

---

# Project Highlights

- Four-site enterprise network
- Dynamic routing using OSPF Area 0
- Layer 3 inter-VLAN routing
- Enterprise VLAN segmentation
- Secure SSH device management
- Extended Access Control Lists (ACLs)
- DHCP, DNS, HTTP, Syslog, NTP and TFTP services
- Professional technical documentation
- Full Layer 3 device configurations included
- Version-controlled development using Git & GitHub

---

# Overview

Project Zero simulates a modern enterprise network consisting of four interconnected locations:

- Headquarters (Kuala Lumpur)
- Penang Branch
- Johor Bahru Branch
- Kota Kinabalu Branch

Originally developed as a university project, this network has evolved into an enterprise-grade networking portfolio focused on secure infrastructure design, dynamic routing, centralized services, and professional documentation.

---

# Current Release

**Latest Stable Release:** `v0.7.0`

Current development is focused on **v0.8.0**, introducing final optimization, production validation, and repository polish before the Version 1.0 release.

---

# Features

- Multi-site enterprise topology
- Layer 3 inter-VLAN routing
- OSPF dynamic routing
- Department-based VLAN segmentation
- Secure SSH management
- Management VTY ACLs
- Extended ACLs
- Wireless network isolation
- IoT network isolation
- Port Security
- Sticky MAC learning
- BPDU Guard
- Native VLAN hardening
- Parking VLAN implementation
- Disabled Dynamic Trunking Protocol (DTP)
- Enterprise MOTD banner
- Standardized interface descriptions
- Private IPv4 addressing
- Centralized DHCP
- Centralized DNS
- Centralized HTTP
- Centralized Syslog
- Centralized NTP
- Centralized TFTP

---

# Enterprise Services

The headquarters hosts the centralized infrastructure services.

| Service | Purpose |
|----------|---------|
| DHCP | Dynamic IP address assignment |
| DNS | Internal name resolution |
| HTTP | Enterprise web services |
| Syslog | Centralized logging |
| NTP | Time synchronization |
| TFTP | Configuration backup |

---

# Security Features

Project Zero implements layered security controls including:

- SSH Version 2
- Local administrator authentication
- Encrypted passwords
- Extended ACLs
- Management VTY ACLs
- Department isolation
- Wireless isolation
- IoT isolation
- Port Security
- Sticky MAC learning
- BPDU Guard
- Native VLAN hardening
- Parking VLANs
- Disabled Dynamic Trunking Protocol (DTP)

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

![Johor Bahru](images/johor.png)

---

## Kota Kinabalu Branch

![Kota Kinabalu](images/kota.png)

---

# Repository Structure

```text
enterprise-multi-branch-network/

├── configs/
│   ├── KL-RTR.txt
│   ├── KL-DIST.txt
│   ├── PNG-RTR.txt
│   ├── PNG-DIST.txt
│   ├── JB-RTR.txt
│   ├── JB-DIST.txt
│   ├── KOTA-RTR.txt
│   └── KOTA-DIST.txt
│
├── docs/
│   ├── architecture.md
│   ├── ip-addressing.md
│   ├── routing.md
│   ├── security.md
│   ├── validation.md
│   └── vlan-design.md
│
├── images/
│   ├── overview.png
│   ├── headquarters.png
│   ├── penang.png
│   ├── johor.png
│   └── kota.png
│
├── packet-tracer/
│   ├── enterprise-network-v1.0-original.pkt
│   └── enterprise-network-v0.7.0.pkt
│
├── .gitignore
├── CHANGELOG.md
├── LICENSE
└── README.md
```

---

# Documentation

Comprehensive technical documentation is available in the `docs/` directory.

- Enterprise Architecture
- IP Addressing Plan
- VLAN Design
- Routing Design
- Security Architecture
- Network Validation

---

# Device Configurations

The `configs/` directory contains the running configurations for all Layer 3 devices in the enterprise.

Included devices:

- KL-RTR
- KL-DIST
- PNG-RTR
- PNG-DIST
- JB-RTR
- JB-DIST
- KOTA-RTR
- KOTA-DIST

---

# Technologies

- Cisco Packet Tracer 9
- Cisco IOS
- VLANs
- IEEE 802.1Q
- Layer 3 Switching
- OSPF
- Extended ACLs
- SSH
- DHCP
- DNS
- HTTP
- Syslog
- NTP
- TFTP
- STP
- Port Security
- Git
- GitHub

---

# Development Roadmap

| Version | Status | Description |
|----------|:------:|-------------|
| v0.1.0 | Complete | Enterprise topology redesign |
| v0.2.0 | Complete | Headquarters security hardening |
| v0.3.0 | Complete | Infrastructure services deployment |
| v0.4.0 | Complete | Enterprise-wide OSPF deployment |
| v0.5.0 | Complete | Enterprise security hardening |
| v0.6.0 | Complete | Infrastructure standardization |
| v0.7.0 | Complete | Documentation and repository enhancement |
| v0.8.0 | In Progress | Final optimization and validation |
| v1.0.0 | Planned | Stable public release |

---

# Changelog

A complete project history is available in **CHANGELOG.md**.

---

# License

This project is licensed under the MIT License.

See **LICENSE** for details.

---

# Author

**Cezar Abou Al Mouna**

Cybersecurity Student

GitHub: https://github.com/CezarSecurity