# Network Security Lab

A practical network-security learning project covering network architecture, segmentation, firewall policy, secure protocols and common network threats.

## Objectives
- Understand how a small business network can be segmented.
- Document IP addressing and network zones.
- Design basic firewall and access-control rules.
- Identify common network attack scenarios.
- Recommend defensive controls.

## Architecture
```text
Internet
   |
[Firewall]
   |
+--+-------------------+
|                      |
DMZ                Internal Network
|                      |
Web Server          User Devices
                     |
                  Admin VLAN
                     |
                  Server VLAN
```

## Security Zones

| Zone | Purpose | Security Principle |
|---|---|---|
| DMZ | Public-facing services | Limited exposure |
| User VLAN | Employee devices | Least privilege |
| Server VLAN | Internal services | Restricted access |
| Admin VLAN | Administration | Strong access control |

## Example Firewall Policy

| Source | Destination | Protocol | Action |
|---|---|---|---|
| Internet | Web server | HTTPS | Allow |
| Internet | Internal network | Any | Deny |
| User VLAN | Server VLAN | HTTPS | Allow |
| User VLAN | Admin VLAN | Any | Deny |
| Admin VLAN | Server VLAN | SSH/HTTPS | Allow |

## Threats
Port scanning, brute-force authentication, traffic interception, lateral movement and insecure protocols.

## Skills Demonstrated
Networking, segmentation, access control, firewall policy, threat analysis and security documentation.

## Next Step
Build this topology in Cisco Packet Tracer and add screenshots of VLANs, routing and security controls.
