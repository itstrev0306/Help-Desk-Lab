
# Helpdesk Simulation Project

This project emulates the role of an IT helpdesk technician by setting up a virtual environment that integrates **Active Directory** on an EC2 instance and **ServiceNow** to manage tickets and incidents. The aim was to simulate common helpdesk tasks in a controlled, cloud-based environment for practice and demonstration purposes.

---

## 🛠️ Project Overview

This project includes:

- Provisioning a Windows Server EC2 instance on AWS.
- Installing and configuring **Active Directory Domain Services (AD DS)**.
- Setting up a **developer instance of ServiceNow** for ticket tracking.
- Performing essential helpdesk operations such as:
  - Creating and managing user accounts.
  - Creating and managing security groups.
  - Resetting user passwords.
  - Managing tickets and incidents through ServiceNow.

---

## ☁️ EC2 Instance Setup

### Step 1: Launching the EC2 Instance
- Launched a **Windows Server 2019 Base** EC2 instance via AWS Console.
- Instance type: `t2.medium` (2 vCPU, 4GB RAM).
- Configured key pair for remote access and opened RDP (port 3389) in the security group.

### Step 2: Initial Configuration
- Connected to the instance via Remote Desktop.
- Set static IP via EC2 settings for consistency in DNS and AD use.
- Renamed the computer for easier domain management (`AD-Server`).

---

## 🧱 Active Directory Setup

### Step 1: Installing AD DS
- Installed **Active Directory Domain Services** using Server Manager.
- Promoted the server to a **Domain Controller**.
- Created a new forest with the domain name: `helpdesk.local`.

### Step 2: DNS Configuration
- DNS installed and configured during AD setup.
- Verified forward and reverse lookup zones.

---

## 👤 Active Directory Tasks

### ✔️ Creating Users
Used the **Active Directory Users and Computers (ADUC)** tool to create users:
- Created organizational units (OUs): `IT`, `HR`, `Sales`.
- Added users such as `jdoe`, `asmith` with usernames, email, and password.

### ✔️ Creating Groups
- Created **Security Groups**: `IT_Staff`, `HR_Managers`, `Sales_Team`.
- Assigned users to appropriate groups for access control and policy application.

### ✔️ Resetting Passwords
- Simulated common helpdesk request by resetting passwords via ADUC.
- Enforced “User must change password at next login” for security.

---

## 🧾 ServiceNow Integration

### Step 1: Developer Instance Setup
- Registered for a free **ServiceNow Developer Instance**.
- Selected the **ITSM** (IT Service Management) application for ticket handling.

### Step 2: Ticket Management
- Created simulated incidents like:
  - *User locked out of account.*
  - *Password reset request.*
  - *Access request for shared folder.*

Each ticket included:
- User details.
- Description of issue.
- Resolution steps (e.g., reset password, unlocked user, added to group).

---

## 📸 Screenshots (Optional)
Include screenshots of:
- ADUC user creation.
- Group assignments.
- ServiceNow incident creation and resolution.
*(Can be added to the repo’s `screenshots/` folder.)*

---

## ✅ Outcomes

By completing this project, I:
- Gained hands-on experience provisioning cloud infrastructure.
- Developed familiarity with Windows Server and Active Directory.
- Practiced core helpdesk tasks and ticket management workflows.

---

## 🔗 Resources Used

- [AWS EC2 Documentation](https://docs.aws.amazon.com/ec2/)
- [Microsoft AD DS Documentation](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/)
- [ServiceNow Developer Site](https://developer.servicenow.com/)
