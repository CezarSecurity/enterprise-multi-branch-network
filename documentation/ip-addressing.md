# IP Addressing Plan

## Headquarters

The headquarters uses private IPv4 addressing for all production VLANs.

| VLAN | Department      | Network       |
| ---- | --------------- | ------------- |
| 10   | Operations      | 10.10.10.0/27 |
| 20   | Administration  | 10.10.20.0/27 |
| 30   | IT              | 10.10.30.0/27 |
| 40   | Servers         | 10.10.40.0/27 |
| 50   | Finance         | 10.10.50.0/27 |
| 60   | Wireless        | 10.10.60.0/24 |
| 70   | Human Resources | 10.10.70.0/27 |
| 80   | IoT             | 10.10.80.0/24 |
| 99   | Management      | 10.10.99.0/27 |

---

## WAN Addressing

Point-to-point WAN links use /30 subnets.

| Connection         | Network      |
| ------------------ | ------------ |
| HQ ↔ Penang        | 200.0.0.0/30 |
| HQ ↔ Johor Bahru   | 200.0.0.4/30 |
| HQ ↔ Kota Kinabalu | 200.0.0.8/30 |

---

## Branch Networks

Each branch's department VLANs are carved into /27 subnets from a dedicated /24 base network. Management VLANs are addressed separately, outside the base /24, following the same pattern used at headquarters.

### Penang

Base Network: **200.20.20.0/24**

| VLAN | Department         | Network          | Gateway | Notes                             |
| ---- | ------------------ | ---------------- | ------- | --------------------------------- |
| 15   | Customer           | 200.20.20.0/27   | .1      | DHCP                              |
| 25   | Technical Services | 200.20.20.32/27  | .33     | DHCP                              |
| 35   | Sales              | 200.20.20.64/27  | .65     | DHCP                              |
| 45   | Logistics          | 200.20.20.96/27  | .97     | DHCP                              |
| 55   | Data Center        | 200.20.20.128/27 | .129    | No active devices deployed        |
| 65   | Wireless           | 200.20.20.160/27 | .161    | DHCP                              |
| 75   | IoT                | 200.20.20.192/27 | .193    | DHCP                              |
| 85   | Executive          | 200.20.20.224/27 | .225    | Static addressing                 |
| 99   | Management         | 200.20.21.0/27   | .1      | Separate block; static addressing |

---

### Johor Bahru

Base Network: **200.30.30.0/24**

| VLAN | Department  | Network          | Gateway | Notes                             |
| ---- | ----------- | ---------------- | ------- | --------------------------------- |
| 110  | Operations  | 200.30.30.0/27   | .1      | DHCP                              |
| 120  | Corporate   | 200.30.30.32/27  | .33     | DHCP                              |
| 130  | Research    | 200.30.30.64/27  | .65     | DHCP                              |
| 140  | Procurement | 200.30.30.96/27  | .97     | DHCP                              |
| 150  | Systems     | 200.30.30.128/27 | .129    | DHCP                              |
| 160  | Wireless    | 200.30.30.160/27 | .161    | DHCP                              |
| 170  | IoT         | 200.30.30.192/27 | .193    | No devices deployed               |
| 180  | Servers     | 200.30.30.224/27 | .225    | No active devices deployed        |
| 199  | Management  | 200.30.31.0/27   | .1      | Separate block; static addressing |

---

### Kota Kinabalu

Base Network: **200.40.40.0/24**

| VLAN | Department        | Network          | Gateway | Notes                                                        |
| ---- | ----------------- | ---------------- | ------- | ------------------------------------------------------------ |
| 210  | Strategy          | 200.40.40.0/27   | .1      | DHCP                                                         |
| 220  | Accounts          | 200.40.40.32/27  | .33     | DHCP                                                         |
| 230  | Talent            | 200.40.40.64/27  | .65     | DHCP                                                         |
| 240  | Technical Support | 200.40.40.96/27  | .97     | DHCP                                                         |
| 250  | Data Center       | 200.40.40.128/27 | .129    | No active devices deployed                                   |
| 260  | Wireless          | 200.40.40.160/27 | .161    | DHCP                                                         |
| 270  | Smart IoT         | 200.40.40.192/27 | .193    | No devices deployed                                          |
| 280  | Client Success    | 200.40.40.224/27 | .225    | DHCP                                                         |
| 299  | Management        | Unassigned       | —       | No local management network; site is managed centrally from headquarters |

---

## Addressing Strategy

Each site uses a dedicated address block, with the Layer 3 distribution switch providing the default gateway for connected hosts. Department VLANs are dynamically addressed via DHCP; management and executive-tier VLANs use static addressing so administrative access does not depend on a DHCP service running on the same infrastructure it manages.

Management VLANs are addressed from a separate block outside each site's department /24, matching the pattern used at headquarters (`10.10.99.0/27` sits outside the `10.10.x.0` department range in the same way). Kota Kinabalu has no local management subnet; administrative access to its devices is handled centrally from headquarters.

OSPF dynamically advertises all VLAN networks — including branch management subnets — between headquarters and branch offices.