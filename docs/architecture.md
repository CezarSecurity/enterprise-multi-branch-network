- # Enterprise Network Architecture

  ## Overview

  Project Zero is a multi-site enterprise network designed and implemented using Cisco Packet Tracer. The network simulates a medium-sized organization with a centralized headquarters and three geographically distributed branch offices.

  Locations include:

  - Kuala Lumpur Headquarters
  - Penang Branch
  - Johor Bahru Branch
  - Kota Kinabalu Branch

  The headquarters functions as the core of the enterprise, providing centralized network services while acting as the routing hub for all branch offices.

  ---

  ## Network Topology

  Project Zero follows a hub-and-spoke topology.

  The headquarters router maintains WAN connections to each branch router using dedicated point-to-point serial links. Every branch contains a dedicated WAN router connected to a Layer 3 distribution switch responsible for inter-VLAN routing.

  This architecture provides:

  - Centralized management
  - Simplified routing
  - Scalable branch expansion
  - Enterprise-grade segmentation

  ---

  ## Device Naming Convention

  All Layer 3 devices follow a standardized naming convention across the enterprise:

  | Site          | Distribution Switch | Router    |
  | ------------- | ------------------- | --------- |
  | Headquarters  | HQ-CORE-SW1         | HQ-RTR-01 |
  | Penang        | PG-CORE-SW1         | PG-RTR-01 |
  | Johor Bahru   | JB-CORE-SW1         | JB-RTR-01 |
  | Kota Kinabalu | KK-CORE-SW1         | KK-RTR-01 |

  ---

  ## Headquarters

  The headquarters hosts the enterprise infrastructure services and contains:

  - One WAN Router
  - One Layer 3 Distribution Switch
  - Eight Access Switches
  - Enterprise Server Infrastructure

  The Layer 3 distribution switch performs inter-VLAN routing while the headquarters router provides WAN connectivity to all branch offices.

  ---

  ## Branch Offices

  Each branch consists of:

  - One WAN Router
  - One Layer 3 Distribution Switch
  - Department-based VLAN segmentation
  - Multiple Access Switches

  The distribution switch performs local inter-VLAN routing while forwarding off-site traffic to the local branch router.

  ---

  ## Dynamic Routing

  Dynamic routing is implemented using OSPF Area 0.

  The headquarters router acts as the backbone router while every branch router participates in the same OSPF area, allowing automatic route learning and route convergence throughout the enterprise.

  ---

  ## Enterprise Design Principles

  Project Zero was designed around several enterprise networking principles:

  - Layered network architecture
  - Department-based segmentation
  - Centralized infrastructure services
  - Secure device management
  - Dynamic routing
  - Configuration standardization
  - Network scalability