<img width="1920" height="967" alt="Screenshot (14)" src="https://github.com/user-attachments/assets/beb53bcb-6c54-4d60-8818-4af9ab14fe0b" />
<img width="1920" height="1080" alt="Screenshot (15)" src="https://github.com/user-attachments/assets/40d7d768-e2c5-4d5e-b0ca-cab7fa8e60ec" />
<img width="1920" height="958" alt="Screenshot (16)" src="https://github.com/user-attachments/assets/6a144ead-a95a-4614-ac8e-cb4b9cdfed4a" />
<img width="1920" height="1041" alt="Screenshot (17)" src="https://github.com/user-attachments/assets/303ff4c9-beeb-4f05-8698-e22b794d0752" />
<img width="1920" height="1080" alt="Screenshot (18)" src="https://github.com/user-attachments/assets/0a841dda-d6c5-4f6f-8eb9-4a04ad142679" />
<img width="4000" height="3000" alt="20260428_161414" src="https://github.com/user-attachments/assets/6cbc0449-ee89-4b10-a078-3ef01b77b2f7" />

### Project Overview
This project demonstrates the setup and configuration of a fully functional Active Directory (AD) home lab environment using Oracle VirtualBox. 
The lab simulates a real-world enterprise IT environment where a Domain Controller manages users, groups, and security policies — identical to what IT Support Specialists work with daily in corporate environments.
This hands-on lab was built to develop practical skills in:
Active Directory Domain Services
User account and group management
IT Support troubleshooting in a domain environment

Domain Controller: DC-01 (Windows Server 2019)
Client Machine: Client-01 (Windows 10)
Network Type: VirtualBox Internal Network

Phase 1 — Environment Setup

Step 1 - Install Oracle VirtualBox
Step 2 - Install VirtualBox Extension Pack
Step 3 - Download Windows Server 2019 ISO
Step 4 - Download Windows 10 ISO
Step 5 - Create Domain Controller VM (DC-01)
Step 6 - Install Windows Server 2019
Step 7 - Create Client VM (Client-01)
Step 8 - Install Windows 10 on Client-01

 Active Directory Setup
 Step 9 - Install Active Directory Domain Services

<img width="4000" height="3000" alt="20260428_163801" src="https://github.com/user-attachments/assets/4f1c4a5e-5b71-4672-9bf8-62a384231651" />
<img width="3000" height="4000" alt="20260428_174742" src="https://github.com/user-attachments/assets/b2037b0e-cd7a-4c2d-b530-b323c8ebfd3a" />
<img width="3000" height="4000" alt="20260428_174835" src="https://github.com/user-attachments/assets/bf4f3af1-5648-409e-87e9-576dc9ce79af" />
<img width="3000" height="4000" alt="20260428_174842" src="https://github.com/user-attachments/assets/2fb996a1-0e9b-40f2-9705-b4c1c76f3eb7" />
<img width="3000" height="4000" alt="20260428_174911" src="https://github.com/user-attachments/assets/6901bf97-e982-4838-add0-6170ae1a02cc" />

User and Admin Account Management
Step 10 - Create Organizational Unit (OU)

Opened Active Directory Users and Computers (ADUC) from Server Manager → Tools
Expanded maxtech.local domain
Right-clicked domain → New → Organizational Unit
Created OU named: IT-Admins

Purpose: Organizes admin accounts separately from standard users — reflects real enterprise AD structure

Step 11 - Create Admin User Accounts
Created 3 admin user accounts inside the IT-Admins OU with the following configuration:
Full Name     Username        Role
shivang       shivang123      Admin
shivam        shivam1234      Admin
suresh        suresh12345     Admin

Account Settings applied for each user:

✅ Strong password set (uppercase + lowercase + numbers + special characters)
✅ Password never expires — selected (reflects service account best practice for lab)
✅ Account enabled
✅ User added to Domain Admins group

Steps to create each user:

Right-clicked IT-Admins OU → New → User
Filled First name, Last name, and User logon name
Set password meeting complexity requirements
Checked Password never expires
Clicked Finish to create account

IT Support Tasks Performed

These are real-world IT Support tasks performed inside the lab — identical to daily tasks in a corporate IT environment:

Task 1 — Password Reset

Scenario: User forgot domain account password
Action: ADUC → Right-clicked user → Reset Password → Set new temporary password → Checked User must change password at next logon
Skill demonstrated: L1 IT Support — most common daily task

Task 2 — Unlock User Account

Scenario: User locked out after multiple failed login attempts
Action: ADUC → User Properties → Account tab → Checked Unlock account → Applied
Skill demonstrated: Account management and helpdesk troubleshooting

Task 3 — Create New User Account

Scenario: New employee joining the organization
Action: Created new user in appropriate OU → Set password → Assigned to correct security group
Skill demonstrated: Onboarding workflow and AD user provisioning

Task 4 — Disable User Account

Scenario: Employee left the organization — account must be disabled immediately
Action: ADUC → Right-clicked user → Disable Account
Skill demonstrated: IT Security — offboarding procedure

Task 5 — Remote Desktop Connection

Scenario: User reported issue on their machine — remote access needed for troubleshooting
Action: Used Remote Desktop Connection (RDP) from DC-01 to connect to Client-01 (192.168.1.10) using domain admin credentials
Skill demonstrated: Remote support — critical for IT helpdesk roles

What I Learned

How enterprises use Active Directory to centrally manage thousands of users and computers
The complete lifecycle of a user account — creation, management, and deactivation
How Domain Controllers authenticate users across a network
Why Organizational Units are used to organize and apply policies to groups of users
How IT Support specialists use ADUC daily for password resets, account unlocks, and user management
The importance of the Domain Admin role and why it must be carefully controlled in real environments


About Me
B.Tech Computer Science & IT | Google IT Support Professional Certificate
This project is part of my IT Support portfolio demonstrating hands-on skills in enterprise technologies used in real corporate environments.





 


