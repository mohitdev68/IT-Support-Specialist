<img width="1920" height="1080" alt="Screenshot (31)" src="https://github.com/user-attachments/assets/ebed22c7-17ca-4b2c-97cf-20084b246890" />
<img width="4000" height="3000" alt="20260430_125341" src="https://github.com/user-attachments/assets/c9a1e4b6-20da-4b2b-829f-71fdcaecff15" />
<img width="4000" height="3000" alt="20260430_125348" src="https://github.com/user-attachments/assets/b4f2933b-733c-4aa1-a94b-e17fe709227d" />
<img width="1920" height="1080" alt="Screenshot (32)" src="https://github.com/user-attachments/assets/9961741e-8660-4945-b6a5-5b842f49dbd2" />
<img width="1920" height="1080" alt="Screenshot (33)" src="https://github.com/user-attachments/assets/e55b493f-77e9-49cb-9e5d-1e228baa2be8" />
<img width="1920" height="1080" alt="Screenshot (34)" src="https://github.com/user-attachments/assets/8de690eb-32e5-4181-ab9e-56c9805d135d" />
<img width="1920" height="1080" alt="Screenshot (35)" src="https://github.com/user-attachments/assets/409cabbe-9a1d-42de-a7d2-9f464f645b36" />
<img width="1920" height="1080" alt="Screenshot (36)" src="https://github.com/user-attachments/assets/c3e85119-5c2a-4a54-ba62-5a41617dae4b" />

## Project Overview
This project demonstrates hands-on network traffic analysis and troubleshooting using Wireshark — the industry standard packet analyzer used by network engineers and IT support specialists worldwide.
The lab uses two virtual machines (a Windows Server 2019 Domain Controller and a Windows 10 client) connected via a private internal network inside Oracle VirtualBox, with Wireshark installed on the host machine to capture and analyze real network traffic flowing between the VMs.

Why this project matters for IT Support roles:

Network issues are the #1 cause of IT support tickets in enterprise environments
Wireshark is used daily by L2/L3 IT support and network engineers for troubleshooting
Understanding ICMP and DNS at packet level separates good IT support engineers from great ones
Demonstrates practical networking knowledge beyond just theoretical understanding

Tools & Technologies Used
Tool                        Version                    Purpose
Oracle VirtualBox           Latest                     Virtualization platform to run both VMs
Windows Server 2019         Evaluation (180-day)       Domain Controller — DC-01
Windows 10 Pro              ISO                        Client machine — Client-01
Wireshark                   Latest                     Network packet capture and analysis
Npcap                       Built into Wireshark       Packet capture driver for Windows
Windows CMD                 Built-in                   ping, ipconfig, nslookup commands

Step 1 — Create VM 1 — DC-01 (Domain Controller)
Created the first virtual machine in VirtualBox with these specifications

Installation steps:

Downloaded Windows Server 2019 Evaluation ISO (180-day free trial) from Microsoft Evaluation Center
Created VM in VirtualBox with above specifications
Installed Windows Server 2019 Standard Evaluation (Desktop Experience)
Set Administrator password meeting complexity requirements
Renamed server to DC-01 via System Properties
Installed Active Directory Domain Services role via Server Manager
Promoted server to Domain Controller — domain name: mydomain.com

Static IP Configuration on DC-01:
IP Address:      192.168.1.1
Subnet Mask:     255.255.255.0
Default Gateway: (blank — internal network only)
Preferred DNS:   127.0.0.1 (points to itself as DNS server)

Important — Disable extra network adapter:
During setup, DC-01 showed two Ethernet adapters in Network Connections. The extra adapter (X_Internal_X) showing "Media Disconnected" was disabled via:

Press Win+R → type ncpa.cpl → right-click extra adapter → Disable
This ensured only one active adapter with the correct static IP 192.168.1.1

Step 2 — Create VM 2 — Client-01 (Windows 10)
Created the second virtual machine with these specifications

