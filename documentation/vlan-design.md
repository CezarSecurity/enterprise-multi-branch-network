- # VLAN Design

  ## Overview

  Project Zero uses VLAN segmentation to isolate departments into separate broadcast domains. Inter-VLAN routing is performed locally on each Layer 3 distribution switch, minimizing unnecessary WAN traffic while improving security and scalability.

  ---

  ## Headquarters

  | VLAN | Department         |
  | ---- | ------------------ |
  | 10   | Operations         |
  | 20   | Administration     |
  | 30   | IT                 |
  | 40   | Servers            |
  | 50   | Finance            |
  | 60   | Wireless           |
  | 70   | Human Resources    |
  | 80   | IoT                |
  | 99   | Management         |
  | 998  | Native Unused VLAN |
  | 999  | Parking Lot        |

  ---

  ## Penang Branch

  | VLAN | Department         |
  | ---- | ------------------ |
  | 15   | Customer           |
  | 25   | Technical Services |
  | 35   | Sales              |
  | 45   | Logistics          |
  | 55   | Data Center        |
  | 65   | Wireless           |
  | 75   | IoT                |
  | 85   | Executive          |
  | 99   | Management         |
  | 998  | Native Unused VLAN |
  | 999  | Parking Lot        |

  ---

  ## Johor Bahru Branch

  | VLAN | Department         |
  | ---- | ------------------ |
  | 110  | Operations         |
  | 120  | Corporate          |
  | 130  | Research           |
  | 140  | Procurement        |
  | 150  | Systems            |
  | 160  | Wireless           |
  | 170  | IoT                |
  | 180  | Servers            |
  | 199  | Management         |
  | 998  | Native Unused VLAN |
  | 999  | Parking Lot        |

  ---

  ## Kota Kinabalu Branch

  | VLAN | Department                                            |
  | ---- | ----------------------------------------------------- |
  | 210  | Strategy                                              |
  | 220  | Accounts                                              |
  | 230  | Talent                                                |
  | 240  | Technical Support                                     |
  | 250  | Data Center                                           |
  | 260  | Wireless                                              |
  | 270  | Smart IoT                                             |
  | 280  | Client Success                                        |
  | 299  | Management (unassigned — no local management network) |
  | 998  | Native Unused VLAN                                    |
  | 999  | Parking Lot                                           |

  ---

  ## Trunk Design

  IEEE 802.1Q trunking is used between distribution and access switches, enforced identically across all four sites.

  Security enhancements include:

  - Native VLAN hardening — all trunk ports use a dedicated, unused VLAN (998) as native, rather than a live department or management VLAN, preventing native VLAN traffic from carrying real data
  - Explicit allowed VLAN lists
  - Dynamic Trunking Protocol (DTP) disabled on every trunk port (`switchport nonegotiate`), removing the negotiation surface that untrusted devices could exploit to force trunking
  - Standardized trunk configuration across all sites, applied to both distribution switches and every access switch
  - Unused switchports administratively shut down and parked in a dedicated, isolated VLAN (999) rather than left active in the default VLAN

  ---

  ## Benefits

  The VLAN architecture provides:

  - Department isolation
  - Reduced broadcast domains
  - Improved security
  - Simplified administration
  - Scalable network expansion