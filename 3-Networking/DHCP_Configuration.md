
# DHCP Configuration - DC01

## Description
This document describes the DHCP service configuration implemented on the Windows Server domain controller (DC01) in the HomeLab environment. It provides automatic IP address assignment and network configuration for domain-joined clients.

---

## Server Details
- DHCP Server: DC01 (10.0.2.10)
- Authorization: Active Directory

---

## Scope Configuration
- Scope Name: Lab Scope
- IP Range: 10.0.2.100 – 10.0.2.200
- Subnet Mask: 255.255.255.0 (/24)
- Lease Duration: 8 Days

---

## DHCP Options
- Default Gateway: 10.0.2.1
- DNS Server: 10.0.2.10
- Domain Name: homelab.local

---

## Client Validation (CLIENT01)
- IP Address: 10.0.2.100
- Gateway: 10.0.2.1
- DNS: 10.0.2.10
- DHCP Server: DC01 (10.0.2.10)

---

## Summary
DHCP is successfully integrated with Active Directory and DNS services, providing centralized IP management for all clients.