# Cody J. Tilley

Cybersecurity professional focused on **network security, detection engineering, and offensive security research**.

## Certifications

![CompTIA Sec+ CE](https://github.com/cta0930/cta0930/blob/main/assets/comptia-security-ce-certification.png)
![GIAC GFACT](https://github.com/cta0930/cta0930/blob/main/assets/giac-foundational-cybersecurity-technologies-gfact.png)
![GIAC Security Essenstials](https://github.com/cta0930/cta0930/blob/main/assets/giac-security-essentials-certification-gsec.png)

---
I operate a segmented **cybersecurity lab environment** used for:
- penetration testing practice
- intrusion detection research
- network traffic analysis
- threat intelligence integration
- SIEM experimentation

My work focuses on understanding how attacks occur and building **defensive visibility to detect them**.

## Home Lab Topology

The lab is designed as a segmented enterprise-style network architecture centered around an OPNsense firewall, managed switching, dedicated infrastructure segments, and containerized security tooling.

```mermaid
graph TD

Internet[Internet] --> OPNsense[OPNsense Firewall<br/>Protectli VP2420]

OPNsense --> SWIF[igc1 - Netgear Switch Uplink]
OPNsense --> NUCIF[igc2 - Intel NUC Segment]
OPNsense --> DSHIF[igc3 - DShield Segment]
OPNsense --> DNSIF[DNS Privacy Segment]

OPNsense --> WG[WireGuard VPN<br/>Remote Access]

SWIF --> Switch[Netgear Managed Switch]

Switch --> VLAN10[VLAN10 - Cyber Lab]
Switch --> VLAN20[VLAN20 - Remote Work]
Switch --> VLAN30[VLAN30 - Trusted Wireless]
Switch --> VLAN40[VLAN40 - Guest / IoT Wireless]
Switch --> VLAN50[VLAN50 - Printer / Scanner]
Switch --> VLAN99[VLAN99 - Management]

VLAN30 --> SecureSSID[Trusted SSID]

VLAN40 --> GuestSSID[Guest SSID]
VLAN40 --> IoTSSID[IoT SSID]
VLAN40 --> KodiPi[Raspberry Pi<br/>Kodi Media Streaming]

DNSIF --> DNSPrivacy[Raspberry Pi<br/>DNS Privacy Stack]

NUCIF --> SecurityServer[Intel NUC Ubuntu Server<br/>Docker Security Stack]

SecurityServer --> Wazuh[Wazuh SIEM]
SecurityServer --> TheHive[TheHive]
SecurityServer --> Cortex[Cortex]
SecurityServer --> OpenCTI[OpenCTI]

DSHIF --> DShield[Raspberry Pi<br/>DShield Honeypot Sensor]

WG --> RemoteClients[Remote Devices<br/>4 WireGuard Endpoints]
```
---
## Lab Capabilities

This environment supports hands-on experimentation with:
- intrusion detection tuning
- SIEM alert correlation
- network traffic inspection
- adversary simulation
- threat intelligence enrichment
- firewall rule analysis
- DNS privacy infrastructure
- remote secure access via VPN

The architecture isolates lab, work, wireless, IoT, printer, and management networks while enabling controlled monitoring and telemetry collection.

## Security Stack

### Detection Pipeline

Security telemetry collected within the lab environment flows through the following monitoring and analysis pipeline.

```mermaid
graph LR

Traffic[Network Traffic] --> Firewall[OPNsense Firewall]
Firewall --> Suricata[Suricata IDS/IPS]

Suricata --> Wazuh[Wazuh SIEM]

Wazuh --> Alerts[Alert Generation]

Alerts --> TheHive[TheHive Incident Response]

TheHive --> Cortex[Cortex Automated Analysis]

Cortex --> OpenCTI[OpenCTI Threat Intelligence]

OpenCTI --> Investigation[Security Investigation]
```
---
### Firewall & Network Segmentation
- OPNsense Firewall (Protectli VP2420)
- VLAN segmentation with managed switching
- WireGuard VPN for secure remote access
- Suricata IDS/IPS
- ZenArmor traffic analysis

### Security Monitoring & Incident Response
- Wazuh SIEM
- TheHive incident response platform
- Cortex automated analysis engine

## Infrastrucure
- Ubuntu server running Docker security stack
- Intel NUC security host
- Raspberry Pi sensors and infrastructure services
- DNS privacy stack for internal resolution hardening
- DShield honeypot sensor

## Security Research & Projects

### Network Security Lab

A segmented cybersecurity lab environment built with **OPNsense firewall and VLAN isolation**.

Research areas include:
- IDS rule tuning
- firewall policy validation
- network traffic analysis
- SIEM event correlation
- detection engineering experimentation

---
### Security Research & Lab Writeups

Documenting security research and lab exercises including:
- penetration testing labs
- network security experiments
- vulnerability analysis
- detection engineering techniques

Research notes and walkthroughs are published at:

[Walkthroughs](https://cta0930.github.io)

---
# Professional Links

### LinkedIn  
[![Cody Tilley](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/ctilley0124)
All Links  
[Linktr](https://linktr.ee/cta0930)

---
## Repository Focus

This GitHub will continue to grow with:

- security research
- lab infrastructure projects
- penetration testing tooling
- detection engineering experiments
- security walkthroughs

---
### **TryHackMe Progress**
![TryHackMe Badge](https://tryhackme-badges.s3.amazonaws.com/spectr1.png)
---
### ***Join me on CTFs and labs***
[![TryHackMe](https://img.shields.io/badge/TryHackMe-Profile-red?logo=tryhackme&logoColor=white&style=for-the-badge)](https://tryhackme.com/p/spectr1)
[![Hack The Box](https://img.shields.io/badge/Hack%20The%20Box-Profile-9FEF00?logo=hackthebox&logoColor=black&style=for-the-badge)](https://profile.hackthebox.com/profile/019cda26-69e8-73b8-88c2-07d88618efe7)
---

