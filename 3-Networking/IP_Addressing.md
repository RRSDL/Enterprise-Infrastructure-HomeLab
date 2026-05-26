# IP Address Configuration

## Objective

Assign a static IP address to the Domain Controller.

## Configuration

Server: DC01

IP Address:
10.0.2.10

Subnet Mask:
255.255.255.0

Default Gateway:
10.0.2.1

Preferred DNS:
10.0.2.10

## Why

Domain Controllers should use static IP addresses.

Clients rely on the Domain Controller for:

- DNS
- Authentication
- Active Directory services

If the IP changes unexpectedly, clients may not be able to locate domain services.