\# Network Overview



\---



\# Apex Manufacturing, Inc.



\## Purpose



This document provides a high-level overview of the enterprise network architecture used throughout the Apex Manufacturing lab environment.



The network is designed to simulate a modern mid-sized enterprise supporting approximately 850 employees across multiple office locations. It serves as the authoritative reference for network design, IP addressing, VLAN segmentation, core infrastructure, and connectivity standards.



\---



\# Network Objectives



The enterprise network is designed to provide:



\- Secure communication between corporate locations

\- High availability for critical business services

\- Segmentation of business departments

\- Secure remote access for hybrid employees

\- Centralized authentication

\- Scalable infrastructure for future growth

\- Support for cybersecurity monitoring and incident response



\---



\# Corporate Locations



| Location | Purpose |

|----------|---------|

| Dallas Headquarters | Executive leadership, IT, HR, Finance, Engineering, Marketing |

| Phoenix Distribution Center | Operations, Manufacturing, Warehouse |

| Atlanta Sales Office | Sales and Customer Support |



\---



\# Core Infrastructure



The Dallas Headquarters hosts the primary infrastructure for the organization.



\## Core Services



\- Active Directory Domain Services

\- DNS

\- DHCP

\- File Services

\- Print Services

\- Group Policy

\- Microsoft 365 Integration

\- VPN Gateway

\- Backup Services

\- Endpoint Management

\- Monitoring Platform



\---



\# Network Topology



```text

&#x20;                          Internet

&#x20;                              │

&#x20;                        ISP Connection

&#x20;                              │

&#x20;                       Next-Generation Firewall

&#x20;                              │

&#x20;                      Core Layer Switch Stack

&#x20;                              │

&#x20;     ┌───────────────┬───────────────┬───────────────┐

&#x20;     │               │               │               │

&#x20; Server VLAN     User VLAN      Voice VLAN      Guest VLAN

&#x20;     │               │               │               │

&#x20;  DC01           Employee PCs     IP Phones      Guest Wi-Fi

&#x20;  FILE01

&#x20;  PRINT01

&#x20;  APP01

&#x20;  BACKUP01

```



\---



\# IP Addressing Plan



| Network | Subnet | Purpose |

|----------|---------|---------|

| Server Network | 192.168.10.0/24 | Infrastructure servers |

| User Network | 192.168.20.0/24 | Employee workstations |

| Voice Network | 192.168.30.0/24 | VoIP phones |

| Printer Network | 192.168.40.0/24 | Network printers |

| Guest Network | 192.168.50.0/24 | Guest Wi-Fi |

| Management Network | 192.168.60.0/24 | Network management devices |

| VPN Network | 192.168.70.0/24 | Remote users |



\---



\# VLAN Design



| VLAN | Name | Purpose |

|------|------|---------|

| 10 | Servers | Domain controllers and infrastructure |

| 20 | Users | Employee workstations |

| 30 | Voice | IP telephony |

| 40 | Printers | Network printers |

| 50 | Guest | Internet-only guest access |

| 60 | Management | Administrative devices |

| 70 | VPN | Remote employee access |



\---



\# Core Servers



| Hostname | Primary Function |

|----------|------------------|

| DC01 | Active Directory Domain Controller |

| FILE01 | File Services |

| PRINT01 | Print Services |

| APP01 | Internal Applications |

| BACKUP01 | Backup and Recovery |

| MGMT01 | Systems Management |

| WSUS01 | Windows Updates |

| MONITOR01 | Infrastructure Monitoring |



\---



\# Authentication



Users authenticate using:



\- Active Directory

\- Domain credentials

\- Multi-Factor Authentication (where applicable)

\- Role-Based Access Control (RBAC)



\---



\# Remote Access



Authorized remote employees connect using:



\- Corporate VPN

\- Multi-Factor Authentication

\- Company-managed devices

\- Domain credentials



\---



\# Internet Security



All inbound and outbound traffic is protected through a next-generation firewall.



Security controls include:



\- Web filtering

\- Intrusion Prevention System (IPS)

\- Malware inspection

\- Application control

\- Geo-blocking (where applicable)

\- Secure VPN termination



\---



\# Wireless Networks



| SSID | Purpose |

|------|---------|

| Apex-Corporate | Corporate-managed devices |

| Apex-Guest | Guest Internet access |

| Apex-IT | IT administration and testing |



\---



\# DNS Standards



Internal domain:



```text

apex.local

```



Public email domain:



```text

apexmanufacturing.com

```



\---



\# High Availability



Critical infrastructure includes:



\- Redundant power

\- Nightly backups

\- UPS protection

\- RAID storage

\- Virtual machine snapshots

\- Disaster recovery procedures



\---



\# Monitoring



The IT department continuously monitors:



\- Server availability

\- Network latency

\- Firewall events

\- VPN connections

\- Disk utilization

\- Authentication failures

\- Security alerts

\- Backup success

\- Service health



\---



\# Future Expansion



Planned enhancements include:



\- Azure hybrid integration

\- Microsoft Entra ID

\- Microsoft Intune

\- Microsoft Defender

\- Microsoft Sentinel

\- Splunk Enterprise

\- Wazuh

\- Endpoint Detection and Response (EDR)

\- Network Access Control (NAC)



\---



\# Related Documentation



\- Company-Profile.md

\- Organizational-Chart.md

\- Employee-Directory.md

\- Server-Inventory.md

\- Asset-Inventory.md

\- IT-Infrastructure.md

\- Security-Policies.md



\---



\# Revision History



| Version | Date | Author | Description |

|----------|------|--------|-------------|

| 1.0 | July 2026 | Kenyotta Eave | Initial network overview created. |

