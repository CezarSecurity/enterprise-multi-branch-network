# Routing Design

## Overview

Project Zero uses Open Shortest Path First (OSPF) as its enterprise routing protocol.

OSPF replaces the static routing used during the early stages of the project and provides automatic route discovery throughout the enterprise.

---

## OSPF Design

All routing devices participate in a single OSPF Area 0 backbone.

Each router and Layer 3 distribution switch advertises its directly connected networks into the routing domain.

This allows automatic route propagation between:

- Headquarters
- Penang
- Johor Bahru
- Kota Kinabalu

---

## Inter-VLAN Routing

Inter-VLAN routing is performed on the Layer 3 distribution switches using Switch Virtual Interfaces (SVIs).

Each VLAN gateway resides on the distribution switch.

This reduces unnecessary WAN traffic by keeping local traffic within each site.

---

## Default Routing

Each distribution switch forwards unknown traffic to its local WAN router using a default route.

The WAN routers then forward traffic across the enterprise using OSPF.

---

## Benefits

Using OSPF provides:

- Dynamic route learning
- Fast convergence
- Reduced administrative overhead
- Scalable enterprise routing
- Simplified network expansion