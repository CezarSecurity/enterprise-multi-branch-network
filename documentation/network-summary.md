# Network Summary

## Enterprise Overview

Project Zero is a four-site enterprise network consisting of a centralized headquarters and three geographically distributed branch offices, using standardized device naming across all sites.

---

## Infrastructure

### Headquarters — HQ-CORE-SW1 / HQ-RTR-01

- 1 WAN Router
- 1 Layer 3 Distribution Switch
- 8 Access Switches
- Centralized Enterprise Servers

### Penang Branch — PG-CORE-SW1 / PG-RTR-01

- 1 WAN Router
- 1 Layer 3 Distribution Switch
- 6 Access Switches
- Department VLANs:
  - Customer
  - Technical Services
  - Sales
  - Logistics
  - Data Center (no active devices)
  - Wireless
  - IoT
  - Executive (static addressing)
  - Management (static addressing, separate address block)

### Johor Bahru Branch — JB-CORE-SW1 / JB-RTR-01

- 1 WAN Router
- 1 Layer 3 Distribution Switch
- 7 Access Switches
- Department VLANs:
  - Operations
  - Corporate
  - Research
  - Procurement
  - Systems
  - Wireless
  - IoT (no devices deployed)
  - Servers (no active devices)
  - Management (static addressing, separate address block)

### Kota Kinabalu Branch — KK-CORE-SW1 / KK-RTR-01

- 1 WAN Router
- 1 Layer 3 Distribution Switch
- Department VLANs:
  - Strategy
  - Accounts
  - Talent
  - Technical Support
  - Data Center (no active devices)
  - Wireless
  - Smart IoT (no devices deployed)
  - Client Success

No local management network — administered centrally from headquarters.

---

## Routing

- OSPF Area 0
- Dynamic routing across all sites, including branch management subnets
- Inter-VLAN routing using Layer 3 distribution switches

---

## Security

- SSH Version 2
- Local administrator authentication
- Centralized SSH management access, restricted to headquarters' IT and Management VLANs across every site
- Extended Access Control Lists (ACLs), tailored per site to isolate each site's most sensitive department
- VTY Management ACLs
- Port Security with sticky MAC learning
- BPDU Guard
- Native VLAN hardening
- Parking VLANs for unused interfaces
- Disabled Dynamic Trunking Protocol (DTP)

---

## Enterprise Services

Services follow a centralized or distributed model depending on function:

Centralized at headquarters, used by all sites:
- DNS
- HTTP
- Syslog
- NTP
- TFTP

Distributed per site:
- DHCP — independent local pools at headquarters and each branch

---

## Current Status

Target Release: **v1.0.0**

Project Zero successfully demonstrates a secure multi-site enterprise network featuring dynamic routing, Layer 3 switching, VLAN segmentation, standardized addressing and device naming, per-site access control, and a mix of centralized and distributed infrastructure services.