Installation steps:

Downloaded Windows 10 ISO using Microsoft Media Creation Tool (free)
Created VM in VirtualBox with above specifications
Selected Windows 10 Pro during installation (Home does not support domain join)
Chose Domain join instead during OOBE setup
Created local account: LocalUser

Static IP Configuration on Client-01:
IP Address:      192.168.1.10
Subnet Mask:     255.255.255.0
Default Gateway: 192.168.1.1
Preferred DNS:   192.168.1.1 (points to DC-01 as DNS server)

Step 3 — Join Client-01 to Domain

Pressed Win+R → typed sysdm.cpl → System Properties opened
Computer Name tab → clicked Change
Selected Domain → typed: maxtech.local
Entered Domain Administrator credentials when prompted
Received confirmation: "Welcome to the maxtech.local domain" ✅
Restarted Client-01
Logged in as My Domain\Administrator — domain login confirmed ✅

Step 4 — Verify Network Connectivity Between VMs
Connectivity test — ping from Client-01 to DC-01:
On Client-01 CMD:
ping 192.168.1.1
Result:
Pinging 192.168.1.1 with 32 bytes of data:
Reply from 192.168.1.1: bytes=32 time<1ms TTL=128
Reply from 192.168.1.1: bytes=32 time<1ms TTL=128
Reply from 192.168.1.1: bytes=32 time<1ms TTL=128
Reply from 192.168.1.1: bytes=32 time<1ms TTL=128

Ping statistics for 192.168.1.1:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss)
Network connectivity between VMs confirmed ✅

Wireshark Installation
Step 5 — Download and Install Wireshark on Host Machine
Why install on host machine instead of VM:

Host machine has full 8GB RAM available — Wireshark runs smoothly
VMs have only 2GB RAM each — Wireshark would be slow and laggy
Host machine can capture all VM traffic through VirtualBox network adapters
Simpler setup — no need to change VM network adapters for internet access

Installation steps:

Navigated to: wireshark.org/download.html on host machine
Downloaded Windows x64 Installer (~80 MB)
Ran the installer → accepted all defaults
When prompted about Npcap → clicked Install

Npcap is the packet capture driver — required for Wireshark to capture traffic


Installation completed successfully
Opened Wireshark → selected network adapter → confirmed live traffic graph visible ✅


ICMP Traffic (Ping Analysis)
What is ICMP:
ICMP (Internet Control Message Protocol) is the protocol used by the ping command to test network connectivity between devices. It is the first tool used in any network troubleshooting scenario.
Purpose of this capture:
To observe and analyze ICMP Echo Request and Echo Reply packets at the network level — demonstrating how ping works beyond just seeing "replies" in the command prompt.
Wireshark filter used:
icmp
Command run on Client-01:
ping 192.168.1.1 -n 10

DNS Traffic Analysis
What is DNS:
DNS (Domain Name System) is the protocol that translates human-readable domain names into IP addresses. It is often called the "phone book of the internet." DNS issues are responsible for approximately 40% of network connectivity problems in enterprise environments — making it the most important protocol for IT support engineers to understand.
Purpose of this capture:
To observe DNS Query and DNS Response packets — demonstrating exactly how domain name resolution works at the packet level, and what DNS failure looks like in Wireshark.
Wireshark filter used:
dns


What I Learned

How ICMP works at the packet level.
Why DNS is called the most common cause of network failures — and how to identify DNS failure in Wireshark within seconds by looking for unanswered queries.

Related Projects

Active Directory Home Lab — DC-01 and Client-01 VMs were originally built for this project
Helpdesk Ticketing System — osTicket — Ticketing system where network issues like those analyzed here would be logged and resolved



About Me
B.Tech Computer Science & IT | Google IT Support Professional Certificate
This project is part of my IT Support portfolio demonstrating practical network analysis skills using industry standard tools — Wireshark, VirtualBox, and Windows Server — in a hands-on home lab environment.










