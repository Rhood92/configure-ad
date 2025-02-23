# Active Directory (AD) Infrastructure & Management in Azure

A comprehensive guide on setting up and managing Active Directory in an Azure environment.

## Features

- Active Directory Infrastructure Setup in Azure
- Active Directory Deployment and Configuration
- Automated User Creation with PowerShell
- Group Policy and Account Management
- Network File Shares and Permission Management
- Event Logging and Security Monitoring

## Table of Contents

1. [Preparing AD Infrastructure in Azure](#preparing-ad-infrastructure-in-azure)
2. [Deploying Active Directory](#deploying-active-directory)
3. [Creating Users with PowerShell](#creating-users-with-powershell)
4. [Group Policy and Managing Accounts](#group-policy-and-managing-accounts)
5. [Network File Shares and Permissions](#network-file-shares-and-permissions)
6. [Event Logging and Security](#event-logging-and-security)
7. [User Management in Active Directory](#user-management-in-active-directory)
8. [Final Tests and Validation](#final-tests-and-validation)
9. [Conclusion](#conclusion)

## Preparing AD Infrastructure in Azure

Before deploying AD, the infrastructure needs to be prepared in Azure. This includes:
- Creating a Virtual Machine (VM)
- Configuring the VM as an Active Directory Domain Controller
- Setting up necessary networking components

![Preparing AD Infrastructure](./images/01-ad-infrastructure.png)

## Deploying Active Directory

The deployment process includes:
- Installing Active Directory Domain Services (AD DS)
- Promoting the server to a Domain Controller
- Configuring DNS and domain settings

![Deploying AD](./images/02-deploying-ad.png)

## Creating Users with PowerShell

PowerShell automation is used for efficient user creation and management.

## Group Policy and Managing Accounts

### Account Lockout Policy
Implementation of security-focused account policies including:
- Login attempt restrictions
- Account lockout duration settings
- Password complexity requirements

![Account Lockout Policy](./images/account_lockout_policy.png)

### Account Management
Using Active Directory Users and Computers (ADUC) for:
- Account unlocking
- Permission management
- User profile configuration

![Unlocking Account](./images/unlock_account.png)

## Network File Shares and Permissions

### Permission Levels
Three primary access levels are configured:
- Read-Access: Domain users can view files
- Write-Access: Specific groups can modify files
- Restricted Access: Admin-only areas

![Folder Permissions](./images/folder_permissions.png)

### Permission Configuration
Detailed setup of:
- Advanced Sharing settings
- NTFS permissions
- Access control lists

## Event Logging and Security

### Security Monitoring
Implementation of comprehensive logging:
- Login attempt tracking
- Security event monitoring
- Policy violation alerts

![Failed Logins](./images/failed_logins.png)
![Event Logs](./images/event_logs.png)

## User Management in Active Directory

### Account Management
Procedures for:
- Account enabling/disabling
- Security group management
- Role-based access control

![Disabling Account](./images/disable_account.png)
![Security Groups](./images/security_groups.png)

## Final Tests and Validation

### Access Testing Results
Comprehensive testing of:
- No-Access restrictions
- Read-Only permissions
- Write Access capabilities
- Full Access privileges

![No Access](./images/no_access.png)
![Read-Only Test](./images/read_only_test.png)
![Write Access Test](./images/write_access_test.png)
![Full Access Test](./images/full_access_test.png)

## Conclusion

This project successfully demonstrates:
- Active Directory deployment in Azure
- Automated user management
- Security policy implementation
- Access control configuration
- Security monitoring setup

### Future Enhancements

Planned improvements include:
- Multi-Factor Authentication (MFA) implementation
- Azure AD Connect integration
- Additional security policy automation

## Contributing

Feel free to contribute to this project by submitting pull requests or creating issues for any improvements you'd like to suggest.

## License

[Add your chosen license here]

---

**Note**: This repository serves as a practical guide for setting up and managing Active Directory in Azure while implementing security best practices.
