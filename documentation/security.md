# Security Architecture

Project Zero implements multiple layers of security throughout the enterprise network.

---

## Secure Device Management

Administrative access is secured using:

- SSH Version 2
- Local user authentication
- Encrypted passwords
- VTY access restrictions

Only authorized management networks are permitted to establish SSH sessions with network devices.

---

## Layer 2 Security

Layer 2 protections include:

- Port Security
- Sticky MAC learning
- BPDU Guard
- Disabled Dynamic Trunking Protocol (DTP)
- Native VLAN hardening
- Dedicated parking VLANs for unused interfaces

These controls reduce the attack surface and protect against common Layer 2 attacks.

---

## Layer 3 Security

Extended Access Control Lists (ACLs) are used to enforce communication policies between departments.

Examples include:

- Finance isolation
- Human Resources isolation
- Wireless client restrictions
- IoT network isolation
- Management access control

---

## Infrastructure Security

Enterprise infrastructure services are centrally hosted at headquarters.

These include:

- DHCP
- DNS
- HTTP
- Syslog
- NTP
- TFTP

Centralizing infrastructure simplifies administration while providing consistent services across every site.