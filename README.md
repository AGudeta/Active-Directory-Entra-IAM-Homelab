# Active Directory & Microsoft Entra ID IAM Homelab

## Project Overview

Built a hands-on Identity and Access Management (IAM) homelab to simulate enterprise user administration, access control, and identity security operations.

The project includes an on-premises Active Directory environment and a separate Microsoft Entra ID cloud environment.

## Technologies Used

- Windows Server 2025
- Active Directory Domain Services (AD DS)
- Microsoft Entra ID
- Windows 11 Pro
- PowerShell
- Group Policy
- Oracle VirtualBox

## Lab Architecture

### On-Premises Environment

| Component | Configuration |
|---|---|
| Domain Controller | DC01 — Windows Server 2025 |
| Domain | corp.homelab.test |
| Workstation | CLIENT01 — Windows 11 Pro |
| Departmental OUs | IT, HR, Finance |
| Security Groups | SG_IT, SG_HR, SG_Finance |

The domain controller provides Active Directory Domain Services and DNS. CLIENT01 is joined to the domain for testing authentication and access permissions.

### Cloud Environment

Configured a personal Microsoft Entra ID tenant for cloud identity administration, including user provisioning, security groups, password resets, account disablement, and audit log review.

**Current status:** On-premises Active Directory and Microsoft Entra ID are managed separately. Hybrid identity synchronization has not yet been implemented.

## Implemented IAM Features

### 1. Active Directory User Administration
- Created employee accounts and organized them into departmental organizational units.
- Configured department-based security group membership.
- Enabled and disabled user accounts using PowerShell.

### 2. Role-Based Access Control
- Created departmental shared folders.
- Configured NTFS permissions based on security group membership.
- Tested access revocation and restoration by changing group membership.

### 3. Group Policy and Account Security
- Configured an account lockout policy of five failed attempts.
- Configured a workstation inactivity lock policy of 600 seconds.
- Verified policy application using Windows administrative tools.

### 4. Microsoft Entra ID Administration
- Created a cloud-only test user and security group.
- Managed group membership and user account states.
- Performed password resets.
- Reviewed administrative audit logs.

### 5. PowerShell Administration
- Queried Active Directory users.
- Enabled and disabled user accounts.
- Modified security group membership.
- Updated user principal names.

## Security Testing

Validated departmental file access using a domain-joined Windows 11 workstation.

Confirmed that security group membership changes affected access to protected resources.

Reviewed Windows Security events and Microsoft Entra ID audit logs to observe identity administration activities.

## Skills Demonstrated

- Identity and Access Management (IAM)
- Active Directory administration
- Microsoft Entra ID administration
- Role-Based Access Control (RBAC)
- User lifecycle management
- Group Policy
- PowerShell
- Access auditing and troubleshooting

## Future Enhancements

- Hybrid identity synchronization
- Automated user provisioning and deprovisioning
- Additional authentication and identity security controls
