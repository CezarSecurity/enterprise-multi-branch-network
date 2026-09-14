# Security Architecture

Project Zero implements multiple layers of security throughout the enterprise network.

---

## Secure Device Management

Administrative access is secured using:

- SSH Version 2
- Local user authentication
- Encrypted passwords
- VTY access restrictions

SSH management access follows a centralized model: only headquarters' IT and Management VLANs (`10.10.30.0/27` and `10.10.99.0/27`) are permitted to establish SSH sessions with any device in the enterprise, including branch devices. Branch management subnets, where they exist, are not granted local SSH access — administration is handled centrally from headquarters.

---

## Layer 2 Security

Confirmed enterprise-wide, at headquarters and all three branches:

- Port Security with sticky MAC learning, limiting each access port to a single learned device
- BPDU Guard on all access ports
- Disabled Dynamic Trunking Protocol (DTP) on every trunk port, distribution switch and access switch alike
- Native VLAN hardening — all trunk ports use a dedicated, unused VLAN (998) as native, rather than a live department or management VLAN
- Dedicated parking VLAN (999) for unused, administratively shut down interfaces

---

## Layer 3 Security

Extended Access Control Lists (ACLs) enforce communication policies between departments at every site.

**Headquarters:**
- Finance isolation
- Human Resources isolation
- Operations and Administration restrictions
- Wireless client restrictions
- IoT network isolation (DNS-only)

**Penang:**
- Executive isolation from Customer, Sales, and Logistics
- Wireless client restrictions
- IoT network isolation (DNS-only)

**Johor Bahru:**
- Corporate isolation from Operations and Procurement
- Wireless client restrictions
- IoT network isolation (DNS-only)

**Kota Kinabalu:**
- Accounts isolation from Talent, Technical Support, and Client Success
- Wireless client restrictions
- IoT network isolation (DNS-only)

All sites additionally restrict SSH management access (VTY) to headquarters' IT and Management VLANs only.

---

## Infrastructure Security

Enterprise services are split between centralized and distributed models:

**Centrally hosted at headquarters** (all sites use these):
- DNS
- Syslog
- NTP
- HTTP
- TFTP

**Distributed per site:**
- DHCP — each site runs its own independent DHCP pools on its local distribution switch, rather than relying on a centralized DHCP server or relay. This avoids making local address assignment dependent on WAN connectivity to headquarters.

---

## Known Limitations

All devices across the enterprise currently share a common administrative credential set for lab simplicity. In a production deployment, credentials would be unique per device or managed centrally via TACACS+/RADIUS rather than local authentication.