# Enterprise Multi-Site Network Design

A multi-site enterprise network designed and implemented in Cisco Packet Tracer, connecting three branch offices with VLAN segmentation, dynamic routing, and ACL-based security policy enforcement.

![Network Topology Diagram](network-design-diagram.png,network-design-diagram-.png)

## Overview

Small-to-mid-sized businesses running flat, unsegmented networks face two recurring problems: broadcast traffic slowing everything down, and no isolation between departments. This project solves both by building a segmented, dynamically-routed, security-enforced network topology connecting three branch offices.

## What I Built

- Designed a hierarchical, multi-router, multi-switch network topology connecting three branch offices using Cisco ISR routers and Layer 2 switches
- Implemented IPv4 subnetting on the 192.168.1.0/24 network
- Configured VLAN segmentation — VLAN 10 (Sales), VLAN 20 (HR), VLAN 30 (IT) — with Inter-VLAN Routing
- Set up DHCP pools for automatic IP address allocation to client devices
- Implemented OSPF (Area 0) across 5 routers for dynamic routing and automatic failover, replacing static routing entirely for improved resilience
- Configured NAT for external network access
- Applied Standard and Extended ACLs to enforce a real security policy:
  - Blocked the HR VLAN from accessing the Server Network entirely
  - Restricted the Sales VLAN to HTTP and ICMP traffic only when reaching the Server Network
- Verified full neighbor adjacency, route convergence, VLAN communication, and ACL behavior using Cisco IOS `show` commands, `ping`, and `traceroute`

## Technologies Used

`Cisco Packet Tracer` `Cisco IOS` `OSPF` `Static Routing` `VLAN` `Inter-VLAN Routing` `DHCP` `ACL (Standard & Extended)` `NAT` `IPv4 Subnetting` `TCP/IP`

## Key Highlights

- Least-privilege network security policy enforced at the ACL level, not just perimeter firewalling
- Dynamic routing (OSPF) provides automatic failover — verified by testing route reconvergence
- Fully verified, not just configured — every routing and access decision tested with real diagnostic commands

---
📄 Full write-up and diagram also available on my [portfolio](https://rohanportfolio.online)
