# VirtualBox Setup

## Objective

Prepare a virtualization environment for a Windows Server Active Directory lab.

## Host Specifications

RAM: 24 GB
CPU: Intel i7-9700
Storage Available: ~210 GB

## Software

- Oracle VirtualBox
- Windows Server 2022 Evaluation ISO
- Windows 11 ISO

## Notes

Initially used NAT networking.

Created a dedicated NAT Network in VirtualBox so DC01 and CLIENT01 could communicate on the same virtual network.

Both virtual machines were later connected to the same NAT Network.

