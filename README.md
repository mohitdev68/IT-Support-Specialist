# Google IT Support Professional Certificate
<img width="1772" height="928" alt="image" src="https://github.com/user-attachments/assets/4bff871e-998d-4bd7-b0c4-585a569d88a5" />

https://coursera.org/share/d7a76147886eb17da0545a19cf92cdae

The Google IT Support Professional Certificate is a comprehensive, industry-recognized program designed and taught by Google engineers and IT professionals. Completing this program signals to employers that the candidate possesses the practical, job-ready skills required to work as an IT Support Specialist in real enterprise environments.

Courses Completed

Course 1 — Technical Support Fundamentals

The foundation course covering what IT support means in a professional context — from understanding how computers work at the hardware level to supporting users effectively in a corporate environment.
Key topics mastered:

Binary number system and how computers process data
Computer hardware components — CPU, RAM, storage, motherboard, GPU, PSU
How operating systems manage hardware resources
The role of an IT Support Specialist in an organisation
Customer service and communication in IT support contexts
Troubleshooting methodology — identifying, researching, and resolving issues systematically

Practical skills gained:
Learned to approach IT problems using a structured troubleshooting framework — asking the right questions, isolating variables, and documenting solutions — the same methodology used by L1 and L2 support engineers in enterprise helpdesk environments.

Course 2 — The Bits and Bytes of Computer Networking

The most technically intensive course in the program — covering how data moves across networks from physical cables to application layer protocols. This knowledge directly translates to diagnosing and resolving the network issues that make up 40% of all IT support tickets.
Key topics mastered:

The TCP/IP five-layer model and how each layer functions
IP addressing — IPv4, IPv6, subnetting, CIDR notation
DNS (Domain Name System) — how names resolve to IP addresses
DHCP — how devices automatically receive IP configuration
NAT (Network Address Translation) — how private networks access the internet
HTTP, HTTPS, FTP, SMTP, SSH — application layer protocols
VPN — how virtual private networks secure remote connections
Network hardware — routers, switches, hubs, access points
Wireless networking — 802.11 standards, WPA2, WPA3 security
Network troubleshooting — ping, traceroute, nslookup, netstat

Practical skills gained:
Can diagnose network connectivity issues by systematically checking physical layer, IP configuration, DNS resolution, and gateway connectivity — the exact troubleshooting path used in real helpdesk environments. Supplemented this course with hands-on Wireshark packet analysis in home lab — capturing and analyzing ICMP and DNS traffic at the packet level.

Course 3 — Operating Systems and You — Becoming a Power User

Deep dive into the two operating systems that dominate enterprise IT environments — Windows and Linux. An IT support specialist who cannot navigate both operating systems confidently cannot function effectively in a modern workplace.
Key topics mastered:
Windows:

Windows file system — NTFS, FAT32, directory structure
Windows Registry — understanding and safely editing registry keys
Process management — Task Manager, services, startup programs
User and group management — Local Users and Groups
Active Directory integration — domain accounts, group policies
Windows command line — ipconfig, ping, netstat, sfc, chkdsk, robocopy
PowerShell — automation and system administration scripts
Remote Desktop Protocol (RDP) — remote support and administration
Windows troubleshooting — Event Viewer, Device Manager, System Restore

Linux:

Linux file system hierarchy — /etc, /var, /home, /bin, /usr
Essential Linux commands — ls, cd, chmod, chown, grep, find, ps, top, kill
File permissions — read, write, execute for user, group, others
Package management — apt, yum for installing and updating software
User management — useradd, usermod, passwd, sudo
SSH — secure remote access to Linux systems
Log files — /var/log for troubleshooting system issues
Bash scripting basics — automating repetitive IT tasks

Practical skills gained:
Comfortable administering both Windows and Linux systems from command line and GUI — critical for supporting mixed enterprise environments. Built hands-on experience through Active Directory home lab running Windows Server 2019 and Windows 10 in VirtualBox.

Course 4 — System Administration and IT Infrastructure Services

The transition from individual machine support to managing infrastructure for an entire organisation. This course covers the skills needed to step from L1 helpdesk into L2 system administration — where career growth and salary increases happen.
Key topics mastered:
Directory Services:

Active Directory — users, groups, organisational units, group policies
LDAP — Lightweight Directory Access Protocol
Single Sign-On (SSO) — how enterprise authentication works
User lifecycle management — onboarding, access provisioning, offboarding

Cloud Computing:

Cloud deployment models — Public, Private, Hybrid
Cloud service models — IaaS, PaaS, SaaS
Major cloud providers — AWS, Microsoft Azure, Google Cloud Platform
Cloud storage — object storage, block storage, file storage
Cloud vs on-premise — when to use each and cost considerations
Office 365 and Google Workspace administration basics

IT Infrastructure:

DHCP server configuration and management
DNS server setup and record types — A, AAAA, CNAME, MX, PTR
File servers and shared folder permissions
Print server management
Backup strategies — 3-2-1 backup rule, full vs incremental backup
Disaster recovery — RTO (Recovery Time Objective), RPO (Recovery Point Objective)
Ticketing systems — ticket lifecycle, SLA management, escalation procedures

