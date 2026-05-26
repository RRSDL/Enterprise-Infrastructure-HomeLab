# NTFS Permissions

## Objective

Restrict folder access by department using security groups.

## Folder Structure

C:\Shares
│
├── HR
├── IT
└── Finance

## Initial Problem

HR users could access Finance resources.

## Cause

Folder permissions were inherited.

The group:

HOMELAB\Users

still had access.

## Resolution

1. Open folder properties
2. Security tab
3. Advanced
4. Disable inheritance
5. Select:

Convert inherited permissions into explicit permissions

6. Remove:

HOMELAB\Users

7. Keep:

- SYSTEM
- Administrators
- Department Security Group

Examples:

HR Folder

- SYSTEM
- Administrators
- HR-Users

IT Folder

- SYSTEM
- Administrators
- IT-Users

Finance Folder

- SYSTEM
- Administrators
- Finance-Users

## Result

Department access properly restricted.

Examples:

hr.john
✔ HR
✖ IT
✖ Finance

it.support
✔ IT
✖ HR
✖ Finance

fin.anna
✔ Finance
✖ HR
✖ IT

## Lessons Learned

Disable inheritance carefully.

Prefer:

Convert inherited permissions into explicit permissions

instead of removing all permissions.

Assign permissions to groups, not users.