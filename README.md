# 🏠 Secure Home Network & UniFi VLAN Segmentation Lab

## Overview
This project documents the design, deployment, and security hardening of a **multi-VLAN UniFi home network** built using enterprise-style networking practices. The goal was to simulate a **small-business / SOHO security architecture** while maintaining high performance for daily use.

The lab demonstrates hands-on experience with:
- Network segmentation
- Firewall policy design
- Secure wireless configuration
- Hardware installation & rack design
- Real-world troubleshooting

---

## Objectives
- Segment trusted, untrusted, and guest devices using VLANs
- Reduce attack surface between IoT, Guest, and Home networks
- Implement least-privilege firewall rules
- Maintain multi-gigabit wired performance
- Document the system in a reproducible, professional manner

---

## Hardware & Platform
**Network Equipment**
- UniFi Cloud Gateway Max (2.5 GbE)
- UniFi Flex 2.5G PoE Switch
- UniFi Switch 210W
- UniFi U7 Pro Wi-Fi Access Point

**Rack & Physical Setup**
- 4U Mini network rack
- Custom 3D-printed rack shelves and cable guides
- Structured cabling with labeled runs

📷 *Insert rack overview image here*

---

## Network Architecture

### VLAN Design
| VLAN Name | Purpose | Example Devices |
|---------|--------|----------------|
| Management | Network infrastructure | Gateway, switches, APs |
| Home | Trusted clients | PC, phone, laptop |
| IoT | Untrusted smart devices | TV, smart speakers, cameras |
| Guest | Isolated internet access | Visitor devices |

📷 *Insert network diagram here*

---

## Wireless Configuration
- Separate SSIDs mapped to VLANs
- IoT SSID optimized for compatibility
- Guest SSID fully isolated from internal networks
- WPA3 / WPA2 mixed where supported
- Band steering enabled for performance-capable devices

📷 *Insert UniFi Wi-Fi settings screenshot here*

---

## Firewall & Security Controls

### Firewall Strategy
- Default deny between VLANs
- Explicit allow rules for required services
- Zone-based policy model

### Example Rules
- Block IoT → Home traffic
- Allow Home → IoT (limited control)
- Allow Guest → WAN only
- Permit Management VLAN to infrastructure devices only

📷 *Insert firewall rule screenshot here*

---

## Performance Validation
- Verified 2.5 GbE uplinks between gateway and switch
- Confirmed VLAN tagging and client placement
- Validated wired and wireless throughput
- Troubleshot port negotiation and AP band behavior

---

## Key Lessons Learned
- Application throughput ≠ link speed
- IoT optimization can impact modern devices
- Firewall logging is critical for validation
- Physical layer issues often mimic logical problems

---

## Future Improvements
- VPN access to Management VLAN
- IDS/IPS tuning and alerting
- Centralized logging
- Network monitoring dashboards

---

## Why This Project Matters
This lab reflects **real-world networking and security workflows**, including planning, deployment, validation, and troubleshooting — not just theoretical knowledge.

