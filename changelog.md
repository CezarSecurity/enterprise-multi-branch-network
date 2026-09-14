# Changelog

All notable changes to Project Zero are documented in this file.

This project follows semantic versioning during development, with milestone releases representing major improvements to the enterprise network.

---

## [v1.0.0] - Enterprise-Wide Standardization and Security Hardening

Note: v0.8.0 and v0.9.0 were planned but skipped — all remaining work was completed and released directly as v1.0.0 rather than staged across additional pre-release versions.

### Added

- Standardized device naming across all branches, matching headquarters' convention (`PG-CORE-SW1`/`PG-RTR-01`, `JB-CORE-SW1`/`JB-RTR-01`, `KK-CORE-SW1`/`KK-RTR-01`)
- Branch management VLAN addressing at Penang and Johor Bahru, with static assignments for administrative devices
- Per-branch DHCP pools, sized to actual department device counts
- Centralized Syslog and NTP configuration on all branch devices
- OSPF advertisement of branch management subnets, closing a gap where they were locally functional but unreachable enterprise-wide
- Trunk hardening on all branches: DTP disabled, dedicated unused native VLAN (998), standardized trunk configuration across every distribution and access switch
- Unused switchport hardening on all branches: administrative shutdown, dedicated parking VLAN (999)
- Port Security, sticky MAC learning, and BPDU Guard on all branch access switches
- Per-site Extended ACLs enforcing department, wireless, and IoT isolation, tailored to each branch's most sensitive department
- Full documentation refresh across all `docs/` files to accurately reflect the deployed network

### Changed

- Removed a dead default route on the headquarters router pointing to an unreachable, non-existent next hop
- Updated interface descriptions enterprise-wide to reflect standardized device naming
- Corrected DHCP pool exclusions after real-world testing revealed lease failures in a fully populated department; exclusions now reserve only the gateway address rather than a fixed block

### Removed

- Decorative, non-functional server devices at Penang, Johor Bahru, and Kota Kinabalu

---

## [v0.7.0] - Documentation & Repository Enhancement

### Added

- Professional technical documentation
- Enterprise architecture documentation
- IP addressing documentation
- VLAN design documentation
- Routing design documentation
- Security architecture documentation
- Network validation documentation
- Full Layer 3 device configuration backups
- Repository structure improvements

### Changed

- Updated project documentation to accurately reflect the deployed enterprise network
- Improved repository organization
- Enhanced project maintainability

---

## [v0.6.0] - Infrastructure Standardization

### Added

- Enterprise MOTD banner
- Standardized interface descriptions
- Consistent device naming
- Standardized management account configuration

### Changed

- Standardized Layer 3 device configurations
- Improved infrastructure consistency
- Cleaned legacy configuration remnants

### Removed

- Obsolete static routes
- Legacy configuration artifacts

---

## [v0.5.0] - Enterprise Security Hardening

### Added

- Extended Access Control Lists (ACLs)
- Management VTY ACLs
- Secure SSH management across all Layer 3 devices
- Department isolation policies
- Wireless network isolation
- IoT network isolation

### Changed

- Standardized enterprise security baseline
- Improved secure management access

---

## [v0.4.0] - Dynamic Routing Migration

### Added

- Enterprise-wide OSPF deployment
- OSPF Area 0 backbone
- Dynamic route advertisement
- Automatic route learning

### Changed

- Migrated from static routing to OSPF
- Improved enterprise routing scalability

### Removed

- Legacy enterprise static routing

---

## [v0.3.0] - Infrastructure Services

### Added

- Private IPv4 addressing
- Centralized DHCP services
- DNS services
- HTTP services
- Syslog server
- NTP server
- TFTP server

### Changed

- Migrated headquarters to private addressing
- Centralized enterprise network services

---

## [v0.2.0] - Headquarters Security

### Added

- SSH Version 2
- Local administrator authentication
- Port Security
- Sticky MAC learning
- BPDU Guard
- Native VLAN hardening
- Parking VLAN
- Disabled Dynamic Trunking Protocol (DTP)

### Changed

- Hardened headquarters switching infrastructure

---

## [v0.1.0] - Initial Release

### Added

- Enterprise topology redesign
- Four-site enterprise architecture
- Professional branch layouts
- Standardized device naming
- GitHub repository
- Initial project documentation