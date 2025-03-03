# **Project Overview: Azure Active Directory Implementation**

This project showcases the step-by-step process of setting up and securing an **Azure-based Active Directory (AD) environment**. 

## **1. Initial Azure Infrastructure Setup**
- 🚀 **Creating & Configuring** the **Domain Controller VM**
  - Provision a Windows Server VM in Azure.
  - Assign a static IP address to the VM.
  - Install necessary updates and roles.
- 🌐 Setting up **necessary networking components**
  - Create a Virtual Network (VNet) with appropriate subnets.
  - Configure Network Security Groups (NSGs) to control traffic.
  - Set up DNS to point to the Domain Controller.
- 🏗️ Establishing the **foundation for AD services**
  - Ensure the Domain Controller has a reliable connection.
  - Verify that time synchronization is configured correctly.

## **2. Active Directory Implementation**
- 🛠️ **Installing & Configuring** **Active Directory Domain Services (AD DS)**
  - Install the AD DS role on the Domain Controller.
  - Promote the server to a Domain Controller.
- 🏢 Creating an **organizational structure**:
  - 📂 **Admin Organizational Unit (OU)**
    - Create an OU for administrative accounts.
    - Apply Group Policies specific to administrators.
  - 📂 **Employees Organizational Unit (OU)**
    - Create an OU for employee accounts.
    - Apply Group Policies specific to employees.
- 💻 **Client System Integration** into the domain
  - Join client machines to the domain.
  - Configure client machines to use the Domain Controller for DNS.
- 🖥️ Configuring **Remote Desktop Access**
  - Enable Remote Desktop on the Domain Controller and client machines.
  - Configure Remote Desktop Gateway if needed.

## **3. User Management Automation**
- ⚡ **PowerShell Scripting** for **bulk user creation**
  - Write PowerShell scripts to create user accounts in bulk.
  - Include parameters for user attributes like name, department, and email.
- ✅ **Account Verification & Testing**
  - Verify that user accounts are created correctly.
  - Test logins and permissions for a sample of the created users.
- 🔐 **Security Group Management**
  - Create security groups for different departments or roles.
  - Assign users to appropriate groups based on their roles.

## **4. Security Implementation**
- 🔒 **Account Lockout Policies**
  - Define policies for account lockout thresholds and durations.
- 🚫 **Login Attempt Restrictions**
  - Set up restrictions on the number of failed login attempts.
- 📁 **Comprehensive File Share Permissions**
  - Configure file share permissions based on security groups.
- 👥 **Group-Based Access Control**
  - Implement group-based access control for resources.
- 🔎 **Security Log Event Viewer**
  - Monitor security logs for suspicious activities.

---

This project demonstrates **efficient Active Directory deployment, automation, and security best practices** within an Azure environment.


