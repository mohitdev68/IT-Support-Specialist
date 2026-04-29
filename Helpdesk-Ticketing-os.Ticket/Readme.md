<img width="1920" height="1080" alt="Screenshot (20)" src="https://github.com/user-attachments/assets/ee9465a6-65ac-4d43-8b67-7a38b5f152bf" />
<img width="1920" height="1080" alt="Screenshot (21)" src="https://github.com/user-attachments/assets/fe0f5eb4-de47-45d2-88a9-b7e784a17a7b" />
<img width="1920" height="1080" alt="Screenshot (22)" src="https://github.com/user-attachments/assets/adcb99f0-6a93-4758-9e75-8bf98f70f2a9" />
<img width="1920" height="1080" alt="Screenshot (23)" src="https://github.com/user-attachments/assets/430fd142-f102-4877-91ff-2c3f4048b9c9" />
<img width="1920" height="1080" alt="Screenshot (24)" src="https://github.com/user-attachments/assets/ff1d0d05-2456-40dd-a4b7-d1b11378b5fb" />
<img width="1920" height="1080" alt="Screenshot (25)" src="https://github.com/user-attachments/assets/290f7cae-2de0-4c5c-841a-c180ddfe1dbb" />
<img width="1920" height="1080" alt="Screenshot (26)" src="https://github.com/user-attachments/assets/99ac8cd1-0976-43d6-9d4d-73cc41d6765c" />
<img width="1920" height="1080" alt="Screenshot (27)" src="https://github.com/user-attachments/assets/deaae84c-4c6a-4ce8-bfa5-2195a42b4f5f" />
<img width="1920" height="1080" alt="Screenshot (28)" src="https://github.com/user-attachments/assets/bcef99d1-f8ef-4823-bc45-48cf4284c706" />
<img width="1920" height="1080" alt="Screenshot (29)" src="https://github.com/user-attachments/assets/61a2ba34-e898-492a-bf0f-3f29d1643dad" />
<img width="1920" height="1080" alt="Screenshot (30)" src="https://github.com/user-attachments/assets/20ea2702-7e13-4dc1-b8c8-14b3b4a59f7d" />

## Project Overview
This project demonstrates the deployment and configuration of a fully functional IT Helpdesk Ticketing System using osTicket — a widely used open source platform that operates on the same principles as enterprise tools like ServiceNow, Jira Service Management, Zendesk, and Freshdesk.
The lab simulates a real-world corporate IT support environment where end users submit support tickets, IT agents receive and manage them, and the full ticket lifecycle is tracked from creation to resolution — identical to how IT Support Specialists operate in companies daily.
Why this project matters for IT Support roles:

90% of IT Support jobs require experience with ticketing systems
Understanding SLA management, ticket prioritization, and escalation is a core L1/L2 skill
Demonstrates practical knowledge of helpdesk workflows without requiring enterprise software access

Step 1 — Download XAMPP

Navigated to the official website: apachefriends.org/download.html
Clicked XAMPP for Windows — downloaded the latest version (~160 MB)
XAMPP provides the complete stack needed to run osTicket:

Apache — web server that hosts the osTicket application
MySQL — database that stores all tickets, users, and configurations
PHP — programming language that osTicket is built on
phpMyAdmin — browser-based database management tool



Step 2 — Install XAMPP

Ran the XAMPP installer as Administrator
Accepted all default settings during installation
XAMPP Control Panel opened automatically after installation
Clicked Start next to Apache — status turned green ✅
Clicked Start next to MySQL — status turned green ✅
Verified installation by opening Chrome and navigating to localhost — XAMPP welcome page confirmed ✅

Step 3 — Create osTicket Database

Opened Chrome → navigated to localhost/phpmyadmin
Clicked New in the left sidebar
Database name: osticket
Collation: utf8_general_ci
Clicked Create — database created successfully ✅

Why this step matters: osTicket stores all ticket data, user accounts, and configurations in a MySQL database. Creating the database manually before installation is standard database administration practice used in enterprise environments.
Step 4 — Download osTicket

Navigated to: osticket.com/download
Clicked Download Free — open source version
Downloaded the ZIP file (~15 MB)

Step 5 — Install osTicket

Extracted the osTicket ZIP file
Located the upload folder inside the extracted files
Copied the upload folder to: *C:\xampp\htdocs*
Renamed the folder from upload to osticket
Navigated to: *C:\xampp\htdocs\osticket\include*
Renamed ost-sampleconfig.php to ost-config.php
Set Full Control permissions on ost-config.php for the installer to write configuration

Step 6 — Secure the Installation

Deleted the setup folder from *C:\xampp\htdocs\osticket* — prevents reinstallation attacks
Set ost-config.php to Read Only — prevents unauthorized configuration changes

 ## Helpdesk Configuration

  Create Departments
Logged into Admin Panel at localhost/osticket/scp
Navigated to: Admin Panel → Agents → Departments → Add New Department
Created 3 departments mirroring a real enterprise IT structure:
Department                      Purpose                       Handles
IT Support — Level 1            First line helpdesk           Password resets, basic troubleshooting
Network & Infrastructure        Networking team               Connectivity, switches, routers, VPN
Hardware & Systems              Hardware team                 Physical device issues, replacements

Create Help Topics
Navigated to: Admin Panel → Manage → Help Topics → Add New Help Topic

Configure SLA Plans
Navigated to: Admin Panel → Manage → SLA → Add New SLA Plan

Create Agent Accounts
Navigated to: Admin Panel → Agents → Agents → Add New Agent

Create End Users
Navigated to: Agent Panel → Users → Add User

Ticket Lifecycle Management
All tickets were created via the User Portal at localhost/osticket and managed through the Staff Panel at localhost/osticket.

 Password Reset (Priority: High | SLA: 4 Hours)
Submitted by: Rahul Sharma
Help Topic: Password Reset / Account Unlock
Department: IT Support Level 1
Assigned Agent: Shivam Kumar
Issue Description:

"I am unable to login to my computer this morning. I think I forgot my password after the weekend. I have an urgent client meeting in 1 hour and need access immediately."

Troubleshooting Steps Taken:

Verified user identity via employee ID and manager confirmation
Accessed Active Directory Users and Computers on Domain Controller
Located user account — confirmed account was not locked, only password forgotten
Right-clicked user → Reset Password → Set temporary password
Checked "User must change password at next logon"
Communicated temporary password to user via phone call
Confirmed user logged in successfully

Resolution:
User identity verified and domain account password reset in Active Directory. Temporary password issued via phone. User confirmed successful login within 10 minutes. User advised to set a strong memorable password and enable password hint. Ticket resolved within SLA.
Time to Resolve: 12 minutes
Status: ✅ Resolved


What I Learned

How enterprise helpdesk systems like ServiceNow and Zendesk operate at a fundamental level
The importance of SLA management and how it affects business operations and IT team KPIs
How ITIL principles apply to real IT support workflows — ticket categorization, prioritization, escalation, and closure
Why proper ticket documentation is critical — resolution notes become the knowledge base for future issues
How remote support via RDP reduces resolution time by eliminating the need for physical presence
The difference between L1 (basic helpdesk), L2 (technical support), and L3 (specialist) support tiers
How asset management integrates with the helpdesk workflow — tracking hardware changes and software licenses


About Me
B.Tech Computer Science & IT | Google IT Support Professional Certificate
This project is part of my IT Support portfolio demonstrating hands-on experience with enterprise helpdesk tools, ITIL-aligned ticketing workflows, and real-world IT support scenarios.
 
