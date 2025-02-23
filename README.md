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

<img src="https://github.com/user-attachments/assets/785e3d7d-0ac6-41a0-8676-63ea9d41d95f" width="600" height="500">
<img src="https://github.com/user-attachments/assets/3694399b-b7bb-4c84-890e-3b3396de4b57" width="600" height="500">
<img src="https://github.com/user-attachments/assets/bad88670-b696-4aba-9b88-4a429cdd1409" width="600" height="500">


## Deploying Active Directory

## The deployment process includes:

## Step 1: Installing Active Directory Domain Services (AD DS)

<img src="https://github.com/user-attachments/assets/52252559-9e3f-4122-b804-4d92d260d738" width="600" height="500">

<img src="https://github.com/user-attachments/assets/13aabad0-3d0e-4bc6-8539-8359b5879be8" wwidth="600" height="500">

## Step 2: Promoting the server to a Domain Controller

<img src="https://github.com/user-attachments/assets/3ae3dce7-1e7c-420c-a69f-f01f05d90780" width="600" height="500">

## Step 3: Creating Organizational Units (Admin and Employees)
<img src="https://github.com/user-attachments/assets/12216fce-ea5d-43bc-9851-6101f04d61db" width="600" height="500">


<img src="https://github.com/user-attachments/assets/b47cb77f-212c-45ee-8780-a944a341c257" width="600" height="500">
<img src="https://github.com/user-attachments/assets/e13705a1-b82c-42b4-8ccf-423c48ed0ce6" width="600" height="500">

## Step 4: Joining Client 1 in the Domain
<img src="https://github.com/user-attachments/assets/267c3f8b-430e-44a8-b8da-87c94205a1f7" width="600" height="500">
<img src="https://github.com/user-attachments/assets/0bac07c3-c57a-46c1-aa7f-05c7284a3d9a" width="600" height="500">

## Step 5: Logging into client 1 as an Admin to give all users access to the remote desktop 
<img src="https://github.com/user-attachments/assets/d72d8d26-400b-479d-b8de-a42408e4f5fb" width="600" height="500">
<img src="https://github.com/user-attachments/assets/1c9a7fe3-2931-4fca-85e4-2004f9510dff" width="600" height="500">


## Creating Users with PowerShell

PowerShell automation is used for efficient user creation and management. //Didn't do this yet, this is for later

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