## **Table of Contents**
1. [Preparing AD Infrastructure in Azure](#preparing-ad-infrastructure-in-azure)
2. [Deploying Active Directory](#deploying-active-directory)
3. [Creating Users with PowerShell](#creating-users-with-powershell)
4. [Group Policy and Managing Accounts](#group-policy-and-managing-accounts)
5. [Network File Shares and Permissions](#network-file-shares-and-permissions)
6. [User Management in Active Directory](#user-management-in-active-directory)
7. [Security Log Event Viewer](#security-log-event-viewer)
8. [Conclusion](#conclusion)

---

## **Preparing AD Infrastructure in Azure**
Before deploying Active Directory, the necessary infrastructure must be set up in Azure.

### **Step 1: Creating Virtual Machines**
- One **Domain Controller (Server)**
  - Provision a Windows Server VM in Azure.
  - Assign a static IP address to the VM.
  - Install necessary updates and roles.
- One **Client Machine**
  - Provision a Windows 10 VM in Azure.
  - Configure the VM to join the domain.

<img src="https://github.com/user-attachments/assets/785e3d7d-0ac6-41a0-8676-63ea9d41d95f" width="600" height="500">

### **Step 2: Configuring Networking Components**
- Ensuring proper communication between VMs.
  - Configure the Virtual Network (VNet) with appropriate subnets.
  - Set up Network Security Groups (NSGs) to control traffic.
- Setting up the Virtual Network.
  - Create a VNet with subnets for Domain Controllers, clients, and other services.
  - Ensure DNS settings point to the Domain Controller.

<img src="https://github.com/user-attachments/assets/3694399b-b7bb-4c84-890e-3b3396de4b57" width="600" height="500">
<img src="https://github.com/user-attachments/assets/bad88670-b696-4aba-9b88-4a429cdd1409" width="600" height="500">

---

## **Deploying Active Directory**
### **Step 1: Installing Active Directory Domain Services (AD DS)**
- Install the AD DS role on the Domain Controller.
  - Open Server Manager and add the AD DS role.
  - Follow the wizard to complete the installation.

<img src="https://github.com/user-attachments/assets/52252559-9e3f-4122-b804-4d92d260d738" width="600" height="500">
<img src="https://github.com/user-attachments/assets/13aabad0-3d0e-4bc6-8539-8359b5879be8" width="600" height="500">

### **Step 2: Promoting the Server to a Domain Controller**
- Promote the server to a Domain Controller.
  - Configure the server as a new forest.
  - Set the domain name and NetBIOS name.
  - Provide Directory Services Restore Mode (DSRM) password.

<img src="https://github.com/user-attachments/assets/3ae3dce7-1e7c-420c-a69f-f01f05d90780" width="600" height="500">

### **Step 3: Creating Organizational Units (OUs)**
- **Admin OU**
  - Create an OU for administrative accounts.
  - Apply Group Policies specific to administrators.
- **Employees OU**
  - Create an OU for employee accounts.
  - Apply Group Policies specific to employees.

<img src="https://github.com/user-attachments/assets/12216fce-ea5d-43bc-9851-6101f04d61db" width="600" height="500">
<img src="https://github.com/user-attachments/assets/b47cb77f-212c-45ee-8780-a944a341c257" width="600" height="500">
<img src="https://github.com/user-attachments/assets/e13705a1-b82c-42b4-8ccf-423c48ed0ce6" width="600" height="500">

### **Step 4: Joining a Client to the Domain**
- Join client machines to the domain.
  - Configure the client machine to use the Domain Controller for DNS.
  - Join the domain using the system properties.

<img src="https://github.com/user-attachments/assets/267c3f8b-430e-44a8-b8da-87c94205a1f7" width="600" height="500">
<img src="https://github.com/user-attachments/assets/0bac07c3-c57a-46c1-aa7f-05c7284a3d9a" width="600" height="500">

### **Step 5: Configuring Remote Desktop Access**
- Enable Remote Desktop on the Domain Controller and client machines.
  - Configure Remote Desktop Gateway if needed.

<img src="https://github.com/user-attachments/assets/d72d8d26-400b-479d-b8de-a42408e4f5fb" width="600" height="500">
<img src="https://github.com/user-attachments/assets/1c9a7fe3-2931-4fca-85e4-2004f9510dff" width="600" height="500">

---

## **Creating Users with PowerShell**
### **Automating User Creation**
- Write PowerShell scripts to create user accounts in bulk.
  - Include parameters for user attributes like name, department, and email.
 <img src="https://github.com/user-attachments/assets/6ac62a49-8bc1-4eef-ac27-cfa5aea638d6" width="750" height="500">
 
- Verify that user accounts are created correctly.
  - Test logins and permissions for a sample of the created users.

<img src="https://github.com/user-attachments/assets/1f3416df-1a9b-4604-8a35-fcdbb3c7a84e" width="750" height="500">

### **Verifying User Accounts**
- Verify that user accounts are created correctly.
  - Test logins and permissions for a sample of the created users.

<img src="https://github.com/user-attachments/assets/cc4f1fe1-447c-4648-a5a8-f1ae685ccb52" width="750" height="500">

---

## **Group Policy and Managing Accounts**
### **Account Lockout Policies**
#### **Login Attempt Restrictions**
- Set up restrictions on the number of failed login attempts.
  - Configure account lockout thresholds and durations.

<img src="https://github.com/user-attachments/assets/7bb19996-6c85-4075-82d6-5b3c998762cc" width="750" height="500">

#### **Configuring Account Lockout Settings**
- Define policies for account lockout thresholds and durations.
  - Configure account lockout thresholds and durations.

<img src="https://github.com/user-attachments/assets/822eb9f2-a0c0-4bcd-9418-01d01e8d95b1" width="750" height="500">
<img src="https://github.com/user-attachments/assets/60fc272f-c364-45f1-b78e-a0c584a4b25f" width="750" height="500">

#### **Account Lockout Demonstration**
- Demonstrate the account lockout process.
  - Show the steps to lock and unlock an account.

<img src="https://github.com/user-attachments/assets/dec200d2-b0fe-48b2-a489-7110459d40cf" width="750" height="500">

### **Account Unlocking Procedure**
- Show the steps to unlock an account.
  - Use Active Directory Users and Computers (ADUC) to unlock accounts.

<img src="https://github.com/user-attachments/assets/87b7c16d-f6e1-4774-ac68-e4bca258539a" width="750" height="500">
<img src="https://github.com/user-attachments/assets/74a7f6f8-1b9c-4497-b175-dac29a77616e" width="750" height="500">

---

## **Network File Shares and Permissions**
### **Configuring Permission Levels**
- Configure file share permissions based on security groups.
  - Create shared folders and assign permissions.

<img src="https://github.com/user-attachments/assets/3870ec3e-f236-4ec1-9d78-0d7062e9e7ab" width="750" height="500">

## **Read, Write, and Restricted Access Settings**
### Read-Access: Domain users can view files only
- Configure read-only access for domain users.
  - Use NTFS permissions to restrict access.

<img src="https://github.com/user-attachments/assets/4e1ff17d-0022-4858-8b8c-7b33e5b74c7e" width="750" height="500">
<img src="https://github.com/user-attachments/assets/1a300c0a-382d-4841-956d-7def3b7de417" width="750" height="500">
<img src="https://github.com/user-attachments/assets/cf74b76e-b9aa-4339-97c5-dc7efe7030d2" width="750" height="500">

### Write-Access: Specific groups can modify files
- Configure write access for specific groups.
  - Use NTFS permissions to allow modifications.

<img src="https://github.com/user-attachments/assets/d08e1232-95d2-4b9d-a041-f4e9f12f6ffa" width="750" height="500">
<img src="https://github.com/user-attachments/assets/32c7ec74-5c57-47ba-b3f2-3ccdbe351534" width="750" height="500">
<img src="https://github.com/user-attachments/assets/68609839-afbd-4117-bc84-d88891638fb9" width="750" height="500">

### Restricted Access: Admin-only areas
- Configure restricted access for administrators.
  - Use NTFS permissions to restrict access to admin areas.

<img src="https://github.com/user-attachments/assets/58548888-50b8-47f8-91fd-6b819605c2ff" width="750" height="500">
<img src="https://github.com/user-attachments/assets/c65d0447-45d7-4383-9f26-f5ef0dc56eb0" width="750" height="500">

### **Group-Based Access Control**
- Implement group-based access control for resources.
  - Assign permissions based on security groups.

<img src="https://github.com/user-attachments/assets/059ebad0-48ad-492f-ac78-223faf8756a2" width="750" height="500">
<img src="https://github.com/user-attachments/assets/10843954-cf54-4a20-b92a-559ff7791ea7" width="750" height="500">
<img src="https://github.com/user-attachments/assets/e6387d57-03ef-4781-bb54-a7be7fb6a9f7" width="750" height="500">
<img src="https://github.com/user-attachments/assets/84c9304b-395c-47c8-9f0b-10d0db497f5f" width="750" height="500">
<img src="https://github.com/user-attachments/assets/a54b1186-8669-4851-a3da-e7e0de5faf0c" width="750" height="500">
<img src="https://github.com/user-attachments/assets/b5f8bae1-672f-45d9-bc55-a5298ec2833e" width="750" height="500">

---

## **User Management in Active Directory**
### **Enabling and Disabling Accounts**
- Enable and disable user accounts in Active Directory.
  - Use Active Directory Users and Computers (ADUC) to manage accounts.

<img src="https://github.com/user-attachments/assets/159fa866-0f22-4475-9639-2cb68127cc12" width="750" height="500">
<img src="https://github.com/user-attachments/assets/a2f7bac6-3777-4703-ae40-4baf23a9d618" width="750" height="500">
<img src="https://github.com/user-attachments/assets/b8263ff5-9365-474b-bca7-ae73563c968c" width="750" height="500">

---

## **Security Log Event Viewer**
Monitoring **user activity, login attempts, and security events** is a critical part of Active Directory management. **Windows Event Viewer** provides detailed logs for security auditing.

### **Searching for User Logs in Event Viewer**
- **Objective**: Searching for the logs of a specific user, **Devima**, within **Event Viewer** on the **Domain Controller**.
- **Steps**:
  1. Open **Event Viewer** on the Domain Controller.
  2. Navigate to **Windows Logs > Security**.
  3. Use the **Find** function to locate logs related to the user.

#### **Log Screenshot: Searching for Devima's Logs**
<img src="https://github.com/user-attachments/assets/48170774-a173-4016-921d-9db22bbfbb88" width="750" height="500">

---

### **Failed Login Attempts in Event Viewer**
- **Objective**: Checking **audit failures** related to login attempts for the user **Devima**.
- **Steps**:
  1. Navigate to **Windows Logs > Security** in **Event Viewer**.
  2. Look for **Event ID 4776 (Credential Validation Failure)**.
  3. Analyze failure reasons and timestamps.

#### **Log Screenshot: Failed Login Attempts for Devima**
<img src="https://github.com/user-attachments/assets/871bd9a4-ed62-4810-ad40-f4e3861391f4" width="750" height="500">

---

# 🎯 **Conclusion**

## **Thank You for Viewing My Active Directory Project!**

Thank you for taking the time to explore my **Active Directory infrastructure project**. This implementation showcases the **practical application of enterprise-level identity and access management in an Azure environment**.

💡 This **hands-on project** reflects real-world scenarios and **best practices** in Active Directory management. It serves as both a **learning resource** and a **practical reference** for similar implementations.

---

## 🤝 **Connect With Me**
💬 If you have **questions** about the implementation or would like to **discuss Active Directory configurations**, feel free to reach out! I'm always interested in discussions on:
- 🔐 **IT Security Best Practices**
- ☁️ **Cloud Solutions**
- 🏗️ **Enterprise IT Infrastructure**

---

**📌 Project Completed By:**  
**📝 Richard Hood Jr.**
