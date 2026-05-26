# Domain Controller Promotion

## Objective

Create a new Active Directory domain.

## Domain

homelab.local

## Steps

1. Open Server Manager
2. Click notification flag
3. Select:

Promote this server to a domain controller

4. Choose:

Add a new forest

5. Enter:

homelab.local

6. Configure DSRM password
7. Complete promotion wizard
8. Restart server

## Result

DC01 became the first Domain Controller for homelab.local.