# Active Directory (AD) Infrastructure & Management in Azure

A comprehensive guide on setting up and managing Active Directory in an Azure environment.

# Features

- Active Directory Infrastructure Setup in Azure
- Active Directory Deployment and Configuration
- Automated User Creation with PowerShell
- Group Policy and Account Management
- Network File Shares and Permission Management
- Event Logging and Security Monitoring

# Table of Contents

1. [Preparing AD Infrastructure in Azure](#preparing-ad-infrastructure-in-azure)
2. [Deploying Active Directory](#deploying-active-directory)
3. [Creating Users with PowerShell](#creating-users-with-powershell)
4. [Group Policy and Managing Accounts](#group-policy-and-managing-accounts)
5. [Network File Shares and Permissions](#network-file-shares-and-permissions)
6. [Event Logging and Security](#event-logging-and-security)
7. [User Management in Active Directory](#user-management-in-active-directory)
8. [Final Tests and Validation](#final-tests-and-validation)
9. [Conclusion](#conclusion)

# Preparing AD Infrastructure in Azure

Before deploying AD, the infrastructure needs to be prepared in Azure. This includes:

### Step 1: Creating a Virtual Machine (VM)
<img src="https://github.com/user-attachments/assets/785e3d7d-0ac6-41a0-8676-63ea9d41d95f" width="600" height="500">

### Step 2: Setting up necessary networking components
<img src="https://github.com/user-attachments/assets/3694399b-b7bb-4c84-890e-3b3396de4b57" width="600" height="500">
<img src="https://github.com/user-attachments/assets/bad88670-b696-4aba-9b88-4a429cdd1409" width="600" height="500">


# Deploying Active Directory

## The deployment process includes:

### Step 1: Installing Active Directory Domain Services (AD DS)

<img src="https://github.com/user-attachments/assets/52252559-9e3f-4122-b804-4d92d260d738" width="600" height="500">

<img src="https://github.com/user-attachments/assets/13aabad0-3d0e-4bc6-8539-8359b5879be8" wwidth="600" height="500">

### Step 2: Promoting the server to a Domain Controller

<img src="https://github.com/user-attachments/assets/3ae3dce7-1e7c-420c-a69f-f01f05d90780" width="600" height="500">

### Step 3: Creating Organizational Units (Admin and Employees)
<img src="https://github.com/user-attachments/assets/12216fce-ea5d-43bc-9851-6101f04d61db" width="600" height="500">


<img src="https://github.com/user-attachments/assets/b47cb77f-212c-45ee-8780-a944a341c257" width="600" height="500">
<img src="https://github.com/user-attachments/assets/e13705a1-b82c-42b4-8ccf-423c48ed0ce6" width="600" height="500">

### Step 4: Joining Client 1 in the Domain
<img src="https://github.com/user-attachments/assets/267c3f8b-430e-44a8-b8da-87c94205a1f7" width="600" height="500">
<img src="https://github.com/user-attachments/assets/0bac07c3-c57a-46c1-aa7f-05c7284a3d9a" width="600" height="500">

### Step 5: Logging into client 1 as an Admin to give all users access to the remote desktop 
<img src="https://github.com/user-attachments/assets/d72d8d26-400b-479d-b8de-a42408e4f5fb" width="600" height="500">
<img src="https://github.com/user-attachments/assets/1c9a7fe3-2931-4fca-85e4-2004f9510dff" width="600" height="500">


# Creating Users with PowerShell

## PowerShell automation is used for efficient user creation and management.

<img src="https://github.com/user-attachments/assets/6ac62a49-8bc1-4eef-ac27-cfa5aea638d6" width="750" height="500">
<img src="https://github.com/user-attachments/assets/1f3416df-1a9b-4604-8a35-fcdbb3c7a84e" width="750" height="500">

## Logged into one of the User Accounts

<img src="https://github.com/user-attachments/assets/cc4f1fe1-447c-4648-a5a8-f1ae685ccb52" width="750" height="500">

# Group Policy and Managing Accounts

## Account Lockout Policy
### Implementation of security-focused account policies including:

### Login attempt restrictions

![image](https://github.com/user-attachments/assets/7bb19996-6c85-4075-82d6-5b3c998762cc)

### Account lockout duration settings
![image](https://github.com/user-attachments/assets/822eb9f2-a0c0-4bcd-9418-01d01e8d95b1)
![image](https://github.com/user-attachments/assets/60fc272f-c364-45f1-b78e-a0c584a4b25f)
![image](https://github.com/user-attachments/assets/fe68eac1-dc47-4302-a69a-9db890f97368)

### Too many failed attempts caused an account lockout
![image](https://github.com/user-attachments/assets/dec200d2-b0fe-48b2-a489-7110459d40cf)


# Account Management
## Using Active Directory Users and Computers (ADUC) for:

### Account unlocking
![image](https://github.com/user-attachments/assets/87b7c16d-f6e1-4774-ac68-e4bca258539a)
![image](https://github.com/user-attachments/assets/654fef88-889c-4ea7-a11b-13b2c5c9139c)
![image](https://github.com/user-attachments/assets/33bf72c0-b10e-49ae-aea1-6015c19dd98b)




### Permission management

### User profile configuration

![Unlocking Account](./images/unlock_account.png)

# Network File Shares and Permissions

## Permission Levels
## Three primary access levels are configured:
![image](https://github.com/user-attachments/assets/3870ec3e-f236-4ec1-9d78-0d7062e9e7ab)

### Read-Access: Domain users can view files
![image](https://github.com/user-attachments/assets/4e1ff17d-0022-4858-8b8c-7b33e5b74c7e)
![image](https://github.com/user-attachments/assets/1a300c0a-382d-4841-956d-7def3b7de417)
![image](https://github.com/user-attachments/assets/cf74b76e-b9aa-4339-97c5-dc7efe7030d2)


### Write-Access: Specific groups can modify files
![image](https://github.com/user-attachments/assets/d08e1232-95d2-4b9d-a041-f4e9f12f6ffa)
![image](https://github.com/user-attachments/assets/32c7ec74-5c57-47ba-b3f2-3ccdbe351534)
![image](https://github.com/user-attachments/assets/68609839-afbd-4117-bc84-d88891638fb9)


### Restricted Access: Admin-only areas
![image](https://github.com/user-attachments/assets/58548888-50b8-47f8-91fd-6b819605c2ff)
![image](https://github.com/user-attachments/assets/c65d0447-45d7-4383-9f26-f5ef0dc56eb0)

### Accountants Group Access: Read/Write Acess:
![image](https://github.com/user-attachments/assets/059ebad0-48ad-492f-ac78-223faf8756a2)
![image](https://github.com/user-attachments/assets/10843954-cf54-4a20-b92a-559ff7791ea7)
![image](https://github.com/user-attachments/assets/e6387d57-03ef-4781-bb54-a7be7fb6a9f7)
![image](https://github.com/user-attachments/assets/84c9304b-395c-47c8-9f0b-10d0db497f5f)
![image](https://github.com/user-attachments/assets/a54b1186-8669-4851-a3da-e7e0de5faf0c)
![image](https://github.com/user-attachments/assets/b5f8bae1-672f-45d9-bc55-a5298ec2833e)

# User Management/Security Group Management in Active Directory

## Account Management
## Procedures for:

### Account enabling/disabling
![image](https://github.com/user-attachments/assets/159fa866-0f22-4475-9639-2cb68127cc12)
![image](https://github.com/user-attachments/assets/a2f7bac6-3777-4703-ae40-4baf23a9d618)
![image](https://github.com/user-attachments/assets/b8263ff5-9365-474b-bca7-ae73563c968c)


# Conclusion

This project successfully demonstrates:
- Active Directory deployment in Azure
- Automated user management
- Security policy implementation
- Access control configuration
- Security monitoring setup



