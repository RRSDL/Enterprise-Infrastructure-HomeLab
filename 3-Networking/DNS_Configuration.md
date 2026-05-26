# DNS Configuration

## Objective

Configure DNS for Active Directory.

## Domain Controller

DC01 acts as the DNS Server.

DNS Address:

10.0.2.10

## Client Configuration

CLIENT01 DNS Server:

10.0.2.10

## Why

Active Directory depends heavily on DNS.

Without correct DNS configuration:

- Domain Join fails
- Authentication fails
- Group Policy may fail

## Result

CLIENT01 successfully located and joined the domain.