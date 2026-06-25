# AD Enterprise Lab Build Log

## Completed

✓ Installed Windows Server 2022

✓ Configured static IP address

✓ Installed Active Directory Domain Services

✓ Installed DNS Server

✓ Promoted DC01 to Domain Controller

✓ Created homelab.local

✓ Created Organizational Units

✓ Created users

✓ Created security groups

✓ Added users to groups

✓ Created shared folders

✓ Configured NTFS permissions

✓ Installed Windows 11

✓ Joined CLIENT01 to domain

✓ Logged in using domain accounts

✓ Configured DHCP Server

✓ Configured DHCP Scope

✓ Configured DNS Resolution

✓ Implemented GPO Restrictions

✓ Verified DHCP Client Leasing

✓ Performed GPO Troubleshooting

✓ Started PowerShell AD Administration

✓ Queried Users, Groups and OUs using PowerShell

✓ Managed Group Membership using PowerShell

## Current Environment

DC01
Role:
- Domain Controller
- DNS Server

CLIENT01
Role:
- Domain-Joined Workstation

Domain:
homelab.local

## Current Status

Environment operational.

Authentication functioning.

Department access restrictions functioning.

## Next Steps

- Create users using PowerShell
- Create groups using PowerShell
- Automate user provisioning
- Perform bulk user creation via CSV
- Document PowerShell automation tasks
- Continue screenshot collection for project portfolio

## Issues Encountered & Resolutions
GPO Restriction Applied to Administrator Account

Issue:
Control Panel and Network Connections (ncpa.cpl) could not be opened on DC01 while logged in as Administrator.

Investigation:
Used:

gpresult /r

to identify applied Group Policies.

Finding:
The Corporate Desktop Policy was applied and contained the setting:

Prevent access to Control Panel and PC settings

Resolution:
Disabled the setting within the Corporate Desktop Policy and refreshed policies using:

gpupdate /force

Result:
Control Panel and Network Connections became accessible again.

Lessons Learned:

Use gpresult /r to troubleshoot Group Policy issues.
Validate GPO scope before applying restrictions.
Test restrictive policies using non-administrative accounts first.