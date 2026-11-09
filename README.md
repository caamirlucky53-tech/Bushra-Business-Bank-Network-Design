# Bushra Business Bank – Enterprise Network Design

**Course:** Network Analysis and Design
**Type:** Group project (design only, no device configuration)
**Deadline:** Wednesday, 18 November 2026

## Group Members

| # | Name | ID |
|---|------|----|
| 1 | Zakariye Abdirzak Hassan | C6240122 |
| 2 | Clshakuur Cumar Maxamuud | C6240289 |
| 3 | Abdulkadir Artan Abdi | C6240257 |
| 4 | Aamir Ahmed Muhidin | C6240174 |
| 5 | Ahmed Mohamed Ahmed | C6240167 |

## Project Summary

This project designs a secure, resilient and scalable network for **Bushra Business Bank**, which has a Head Office, three branches, a Data Center and a Disaster Recovery (DR) site.

### Problems solved

| Problem | Solution |
|---|---|
| Insecure branch connections | Private WAN, IPsec VPN encryption, firewalls at every site |
| Single internet connection | Dual ISP with automatic failover |
| Flat, unsafe network | VLAN segmentation, ACLs, DMZ, firewalls |
| No disaster recovery | DR site with continuous data replication |
| Poor IP planning | Structured, documented addressing with room to grow |

### Design highlights

- **Hierarchical 3-layer design** at Head Office (Core, Distribution, Access)
- **Redundancy:** dual ISP, HSRP, EtherChannel, HA firewalls, DR site
- **Security:** NGFW, DMZ, VLANs, ACLs, IPS, IPsec VPN, port security, AAA/802.1X
- **WAN:** MPLS / leased line (primary) with IPsec VPN over the internet (backup)

### IP addressing overview

| Site | Block |
|---|---|
| Head Office | 10.0.0.0/16 |
| Branch 1 | 10.1.0.0/16 |
| Branch 2 | 10.2.0.0/16 |
| Branch 3 | 10.3.0.0/16 |
| Data Center | 10.10.0.0/16 |
| DR Site | 10.20.0.0/16 |
| DMZ | 192.168.100.0/24 |
| WAN links | 172.16.x.0/30 |

Head Office VLANs: 10 Management, 20 Staff, 30 Servers, 40 Tellers/ATM, 50 Guest Wi-Fi, 60 VoIP (each a /24, e.g. 10.0.20.0/24).

## Repository Contents

| File | Description |
|---|---|
| `Bushra-Bank-Network-Design.pdf` | Full design document (requirements, IP plan, security, redundancy) |
| `Network-Diagram.png` | Network topology diagram |
| `README.md` | This file |

## Note

This is a design-only project. No device configuration is included, as required by the course.
