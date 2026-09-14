# Enterprise Multi-Branch Network

> A professionally designed enterprise network built using Cisco Packet Tracer, demonstrating secure multi-site connectivity, Layer 3 switching, dynamic routing, and a mix of centralized and distributed infrastructure services.

![Version](https://img.shields.io/badge/Version-v1.0.0-blue)
![Routing](https://img.shields.io/badge/Routing-OSPF-success)
![License](https://img.shields.io/badge/License-MIT-orange)

---

# Project Highlights

- Four-site enterprise network with standardized device naming
- Dynamic routing using OSPF Area 0, including full management-subnet reachability
- Enterprise VLAN segmentation with per-site Extended ACLs
- Layer 2 hardening across every site: Port Security, BPDU Guard, DTP disabled, native VLAN protection
- Centralized SSH management, restricted to headquarters
- Full Layer 3 device configurations and technical documentation included

---

![Enterprise Overview](images/overview.png)

# Overview

Project Zero simulates a modern enterprise network consisting of four interconnected locations:

- Headquarters (Kuala Lumpur)
- Penang Branch
- Johor Bahru Branch
- Kota Kinabalu Branch

Originally developed as a university project, this network has evolved into an enterprise-grade networking portfolio focused on secure infrastructure design, dynamic routing, distributed and centralized services, and professional documentation.

---

# Current Release

**Latest Stable Release:** `v1.0.0`

---

# Features

Core networking and infrastructure capabilities:

- Multi-site enterprise topology with standardized device naming (`HQ-CORE-SW1`, `PG-RTR-01`, etc.)
- Layer 3 inter-VLAN routing
- OSPF dynamic routing across all sites and management subnets
- Department-based VLAN segmentation
- Private and enterprise-style IPv4 addressing, standardized per site
- Distributed DHCP (independent pools per site) and centralized DNS, HTTP, Syslog, NTP, TFTP
- Standardized interface descriptions and enterprise MOTD banner
- Version-controlled development using Git & GitHub

---

# Enterprise Services

Infrastructure services follow a centralized or distributed model depending on function.

| Service | Model                       | Purpose                                                      |
| ------- | --------------------------- | ------------------------------------------------------------ |
| DHCP    | Distributed per site        | Dynamic IP address assignment, local to each site's own infrastructure |
| DNS     | Centralized at headquarters | Internal name resolution                                     |
| HTTP    | Centralized at headquarters | Enterprise web services                                      |
| Syslog  | Centralized at headquarters | Centralized logging                                          |
| NTP     | Centralized at headquarters | Time synchronization                                         |
| TFTP    | Centralized at headquarters | Configuration backup                                         |

---

# Security Features

Project Zero implements layered security controls across every site:

- SSH Version 2 with local administrator authentication and encrypted passwords
- Centralized SSH management — administrative access is restricted to headquarters' IT and Management VLANs enterprise-wide
- Extended ACLs enforcing department, wireless, and IoT isolation, tailored to each site's most sensitive department
- Port Security with sticky MAC learning
- BPDU Guard
- Disabled Dynamic Trunking Protocol (DTP) on every trunk port
- Native VLAN hardening via a dedicated, unused VLAN
- Parking VLAN for unused, administratively shut down interfaces

---

# Network Overview

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
│   ├── HQ-CORE-SW1_running-config.txt
│   ├── HQ-RTR-01_running-config.txt
│   ├── PG-CORE-SW1_running-config.txt
│   ├── PG-RTR-01_running-config.txt
│   ├── JB-CORE-SW1_running-config.txt
│   ├── JB-RTR-01_running-config.txt
│   ├── KK-CORE-SW1_running-config.txt
│   └── KK-RTR-01_running-config.txt
│
├── docs/
│   ├── architecture.md
│   ├── ip-addressing.md
│   ├── network-summary.md
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
│   └── enterprise-network-v1.0.0.pkt
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
- Network Summary
- VLAN Design
- Routing Design
- Security Architecture
- Network Validation

---

# Device Configurations

The `configs/` directory contains the running configurations for all Layer 3 devices in the enterprise.

Included devices:

- HQ-CORE-SW1
- HQ-RTR-01
- PG-CORE-SW1
- PG-RTR-01
- JB-CORE-SW1
- JB-RTR-01
- KK-CORE-SW1
- KK-RTR-01

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

| Version |  Status  | Description                                                  |
| ------- | :------: | ------------------------------------------------------------ |
| v0.1.0  | Complete | Enterprise topology redesign                                 |
| v0.2.0  | Complete | Headquarters security hardening                              |
| v0.3.0  | Complete | Infrastructure services deployment                           |
| v0.4.0  | Complete | Enterprise-wide OSPF deployment                              |
| v0.5.0  | Complete | Enterprise security hardening                                |
| v0.6.0  | Complete | Infrastructure standardization                               |
| v0.7.0  | Complete | Documentation and repository enhancement                     |
| v1.0.0  | Complete | Branch addressing standardization, enterprise-wide Layer 2/3 security hardening, and full documentation refresh |

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