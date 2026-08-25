# IP Addressing Plan

## Headquarters

The headquarters uses private IPv4 addressing for all production VLANs.

| VLAN | Department | Network |
|------|------------|---------------|
| 10 | Operations | 10.10.10.0/27 |
| 20 | Administration | 10.10.20.0/27 |
| 30 | IT | 10.10.30.0/27 |
| 40 | Servers | 10.10.40.0/27 |
| 50 | Finance | 10.10.50.0/27 |
| 60 | Wireless | 10.10.60.0/24 |
| 70 | Human Resources | 10.10.70.0/27 |
| 80 | IoT | 10.10.80.0/24 |
| 99 | Management | 10.10.99.0/27 |

---

## WAN Addressing

Point-to-point WAN links use /30 subnets.

| Connection | Network |
|------------|----------------|
| KL ↔ Penang | 200.0.0.0/30 |
| KL ↔ Johor Bahru | 200.0.0.4/30 |
| KL ↔ Kota Kinabalu | 200.0.0.8/30 |

---

## Branch Networks

### Penang

Base Network: **200.20.20.0/24**

| VLAN | Department |
|------|------------|
| 15 | Customer |
| 25 | Technical Services |
| 35 | Sales |
| 45 | Logistics |
| 55 | Data Center |
| 65 | Wireless |
| 75 | IoT |
| 85 | Executive |
| 99 | Management |

---

### Johor Bahru

Base Network: **200.30.30.0/24**

| VLAN | Department |
|------|------------|
| 110 | Operations |
| 120 | Corporate |
| 130 | Research |
| 140 | Procurement |
| 150 | Systems |
| 160 | Wireless |
| 170 | IoT |
| 180 | Servers |
| 199 | Management |

---

### Kota Kinabalu

Base Network: **200.40.40.0/24**

| VLAN | Department |
|------|------------|
| 210 | Strategy |
| 220 | Accounts |
| 230 | Talent |
| 240 | Technical Support |
| 250 | Data Center |
| 260 | Wireless |
| 270 | Smart IoT |
| 280 | Client Success |
| 299 | Management |

---

## Addressing Strategy

Each site uses a dedicated address block. Every VLAN is assigned its own subnet, with the Layer 3 distribution switch providing the default gateway for connected hosts. OSPF dynamically advertises all VLAN networks between headquarters and branch offices.