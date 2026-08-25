# Network Summary

## Enterprise Overview

Project Zero is a four-site enterprise network consisting of a centralized headquarters and three geographically distributed branch offices.

---

## Infrastructure

### Headquarters

- 1 WAN Router
- 1 Layer 3 Distribution Switch
- 8 Access Switches
- Centralized Enterprise Servers

### Penang Branch

- 1 WAN Router
- 1 Layer 3 Distribution Switch
- Department VLANs:
  - Customer
  - Technical Services
  - Sales
  - Logistics
  - Data Center
  - Wireless
  - IoT
  - Executive

### Johor Bahru Branch

- 1 WAN Router
- 1 Layer 3 Distribution Switch
- Department VLANs:
  - Operations
  - Corporate
  - Research
  - Procurement
  - Systems
  - Wireless
  - IoT
  - Servers

### Kota Kinabalu Branch

- 1 WAN Router
- 1 Layer 3 Distribution Switch
- Department VLANs:
  - Strategy
  - Accounts
  - Talent
  - Technical Support
  - Data Center
  - Wireless
  - Smart IoT
  - Client Success

---

## Routing

- OSPF Area 0
- Dynamic routing
- Inter-VLAN routing using Layer 3 distribution switches

---

## Security

- SSH Version 2
- Local administrator authentication
- Extended Access Control Lists (ACLs)
- VTY Management ACLs
- Port Security
- BPDU Guard
- Native VLAN hardening
- Parking VLANs
- Disabled Dynamic Trunking Protocol (DTP)

---

## Enterprise Services

All core services are hosted at headquarters.

- DHCP
- DNS
- HTTP
- Syslog
- NTP
- TFTP

---

## Current Status

Current Stable Release: **v0.6.0**

Project Zero successfully demonstrates a secure multi-site enterprise network featuring dynamic routing, Layer 3 switching, VLAN segmentation, centralized infrastructure services, and enterprise security controls.