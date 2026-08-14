# Inter-VLAN Routing with a Multilayer Switch

A hands-on Cisco Packet Tracer lab demonstrating how a Multilayer Switch (MLS) can perform inter-VLAN routing using Switched Virtual Interfaces (SVIs).

## 🎯 Objective

The goal of this lab is to configure multiple VLANs and enable communication between them using a Layer 3 Multilayer Switch.

## 🌐 Network Design

The network contains three VLANs:

| VLAN | Devices | Network | Default Gateway |
|---|---|---|---|
| 10 | Laptops | 192.168.10.0/24 | 192.168.10.1 |
| 20 | PCs | 192.168.20.0/24 | 192.168.20.1 |
| 100 | Servers | 192.168.100.0/24 | 192.168.100.1 |

## ⚙️ Configuration

### VLANs

- VLAN 10 → Laptops
- VLAN 20 → PCs
- VLAN 100 → Servers

### Access Ports

Devices are connected to access ports assigned to their respective VLANs.

### Switched Virtual Interfaces (SVIs)

The Multilayer Switch uses an SVI for each VLAN:

```text
interface vlan 10
 ip address 192.168.10.1 255.255.255.0

interface vlan 20
 ip address 192.168.20.1 255.255.255.0

interface vlan 100
 ip address 192.168.100.1 255.255.255.0