Practical skills gained:
Deployed a fully functional Active Directory home lab — created domain controller, configured users and groups, implemented group policies, and joined client machines to the domain. Also deployed osTicket helpdesk system simulating enterprise SLA management and ticket workflows.

Course 5 — IT Security — Defense Against the Digital Dark Arts

The most critical course for the modern IT support landscape — cybersecurity threats are the fastest growing challenge facing IT teams in every organisation regardless of size or industry. This course transforms an IT support specialist from someone who just fixes computers into someone who actively protects the organisation.
Key topics mastered:
Threat Landscape:

Types of malware — viruses, worms, trojans, ransomware, spyware, adware, rootkits
Social engineering attacks — phishing, spear phishing, vishing, pretexting
Man-in-the-middle attacks — how attackers intercept communications
Denial of Service (DoS) and Distributed DoS (DDoS) attacks
SQL injection and cross-site scripting — web application vulnerabilities
Password attacks — brute force, dictionary attacks, credential stuffing

Security Controls:

CIA Triad — Confidentiality, Integrity, Availability
Defence in depth — layered security approach
Principle of least privilege — minimum access required
Antivirus and endpoint protection — how detection works
Firewall types — packet filtering, stateful inspection, application layer
Intrusion Detection Systems (IDS) and Intrusion Prevention Systems (IPS)
Encryption — symmetric vs asymmetric, TLS/SSL, HTTPS, VPN tunnels
Multi-factor authentication (MFA) — TOTP, hardware tokens, biometrics
Public Key Infrastructure (PKI) — certificates, certificate authorities

Security Policies and Compliance:

Password policies — complexity, expiry, lockout thresholds
Acceptable Use Policy (AUP)
Data classification — public, internal, confidential, restricted
Incident response — identify, contain, eradicate, recover, lessons learned
Security awareness training — how to train users to recognise threats

Practical skills gained:
Conducted a full Windows 11 Security Audit covering Windows Defender status, firewall rule analysis, user account permission review, password policy assessment, and patch management review using built-in Windows tools and PowerShell — documented findings with risk ratings and remediation recommendations in a formal IT Security Audit Report.

Hands-On Labs Completed
Beyond the Coursera curriculum — built a complete home lab environment to reinforce every concept with real hands-on practice:

Lab 1 — Active Directory Environment
Built enterprise-style AD lab with Windows Server 2019 Domain Controller and Windows 10 client machine in VirtualBox. Performed real IT support tasks — user creation, password resets, account unlocks, group policy configuration, and remote desktop support.

View Project https://github.com/mohitdev68/IT-Support-Specialist/tree/b3044cdbbccfea553c4c3e514624ef1a3aeb937d/Active%20Directory%20Home%20Lab

Lab 2 — Helpdesk Ticketing System
Deployed and configured osTicket helpdesk system using XAMPP. Set up departments, SLA plans, and agent accounts. Created and resolved 5 realistic IT support tickets covering the most common enterprise helpdesk scenarios.

View Project https://github.com/mohitdev68/IT-Support-Specialist/tree/b3044cdbbccfea553c4c3e514624ef1a3aeb937d/Helpdesk-Ticketing-os.Ticket

Lab 3 — Network Traffic Analysis
Used Wireshark to capture and analyze ICMP and DNS protocol traffic in a live VirtualBox network environment. Simulated DNS failure and diagnosed using systematic troubleshooting — nslookup, ipconfig /flushdns, and packet-level analysis.

View Project https://github.com/mohitdev68/IT-Support-Specialist/tree/b3044cdbbccfea553c4c3e514624ef1a3aeb937d/Network%20Home%20Lab%20%2B%20Wireshark%20Traffic%20Analysis

Lab 4 — Windows Security Audit
Conducted a complete Windows 11 security audit covering 5 domains — antivirus, firewall, user permissions, password policies, and patch management. Documented findings with risk ratings and remediation recommendations in a formal security audit report.

View Project https://github.com/mohitdev68/IT-Support-Specialist/tree/b3044cdbbccfea553c4c3e514624ef1a3aeb937d/IT%20Security%20Audit%20%2B%20Report

I did not just study these topics — I built labs, ran commands, captured packets, created users, resolved tickets, and wrote audit reports. The projects on this GitHub profile are the evidence.

About Me
I am a B.Tech Computer Science and IT graduate with a genuine passion for IT infrastructure, networking, and helping users solve technical problems efficiently.I am not someone who just passed an online course. I built virtual machines, configured domain controllers, deployed helpdesk systems, captured network packets with Wireshark, and wrote formal security audit reports. Every project on this GitHub profile represents real hours of hands-on work — not just certificate collection.I am actively seeking an IT Support Engineer / Technical Support Specialist role  where I can contribute immediately, grow technically, and become a reliable member of an IT team.

What I bring to your team:

Solid foundation in Windows and Linux system administration
Practical networking knowledge — TCP/IP, DNS, DHCP, VPN, Wireshark
Active Directory experience — user management, group policies, domain administration
Helpdesk workflow knowledge — ticketing, SLA management, escalation
Security mindset — threat awareness, audit skills, policy compliance
Strong troubleshooting approach — systematic, documented, and user-focused
Fast learner — CompTIA A+ already in progress

Linkedin Profile
www.linkedin.com/in/mohit-chandel-67b255191
