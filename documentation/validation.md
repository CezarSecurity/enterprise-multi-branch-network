# Network Validation

The enterprise network has been tested to verify functionality, connectivity, routing, and security across all four sites.

---

## OSPF Validation

Tests Performed

- OSPF neighbor formation across all WAN links
- Dynamic route advertisement, including branch management subnets
- End-to-end WAN routing between headquarters and all branches

Result

PASS

---

## DHCP Validation

Tests Performed

- Automatic IP address assignment per department VLAN, at headquarters and all three branches
- Default gateway assignment
- DNS server assignment
- Pool sizing validated against real device counts per department

Result

PASS

Note: initial DHCP exclusions at one branch were sized too conservatively for a fully populated department, causing lease failures under real load. Pool exclusions were corrected to reserve only the gateway address rather than a fixed block, resolving the issue with adequate headroom.

---

## DNS Validation

Tests Performed

- Internal hostname resolution
- Web server resolution

Result

PASS

---

## SSH Validation

Tests Performed

- Secure remote device access
- Local authentication
- VTY ACL enforcement, confirming SSH access is restricted to headquarters' IT and Management VLANs across every site

Result

PASS

---

## Layer 2 Security Validation

Tests Performed

- Native VLAN consistency across all trunk links, distribution switch to access switch
- Dynamic Trunking Protocol (DTP) disabled on all trunk ports
- Port Security and BPDU Guard enforcement on all access ports

Result

PASS

Notes: during native VLAN hardening, a genuine PVID mismatch was observed and confirmed working as intended — Spanning Tree correctly blocked a trunk port until both ends were aligned to the hardened native VLAN, demonstrating the control functions as designed rather than being merely configured. Separately, a blanket Port Security deployment briefly misapplied access-port settings to one switch's trunk uplink; this was identified through the resulting violation logs and corrected before rollout to the remaining switches.

---

## Access Control Validation

Tests Performed

- Headquarters: Finance isolation, Human Resources isolation, wireless client restrictions, IoT network isolation
- Penang: Executive isolation from Customer, Sales, and Logistics; wireless and IoT restrictions
- Johor Bahru: Corporate isolation from Operations and Procurement; wireless and IoT restrictions
- Kota Kinabalu: Accounts isolation from Talent, Technical Support, and Client Success; wireless and IoT restrictions

Result

PASS

---

## Infrastructure Services

Verified Services

Centralized at headquarters, used by all sites:
- DNS
- HTTP
- Syslog
- NTP
- TFTP

Distributed per site:
- DHCP — independent local pools at headquarters and each branch

Result

PASS

---

## Overall Assessment

Project Zero successfully demonstrates the design and implementation of a secure multi-site enterprise network.

Key capabilities include:

- Layer 3 switching
- Department-based VLAN segmentation
- Dynamic routing using OSPF, including management subnet reachability
- Secure, centralized device management
-