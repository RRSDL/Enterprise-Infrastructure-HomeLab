
# DHCP Troubleshooting - VirtualBox Conflict

## Description
This document covers troubleshooting steps performed to resolve DHCP assignment issues in the HomeLab environment, specifically due to conflicting DHCP services from VirtualBox NAT Network.

---

## Issue
Client received incorrect IP address outside DHCP scope (10.0.2.4 instead of 10.0.2.100–200 range).

---

## Symptoms
- CLIENT01 assigned incorrect IP
- DHCP server shown as 10.0.2.2 instead of DC01
- DHCP scope not being used

---

## Root Cause
VirtualBox NAT Network DHCP service was enabled, causing conflict with Windows Server DHCP.

---

## Resolution Steps
- Disabled VirtualBox NAT DHCP service
- Restarted virtual machines
- Released and renewed IP address on CLIENT01

Commands used:
```cmd
ipconfig /release
ipconfig /renew
# DHCP Troubleshooting - VirtualBox Conflict

## Description
This document covers troubleshooting steps performed to resolve DHCP assignment issues in the HomeLab environment, specifically due to conflicting DHCP services from VirtualBox NAT Network.

---

## Issue
Client received incorrect IP address outside DHCP scope (10.0.2.4 instead of 10.0.2.100–200 range).

---

## Symptoms
- CLIENT01 assigned incorrect IP
- DHCP server shown as 10.0.2.2 instead of DC01
- DHCP scope not being used

---

## Root Cause
VirtualBox NAT Network DHCP service was enabled, causing conflict with Windows Server DHCP.

---

## Resolution Steps
- Disabled VirtualBox NAT DHCP service
- Restarted virtual machines
- Released and renewed IP address on CLIENT01

Commands used:
```cmd
ipconfig /release
ipconfig /renew